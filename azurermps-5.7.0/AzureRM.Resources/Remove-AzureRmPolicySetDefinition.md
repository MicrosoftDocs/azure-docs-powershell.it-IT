---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicySetDefinition.md
ms.openlocfilehash: fa96d686d66f9ef94322896974dc4dd3b81ad154
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518003"
---
# <span data-ttu-id="59d57-101">Remove-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="59d57-101">Remove-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="59d57-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="59d57-102">SYNOPSIS</span></span>
<span data-ttu-id="59d57-103">Rimuove una definizione di set di criteri.</span><span class="sxs-lookup"><span data-stu-id="59d57-103">Removes a policy set definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59d57-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="59d57-104">SYNTAX</span></span>

### <span data-ttu-id="59d57-105">RemoveByNameAndResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="59d57-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzureRmPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59d57-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="59d57-106">RemoveById</span></span>
```
Remove-AzureRmPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59d57-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59d57-107">DESCRIPTION</span></span>
<span data-ttu-id="59d57-108">Il cmdlet **Remove-AzureRmPolicySetDefinition** rimuove una definizione di criteri.</span><span class="sxs-lookup"><span data-stu-id="59d57-108">The **Remove-AzureRmPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="59d57-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="59d57-109">EXAMPLES</span></span>

### <span data-ttu-id="59d57-110">Esempio 1: rimuovere la definizione del set di criteri in base all'ID risorsa</span><span class="sxs-lookup"><span data-stu-id="59d57-110">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\>$PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId "/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition"
PS C:\>Remove-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="59d57-111">Il primo comando ottiene una definizione di set di criteri usando il cmdlet Get-AzureRmPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="59d57-111">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="59d57-112">Il comando lo archivia nella variabile $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="59d57-112">The command stores it in the $PolicySetDefinition variable.</span></span>

<span data-ttu-id="59d57-113">Il secondo comando rimuove la definizione del set di criteri identificata dalla proprietà **resourceId** di $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="59d57-113">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="59d57-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="59d57-114">PARAMETERS</span></span>

### <span data-ttu-id="59d57-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="59d57-115">-ApiVersion</span></span>
<span data-ttu-id="59d57-116">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="59d57-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="59d57-117">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="59d57-117">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59d57-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59d57-118">-DefaultProfile</span></span>
<span data-ttu-id="59d57-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="59d57-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59d57-120">-Force</span><span class="sxs-lookup"><span data-stu-id="59d57-120">-Force</span></span>
<span data-ttu-id="59d57-121">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="59d57-121">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59d57-122">-ID</span><span class="sxs-lookup"><span data-stu-id="59d57-122">-Id</span></span>
<span data-ttu-id="59d57-123">ID di definizione del set di criteri completo, incluso l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="59d57-123">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="59d57-124">ad esempio/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="59d57-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: RemoveById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59d57-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="59d57-125">-Name</span></span>
<span data-ttu-id="59d57-126">Nome della definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="59d57-126">The policy set definition name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59d57-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="59d57-127">-Pre</span></span>
<span data-ttu-id="59d57-128">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="59d57-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59d57-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="59d57-129">-Confirm</span></span>
<span data-ttu-id="59d57-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59d57-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59d57-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59d57-131">-WhatIf</span></span>
<span data-ttu-id="59d57-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="59d57-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59d57-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="59d57-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59d57-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59d57-134">CommonParameters</span></span>
<span data-ttu-id="59d57-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59d57-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59d57-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59d57-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59d57-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="59d57-137">INPUTS</span></span>

### <span data-ttu-id="59d57-138">System. String</span><span class="sxs-lookup"><span data-stu-id="59d57-138">System.String</span></span>

## <span data-ttu-id="59d57-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="59d57-139">OUTPUTS</span></span>

### <span data-ttu-id="59d57-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="59d57-140">System.Boolean</span></span>

## <span data-ttu-id="59d57-141">Note</span><span class="sxs-lookup"><span data-stu-id="59d57-141">NOTES</span></span>

## <span data-ttu-id="59d57-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="59d57-142">RELATED LINKS</span></span>
