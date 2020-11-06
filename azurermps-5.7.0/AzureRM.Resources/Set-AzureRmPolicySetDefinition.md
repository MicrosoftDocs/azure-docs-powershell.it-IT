---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
ms.openlocfilehash: 16a27c7756a25c4b8e4270a0c363f8a04528d12c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507979"
---
# <span data-ttu-id="2a58f-101">Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="2a58f-101">Set-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="2a58f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2a58f-102">SYNOPSIS</span></span>
<span data-ttu-id="2a58f-103">Modifica di una definizione di set di criteri</span><span class="sxs-lookup"><span data-stu-id="2a58f-103">Modifies a policy set definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a58f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2a58f-104">SYNTAX</span></span>

### <span data-ttu-id="2a58f-105">SetByNameAndResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2a58f-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a58f-106">SetById</span><span class="sxs-lookup"><span data-stu-id="2a58f-106">SetById</span></span>
```
Set-AzureRmPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a58f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2a58f-107">DESCRIPTION</span></span>
<span data-ttu-id="2a58f-108">Il cmdlet **set-AzureRmPolicySetDefinition** modifica una definizione di criteri.</span><span class="sxs-lookup"><span data-stu-id="2a58f-108">The **Set-AzureRmPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="2a58f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2a58f-109">EXAMPLES</span></span>

### <span data-ttu-id="2a58f-110">Esempio 1: aggiornare la descrizione di una definizione di set di criteri</span><span class="sxs-lookup"><span data-stu-id="2a58f-110">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\>$PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId "/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition"
PS C:\> Set-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description "Updated policy to not allow virtual machine creation"
```

<span data-ttu-id="2a58f-111">Il primo comando ottiene una definizione di set di criteri usando il cmdlet Get-AzureRmPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="2a58f-111">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="2a58f-112">Il comando Archivia l'oggetto nella variabile $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="2a58f-112">The command stores that object in the $PolicySetDefinition variable.</span></span>

<span data-ttu-id="2a58f-113">Il secondo comando Aggiorna la descrizione della definizione del set di criteri identificata dalla proprietà **resourceId** di $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="2a58f-113">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="2a58f-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2a58f-114">PARAMETERS</span></span>

### <span data-ttu-id="2a58f-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2a58f-115">-ApiVersion</span></span>
<span data-ttu-id="2a58f-116">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="2a58f-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="2a58f-117">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="2a58f-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="2a58f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a58f-118">-DefaultProfile</span></span>
<span data-ttu-id="2a58f-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="2a58f-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2a58f-120">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="2a58f-120">-Description</span></span>
<span data-ttu-id="2a58f-121">Descrizione della definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="2a58f-121">The description for policy set definition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a58f-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2a58f-122">-DisplayName</span></span>
<span data-ttu-id="2a58f-123">Nome visualizzato per la definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="2a58f-123">The display name for policy set definition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a58f-124">-ID</span><span class="sxs-lookup"><span data-stu-id="2a58f-124">-Id</span></span>
<span data-ttu-id="2a58f-125">ID di definizione dei criteri completo, incluso l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="2a58f-125">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="2a58f-126">ad esempio/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="2a58f-126">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: SetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a58f-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="2a58f-127">-Name</span></span>
<span data-ttu-id="2a58f-128">Nome della definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="2a58f-128">The policy set definition name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a58f-129">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="2a58f-129">-PolicyDefinition</span></span>
<span data-ttu-id="2a58f-130">Definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="2a58f-130">The policy set definition.</span></span> <span data-ttu-id="2a58f-131">Può trattarsi di un percorso di un nome di file contenente le definizioni dei criteri oppure la definizione del set di criteri come stringa.</span><span class="sxs-lookup"><span data-stu-id="2a58f-131">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a58f-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="2a58f-132">-Pre</span></span>
<span data-ttu-id="2a58f-133">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="2a58f-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="2a58f-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2a58f-134">-Confirm</span></span>
<span data-ttu-id="2a58f-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a58f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a58f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a58f-136">-WhatIf</span></span>
<span data-ttu-id="2a58f-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2a58f-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2a58f-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2a58f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a58f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a58f-139">CommonParameters</span></span>
<span data-ttu-id="2a58f-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a58f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a58f-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a58f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a58f-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2a58f-142">INPUTS</span></span>

### <span data-ttu-id="2a58f-143">System. String</span><span class="sxs-lookup"><span data-stu-id="2a58f-143">System.String</span></span>

## <span data-ttu-id="2a58f-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2a58f-144">OUTPUTS</span></span>

### <span data-ttu-id="2a58f-145">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="2a58f-145">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="2a58f-146">Note</span><span class="sxs-lookup"><span data-stu-id="2a58f-146">NOTES</span></span>

## <span data-ttu-id="2a58f-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2a58f-147">RELATED LINKS</span></span>
