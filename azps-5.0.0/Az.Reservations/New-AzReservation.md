---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/new-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/New-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/New-AzReservation.md
ms.openlocfilehash: 60de1572afda000c8c1a99f53df1344b9b0fbfda
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193872"
---
# <span data-ttu-id="62a9a-101">New-AzReservation</span><span class="sxs-lookup"><span data-stu-id="62a9a-101">New-AzReservation</span></span>

## <span data-ttu-id="62a9a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="62a9a-102">SYNOPSIS</span></span>
<span data-ttu-id="62a9a-103">Acquistare una prenotazione</span><span class="sxs-lookup"><span data-stu-id="62a9a-103">Purchase a reservation</span></span>

## <span data-ttu-id="62a9a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="62a9a-104">SYNTAX</span></span>

```
New-AzReservation -ReservationOrderId <String> -ReservedResourceType <String> -Sku <String>
 [-Location <String>] -BillingScopeId <String> -Term <String> [-BillingPlan <String>] -Quantity <Int32>
 -DisplayName <String> -AppliedScopeType <String> [-AppliedScope <String>] [-Renew <Boolean>]
 [-InstanceFlexibility <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="62a9a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="62a9a-105">DESCRIPTION</span></span>
<span data-ttu-id="62a9a-106">Acquistare un'istanza di prenotazione e ottenere vantaggi</span><span class="sxs-lookup"><span data-stu-id="62a9a-106">Purchase a reservation Instance and get benefit</span></span>

## <span data-ttu-id="62a9a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="62a9a-107">EXAMPLES</span></span>

### <span data-ttu-id="62a9a-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="62a9a-108">Example 1</span></span>
```powershell
PS C:\> New-AzReservation -ReservationOrderId "112382d9-9af7-4fd5-b136-b71f0a69a1d0" -ReservedResourceType "VirtualMachines" [-Sku "standard b1"] -Location "centralus"
-BillingScopeId "/subscriptions/79c182d9-9af7-4fd5-b136-b71f0a69a1d0" -Term "P1Y" [-BillingPlan "Monthly"] -Quantity 2 [-DisplayName "demo"] -AppliedScopeType "Shared" [-AppliedScopes ""]
```

<span data-ttu-id="62a9a-109">Dopo il calcolo del prezzo, il cliente può Purcahse che RI offre calculatePrice</span><span class="sxs-lookup"><span data-stu-id="62a9a-109">After calculate price, customer could purcahse that RI provide by calculatePrice</span></span>

## <span data-ttu-id="62a9a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="62a9a-110">PARAMETERS</span></span>

### <span data-ttu-id="62a9a-111">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="62a9a-111">-AppliedScope</span></span>
<span data-ttu-id="62a9a-112">Abbonamento a cui verrà applicato il vantaggio.</span><span class="sxs-lookup"><span data-stu-id="62a9a-112">Subscription that the benefit will be applied.</span></span> <span data-ttu-id="62a9a-113">Obbligatorio se--applicato-scope-Type è single.</span><span class="sxs-lookup"><span data-stu-id="62a9a-113">Required if --applied-scope-type is Single.</span></span> <span data-ttu-id="62a9a-114">Non specificare se--applicato-scope-Type è condiviso.</span><span class="sxs-lookup"><span data-stu-id="62a9a-114">Do not specify if --applied-scope-type is Shared.</span></span>

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

### <span data-ttu-id="62a9a-115">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="62a9a-115">-AppliedScopeType</span></span>
<span data-ttu-id="62a9a-116">Tipo di ambito applicato per aggiornare la prenotazione con "single" o "Shared"</span><span class="sxs-lookup"><span data-stu-id="62a9a-116">Type of the Applied Scope to update the reservation with "Single" or "Shared"</span></span>

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

### <span data-ttu-id="62a9a-117">-BillingPlan</span><span class="sxs-lookup"><span data-stu-id="62a9a-117">-BillingPlan</span></span>
<span data-ttu-id="62a9a-118">Opzioni del piano di fatturazione disponibili per l'USK.</span><span class="sxs-lookup"><span data-stu-id="62a9a-118">The billing plan options available for this SKU.</span></span> <span data-ttu-id="62a9a-119">"Mensile" o "upfront"</span><span class="sxs-lookup"><span data-stu-id="62a9a-119">"Monthly" or "Upfront"</span></span>

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

### <span data-ttu-id="62a9a-120">-BillingScopeId</span><span class="sxs-lookup"><span data-stu-id="62a9a-120">-BillingScopeId</span></span>
<span data-ttu-id="62a9a-121">Abbonamento che verrà addebitato per l'acquisto della prenotazione.</span><span class="sxs-lookup"><span data-stu-id="62a9a-121">Subscription that will be charged for purchasing Reservation.</span></span>

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

### <span data-ttu-id="62a9a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62a9a-122">-DefaultProfile</span></span>
<span data-ttu-id="62a9a-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="62a9a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62a9a-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="62a9a-124">-DisplayName</span></span>
<span data-ttu-id="62a9a-125">Nome descrittivo per l'utente per identificare facilmente la prenotazione.</span><span class="sxs-lookup"><span data-stu-id="62a9a-125">Friendly name for user to easily identified the reservation.</span></span>

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

### <span data-ttu-id="62a9a-126">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="62a9a-126">-InstanceFlexibility</span></span>
<span data-ttu-id="62a9a-127">{{Fill InstanceFlexibility Description}}</span><span class="sxs-lookup"><span data-stu-id="62a9a-127">{{ Fill InstanceFlexibility Description }}</span></span>

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

### <span data-ttu-id="62a9a-128">-Posizione</span><span class="sxs-lookup"><span data-stu-id="62a9a-128">-Location</span></span>
<span data-ttu-id="62a9a-129">Posizione in cui è disponibile l'USK.</span><span class="sxs-lookup"><span data-stu-id="62a9a-129">Location that the SKU is available.</span></span>

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

### <span data-ttu-id="62a9a-130">-Quantità</span><span class="sxs-lookup"><span data-stu-id="62a9a-130">-Quantity</span></span>
<span data-ttu-id="62a9a-131">Quantità di prodotto per il calcolo del prezzo o dell'acquisto.</span><span class="sxs-lookup"><span data-stu-id="62a9a-131">Quantity of product for calculating price or purchasing.</span></span>

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

### <span data-ttu-id="62a9a-132">-Rinnovo</span><span class="sxs-lookup"><span data-stu-id="62a9a-132">-Renew</span></span>
<span data-ttu-id="62a9a-133">Imposta questo valore su true per acquistare automaticamente una nuova prenotazione al momento della data di scadenza.</span><span class="sxs-lookup"><span data-stu-id="62a9a-133">Set this to true will automatically purchase a new reservation on the expiration date time.</span></span>

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

### <span data-ttu-id="62a9a-134">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="62a9a-134">-ReservationOrderId</span></span>
<span data-ttu-id="62a9a-135">ID dell'ordine di prenotazione per l'acquisto, genera da AZ prenotazione prenotazioni-calcola ordine.</span><span class="sxs-lookup"><span data-stu-id="62a9a-135">Id of reservation order to purchase, generate by az reservations reservation-order calculate.</span></span>

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

### <span data-ttu-id="62a9a-136">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="62a9a-136">-ReservedResourceType</span></span>
<span data-ttu-id="62a9a-137">Tipo della risorsa per cui devono essere forniti gli SKU.</span><span class="sxs-lookup"><span data-stu-id="62a9a-137">Type of the resource for which the skus should be provided.</span></span>

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

### <span data-ttu-id="62a9a-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="62a9a-138">-Sku</span></span>
<span data-ttu-id="62a9a-139">Nome SKU</span><span class="sxs-lookup"><span data-stu-id="62a9a-139">Sku name</span></span>

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

### <span data-ttu-id="62a9a-140">-Termine</span><span class="sxs-lookup"><span data-stu-id="62a9a-140">-Term</span></span>
<span data-ttu-id="62a9a-141">Condizioni di prenotazione disponibili per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="62a9a-141">Available reservation terms for this resource.</span></span>


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

### <span data-ttu-id="62a9a-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="62a9a-142">-Confirm</span></span>
<span data-ttu-id="62a9a-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62a9a-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62a9a-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62a9a-144">-WhatIf</span></span>
<span data-ttu-id="62a9a-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="62a9a-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="62a9a-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="62a9a-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62a9a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62a9a-147">CommonParameters</span></span>
<span data-ttu-id="62a9a-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62a9a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62a9a-149">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="62a9a-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62a9a-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="62a9a-150">INPUTS</span></span>

### <span data-ttu-id="62a9a-151">Nessuno</span><span class="sxs-lookup"><span data-stu-id="62a9a-151">None</span></span>

## <span data-ttu-id="62a9a-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="62a9a-152">OUTPUTS</span></span>

### <span data-ttu-id="62a9a-153">Microsoft. Azure. Management. reservations. Models. ReservationOrderResponse</span><span class="sxs-lookup"><span data-stu-id="62a9a-153">Microsoft.Azure.Management.Reservations.Models.ReservationOrderResponse</span></span>

## <span data-ttu-id="62a9a-154">Note</span><span class="sxs-lookup"><span data-stu-id="62a9a-154">NOTES</span></span>

## <span data-ttu-id="62a9a-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="62a9a-155">RELATED LINKS</span></span>