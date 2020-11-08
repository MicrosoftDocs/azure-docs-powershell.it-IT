---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
ms.openlocfilehash: 8a8559058b0bb5e1b33d93451bed35182a44783b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019692"
---
# <span data-ttu-id="1bfbb-101">Set-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="1bfbb-101">Set-AzPolicySetDefinition</span></span>

## <span data-ttu-id="1bfbb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1bfbb-102">SYNOPSIS</span></span>
<span data-ttu-id="1bfbb-103">Modifica di una definizione di set di criteri</span><span class="sxs-lookup"><span data-stu-id="1bfbb-103">Modifies a policy set definition</span></span>

## <span data-ttu-id="1bfbb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1bfbb-104">SYNTAX</span></span>

### <span data-ttu-id="1bfbb-105">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1bfbb-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1bfbb-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1bfbb-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -ManagementGroupName <String>
 [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bfbb-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1bfbb-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -SubscriptionId <Guid>
 [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bfbb-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1bfbb-108">IdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1bfbb-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1bfbb-109">DESCRIPTION</span></span>
<span data-ttu-id="1bfbb-110">Il cmdlet **set-AzPolicySetDefinition** modifica una definizione di criteri.</span><span class="sxs-lookup"><span data-stu-id="1bfbb-110">The **Set-AzPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="1bfbb-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1bfbb-111">EXAMPLES</span></span>

### <span data-ttu-id="1bfbb-112">Esempio 1: aggiornare la descrizione di una definizione di set di criteri</span><span class="sxs-lookup"><span data-stu-id="1bfbb-112">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Set-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="1bfbb-113">Il primo comando ottiene una definizione di set di criteri usando il cmdlet Get-AzPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="1bfbb-113">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="1bfbb-114">Il comando Archivia l'oggetto nella variabile $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="1bfbb-114">The command stores that object in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="1bfbb-115">Il secondo comando Aggiorna la descrizione della definizione del set di criteri identificata dalla proprietà **resourceId** di $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="1bfbb-115">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

### <span data-ttu-id="1bfbb-116">Esempio 2: aggiornare i metadati di una definizione di set di criteri</span><span class="sxs-lookup"><span data-stu-id="1bfbb-116">Example 2: Update the metadata of a policy set definition</span></span>
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

<span data-ttu-id="1bfbb-117">Questo comando Aggiorna i metadati di una definizione di set di criteri denominata VMPolicySetDefinition per indicare che la categoria è "macchina virtuale".</span><span class="sxs-lookup"><span data-stu-id="1bfbb-117">This command updates the metadata of a policy set definition named VMPolicySetDefinition to indicate its category is "Virtual Machine".</span></span>

### <span data-ttu-id="1bfbb-118">Esempio 3: aggiornare i gruppi di una definizione di set di criteri</span><span class="sxs-lookup"><span data-stu-id="1bfbb-118">Example 3: Update the groups of a policy set definition</span></span>
```
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition '[{ "name": "group1", "displayName": "Virtual Machine Security" }, { "name": "group2" }]'
```

<span data-ttu-id="1bfbb-119">Questo comando Aggiorna i gruppi di una definizione di set di criteri denominata VMPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="1bfbb-119">This command updates the groups of a policy set definition named VMPolicySetDefinition.</span></span>

### <span data-ttu-id="1bfbb-120">Esempio 4: aggiornare i gruppi di una definizione di set di criteri tramite una tabella hash</span><span class="sxs-lookup"><span data-stu-id="1bfbb-120">Example 4: Update the groups of a policy set definition using a hash table</span></span>
```
$groupsJson = ConvertTo-Json @{ name = "group1", displayName = "Virtual Machine Security" }, @{ name = "group2" }
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition $groupsJson
```

<span data-ttu-id="1bfbb-121">Questo comando Aggiorna i gruppi di una definizione di set di criteri denominata VMPolicySetDefinition utilizzando una tabella hash per creare i gruppi.</span><span class="sxs-lookup"><span data-stu-id="1bfbb-121">This command updates the groups of a policy set definition named VMPolicySetDefinition using a hash table to construct the groups.</span></span>

## <span data-ttu-id="1bfbb-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1bfbb-122">PARAMETERS</span></span>

### <span data-ttu-id="1bfbb-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1bfbb-123">-ApiVersion</span></span>
<span data-ttu-id="1bfbb-124">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="1bfbb-124">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="1bfbb-125">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="1bfbb-125">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="1bfbb-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bfbb-126">-DefaultProfile</span></span>
<span data-ttu-id="1bfbb-127">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1bfbb-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1bfbb-128">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="1bfbb-128">-Description</span></span>
<span data-ttu-id="1bfbb-129">Descrizione della definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="1bfbb-129">The description for policy set definition.</span></span>

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

### <span data-ttu-id="1bfbb-130">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1bfbb-130">-DisplayName</span></span>
<span data-ttu-id="1bfbb-131">Nome visualizzato per la definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="1bfbb-131">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="1bfbb-132">-GroupDefinition</span><span class="sxs-lookup"><span data-stu-id="1bfbb-132">-GroupDefinition</span></span>
<span data-ttu-id="1bfbb-133">Gruppi di definizione dei criteri della definizione del set di criteri aggiornata.</span><span class="sxs-lookup"><span data-stu-id="1bfbb-133">The policy definition groups of the updated policy set definition.</span></span> <span data-ttu-id="1bfbb-134">Può essere un percorso di un file contenente i gruppi o i gruppi come stringa JSON.</span><span class="sxs-lookup"><span data-stu-id="1bfbb-134">This can either be a path to a file containing the groups, or the groups as a JSON string.</span></span>

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

### <span data-ttu-id="1bfbb-135">-ID</span><span class="sxs-lookup"><span data-stu-id="1bfbb-135">-Id</span></span>
<span data-ttu-id="1bfbb-136">ID di definizione dei criteri completo, incluso l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="1bfbb-136">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="1bfbb-137">ad esempio/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="1bfbb-137">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="1bfbb-138">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="1bfbb-138">-ManagementGroupName</span></span>
<span data-ttu-id="1bfbb-139">Nome del gruppo di gestione della definizione del set di criteri da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="1bfbb-139">The name of the management group of the policy set definition to update.</span></span>

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

### <span data-ttu-id="1bfbb-140">-Metadata</span><span class="sxs-lookup"><span data-stu-id="1bfbb-140">-Metadata</span></span>
<span data-ttu-id="1bfbb-141">Metadati della definizione del set di criteri aggiornata.</span><span class="sxs-lookup"><span data-stu-id="1bfbb-141">The metadata of the updated policy set definition.</span></span> <span data-ttu-id="1bfbb-142">Può essere un percorso per un nome di file contenente i metadati o i metadati come stringa JSON.</span><span class="sxs-lookup"><span data-stu-id="1bfbb-142">This can either be a path to a file name containing the metadata, or the metadata as a JSON string.</span></span>

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

### <span data-ttu-id="1bfbb-143">-Nome</span><span class="sxs-lookup"><span data-stu-id="1bfbb-143">-Name</span></span>
<span data-ttu-id="1bfbb-144">Nome della definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="1bfbb-144">The policy set definition name.</span></span>

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

### <span data-ttu-id="1bfbb-145">Parametro-</span><span class="sxs-lookup"><span data-stu-id="1bfbb-145">-Parameter</span></span>
<span data-ttu-id="1bfbb-146">Dichiarazione Parameters della definizione del set di criteri aggiornata.</span><span class="sxs-lookup"><span data-stu-id="1bfbb-146">The parameters declaration of the updated policy set definition.</span></span> <span data-ttu-id="1bfbb-147">Può trattarsi di un percorso di un nome file o di un URI che contiene la dichiarazione parameters o della dichiarazione Parameters come stringa JSON.</span><span class="sxs-lookup"><span data-stu-id="1bfbb-147">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as a JSON string.</span></span>

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

### <span data-ttu-id="1bfbb-148">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1bfbb-148">-PolicyDefinition</span></span>
<span data-ttu-id="1bfbb-149">Definizioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="1bfbb-149">The policy definitions.</span></span> <span data-ttu-id="1bfbb-150">Può essere un percorso per un nome di file contenente le definizioni dei criteri o le definizioni dei criteri come stringa JSON.</span><span class="sxs-lookup"><span data-stu-id="1bfbb-150">This can either be a path to a file name containing the policy definitions, or the policy definitions as a JSON string.</span></span>

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

### <span data-ttu-id="1bfbb-151">-Pre</span><span class="sxs-lookup"><span data-stu-id="1bfbb-151">-Pre</span></span>
<span data-ttu-id="1bfbb-152">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="1bfbb-152">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="1bfbb-153">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1bfbb-153">-SubscriptionId</span></span>
<span data-ttu-id="1bfbb-154">ID sottoscrizione della definizione del set di criteri da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="1bfbb-154">The subscription ID of the policy set definition to update.</span></span>

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

### <span data-ttu-id="1bfbb-155">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1bfbb-155">-Confirm</span></span>
<span data-ttu-id="1bfbb-156">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1bfbb-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bfbb-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bfbb-157">-WhatIf</span></span>
<span data-ttu-id="1bfbb-158">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1bfbb-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1bfbb-159">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1bfbb-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bfbb-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bfbb-160">CommonParameters</span></span>
<span data-ttu-id="1bfbb-161">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bfbb-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bfbb-162">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1bfbb-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bfbb-163">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1bfbb-163">INPUTS</span></span>

### <span data-ttu-id="1bfbb-164">System. String</span><span class="sxs-lookup"><span data-stu-id="1bfbb-164">System.String</span></span>

### <span data-ttu-id="1bfbb-165">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1bfbb-165">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="1bfbb-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1bfbb-166">OUTPUTS</span></span>

### <span data-ttu-id="1bfbb-167">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="1bfbb-167">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="1bfbb-168">Note</span><span class="sxs-lookup"><span data-stu-id="1bfbb-168">NOTES</span></span>

## <span data-ttu-id="1bfbb-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1bfbb-169">RELATED LINKS</span></span>
