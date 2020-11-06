---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservation.md
ms.openlocfilehash: 1003dcf38815be8daba8b0e218dbca430a89f9e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509115"
---
# <span data-ttu-id="7b9a6-101">Get-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="7b9a6-101">Get-AzureRmReservation</span></span>

## <span data-ttu-id="7b9a6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7b9a6-102">SYNOPSIS</span></span>
<span data-ttu-id="7b9a6-103">Ottenere `Reservation` s in un ordine di prenotazione specifico</span><span class="sxs-lookup"><span data-stu-id="7b9a6-103">Get `Reservation`s in a given reservation Order</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b9a6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7b9a6-104">SYNTAX</span></span>

### <span data-ttu-id="7b9a6-105">CommandLine (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7b9a6-105">CommandLine (Default)</span></span>
```
Get-AzureRmReservation -ReservationOrderId <Guid> [-ReservationId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b9a6-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="7b9a6-106">PipeObject</span></span>
```
Get-AzureRmReservation [-ReservationOrder <PSReservationOrder>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7b9a6-107">PagePipeObject</span><span class="sxs-lookup"><span data-stu-id="7b9a6-107">PagePipeObject</span></span>
```
Get-AzureRmReservation [-ReservationOrderPage <PSReservationOrderPage>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b9a6-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7b9a6-108">DESCRIPTION</span></span>
<span data-ttu-id="7b9a6-109">Elenco `Reservation` s all'interno di un singolo `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="7b9a6-109">List `Reservation`s within a single `ReservationOrder`.</span></span>

## <span data-ttu-id="7b9a6-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7b9a6-110">EXAMPLES</span></span>

### <span data-ttu-id="7b9a6-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7b9a6-111">Example 1</span></span>
```
PS C:\> Get-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="7b9a6-112">Elenco `Reservation` s all'interno dell'oggetto specificato `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="7b9a6-112">List `Reservation`s within the specified `ReservationOrder`.</span></span>

### <span data-ttu-id="7b9a6-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7b9a6-113">Example 2</span></span>
```
PS C:\> Get-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

<span data-ttu-id="7b9a6-114">Ottenere `Reservation` dettagli specifici.</span><span class="sxs-lookup"><span data-stu-id="7b9a6-114">Get specific `Reservation` details.</span></span>

## <span data-ttu-id="7b9a6-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7b9a6-115">PARAMETERS</span></span>

### <span data-ttu-id="7b9a6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b9a6-116">-DefaultProfile</span></span>
<span data-ttu-id="7b9a6-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7b9a6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b9a6-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="7b9a6-118">-ReservationId</span></span>
<span data-ttu-id="7b9a6-119">ID dell'interfaccia `Reservation` da esaminare</span><span class="sxs-lookup"><span data-stu-id="7b9a6-119">Id of the `Reservation` to look at</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b9a6-120">-ReservationOrder</span><span class="sxs-lookup"><span data-stu-id="7b9a6-120">-ReservationOrder</span></span>
<span data-ttu-id="7b9a6-121">Parametro oggetto pipe per `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="7b9a6-121">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder
Parameter Sets: PipeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b9a6-122">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="7b9a6-122">-ReservationOrderId</span></span>
<span data-ttu-id="7b9a6-123">ID dell' `ReservationOrder` che contiene `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="7b9a6-123">Id of the `ReservationOrder` that contains the `Reservation`.</span></span> <span data-ttu-id="7b9a6-124">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="7b9a6-124">Required.</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b9a6-125">-ReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="7b9a6-125">-ReservationOrderPage</span></span>
<span data-ttu-id="7b9a6-126">Parametro oggetto pipe per `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="7b9a6-126">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage
Parameter Sets: PagePipeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b9a6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b9a6-127">CommonParameters</span></span>
<span data-ttu-id="7b9a6-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b9a6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b9a6-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b9a6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b9a6-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7b9a6-130">INPUTS</span></span>

### <span data-ttu-id="7b9a6-131">System. Guid</span><span class="sxs-lookup"><span data-stu-id="7b9a6-131">System.Guid</span></span>

### <span data-ttu-id="7b9a6-132">Microsoft. Azure. Commands. reservations. Models. PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="7b9a6-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>
<span data-ttu-id="7b9a6-133">Parametri: ReservationOrder (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7b9a6-133">Parameters: ReservationOrder (ByValue)</span></span>

### <span data-ttu-id="7b9a6-134">Microsoft. Azure. Commands. reservations. Models. PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="7b9a6-134">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>
<span data-ttu-id="7b9a6-135">Parametri: ReservationOrderPage (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7b9a6-135">Parameters: ReservationOrderPage (ByValue)</span></span>

## <span data-ttu-id="7b9a6-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7b9a6-136">OUTPUTS</span></span>

### <span data-ttu-id="7b9a6-137">Microsoft. Azure. Commands. reservations. Models. PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="7b9a6-137">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

### <span data-ttu-id="7b9a6-138">Microsoft. Azure. Commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="7b9a6-138">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="7b9a6-139">Note</span><span class="sxs-lookup"><span data-stu-id="7b9a6-139">NOTES</span></span>

## <span data-ttu-id="7b9a6-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7b9a6-140">RELATED LINKS</span></span>
