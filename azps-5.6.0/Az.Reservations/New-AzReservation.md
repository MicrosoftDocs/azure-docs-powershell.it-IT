---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/new-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/New-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/New-AzReservation.md
ms.openlocfilehash: 37be462c2af2c33987e6acd0118c3169b1e062d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000205"
---
# <span data-ttu-id="1f52c-101">New-AzReservation</span><span class="sxs-lookup"><span data-stu-id="1f52c-101">New-AzReservation</span></span>

## <span data-ttu-id="1f52c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f52c-102">SYNOPSIS</span></span>
<span data-ttu-id="1f52c-103">Acquistare una prenotazione</span><span class="sxs-lookup"><span data-stu-id="1f52c-103">Purchase a reservation</span></span>

## <span data-ttu-id="1f52c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1f52c-104">SYNTAX</span></span>

```
New-AzReservation -ReservationOrderId <String> -ReservedResourceType <String> -Sku <String>
 [-Location <String>] -BillingScopeId <String> -Term <String> [-BillingPlan <String>] -Quantity <Int32>
 -DisplayName <String> -AppliedScopeType <String> [-AppliedScope <String>] [-Renew <Boolean>]
 [-InstanceFlexibility <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1f52c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1f52c-105">DESCRIPTION</span></span>
<span data-ttu-id="1f52c-106">Acquistare un'istanza di prenotazione e ottenere vantaggio</span><span class="sxs-lookup"><span data-stu-id="1f52c-106">Purchase a reservation Instance and get benefit</span></span>

## <span data-ttu-id="1f52c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1f52c-107">EXAMPLES</span></span>

### <span data-ttu-id="1f52c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1f52c-108">Example 1</span></span>
```powershell
PS C:\> New-AzReservation -ReservationOrderId "112382d9-9af7-4fd5-b136-b71f0a69a1d0" -ReservedResourceType "VirtualMachines" [-Sku "standard b1"] -Location "centralus"
-BillingScopeId "/subscriptions/79c182d9-9af7-4fd5-b136-b71f0a69a1d0" -Term "P1Y" [-BillingPlan "Monthly"] -Quantity 2 [-DisplayName "demo"] -AppliedScopeType "Shared" [-AppliedScopes ""]
```

<span data-ttu-id="1f52c-109">Dopo aver calcolato il prezzo, il cliente potrebbe ripulire quello fornito da RI con calculatePrice</span><span class="sxs-lookup"><span data-stu-id="1f52c-109">After calculate price, customer could purcahse that RI provide by calculatePrice</span></span>

## <span data-ttu-id="1f52c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f52c-110">PARAMETERS</span></span>

### <span data-ttu-id="1f52c-111">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="1f52c-111">-AppliedScope</span></span>
<span data-ttu-id="1f52c-112">Abbonamento in cui verrà applicato il vantaggio.</span><span class="sxs-lookup"><span data-stu-id="1f52c-112">Subscription that the benefit will be applied.</span></span> <span data-ttu-id="1f52c-113">Obbligatorio se --applied-scope-type è Single.</span><span class="sxs-lookup"><span data-stu-id="1f52c-113">Required if --applied-scope-type is Single.</span></span> <span data-ttu-id="1f52c-114">Non specificare se --applied-scope-type è Shared.</span><span class="sxs-lookup"><span data-stu-id="1f52c-114">Do not specify if --applied-scope-type is Shared.</span></span>

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

### <span data-ttu-id="1f52c-115">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="1f52c-115">-AppliedScopeType</span></span>
<span data-ttu-id="1f52c-116">Tipo di ambito applicato per aggiornare la prenotazione con "Singola" o "Condivisa"</span><span class="sxs-lookup"><span data-stu-id="1f52c-116">Type of the Applied Scope to update the reservation with "Single" or "Shared"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f52c-117">-BillingPlan</span><span class="sxs-lookup"><span data-stu-id="1f52c-117">-BillingPlan</span></span>
<span data-ttu-id="1f52c-118">Opzioni del piano di fatturazione disponibili per questo SKU.</span><span class="sxs-lookup"><span data-stu-id="1f52c-118">The billing plan options available for this SKU.</span></span> <span data-ttu-id="1f52c-119">"Mensile" o "Anticipato"</span><span class="sxs-lookup"><span data-stu-id="1f52c-119">"Monthly" or "Upfront"</span></span>

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

### <span data-ttu-id="1f52c-120">-BillingScopeId</span><span class="sxs-lookup"><span data-stu-id="1f52c-120">-BillingScopeId</span></span>
<span data-ttu-id="1f52c-121">Abbonamento che verrà addebitato per la prenotazione degli acquisti.</span><span class="sxs-lookup"><span data-stu-id="1f52c-121">Subscription that will be charged for purchasing Reservation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f52c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f52c-122">-DefaultProfile</span></span>
<span data-ttu-id="1f52c-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1f52c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f52c-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1f52c-124">-DisplayName</span></span>
<span data-ttu-id="1f52c-125">Nome descrittivo dell'utente per identificare facilmente la prenotazione.</span><span class="sxs-lookup"><span data-stu-id="1f52c-125">Friendly name for user to easily identified the reservation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f52c-126">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="1f52c-126">-InstanceFlexibility</span></span>
<span data-ttu-id="1f52c-127">{{ Fill InstanceFlexibility Description }}</span><span class="sxs-lookup"><span data-stu-id="1f52c-127">{{ Fill InstanceFlexibility Description }}</span></span>

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

### <span data-ttu-id="1f52c-128">-Location</span><span class="sxs-lookup"><span data-stu-id="1f52c-128">-Location</span></span>
<span data-ttu-id="1f52c-129">Posizione in cui è disponibile lo SKU.</span><span class="sxs-lookup"><span data-stu-id="1f52c-129">Location that the SKU is available.</span></span>

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

### <span data-ttu-id="1f52c-130">-Quantity</span><span class="sxs-lookup"><span data-stu-id="1f52c-130">-Quantity</span></span>
<span data-ttu-id="1f52c-131">Quantità di prodotto per il calcolo del prezzo o dell'acquisto.</span><span class="sxs-lookup"><span data-stu-id="1f52c-131">Quantity of product for calculating price or purchasing.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f52c-132">-Rinnova</span><span class="sxs-lookup"><span data-stu-id="1f52c-132">-Renew</span></span>
<span data-ttu-id="1f52c-133">Imposta questa opzione su True per acquistare automaticamente una nuova prenotazione alla data di scadenza.</span><span class="sxs-lookup"><span data-stu-id="1f52c-133">Set this to true will automatically purchase a new reservation on the expiration date time.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f52c-134">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="1f52c-134">-ReservationOrderId</span></span>
<span data-ttu-id="1f52c-135">ID dell'ordine di prenotazione da acquistare, generato dal calcolo dell'ordine di prenotazione delle prenotazioni.</span><span class="sxs-lookup"><span data-stu-id="1f52c-135">Id of reservation order to purchase, generate by az reservations reservation-order calculate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f52c-136">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="1f52c-136">-ReservedResourceType</span></span>
<span data-ttu-id="1f52c-137">Tipo della risorsa per cui devono essere fornite le SKU.</span><span class="sxs-lookup"><span data-stu-id="1f52c-137">Type of the resource for which the skus should be provided.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f52c-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="1f52c-138">-Sku</span></span>
<span data-ttu-id="1f52c-139">Nome SKU</span><span class="sxs-lookup"><span data-stu-id="1f52c-139">Sku name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f52c-140">-Term</span><span class="sxs-lookup"><span data-stu-id="1f52c-140">-Term</span></span>
<span data-ttu-id="1f52c-141">Termini di prenotazione disponibili per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="1f52c-141">Available reservation terms for this resource.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f52c-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f52c-142">-Confirm</span></span>
<span data-ttu-id="1f52c-143">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f52c-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f52c-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f52c-144">-WhatIf</span></span>
<span data-ttu-id="1f52c-145">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f52c-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f52c-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f52c-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f52c-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f52c-147">CommonParameters</span></span>
<span data-ttu-id="1f52c-148">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f52c-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f52c-149">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1f52c-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f52c-150">INPUT</span><span class="sxs-lookup"><span data-stu-id="1f52c-150">INPUTS</span></span>

### <span data-ttu-id="1f52c-151">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1f52c-151">None</span></span>

## <span data-ttu-id="1f52c-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1f52c-152">OUTPUTS</span></span>

### <span data-ttu-id="1f52c-153">Microsoft.Azure.Management.Reservations.Models.ReservationOrderResponse</span><span class="sxs-lookup"><span data-stu-id="1f52c-153">Microsoft.Azure.Management.Reservations.Models.ReservationOrderResponse</span></span>

## <span data-ttu-id="1f52c-154">NOTE</span><span class="sxs-lookup"><span data-stu-id="1f52c-154">NOTES</span></span>

## <span data-ttu-id="1f52c-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1f52c-155">RELATED LINKS</span></span>
