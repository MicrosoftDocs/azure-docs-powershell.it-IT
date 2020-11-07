---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscription/set-azssubscription
schema: 2.0.0
ms.openlocfilehash: d4636bb8f6e3fdbe9fc1911c173680f966e0f9e4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860125"
---
# <span data-ttu-id="a27b3-101">Set-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="a27b3-101">Set-AzsSubscription</span></span>

## <span data-ttu-id="a27b3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a27b3-102">SYNOPSIS</span></span>
<span data-ttu-id="a27b3-103">Creare o aggiornare un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a27b3-103">Create or updates a subscription.</span></span>

## <span data-ttu-id="a27b3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a27b3-104">SYNTAX</span></span>

### <span data-ttu-id="a27b3-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a27b3-105">UpdateExpanded (Default)</span></span>
```
Set-AzsSubscription -SubscriptionId <String> [-DisplayName <String>] [-Id <String>] [-OfferId <String>]
 [-State <SubscriptionState>] [-TenantId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="a27b3-106">Aggiornamento</span><span class="sxs-lookup"><span data-stu-id="a27b3-106">Update</span></span>
```
Set-AzsSubscription -SubscriptionDefinition <ISubscription> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="a27b3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a27b3-107">DESCRIPTION</span></span>
<span data-ttu-id="a27b3-108">Creare o aggiornare un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a27b3-108">Create or updates a subscription.</span></span>

## <span data-ttu-id="a27b3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a27b3-109">EXAMPLES</span></span>

### <span data-ttu-id="a27b3-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a27b3-110">Example 1</span></span>
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

<span data-ttu-id="a27b3-111">Aggiorna un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a27b3-111">Updates a subscription.</span></span>

## <span data-ttu-id="a27b3-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a27b3-112">PARAMETERS</span></span>

### <span data-ttu-id="a27b3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a27b3-113">-DefaultProfile</span></span>
<span data-ttu-id="a27b3-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a27b3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a27b3-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a27b3-115">-DisplayName</span></span>
<span data-ttu-id="a27b3-116">Nome dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a27b3-116">Subscription name.</span></span>

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

### <span data-ttu-id="a27b3-117">-ID</span><span class="sxs-lookup"><span data-stu-id="a27b3-117">-Id</span></span>
<span data-ttu-id="a27b3-118">Identificatore completo.</span><span class="sxs-lookup"><span data-stu-id="a27b3-118">Fully qualified identifier.</span></span>

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

### <span data-ttu-id="a27b3-119">-Idofferta</span><span class="sxs-lookup"><span data-stu-id="a27b3-119">-OfferId</span></span>
<span data-ttu-id="a27b3-120">Identificatore dell'offerta sotto l'ambito di un provider delegato.</span><span class="sxs-lookup"><span data-stu-id="a27b3-120">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="a27b3-121">-Stato</span><span class="sxs-lookup"><span data-stu-id="a27b3-121">-State</span></span>
<span data-ttu-id="a27b3-122">Stato sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="a27b3-122">Subscription state.</span></span>

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

### <span data-ttu-id="a27b3-123">-SubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="a27b3-123">-SubscriptionDefinition</span></span>
<span data-ttu-id="a27b3-124">Elenco delle operazioni supportate.</span><span class="sxs-lookup"><span data-stu-id="a27b3-124">List of supported operations.</span></span>
<span data-ttu-id="a27b3-125">Per costruire, vedere la sezione Note per le proprietà di SUBSCRIPTIONDEFINITION e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="a27b3-125">To construct, see NOTES section for SUBSCRIPTIONDEFINITION properties and create a hash table.</span></span>

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

### <span data-ttu-id="a27b3-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a27b3-126">-SubscriptionId</span></span>
<span data-ttu-id="a27b3-127">ID dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a27b3-127">Id of the subscription.</span></span>

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

### <span data-ttu-id="a27b3-128">-ID tenant</span><span class="sxs-lookup"><span data-stu-id="a27b3-128">-TenantId</span></span>
<span data-ttu-id="a27b3-129">Identificatore del tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="a27b3-129">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="a27b3-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a27b3-130">-Confirm</span></span>
<span data-ttu-id="a27b3-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a27b3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a27b3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a27b3-132">-WhatIf</span></span>
<span data-ttu-id="a27b3-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a27b3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a27b3-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a27b3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a27b3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a27b3-135">CommonParameters</span></span>
<span data-ttu-id="a27b3-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a27b3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a27b3-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a27b3-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a27b3-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a27b3-138">INPUTS</span></span>

### <span data-ttu-id="a27b3-139">Microsoft. Azure. PowerShell. Cmdlets. Subscription. Models. Api20151101. ISubscription</span><span class="sxs-lookup"><span data-stu-id="a27b3-139">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription</span></span>

## <span data-ttu-id="a27b3-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a27b3-140">OUTPUTS</span></span>

### <span data-ttu-id="a27b3-141">Microsoft. Azure. PowerShell. Cmdlets. Subscription. Models. Api20151101. ISubscription</span><span class="sxs-lookup"><span data-stu-id="a27b3-141">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription</span></span>



## <span data-ttu-id="a27b3-142">Note</span><span class="sxs-lookup"><span data-stu-id="a27b3-142">NOTES</span></span>

<span data-ttu-id="a27b3-143">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="a27b3-143">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a27b3-144">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a27b3-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="a27b3-145">SUBSCRIPTIONDEFINITION <ISubscription> : elenco delle operazioni supportate.</span><span class="sxs-lookup"><span data-stu-id="a27b3-145">SUBSCRIPTIONDEFINITION <ISubscription>: List of supported operations.</span></span>
  - <span data-ttu-id="a27b3-146">`[DisplayName <String>]`: Nome sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="a27b3-146">`[DisplayName <String>]`: Subscription name.</span></span>
  - <span data-ttu-id="a27b3-147">`[Id <String>]`: Identificatore completo.</span><span class="sxs-lookup"><span data-stu-id="a27b3-147">`[Id <String>]`: Fully qualified identifier.</span></span>
  - <span data-ttu-id="a27b3-148">`[OfferId <String>]`: Identificatore dell'offerta sotto l'ambito di un provider delegato.</span><span class="sxs-lookup"><span data-stu-id="a27b3-148">`[OfferId <String>]`: Identifier of the offer under the scope of a delegated provider.</span></span>
  - <span data-ttu-id="a27b3-149">`[State <SubscriptionState?>]`: Stato sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="a27b3-149">`[State <SubscriptionState?>]`: Subscription state.</span></span>
  - <span data-ttu-id="a27b3-150">`[SubscriptionId <String>]`: Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a27b3-150">`[SubscriptionId <String>]`: Subscription identifier.</span></span>
  - <span data-ttu-id="a27b3-151">`[TenantId <String>]`: Identificatore tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="a27b3-151">`[TenantId <String>]`: Directory tenant identifier.</span></span>

## <span data-ttu-id="a27b3-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a27b3-152">RELATED LINKS</span></span>

