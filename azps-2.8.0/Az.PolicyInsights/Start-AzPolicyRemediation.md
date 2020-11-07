---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/start-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
ms.openlocfilehash: df7b0803952a7a972d2c68ef2d8e7ec61d42c5e9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855349"
---
# <span data-ttu-id="d3262-101">Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="d3262-101">Start-AzPolicyRemediation</span></span>

## <span data-ttu-id="d3262-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d3262-102">SYNOPSIS</span></span>
<span data-ttu-id="d3262-103">Crea e avvia un criterio di correzione per un'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="d3262-103">Creates and starts a policy remediation for a policy assignment.</span></span>

## <span data-ttu-id="d3262-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d3262-104">SYNTAX</span></span>

### <span data-ttu-id="d3262-105">ByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d3262-105">ByName (Default)</span></span>
```
Start-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] -PolicyAssignmentId <String> [-PolicyDefinitionReferenceId <String>]
 [-LocationFilter <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d3262-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d3262-106">ByResourceId</span></span>
```
Start-AzPolicyRemediation -ResourceId <String> -PolicyAssignmentId <String>
 [-PolicyDefinitionReferenceId <String>] [-LocationFilter <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3262-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3262-107">DESCRIPTION</span></span>
<span data-ttu-id="d3262-108">Il cmdlet **Start-AzPolicyRemediation** crea un criterio di correzione per una specifica assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="d3262-108">The **Start-AzPolicyRemediation** cmdlet creates a policy remediation for a particular policy assignment.</span></span> <span data-ttu-id="d3262-109">Tutte le risorse non conformi a o sotto l'ambito del correttivo verranno risanate.</span><span class="sxs-lookup"><span data-stu-id="d3262-109">All non-compliant resources at or below the remediation's scope will be remediated.</span></span> <span data-ttu-id="d3262-110">Il risanamento è supportato solo per i criteri con l'effetto ' deployIfNotExists '.</span><span class="sxs-lookup"><span data-stu-id="d3262-110">Remediation is only supported for policies with the 'deployIfNotExists' effect.</span></span>

## <span data-ttu-id="d3262-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d3262-111">EXAMPLES</span></span>

### <span data-ttu-id="d3262-112">Esempio 1: avviare un aggiornamento nell'ambito dell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="d3262-112">Example 1: Start a remediation at subscription scope</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1"
```

<span data-ttu-id="d3262-113">Questo comando crea un nuovo criterio di correzione dei criteri nell'abbonamento "abbonamento" per l'assegnazione di criteri specificata.</span><span class="sxs-lookup"><span data-stu-id="d3262-113">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span>

### <span data-ttu-id="d3262-114">Esempio 2: avviare una correzione nell'ambito di un gruppo di gestione con filtri facoltativi</span><span class="sxs-lookup"><span data-stu-id="d3262-114">Example 2: Start a remediation at management group scope with optional filters</span></span>
```
PS C:\> $policyAssignmentId = "/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1"
PS C:\> Start-AzPolicyRemediation -ManagementGroupName "mg1" -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -LocationFilter "westus","eastus"
```

<span data-ttu-id="d3262-115">Questo comando crea un nuovo criterio di correzione dei criteri nel gruppo di gestione "MG1" per l'assegnazione di criteri specificata.</span><span class="sxs-lookup"><span data-stu-id="d3262-115">This command creates a new policy remediation in management group 'mg1' for the given policy assignment.</span></span> <span data-ttu-id="d3262-116">Verranno risanate solo le risorse nelle posizioni "westus" o "eastus".</span><span class="sxs-lookup"><span data-stu-id="d3262-116">Only resources in the 'westus' or 'eastus' locations will be remediated.</span></span>

### <span data-ttu-id="d3262-117">Esempio 3: avviare un'attività di correzione nell'ambito di un gruppo di risorse per un'assegnazione di definizione di set di criteri</span><span class="sxs-lookup"><span data-stu-id="d3262-117">Example 3: Start a remediation at resource group scope for a policy set definition assignment</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/resourceGroups/myRG/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Start-AzPolicyRemediation -ResourceGroupName "myRG" -PolicyAssignmentId $policyAssignmentId -PolicyDefinitionReferenceId "0349234412441" -Name "remediation1"
```

<span data-ttu-id="d3262-118">Questo comando crea una nuova correzione dei criteri nel gruppo di risorse "myRG" per l'assegnazione di criteri specificata.</span><span class="sxs-lookup"><span data-stu-id="d3262-118">This command creates a new policy remediation in resource group 'myRG' for the given policy assignment.</span></span> <span data-ttu-id="d3262-119">L'assegnazione dei criteri assegna una definizione di set di criteri (nota anche come iniziativa).</span><span class="sxs-lookup"><span data-stu-id="d3262-119">The policy assignment assigns a policy set definition (also known as an initiative).</span></span> <span data-ttu-id="d3262-120">L'ID riferimento per la definizione dei criteri indica quali criteri all'interno dell'iniziativa devono essere corretti.</span><span class="sxs-lookup"><span data-stu-id="d3262-120">The policy definition reference ID indicates which policy within the initiative should be remediated.</span></span>

### <span data-ttu-id="d3262-121">Esempio 4: avviare una correzione e attendere che venga completata in background</span><span class="sxs-lookup"><span data-stu-id="d3262-121">Example 4: Start a remediation and wait for it to complete in the background</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription f0710c27-9663-4c05-19f8-1b4be01e86a5
PS C:\> $job = Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -AsJob
PS C:\> $job | Wait-Job
PS C:\> $remediation = $job | Receive-Job
```

<span data-ttu-id="d3262-122">Questo comando avvia un nuovo aggiornamento dei criteri nell'abbonamento "abbonamento" per l'assegnazione di criteri specificata.</span><span class="sxs-lookup"><span data-stu-id="d3262-122">This command starts a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="d3262-123">Attenderà che il completamento della correzione venga completato prima di restituire lo stato di correzione finale.</span><span class="sxs-lookup"><span data-stu-id="d3262-123">It will wait for the remediation to complete before returning the final remediation status.</span></span>

## <span data-ttu-id="d3262-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d3262-124">PARAMETERS</span></span>

### <span data-ttu-id="d3262-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3262-125">-AsJob</span></span>
<span data-ttu-id="d3262-126">Esegui cmdlet in background.</span><span class="sxs-lookup"><span data-stu-id="d3262-126">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="d3262-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3262-127">-DefaultProfile</span></span>
<span data-ttu-id="d3262-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d3262-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3262-129">-LocationFilter</span><span class="sxs-lookup"><span data-stu-id="d3262-129">-LocationFilter</span></span>
<span data-ttu-id="d3262-130">Percorsi delle risorse che devono essere inclusi nella correzione.</span><span class="sxs-lookup"><span data-stu-id="d3262-130">The resource locations that should be included in the remediation.</span></span>
<span data-ttu-id="d3262-131">Le risorse che non si trovano in questi percorsi non verranno risanate.</span><span class="sxs-lookup"><span data-stu-id="d3262-131">Resources that don't reside in these locations will not be remediated.</span></span>

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

### <span data-ttu-id="d3262-132">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="d3262-132">-ManagementGroupName</span></span>
<span data-ttu-id="d3262-133">ID gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="d3262-133">Management group ID.</span></span>

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

### <span data-ttu-id="d3262-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="d3262-134">-Name</span></span>
<span data-ttu-id="d3262-135">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="d3262-135">Resource name.</span></span>

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

### <span data-ttu-id="d3262-136">-PolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="d3262-136">-PolicyAssignmentId</span></span>
<span data-ttu-id="d3262-137">ID assegnazione criteri.</span><span class="sxs-lookup"><span data-stu-id="d3262-137">Policy assignment ID.</span></span>
<span data-ttu-id="d3262-138">Ad esempio.</span><span class="sxs-lookup"><span data-stu-id="d3262-138">E.g.</span></span>
<span data-ttu-id="d3262-139">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span><span class="sxs-lookup"><span data-stu-id="d3262-139">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span></span>

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

### <span data-ttu-id="d3262-140">-PolicyDefinitionReferenceId</span><span class="sxs-lookup"><span data-stu-id="d3262-140">-PolicyDefinitionReferenceId</span></span>
<span data-ttu-id="d3262-141">Ottiene l'ID di riferimento per la definizione dei criteri della singola definizione da correggere.</span><span class="sxs-lookup"><span data-stu-id="d3262-141">Gets the policy definition reference ID of the individual definition that is being remediated.</span></span>
<span data-ttu-id="d3262-142">Obbligatorio quando l'assegnazione di criteri assegna una definizione di set di criteri.</span><span class="sxs-lookup"><span data-stu-id="d3262-142">Required when the policy assignment assigns a policy set definition.</span></span>

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

### <span data-ttu-id="d3262-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3262-143">-ResourceGroupName</span></span>
<span data-ttu-id="d3262-144">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d3262-144">Resource group name.</span></span>

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

### <span data-ttu-id="d3262-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3262-145">-ResourceId</span></span>
<span data-ttu-id="d3262-146">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="d3262-146">Resource ID.</span></span>

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

### <span data-ttu-id="d3262-147">-Ambito</span><span class="sxs-lookup"><span data-stu-id="d3262-147">-Scope</span></span>
<span data-ttu-id="d3262-148">Ambito della risorsa.</span><span class="sxs-lookup"><span data-stu-id="d3262-148">Scope of the resource.</span></span>
<span data-ttu-id="d3262-149">Ad esempio.</span><span class="sxs-lookup"><span data-stu-id="d3262-149">E.g.</span></span>
<span data-ttu-id="d3262-150">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="d3262-150">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="d3262-151">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d3262-151">-Confirm</span></span>
<span data-ttu-id="d3262-152">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3262-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3262-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3262-153">-WhatIf</span></span>
<span data-ttu-id="d3262-154">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d3262-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3262-155">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d3262-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3262-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3262-156">CommonParameters</span></span>
<span data-ttu-id="d3262-157">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3262-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3262-158">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3262-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3262-159">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d3262-159">INPUTS</span></span>

### <span data-ttu-id="d3262-160">System. String</span><span class="sxs-lookup"><span data-stu-id="d3262-160">System.String</span></span>

### <span data-ttu-id="d3262-161">System. String []</span><span class="sxs-lookup"><span data-stu-id="d3262-161">System.String[]</span></span>

## <span data-ttu-id="d3262-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3262-162">OUTPUTS</span></span>

### <span data-ttu-id="d3262-163">Microsoft. Azure. Commands. PolicyInsights. Models. remediation. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="d3262-163">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="d3262-164">Note</span><span class="sxs-lookup"><span data-stu-id="d3262-164">NOTES</span></span>

## <span data-ttu-id="d3262-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d3262-165">RELATED LINKS</span></span>
