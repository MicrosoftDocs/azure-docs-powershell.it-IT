---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/get-azurermpolicystatesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyStateSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyStateSummary.md
ms.openlocfilehash: 4b4d45414a9a27561c3be4be195a1e5f77076e6b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511599"
---
# <span data-ttu-id="29774-101">Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="29774-101">Get-AzureRmPolicyStateSummary</span></span>

## <span data-ttu-id="29774-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="29774-102">SYNOPSIS</span></span>
<span data-ttu-id="29774-103">Ottiene il riepilogo degli Stati di conformità dei criteri più recenti per le risorse.</span><span class="sxs-lookup"><span data-stu-id="29774-103">Gets latest policy compliance states summary for resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29774-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="29774-104">SYNTAX</span></span>

### <span data-ttu-id="29774-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="29774-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29774-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="29774-106">ManagementGroupScope</span></span>
```
Get-AzureRmPolicyStateSummary -ManagementGroupName <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29774-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="29774-107">ResourceGroupScope</span></span>
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="29774-108">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="29774-108">PolicySetDefinitionScope</span></span>
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="29774-109">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="29774-109">PolicyDefinitionScope</span></span>
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="29774-110">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="29774-110">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="29774-111">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="29774-111">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String>
 -PolicyAssignmentName <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29774-112">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="29774-112">ResourceScope</span></span>
```
Get-AzureRmPolicyStateSummary -ResourceId <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29774-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="29774-113">DESCRIPTION</span></span>
<span data-ttu-id="29774-114">Ottiene una visualizzazione di riepilogo degli ultimi numeri di stato di conformità dei criteri in diversi ambiti, suddivisi in assegnazioni di criteri e definizioni di criteri.</span><span class="sxs-lookup"><span data-stu-id="29774-114">Gets a summary view of latest policy compliance state numbers at various scopes, broken down into policy assignments and policy definitions.</span></span> <span data-ttu-id="29774-115">Include solo gli Stati dei criteri non conformi.</span><span class="sxs-lookup"><span data-stu-id="29774-115">It includes only non-compliant policy states.</span></span>

## <span data-ttu-id="29774-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="29774-116">EXAMPLES</span></span>

### <span data-ttu-id="29774-117">Esempio 1: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi nell'ambito corrente della sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="29774-117">Example 1: Get latest non-compliant policy states summary in current subscription scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary
```

<span data-ttu-id="29774-118">Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="29774-118">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="29774-119">Esempio 2: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi nell'ambito di sottoscrizione specificato</span><span class="sxs-lookup"><span data-stu-id="29774-119">Example 2: Get latest non-compliant policy states summary in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="29774-120">Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione specificata.</span><span class="sxs-lookup"><span data-stu-id="29774-120">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="29774-121">Esempio 3: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi nell'ambito del gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="29774-121">Example 3: Get latest non-compliant policy states summary in management group scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="29774-122">Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'ultimo giorno per tutte le risorse all'interno del gruppo di gestione specificato.</span><span class="sxs-lookup"><span data-stu-id="29774-122">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="29774-123">Esempio 4: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi nell'ambito di un gruppo di risorse nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="29774-123">Example 4: Get latest non-compliant policy states summary in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="29774-124">Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'ultimo giorno per tutte le risorse all'interno del gruppo di risorse specificato (nell'abbonamento nel contesto della sessione corrente).</span><span class="sxs-lookup"><span data-stu-id="29774-124">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="29774-125">Esempio 5: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi nell'ambito di un gruppo di risorse nell'abbonamento specificato</span><span class="sxs-lookup"><span data-stu-id="29774-125">Example 5: Get latest non-compliant policy states summary in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="29774-126">Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'ultimo giorno per tutte le risorse all'interno del gruppo di risorse specificato (nell'abbonamento specificato).</span><span class="sxs-lookup"><span data-stu-id="29774-126">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="29774-127">Esempio 6: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi per una risorsa</span><span class="sxs-lookup"><span data-stu-id="29774-127">Example 6: Get latest non-compliant policy states summary for a resource</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="29774-128">Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'ultimo giorno per la risorsa specificata.</span><span class="sxs-lookup"><span data-stu-id="29774-128">Gets the summary view of latest policy compliance states generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="29774-129">Esempio 7: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi per una definizione di set di criteri nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="29774-129">Example 7: Get latest non-compliant policy states summary for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="29774-130">Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) effettuate dalla definizione del set di criteri specificata (presente nell'abbonamento nel contesto della sessione corrente).</span><span class="sxs-lookup"><span data-stu-id="29774-130">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="29774-131">Esempio 8: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi per una definizione di set di criteri nella sottoscrizione specificata</span><span class="sxs-lookup"><span data-stu-id="29774-131">Example 8: Get latest non-compliant policy states summary for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="29774-132">Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) effettuate dalla definizione del set di criteri specificata (presente nell'abbonamento specificato).</span><span class="sxs-lookup"><span data-stu-id="29774-132">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="29774-133">Esempio 9: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi per una definizione di criteri nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="29774-133">Example 9: Get latest non-compliant policy states summary for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="29774-134">Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) effettuate dalla definizione di criteri specificata (presente nell'abbonamento nel contesto della sessione corrente).</span><span class="sxs-lookup"><span data-stu-id="29774-134">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="29774-135">Esempio 10: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi per una definizione di criterio nella sottoscrizione specificata</span><span class="sxs-lookup"><span data-stu-id="29774-135">Example 10: Get latest non-compliant policy states summary for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="29774-136">Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) effettuate dalla definizione di criteri specificata (presente nell'abbonamento specificato).</span><span class="sxs-lookup"><span data-stu-id="29774-136">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="29774-137">Esempio 11: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi per un'assegnazione di criteri nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="29774-137">Example 11: Get latest non-compliant policy states summary for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="29774-138">Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) effettuate dall'assegnazione di criteri specificata (che esiste nell'abbonamento nel contesto della sessione corrente).</span><span class="sxs-lookup"><span data-stu-id="29774-138">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="29774-139">Esempio 12: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi per un'assegnazione di criteri nell'abbonamento specificato</span><span class="sxs-lookup"><span data-stu-id="29774-139">Example 12: Get latest non-compliant policy states summary for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="29774-140">Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) effettuate dall'assegnazione di criteri specificata (che esiste nell'abbonamento specificato).</span><span class="sxs-lookup"><span data-stu-id="29774-140">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="29774-141">Esempio 13: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi per un'assegnazione di criteri nel gruppo di risorse specificato nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="29774-141">Example 13: Get latest non-compliant policy states summary for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="29774-142">Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) effettuate dall'assegnazione di criteri specificata (esistente nel gruppo risorse della sottoscrizione nel contesto della sessione corrente).</span><span class="sxs-lookup"><span data-stu-id="29774-142">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="29774-143">Esempio 14: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi nell'ambito corrente della sottoscrizione, con l'opzione query superiore</span><span class="sxs-lookup"><span data-stu-id="29774-143">Example 14: Get latest non-compliant policy states summary in current subscription scope, with Top query option</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -Top 5
```

<span data-ttu-id="29774-144">Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="29774-144">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="29774-145">Il comando Ordina i riepiloghi delle assegnazioni dei criteri nei risultati per i conteggi delle risorse non conformi in ordine decrescente e accetta solo i primi 5 riepiloghi delle assegnazioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="29774-145">The command orders the policy assignment summaries in the results by non-compliant resource counts in descending order, and takes only top 5 of those policy assignment summaries.</span></span>

### <span data-ttu-id="29774-146">Esempio 15: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi nell'ambito corrente della sottoscrizione, con le opzioni da e a query</span><span class="sxs-lookup"><span data-stu-id="29774-146">Example 15: Get latest non-compliant policy states summary in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="29774-147">Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'intervallo di date specificato per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="29774-147">Gets the summary view of latest policy compliance states generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="29774-148">Esempio 16: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi nell'ambito corrente della sottoscrizione, con l'opzione filtro query</span><span class="sxs-lookup"><span data-stu-id="29774-148">Example 16: Get latest non-compliant policy states summary in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="29774-149">Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="29774-149">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="29774-150">Il comando limita i risultati restituiti dal filtro in base all'azione di definizione dei criteri (include le azioni Deny o audit) e la posizione delle risorse (esclude la posizione eastus).</span><span class="sxs-lookup"><span data-stu-id="29774-150">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions), and resource location (excludes eastus location).</span></span>

## <span data-ttu-id="29774-151">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="29774-151">PARAMETERS</span></span>

### <span data-ttu-id="29774-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29774-152">-DefaultProfile</span></span>
<span data-ttu-id="29774-153">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="29774-153">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29774-154">-Filtro</span><span class="sxs-lookup"><span data-stu-id="29774-154">-Filter</span></span>
<span data-ttu-id="29774-155">Filtrare l'espressione usando la notazione OData.</span><span class="sxs-lookup"><span data-stu-id="29774-155">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="29774-156">-Da</span><span class="sxs-lookup"><span data-stu-id="29774-156">-From</span></span>
<span data-ttu-id="29774-157">Timestamp formattato ISO 8601 che specifica l'ora di inizio dell'intervallo di query.</span><span class="sxs-lookup"><span data-stu-id="29774-157">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="29774-158">Se non viene specificato, il valore predefinito è "a" meno 1 giorno.</span><span class="sxs-lookup"><span data-stu-id="29774-158">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="29774-159">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="29774-159">-ManagementGroupName</span></span>
<span data-ttu-id="29774-160">Nome del gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="29774-160">Management group name.</span></span>

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

### <span data-ttu-id="29774-161">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="29774-161">-PolicyAssignmentName</span></span>
<span data-ttu-id="29774-162">Nome assegnazione criteri.</span><span class="sxs-lookup"><span data-stu-id="29774-162">Policy assignment name.</span></span>

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

### <span data-ttu-id="29774-163">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="29774-163">-PolicyDefinitionName</span></span>
<span data-ttu-id="29774-164">Nome definizione criterio.</span><span class="sxs-lookup"><span data-stu-id="29774-164">Policy definition name.</span></span>

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

### <span data-ttu-id="29774-165">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="29774-165">-PolicySetDefinitionName</span></span>
<span data-ttu-id="29774-166">Nome definizione set di criteri.</span><span class="sxs-lookup"><span data-stu-id="29774-166">Policy set definition name.</span></span>

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

### <span data-ttu-id="29774-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29774-167">-ResourceGroupName</span></span>
<span data-ttu-id="29774-168">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="29774-168">Resource group name.</span></span>

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

### <span data-ttu-id="29774-169">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29774-169">-ResourceId</span></span>
<span data-ttu-id="29774-170">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="29774-170">Resource ID.</span></span>

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

### <span data-ttu-id="29774-171">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="29774-171">-SubscriptionId</span></span>
<span data-ttu-id="29774-172">ID abbonamento.</span><span class="sxs-lookup"><span data-stu-id="29774-172">Subscription ID.</span></span>

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

### <span data-ttu-id="29774-173">-To</span><span class="sxs-lookup"><span data-stu-id="29774-173">-To</span></span>
<span data-ttu-id="29774-174">Timestamp formattato ISO 8601 che specifica l'ora di fine dell'intervallo di query.</span><span class="sxs-lookup"><span data-stu-id="29774-174">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="29774-175">Se non viene specificato, il valore predefinito è l'ora della richiesta.</span><span class="sxs-lookup"><span data-stu-id="29774-175">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="29774-176">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="29774-176">-Top</span></span>
<span data-ttu-id="29774-177">Numero massimo di record da restituire.</span><span class="sxs-lookup"><span data-stu-id="29774-177">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="29774-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29774-178">CommonParameters</span></span>
<span data-ttu-id="29774-179">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29774-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29774-180">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29774-180">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29774-181">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="29774-181">INPUTS</span></span>

### <span data-ttu-id="29774-182">System. String</span><span class="sxs-lookup"><span data-stu-id="29774-182">System.String</span></span>

## <span data-ttu-id="29774-183">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="29774-183">OUTPUTS</span></span>

### <span data-ttu-id="29774-184">Microsoft. Azure. Commands. PolicyInsights. Models. PolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="29774-184">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyStateSummary</span></span>

## <span data-ttu-id="29774-185">Note</span><span class="sxs-lookup"><span data-stu-id="29774-185">NOTES</span></span>

## <span data-ttu-id="29774-186">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="29774-186">RELATED LINKS</span></span>

[<span data-ttu-id="29774-187">Get-AzureRmPolicyState</span><span class="sxs-lookup"><span data-stu-id="29774-187">Get-AzureRmPolicyState</span></span>](./Get-AzureRmPolicyState.md)