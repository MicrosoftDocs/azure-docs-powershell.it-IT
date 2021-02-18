---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicystatesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
ms.openlocfilehash: ad622662615e74908c3d34c513e8570286b76297
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206266"
---
# <span data-ttu-id="75731-101">Get-AzPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="75731-101">Get-AzPolicyStateSummary</span></span>

## <span data-ttu-id="75731-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75731-102">SYNOPSIS</span></span>
<span data-ttu-id="75731-103">Recupera il riepilogo più recente degli stati di conformità dei criteri per le risorse.</span><span class="sxs-lookup"><span data-stu-id="75731-103">Gets latest policy compliance states summary for resources.</span></span>

## <span data-ttu-id="75731-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="75731-104">SYNTAX</span></span>

### <span data-ttu-id="75731-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="75731-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75731-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="75731-106">ManagementGroupScope</span></span>
```
Get-AzPolicyStateSummary -ManagementGroupName <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75731-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="75731-107">ResourceGroupScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="75731-108">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="75731-108">PolicySetDefinitionScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="75731-109">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="75731-109">PolicyDefinitionScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="75731-110">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="75731-110">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="75731-111">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="75731-111">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75731-112">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="75731-112">ResourceScope</span></span>
```
Get-AzPolicyStateSummary -ResourceId <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75731-113">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="75731-113">DESCRIPTION</span></span>
<span data-ttu-id="75731-114">Ottiene una visualizzazione di riepilogo dei numeri più recenti dello stato di conformità ai criteri in vari ambiti, suddivisi in assegnazioni di criteri e definizioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="75731-114">Gets a summary view of latest policy compliance state numbers at various scopes, broken down into policy assignments and policy definitions.</span></span> <span data-ttu-id="75731-115">Include solo gli stati dei criteri non conformi.</span><span class="sxs-lookup"><span data-stu-id="75731-115">It includes only non-compliant policy states.</span></span>

## <span data-ttu-id="75731-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="75731-116">EXAMPLES</span></span>

### <span data-ttu-id="75731-117">Esempio 1: Ottenere un riepilogo degli stati dei criteri non conformi più recenti nell'ambito della sottoscrizione corrente</span><span class="sxs-lookup"><span data-stu-id="75731-117">Example 1: Get latest non-compliant policy states summary in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary
```

<span data-ttu-id="75731-118">Ottiene la visualizzazione di riepilogo degli stati di conformità dei criteri più recenti generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="75731-118">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="75731-119">Esempio 2: Ottenere un riepilogo degli stati dei criteri non conformi più recenti nell'ambito di sottoscrizione specificato</span><span class="sxs-lookup"><span data-stu-id="75731-119">Example 2: Get latest non-compliant policy states summary in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="75731-120">Ottiene la visualizzazione di riepilogo degli stati di conformità dei criteri più recenti generati nell'ultimo giorno per tutte le risorse nella sottoscrizione specificata.</span><span class="sxs-lookup"><span data-stu-id="75731-120">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="75731-121">Esempio 3: Ottenere un riepilogo degli stati dei criteri non conformi più recenti nell'ambito del gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="75731-121">Example 3: Get latest non-compliant policy states summary in management group scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="75731-122">Ottiene la visualizzazione di riepilogo degli stati di conformità dei criteri più recenti generati nell'ultimo giorno per tutte le risorse all'interno del gruppo di gestione specificato.</span><span class="sxs-lookup"><span data-stu-id="75731-122">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="75731-123">Esempio 4: Ottenere un riepilogo degli stati dei criteri non conformi più recenti nell'ambito del gruppo di risorse nella sottoscrizione corrente</span><span class="sxs-lookup"><span data-stu-id="75731-123">Example 4: Get latest non-compliant policy states summary in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="75731-124">Ottiene la visualizzazione di riepilogo degli stati di conformità dei criteri più recenti generati nell'ultimo giorno per tutte le risorse all'interno del gruppo di risorse specificato (nella sottoscrizione nel contesto della sessione corrente).</span><span class="sxs-lookup"><span data-stu-id="75731-124">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="75731-125">Esempio 5: Ottenere un riepilogo degli stati dei criteri non conformi più recenti nell'ambito del gruppo di risorse nella sottoscrizione specificata</span><span class="sxs-lookup"><span data-stu-id="75731-125">Example 5: Get latest non-compliant policy states summary in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="75731-126">Ottiene la visualizzazione di riepilogo degli stati di conformità dei criteri più recenti generati nell'ultimo giorno per tutte le risorse all'interno del gruppo di risorse specificato (nella sottoscrizione specificata).</span><span class="sxs-lookup"><span data-stu-id="75731-126">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="75731-127">Esempio 6: Ottenere il riepilogo più recente degli stati dei criteri non conformi per una risorsa</span><span class="sxs-lookup"><span data-stu-id="75731-127">Example 6: Get latest non-compliant policy states summary for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="75731-128">Ottiene la visualizzazione di riepilogo degli stati di conformità dei criteri più recenti generati nell'ultimo giorno per la risorsa specificata.</span><span class="sxs-lookup"><span data-stu-id="75731-128">Gets the summary view of latest policy compliance states generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="75731-129">Esempio 7: Ottenere il riepilogo più recente degli stati dei criteri non conformi per la definizione di un set di criteri nella sottoscrizione corrente</span><span class="sxs-lookup"><span data-stu-id="75731-129">Example 7: Get latest non-compliant policy states summary for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="75731-130">Ottiene la visualizzazione di riepilogo degli stati di conformità dei criteri più recenti generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) applicate dalla definizione del set di criteri specificata (che esiste nella sottoscrizione nel contesto della sessione corrente).</span><span class="sxs-lookup"><span data-stu-id="75731-130">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="75731-131">Esempio 8: Ottenere il riepilogo più recente degli stati dei criteri non conformi per la definizione di un set di criteri nella sottoscrizione specificata</span><span class="sxs-lookup"><span data-stu-id="75731-131">Example 8: Get latest non-compliant policy states summary for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="75731-132">Ottiene la visualizzazione di riepilogo degli stati di conformità dei criteri più recenti generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) applicate dalla definizione del set di criteri specificata (esistente nella sottoscrizione specificata).</span><span class="sxs-lookup"><span data-stu-id="75731-132">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="75731-133">Esempio 9: Ottenere il riepilogo più recente degli stati dei criteri non conformi per la definizione di un criterio nella sottoscrizione corrente</span><span class="sxs-lookup"><span data-stu-id="75731-133">Example 9: Get latest non-compliant policy states summary for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="75731-134">Ottiene la visualizzazione di riepilogo degli stati di conformità dei criteri più recenti generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) applicate dalla definizione dei criteri specificata (presente nella sottoscrizione nel contesto della sessione corrente).</span><span class="sxs-lookup"><span data-stu-id="75731-134">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="75731-135">Esempio 10: Ottenere il riepilogo più recente degli stati dei criteri non conformi per la definizione di un criterio nella sottoscrizione specificata</span><span class="sxs-lookup"><span data-stu-id="75731-135">Example 10: Get latest non-compliant policy states summary for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="75731-136">Ottiene la visualizzazione di riepilogo degli stati di conformità dei criteri più recenti generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) applicate dalla definizione dei criteri specificata (esistente nella sottoscrizione specificata).</span><span class="sxs-lookup"><span data-stu-id="75731-136">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="75731-137">Esempio 11: Ottenere il riepilogo più recente degli stati dei criteri non conformi per un'assegnazione di criteri nella sottoscrizione corrente</span><span class="sxs-lookup"><span data-stu-id="75731-137">Example 11: Get latest non-compliant policy states summary for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="75731-138">Ottiene la visualizzazione di riepilogo degli stati di conformità dei criteri più recenti generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) applicate dall'assegnazione di criteri specificata (presente nella sottoscrizione nel contesto della sessione corrente).</span><span class="sxs-lookup"><span data-stu-id="75731-138">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="75731-139">Esempio 12: Ottenere il riepilogo più recente degli stati dei criteri non conformi per un'assegnazione di criteri nella sottoscrizione specificata</span><span class="sxs-lookup"><span data-stu-id="75731-139">Example 12: Get latest non-compliant policy states summary for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="75731-140">Ottiene la visualizzazione di riepilogo degli stati di conformità dei criteri più recenti generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) applicate dall'assegnazione dei criteri specificata (esistente nella sottoscrizione specificata).</span><span class="sxs-lookup"><span data-stu-id="75731-140">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="75731-141">Esempio 13: Ottenere il riepilogo più recente degli stati dei criteri non conformi per un'assegnazione di criteri nel gruppo di risorse specificato nella sottoscrizione corrente</span><span class="sxs-lookup"><span data-stu-id="75731-141">Example 13: Get latest non-compliant policy states summary for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="75731-142">Ottiene la visualizzazione di riepilogo degli stati di conformità dei criteri più recenti generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) applicate dall'assegnazione di criteri specificata (presente nel gruppo di risorse nella sottoscrizione nel contesto della sessione corrente).</span><span class="sxs-lookup"><span data-stu-id="75731-142">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="75731-143">Esempio 14: Ottenere il riepilogo più recente degli stati dei criteri non conformi nell'ambito della sottoscrizione corrente, con l'opzione di query Principale</span><span class="sxs-lookup"><span data-stu-id="75731-143">Example 14: Get latest non-compliant policy states summary in current subscription scope, with Top query option</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -Top 5
```

<span data-ttu-id="75731-144">Ottiene la visualizzazione di riepilogo degli stati di conformità dei criteri più recenti generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="75731-144">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="75731-145">Il comando ordina i riepiloghi delle assegnazioni dei criteri nei risultati in base al numero di risorse non conformi in ordine decrescente e accetta solo i primi 5 riepiloghi delle assegnazioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="75731-145">The command orders the policy assignment summaries in the results by non-compliant resource counts in descending order, and takes only top 5 of those policy assignment summaries.</span></span>

### <span data-ttu-id="75731-146">Esempio 15: Ottenere il riepilogo più recente degli stati dei criteri non conformi nell'ambito della sottoscrizione corrente, con le opzioni di query Da e A</span><span class="sxs-lookup"><span data-stu-id="75731-146">Example 15: Get latest non-compliant policy states summary in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="75731-147">Ottiene la visualizzazione di riepilogo degli stati di conformità dei criteri più recenti generati nell'intervallo di date specificato per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="75731-147">Gets the summary view of latest policy compliance states generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="75731-148">Esempio 16: Ottenere il riepilogo più recente degli stati dei criteri non conformi nell'ambito della sottoscrizione corrente, con l'opzione della query di filtro</span><span class="sxs-lookup"><span data-stu-id="75731-148">Example 16: Get latest non-compliant policy states summary in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="75731-149">Ottiene la visualizzazione di riepilogo degli stati di conformità dei criteri più recenti generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="75731-149">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="75731-150">Il comando limita i risultati restituiti filtrando in base all'azione di definizione dei criteri (incluse le azioni di negazione o controllo) e alla posizione delle risorse (esclusa la posizione est).</span><span class="sxs-lookup"><span data-stu-id="75731-150">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions), and resource location (excludes eastus location).</span></span>

## <span data-ttu-id="75731-151">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75731-151">PARAMETERS</span></span>

### <span data-ttu-id="75731-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75731-152">-DefaultProfile</span></span>
<span data-ttu-id="75731-153">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="75731-153">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75731-154">-Filter</span><span class="sxs-lookup"><span data-stu-id="75731-154">-Filter</span></span>
<span data-ttu-id="75731-155">Espressione di filtro con notazione OData.</span><span class="sxs-lookup"><span data-stu-id="75731-155">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="75731-156">-Da</span><span class="sxs-lookup"><span data-stu-id="75731-156">-From</span></span>
<span data-ttu-id="75731-157">Timestamp formattato ISO 8601 che specifica l'ora di inizio dell'intervallo in cui eseguire la query.</span><span class="sxs-lookup"><span data-stu-id="75731-157">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="75731-158">Se non è specificato, per impostazione predefinita viene utilizzato il valore del parametro "A" meno 1 giorno.</span><span class="sxs-lookup"><span data-stu-id="75731-158">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="75731-159">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="75731-159">-ManagementGroupName</span></span>
<span data-ttu-id="75731-160">Nome del gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="75731-160">Management group name.</span></span>

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

### <span data-ttu-id="75731-161">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="75731-161">-PolicyAssignmentName</span></span>
<span data-ttu-id="75731-162">Nome dell'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="75731-162">Policy assignment name.</span></span>

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

### <span data-ttu-id="75731-163">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="75731-163">-PolicyDefinitionName</span></span>
<span data-ttu-id="75731-164">Nome della definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="75731-164">Policy definition name.</span></span>

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

### <span data-ttu-id="75731-165">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="75731-165">-PolicySetDefinitionName</span></span>
<span data-ttu-id="75731-166">Nome della definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="75731-166">Policy set definition name.</span></span>

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

### <span data-ttu-id="75731-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75731-167">-ResourceGroupName</span></span>
<span data-ttu-id="75731-168">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="75731-168">Resource group name.</span></span>

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

### <span data-ttu-id="75731-169">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75731-169">-ResourceId</span></span>
<span data-ttu-id="75731-170">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="75731-170">Resource ID.</span></span>

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

### <span data-ttu-id="75731-171">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="75731-171">-SubscriptionId</span></span>
<span data-ttu-id="75731-172">ID abbonamento.</span><span class="sxs-lookup"><span data-stu-id="75731-172">Subscription ID.</span></span>

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

### <span data-ttu-id="75731-173">-A</span><span class="sxs-lookup"><span data-stu-id="75731-173">-To</span></span>
<span data-ttu-id="75731-174">Timestamp formattato ISO 8601 che specifica l'ora di fine dell'intervallo in cui eseguire la query.</span><span class="sxs-lookup"><span data-stu-id="75731-174">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="75731-175">Se non è specificato, per impostazione predefinita viene visualizzato il momento della richiesta.</span><span class="sxs-lookup"><span data-stu-id="75731-175">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="75731-176">-In alto</span><span class="sxs-lookup"><span data-stu-id="75731-176">-Top</span></span>
<span data-ttu-id="75731-177">Numero massimo di record da restituire.</span><span class="sxs-lookup"><span data-stu-id="75731-177">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="75731-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75731-178">CommonParameters</span></span>
<span data-ttu-id="75731-179">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75731-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75731-180">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="75731-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75731-181">INPUT</span><span class="sxs-lookup"><span data-stu-id="75731-181">INPUTS</span></span>

### <span data-ttu-id="75731-182">System.String</span><span class="sxs-lookup"><span data-stu-id="75731-182">System.String</span></span>

## <span data-ttu-id="75731-183">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="75731-183">OUTPUTS</span></span>

### <span data-ttu-id="75731-184">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="75731-184">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyStateSummary</span></span>

## <span data-ttu-id="75731-185">NOTE</span><span class="sxs-lookup"><span data-stu-id="75731-185">NOTES</span></span>

## <span data-ttu-id="75731-186">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="75731-186">RELATED LINKS</span></span>

[<span data-ttu-id="75731-187">Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="75731-187">Get-AzPolicyState</span></span>](./Get-AzPolicyState.md)
