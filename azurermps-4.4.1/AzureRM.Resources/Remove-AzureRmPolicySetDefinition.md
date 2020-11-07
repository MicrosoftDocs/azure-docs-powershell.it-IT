---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicySetDefinition.md
ms.openlocfilehash: d3b9d8af81f08786536abf0d26b3c4ba2f2d66bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686788"
---
# <span data-ttu-id="d6cca-101">Remove-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="d6cca-101">Remove-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="d6cca-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d6cca-102">SYNOPSIS</span></span>
<span data-ttu-id="d6cca-103">Rimuove una definizione di set di criteri.</span><span class="sxs-lookup"><span data-stu-id="d6cca-103">Removes a policy set definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6cca-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d6cca-104">SYNTAX</span></span>

### <span data-ttu-id="d6cca-105">Set di parametri del nome della definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="d6cca-105">The policy set definition name parameter set.</span></span> <span data-ttu-id="d6cca-106">Predefinita</span><span class="sxs-lookup"><span data-stu-id="d6cca-106">(Default)</span></span>
```
Remove-AzureRmPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6cca-107">Set di parametri ID definizione set di criteri.</span><span class="sxs-lookup"><span data-stu-id="d6cca-107">The policy set definition Id parameter set.</span></span>
```
Remove-AzureRmPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6cca-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d6cca-108">DESCRIPTION</span></span>
<span data-ttu-id="d6cca-109">Il cmdlet **Remove-AzureRmPolicySetDefinition** rimuove una definizione di criteri.</span><span class="sxs-lookup"><span data-stu-id="d6cca-109">The **Remove-AzureRmPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="d6cca-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d6cca-110">EXAMPLES</span></span>

### <span data-ttu-id="d6cca-111">Esempio 1: rimuovere la definizione del set di criteri in base all'ID risorsa</span><span class="sxs-lookup"><span data-stu-id="d6cca-111">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\>$PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId "/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition"
PS C:\>Remove-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="d6cca-112">Il primo comando ottiene una definizione di set di criteri usando il cmdlet Get-AzureRmPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="d6cca-112">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="d6cca-113">Il comando lo archivia nella variabile $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="d6cca-113">The command stores it in the $PolicySetDefinition variable.</span></span>

<span data-ttu-id="d6cca-114">Il secondo comando rimuove la definizione del set di criteri identificata dalla proprietà **resourceId** di $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="d6cca-114">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="d6cca-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d6cca-115">PARAMETERS</span></span>

### <span data-ttu-id="d6cca-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d6cca-116">-ApiVersion</span></span>
<span data-ttu-id="d6cca-117">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="d6cca-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="d6cca-118">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="d6cca-118">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6cca-119">-Force</span><span class="sxs-lookup"><span data-stu-id="d6cca-119">-Force</span></span>
<span data-ttu-id="d6cca-120">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="d6cca-120">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6cca-121">-ID</span><span class="sxs-lookup"><span data-stu-id="d6cca-121">-Id</span></span>
<span data-ttu-id="d6cca-122">ID di definizione del set di criteri completo, incluso l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="d6cca-122">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="d6cca-123">ad esempio/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="d6cca-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The policy set definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6cca-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="d6cca-124">-Name</span></span>
<span data-ttu-id="d6cca-125">Nome della definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="d6cca-125">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy set definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6cca-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="d6cca-126">-Pre</span></span>
<span data-ttu-id="d6cca-127">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="d6cca-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6cca-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d6cca-128">-Confirm</span></span>
<span data-ttu-id="d6cca-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6cca-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6cca-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6cca-130">-WhatIf</span></span>
<span data-ttu-id="d6cca-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d6cca-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6cca-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d6cca-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6cca-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6cca-133">-DefaultProfile</span></span>
<span data-ttu-id="d6cca-134">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d6cca-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6cca-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6cca-135">CommonParameters</span></span>
<span data-ttu-id="d6cca-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6cca-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6cca-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6cca-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6cca-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d6cca-138">INPUTS</span></span>

### <span data-ttu-id="d6cca-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d6cca-139">System.String</span></span>

## <span data-ttu-id="d6cca-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d6cca-140">OUTPUTS</span></span>

### <span data-ttu-id="d6cca-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d6cca-141">System.Boolean</span></span>

## <span data-ttu-id="d6cca-142">Note</span><span class="sxs-lookup"><span data-stu-id="d6cca-142">NOTES</span></span>

## <span data-ttu-id="d6cca-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d6cca-143">RELATED LINKS</span></span>

