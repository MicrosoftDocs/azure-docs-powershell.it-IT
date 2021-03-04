---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/get-azpolicystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
ms.openlocfilehash: 82aa08a3d4b4eb42638e1b9def55b5d936f176b8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989097"
---
# <span data-ttu-id="8c440-101">Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="8c440-101">Get-AzPolicyState</span></span>

## <span data-ttu-id="8c440-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c440-102">SYNOPSIS</span></span>
<span data-ttu-id="8c440-103">Ottiene gli stati di conformità dei criteri per le risorse.</span><span class="sxs-lookup"><span data-stu-id="8c440-103">Gets policy compliance states for resources.</span></span>

## <span data-ttu-id="8c440-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8c440-104">SYNTAX</span></span>

### <span data-ttu-id="8c440-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8c440-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c440-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="8c440-106">ManagementGroupScope</span></span>
```
Get-AzPolicyState [-All] -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c440-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="8c440-107">ResourceGroupScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c440-108">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="8c440-108">ResourceScope</span></span>
```
Get-AzPolicyState [-All] -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-Expand <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c440-109">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="8c440-109">PolicySetDefinitionScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c440-110">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="8c440-110">PolicyDefinitionScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c440-111">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="8c440-111">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c440-112">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="8c440-112">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c440-113">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8c440-113">DESCRIPTION</span></span>
<span data-ttu-id="8c440-114">Ottiene gli stati di conformità dei criteri per le risorse.</span><span class="sxs-lookup"><span data-stu-id="8c440-114">Gets policy compliance states for resources.</span></span> <span data-ttu-id="8c440-115">È possibile eseguire query sui record dello stato dei criteri in vari ambiti.</span><span class="sxs-lookup"><span data-stu-id="8c440-115">Policy state records can be queried at various scopes.</span></span> <span data-ttu-id="8c440-116">In base all'intervallo di tempo specificato (per impostazione predefinita, ultimo giorno), è possibile eseguire una query su tutti gli stati dei criteri o su tutte le transizioni dello stato dei criteri.</span><span class="sxs-lookup"><span data-stu-id="8c440-116">Based on the time interval specified (defaults to last day), either latest policy states or all policy state transitions can be queried.</span></span> <span data-ttu-id="8c440-117">È possibile filtrare, raggruppare e calcolare le aggregazioni di gruppi dei risultati.</span><span class="sxs-lookup"><span data-stu-id="8c440-117">Results can be filtered, grouped, and group aggregations can be computed.</span></span>

## <span data-ttu-id="8c440-118">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8c440-118">EXAMPLES</span></span>

### <span data-ttu-id="8c440-119">Esempio 1: Ottenere gli stati dei criteri più recenti nell'ambito della sottoscrizione corrente</span><span class="sxs-lookup"><span data-stu-id="8c440-119">Example 1: Get latest policy states in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyState
```

<span data-ttu-id="8c440-120">Recupera i record di stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse nella sottoscrizione nel contesto della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="8c440-120">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="8c440-121">Esempio 2: Ottenere gli stati dei criteri più recenti nell'ambito di sottoscrizione specificato</span><span class="sxs-lookup"><span data-stu-id="8c440-121">Example 2: Get latest policy states in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="8c440-122">Recupera i record di stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse nella sottoscrizione specificata.</span><span class="sxs-lookup"><span data-stu-id="8c440-122">Gets latest policy state records generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="8c440-123">Esempio 3: Ottenere tutti gli stati dei criteri nell'ambito di sottoscrizione corrente</span><span class="sxs-lookup"><span data-stu-id="8c440-123">Example 3: Get all policy states in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyState -All
```

<span data-ttu-id="8c440-124">Recupera tutti i record dello stato dei criteri cronologici (incluso l'ultimo) generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="8c440-124">Gets all historical policy state records (including latest) generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="8c440-125">Esempio 4: Ottenere gli stati dei criteri più recenti nell'ambito del gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="8c440-125">Example 4: Get latest policy states in management group scope</span></span>
```powershell
PS C:\> Get-AzPolicyState -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="8c440-126">Recupera i record di stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse all'interno del gruppo di gestione specificato.</span><span class="sxs-lookup"><span data-stu-id="8c440-126">Gets latest policy state records generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="8c440-127">Esempio 5: Ottenere gli stati dei criteri più recenti nell'ambito del gruppo di risorse nella sottoscrizione corrente</span><span class="sxs-lookup"><span data-stu-id="8c440-127">Example 5: Get latest policy states in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="8c440-128">Recupera i record di stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse all'interno del gruppo di risorse specificato (nella sottoscrizione nel contesto della sessione corrente).</span><span class="sxs-lookup"><span data-stu-id="8c440-128">Gets latest policy state records generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="8c440-129">Esempio 6: Ottenere gli stati dei criteri più recenti nell'ambito del gruppo di risorse nella sottoscrizione specificata</span><span class="sxs-lookup"><span data-stu-id="8c440-129">Example 6: Get latest policy states in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="8c440-130">Recupera i record di stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse all'interno del gruppo di risorse specificato (nella sottoscrizione specificata).</span><span class="sxs-lookup"><span data-stu-id="8c440-130">Gets latest policy state records generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="8c440-131">Esempio 7: Ottenere gli stati dei criteri più recenti per una risorsa</span><span class="sxs-lookup"><span data-stu-id="8c440-131">Example 7: Get latest policy states for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="8c440-132">Recupera i record di stato dei criteri più recenti generati nell'ultimo giorno per la risorsa specificata.</span><span class="sxs-lookup"><span data-stu-id="8c440-132">Gets latest policy state records generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="8c440-133">Esempio 8: Ottenere gli stati dei criteri più recenti per la definizione di un set di criteri nella sottoscrizione corrente</span><span class="sxs-lookup"><span data-stu-id="8c440-133">Example 8: Get latest policy states for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="8c440-134">Recupera i record dello stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) a cui è stata attivata la definizione del set di criteri specificata (presente nella sottoscrizione nel contesto della sessione corrente).</span><span class="sxs-lookup"><span data-stu-id="8c440-134">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="8c440-135">Esempio 9: Ottenere gli stati dei criteri più recenti per la definizione di un set di criteri nella sottoscrizione specificata</span><span class="sxs-lookup"><span data-stu-id="8c440-135">Example 9: Get latest policy states for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="8c440-136">Recupera i record dello stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) a cui è stata applicate la definizione del set di criteri specificata (esistente nella sottoscrizione specificata).</span><span class="sxs-lookup"><span data-stu-id="8c440-136">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="8c440-137">Esempio 10: Ottenere gli stati dei criteri più recenti per una definizione di criteri nella sottoscrizione corrente</span><span class="sxs-lookup"><span data-stu-id="8c440-137">Example 10: Get latest policy states for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="8c440-138">Recupera i record di stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) a cui è stata attivata la definizione dei criteri specificata (presente nella sottoscrizione nel contesto della sessione corrente).</span><span class="sxs-lookup"><span data-stu-id="8c440-138">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="8c440-139">Esempio 11: Ottenere gli stati dei criteri più recenti per una definizione di criteri nella sottoscrizione specificata</span><span class="sxs-lookup"><span data-stu-id="8c440-139">Example 11: Get latest policy states for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="8c440-140">Recupera i record di stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) a cui è stata attivata la definizione dei criteri specificata (esistente nella sottoscrizione specificata).</span><span class="sxs-lookup"><span data-stu-id="8c440-140">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="8c440-141">Esempio 12: Ottenere gli stati dei criteri più recenti per un'assegnazione di criteri nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="8c440-141">Example 12: Get latest policy states for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="8c440-142">Recupera i record dello stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) a cui è stata attivata l'assegnazione di criteri specificata (che esiste nella sottoscrizione nel contesto della sessione corrente).</span><span class="sxs-lookup"><span data-stu-id="8c440-142">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="8c440-143">Esempio 13: Ottenere gli stati dei criteri più recenti per un'assegnazione di criteri nella sottoscrizione specificata</span><span class="sxs-lookup"><span data-stu-id="8c440-143">Example 13: Get latest policy states for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="8c440-144">Recupera i record di stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) a cui è stata attivata l'assegnazione di criteri specificata (esistente nella sottoscrizione specificata).</span><span class="sxs-lookup"><span data-stu-id="8c440-144">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="8c440-145">Esempio 14: Ottenere gli stati dei criteri più recenti per un'assegnazione di criteri nel gruppo di risorse specificato nella sottoscrizione corrente</span><span class="sxs-lookup"><span data-stu-id="8c440-145">Example 14: Get latest policy states for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="8c440-146">Recupera i record di stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) esequisiti dall'assegnazione di criteri specificata (che esiste nel gruppo di risorse nella sottoscrizione nel contesto della sessione corrente).</span><span class="sxs-lookup"><span data-stu-id="8c440-146">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="8c440-147">Esempio 15: Ottenere gli stati dei criteri più recenti nell'ambito della sottoscrizione corrente, con le opzioni di query OrdinaPer, Principali e Seleziona</span><span class="sxs-lookup"><span data-stu-id="8c440-147">Example 15: Get latest policy states in current subscription scope, with OrderBy, Top and Select query options</span></span>
```powershell
PS C:\> Get-AzPolicyState -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId, IsCompliant"
```

<span data-ttu-id="8c440-148">Recupera i record di stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse nella sottoscrizione nel contesto della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="8c440-148">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="8c440-149">Il comando ordina i risultati in base alla data e ora e alle proprietà dei nomi delle assegnazioni dei criteri e accetta solo le prime 5 di quelle elencate in questo ordine.</span><span class="sxs-lookup"><span data-stu-id="8c440-149">The command orders the results by timestamp and policy assignment name properties, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="8c440-150">Si può anche selezionare di elencare solo un sottoinsieme di colonne per ogni record.</span><span class="sxs-lookup"><span data-stu-id="8c440-150">It also selects to list only a subset of the columns for each record.</span></span>

### <span data-ttu-id="8c440-151">Esempio 16: Ottenere gli stati dei criteri più recenti nell'ambito della sottoscrizione corrente, con le opzioni della query Da e A</span><span class="sxs-lookup"><span data-stu-id="8c440-151">Example 16: Get latest policy states in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzPolicyState -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="8c440-152">Recupera i record di stato dei criteri più recenti generati nell'intervallo di date specificato per tutte le risorse nella sottoscrizione nel contesto della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="8c440-152">Gets latest policy state records generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="8c440-153">Esempio 17: Ottenere gli stati dei criteri più recenti nell'ambito della sottoscrizione corrente, con l'opzione della query di filtro</span><span class="sxs-lookup"><span data-stu-id="8c440-153">Example 17: Get latest policy states in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ComplianceState eq 'NonCompliant' and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="8c440-154">Recupera i record di stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse nella sottoscrizione nel contesto della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="8c440-154">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="8c440-155">Il comando limita i risultati restituiti filtrando in base all'azione di definizione dei criteri (incluse le azioni di negazione o controllo), lo stato di conformità (include solo lo stato non conforme) e la posizione delle risorse (esclusa la posizione estus).</span><span class="sxs-lookup"><span data-stu-id="8c440-155">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions), compliance status (includes only non-compliant status) and resource location (excludes eastus location).</span></span>

### <span data-ttu-id="8c440-156">Esempio 18: Ottenere gli stati dei criteri più recenti nell'ambito della sottoscrizione corrente, con l'opzione Applica che specifica l'aggregazione del numero di righe</span><span class="sxs-lookup"><span data-stu-id="8c440-156">Example 18: Get latest policy states in current subscription scope, with Apply specifying row count aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyState -Apply "aggregate(`$count as NumberOfRecords)"
```

<span data-ttu-id="8c440-157">Ottiene il numero di record di stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse nella sottoscrizione nel contesto della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="8c440-157">Gets the number of latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="8c440-158">Il comando restituisce solo il conteggio dei record dello stato dei criteri, che viene restituito all'interno della proprietà AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="8c440-158">The command returns the count of the policy state records only, which is returned inside AdditionalProperties property.</span></span>

### <span data-ttu-id="8c440-159">Esempio 19: Ottenere gli stati dei criteri più recenti nell'ambito della sottoscrizione corrente, con Applica il raggruppamento specificato con aggregazione</span><span class="sxs-lookup"><span data-stu-id="8c440-159">Example 19: Get latest policy states in current subscription scope, with Apply specifying grouping with aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumStates))" -OrderBy "NumStates desc" -Top 5
```

<span data-ttu-id="8c440-160">Recupera i record di stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse nella sottoscrizione nel contesto della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="8c440-160">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="8c440-161">Il comando limita i risultati restituiti filtrando in base allo stato di conformità (include solo lo stato non conforme).</span><span class="sxs-lookup"><span data-stu-id="8c440-161">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="8c440-162">Raggruppa i risultati in base all'assegnazione dei criteri, alla definizione del set di criteri e alla definizione dei criteri e calcola il numero di record in ogni gruppo, che viene restituito all'interno della proprietà AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="8c440-162">It groups the results based on policy assignment, policy set definition, and policy definition, and computes the number of records in each group, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="8c440-163">Ordina i risultati in base all'aggregazione conteggio in ordine decrescente e accetta solo i primi 5 di quelli elencati in tale ordine.</span><span class="sxs-lookup"><span data-stu-id="8c440-163">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>

### <span data-ttu-id="8c440-164">Esempio 20: Ottenere gli stati dei criteri più recenti nell'ambito della sottoscrizione corrente, con Applica che specifica il raggruppamento senza aggregazione</span><span class="sxs-lookup"><span data-stu-id="8c440-164">Example 20: Get latest policy states in current subscription scope, with Apply specifying grouping without aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((ResourceId))"
```

<span data-ttu-id="8c440-165">Recupera i record di stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse nella sottoscrizione nel contesto della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="8c440-165">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="8c440-166">Il comando limita i risultati restituiti filtrando in base allo stato di conformità (include solo lo stato non conforme).</span><span class="sxs-lookup"><span data-stu-id="8c440-166">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="8c440-167">Raggruppa i risultati in base all'ID risorsa. In questo modo viene generato l'elenco di tutte le risorse all'interno della sottoscrizione non conformi ad almeno un criterio.</span><span class="sxs-lookup"><span data-stu-id="8c440-167">It groups the results based on resource id. This generates the list of all resources within the subscription that are non-compliant for at least one policy.</span></span>

### <span data-ttu-id="8c440-168">Esempio 21: Ottenere gli stati dei criteri più recenti nell'ambito della sottoscrizione corrente, con Applica che specifica più raggruppamenti</span><span class="sxs-lookup"><span data-stu-id="8c440-168">Example 21: Get latest policy states in current subscription scope, with Apply specifying multiple groupings</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumNonCompliantResources))" -OrderBy "NumNonCompliantResources desc" -Top 5
```

### <span data-ttu-id="8c440-169">Esempio 22: Ottenere gli stati dei criteri più recenti, inclusi i dettagli di valutazione dei criteri per una risorsa</span><span class="sxs-lookup"><span data-stu-id="8c440-169">Example 22: Get latest policy states including policy evaluation details for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1" -Expand "PolicyEvaluationDetails"
```

<span data-ttu-id="8c440-170">Recupera i record di stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse nella sottoscrizione nel contesto della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="8c440-170">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="8c440-171">Il comando limita i risultati restituiti filtrando in base allo stato di conformità (include solo lo stato non conforme).</span><span class="sxs-lookup"><span data-stu-id="8c440-171">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="8c440-172">Raggruppa prima i risultati in base all'assegnazione dei criteri, alla definizione del set di criteri, alla definizione del criterio e all'ID risorsa. Quindi, raggruppa ulteriormente i risultati di questo raggruppamento con le stesse proprietà tranne l'ID risorsa e calcola il numero di record in ognuno di questi gruppi, che viene restituito all'interno della proprietà AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="8c440-172">It groups the results first based on policy assignment, policy set definition, policy definition, and resource id. Then, it further groups the results of this grouping with the same properties except for resource id, and computes the number of records in each of these groups, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="8c440-173">Ordina i risultati in base all'aggregazione conteggio in ordine decrescente e accetta solo i primi 5 di quelli elencati in tale ordine.</span><span class="sxs-lookup"><span data-stu-id="8c440-173">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="8c440-174">In questo modo i 5 criteri principali vengono generati con il maggior numero di risorse non conformi.</span><span class="sxs-lookup"><span data-stu-id="8c440-174">This generates the top 5 policies with the most number of non-compliant resources.</span></span>

## <span data-ttu-id="8c440-175">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c440-175">PARAMETERS</span></span>

### <span data-ttu-id="8c440-176">-All</span><span class="sxs-lookup"><span data-stu-id="8c440-176">-All</span></span>
<span data-ttu-id="8c440-177">All'interno dell'intervallo di tempo specificato, ottenere tutti gli stati dei criteri anziché solo l'ultimo.</span><span class="sxs-lookup"><span data-stu-id="8c440-177">Within the specified time interval, get all policy states instead of the latest only.</span></span>

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

### <span data-ttu-id="8c440-178">-Applica</span><span class="sxs-lookup"><span data-stu-id="8c440-178">-Apply</span></span>
<span data-ttu-id="8c440-179">Applicare un'espressione per le aggregazioni usando la notazione OData.</span><span class="sxs-lookup"><span data-stu-id="8c440-179">Apply expression for aggregations using OData notation.</span></span>

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

### <span data-ttu-id="8c440-180">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c440-180">-DefaultProfile</span></span>
<span data-ttu-id="8c440-181">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8c440-181">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c440-182">-Expand</span><span class="sxs-lookup"><span data-stu-id="8c440-182">-Expand</span></span>
<span data-ttu-id="8c440-183">Espandere l'espressione usando la notazione OData.</span><span class="sxs-lookup"><span data-stu-id="8c440-183">Expand expression using OData notation.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c440-184">-Filter</span><span class="sxs-lookup"><span data-stu-id="8c440-184">-Filter</span></span>
<span data-ttu-id="8c440-185">Espressione di filtro con notazione OData.</span><span class="sxs-lookup"><span data-stu-id="8c440-185">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="8c440-186">-Da</span><span class="sxs-lookup"><span data-stu-id="8c440-186">-From</span></span>
<span data-ttu-id="8c440-187">Timestamp formattato ISO 8601 che specifica l'ora di inizio dell'intervallo in cui eseguire la query.</span><span class="sxs-lookup"><span data-stu-id="8c440-187">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="8c440-188">Se non è specificato, per impostazione predefinita viene utilizzato il valore del parametro "A" meno 1 giorno.</span><span class="sxs-lookup"><span data-stu-id="8c440-188">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c440-189">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="8c440-189">-ManagementGroupName</span></span>
<span data-ttu-id="8c440-190">Nome del gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="8c440-190">Management group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c440-191">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="8c440-191">-OrderBy</span></span>
<span data-ttu-id="8c440-192">Espressione di ordinamento con notazione OData.</span><span class="sxs-lookup"><span data-stu-id="8c440-192">Ordering expression using OData notation.</span></span>
<span data-ttu-id="8c440-193">Uno o più nomi di colonna separati da virgola con un valore facoltativo "desc" (impostazione predefinita) o "asc".</span><span class="sxs-lookup"><span data-stu-id="8c440-193">One or more comma-separated column names with an optional 'desc' (the default) or 'asc'.</span></span>

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

### <span data-ttu-id="8c440-194">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="8c440-194">-PolicyAssignmentName</span></span>
<span data-ttu-id="8c440-195">Nome dell'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="8c440-195">Policy assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelPolicyAssignmentScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c440-196">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="8c440-196">-PolicyDefinitionName</span></span>
<span data-ttu-id="8c440-197">Nome della definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="8c440-197">Policy definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyDefinitionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c440-198">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="8c440-198">-PolicySetDefinitionName</span></span>
<span data-ttu-id="8c440-199">Nome della definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="8c440-199">Policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicySetDefinitionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c440-200">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c440-200">-ResourceGroupName</span></span>
<span data-ttu-id="8c440-201">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8c440-201">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c440-202">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c440-202">-ResourceId</span></span>
<span data-ttu-id="8c440-203">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="8c440-203">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c440-204">-Select</span><span class="sxs-lookup"><span data-stu-id="8c440-204">-Select</span></span>
<span data-ttu-id="8c440-205">Espressione di selezione con notazione OData.</span><span class="sxs-lookup"><span data-stu-id="8c440-205">Select expression using OData notation.</span></span>
<span data-ttu-id="8c440-206">Uno o più nomi di colonna separati da virgola.</span><span class="sxs-lookup"><span data-stu-id="8c440-206">One or more comma-separated column names.</span></span>
<span data-ttu-id="8c440-207">Limita le colonne di ogni record solo a quelle richieste.</span><span class="sxs-lookup"><span data-stu-id="8c440-207">Limits the columns on each record to just those requested.</span></span>

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

### <span data-ttu-id="8c440-208">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8c440-208">-SubscriptionId</span></span>
<span data-ttu-id="8c440-209">ID abbonamento.</span><span class="sxs-lookup"><span data-stu-id="8c440-209">Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, ResourceGroupScope, PolicySetDefinitionScope, PolicyDefinitionScope, SubscriptionLevelPolicyAssignmentScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c440-210">-A</span><span class="sxs-lookup"><span data-stu-id="8c440-210">-To</span></span>
<span data-ttu-id="8c440-211">Timestamp formattato ISO 8601 che specifica l'ora di fine dell'intervallo in cui eseguire la query.</span><span class="sxs-lookup"><span data-stu-id="8c440-211">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="8c440-212">Se non è specificato, per impostazione predefinita viene visualizzato il momento della richiesta.</span><span class="sxs-lookup"><span data-stu-id="8c440-212">When not specified, defaults to time of request.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c440-213">-In alto</span><span class="sxs-lookup"><span data-stu-id="8c440-213">-Top</span></span>
<span data-ttu-id="8c440-214">Numero massimo di record da restituire.</span><span class="sxs-lookup"><span data-stu-id="8c440-214">Maximum number of records to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c440-215">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c440-215">CommonParameters</span></span>
<span data-ttu-id="8c440-216">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c440-216">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c440-217">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8c440-217">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c440-218">INPUT</span><span class="sxs-lookup"><span data-stu-id="8c440-218">INPUTS</span></span>

### <span data-ttu-id="8c440-219">System.String</span><span class="sxs-lookup"><span data-stu-id="8c440-219">System.String</span></span>

## <span data-ttu-id="8c440-220">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8c440-220">OUTPUTS</span></span>

### <span data-ttu-id="8c440-221">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyState</span><span class="sxs-lookup"><span data-stu-id="8c440-221">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyState</span></span>

## <span data-ttu-id="8c440-222">NOTE</span><span class="sxs-lookup"><span data-stu-id="8c440-222">NOTES</span></span>

## <span data-ttu-id="8c440-223">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8c440-223">RELATED LINKS</span></span>

[<span data-ttu-id="8c440-224">Get-AzPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="8c440-224">Get-AzPolicyStateSummary</span></span>](./Get-AzPolicyStateSummary.md)
