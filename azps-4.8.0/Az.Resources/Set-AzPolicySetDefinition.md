---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
ms.openlocfilehash: cd8bc24a0cedac91ef18e19a80e1662fdcbac297
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189365"
---
# <span data-ttu-id="ec6b4-101">Set-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="ec6b4-101">Set-AzPolicySetDefinition</span></span>

## <span data-ttu-id="ec6b4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ec6b4-102">SYNOPSIS</span></span>
<span data-ttu-id="ec6b4-103">Modifica di una definizione di set di criteri</span><span class="sxs-lookup"><span data-stu-id="ec6b4-103">Modifies a policy set definition</span></span>

## <span data-ttu-id="ec6b4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ec6b4-104">SYNTAX</span></span>

### <span data-ttu-id="ec6b4-105">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ec6b4-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ec6b4-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec6b4-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -ManagementGroupName <String>
 [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec6b4-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec6b4-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -SubscriptionId <Guid>
 [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec6b4-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec6b4-108">IdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ec6b4-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec6b4-109">InputObjectParameterSet</span></span>
```
Set-AzPolicySetDefinition [-DisplayName <String>] [-Description <String>] [-PolicyDefinition <String>]
 [-Metadata <String>] [-Parameter <String>] -InputObject <PsPolicySetDefinition> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ec6b4-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ec6b4-110">DESCRIPTION</span></span>
<span data-ttu-id="ec6b4-111">Il cmdlet **set-AzPolicySetDefinition** modifica una definizione di criteri.</span><span class="sxs-lookup"><span data-stu-id="ec6b4-111">The **Set-AzPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="ec6b4-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ec6b4-112">EXAMPLES</span></span>

### <span data-ttu-id="ec6b4-113">Esempio 1: aggiornare la descrizione di una definizione di set di criteri</span><span class="sxs-lookup"><span data-stu-id="ec6b4-113">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Set-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="ec6b4-114">Il primo comando ottiene una definizione di set di criteri usando il cmdlet Get-AzPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="ec6b4-114">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="ec6b4-115">Il comando Archivia l'oggetto nella variabile $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="ec6b4-115">The command stores that object in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="ec6b4-116">Il secondo comando Aggiorna la descrizione della definizione del set di criteri identificata dalla proprietà **resourceId** di $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="ec6b4-116">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

### <span data-ttu-id="ec6b4-117">Esempio 2: aggiornare i metadati di una definizione di set di criteri</span><span class="sxs-lookup"><span data-stu-id="ec6b4-117">Example 2: Update the metadata of a policy set definition</span></span>
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

<span data-ttu-id="ec6b4-118">Questo comando Aggiorna i metadati di una definizione di set di criteri denominata VMPolicySetDefinition per indicare che la categoria è "macchina virtuale".</span><span class="sxs-lookup"><span data-stu-id="ec6b4-118">This command updates the metadata of a policy set definition named VMPolicySetDefinition to indicate its category is "Virtual Machine".</span></span>

### <span data-ttu-id="ec6b4-119">Esempio 3: aggiornare i gruppi di una definizione di set di criteri</span><span class="sxs-lookup"><span data-stu-id="ec6b4-119">Example 3: Update the groups of a policy set definition</span></span>
```
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition '[{ "name": "group1", "displayName": "Virtual Machine Security" }, { "name": "group2" }]'
```

<span data-ttu-id="ec6b4-120">Questo comando Aggiorna i gruppi di una definizione di set di criteri denominata VMPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="ec6b4-120">This command updates the groups of a policy set definition named VMPolicySetDefinition.</span></span>

### <span data-ttu-id="ec6b4-121">Esempio 4: aggiornare i gruppi di una definizione di set di criteri tramite una tabella hash</span><span class="sxs-lookup"><span data-stu-id="ec6b4-121">Example 4: Update the groups of a policy set definition using a hash table</span></span>
```
$groupsJson = ConvertTo-Json @{ name = "group1", displayName = "Virtual Machine Security" }, @{ name = "group2" }
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition $groupsJson
```

<span data-ttu-id="ec6b4-122">Questo comando Aggiorna i gruppi di una definizione di set di criteri denominata VMPolicySetDefinition utilizzando una tabella hash per creare i gruppi.</span><span class="sxs-lookup"><span data-stu-id="ec6b4-122">This command updates the groups of a policy set definition named VMPolicySetDefinition using a hash table to construct the groups.</span></span>

## <span data-ttu-id="ec6b4-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ec6b4-123">PARAMETERS</span></span>

### <span data-ttu-id="ec6b4-124">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ec6b4-124">-ApiVersion</span></span>
<span data-ttu-id="ec6b4-125">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="ec6b4-125">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="ec6b4-126">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="ec6b4-126">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="ec6b4-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec6b4-127">-DefaultProfile</span></span>
<span data-ttu-id="ec6b4-128">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ec6b4-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ec6b4-129">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="ec6b4-129">-Description</span></span>
<span data-ttu-id="ec6b4-130">Descrizione della definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="ec6b4-130">The description for policy set definition.</span></span>

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

### <span data-ttu-id="ec6b4-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ec6b4-131">-DisplayName</span></span>
<span data-ttu-id="ec6b4-132">Nome visualizzato per la definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="ec6b4-132">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="ec6b4-133">-GroupDefinition</span><span class="sxs-lookup"><span data-stu-id="ec6b4-133">-GroupDefinition</span></span>
<span data-ttu-id="ec6b4-134">Gruppi di definizione dei criteri della definizione del set di criteri aggiornata.</span><span class="sxs-lookup"><span data-stu-id="ec6b4-134">The policy definition groups of the updated policy set definition.</span></span> <span data-ttu-id="ec6b4-135">Può essere un percorso di un file contenente i gruppi o i gruppi come stringa JSON.</span><span class="sxs-lookup"><span data-stu-id="ec6b4-135">This can either be a path to a file containing the groups, or the groups as a JSON string.</span></span>

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

### <span data-ttu-id="ec6b4-136">-ID</span><span class="sxs-lookup"><span data-stu-id="ec6b4-136">-Id</span></span>
<span data-ttu-id="ec6b4-137">ID di definizione dei criteri completo, incluso l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="ec6b4-137">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="ec6b4-138">ad esempio/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="ec6b4-138">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="ec6b4-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec6b4-139">-InputObject</span></span>
<span data-ttu-id="ec6b4-140">Oggetto definizione del set di criteri da aggiornare che è stato restituito da un altro cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec6b4-140">The policy set definition object to update that was output from another cmdlet.</span></span>

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

### <span data-ttu-id="ec6b4-141">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="ec6b4-141">-ManagementGroupName</span></span>
<span data-ttu-id="ec6b4-142">Nome del gruppo di gestione della definizione del set di criteri da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="ec6b4-142">The name of the management group of the policy set definition to update.</span></span>

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

### <span data-ttu-id="ec6b4-143">-Metadata</span><span class="sxs-lookup"><span data-stu-id="ec6b4-143">-Metadata</span></span>
<span data-ttu-id="ec6b4-144">Metadati della definizione del set di criteri aggiornata.</span><span class="sxs-lookup"><span data-stu-id="ec6b4-144">The metadata of the updated policy set definition.</span></span> <span data-ttu-id="ec6b4-145">Può essere un percorso per un nome di file contenente i metadati o i metadati come stringa JSON.</span><span class="sxs-lookup"><span data-stu-id="ec6b4-145">This can either be a path to a file name containing the metadata, or the metadata as a JSON string.</span></span>

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

### <span data-ttu-id="ec6b4-146">-Nome</span><span class="sxs-lookup"><span data-stu-id="ec6b4-146">-Name</span></span>
<span data-ttu-id="ec6b4-147">Nome della definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="ec6b4-147">The policy set definition name.</span></span>

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

### <span data-ttu-id="ec6b4-148">Parametro-</span><span class="sxs-lookup"><span data-stu-id="ec6b4-148">-Parameter</span></span>
<span data-ttu-id="ec6b4-149">Dichiarazione Parameters della definizione del set di criteri aggiornata.</span><span class="sxs-lookup"><span data-stu-id="ec6b4-149">The parameters declaration of the updated policy set definition.</span></span> <span data-ttu-id="ec6b4-150">Può trattarsi di un percorso di un nome file o di un URI che contiene la dichiarazione parameters o della dichiarazione Parameters come stringa JSON.</span><span class="sxs-lookup"><span data-stu-id="ec6b4-150">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as a JSON string.</span></span>

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

### <span data-ttu-id="ec6b4-151">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ec6b4-151">-PolicyDefinition</span></span>
<span data-ttu-id="ec6b4-152">Definizioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="ec6b4-152">The policy definitions.</span></span> <span data-ttu-id="ec6b4-153">Può essere un percorso per un nome di file contenente le definizioni dei criteri o le definizioni dei criteri come stringa JSON.</span><span class="sxs-lookup"><span data-stu-id="ec6b4-153">This can either be a path to a file name containing the policy definitions, or the policy definitions as a JSON string.</span></span>

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

### <span data-ttu-id="ec6b4-154">-Pre</span><span class="sxs-lookup"><span data-stu-id="ec6b4-154">-Pre</span></span>
<span data-ttu-id="ec6b4-155">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="ec6b4-155">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="ec6b4-156">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ec6b4-156">-SubscriptionId</span></span>
<span data-ttu-id="ec6b4-157">ID sottoscrizione della definizione del set di criteri da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="ec6b4-157">The subscription ID of the policy set definition to update.</span></span>

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

### <span data-ttu-id="ec6b4-158">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ec6b4-158">-Confirm</span></span>
<span data-ttu-id="ec6b4-159">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec6b4-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec6b4-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec6b4-160">-WhatIf</span></span>
<span data-ttu-id="ec6b4-161">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ec6b4-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ec6b4-162">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ec6b4-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec6b4-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec6b4-163">CommonParameters</span></span>
<span data-ttu-id="ec6b4-164">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec6b4-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec6b4-165">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec6b4-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec6b4-166">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ec6b4-166">INPUTS</span></span>

### <span data-ttu-id="ec6b4-167">System. String</span><span class="sxs-lookup"><span data-stu-id="ec6b4-167">System.String</span></span>

### <span data-ttu-id="ec6b4-168">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ec6b4-168">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="ec6b4-169">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ec6b4-169">OUTPUTS</span></span>

### <span data-ttu-id="ec6b4-170">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="ec6b4-170">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="ec6b4-171">Note</span><span class="sxs-lookup"><span data-stu-id="ec6b4-171">NOTES</span></span>

## <span data-ttu-id="ec6b4-172">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ec6b4-172">RELATED LINKS</span></span>
