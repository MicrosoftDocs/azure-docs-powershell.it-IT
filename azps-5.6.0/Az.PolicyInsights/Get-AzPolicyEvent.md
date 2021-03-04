---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/get-azpolicyevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
ms.openlocfilehash: 7c9ee7af59acc90fba6a17e78ffd3dfc4822472d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989168"
---
# <span data-ttu-id="bcb38-101">Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="bcb38-101">Get-AzPolicyEvent</span></span>

## <span data-ttu-id="bcb38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcb38-102">SYNOPSIS</span></span>
<span data-ttu-id="bcb38-103">Recupera gli eventi di valutazione dei criteri generati quando le risorse vengono create o aggiornate.</span><span class="sxs-lookup"><span data-stu-id="bcb38-103">Gets policy evaluation events generated as resources are created or updated.</span></span>

## <span data-ttu-id="bcb38-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bcb38-104">SYNTAX</span></span>

### <span data-ttu-id="bcb38-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bcb38-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcb38-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="bcb38-106">ManagementGroupScope</span></span>
```
Get-AzPolicyEvent -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcb38-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="bcb38-107">ResourceGroupScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcb38-108">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="bcb38-108">PolicySetDefinitionScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcb38-109">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="bcb38-109">PolicyDefinitionScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcb38-110">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="bcb38-110">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcb38-111">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="bcb38-111">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcb38-112">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="bcb38-112">ResourceScope</span></span>
```
Get-AzPolicyEvent -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>]
 [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bcb38-113">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bcb38-113">DESCRIPTION</span></span>
<span data-ttu-id="bcb38-114">Recupera gli eventi di valutazione dei criteri generati quando le risorse vengono create o aggiornate.</span><span class="sxs-lookup"><span data-stu-id="bcb38-114">Gets policy evaluation events generated as resources are created or updated.</span></span> <span data-ttu-id="bcb38-115">È possibile eseguire query sui record di eventi dei criteri in vari ambiti in base all'intervallo di tempo specificato (l'impostazione predefinita è l'ultimo giorno).</span><span class="sxs-lookup"><span data-stu-id="bcb38-115">Policy event records can be queried at various scopes based on the time interval specified (defaults to last day).</span></span> <span data-ttu-id="bcb38-116">È possibile filtrare, raggruppare e calcolare le aggregazioni di gruppi dei risultati.</span><span class="sxs-lookup"><span data-stu-id="bcb38-116">Results can be filtered, grouped, and group aggregations can be computed.</span></span>

## <span data-ttu-id="bcb38-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bcb38-117">EXAMPLES</span></span>

### <span data-ttu-id="bcb38-118">Esempio 1: Ottenere eventi dei criteri nell'ambito della sottoscrizione corrente</span><span class="sxs-lookup"><span data-stu-id="bcb38-118">Example 1: Get policy events in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyEvent
```

<span data-ttu-id="bcb38-119">Recupera i record dell'evento dei criteri generati nell'ultimo giorno per tutte le risorse nella sottoscrizione nel contesto della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="bcb38-119">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="bcb38-120">Esempio 2: Ottenere eventi dei criteri nell'ambito di sottoscrizione specificato</span><span class="sxs-lookup"><span data-stu-id="bcb38-120">Example 2: Get policy events in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="bcb38-121">Ottiene i record dell'evento dei criteri generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione specificata.</span><span class="sxs-lookup"><span data-stu-id="bcb38-121">Gets policy event records generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="bcb38-122">Esempio 3: Ottenere eventi dei criteri nell'ambito del gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="bcb38-122">Example 3: Get policy events in management group scope</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="bcb38-123">Ottiene i record dell'evento dei criteri generati nell'ultimo giorno per tutte le risorse all'interno del gruppo di gestione specificato.</span><span class="sxs-lookup"><span data-stu-id="bcb38-123">Gets policy event records generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="bcb38-124">Esempio 4: Ottenere eventi dei criteri nell'ambito del gruppo di risorse nella sottoscrizione corrente</span><span class="sxs-lookup"><span data-stu-id="bcb38-124">Example 4: Get policy events in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="bcb38-125">Ottiene i record dell'evento dei criteri generati nell'ultimo giorno per tutte le risorse all'interno del gruppo di risorse specificato (nella sottoscrizione nel contesto della sessione corrente).</span><span class="sxs-lookup"><span data-stu-id="bcb38-125">Gets policy event records generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="bcb38-126">Esempio 5: Ottenere eventi dei criteri nell'ambito del gruppo di risorse nella sottoscrizione specificata</span><span class="sxs-lookup"><span data-stu-id="bcb38-126">Example 5: Get policy events in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="bcb38-127">Ottiene i record dell'evento dei criteri generati nell'ultimo giorno per tutte le risorse all'interno del gruppo di risorse specificato (nella sottoscrizione specificata).</span><span class="sxs-lookup"><span data-stu-id="bcb38-127">Gets policy event records generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="bcb38-128">Esempio 6: Ottenere eventi dei criteri per una risorsa</span><span class="sxs-lookup"><span data-stu-id="bcb38-128">Example 6: Get policy events for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="bcb38-129">Ottiene i record dell'evento dei criteri generati nell'ultimo giorno per la risorsa specificata.</span><span class="sxs-lookup"><span data-stu-id="bcb38-129">Gets policy event records generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="bcb38-130">Esempio 7: Ottenere eventi dei criteri per la definizione di un set di criteri nella sottoscrizione corrente</span><span class="sxs-lookup"><span data-stu-id="bcb38-130">Example 7: Get policy events for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="bcb38-131">Recupera i record dell'evento dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) a cui è stata attivata la definizione del set di criteri specificata (presente nella sottoscrizione nel contesto della sessione corrente).</span><span class="sxs-lookup"><span data-stu-id="bcb38-131">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="bcb38-132">Esempio 8: Ottenere eventi dei criteri per la definizione di un set di criteri nella sottoscrizione specificata</span><span class="sxs-lookup"><span data-stu-id="bcb38-132">Example 8: Get policy events for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="bcb38-133">Recupera i record di eventi dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) a cui è stata attivata la definizione del set di criteri specificata (esistente nella sottoscrizione specificata).</span><span class="sxs-lookup"><span data-stu-id="bcb38-133">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="bcb38-134">Esempio 9: Ottenere eventi dei criteri per una definizione di criteri nella sottoscrizione corrente</span><span class="sxs-lookup"><span data-stu-id="bcb38-134">Example 9: Get policy events for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="bcb38-135">Recupera i record dell'evento dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) a cui è stata attivata la definizione dei criteri specificata (presente nella sottoscrizione nel contesto della sessione corrente).</span><span class="sxs-lookup"><span data-stu-id="bcb38-135">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="bcb38-136">Esempio 10: Ottenere eventi dei criteri per una definizione di criteri nella sottoscrizione specificata</span><span class="sxs-lookup"><span data-stu-id="bcb38-136">Example 10: Get policy events for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="bcb38-137">Recupera i record dell'evento dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) a cui è stata attivata la definizione dei criteri specificata (esistente nella sottoscrizione specificata).</span><span class="sxs-lookup"><span data-stu-id="bcb38-137">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="bcb38-138">Esempio 11: Ottenere eventi dei criteri per un'assegnazione di criteri nella sottoscrizione corrente</span><span class="sxs-lookup"><span data-stu-id="bcb38-138">Example 11: Get policy events for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="bcb38-139">Recupera i record dell'evento dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) applicate dall'assegnazione di criteri specificata (che esiste nella sottoscrizione nel contesto della sessione corrente).</span><span class="sxs-lookup"><span data-stu-id="bcb38-139">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="bcb38-140">Esempio 12: Ottenere eventi dei criteri per un'assegnazione di criteri nella sottoscrizione specificata</span><span class="sxs-lookup"><span data-stu-id="bcb38-140">Example 12: Get policy events for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="bcb38-141">Recupera i record di eventi dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) applicate dall'assegnazione di criteri specificata (esistente nella sottoscrizione specificata).</span><span class="sxs-lookup"><span data-stu-id="bcb38-141">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="bcb38-142">Esempio 13: Ottenere eventi dei criteri per un'assegnazione di criteri nel gruppo di risorse specificato nella sottoscrizione corrente</span><span class="sxs-lookup"><span data-stu-id="bcb38-142">Example 13: Get policy events for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="bcb38-143">Recupera i record dell'evento dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) applicate dall'assegnazione di criteri specificata (presente nel gruppo di risorse nella sottoscrizione nel contesto della sessione corrente).</span><span class="sxs-lookup"><span data-stu-id="bcb38-143">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="bcb38-144">Esempio 14: Ottenere eventi dei criteri nell'ambito della sottoscrizione corrente, con le opzioni di query OrdinaPer, Principali e Seleziona</span><span class="sxs-lookup"><span data-stu-id="bcb38-144">Example 14: Get policy events in current subscription scope, with OrderBy, Top and Select query options</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId"
```

<span data-ttu-id="bcb38-145">Recupera i record dell'evento dei criteri generati nell'ultimo giorno per tutte le risorse nella sottoscrizione nel contesto della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="bcb38-145">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="bcb38-146">Il comando ordina i risultati in base alla data e ora e alle proprietà dei nomi delle assegnazioni dei criteri e accetta solo le prime 5 di quelle elencate in questo ordine.</span><span class="sxs-lookup"><span data-stu-id="bcb38-146">The command orders the results by timestamp and policy assignment name properties, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="bcb38-147">Si può anche selezionare di elencare solo un sottoinsieme di colonne per ogni record.</span><span class="sxs-lookup"><span data-stu-id="bcb38-147">It also selects to list only a subset of the columns for each record.</span></span>

### <span data-ttu-id="bcb38-148">Esempio 15: Ottenere eventi dei criteri nell'ambito della sottoscrizione corrente, con le opzioni della query Da e A</span><span class="sxs-lookup"><span data-stu-id="bcb38-148">Example 15: Get policy events in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="bcb38-149">Ottiene i record dell'evento dei criteri generati nell'intervallo di date specificato per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="bcb38-149">Gets policy event records generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="bcb38-150">Esempio 16: Ottenere eventi dei criteri nell'ambito della sottoscrizione corrente, con l'opzione della query di filtro</span><span class="sxs-lookup"><span data-stu-id="bcb38-150">Example 16: Get policy events in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="bcb38-151">Recupera i record dell'evento dei criteri generati nell'ultimo giorno per tutte le risorse nella sottoscrizione nel contesto della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="bcb38-151">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="bcb38-152">Il comando limita i risultati restituiti filtrando in base all'azione di definizione dei criteri (incluse le azioni di negazione o controllo) e alla posizione delle risorse (esclusa la posizione est).</span><span class="sxs-lookup"><span data-stu-id="bcb38-152">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions) and resource location (excludes eastus location).</span></span>

### <span data-ttu-id="bcb38-153">Esempio 17: Ottenere eventi dei criteri nell'ambito della sottoscrizione corrente, con l'opzione Applica che specifica l'aggregazione del numero di righe</span><span class="sxs-lookup"><span data-stu-id="bcb38-153">Example 17: Get policy events in current subscription scope, with Apply specifying row count aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Apply "aggregate(`$count as NumberOfRecords)"
```

<span data-ttu-id="bcb38-154">Ottiene il numero di record di eventi dei criteri generati nell'ultimo giorno per tutte le risorse nella sottoscrizione nel contesto della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="bcb38-154">Gets the number of policy event records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="bcb38-155">Il comando restituisce solo il conteggio dei record dell'evento dei criteri, che viene restituito all'interno della proprietà AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="bcb38-155">The command returns the count of the policy event records only, which is returned inside AdditionalProperties property.</span></span>

### <span data-ttu-id="bcb38-156">Esempio 18: Ottenere eventi dei criteri nell'ambito della sottoscrizione corrente, con Applica che specifica il raggruppamento con l'aggregazione</span><span class="sxs-lookup"><span data-stu-id="bcb38-156">Example 18: Get policy events in current subscription scope, with Apply specifying grouping with aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, PolicyDefinitionAction, ResourceId), aggregate(`$count as NumEvents))" -OrderBy "NumEvents desc" -Top 5
```

<span data-ttu-id="bcb38-157">Recupera i record dell'evento dei criteri generati nell'ultimo giorno per tutte le risorse nella sottoscrizione nel contesto della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="bcb38-157">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="bcb38-158">Il comando limita i risultati restituiti dal filtro in base all'azione di definizione dei criteri (include solo gli eventi di controllo e di negazione).</span><span class="sxs-lookup"><span data-stu-id="bcb38-158">The command limits the results returned by filtering based on policy definition action (includes only audit and deny events).</span></span>
<span data-ttu-id="bcb38-159">Raggruppa i risultati in base all'assegnazione dei criteri, alla definizione dei criteri, all'azione di definizione dei criteri e all'ID risorsa e calcola il numero di record in ogni gruppo, che viene restituito all'interno della proprietà AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="bcb38-159">It groups the results based on policy assignment, policy definition, policy definition action, and resource id, and computes the number of records in each group, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="bcb38-160">Ordina i risultati in base all'aggregazione conteggio in ordine decrescente e accetta solo i primi 5 di quelli elencati in tale ordine.</span><span class="sxs-lookup"><span data-stu-id="bcb38-160">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>

### <span data-ttu-id="bcb38-161">Esempio 19: Ottenere eventi dei criteri nell'ambito della sottoscrizione corrente, con Applica che specifica il raggruppamento senza aggregazione</span><span class="sxs-lookup"><span data-stu-id="bcb38-161">Example 19: Get policy events in current subscription scope, with Apply specifying grouping without aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((ResourceId))"
```

<span data-ttu-id="bcb38-162">Recupera i record dell'evento dei criteri generati nell'ultimo giorno per tutte le risorse nella sottoscrizione nel contesto della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="bcb38-162">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="bcb38-163">Il comando limita i risultati restituiti dal filtro in base all'azione di definizione dei criteri (include solo gli eventi di controllo e di negazione).</span><span class="sxs-lookup"><span data-stu-id="bcb38-163">The command limits the results returned by filtering based on policy definition action (includes only audit and deny events).</span></span>
<span data-ttu-id="bcb38-164">Raggruppa i risultati in base all'ID risorsa. In questo modo viene generato l'elenco di tutte le risorse all'interno della sottoscrizione che ha generato un evento dei criteri per almeno un criterio di controllo o di negazione.</span><span class="sxs-lookup"><span data-stu-id="bcb38-164">It groups the results based on resource id. This generates the list of all resources within the subscription that generated a policy event for at least one audit or deny policy.</span></span>

### <span data-ttu-id="bcb38-165">Esempio 20: Ottenere eventi dei criteri nell'ambito della sottoscrizione corrente, con Applica che specifica più raggruppamenti</span><span class="sxs-lookup"><span data-stu-id="bcb38-165">Example 20: Get policy events in current subscription scope, with Apply specifying multiple groupings</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicyDefinitionId), aggregate(`$count as NumDeniedResources))" -OrderBy "NumDeniedResources desc" -Top 5
```

<span data-ttu-id="bcb38-166">Recupera i record dell'evento dei criteri generati nell'ultimo giorno per tutte le risorse nella sottoscrizione nel contesto della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="bcb38-166">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="bcb38-167">Il comando limita i risultati restituiti dal filtro in base all'azione di definizione dei criteri (include solo gli eventi di negazione).</span><span class="sxs-lookup"><span data-stu-id="bcb38-167">The command limits the results returned by filtering based on policy definition action (includes only deny events).</span></span>
<span data-ttu-id="bcb38-168">Raggruppa prima i risultati in base all'assegnazione dei criteri, alla definizione dei criteri e all'ID risorsa. Quindi, raggruppa ulteriormente i risultati di questo raggruppamento con le stesse proprietà tranne l'ID risorsa e calcola il numero di record in ognuno di questi gruppi, che viene restituito all'interno della proprietà AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="bcb38-168">It groups the results first based on policy assignment, policy definition, and resource id. Then, it further groups the results of this grouping with the same properties except for resource id, and computes the number of records in each of these groups, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="bcb38-169">Ordina i risultati in base all'aggregazione conteggio in ordine decrescente e accetta solo i primi 5 di quelli elencati in tale ordine.</span><span class="sxs-lookup"><span data-stu-id="bcb38-169">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="bcb38-170">In questo modo vengono generati i 5 criteri di negazione principali con il maggior numero di risorse negate.</span><span class="sxs-lookup"><span data-stu-id="bcb38-170">This generates the top 5 deny policies with the most number of denied resources.</span></span>

## <span data-ttu-id="bcb38-171">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bcb38-171">PARAMETERS</span></span>

### <span data-ttu-id="bcb38-172">-Applica</span><span class="sxs-lookup"><span data-stu-id="bcb38-172">-Apply</span></span>
<span data-ttu-id="bcb38-173">Applicare un'espressione per le aggregazioni usando la notazione OData.</span><span class="sxs-lookup"><span data-stu-id="bcb38-173">Apply expression for aggregations using OData notation.</span></span>

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

### <span data-ttu-id="bcb38-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcb38-174">-DefaultProfile</span></span>
<span data-ttu-id="bcb38-175">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bcb38-175">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcb38-176">-Filter</span><span class="sxs-lookup"><span data-stu-id="bcb38-176">-Filter</span></span>
<span data-ttu-id="bcb38-177">Espressione di filtro con notazione OData.</span><span class="sxs-lookup"><span data-stu-id="bcb38-177">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="bcb38-178">-Da</span><span class="sxs-lookup"><span data-stu-id="bcb38-178">-From</span></span>
<span data-ttu-id="bcb38-179">Timestamp formattato ISO 8601 che specifica l'ora di inizio dell'intervallo in cui eseguire la query.</span><span class="sxs-lookup"><span data-stu-id="bcb38-179">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="bcb38-180">Se non è specificato, per impostazione predefinita viene utilizzato il valore del parametro "A" meno 1 giorno.</span><span class="sxs-lookup"><span data-stu-id="bcb38-180">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="bcb38-181">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="bcb38-181">-ManagementGroupName</span></span>
<span data-ttu-id="bcb38-182">Nome del gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="bcb38-182">Management group name.</span></span>

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

### <span data-ttu-id="bcb38-183">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="bcb38-183">-OrderBy</span></span>
<span data-ttu-id="bcb38-184">Espressione di ordinamento con notazione OData.</span><span class="sxs-lookup"><span data-stu-id="bcb38-184">Ordering expression using OData notation.</span></span>
<span data-ttu-id="bcb38-185">Uno o più nomi di colonna separati da virgola con un valore facoltativo "desc" (impostazione predefinita) o "asc".</span><span class="sxs-lookup"><span data-stu-id="bcb38-185">One or more comma-separated column names with an optional 'desc' (the default) or 'asc'.</span></span>

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

### <span data-ttu-id="bcb38-186">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="bcb38-186">-PolicyAssignmentName</span></span>
<span data-ttu-id="bcb38-187">Nome dell'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="bcb38-187">Policy assignment name.</span></span>

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

### <span data-ttu-id="bcb38-188">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="bcb38-188">-PolicyDefinitionName</span></span>
<span data-ttu-id="bcb38-189">Nome della definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="bcb38-189">Policy definition name.</span></span>

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

### <span data-ttu-id="bcb38-190">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="bcb38-190">-PolicySetDefinitionName</span></span>
<span data-ttu-id="bcb38-191">Nome della definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="bcb38-191">Policy set definition name.</span></span>

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

### <span data-ttu-id="bcb38-192">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcb38-192">-ResourceGroupName</span></span>
<span data-ttu-id="bcb38-193">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bcb38-193">Resource group name.</span></span>

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

### <span data-ttu-id="bcb38-194">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bcb38-194">-ResourceId</span></span>
<span data-ttu-id="bcb38-195">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="bcb38-195">Resource ID.</span></span>

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

### <span data-ttu-id="bcb38-196">-Select</span><span class="sxs-lookup"><span data-stu-id="bcb38-196">-Select</span></span>
<span data-ttu-id="bcb38-197">Espressione di selezione con notazione OData.</span><span class="sxs-lookup"><span data-stu-id="bcb38-197">Select expression using OData notation.</span></span>
<span data-ttu-id="bcb38-198">Uno o più nomi di colonna separati da virgola.</span><span class="sxs-lookup"><span data-stu-id="bcb38-198">One or more comma-separated column names.</span></span>
<span data-ttu-id="bcb38-199">Limita le colonne di ogni record solo a quelle richieste.</span><span class="sxs-lookup"><span data-stu-id="bcb38-199">Limits the columns on each record to just those requested.</span></span>

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

### <span data-ttu-id="bcb38-200">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bcb38-200">-SubscriptionId</span></span>
<span data-ttu-id="bcb38-201">ID abbonamento.</span><span class="sxs-lookup"><span data-stu-id="bcb38-201">Subscription ID.</span></span>

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

### <span data-ttu-id="bcb38-202">-A</span><span class="sxs-lookup"><span data-stu-id="bcb38-202">-To</span></span>
<span data-ttu-id="bcb38-203">Timestamp formattato ISO 8601 che specifica l'ora di fine dell'intervallo in cui eseguire la query.</span><span class="sxs-lookup"><span data-stu-id="bcb38-203">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="bcb38-204">Se non è specificato, per impostazione predefinita viene visualizzato il momento della richiesta.</span><span class="sxs-lookup"><span data-stu-id="bcb38-204">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="bcb38-205">-In alto</span><span class="sxs-lookup"><span data-stu-id="bcb38-205">-Top</span></span>
<span data-ttu-id="bcb38-206">Numero massimo di record da restituire.</span><span class="sxs-lookup"><span data-stu-id="bcb38-206">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="bcb38-207">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcb38-207">CommonParameters</span></span>
<span data-ttu-id="bcb38-208">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcb38-208">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcb38-209">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bcb38-209">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcb38-210">INPUT</span><span class="sxs-lookup"><span data-stu-id="bcb38-210">INPUTS</span></span>

### <span data-ttu-id="bcb38-211">System.String</span><span class="sxs-lookup"><span data-stu-id="bcb38-211">System.String</span></span>

## <span data-ttu-id="bcb38-212">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bcb38-212">OUTPUTS</span></span>

### <span data-ttu-id="bcb38-213">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyEvent</span><span class="sxs-lookup"><span data-stu-id="bcb38-213">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyEvent</span></span>

## <span data-ttu-id="bcb38-214">NOTE</span><span class="sxs-lookup"><span data-stu-id="bcb38-214">NOTES</span></span>

## <span data-ttu-id="bcb38-215">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bcb38-215">RELATED LINKS</span></span>
