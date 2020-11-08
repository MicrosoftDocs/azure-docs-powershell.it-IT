---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationquote
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationQuote.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationQuote.md
ms.openlocfilehash: 844e67f7491825fe0484a60d55cb254988cfb5c9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199825"
---
# <span data-ttu-id="4e1dd-101">Get-AzReservationQuote</span><span class="sxs-lookup"><span data-stu-id="4e1dd-101">Get-AzReservationQuote</span></span>

## <span data-ttu-id="4e1dd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4e1dd-102">SYNOPSIS</span></span>
<span data-ttu-id="4e1dd-103">{{Fill in Sinossi}}</span><span class="sxs-lookup"><span data-stu-id="4e1dd-103">{{ Fill in the Synopsis }}</span></span>

## <span data-ttu-id="4e1dd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4e1dd-104">SYNTAX</span></span>

```
Get-AzReservationQuote -ReservedResourceType <String> -Sku <String> [-Location <String>]
 -BillingScopeId <String> -Term <String> [-BillingPlan <String>] -Quantity <Int32> -DisplayName <String>
 -AppliedScopeType <String> [-AppliedScope <String>] [-Renew <Boolean>] [-InstanceFlexibility <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e1dd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4e1dd-105">DESCRIPTION</span></span>
<span data-ttu-id="4e1dd-106">Calcolare il prezzo per l'immissione di un ordine di prenotazione.</span><span class="sxs-lookup"><span data-stu-id="4e1dd-106">Calculate price for placing a reservation order.</span></span>

## <span data-ttu-id="4e1dd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4e1dd-107">EXAMPLES</span></span>

### <span data-ttu-id="4e1dd-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4e1dd-108">Example 1</span></span>
```powershell
PS C:\> Get-AzReservationQuote -ReservedResourceType "VirtualMachines" [-Sku "standard b1"] -Location "centralus"
-BillingScopeId "/subscriptions/79c182d9-9af7-4fd5-b136-b71f0a69a1d0" -Term "P1Y" [-BillingPlan "Monthly"] -Quantity 2 [-DisplayName "demo"] -AppliedScopeType "Shared" [-AppliedScopes ""]
```

<span data-ttu-id="4e1dd-109">Dopo aver ottenuto il catalogo, il cliente può ottenere il prodotto diverso in base alla posizione.</span><span class="sxs-lookup"><span data-stu-id="4e1dd-109">After get catalog, customer can get the differe product based on location.</span></span> <span data-ttu-id="4e1dd-110">Usando queste informazioni, controlla il prezzo in modo corretto</span><span class="sxs-lookup"><span data-stu-id="4e1dd-110">By using those infomation, check the price properly</span></span>

## <span data-ttu-id="4e1dd-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4e1dd-111">PARAMETERS</span></span>

### <span data-ttu-id="4e1dd-112">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="4e1dd-112">-AppliedScope</span></span>
<span data-ttu-id="4e1dd-113">Abbonamento a cui verrà applicato il vantaggio.</span><span class="sxs-lookup"><span data-stu-id="4e1dd-113">Subscription that the benefit will be applied.</span></span> <span data-ttu-id="4e1dd-114">Obbligatorio se--applicato-scope-Type è single.</span><span class="sxs-lookup"><span data-stu-id="4e1dd-114">Required if --applied-scope-type is Single.</span></span> <span data-ttu-id="4e1dd-115">Non specificare se--applicato-scope-Type è condiviso.</span><span class="sxs-lookup"><span data-stu-id="4e1dd-115">Do not specify if --applied-scope-type is Shared.</span></span>

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

### <span data-ttu-id="4e1dd-116">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="4e1dd-116">-AppliedScopeType</span></span>
<span data-ttu-id="4e1dd-117">Tipo di ambito applicato per aggiornare la prenotazione con "single" o "Shared"</span><span class="sxs-lookup"><span data-stu-id="4e1dd-117">Type of the Applied Scope to update the reservation with "Single" or "Shared"</span></span>

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

### <span data-ttu-id="4e1dd-118">-BillingPlan</span><span class="sxs-lookup"><span data-stu-id="4e1dd-118">-BillingPlan</span></span>
<span data-ttu-id="4e1dd-119">Opzioni del piano di fatturazione disponibili per l'USK.</span><span class="sxs-lookup"><span data-stu-id="4e1dd-119">The billing plan options available for this SKU.</span></span> <span data-ttu-id="4e1dd-120">"Mensile" o "upfront"</span><span class="sxs-lookup"><span data-stu-id="4e1dd-120">"Monthly" or "Upfront"</span></span>

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

### <span data-ttu-id="4e1dd-121">-BillingScopeId</span><span class="sxs-lookup"><span data-stu-id="4e1dd-121">-BillingScopeId</span></span>
<span data-ttu-id="4e1dd-122">Abbonamento che verrà addebitato per l'acquisto della prenotazione.</span><span class="sxs-lookup"><span data-stu-id="4e1dd-122">Subscription that will be charged for purchasing Reservation.</span></span>

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

### <span data-ttu-id="4e1dd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e1dd-123">-DefaultProfile</span></span>
<span data-ttu-id="4e1dd-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4e1dd-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e1dd-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4e1dd-125">-DisplayName</span></span>
<span data-ttu-id="4e1dd-126">Nome descrittivo per l'utente per identificare facilmente la prenotazione.</span><span class="sxs-lookup"><span data-stu-id="4e1dd-126">Friendly name for user to easily identified the reservation.</span></span>

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

### <span data-ttu-id="4e1dd-127">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="4e1dd-127">-InstanceFlexibility</span></span>
<span data-ttu-id="4e1dd-128">Tipo di flessibilità dell'istanza per l'aggiornamento della prenotazione.</span><span class="sxs-lookup"><span data-stu-id="4e1dd-128">Type of the Instance Flexibility to update the reservation with.</span></span>

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

### <span data-ttu-id="4e1dd-129">-Posizione</span><span class="sxs-lookup"><span data-stu-id="4e1dd-129">-Location</span></span>
<span data-ttu-id="4e1dd-130">Posizione in cui è disponibile l'USK.</span><span class="sxs-lookup"><span data-stu-id="4e1dd-130">Location that the SKU is available.</span></span>

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

### <span data-ttu-id="4e1dd-131">-Quantità</span><span class="sxs-lookup"><span data-stu-id="4e1dd-131">-Quantity</span></span>
<span data-ttu-id="4e1dd-132">Quantità di prodotto per il calcolo del prezzo o dell'acquisto.</span><span class="sxs-lookup"><span data-stu-id="4e1dd-132">Quantity of product for calculating price or purchasing.</span></span>

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

### <span data-ttu-id="4e1dd-133">-Rinnovo</span><span class="sxs-lookup"><span data-stu-id="4e1dd-133">-Renew</span></span>
<span data-ttu-id="4e1dd-134">Imposta questo valore su true per acquistare automaticamente una nuova prenotazione al momento della data di scadenza.</span><span class="sxs-lookup"><span data-stu-id="4e1dd-134">Set this to true will automatically purchase a new reservation on the expiration date time.</span></span>

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

### <span data-ttu-id="4e1dd-135">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="4e1dd-135">-ReservedResourceType</span></span>
<span data-ttu-id="4e1dd-136">Tipo della risorsa per cui devono essere forniti gli SKU.</span><span class="sxs-lookup"><span data-stu-id="4e1dd-136">Type of the resource for which the skus should be provided.</span></span>

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

### <span data-ttu-id="4e1dd-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="4e1dd-137">-Sku</span></span>
<span data-ttu-id="4e1dd-138">Nome Usk, ottenere l'elenco SKU usando il catalogo delle prenotazioni di comando AZ</span><span class="sxs-lookup"><span data-stu-id="4e1dd-138">Sku name, get the sku list by using command az reservations catalog show</span></span>

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

### <span data-ttu-id="4e1dd-139">-Termine</span><span class="sxs-lookup"><span data-stu-id="4e1dd-139">-Term</span></span>
<span data-ttu-id="4e1dd-140">Condizioni di prenotazione disponibili per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="4e1dd-140">Available reservation terms for this resource.</span></span>

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

### <span data-ttu-id="4e1dd-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e1dd-141">CommonParameters</span></span>
<span data-ttu-id="4e1dd-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e1dd-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e1dd-143">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e1dd-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e1dd-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4e1dd-144">INPUTS</span></span>

### <span data-ttu-id="4e1dd-145">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4e1dd-145">None</span></span>

## <span data-ttu-id="4e1dd-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4e1dd-146">OUTPUTS</span></span>

### <span data-ttu-id="4e1dd-147">Microsoft. Azure. Management. reservations. Models. CalculatePriceResponse</span><span class="sxs-lookup"><span data-stu-id="4e1dd-147">Microsoft.Azure.Management.Reservations.Models.CalculatePriceResponse</span></span>

## <span data-ttu-id="4e1dd-148">Note</span><span class="sxs-lookup"><span data-stu-id="4e1dd-148">NOTES</span></span>

## <span data-ttu-id="4e1dd-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4e1dd-149">RELATED LINKS</span></span>
