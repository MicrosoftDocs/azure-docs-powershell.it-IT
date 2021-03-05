---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/get-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
ms.openlocfilehash: 427e715e055cd909d204f92aedd58eca9d7db0f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000317"
---
# <span data-ttu-id="5cb6e-101">Get-AzReservation</span><span class="sxs-lookup"><span data-stu-id="5cb6e-101">Get-AzReservation</span></span>

## <span data-ttu-id="5cb6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cb6e-102">SYNOPSIS</span></span>
<span data-ttu-id="5cb6e-103">Ottieni `Reservation` s in un determinato ordine di prenotazione</span><span class="sxs-lookup"><span data-stu-id="5cb6e-103">Get `Reservation`s in a given reservation Order</span></span>

## <span data-ttu-id="5cb6e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5cb6e-104">SYNTAX</span></span>

### <span data-ttu-id="5cb6e-105">CommandLine (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5cb6e-105">CommandLine (Default)</span></span>
```
Get-AzReservation -ReservationOrderId <Guid> [-ReservationId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5cb6e-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="5cb6e-106">PipeObject</span></span>
```
Get-AzReservation [-ReservationOrder <PSReservationOrder>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5cb6e-107">PagePipeObject</span><span class="sxs-lookup"><span data-stu-id="5cb6e-107">PagePipeObject</span></span>
```
Get-AzReservation [-ReservationOrderPage <PSReservationOrderPage>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5cb6e-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5cb6e-108">DESCRIPTION</span></span>
<span data-ttu-id="5cb6e-109">Elencare `Reservation` s all'interno di un unico `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="5cb6e-109">List `Reservation`s within a single `ReservationOrder`.</span></span>

## <span data-ttu-id="5cb6e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5cb6e-110">EXAMPLES</span></span>

### <span data-ttu-id="5cb6e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5cb6e-111">Example 1</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="5cb6e-112">Elenchi `Reservation` s all'interno dell'intervallo `ReservationOrder` specificato.</span><span class="sxs-lookup"><span data-stu-id="5cb6e-112">List `Reservation`s within the specified `ReservationOrder`.</span></span>

### <span data-ttu-id="5cb6e-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="5cb6e-113">Example 2</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

<span data-ttu-id="5cb6e-114">Ottenere dettagli `Reservation` specifici.</span><span class="sxs-lookup"><span data-stu-id="5cb6e-114">Get specific `Reservation` details.</span></span>

## <span data-ttu-id="5cb6e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5cb6e-115">PARAMETERS</span></span>

### <span data-ttu-id="5cb6e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cb6e-116">-DefaultProfile</span></span>
<span data-ttu-id="5cb6e-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5cb6e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cb6e-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="5cb6e-118">-ReservationId</span></span>
<span data-ttu-id="5cb6e-119">ID della `Reservation` casella da esaminare</span><span class="sxs-lookup"><span data-stu-id="5cb6e-119">Id of the `Reservation` to look at</span></span>

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

### <span data-ttu-id="5cb6e-120">-ReservationOrder</span><span class="sxs-lookup"><span data-stu-id="5cb6e-120">-ReservationOrder</span></span>
<span data-ttu-id="5cb6e-121">Parametro per l'oggetto pipe per `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="5cb6e-121">Pipe object parameter for `ReservationOrder`</span></span>

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

### <span data-ttu-id="5cb6e-122">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="5cb6e-122">-ReservationOrderId</span></span>
<span data-ttu-id="5cb6e-123">ID `ReservationOrder` dell'elemento che contiene l'elemento `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="5cb6e-123">Id of the `ReservationOrder` that contains the `Reservation`.</span></span> <span data-ttu-id="5cb6e-124">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="5cb6e-124">Required.</span></span>

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

### <span data-ttu-id="5cb6e-125">-ReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="5cb6e-125">-ReservationOrderPage</span></span>
<span data-ttu-id="5cb6e-126">Parametro per l'oggetto pipe per `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="5cb6e-126">Pipe object parameter for `ReservationOrder`</span></span>

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

### <span data-ttu-id="5cb6e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cb6e-127">CommonParameters</span></span>
<span data-ttu-id="5cb6e-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cb6e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cb6e-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5cb6e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cb6e-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="5cb6e-130">INPUTS</span></span>

### <span data-ttu-id="5cb6e-131">System.Guid</span><span class="sxs-lookup"><span data-stu-id="5cb6e-131">System.Guid</span></span>

### <span data-ttu-id="5cb6e-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="5cb6e-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

### <span data-ttu-id="5cb6e-133">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="5cb6e-133">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

## <span data-ttu-id="5cb6e-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5cb6e-134">OUTPUTS</span></span>

### <span data-ttu-id="5cb6e-135">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="5cb6e-135">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

### <span data-ttu-id="5cb6e-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="5cb6e-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="5cb6e-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="5cb6e-137">NOTES</span></span>

## <span data-ttu-id="5cb6e-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5cb6e-138">RELATED LINKS</span></span>
