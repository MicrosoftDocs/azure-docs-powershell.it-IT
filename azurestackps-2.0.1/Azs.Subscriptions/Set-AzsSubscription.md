---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscription/set-azssubscription
schema: 2.0.0
ms.openlocfilehash: d4636bb8f6e3fdbe9fc1911c173680f966e0f9e4
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2020
ms.locfileid: "94023208"
---
# <span data-ttu-id="67eef-101">Set-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="67eef-101">Set-AzsSubscription</span></span>

## <span data-ttu-id="67eef-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="67eef-102">SYNOPSIS</span></span>
<span data-ttu-id="67eef-103">Creare o aggiornare un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="67eef-103">Create or updates a subscription.</span></span>

## <span data-ttu-id="67eef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="67eef-104">SYNTAX</span></span>

### <span data-ttu-id="67eef-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="67eef-105">UpdateExpanded (Default)</span></span>
```
Set-AzsSubscription -SubscriptionId <String> [-DisplayName <String>] [-Id <String>] [-OfferId <String>]
 [-State <SubscriptionState>] [-TenantId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="67eef-106">Aggiornamento</span><span class="sxs-lookup"><span data-stu-id="67eef-106">Update</span></span>
```
Set-AzsSubscription -SubscriptionDefinition <ISubscription> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="67eef-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="67eef-107">DESCRIPTION</span></span>
<span data-ttu-id="67eef-108">Creare o aggiornare un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="67eef-108">Create or updates a subscription.</span></span>

## <span data-ttu-id="67eef-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="67eef-109">EXAMPLES</span></span>

### <span data-ttu-id="67eef-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="67eef-110">Example 1</span></span>
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

<span data-ttu-id="67eef-111">Aggiorna un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="67eef-111">Updates a subscription.</span></span>

## <span data-ttu-id="67eef-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="67eef-112">PARAMETERS</span></span>

### <span data-ttu-id="67eef-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67eef-113">-DefaultProfile</span></span>
<span data-ttu-id="67eef-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="67eef-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67eef-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="67eef-115">-DisplayName</span></span>
<span data-ttu-id="67eef-116">Nome dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="67eef-116">Subscription name.</span></span>

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

### <span data-ttu-id="67eef-117">-ID</span><span class="sxs-lookup"><span data-stu-id="67eef-117">-Id</span></span>
<span data-ttu-id="67eef-118">Identificatore completo.</span><span class="sxs-lookup"><span data-stu-id="67eef-118">Fully qualified identifier.</span></span>

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

### <span data-ttu-id="67eef-119">-Idofferta</span><span class="sxs-lookup"><span data-stu-id="67eef-119">-OfferId</span></span>
<span data-ttu-id="67eef-120">Identificatore dell'offerta sotto l'ambito di un provider delegato.</span><span class="sxs-lookup"><span data-stu-id="67eef-120">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="67eef-121">-Stato</span><span class="sxs-lookup"><span data-stu-id="67eef-121">-State</span></span>
<span data-ttu-id="67eef-122">Stato sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="67eef-122">Subscription state.</span></span>

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

### <span data-ttu-id="67eef-123">-SubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="67eef-123">-SubscriptionDefinition</span></span>
<span data-ttu-id="67eef-124">Elenco delle operazioni supportate.</span><span class="sxs-lookup"><span data-stu-id="67eef-124">List of supported operations.</span></span>
<span data-ttu-id="67eef-125">Per costruire, vedere la sezione Note per le proprietà di SUBSCRIPTIONDEFINITION e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="67eef-125">To construct, see NOTES section for SUBSCRIPTIONDEFINITION properties and create a hash table.</span></span>

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

### <span data-ttu-id="67eef-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="67eef-126">-SubscriptionId</span></span>
<span data-ttu-id="67eef-127">ID dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="67eef-127">Id of the subscription.</span></span>

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

### <span data-ttu-id="67eef-128">-ID tenant</span><span class="sxs-lookup"><span data-stu-id="67eef-128">-TenantId</span></span>
<span data-ttu-id="67eef-129">Identificatore del tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="67eef-129">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="67eef-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="67eef-130">-Confirm</span></span>
<span data-ttu-id="67eef-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67eef-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67eef-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67eef-132">-WhatIf</span></span>
<span data-ttu-id="67eef-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="67eef-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67eef-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="67eef-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67eef-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67eef-135">CommonParameters</span></span>
<span data-ttu-id="67eef-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67eef-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67eef-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="67eef-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67eef-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="67eef-138">INPUTS</span></span>

### <span data-ttu-id="67eef-139">Microsoft. Azure. PowerShell. Cmdlets. Subscription. Models. Api20151101. ISubscription</span><span class="sxs-lookup"><span data-stu-id="67eef-139">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription</span></span>

## <span data-ttu-id="67eef-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="67eef-140">OUTPUTS</span></span>

### <span data-ttu-id="67eef-141">Microsoft. Azure. PowerShell. Cmdlets. Subscription. Models. Api20151101. ISubscription</span><span class="sxs-lookup"><span data-stu-id="67eef-141">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription</span></span>



## <span data-ttu-id="67eef-142">Note</span><span class="sxs-lookup"><span data-stu-id="67eef-142">NOTES</span></span>

<span data-ttu-id="67eef-143">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="67eef-143">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="67eef-144">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="67eef-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="67eef-145">SUBSCRIPTIONDEFINITION <ISubscription> : elenco delle operazioni supportate.</span><span class="sxs-lookup"><span data-stu-id="67eef-145">SUBSCRIPTIONDEFINITION <ISubscription>: List of supported operations.</span></span>
  - <span data-ttu-id="67eef-146">`[DisplayName <String>]`: Nome sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="67eef-146">`[DisplayName <String>]`: Subscription name.</span></span>
  - <span data-ttu-id="67eef-147">`[Id <String>]`: Identificatore completo.</span><span class="sxs-lookup"><span data-stu-id="67eef-147">`[Id <String>]`: Fully qualified identifier.</span></span>
  - <span data-ttu-id="67eef-148">`[OfferId <String>]`: Identificatore dell'offerta sotto l'ambito di un provider delegato.</span><span class="sxs-lookup"><span data-stu-id="67eef-148">`[OfferId <String>]`: Identifier of the offer under the scope of a delegated provider.</span></span>
  - <span data-ttu-id="67eef-149">`[State <SubscriptionState?>]`: Stato sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="67eef-149">`[State <SubscriptionState?>]`: Subscription state.</span></span>
  - <span data-ttu-id="67eef-150">`[SubscriptionId <String>]`: Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="67eef-150">`[SubscriptionId <String>]`: Subscription identifier.</span></span>
  - <span data-ttu-id="67eef-151">`[TenantId <String>]`: Identificatore tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="67eef-151">`[TenantId <String>]`: Directory tenant identifier.</span></span>

## <span data-ttu-id="67eef-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="67eef-152">RELATED LINKS</span></span>

