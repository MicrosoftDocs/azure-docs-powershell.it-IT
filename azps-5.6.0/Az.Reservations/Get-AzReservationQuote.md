---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/get-azreservationquote
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationQuote.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationQuote.md
ms.openlocfilehash: 3a06de95cedd0ea38fa38b2fb8784e553ae6f4d7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000254"
---
# <span data-ttu-id="ad704-101">Get-AzReservationQuote</span><span class="sxs-lookup"><span data-stu-id="ad704-101">Get-AzReservationQuote</span></span>

## <span data-ttu-id="ad704-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad704-102">SYNOPSIS</span></span>
<span data-ttu-id="ad704-103">Ottieni un preventivo per la prenotazione.</span><span class="sxs-lookup"><span data-stu-id="ad704-103">Get a quote for the reservation.</span></span> <span data-ttu-id="ad704-104">Questo valore viene passato `New-AzReservation` all'acquisto.</span><span class="sxs-lookup"><span data-stu-id="ad704-104">This is passed to `New-AzReservation` to purchase.</span></span>

## <span data-ttu-id="ad704-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ad704-105">SYNTAX</span></span>

```
Get-AzReservationQuote -ReservedResourceType <String> -Sku <String> [-Location <String>]
 -BillingScopeId <String> -Term <String> [-BillingPlan <String>] -Quantity <Int32> -DisplayName <String>
 -AppliedScopeType <String> [-AppliedScope <String>] [-Renew <Boolean>] [-InstanceFlexibility <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad704-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ad704-106">DESCRIPTION</span></span>
<span data-ttu-id="ad704-107">Calcolare il prezzo per l'esecuzione di un ordine di prenotazione.</span><span class="sxs-lookup"><span data-stu-id="ad704-107">Calculate price for placing a reservation order.</span></span>

## <span data-ttu-id="ad704-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ad704-108">EXAMPLES</span></span>

### <span data-ttu-id="ad704-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ad704-109">Example 1</span></span>
```powershell
PS C:\> Get-AzReservationQuote -ReservedResourceType "VirtualMachines" [-Sku "standard b1"] -Location "centralus"
-BillingScopeId "/subscriptions/79c182d9-9af7-4fd5-b136-b71f0a69a1d0" -Term "P1Y" [-BillingPlan "Monthly"] -Quantity 2 [-DisplayName "demo"] -AppliedScopeType "Shared" [-AppliedScopes ""]
```

<span data-ttu-id="ad704-110">Dopo aver ottenere il catalogo, il cliente può ottenere il prodotto diverso in base alla posizione.</span><span class="sxs-lookup"><span data-stu-id="ad704-110">After get catalog, customer can get the differe product based on location.</span></span> <span data-ttu-id="ad704-111">Usando queste informazioni, controlla il prezzo correttamente</span><span class="sxs-lookup"><span data-stu-id="ad704-111">By using those infomation, check the price properly</span></span>

## <span data-ttu-id="ad704-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad704-112">PARAMETERS</span></span>

### <span data-ttu-id="ad704-113">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="ad704-113">-AppliedScope</span></span>
<span data-ttu-id="ad704-114">Abbonamento in cui verrà applicato il vantaggio.</span><span class="sxs-lookup"><span data-stu-id="ad704-114">Subscription that the benefit will be applied.</span></span> <span data-ttu-id="ad704-115">Obbligatorio se --applied-scope-type è Single.</span><span class="sxs-lookup"><span data-stu-id="ad704-115">Required if --applied-scope-type is Single.</span></span> <span data-ttu-id="ad704-116">Non specificare se --applied-scope-type è Shared.</span><span class="sxs-lookup"><span data-stu-id="ad704-116">Do not specify if --applied-scope-type is Shared.</span></span>

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

### <span data-ttu-id="ad704-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="ad704-117">-AppliedScopeType</span></span>
<span data-ttu-id="ad704-118">Tipo di ambito applicato per aggiornare la prenotazione con "Singola" o "Condivisa"</span><span class="sxs-lookup"><span data-stu-id="ad704-118">Type of the Applied Scope to update the reservation with "Single" or "Shared"</span></span>

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

### <span data-ttu-id="ad704-119">-BillingPlan</span><span class="sxs-lookup"><span data-stu-id="ad704-119">-BillingPlan</span></span>
<span data-ttu-id="ad704-120">Opzioni del piano di fatturazione disponibili per questo SKU.</span><span class="sxs-lookup"><span data-stu-id="ad704-120">The billing plan options available for this SKU.</span></span> <span data-ttu-id="ad704-121">"Mensile" o "Anticipato"</span><span class="sxs-lookup"><span data-stu-id="ad704-121">"Monthly" or "Upfront"</span></span>

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

### <span data-ttu-id="ad704-122">-BillingScopeId</span><span class="sxs-lookup"><span data-stu-id="ad704-122">-BillingScopeId</span></span>
<span data-ttu-id="ad704-123">Abbonamento che verrà addebitato per la prenotazione degli acquisti.</span><span class="sxs-lookup"><span data-stu-id="ad704-123">Subscription that will be charged for purchasing Reservation.</span></span>

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

### <span data-ttu-id="ad704-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad704-124">-DefaultProfile</span></span>
<span data-ttu-id="ad704-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ad704-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad704-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ad704-126">-DisplayName</span></span>
<span data-ttu-id="ad704-127">Nome descrittivo dell'utente per identificare facilmente la prenotazione.</span><span class="sxs-lookup"><span data-stu-id="ad704-127">Friendly name for user to easily identified the reservation.</span></span>

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

### <span data-ttu-id="ad704-128">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="ad704-128">-InstanceFlexibility</span></span>
<span data-ttu-id="ad704-129">Tipo di flessibilità delle istanze con cui aggiornare la prenotazione.</span><span class="sxs-lookup"><span data-stu-id="ad704-129">Type of the Instance Flexibility to update the reservation with.</span></span>

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

### <span data-ttu-id="ad704-130">-Location</span><span class="sxs-lookup"><span data-stu-id="ad704-130">-Location</span></span>
<span data-ttu-id="ad704-131">Posizione in cui è disponibile lo SKU.</span><span class="sxs-lookup"><span data-stu-id="ad704-131">Location that the SKU is available.</span></span>

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

### <span data-ttu-id="ad704-132">-Quantity</span><span class="sxs-lookup"><span data-stu-id="ad704-132">-Quantity</span></span>
<span data-ttu-id="ad704-133">Quantità di prodotto per il calcolo del prezzo o dell'acquisto.</span><span class="sxs-lookup"><span data-stu-id="ad704-133">Quantity of product for calculating price or purchasing.</span></span>

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

### <span data-ttu-id="ad704-134">-Rinnova</span><span class="sxs-lookup"><span data-stu-id="ad704-134">-Renew</span></span>
<span data-ttu-id="ad704-135">Imposta questa opzione su True per acquistare automaticamente una nuova prenotazione alla data di scadenza.</span><span class="sxs-lookup"><span data-stu-id="ad704-135">Set this to true will automatically purchase a new reservation on the expiration date time.</span></span>

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

### <span data-ttu-id="ad704-136">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="ad704-136">-ReservedResourceType</span></span>
<span data-ttu-id="ad704-137">Tipo della risorsa per cui devono essere fornite le SKU.</span><span class="sxs-lookup"><span data-stu-id="ad704-137">Type of the resource for which the skus should be provided.</span></span>

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

### <span data-ttu-id="ad704-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="ad704-138">-Sku</span></span>
<span data-ttu-id="ad704-139">Nome SKU, ottenere l'elenco di SKU usando il comando az reservations catalog show</span><span class="sxs-lookup"><span data-stu-id="ad704-139">Sku name, get the sku list by using command az reservations catalog show</span></span>

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

### <span data-ttu-id="ad704-140">-Term</span><span class="sxs-lookup"><span data-stu-id="ad704-140">-Term</span></span>
<span data-ttu-id="ad704-141">Termini di prenotazione disponibili per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="ad704-141">Available reservation terms for this resource.</span></span>

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

### <span data-ttu-id="ad704-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad704-142">CommonParameters</span></span>
<span data-ttu-id="ad704-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad704-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad704-144">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ad704-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad704-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="ad704-145">INPUTS</span></span>

### <span data-ttu-id="ad704-146">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ad704-146">None</span></span>

## <span data-ttu-id="ad704-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ad704-147">OUTPUTS</span></span>

### <span data-ttu-id="ad704-148">Microsoft.Azure.Management.Reservations.Models.CalculatePriceResponse</span><span class="sxs-lookup"><span data-stu-id="ad704-148">Microsoft.Azure.Management.Reservations.Models.CalculatePriceResponse</span></span>

## <span data-ttu-id="ad704-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="ad704-149">NOTES</span></span>

## <span data-ttu-id="ad704-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ad704-150">RELATED LINKS</span></span>
