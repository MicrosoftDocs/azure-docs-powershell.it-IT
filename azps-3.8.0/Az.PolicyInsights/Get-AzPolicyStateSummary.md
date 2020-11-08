---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicystatesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
ms.openlocfilehash: ad622662615e74908c3d34c513e8570286b76297
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020932"
---
# <span data-ttu-id="36227-101">Get-AzPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="36227-101">Get-AzPolicyStateSummary</span></span>

## <span data-ttu-id="36227-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="36227-102">SYNOPSIS</span></span>
<span data-ttu-id="36227-103">Ottiene il riepilogo degli Stati di conformità dei criteri più recenti per le risorse.</span><span class="sxs-lookup"><span data-stu-id="36227-103">Gets latest policy compliance states summary for resources.</span></span>

## <span data-ttu-id="36227-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="36227-104">SYNTAX</span></span>

### <span data-ttu-id="36227-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="36227-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36227-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="36227-106">ManagementGroupScope</span></span>
```
Get-AzPolicyStateSummary -ManagementGroupName <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36227-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="36227-107">ResourceGroupScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="36227-108">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="36227-108">PolicySetDefinitionScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="36227-109">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="36227-109">PolicyDefinitionScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="36227-110">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="36227-110">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="36227-111">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="36227-111">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36227-112">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="36227-112">ResourceScope</span></span>
```
Get-AzPolicyStateSummary -ResourceId <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36227-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="36227-113">DESCRIPTION</span></span>
<span data-ttu-id="36227-114">Ottiene una visualizzazione di riepilogo degli ultimi numeri di stato di conformità dei criteri in diversi ambiti, suddivisi in assegnazioni di criteri e definizioni di criteri.</span><span class="sxs-lookup"><span data-stu-id="36227-114">Gets a summary view of latest policy compliance state numbers at various scopes, broken down into policy assignments and policy definitions.</span></span> <span data-ttu-id="36227-115">Include solo gli Stati dei criteri non conformi.</span><span class="sxs-lookup"><span data-stu-id="36227-115">It includes only non-compliant policy states.</span></span>

## <span data-ttu-id="36227-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="36227-116">EXAMPLES</span></span>

### <span data-ttu-id="36227-117">Esempio 1: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi nell'ambito corrente della sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="36227-117">Example 1: Get latest non-compliant policy states summary in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary
```

<span data-ttu-id="36227-118">Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="36227-118">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="36227-119">Esempio 2: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi nell'ambito di sottoscrizione specificato</span><span class="sxs-lookup"><span data-stu-id="36227-119">Example 2: Get latest non-compliant policy states summary in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="36227-120">Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione specificata.</span><span class="sxs-lookup"><span data-stu-id="36227-120">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="36227-121">Esempio 3: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi nell'ambito del gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="36227-121">Example 3: Get latest non-compliant policy states summary in management group scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="36227-122">Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'ultimo giorno per tutte le risorse all'interno del gruppo di gestione specificato.</span><span class="sxs-lookup"><span data-stu-id="36227-122">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="36227-123">Esempio 4: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi nell'ambito di un gruppo di risorse nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="36227-123">Example 4: Get latest non-compliant policy states summary in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="36227-124">Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'ultimo giorno per tutte le risorse all'interno del gruppo di risorse specificato (nell'abbonamento nel contesto della sessione corrente).</span><span class="sxs-lookup"><span data-stu-id="36227-124">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="36227-125">Esempio 5: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi nell'ambito di un gruppo di risorse nell'abbonamento specificato</span><span class="sxs-lookup"><span data-stu-id="36227-125">Example 5: Get latest non-compliant policy states summary in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="36227-126">Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'ultimo giorno per tutte le risorse all'interno del gruppo di risorse specificato (nell'abbonamento specificato).</span><span class="sxs-lookup"><span data-stu-id="36227-126">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="36227-127">Esempio 6: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi per una risorsa</span><span class="sxs-lookup"><span data-stu-id="36227-127">Example 6: Get latest non-compliant policy states summary for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="36227-128">Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'ultimo giorno per la risorsa specificata.</span><span class="sxs-lookup"><span data-stu-id="36227-128">Gets the summary view of latest policy compliance states generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="36227-129">Esempio 7: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi per una definizione di set di criteri nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="36227-129">Example 7: Get latest non-compliant policy states summary for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="36227-130">Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) effettuate dalla definizione del set di criteri specificata (presente nell'abbonamento nel contesto della sessione corrente).</span><span class="sxs-lookup"><span data-stu-id="36227-130">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="36227-131">Esempio 8: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi per una definizione di set di criteri nella sottoscrizione specificata</span><span class="sxs-lookup"><span data-stu-id="36227-131">Example 8: Get latest non-compliant policy states summary for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="36227-132">Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) effettuate dalla definizione del set di criteri specificata (presente nell'abbonamento specificato).</span><span class="sxs-lookup"><span data-stu-id="36227-132">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="36227-133">Esempio 9: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi per una definizione di criteri nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="36227-133">Example 9: Get latest non-compliant policy states summary for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="36227-134">Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) effettuate dalla definizione di criteri specificata (presente nell'abbonamento nel contesto della sessione corrente).</span><span class="sxs-lookup"><span data-stu-id="36227-134">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="36227-135">Esempio 10: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi per una definizione di criterio nella sottoscrizione specificata</span><span class="sxs-lookup"><span data-stu-id="36227-135">Example 10: Get latest non-compliant policy states summary for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="36227-136">Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) effettuate dalla definizione di criteri specificata (presente nell'abbonamento specificato).</span><span class="sxs-lookup"><span data-stu-id="36227-136">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="36227-137">Esempio 11: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi per un'assegnazione di criteri nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="36227-137">Example 11: Get latest non-compliant policy states summary for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="36227-138">Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) effettuate dall'assegnazione di criteri specificata (che esiste nell'abbonamento nel contesto della sessione corrente).</span><span class="sxs-lookup"><span data-stu-id="36227-138">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="36227-139">Esempio 12: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi per un'assegnazione di criteri nell'abbonamento specificato</span><span class="sxs-lookup"><span data-stu-id="36227-139">Example 12: Get latest non-compliant policy states summary for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="36227-140">Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) effettuate dall'assegnazione di criteri specificata (che esiste nell'abbonamento specificato).</span><span class="sxs-lookup"><span data-stu-id="36227-140">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="36227-141">Esempio 13: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi per un'assegnazione di criteri nel gruppo di risorse specificato nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="36227-141">Example 13: Get latest non-compliant policy states summary for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="36227-142">Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) effettuate dall'assegnazione di criteri specificata (esistente nel gruppo risorse della sottoscrizione nel contesto della sessione corrente).</span><span class="sxs-lookup"><span data-stu-id="36227-142">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="36227-143">Esempio 14: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi nell'ambito corrente della sottoscrizione, con l'opzione query superiore</span><span class="sxs-lookup"><span data-stu-id="36227-143">Example 14: Get latest non-compliant policy states summary in current subscription scope, with Top query option</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -Top 5
```

<span data-ttu-id="36227-144">Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="36227-144">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="36227-145">Il comando Ordina i riepiloghi delle assegnazioni dei criteri nei risultati per i conteggi delle risorse non conformi in ordine decrescente e accetta solo i primi 5 riepiloghi delle assegnazioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="36227-145">The command orders the policy assignment summaries in the results by non-compliant resource counts in descending order, and takes only top 5 of those policy assignment summaries.</span></span>

### <span data-ttu-id="36227-146">Esempio 15: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi nell'ambito corrente della sottoscrizione, con le opzioni da e a query</span><span class="sxs-lookup"><span data-stu-id="36227-146">Example 15: Get latest non-compliant policy states summary in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="36227-147">Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'intervallo di date specificato per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="36227-147">Gets the summary view of latest policy compliance states generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="36227-148">Esempio 16: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi nell'ambito corrente della sottoscrizione, con l'opzione filtro query</span><span class="sxs-lookup"><span data-stu-id="36227-148">Example 16: Get latest non-compliant policy states summary in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="36227-149">Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="36227-149">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="36227-150">Il comando limita i risultati restituiti dal filtro in base all'azione di definizione dei criteri (include le azioni Deny o audit) e la posizione delle risorse (esclude la posizione eastus).</span><span class="sxs-lookup"><span data-stu-id="36227-150">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions), and resource location (excludes eastus location).</span></span>

## <span data-ttu-id="36227-151">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="36227-151">PARAMETERS</span></span>

### <span data-ttu-id="36227-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36227-152">-DefaultProfile</span></span>
<span data-ttu-id="36227-153">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="36227-153">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36227-154">-Filtro</span><span class="sxs-lookup"><span data-stu-id="36227-154">-Filter</span></span>
<span data-ttu-id="36227-155">Filtrare l'espressione usando la notazione OData.</span><span class="sxs-lookup"><span data-stu-id="36227-155">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="36227-156">-Da</span><span class="sxs-lookup"><span data-stu-id="36227-156">-From</span></span>
<span data-ttu-id="36227-157">Timestamp formattato ISO 8601 che specifica l'ora di inizio dell'intervallo di query.</span><span class="sxs-lookup"><span data-stu-id="36227-157">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="36227-158">Se non viene specificato, il valore predefinito è "a" meno 1 giorno.</span><span class="sxs-lookup"><span data-stu-id="36227-158">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="36227-159">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="36227-159">-ManagementGroupName</span></span>
<span data-ttu-id="36227-160">Nome del gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="36227-160">Management group name.</span></span>

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

### <span data-ttu-id="36227-161">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="36227-161">-PolicyAssignmentName</span></span>
<span data-ttu-id="36227-162">Nome assegnazione criteri.</span><span class="sxs-lookup"><span data-stu-id="36227-162">Policy assignment name.</span></span>

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

### <span data-ttu-id="36227-163">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="36227-163">-PolicyDefinitionName</span></span>
<span data-ttu-id="36227-164">Nome definizione criterio.</span><span class="sxs-lookup"><span data-stu-id="36227-164">Policy definition name.</span></span>

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

### <span data-ttu-id="36227-165">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="36227-165">-PolicySetDefinitionName</span></span>
<span data-ttu-id="36227-166">Nome definizione set di criteri.</span><span class="sxs-lookup"><span data-stu-id="36227-166">Policy set definition name.</span></span>

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

### <span data-ttu-id="36227-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36227-167">-ResourceGroupName</span></span>
<span data-ttu-id="36227-168">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="36227-168">Resource group name.</span></span>

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

### <span data-ttu-id="36227-169">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36227-169">-ResourceId</span></span>
<span data-ttu-id="36227-170">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="36227-170">Resource ID.</span></span>

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

### <span data-ttu-id="36227-171">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="36227-171">-SubscriptionId</span></span>
<span data-ttu-id="36227-172">ID abbonamento.</span><span class="sxs-lookup"><span data-stu-id="36227-172">Subscription ID.</span></span>

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

### <span data-ttu-id="36227-173">-To</span><span class="sxs-lookup"><span data-stu-id="36227-173">-To</span></span>
<span data-ttu-id="36227-174">Timestamp formattato ISO 8601 che specifica l'ora di fine dell'intervallo di query.</span><span class="sxs-lookup"><span data-stu-id="36227-174">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="36227-175">Se non viene specificato, il valore predefinito è l'ora della richiesta.</span><span class="sxs-lookup"><span data-stu-id="36227-175">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="36227-176">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="36227-176">-Top</span></span>
<span data-ttu-id="36227-177">Numero massimo di record da restituire.</span><span class="sxs-lookup"><span data-stu-id="36227-177">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="36227-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36227-178">CommonParameters</span></span>
<span data-ttu-id="36227-179">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36227-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36227-180">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36227-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36227-181">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="36227-181">INPUTS</span></span>

### <span data-ttu-id="36227-182">System. String</span><span class="sxs-lookup"><span data-stu-id="36227-182">System.String</span></span>

## <span data-ttu-id="36227-183">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="36227-183">OUTPUTS</span></span>

### <span data-ttu-id="36227-184">Microsoft. Azure. Commands. PolicyInsights. Models. PolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="36227-184">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyStateSummary</span></span>

## <span data-ttu-id="36227-185">Note</span><span class="sxs-lookup"><span data-stu-id="36227-185">NOTES</span></span>

## <span data-ttu-id="36227-186">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="36227-186">RELATED LINKS</span></span>

[<span data-ttu-id="36227-187">Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="36227-187">Get-AzPolicyState</span></span>](./Get-AzPolicyState.md)
