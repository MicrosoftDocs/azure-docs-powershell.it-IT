---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
ms.openlocfilehash: 3174f56a0488b196dc3dc330cfa6435def73476c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677294"
---
# <span data-ttu-id="18639-101">Remove-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="18639-101">Remove-AzPolicySetDefinition</span></span>

## <span data-ttu-id="18639-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="18639-102">SYNOPSIS</span></span>
<span data-ttu-id="18639-103">Rimuove una definizione di set di criteri.</span><span class="sxs-lookup"><span data-stu-id="18639-103">Removes a policy set definition.</span></span>

## <span data-ttu-id="18639-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="18639-104">SYNTAX</span></span>

### <span data-ttu-id="18639-105">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="18639-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18639-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="18639-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -ManagementGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18639-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="18639-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18639-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="18639-108">IdParameterSet</span></span>
```
Remove-AzPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18639-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18639-109">DESCRIPTION</span></span>
<span data-ttu-id="18639-110">Il cmdlet **Remove-AzPolicySetDefinition** rimuove una definizione di criteri.</span><span class="sxs-lookup"><span data-stu-id="18639-110">The **Remove-AzPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="18639-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="18639-111">EXAMPLES</span></span>

### <span data-ttu-id="18639-112">Esempio 1: rimuovere la definizione del set di criteri in base all'ID risorsa</span><span class="sxs-lookup"><span data-stu-id="18639-112">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Remove-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="18639-113">Il primo comando ottiene una definizione di set di criteri usando il cmdlet Get-AzPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="18639-113">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="18639-114">Il comando lo archivia nella variabile $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="18639-114">The command stores it in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="18639-115">Il secondo comando rimuove la definizione del set di criteri identificata dalla proprietà **resourceId** di $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="18639-115">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="18639-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="18639-116">PARAMETERS</span></span>

### <span data-ttu-id="18639-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="18639-117">-ApiVersion</span></span>
<span data-ttu-id="18639-118">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="18639-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="18639-119">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="18639-119">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="18639-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18639-120">-DefaultProfile</span></span>
<span data-ttu-id="18639-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="18639-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18639-122">-Force</span><span class="sxs-lookup"><span data-stu-id="18639-122">-Force</span></span>
<span data-ttu-id="18639-123">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="18639-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="18639-124">-ID</span><span class="sxs-lookup"><span data-stu-id="18639-124">-Id</span></span>
<span data-ttu-id="18639-125">ID di definizione del set di criteri completo, incluso l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="18639-125">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="18639-126">ad esempio/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="18639-126">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18639-127">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="18639-127">-ManagementGroupName</span></span>
<span data-ttu-id="18639-128">Nome del gruppo di gestione della definizione del set di criteri da eliminare.</span><span class="sxs-lookup"><span data-stu-id="18639-128">The name of the management group of the policy set definition to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18639-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="18639-129">-Name</span></span>
<span data-ttu-id="18639-130">Nome della definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="18639-130">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18639-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="18639-131">-Pre</span></span>
<span data-ttu-id="18639-132">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="18639-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="18639-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="18639-133">-SubscriptionId</span></span>
<span data-ttu-id="18639-134">ID sottoscrizione della definizione del set di criteri da eliminare.</span><span class="sxs-lookup"><span data-stu-id="18639-134">The subscription ID of the policy set definition to delete.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18639-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="18639-135">-Confirm</span></span>
<span data-ttu-id="18639-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18639-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18639-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18639-137">-WhatIf</span></span>
<span data-ttu-id="18639-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="18639-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18639-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="18639-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18639-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18639-140">CommonParameters</span></span>
<span data-ttu-id="18639-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18639-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18639-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18639-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18639-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="18639-143">INPUTS</span></span>

### <span data-ttu-id="18639-144">System. String</span><span class="sxs-lookup"><span data-stu-id="18639-144">System.String</span></span>

### <span data-ttu-id="18639-145">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="18639-145">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="18639-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="18639-146">OUTPUTS</span></span>

### <span data-ttu-id="18639-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="18639-147">System.Boolean</span></span>

## <span data-ttu-id="18639-148">Note</span><span class="sxs-lookup"><span data-stu-id="18639-148">NOTES</span></span>

## <span data-ttu-id="18639-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="18639-149">RELATED LINKS</span></span>
