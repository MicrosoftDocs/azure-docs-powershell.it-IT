---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservation.md
ms.openlocfilehash: 443f7c161cf2e3e44b2e080ef5adbc27665833bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508003"
---
# <span data-ttu-id="0d61e-101">Get-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="0d61e-101">Get-AzureRmReservation</span></span>

## <span data-ttu-id="0d61e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0d61e-102">SYNOPSIS</span></span>
<span data-ttu-id="0d61e-103">Ottenere `Reservation` s in un ordine di prenotazione specifico</span><span class="sxs-lookup"><span data-stu-id="0d61e-103">Get `Reservation`s in a given reservation Order</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d61e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0d61e-104">SYNTAX</span></span>

### <span data-ttu-id="0d61e-105">CommandLine (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0d61e-105">CommandLine (Default)</span></span>
```
Get-AzureRmReservation -ReservationOrderId <String> [-ReservationId <String>] [<CommonParameters>]
```

### <span data-ttu-id="0d61e-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="0d61e-106">PipeObject</span></span>
```
Get-AzureRmReservation [-ReservationOrder <PSReservationOrder>]
 [-ReservationOrderPage <PSReservationOrderPage>] [<CommonParameters>]
```

## <span data-ttu-id="0d61e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0d61e-107">DESCRIPTION</span></span>
<span data-ttu-id="0d61e-108">Elenco `Reservation` s all'interno di un singolo `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="0d61e-108">List `Reservation`s within a single `ReservationOrder`.</span></span>

## <span data-ttu-id="0d61e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0d61e-109">EXAMPLES</span></span>

### <span data-ttu-id="0d61e-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0d61e-110">Example 1</span></span>
```
PS C:\> Get-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="0d61e-111">Elenco `Reservation` s all'interno dell'oggetto specificato `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="0d61e-111">List `Reservation`s within the specified `ReservationOrder`.</span></span>

### <span data-ttu-id="0d61e-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="0d61e-112">Example 2</span></span>
```
PS C:\> Get-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

<span data-ttu-id="0d61e-113">Ottenere `Reservation` dettagli specifici.</span><span class="sxs-lookup"><span data-stu-id="0d61e-113">Get specific `Reservation` details.</span></span>

## <span data-ttu-id="0d61e-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0d61e-114">PARAMETERS</span></span>

### <span data-ttu-id="0d61e-115">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="0d61e-115">-ReservationId</span></span>
<span data-ttu-id="0d61e-116">ID dell'interfaccia `Reservation` da esaminare</span><span class="sxs-lookup"><span data-stu-id="0d61e-116">Id of the `Reservation` to look at</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d61e-117">-ReservationOrder</span><span class="sxs-lookup"><span data-stu-id="0d61e-117">-ReservationOrder</span></span>
<span data-ttu-id="0d61e-118">Parametro oggetto pipe per `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="0d61e-118">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: PSReservationOrder
Parameter Sets: PipeObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d61e-119">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="0d61e-119">-ReservationOrderId</span></span>
<span data-ttu-id="0d61e-120">ID dell' `ReservationOrder` che contiene `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="0d61e-120">Id of the `ReservationOrder` that contains the `Reservation`.</span></span> <span data-ttu-id="0d61e-121">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="0d61e-121">Required.</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d61e-122">-ReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="0d61e-122">-ReservationOrderPage</span></span>
<span data-ttu-id="0d61e-123">Parametro oggetto pipe per `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="0d61e-123">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: PSReservationOrderPage
Parameter Sets: PipeObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d61e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d61e-124">CommonParameters</span></span>
<span data-ttu-id="0d61e-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d61e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d61e-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d61e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d61e-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0d61e-127">INPUTS</span></span>

### <span data-ttu-id="0d61e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="0d61e-128">System.String</span></span>
<span data-ttu-id="0d61e-129">Microsoft. Azure. Commands. reservations. Models. PSReservationOrder Microsoft. Azure. Commands. reservations. Models. PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="0d61e-129">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

## <span data-ttu-id="0d61e-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0d61e-130">OUTPUTS</span></span>

### <span data-ttu-id="0d61e-131">Microsoft. Azure. Commands. reservations. Models. PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="0d61e-131">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>
<span data-ttu-id="0d61e-132">Microsoft. Azure. Commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="0d61e-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="0d61e-133">Note</span><span class="sxs-lookup"><span data-stu-id="0d61e-133">NOTES</span></span>

## <span data-ttu-id="0d61e-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0d61e-134">RELATED LINKS</span></span>

