---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscription/set-azssubscription
schema: 2.0.0
ms.openlocfilehash: d4636bb8f6e3fdbe9fc1911c173680f966e0f9e4
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030482"
---
# <span data-ttu-id="dcf69-101">Set-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="dcf69-101">Set-AzsSubscription</span></span>

## <span data-ttu-id="dcf69-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dcf69-102">SYNOPSIS</span></span>
<span data-ttu-id="dcf69-103">Creare o aggiornare un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="dcf69-103">Create or updates a subscription.</span></span>

## <span data-ttu-id="dcf69-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dcf69-104">SYNTAX</span></span>

### <span data-ttu-id="dcf69-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dcf69-105">UpdateExpanded (Default)</span></span>
```
Set-AzsSubscription -SubscriptionId <String> [-DisplayName <String>] [-Id <String>] [-OfferId <String>]
 [-State <SubscriptionState>] [-TenantId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="dcf69-106">Aggiornamento</span><span class="sxs-lookup"><span data-stu-id="dcf69-106">Update</span></span>
```
Set-AzsSubscription -SubscriptionDefinition <ISubscription> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="dcf69-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dcf69-107">DESCRIPTION</span></span>
<span data-ttu-id="dcf69-108">Creare o aggiornare un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="dcf69-108">Create or updates a subscription.</span></span>

## <span data-ttu-id="dcf69-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dcf69-109">EXAMPLES</span></span>

### <span data-ttu-id="dcf69-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="dcf69-110">Example 1</span></span>
```powershell
PS C:\> $subscription = Get-AzsSubscription | where DisplayName -eq 'testsubscription'
$subscription.DisplayName = 'update subscription'
$subscription | Set-AzsSubscription | fl *

DisplayName    : update subscription
Id             : /subscriptions/f6f9665e-9831-4ac6-a2c3-26a591b9e6e8
OfferId        : /delegatedProviders/default/offers/TestOffer-fef68214-ba47-469c-89a7-07faf7947ad6
State          : Enabled
SubscriptionId : f6f9665e-9831-4ac6-a2c3-26a591b9e6e8
TenantId       : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="dcf69-111">Aggiorna un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="dcf69-111">Updates a subscription.</span></span>

## <span data-ttu-id="dcf69-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dcf69-112">PARAMETERS</span></span>

### <span data-ttu-id="dcf69-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcf69-113">-DefaultProfile</span></span>
<span data-ttu-id="dcf69-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dcf69-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dcf69-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="dcf69-115">-DisplayName</span></span>
<span data-ttu-id="dcf69-116">Nome dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="dcf69-116">Subscription name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dcf69-117">-ID</span><span class="sxs-lookup"><span data-stu-id="dcf69-117">-Id</span></span>
<span data-ttu-id="dcf69-118">Identificatore completo.</span><span class="sxs-lookup"><span data-stu-id="dcf69-118">Fully qualified identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dcf69-119">-Idofferta</span><span class="sxs-lookup"><span data-stu-id="dcf69-119">-OfferId</span></span>
<span data-ttu-id="dcf69-120">Identificatore dell'offerta sotto l'ambito di un provider delegato.</span><span class="sxs-lookup"><span data-stu-id="dcf69-120">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dcf69-121">-Stato</span><span class="sxs-lookup"><span data-stu-id="dcf69-121">-State</span></span>
<span data-ttu-id="dcf69-122">Stato sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="dcf69-122">Subscription state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Support.SubscriptionState
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dcf69-123">-SubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="dcf69-123">-SubscriptionDefinition</span></span>
<span data-ttu-id="dcf69-124">Elenco delle operazioni supportate.</span><span class="sxs-lookup"><span data-stu-id="dcf69-124">List of supported operations.</span></span>
<span data-ttu-id="dcf69-125">Per costruire, vedere la sezione Note per le proprietà di SUBSCRIPTIONDEFINITION e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="dcf69-125">To construct, see NOTES section for SUBSCRIPTIONDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="dcf69-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dcf69-126">-SubscriptionId</span></span>
<span data-ttu-id="dcf69-127">ID dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="dcf69-127">Id of the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dcf69-128">-ID tenant</span><span class="sxs-lookup"><span data-stu-id="dcf69-128">-TenantId</span></span>
<span data-ttu-id="dcf69-129">Identificatore del tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="dcf69-129">Directory tenant identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dcf69-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dcf69-130">-Confirm</span></span>
<span data-ttu-id="dcf69-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dcf69-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcf69-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcf69-132">-WhatIf</span></span>
<span data-ttu-id="dcf69-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dcf69-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcf69-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dcf69-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcf69-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcf69-135">CommonParameters</span></span>
<span data-ttu-id="dcf69-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcf69-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcf69-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dcf69-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcf69-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dcf69-138">INPUTS</span></span>

### <span data-ttu-id="dcf69-139">Microsoft. Azure. PowerShell. Cmdlets. Subscription. Models. Api20151101. ISubscription</span><span class="sxs-lookup"><span data-stu-id="dcf69-139">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription</span></span>

## <span data-ttu-id="dcf69-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dcf69-140">OUTPUTS</span></span>

### <span data-ttu-id="dcf69-141">Microsoft. Azure. PowerShell. Cmdlets. Subscription. Models. Api20151101. ISubscription</span><span class="sxs-lookup"><span data-stu-id="dcf69-141">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription</span></span>



## <span data-ttu-id="dcf69-142">Note</span><span class="sxs-lookup"><span data-stu-id="dcf69-142">NOTES</span></span>

<span data-ttu-id="dcf69-143">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="dcf69-143">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dcf69-144">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dcf69-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="dcf69-145">SUBSCRIPTIONDEFINITION <ISubscription> : elenco delle operazioni supportate.</span><span class="sxs-lookup"><span data-stu-id="dcf69-145">SUBSCRIPTIONDEFINITION <ISubscription>: List of supported operations.</span></span>
  - <span data-ttu-id="dcf69-146">`[DisplayName <String>]`: Nome sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="dcf69-146">`[DisplayName <String>]`: Subscription name.</span></span>
  - <span data-ttu-id="dcf69-147">`[Id <String>]`: Identificatore completo.</span><span class="sxs-lookup"><span data-stu-id="dcf69-147">`[Id <String>]`: Fully qualified identifier.</span></span>
  - <span data-ttu-id="dcf69-148">`[OfferId <String>]`: Identificatore dell'offerta sotto l'ambito di un provider delegato.</span><span class="sxs-lookup"><span data-stu-id="dcf69-148">`[OfferId <String>]`: Identifier of the offer under the scope of a delegated provider.</span></span>
  - <span data-ttu-id="dcf69-149">`[State <SubscriptionState?>]`: Stato sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="dcf69-149">`[State <SubscriptionState?>]`: Subscription state.</span></span>
  - <span data-ttu-id="dcf69-150">`[SubscriptionId <String>]`: Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="dcf69-150">`[SubscriptionId <String>]`: Subscription identifier.</span></span>
  - <span data-ttu-id="dcf69-151">`[TenantId <String>]`: Identificatore tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="dcf69-151">`[TenantId <String>]`: Directory tenant identifier.</span></span>

## <span data-ttu-id="dcf69-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dcf69-152">RELATED LINKS</span></span>

