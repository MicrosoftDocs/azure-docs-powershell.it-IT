---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/get-azurermpolicystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyState.md
ms.openlocfilehash: 6f5f1c341db0c5f57ffb541b9455369c0c6e5ab0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685765"
---
# <span data-ttu-id="e53dc-101">Get-AzureRmPolicyState</span><span class="sxs-lookup"><span data-stu-id="e53dc-101">Get-AzureRmPolicyState</span></span>

## <span data-ttu-id="e53dc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e53dc-102">SYNOPSIS</span></span>
<span data-ttu-id="e53dc-103">Ottiene gli Stati di conformità dei criteri per le risorse.</span><span class="sxs-lookup"><span data-stu-id="e53dc-103">Gets policy compliance states for resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e53dc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e53dc-104">SYNTAX</span></span>

### <span data-ttu-id="e53dc-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e53dc-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmPolicyState [-All] [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e53dc-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="e53dc-106">ManagementGroupScope</span></span>
```
Get-AzureRmPolicyState [-All] -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e53dc-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="e53dc-107">ResourceGroupScope</span></span>
```
Get-AzureRmPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e53dc-108">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="e53dc-108">ResourceScope</span></span>
```
Get-AzureRmPolicyState [-All] -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e53dc-109">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="e53dc-109">PolicySetDefinitionScope</span></span>
```
Get-AzureRmPolicyState [-All] [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e53dc-110">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="e53dc-110">PolicyDefinitionScope</span></span>
```
Get-AzureRmPolicyState [-All] [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e53dc-111">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="e53dc-111">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzureRmPolicyState [-All] [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e53dc-112">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="e53dc-112">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzureRmPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String>
 -PolicyAssignmentName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>]
 [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e53dc-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e53dc-113">DESCRIPTION</span></span>
<span data-ttu-id="e53dc-114">Ottiene gli Stati di conformità dei criteri per le risorse.</span><span class="sxs-lookup"><span data-stu-id="e53dc-114">Gets policy compliance states for resources.</span></span> <span data-ttu-id="e53dc-115">I record di stato dei criteri possono essere interrogati in diversi ambiti.</span><span class="sxs-lookup"><span data-stu-id="e53dc-115">Policy state records can be queried at various scopes.</span></span> <span data-ttu-id="e53dc-116">In base all'intervallo di tempo specificato (il valore predefinito è l'ultimo giorno), è possibile eseguire query sugli stati dei criteri più recenti o su tutte le transizioni di stato dei criteri.</span><span class="sxs-lookup"><span data-stu-id="e53dc-116">Based on the time interval specified (defaults to last day), either latest policy states or all policy state transitions can be queried.</span></span> <span data-ttu-id="e53dc-117">I risultati possono essere filtrati, raggruppati e le aggregazioni di gruppo possono essere calcolate.</span><span class="sxs-lookup"><span data-stu-id="e53dc-117">Results can be filtered, grouped, and group aggregations can be computed.</span></span>

## <span data-ttu-id="e53dc-118">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e53dc-118">EXAMPLES</span></span>

### <span data-ttu-id="e53dc-119">Esempio 1: ottenere gli ultimi stati dei criteri nell'ambito corrente della sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="e53dc-119">Example 1: Get latest policy states in current subscription scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState
```

<span data-ttu-id="e53dc-120">Ottiene i record dello stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="e53dc-120">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="e53dc-121">Esempio 2: ottenere gli ultimi stati dei criteri nell'ambito dell'abbonamento specificato</span><span class="sxs-lookup"><span data-stu-id="e53dc-121">Example 2: Get latest policy states in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="e53dc-122">Ottiene i record dello stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione specificata.</span><span class="sxs-lookup"><span data-stu-id="e53dc-122">Gets latest policy state records generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="e53dc-123">Esempio 3: ottenere tutti gli Stati dei criteri nell'ambito corrente della sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="e53dc-123">Example 3: Get all policy states in current subscription scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -All
```

<span data-ttu-id="e53dc-124">Ottiene tutti i record di stato del criterio cronologico (incluso il più recente) generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="e53dc-124">Gets all historical policy state records (including latest) generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="e53dc-125">Esempio 4: ottenere gli ultimi stati dei criteri nell'ambito del gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="e53dc-125">Example 4: Get latest policy states in management group scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="e53dc-126">Ottiene i record dello stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse all'interno del gruppo di gestione specificato.</span><span class="sxs-lookup"><span data-stu-id="e53dc-126">Gets latest policy state records generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="e53dc-127">Esempio 5: ottenere gli ultimi stati dei criteri nell'ambito di un gruppo di risorse nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="e53dc-127">Example 5: Get latest policy states in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="e53dc-128">Ottiene i record dello stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse all'interno del gruppo di risorse specificato (nell'abbonamento nel contesto della sessione corrente).</span><span class="sxs-lookup"><span data-stu-id="e53dc-128">Gets latest policy state records generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="e53dc-129">Esempio 6: ottenere gli ultimi stati dei criteri nell'ambito di un gruppo di risorse nell'abbonamento specificato</span><span class="sxs-lookup"><span data-stu-id="e53dc-129">Example 6: Get latest policy states in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="e53dc-130">Ottiene i record dello stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse all'interno del gruppo di risorse specificato (nell'abbonamento specificato).</span><span class="sxs-lookup"><span data-stu-id="e53dc-130">Gets latest policy state records generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="e53dc-131">Esempio 7: ottenere gli ultimi stati dei criteri per una risorsa</span><span class="sxs-lookup"><span data-stu-id="e53dc-131">Example 7: Get latest policy states for a resource</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="e53dc-132">Ottiene i record dello stato dei criteri più recenti generati nell'ultimo giorno per la risorsa specificata.</span><span class="sxs-lookup"><span data-stu-id="e53dc-132">Gets latest policy state records generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="e53dc-133">Esempio 8: ottenere gli ultimi stati dei criteri per una definizione di set di criteri nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="e53dc-133">Example 8: Get latest policy states for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="e53dc-134">Ottiene i record dello stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) effettuate dalla definizione del set di criteri specificata (che esiste nell'abbonamento nel contesto della sessione corrente).</span><span class="sxs-lookup"><span data-stu-id="e53dc-134">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="e53dc-135">Esempio 9: ottenere gli Stati dei criteri più recenti per una definizione di set di criteri nell'abbonamento specificato</span><span class="sxs-lookup"><span data-stu-id="e53dc-135">Example 9: Get latest policy states for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="e53dc-136">Ottiene i record dello stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) effettuate dalla definizione del set di criteri specificata (che esiste nell'abbonamento specificato).</span><span class="sxs-lookup"><span data-stu-id="e53dc-136">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="e53dc-137">Esempio 10: ottenere gli Stati dei criteri più recenti per una definizione di criteri nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="e53dc-137">Example 10: Get latest policy states for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="e53dc-138">Ottiene i record dello stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) effettuate dalla definizione di criteri specificata (che esiste nell'abbonamento nel contesto della sessione corrente).</span><span class="sxs-lookup"><span data-stu-id="e53dc-138">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="e53dc-139">Esempio 11: ottenere gli ultimi stati dei criteri per una definizione di criterio nell'abbonamento specificato</span><span class="sxs-lookup"><span data-stu-id="e53dc-139">Example 11: Get latest policy states for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="e53dc-140">Ottiene i record dello stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) effettuate dalla definizione di criteri specificata (che esiste nell'abbonamento specificato).</span><span class="sxs-lookup"><span data-stu-id="e53dc-140">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="e53dc-141">Esempio 12: ottenere gli ultimi stati dei criteri per un'assegnazione di criteri nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="e53dc-141">Example 12: Get latest policy states for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="e53dc-142">Ottiene i record dello stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) effettuate dall'assegnazione di criteri specificata (che esiste nell'abbonamento nel contesto della sessione corrente).</span><span class="sxs-lookup"><span data-stu-id="e53dc-142">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="e53dc-143">Esempio 13: ottenere gli ultimi stati dei criteri per un'assegnazione di criteri nell'abbonamento specificato</span><span class="sxs-lookup"><span data-stu-id="e53dc-143">Example 13: Get latest policy states for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="e53dc-144">Ottiene i record dello stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) effettuate dall'assegnazione di criteri specificata (che esiste nell'abbonamento specificato).</span><span class="sxs-lookup"><span data-stu-id="e53dc-144">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="e53dc-145">Esempio 14: ottenere gli ultimi stati dei criteri per un'assegnazione di criteri nel gruppo di risorse specificato nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="e53dc-145">Example 14: Get latest policy states for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="e53dc-146">Ottiene i record dello stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) effettuate dall'assegnazione di criteri specificata (esistente nel gruppo risorse della sottoscrizione nel contesto della sessione corrente).</span><span class="sxs-lookup"><span data-stu-id="e53dc-146">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="e53dc-147">Esempio 15: ottenere gli ultimi stati dei criteri nell'ambito dell'abbonamento corrente, con le opzioni OrderBy, inizio e seleziona query</span><span class="sxs-lookup"><span data-stu-id="e53dc-147">Example 15: Get latest policy states in current subscription scope, with OrderBy, Top and Select query options</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId, IsCompliant"
```

<span data-ttu-id="e53dc-148">Ottiene i record dello stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="e53dc-148">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="e53dc-149">Il comando Ordina i risultati in base al timestamp e alle proprietà dei nomi delle assegnazioni di criteri e accetta solo i primi 5 di quelli elencati in quell'ordine.</span><span class="sxs-lookup"><span data-stu-id="e53dc-149">The command orders the results by timestamp and policy assignment name properties, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="e53dc-150">Viene inoltre selezionato per elencare solo un sottoinsieme delle colonne per ogni record.</span><span class="sxs-lookup"><span data-stu-id="e53dc-150">It also selects to list only a subset of the columns for each record.</span></span>

### <span data-ttu-id="e53dc-151">Esempio 16: ottenere gli ultimi stati dei criteri nell'ambito dell'abbonamento corrente, con le opzioni da e a query</span><span class="sxs-lookup"><span data-stu-id="e53dc-151">Example 16: Get latest policy states in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="e53dc-152">Ottiene i record dello stato dei criteri più recenti generati nell'intervallo di date specificato per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="e53dc-152">Gets latest policy state records generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="e53dc-153">Esempio 17: ottenere gli ultimi stati dei criteri nell'ambito dell'abbonamento corrente, con l'opzione di query di filtro</span><span class="sxs-lookup"><span data-stu-id="e53dc-153">Example 17: Get latest policy states in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and IsCompliant eq false and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="e53dc-154">Ottiene i record dello stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="e53dc-154">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="e53dc-155">Il comando limita i risultati restituiti dal filtro in base all'azione di definizione dei criteri (include le azioni Deny o audit), lo stato di conformità (include solo lo stato non conforme) e la posizione delle risorse (esclude la posizione eastus).</span><span class="sxs-lookup"><span data-stu-id="e53dc-155">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions), compliance status (includes only non-compliant status) and resource location (excludes eastus location).</span></span>

### <span data-ttu-id="e53dc-156">Esempio 18: ottenere gli ultimi stati dei criteri nell'ambito dell'abbonamento corrente, con l'applicazione specifica dell'aggregazione del conteggio righe</span><span class="sxs-lookup"><span data-stu-id="e53dc-156">Example 18: Get latest policy states in current subscription scope, with Apply specifying row count aggregation</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -Apply "aggregate(`$count as NumberOfRecords)"
```

<span data-ttu-id="e53dc-157">Ottiene il numero di record di stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="e53dc-157">Gets the number of latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="e53dc-158">Il comando restituisce solo il conteggio dei record dello stato del criterio, che viene restituito all'interno della proprietà AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="e53dc-158">The command returns the count of the policy state records only, which is returned inside AdditionalProperties property.</span></span>

### <span data-ttu-id="e53dc-159">Esempio 19: ottenere gli ultimi stati dei criteri nell'ambito dell'abbonamento corrente, con applica specificando il raggruppamento con l'aggregazione</span><span class="sxs-lookup"><span data-stu-id="e53dc-159">Example 19: Get latest policy states in current subscription scope, with Apply specifying grouping with aggregation</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -Filter "IsCompliant eq false" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumStates))" -OrderBy "NumStates desc" -Top 5
```

<span data-ttu-id="e53dc-160">Ottiene i record dello stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="e53dc-160">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="e53dc-161">Il comando limita i risultati restituiti dal filtro in base allo stato di conformità (include solo lo stato non conforme).</span><span class="sxs-lookup"><span data-stu-id="e53dc-161">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="e53dc-162">Raggruppa i risultati in base all'assegnazione dei criteri, alla definizione del set di criteri e alla definizione dei criteri e calcola il numero di record in ogni gruppo, che viene restituito all'interno della proprietà AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="e53dc-162">It groups the results based on policy assignment, policy set definition, and policy definition, and computes the number of records in each group, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="e53dc-163">Ordina i risultati per l'aggregazione del conteggio in ordine decrescente e accetta solo i primi 5 di quelli elencati in quell'ordine.</span><span class="sxs-lookup"><span data-stu-id="e53dc-163">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>

### <span data-ttu-id="e53dc-164">Esempio 20: ottenere gli Stati dei criteri più recenti nell'ambito dell'abbonamento corrente, con applica specificando il raggruppamento senza aggregazione</span><span class="sxs-lookup"><span data-stu-id="e53dc-164">Example 20: Get latest policy states in current subscription scope, with Apply specifying grouping without aggregation</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -Filter "IsCompliant eq false" -Apply "groupby((ResourceId))"
```

<span data-ttu-id="e53dc-165">Ottiene i record dello stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="e53dc-165">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="e53dc-166">Il comando limita i risultati restituiti dal filtro in base allo stato di conformità (include solo lo stato non conforme).</span><span class="sxs-lookup"><span data-stu-id="e53dc-166">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="e53dc-167">Raggruppa i risultati in base all'ID risorsa. In questo articolo viene generato l'elenco di tutte le risorse all'interno dell'abbonamento che non sono conformi per almeno un criterio.</span><span class="sxs-lookup"><span data-stu-id="e53dc-167">It groups the results based on resource id. This generates the list of all resources within the subscription that are non-compliant for at least one policy.</span></span>

### <span data-ttu-id="e53dc-168">Esempio 21: ottenere gli ultimi stati dei criteri nell'ambito corrente della sottoscrizione, con applica specificando più raggruppamenti</span><span class="sxs-lookup"><span data-stu-id="e53dc-168">Example 21: Get latest policy states in current subscription scope, with Apply specifying multiple groupings</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -Filter "IsCompliant eq false" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumNonCompliantResources))" -OrderBy "NumNonCompliantResources desc" -Top 5
```

<span data-ttu-id="e53dc-169">Ottiene i record dello stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="e53dc-169">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="e53dc-170">Il comando limita i risultati restituiti dal filtro in base allo stato di conformità (include solo lo stato non conforme).</span><span class="sxs-lookup"><span data-stu-id="e53dc-170">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="e53dc-171">Raggruppa i risultati in base all'assegnazione dei criteri, alla definizione del set di criteri, alla definizione dei criteri e all'ID risorsa. Viene quindi ulteriormente raggruppati i risultati di questo raggruppamento con le stesse proprietà eccetto l'ID risorsa e viene calcolato il numero di record in ognuno di questi gruppi, che viene restituito all'interno della proprietà AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="e53dc-171">It groups the results first based on policy assignment, policy set definition, policy definition, and resource id. Then, it further groups the results of this grouping with the same properties except for resource id, and computes the number of records in each of these groups, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="e53dc-172">Ordina i risultati per l'aggregazione del conteggio in ordine decrescente e accetta solo i primi 5 di quelli elencati in quell'ordine.</span><span class="sxs-lookup"><span data-stu-id="e53dc-172">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="e53dc-173">Vengono generati i primi 5 criteri con il maggior numero di risorse non conformi.</span><span class="sxs-lookup"><span data-stu-id="e53dc-173">This generates the top 5 policies with the most number of non-compliant resources.</span></span>

## <span data-ttu-id="e53dc-174">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e53dc-174">PARAMETERS</span></span>

### <span data-ttu-id="e53dc-175">-Tutti</span><span class="sxs-lookup"><span data-stu-id="e53dc-175">-All</span></span>
<span data-ttu-id="e53dc-176">Nell'intervallo di tempo specificato, ottenere tutti gli Stati dei criteri al posto della versione più recente.</span><span class="sxs-lookup"><span data-stu-id="e53dc-176">Within the specified time interval, get all policy states instead of the latest only.</span></span>

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

### <span data-ttu-id="e53dc-177">-Applica</span><span class="sxs-lookup"><span data-stu-id="e53dc-177">-Apply</span></span>
<span data-ttu-id="e53dc-178">Applicare l'espressione per le aggregazioni usando la notazione OData.</span><span class="sxs-lookup"><span data-stu-id="e53dc-178">Apply expression for aggregations using OData notation.</span></span>

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

### <span data-ttu-id="e53dc-179">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e53dc-179">-DefaultProfile</span></span>
<span data-ttu-id="e53dc-180">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e53dc-180">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e53dc-181">-Filtro</span><span class="sxs-lookup"><span data-stu-id="e53dc-181">-Filter</span></span>
<span data-ttu-id="e53dc-182">Filtrare l'espressione usando la notazione OData.</span><span class="sxs-lookup"><span data-stu-id="e53dc-182">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="e53dc-183">-Da</span><span class="sxs-lookup"><span data-stu-id="e53dc-183">-From</span></span>
<span data-ttu-id="e53dc-184">Timestamp formattato ISO 8601 che specifica l'ora di inizio dell'intervallo di query.</span><span class="sxs-lookup"><span data-stu-id="e53dc-184">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="e53dc-185">Se non viene specificato, il valore predefinito è "a" meno 1 giorno.</span><span class="sxs-lookup"><span data-stu-id="e53dc-185">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="e53dc-186">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="e53dc-186">-ManagementGroupName</span></span>
<span data-ttu-id="e53dc-187">Nome del gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="e53dc-187">Management group name.</span></span>

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

### <span data-ttu-id="e53dc-188">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="e53dc-188">-OrderBy</span></span>
<span data-ttu-id="e53dc-189">Espressione di ordinamento tramite notazione OData.</span><span class="sxs-lookup"><span data-stu-id="e53dc-189">Ordering expression using OData notation.</span></span>
<span data-ttu-id="e53dc-190">Uno o più nomi di colonna delimitati da virgole con un "DESC" facoltativo (impostazione predefinita) o "ASC".</span><span class="sxs-lookup"><span data-stu-id="e53dc-190">One or more comma-separated column names with an optional 'desc' (the default) or 'asc'.</span></span>

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

### <span data-ttu-id="e53dc-191">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="e53dc-191">-PolicyAssignmentName</span></span>
<span data-ttu-id="e53dc-192">Nome assegnazione criteri.</span><span class="sxs-lookup"><span data-stu-id="e53dc-192">Policy assignment name.</span></span>

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

### <span data-ttu-id="e53dc-193">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="e53dc-193">-PolicyDefinitionName</span></span>
<span data-ttu-id="e53dc-194">Nome definizione criterio.</span><span class="sxs-lookup"><span data-stu-id="e53dc-194">Policy definition name.</span></span>

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

### <span data-ttu-id="e53dc-195">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="e53dc-195">-PolicySetDefinitionName</span></span>
<span data-ttu-id="e53dc-196">Nome definizione set di criteri.</span><span class="sxs-lookup"><span data-stu-id="e53dc-196">Policy set definition name.</span></span>

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

### <span data-ttu-id="e53dc-197">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e53dc-197">-ResourceGroupName</span></span>
<span data-ttu-id="e53dc-198">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e53dc-198">Resource group name.</span></span>

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

### <span data-ttu-id="e53dc-199">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e53dc-199">-ResourceId</span></span>
<span data-ttu-id="e53dc-200">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="e53dc-200">Resource ID.</span></span>

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

### <span data-ttu-id="e53dc-201">-Selezionare</span><span class="sxs-lookup"><span data-stu-id="e53dc-201">-Select</span></span>
<span data-ttu-id="e53dc-202">Selezionare espressione usando la notazione OData.</span><span class="sxs-lookup"><span data-stu-id="e53dc-202">Select expression using OData notation.</span></span>
<span data-ttu-id="e53dc-203">Uno o più nomi di colonna delimitati da virgole.</span><span class="sxs-lookup"><span data-stu-id="e53dc-203">One or more comma-separated column names.</span></span>
<span data-ttu-id="e53dc-204">Limita le colonne di ogni record solo a quelle richieste.</span><span class="sxs-lookup"><span data-stu-id="e53dc-204">Limits the columns on each record to just those requested.</span></span>

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

### <span data-ttu-id="e53dc-205">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e53dc-205">-SubscriptionId</span></span>
<span data-ttu-id="e53dc-206">ID abbonamento.</span><span class="sxs-lookup"><span data-stu-id="e53dc-206">Subscription ID.</span></span>

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

### <span data-ttu-id="e53dc-207">-To</span><span class="sxs-lookup"><span data-stu-id="e53dc-207">-To</span></span>
<span data-ttu-id="e53dc-208">Timestamp formattato ISO 8601 che specifica l'ora di fine dell'intervallo di query.</span><span class="sxs-lookup"><span data-stu-id="e53dc-208">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="e53dc-209">Se non viene specificato, il valore predefinito è l'ora della richiesta.</span><span class="sxs-lookup"><span data-stu-id="e53dc-209">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="e53dc-210">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="e53dc-210">-Top</span></span>
<span data-ttu-id="e53dc-211">Numero massimo di record da restituire.</span><span class="sxs-lookup"><span data-stu-id="e53dc-211">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="e53dc-212">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e53dc-212">CommonParameters</span></span>
<span data-ttu-id="e53dc-213">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e53dc-213">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e53dc-214">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e53dc-214">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e53dc-215">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e53dc-215">INPUTS</span></span>

### <span data-ttu-id="e53dc-216">System. String</span><span class="sxs-lookup"><span data-stu-id="e53dc-216">System.String</span></span>

## <span data-ttu-id="e53dc-217">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e53dc-217">OUTPUTS</span></span>

### <span data-ttu-id="e53dc-218">Microsoft. Azure. Commands. PolicyInsights. Models. PolicyState</span><span class="sxs-lookup"><span data-stu-id="e53dc-218">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyState</span></span>

## <span data-ttu-id="e53dc-219">Note</span><span class="sxs-lookup"><span data-stu-id="e53dc-219">NOTES</span></span>

## <span data-ttu-id="e53dc-220">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e53dc-220">RELATED LINKS</span></span>

[<span data-ttu-id="e53dc-221">Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="e53dc-221">Get-AzureRmPolicyStateSummary</span></span>](./Get-AzureRmPolicyStateSummary.md)
