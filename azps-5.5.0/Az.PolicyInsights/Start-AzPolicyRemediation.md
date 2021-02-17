---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/start-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
ms.openlocfilehash: e4a0e3ad4ffac7e610f5807c7687cdc1bf548770
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186662"
---
# <span data-ttu-id="35e37-101">Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="35e37-101">Start-AzPolicyRemediation</span></span>

## <span data-ttu-id="35e37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35e37-102">SYNOPSIS</span></span>
<span data-ttu-id="35e37-103">Crea e avvia una correzione dei criteri per un'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="35e37-103">Creates and starts a policy remediation for a policy assignment.</span></span>

## <span data-ttu-id="35e37-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="35e37-104">SYNTAX</span></span>

### <span data-ttu-id="35e37-105">ByName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="35e37-105">ByName (Default)</span></span>
```
Start-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] -PolicyAssignmentId <String> [-PolicyDefinitionReferenceId <String>]
 [-LocationFilter <String[]>] [-ResourceDiscoveryMode <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35e37-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="35e37-106">ByResourceId</span></span>
```
Start-AzPolicyRemediation -ResourceId <String> -PolicyAssignmentId <String>
 [-PolicyDefinitionReferenceId <String>] [-LocationFilter <String[]>] [-ResourceDiscoveryMode <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35e37-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="35e37-107">DESCRIPTION</span></span>
<span data-ttu-id="35e37-108">Il cmdlet **Start-AzPolicyRemediation** crea una correzione dei criteri per una particolare assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="35e37-108">The **Start-AzPolicyRemediation** cmdlet creates a policy remediation for a particular policy assignment.</span></span> <span data-ttu-id="35e37-109">Tutte le risorse non conformi nell'ambito della correzione verranno corretti.</span><span class="sxs-lookup"><span data-stu-id="35e37-109">All non-compliant resources at or below the remediation's scope will be remediated.</span></span> <span data-ttu-id="35e37-110">La correzione è supportata solo per i criteri con l'effetto 'deployIfNotExists'.</span><span class="sxs-lookup"><span data-stu-id="35e37-110">Remediation is only supported for policies with the 'deployIfNotExists' effect.</span></span>

## <span data-ttu-id="35e37-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="35e37-111">EXAMPLES</span></span>

### <span data-ttu-id="35e37-112">Esempio 1: Avviare una correzione per l'ambito della sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="35e37-112">Example 1: Start a remediation at subscription scope</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1"
```

<span data-ttu-id="35e37-113">Questo comando crea una nuova correzione dei criteri nella sottoscrizione "La mia sottoscrizione" per l'assegnazione di criteri specificata.</span><span class="sxs-lookup"><span data-stu-id="35e37-113">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span>

### <span data-ttu-id="35e37-114">Esempio 2: Avviare una correzione per l'ambito del gruppo di gestione con filtri facoltativi</span><span class="sxs-lookup"><span data-stu-id="35e37-114">Example 2: Start a remediation at management group scope with optional filters</span></span>
```
PS C:\> $policyAssignmentId = "/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1"
PS C:\> Start-AzPolicyRemediation -ManagementGroupName "mg1" -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -LocationFilter "westus","eastus"
```

<span data-ttu-id="35e37-115">Questo comando crea una nuova correzione dei criteri nel gruppo di gestione 'mg1' per l'assegnazione di criteri specificata.</span><span class="sxs-lookup"><span data-stu-id="35e37-115">This command creates a new policy remediation in management group 'mg1' for the given policy assignment.</span></span> <span data-ttu-id="35e37-116">Verranno corretti solo le risorse nelle posizioni "ovest" o "estus".</span><span class="sxs-lookup"><span data-stu-id="35e37-116">Only resources in the 'westus' or 'eastus' locations will be remediated.</span></span>

### <span data-ttu-id="35e37-117">Esempio 3: Avviare una correzione per l'ambito del gruppo di risorse per l'assegnazione di una definizione del set di criteri</span><span class="sxs-lookup"><span data-stu-id="35e37-117">Example 3: Start a remediation at resource group scope for a policy set definition assignment</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/resourceGroups/myRG/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Start-AzPolicyRemediation -ResourceGroupName "myRG" -PolicyAssignmentId $policyAssignmentId -PolicyDefinitionReferenceId "0349234412441" -Name "remediation1"
```

<span data-ttu-id="35e37-118">Questo comando crea una nuova correzione dei criteri nel gruppo di risorse "myRG" per l'assegnazione di criteri specificata.</span><span class="sxs-lookup"><span data-stu-id="35e37-118">This command creates a new policy remediation in resource group 'myRG' for the given policy assignment.</span></span> <span data-ttu-id="35e37-119">L'assegnazione dei criteri assegna una definizione di set di criteri (nota anche come iniziativa).</span><span class="sxs-lookup"><span data-stu-id="35e37-119">The policy assignment assigns a policy set definition (also known as an initiative).</span></span> <span data-ttu-id="35e37-120">L'ID di riferimento della definizione dei criteri indica quale criterio all'interno dell'iniziativa deve essere corretti.</span><span class="sxs-lookup"><span data-stu-id="35e37-120">The policy definition reference ID indicates which policy within the initiative should be remediated.</span></span>

### <span data-ttu-id="35e37-121">Esempio 4: Avviare una correzione e attendere il completamento in background</span><span class="sxs-lookup"><span data-stu-id="35e37-121">Example 4: Start a remediation and wait for it to complete in the background</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription f0710c27-9663-4c05-19f8-1b4be01e86a5
PS C:\> $job = Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -AsJob
PS C:\> $job | Wait-Job
PS C:\> $remediation = $job | Receive-Job
```

<span data-ttu-id="35e37-122">Questo comando avvia una nuova correzione dei criteri nella sottoscrizione "La mia sottoscrizione" per l'assegnazione di criteri specificata.</span><span class="sxs-lookup"><span data-stu-id="35e37-122">This command starts a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="35e37-123">Attenderà il completamento della correzione prima di restituire lo stato finale della correzione.</span><span class="sxs-lookup"><span data-stu-id="35e37-123">It will wait for the remediation to complete before returning the final remediation status.</span></span>

### <span data-ttu-id="35e37-124">Esempio 5: Avviare una correzione che individua risorse non conformi prima di correggere</span><span class="sxs-lookup"><span data-stu-id="35e37-124">Example 5: Start a remediation that will discover non-compliant resources before remediating</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -ResourceDiscoveryMode ReEvaluateCompliance
```

<span data-ttu-id="35e37-125">Questo comando crea una nuova correzione dei criteri nella sottoscrizione "La mia sottoscrizione" per l'assegnazione di criteri specificata.</span><span class="sxs-lookup"><span data-stu-id="35e37-125">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="35e37-126">Lo stato di conformità delle risorse nella sottoscrizione verrà valutato nuovamente in base all'assegnazione dei criteri e le risorse non conformi verranno corretti.</span><span class="sxs-lookup"><span data-stu-id="35e37-126">The compliance state of resources in the subscription will be re-evaluated against the policy assignment and non-compliant resources will be remediated.</span></span>

## <span data-ttu-id="35e37-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35e37-127">PARAMETERS</span></span>

### <span data-ttu-id="35e37-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35e37-128">-AsJob</span></span>
<span data-ttu-id="35e37-129">Eseguire il cmdlet in background.</span><span class="sxs-lookup"><span data-stu-id="35e37-129">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="35e37-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35e37-130">-DefaultProfile</span></span>
<span data-ttu-id="35e37-131">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="35e37-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35e37-132">-LocationFilter</span><span class="sxs-lookup"><span data-stu-id="35e37-132">-LocationFilter</span></span>
<span data-ttu-id="35e37-133">Posizioni delle risorse da includere nella correzione.</span><span class="sxs-lookup"><span data-stu-id="35e37-133">The resource locations that should be included in the remediation.</span></span>
<span data-ttu-id="35e37-134">Le risorse che non risiedono in questi percorsi non verranno corretti.</span><span class="sxs-lookup"><span data-stu-id="35e37-134">Resources that don't reside in these locations will not be remediated.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35e37-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="35e37-135">-ManagementGroupName</span></span>
<span data-ttu-id="35e37-136">ID gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="35e37-136">Management group ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35e37-137">-Name</span><span class="sxs-lookup"><span data-stu-id="35e37-137">-Name</span></span>
<span data-ttu-id="35e37-138">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="35e37-138">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35e37-139">-PolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="35e37-139">-PolicyAssignmentId</span></span>
<span data-ttu-id="35e37-140">ID assegnazione criteri.</span><span class="sxs-lookup"><span data-stu-id="35e37-140">Policy assignment ID.</span></span>
<span data-ttu-id="35e37-141">Ad esempio</span><span class="sxs-lookup"><span data-stu-id="35e37-141">E.g.</span></span>
<span data-ttu-id="35e37-142">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span><span class="sxs-lookup"><span data-stu-id="35e37-142">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35e37-143">-PolicyDefinitionReferenceId</span><span class="sxs-lookup"><span data-stu-id="35e37-143">-PolicyDefinitionReferenceId</span></span>
<span data-ttu-id="35e37-144">Ottiene l'ID di riferimento della definizione dei criteri della singola definizione da correggere.</span><span class="sxs-lookup"><span data-stu-id="35e37-144">Gets the policy definition reference ID of the individual definition that is being remediated.</span></span>
<span data-ttu-id="35e37-145">Obbligatorio quando l'assegnazione dei criteri assegna una definizione di set di criteri.</span><span class="sxs-lookup"><span data-stu-id="35e37-145">Required when the policy assignment assigns a policy set definition.</span></span>

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

### <span data-ttu-id="35e37-146">-ResourceDiscoveryMode</span><span class="sxs-lookup"><span data-stu-id="35e37-146">-ResourceDiscoveryMode</span></span>
<span data-ttu-id="35e37-147">Descrive in che modo l'attività di correzione individua le risorse che è necessario correggere.</span><span class="sxs-lookup"><span data-stu-id="35e37-147">Describes how the remediation task will discover resources that need to be remediated.</span></span>
<span data-ttu-id="35e37-148">La correzione degli ambiti dei gruppi di gestione non è supportata da ReEvaluateCompliance.</span><span class="sxs-lookup"><span data-stu-id="35e37-148">ReEvaluateCompliance is not supported when remediating management group scopes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ExistingNonCompliant, ReEvaluateCompliance

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35e37-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35e37-149">-ResourceGroupName</span></span>
<span data-ttu-id="35e37-150">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="35e37-150">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35e37-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="35e37-151">-ResourceId</span></span>
<span data-ttu-id="35e37-152">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="35e37-152">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35e37-153">-Scope</span><span class="sxs-lookup"><span data-stu-id="35e37-153">-Scope</span></span>
<span data-ttu-id="35e37-154">Ambito della risorsa.</span><span class="sxs-lookup"><span data-stu-id="35e37-154">Scope of the resource.</span></span>
<span data-ttu-id="35e37-155">Ad esempio</span><span class="sxs-lookup"><span data-stu-id="35e37-155">E.g.</span></span>
<span data-ttu-id="35e37-156">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="35e37-156">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35e37-157">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35e37-157">-Confirm</span></span>
<span data-ttu-id="35e37-158">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35e37-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35e37-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35e37-159">-WhatIf</span></span>
<span data-ttu-id="35e37-160">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35e37-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35e37-161">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35e37-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35e37-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35e37-162">CommonParameters</span></span>
<span data-ttu-id="35e37-163">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35e37-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35e37-164">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="35e37-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35e37-165">INPUT</span><span class="sxs-lookup"><span data-stu-id="35e37-165">INPUTS</span></span>

### <span data-ttu-id="35e37-166">System.String</span><span class="sxs-lookup"><span data-stu-id="35e37-166">System.String</span></span>

### <span data-ttu-id="35e37-167">System.String[]</span><span class="sxs-lookup"><span data-stu-id="35e37-167">System.String[]</span></span>

## <span data-ttu-id="35e37-168">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="35e37-168">OUTPUTS</span></span>

### <span data-ttu-id="35e37-169">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span><span class="sxs-lookup"><span data-stu-id="35e37-169">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="35e37-170">NOTE</span><span class="sxs-lookup"><span data-stu-id="35e37-170">NOTES</span></span>

## <span data-ttu-id="35e37-171">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="35e37-171">RELATED LINKS</span></span>
