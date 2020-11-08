---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicyevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
ms.openlocfilehash: 744618bb2cc12b4d57bfb1ed42267fcbbe7a86ab
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199496"
---
# <span data-ttu-id="4468f-101">Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="4468f-101">Get-AzPolicyEvent</span></span>

## <span data-ttu-id="4468f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4468f-102">SYNOPSIS</span></span>
<span data-ttu-id="4468f-103">Ottiene gli eventi di valutazione dei criteri generati come risorse create o aggiornate.</span><span class="sxs-lookup"><span data-stu-id="4468f-103">Gets policy evaluation events generated as resources are created or updated.</span></span>

## <span data-ttu-id="4468f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4468f-104">SYNTAX</span></span>

### <span data-ttu-id="4468f-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4468f-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4468f-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="4468f-106">ManagementGroupScope</span></span>
```
Get-AzPolicyEvent -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4468f-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="4468f-107">ResourceGroupScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4468f-108">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="4468f-108">PolicySetDefinitionScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4468f-109">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="4468f-109">PolicyDefinitionScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4468f-110">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="4468f-110">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4468f-111">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="4468f-111">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4468f-112">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="4468f-112">ResourceScope</span></span>
```
Get-AzPolicyEvent -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>]
 [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4468f-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4468f-113">DESCRIPTION</span></span>
<span data-ttu-id="4468f-114">Ottiene gli eventi di valutazione dei criteri generati come risorse create o aggiornate.</span><span class="sxs-lookup"><span data-stu-id="4468f-114">Gets policy evaluation events generated as resources are created or updated.</span></span> <span data-ttu-id="4468f-115">I record di eventi dei criteri possono essere interrogati in diversi ambiti in base all'intervallo di tempo specificato (impostazione predefinita per l'ultimo giorno).</span><span class="sxs-lookup"><span data-stu-id="4468f-115">Policy event records can be queried at various scopes based on the time interval specified (defaults to last day).</span></span> <span data-ttu-id="4468f-116">I risultati possono essere filtrati, raggruppati e le aggregazioni di gruppo possono essere calcolate.</span><span class="sxs-lookup"><span data-stu-id="4468f-116">Results can be filtered, grouped, and group aggregations can be computed.</span></span>

## <span data-ttu-id="4468f-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4468f-117">EXAMPLES</span></span>

### <span data-ttu-id="4468f-118">Esempio 1: ottenere gli eventi dei criteri nell'ambito corrente della sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="4468f-118">Example 1: Get policy events in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyEvent
```

<span data-ttu-id="4468f-119">Ottiene i record di eventi dei criteri generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="4468f-119">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="4468f-120">Esempio 2: ottenere gli eventi dei criteri nell'ambito dell'abbonamento specificato</span><span class="sxs-lookup"><span data-stu-id="4468f-120">Example 2: Get policy events in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="4468f-121">Ottiene i record di eventi dei criteri generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione specificata.</span><span class="sxs-lookup"><span data-stu-id="4468f-121">Gets policy event records generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="4468f-122">Esempio 3: ottenere gli eventi dei criteri nell'ambito del gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="4468f-122">Example 3: Get policy events in management group scope</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="4468f-123">Ottiene i record di eventi dei criteri generati nell'ultimo giorno per tutte le risorse all'interno del gruppo di gestione specificato.</span><span class="sxs-lookup"><span data-stu-id="4468f-123">Gets policy event records generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="4468f-124">Esempio 4: ottenere gli eventi dei criteri nell'ambito di un gruppo di risorse nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="4468f-124">Example 4: Get policy events in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="4468f-125">Ottiene i record di eventi dei criteri generati nell'ultimo giorno per tutte le risorse all'interno del gruppo di risorse specificato (nell'abbonamento nel contesto della sessione corrente).</span><span class="sxs-lookup"><span data-stu-id="4468f-125">Gets policy event records generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="4468f-126">Esempio 5: ottenere gli eventi dei criteri nell'ambito di un gruppo di risorse nell'abbonamento specificato</span><span class="sxs-lookup"><span data-stu-id="4468f-126">Example 5: Get policy events in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="4468f-127">Ottiene i record di eventi dei criteri generati nell'ultimo giorno per tutte le risorse all'interno del gruppo di risorse specificato (nell'abbonamento specificato).</span><span class="sxs-lookup"><span data-stu-id="4468f-127">Gets policy event records generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="4468f-128">Esempio 6: ottenere gli eventi dei criteri per una risorsa</span><span class="sxs-lookup"><span data-stu-id="4468f-128">Example 6: Get policy events for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="4468f-129">Ottiene i record di eventi dei criteri generati nell'ultimo giorno per la risorsa specificata.</span><span class="sxs-lookup"><span data-stu-id="4468f-129">Gets policy event records generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="4468f-130">Esempio 7: ottenere gli eventi dei criteri per una definizione di set di criteri nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="4468f-130">Example 7: Get policy events for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="4468f-131">Ottiene i record di eventi dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) effettuate dalla definizione del set di criteri specificata (che esiste nell'abbonamento nel contesto della sessione corrente).</span><span class="sxs-lookup"><span data-stu-id="4468f-131">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="4468f-132">Esempio 8: ottenere gli eventi dei criteri per una definizione di set di criteri nell'abbonamento specificato</span><span class="sxs-lookup"><span data-stu-id="4468f-132">Example 8: Get policy events for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="4468f-133">Ottiene i record di eventi dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) effettuate dalla definizione del set di criteri specificata (che esiste nell'abbonamento specificato).</span><span class="sxs-lookup"><span data-stu-id="4468f-133">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="4468f-134">Esempio 9: ottenere gli eventi dei criteri per una definizione di criterio nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="4468f-134">Example 9: Get policy events for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="4468f-135">Ottiene i record di eventi dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) effettuate dalla definizione di criteri specificata (che esiste nell'abbonamento nel contesto della sessione corrente).</span><span class="sxs-lookup"><span data-stu-id="4468f-135">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="4468f-136">Esempio 10: ottenere gli eventi dei criteri per una definizione di criterio nell'abbonamento specificato</span><span class="sxs-lookup"><span data-stu-id="4468f-136">Example 10: Get policy events for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="4468f-137">Ottiene i record di eventi dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) effettuate dalla definizione di criteri specificata (che esiste nell'abbonamento specificato).</span><span class="sxs-lookup"><span data-stu-id="4468f-137">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="4468f-138">Esempio 11: ottenere gli eventi dei criteri per un'assegnazione di criteri nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="4468f-138">Example 11: Get policy events for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="4468f-139">Ottiene i record di eventi dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) effettuate dall'assegnazione di criteri specificata (che esiste nell'abbonamento nel contesto della sessione corrente).</span><span class="sxs-lookup"><span data-stu-id="4468f-139">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="4468f-140">Esempio 12: ottenere gli eventi dei criteri per un'assegnazione di criteri nell'abbonamento specificato</span><span class="sxs-lookup"><span data-stu-id="4468f-140">Example 12: Get policy events for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="4468f-141">Ottiene i record di eventi dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) effettuate dall'assegnazione di criteri specificata (che esiste nell'abbonamento specificato).</span><span class="sxs-lookup"><span data-stu-id="4468f-141">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="4468f-142">Esempio 13: ottenere gli eventi dei criteri per un'assegnazione di criteri nel gruppo di risorse specificato nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="4468f-142">Example 13: Get policy events for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="4468f-143">Ottiene i record di eventi dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) effettuate dall'assegnazione di criteri specificata (esistente nel gruppo risorse della sottoscrizione nel contesto della sessione corrente).</span><span class="sxs-lookup"><span data-stu-id="4468f-143">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="4468f-144">Esempio 14: ottenere gli eventi dei criteri nell'ambito corrente della sottoscrizione, con le opzioni OrderBy, inizio e seleziona query</span><span class="sxs-lookup"><span data-stu-id="4468f-144">Example 14: Get policy events in current subscription scope, with OrderBy, Top and Select query options</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId"
```

<span data-ttu-id="4468f-145">Ottiene i record di eventi dei criteri generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="4468f-145">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="4468f-146">Il comando Ordina i risultati in base al timestamp e alle proprietà dei nomi delle assegnazioni di criteri e accetta solo i primi 5 di quelli elencati in quell'ordine.</span><span class="sxs-lookup"><span data-stu-id="4468f-146">The command orders the results by timestamp and policy assignment name properties, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="4468f-147">Viene inoltre selezionato per elencare solo un sottoinsieme delle colonne per ogni record.</span><span class="sxs-lookup"><span data-stu-id="4468f-147">It also selects to list only a subset of the columns for each record.</span></span>

### <span data-ttu-id="4468f-148">Esempio 15: ottenere eventi di criteri nell'ambito dell'abbonamento corrente, con le opzioni da e a query</span><span class="sxs-lookup"><span data-stu-id="4468f-148">Example 15: Get policy events in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="4468f-149">Ottiene i record di eventi dei criteri generati nell'intervallo di date specificato per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="4468f-149">Gets policy event records generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="4468f-150">Esempio 16: ottenere eventi di criteri nell'ambito dell'abbonamento corrente, con l'opzione di query di filtro</span><span class="sxs-lookup"><span data-stu-id="4468f-150">Example 16: Get policy events in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="4468f-151">Ottiene i record di eventi dei criteri generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="4468f-151">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="4468f-152">Il comando limita i risultati restituiti dal filtro in base all'azione di definizione dei criteri (include le azioni Deny o audit) e la posizione delle risorse (esclude la posizione eastus).</span><span class="sxs-lookup"><span data-stu-id="4468f-152">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions) and resource location (excludes eastus location).</span></span>

### <span data-ttu-id="4468f-153">Esempio 17: ottenere gli eventi dei criteri nell'ambito corrente della sottoscrizione, con l'applicazione specifica dell'aggregazione del conteggio righe</span><span class="sxs-lookup"><span data-stu-id="4468f-153">Example 17: Get policy events in current subscription scope, with Apply specifying row count aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Apply "aggregate(`$count as NumberOfRecords)"
```

<span data-ttu-id="4468f-154">Ottiene il numero di record di eventi dei criteri generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="4468f-154">Gets the number of policy event records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="4468f-155">Il comando restituisce solo il conteggio dei record di eventi del criterio, che viene restituito all'interno della proprietà AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="4468f-155">The command returns the count of the policy event records only, which is returned inside AdditionalProperties property.</span></span>

### <span data-ttu-id="4468f-156">Esempio 18: ottenere eventi di criteri nell'ambito dell'abbonamento corrente, con applica specificando il raggruppamento con l'aggregazione</span><span class="sxs-lookup"><span data-stu-id="4468f-156">Example 18: Get policy events in current subscription scope, with Apply specifying grouping with aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, PolicyDefinitionAction, ResourceId), aggregate(`$count as NumEvents))" -OrderBy "NumEvents desc" -Top 5
```

<span data-ttu-id="4468f-157">Ottiene i record di eventi dei criteri generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="4468f-157">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="4468f-158">Il comando limita i risultati restituiti dal filtro in base all'azione di definizione dei criteri (include solo gli eventi audit e Deny).</span><span class="sxs-lookup"><span data-stu-id="4468f-158">The command limits the results returned by filtering based on policy definition action (includes only audit and deny events).</span></span>
<span data-ttu-id="4468f-159">Raggruppa i risultati in base all'assegnazione dei criteri, alla definizione di criteri, all'azione di definizione dei criteri e all'ID delle risorse e calcola il numero di record in ogni gruppo, che viene restituito all'interno della proprietà AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="4468f-159">It groups the results based on policy assignment, policy definition, policy definition action, and resource id, and computes the number of records in each group, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="4468f-160">Ordina i risultati per l'aggregazione del conteggio in ordine decrescente e accetta solo i primi 5 di quelli elencati in quell'ordine.</span><span class="sxs-lookup"><span data-stu-id="4468f-160">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>

### <span data-ttu-id="4468f-161">Esempio 19: ottenere eventi di criteri nell'ambito dell'abbonamento corrente, con applica specifica del raggruppamento senza aggregazione</span><span class="sxs-lookup"><span data-stu-id="4468f-161">Example 19: Get policy events in current subscription scope, with Apply specifying grouping without aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((ResourceId))"
```

<span data-ttu-id="4468f-162">Ottiene i record di eventi dei criteri generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="4468f-162">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="4468f-163">Il comando limita i risultati restituiti dal filtro in base all'azione di definizione dei criteri (include solo gli eventi audit e Deny).</span><span class="sxs-lookup"><span data-stu-id="4468f-163">The command limits the results returned by filtering based on policy definition action (includes only audit and deny events).</span></span>
<span data-ttu-id="4468f-164">Raggruppa i risultati in base all'ID risorsa. In questo modo viene generato l'elenco di tutte le risorse dell'abbonamento che hanno generato un evento Policy per almeno un criterio di controllo o di negazione.</span><span class="sxs-lookup"><span data-stu-id="4468f-164">It groups the results based on resource id. This generates the list of all resources within the subscription that generated a policy event for at least one audit or deny policy.</span></span>

### <span data-ttu-id="4468f-165">Esempio 20: ottenere eventi di criteri nell'ambito corrente della sottoscrizione, con applica specificando più raggruppamenti</span><span class="sxs-lookup"><span data-stu-id="4468f-165">Example 20: Get policy events in current subscription scope, with Apply specifying multiple groupings</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicyDefinitionId), aggregate(`$count as NumDeniedResources))" -OrderBy "NumDeniedResources desc" -Top 5
```

<span data-ttu-id="4468f-166">Ottiene i record di eventi dei criteri generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="4468f-166">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="4468f-167">Il comando limita i risultati restituiti dal filtro in base all'azione di definizione dei criteri (include solo gli eventi Deny).</span><span class="sxs-lookup"><span data-stu-id="4468f-167">The command limits the results returned by filtering based on policy definition action (includes only deny events).</span></span>
<span data-ttu-id="4468f-168">Raggruppa i risultati per primi in base all'assegnazione dei criteri, alla definizione di criteri e all'ID risorsa. Viene quindi ulteriormente raggruppati i risultati di questo raggruppamento con le stesse proprietà eccetto l'ID risorsa e viene calcolato il numero di record in ognuno di questi gruppi, che viene restituito all'interno della proprietà AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="4468f-168">It groups the results first based on policy assignment, policy definition, and resource id. Then, it further groups the results of this grouping with the same properties except for resource id, and computes the number of records in each of these groups, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="4468f-169">Ordina i risultati per l'aggregazione del conteggio in ordine decrescente e accetta solo i primi 5 di quelli elencati in quell'ordine.</span><span class="sxs-lookup"><span data-stu-id="4468f-169">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="4468f-170">In questo articolo vengono generati i primi 5 criteri di negazione con il numero maggiore di risorse negate.</span><span class="sxs-lookup"><span data-stu-id="4468f-170">This generates the top 5 deny policies with the most number of denied resources.</span></span>

## <span data-ttu-id="4468f-171">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4468f-171">PARAMETERS</span></span>

### <span data-ttu-id="4468f-172">-Applica</span><span class="sxs-lookup"><span data-stu-id="4468f-172">-Apply</span></span>
<span data-ttu-id="4468f-173">Applicare l'espressione per le aggregazioni usando la notazione OData.</span><span class="sxs-lookup"><span data-stu-id="4468f-173">Apply expression for aggregations using OData notation.</span></span>

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

### <span data-ttu-id="4468f-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4468f-174">-DefaultProfile</span></span>
<span data-ttu-id="4468f-175">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4468f-175">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4468f-176">-Filtro</span><span class="sxs-lookup"><span data-stu-id="4468f-176">-Filter</span></span>
<span data-ttu-id="4468f-177">Filtrare l'espressione usando la notazione OData.</span><span class="sxs-lookup"><span data-stu-id="4468f-177">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="4468f-178">-Da</span><span class="sxs-lookup"><span data-stu-id="4468f-178">-From</span></span>
<span data-ttu-id="4468f-179">Timestamp formattato ISO 8601 che specifica l'ora di inizio dell'intervallo di query.</span><span class="sxs-lookup"><span data-stu-id="4468f-179">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="4468f-180">Se non viene specificato, il valore predefinito è "a" meno 1 giorno.</span><span class="sxs-lookup"><span data-stu-id="4468f-180">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="4468f-181">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="4468f-181">-ManagementGroupName</span></span>
<span data-ttu-id="4468f-182">Nome del gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="4468f-182">Management group name.</span></span>

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

### <span data-ttu-id="4468f-183">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="4468f-183">-OrderBy</span></span>
<span data-ttu-id="4468f-184">Espressione di ordinamento tramite notazione OData.</span><span class="sxs-lookup"><span data-stu-id="4468f-184">Ordering expression using OData notation.</span></span>
<span data-ttu-id="4468f-185">Uno o più nomi di colonna delimitati da virgole con un "DESC" facoltativo (impostazione predefinita) o "ASC".</span><span class="sxs-lookup"><span data-stu-id="4468f-185">One or more comma-separated column names with an optional 'desc' (the default) or 'asc'.</span></span>

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

### <span data-ttu-id="4468f-186">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="4468f-186">-PolicyAssignmentName</span></span>
<span data-ttu-id="4468f-187">Nome assegnazione criteri.</span><span class="sxs-lookup"><span data-stu-id="4468f-187">Policy assignment name.</span></span>

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

### <span data-ttu-id="4468f-188">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="4468f-188">-PolicyDefinitionName</span></span>
<span data-ttu-id="4468f-189">Nome definizione criterio.</span><span class="sxs-lookup"><span data-stu-id="4468f-189">Policy definition name.</span></span>

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

### <span data-ttu-id="4468f-190">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="4468f-190">-PolicySetDefinitionName</span></span>
<span data-ttu-id="4468f-191">Nome definizione set di criteri.</span><span class="sxs-lookup"><span data-stu-id="4468f-191">Policy set definition name.</span></span>

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

### <span data-ttu-id="4468f-192">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4468f-192">-ResourceGroupName</span></span>
<span data-ttu-id="4468f-193">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4468f-193">Resource group name.</span></span>

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

### <span data-ttu-id="4468f-194">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4468f-194">-ResourceId</span></span>
<span data-ttu-id="4468f-195">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="4468f-195">Resource ID.</span></span>

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

### <span data-ttu-id="4468f-196">-Selezionare</span><span class="sxs-lookup"><span data-stu-id="4468f-196">-Select</span></span>
<span data-ttu-id="4468f-197">Selezionare espressione usando la notazione OData.</span><span class="sxs-lookup"><span data-stu-id="4468f-197">Select expression using OData notation.</span></span>
<span data-ttu-id="4468f-198">Uno o più nomi di colonna delimitati da virgole.</span><span class="sxs-lookup"><span data-stu-id="4468f-198">One or more comma-separated column names.</span></span>
<span data-ttu-id="4468f-199">Limita le colonne di ogni record solo a quelle richieste.</span><span class="sxs-lookup"><span data-stu-id="4468f-199">Limits the columns on each record to just those requested.</span></span>

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

### <span data-ttu-id="4468f-200">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4468f-200">-SubscriptionId</span></span>
<span data-ttu-id="4468f-201">ID abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4468f-201">Subscription ID.</span></span>

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

### <span data-ttu-id="4468f-202">-To</span><span class="sxs-lookup"><span data-stu-id="4468f-202">-To</span></span>
<span data-ttu-id="4468f-203">Timestamp formattato ISO 8601 che specifica l'ora di fine dell'intervallo di query.</span><span class="sxs-lookup"><span data-stu-id="4468f-203">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="4468f-204">Se non viene specificato, il valore predefinito è l'ora della richiesta.</span><span class="sxs-lookup"><span data-stu-id="4468f-204">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="4468f-205">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="4468f-205">-Top</span></span>
<span data-ttu-id="4468f-206">Numero massimo di record da restituire.</span><span class="sxs-lookup"><span data-stu-id="4468f-206">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="4468f-207">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4468f-207">CommonParameters</span></span>
<span data-ttu-id="4468f-208">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4468f-208">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4468f-209">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4468f-209">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4468f-210">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4468f-210">INPUTS</span></span>

### <span data-ttu-id="4468f-211">System. String</span><span class="sxs-lookup"><span data-stu-id="4468f-211">System.String</span></span>

## <span data-ttu-id="4468f-212">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4468f-212">OUTPUTS</span></span>

### <span data-ttu-id="4468f-213">Microsoft. Azure. Commands. PolicyInsights. Models. PolicyEvent</span><span class="sxs-lookup"><span data-stu-id="4468f-213">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyEvent</span></span>

## <span data-ttu-id="4468f-214">Note</span><span class="sxs-lookup"><span data-stu-id="4468f-214">NOTES</span></span>

## <span data-ttu-id="4468f-215">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4468f-215">RELATED LINKS</span></span>
