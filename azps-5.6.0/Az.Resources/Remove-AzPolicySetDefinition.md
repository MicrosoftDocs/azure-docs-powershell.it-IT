---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
ms.openlocfilehash: e4f9164e9cfcb84ed9b8fb2051a732886ca74819
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988901"
---
# <span data-ttu-id="df569-101">Remove-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="df569-101">Remove-AzPolicySetDefinition</span></span>

## <span data-ttu-id="df569-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df569-102">SYNOPSIS</span></span>
<span data-ttu-id="df569-103">Rimuove la definizione di un set di criteri.</span><span class="sxs-lookup"><span data-stu-id="df569-103">Removes a policy set definition.</span></span>

## <span data-ttu-id="df569-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="df569-104">SYNTAX</span></span>

### <span data-ttu-id="df569-105">NameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="df569-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df569-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="df569-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -ManagementGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df569-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="df569-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df569-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="df569-108">IdParameterSet</span></span>
```
Remove-AzPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df569-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="df569-109">InputObjectParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Force] -InputObject <PsPolicySetDefinition> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df569-110">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="df569-110">DESCRIPTION</span></span>
<span data-ttu-id="df569-111">Il cmdlet **Remove-AzPolicySetDefinition** rimuove una definizione di criterio.</span><span class="sxs-lookup"><span data-stu-id="df569-111">The **Remove-AzPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="df569-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="df569-112">EXAMPLES</span></span>

### <span data-ttu-id="df569-113">Esempio 1: Rimuovere la definizione del set di criteri in base all'ID risorsa</span><span class="sxs-lookup"><span data-stu-id="df569-113">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Remove-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="df569-114">Il primo comando ottiene la definizione di un set di criteri usando il cmdlet Get-AzPolicySetDefinition criteri.</span><span class="sxs-lookup"><span data-stu-id="df569-114">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="df569-115">Il comando lo archivia nella $PolicySetDefinition variabile.</span><span class="sxs-lookup"><span data-stu-id="df569-115">The command stores it in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="df569-116">Il secondo comando rimuove la definizione del set di criteri identificata dalla **proprietà ResourceId** di $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="df569-116">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="df569-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df569-117">PARAMETERS</span></span>

### <span data-ttu-id="df569-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="df569-118">-ApiVersion</span></span>
<span data-ttu-id="df569-119">Se impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="df569-119">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="df569-120">Se non viene specificato, la versione dell'API viene automaticamente determinata come la più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="df569-120">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="df569-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df569-121">-DefaultProfile</span></span>
<span data-ttu-id="df569-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="df569-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df569-123">-Force</span><span class="sxs-lookup"><span data-stu-id="df569-123">-Force</span></span>
<span data-ttu-id="df569-124">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="df569-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="df569-125">-Id</span><span class="sxs-lookup"><span data-stu-id="df569-125">-Id</span></span>
<span data-ttu-id="df569-126">ID di definizione del set di criteri completo, inclusa la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="df569-126">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="df569-127">ad esempio /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="df569-127">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="df569-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df569-128">-InputObject</span></span>
<span data-ttu-id="df569-129">Oggetto definizione del set di criteri per rimuovere l'output da un altro cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df569-129">The policy set definition object to remove that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicySetDefinition
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df569-130">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="df569-130">-ManagementGroupName</span></span>
<span data-ttu-id="df569-131">Nome del gruppo di gestione della definizione del set di criteri da eliminare.</span><span class="sxs-lookup"><span data-stu-id="df569-131">The name of the management group of the policy set definition to delete.</span></span>

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

### <span data-ttu-id="df569-132">-Name</span><span class="sxs-lookup"><span data-stu-id="df569-132">-Name</span></span>
<span data-ttu-id="df569-133">Nome della definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="df569-133">The policy set definition name.</span></span>

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

### <span data-ttu-id="df569-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="df569-134">-Pre</span></span>
<span data-ttu-id="df569-135">Se impostato, indica che il cmdlet deve usare versioni delle API non beta per determinare automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="df569-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="df569-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="df569-136">-SubscriptionId</span></span>
<span data-ttu-id="df569-137">ID sottoscrizione della definizione del set di criteri da eliminare.</span><span class="sxs-lookup"><span data-stu-id="df569-137">The subscription ID of the policy set definition to delete.</span></span>

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

### <span data-ttu-id="df569-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df569-138">-Confirm</span></span>
<span data-ttu-id="df569-139">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df569-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df569-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df569-140">-WhatIf</span></span>
<span data-ttu-id="df569-141">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="df569-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df569-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="df569-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df569-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df569-143">CommonParameters</span></span>
<span data-ttu-id="df569-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df569-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df569-145">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="df569-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df569-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="df569-146">INPUTS</span></span>

### <span data-ttu-id="df569-147">System.String</span><span class="sxs-lookup"><span data-stu-id="df569-147">System.String</span></span>

### <span data-ttu-id="df569-148">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="df569-148">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="df569-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="df569-149">OUTPUTS</span></span>

### <span data-ttu-id="df569-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="df569-150">System.Boolean</span></span>

## <span data-ttu-id="df569-151">NOTE</span><span class="sxs-lookup"><span data-stu-id="df569-151">NOTES</span></span>

## <span data-ttu-id="df569-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="df569-152">RELATED LINKS</span></span>
