---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/set-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
ms.openlocfilehash: fab07b94c565a37d2884c5074de9f23692878df4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011741"
---
# <span data-ttu-id="c3b16-101">Set-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="c3b16-101">Set-AzPolicySetDefinition</span></span>

## <span data-ttu-id="c3b16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3b16-102">SYNOPSIS</span></span>
<span data-ttu-id="c3b16-103">Modifica la definizione di un set di criteri</span><span class="sxs-lookup"><span data-stu-id="c3b16-103">Modifies a policy set definition</span></span>

## <span data-ttu-id="c3b16-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c3b16-104">SYNTAX</span></span>

### <span data-ttu-id="c3b16-105">NameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="c3b16-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c3b16-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3b16-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -ManagementGroupName <String>
 [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3b16-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3b16-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -SubscriptionId <Guid>
 [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3b16-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3b16-108">IdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c3b16-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3b16-109">InputObjectParameterSet</span></span>
```
Set-AzPolicySetDefinition [-DisplayName <String>] [-Description <String>] [-PolicyDefinition <String>]
 [-Metadata <String>] [-Parameter <String>] -InputObject <PsPolicySetDefinition> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c3b16-110">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c3b16-110">DESCRIPTION</span></span>
<span data-ttu-id="c3b16-111">Il cmdlet **Set-AzPolicySetDefinition** modifica una definizione di criterio.</span><span class="sxs-lookup"><span data-stu-id="c3b16-111">The **Set-AzPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="c3b16-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c3b16-112">EXAMPLES</span></span>

### <span data-ttu-id="c3b16-113">Esempio 1: Aggiornare la descrizione di una definizione del set di criteri</span><span class="sxs-lookup"><span data-stu-id="c3b16-113">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Set-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="c3b16-114">Il primo comando ottiene la definizione di un set di criteri usando il cmdlet Get-AzPolicySetDefinition criteri.</span><span class="sxs-lookup"><span data-stu-id="c3b16-114">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="c3b16-115">Il comando archivia l'oggetto nella $PolicySetDefinition variabile.</span><span class="sxs-lookup"><span data-stu-id="c3b16-115">The command stores that object in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="c3b16-116">Il secondo comando aggiorna la descrizione della definizione del set di criteri identificata dalla **proprietà ResourceId** di $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="c3b16-116">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

### <span data-ttu-id="c3b16-117">Esempio 2: Aggiornare i metadati di una definizione di set di criteri</span><span class="sxs-lookup"><span data-stu-id="c3b16-117">Example 2: Update the metadata of a policy set definition</span></span>
```
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -Metadata '{"category":"Virtual Machine"}'


Name                  : VMPolicySetDefinition
ResourceId            : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policySetDefinitions/VMPolicySetDefinition
ResourceName          : VMPolicySetDefinition
ResourceType          : Microsoft.Authorization/policySetDefinitions
SubscriptionId        : 11111111-1111-1111-1111-111111111111
Properties            : @{displayName=VMPolicySetDefinition; policyType=Custom; metadata=; parameters=; policyDefinitions=System.Object[]}
PolicySetDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policySetDefinitions/VMPolicySetDefinition
```

<span data-ttu-id="c3b16-118">Questo comando aggiorna i metadati di una definizione del set di criteri denominata VMPolicySetDefinition per indicare che la categoria è "Macchina virtuale".</span><span class="sxs-lookup"><span data-stu-id="c3b16-118">This command updates the metadata of a policy set definition named VMPolicySetDefinition to indicate its category is "Virtual Machine".</span></span>

### <span data-ttu-id="c3b16-119">Esempio 3: Aggiornare i gruppi di una definizione di set di criteri</span><span class="sxs-lookup"><span data-stu-id="c3b16-119">Example 3: Update the groups of a policy set definition</span></span>
```
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition '[{ "name": "group1", "displayName": "Virtual Machine Security" }, { "name": "group2" }]'
```

<span data-ttu-id="c3b16-120">Questo comando aggiorna i gruppi di una definizione di set di criteri denominata VMPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="c3b16-120">This command updates the groups of a policy set definition named VMPolicySetDefinition.</span></span>

### <span data-ttu-id="c3b16-121">Esempio 4: Aggiornare i gruppi di una definizione di set di criteri usando una tabella hash</span><span class="sxs-lookup"><span data-stu-id="c3b16-121">Example 4: Update the groups of a policy set definition using a hash table</span></span>
```
$groupsJson = ConvertTo-Json @{ name = "group1", displayName = "Virtual Machine Security" }, @{ name = "group2" }
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition $groupsJson
```

<span data-ttu-id="c3b16-122">Questo comando aggiorna i gruppi di una definizione di set di criteri denominata VMPolicySetDefinition usando una tabella hash per creare i gruppi.</span><span class="sxs-lookup"><span data-stu-id="c3b16-122">This command updates the groups of a policy set definition named VMPolicySetDefinition using a hash table to construct the groups.</span></span>

## <span data-ttu-id="c3b16-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3b16-123">PARAMETERS</span></span>

### <span data-ttu-id="c3b16-124">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c3b16-124">-ApiVersion</span></span>
<span data-ttu-id="c3b16-125">Se impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="c3b16-125">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="c3b16-126">Se non viene specificato, la versione dell'API viene automaticamente determinata come la più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="c3b16-126">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="c3b16-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3b16-127">-DefaultProfile</span></span>
<span data-ttu-id="c3b16-128">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c3b16-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c3b16-129">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="c3b16-129">-Description</span></span>
<span data-ttu-id="c3b16-130">Descrizione della definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="c3b16-130">The description for policy set definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3b16-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c3b16-131">-DisplayName</span></span>
<span data-ttu-id="c3b16-132">Nome visualizzato per la definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="c3b16-132">The display name for policy set definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3b16-133">-GroupDefinition</span><span class="sxs-lookup"><span data-stu-id="c3b16-133">-GroupDefinition</span></span>
<span data-ttu-id="c3b16-134">Gruppi di definizione dei criteri della definizione del set di criteri aggiornata.</span><span class="sxs-lookup"><span data-stu-id="c3b16-134">The policy definition groups of the updated policy set definition.</span></span> <span data-ttu-id="c3b16-135">Può trattarsi del percorso di un file contenente i gruppi o dei gruppi come stringa JSON.</span><span class="sxs-lookup"><span data-stu-id="c3b16-135">This can either be a path to a file containing the groups, or the groups as a JSON string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3b16-136">-Id</span><span class="sxs-lookup"><span data-stu-id="c3b16-136">-Id</span></span>
<span data-ttu-id="c3b16-137">ID di definizione dei criteri completo, inclusa la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="c3b16-137">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="c3b16-138">ad esempio /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="c3b16-138">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="c3b16-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3b16-139">-InputObject</span></span>
<span data-ttu-id="c3b16-140">Oggetto definizione del set di criteri da aggiornare che è stato generato da un altro cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3b16-140">The policy set definition object to update that was output from another cmdlet.</span></span>

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

### <span data-ttu-id="c3b16-141">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="c3b16-141">-ManagementGroupName</span></span>
<span data-ttu-id="c3b16-142">Nome del gruppo di gestione della definizione del set di criteri da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="c3b16-142">The name of the management group of the policy set definition to update.</span></span>

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

### <span data-ttu-id="c3b16-143">-Metadata</span><span class="sxs-lookup"><span data-stu-id="c3b16-143">-Metadata</span></span>
<span data-ttu-id="c3b16-144">Metadati della definizione del set di criteri aggiornata.</span><span class="sxs-lookup"><span data-stu-id="c3b16-144">The metadata of the updated policy set definition.</span></span> <span data-ttu-id="c3b16-145">Può trattarsi del percorso di un nome file contenente i metadati o dei metadati come stringa JSON.</span><span class="sxs-lookup"><span data-stu-id="c3b16-145">This can either be a path to a file name containing the metadata, or the metadata as a JSON string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3b16-146">-Name</span><span class="sxs-lookup"><span data-stu-id="c3b16-146">-Name</span></span>
<span data-ttu-id="c3b16-147">Nome della definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="c3b16-147">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3b16-148">-Parameter</span><span class="sxs-lookup"><span data-stu-id="c3b16-148">-Parameter</span></span>
<span data-ttu-id="c3b16-149">Dichiarazione dei parametri della definizione del set di criteri aggiornata.</span><span class="sxs-lookup"><span data-stu-id="c3b16-149">The parameters declaration of the updated policy set definition.</span></span> <span data-ttu-id="c3b16-150">Può trattarsi del percorso di un nome file o di un URI contenente la dichiarazione dei parametri oppure della dichiarazione dei parametri come stringa JSON.</span><span class="sxs-lookup"><span data-stu-id="c3b16-150">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as a JSON string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3b16-151">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c3b16-151">-PolicyDefinition</span></span>
<span data-ttu-id="c3b16-152">Definizioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="c3b16-152">The policy definitions.</span></span> <span data-ttu-id="c3b16-153">Può trattarsi del percorso di un nome file contenente le definizioni dei criteri oppure delle definizioni dei criteri come stringa JSON.</span><span class="sxs-lookup"><span data-stu-id="c3b16-153">This can either be a path to a file name containing the policy definitions, or the policy definitions as a JSON string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3b16-154">-Pre</span><span class="sxs-lookup"><span data-stu-id="c3b16-154">-Pre</span></span>
<span data-ttu-id="c3b16-155">Se impostato, indica che il cmdlet deve usare versioni delle API non beta per determinare automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="c3b16-155">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="c3b16-156">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c3b16-156">-SubscriptionId</span></span>
<span data-ttu-id="c3b16-157">ID sottoscrizione della definizione del set di criteri da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="c3b16-157">The subscription ID of the policy set definition to update.</span></span>

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

### <span data-ttu-id="c3b16-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c3b16-158">-Confirm</span></span>
<span data-ttu-id="c3b16-159">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3b16-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3b16-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3b16-160">-WhatIf</span></span>
<span data-ttu-id="c3b16-161">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c3b16-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c3b16-162">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c3b16-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3b16-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3b16-163">CommonParameters</span></span>
<span data-ttu-id="c3b16-164">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3b16-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3b16-165">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c3b16-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3b16-166">INPUT</span><span class="sxs-lookup"><span data-stu-id="c3b16-166">INPUTS</span></span>

### <span data-ttu-id="c3b16-167">System.String</span><span class="sxs-lookup"><span data-stu-id="c3b16-167">System.String</span></span>

### <span data-ttu-id="c3b16-168">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c3b16-168">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="c3b16-169">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c3b16-169">OUTPUTS</span></span>

### <span data-ttu-id="c3b16-170">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="c3b16-170">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c3b16-171">NOTE</span><span class="sxs-lookup"><span data-stu-id="c3b16-171">NOTES</span></span>

## <span data-ttu-id="c3b16-172">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c3b16-172">RELATED LINKS</span></span>
