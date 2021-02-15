---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/split-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
ms.openlocfilehash: b879b5b47c752a331f0c2d70a6d37e57b113d816
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176438"
---
# <span data-ttu-id="f86ff-101">Split-AzReservation</span><span class="sxs-lookup"><span data-stu-id="f86ff-101">Split-AzReservation</span></span>

## <span data-ttu-id="f86ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f86ff-102">SYNOPSIS</span></span>
<span data-ttu-id="f86ff-103">Dividere un `Reservation` elemento .</span><span class="sxs-lookup"><span data-stu-id="f86ff-103">Split a `Reservation`.</span></span>

## <span data-ttu-id="f86ff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f86ff-104">SYNTAX</span></span>

### <span data-ttu-id="f86ff-105">CommandLine (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f86ff-105">CommandLine (Default)</span></span>
```
Split-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -Quantity <Int32[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f86ff-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="f86ff-106">PipeObject</span></span>
```
Split-AzReservation -Quantity <Int32[]> -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f86ff-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f86ff-107">DESCRIPTION</span></span>
<span data-ttu-id="f86ff-108">Dividere una in `Reservation` due con la distribuzione di quantità `Reservation` specificata.</span><span class="sxs-lookup"><span data-stu-id="f86ff-108">Split a `Reservation` into two `Reservation`s with specified quantity distribution.</span></span>

## <span data-ttu-id="f86ff-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f86ff-109">EXAMPLES</span></span>

### <span data-ttu-id="f86ff-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f86ff-110">Example 1</span></span>
```
PS C:\> Split-AzReservation -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111" -Quantities 2,3
```

<span data-ttu-id="f86ff-111">Dividere le specificate `Reservation` in due s con le quantità `Reservation` corrispondenti</span><span class="sxs-lookup"><span data-stu-id="f86ff-111">Split the specified `Reservation` into two `Reservation`s with the corresponding quantities</span></span>

## <span data-ttu-id="f86ff-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f86ff-112">PARAMETERS</span></span>

### <span data-ttu-id="f86ff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f86ff-113">-DefaultProfile</span></span>
<span data-ttu-id="f86ff-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f86ff-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f86ff-115">-Quantity</span><span class="sxs-lookup"><span data-stu-id="f86ff-115">-Quantity</span></span>
<span data-ttu-id="f86ff-116">Numeri interi separati da virgola per il campo della quantità delle due `Reservation` unità</span><span class="sxs-lookup"><span data-stu-id="f86ff-116">Comma-separated integers for quantity field of the two `Reservation`s</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f86ff-117">-Prenotazione</span><span class="sxs-lookup"><span data-stu-id="f86ff-117">-Reservation</span></span>
<span data-ttu-id="f86ff-118">Parametro per l'oggetto pipe per `Reservation`</span><span class="sxs-lookup"><span data-stu-id="f86ff-118">Pipe object parameter for `Reservation`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservation
Parameter Sets: PipeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f86ff-119">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="f86ff-119">-ReservationId</span></span>
<span data-ttu-id="f86ff-120">ID `Reservation` dell'elemento da dividere</span><span class="sxs-lookup"><span data-stu-id="f86ff-120">Id of the `Reservation` to split</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f86ff-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="f86ff-121">-ReservationOrderId</span></span>
<span data-ttu-id="f86ff-122">ID `ReservationOrder` dell'elemento che contiene `Reservation` l'utente da dividere</span><span class="sxs-lookup"><span data-stu-id="f86ff-122">Id of the `ReservationOrder` that contains the `Reservation` that user wants to split</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f86ff-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f86ff-123">-Confirm</span></span>
<span data-ttu-id="f86ff-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f86ff-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f86ff-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f86ff-125">-WhatIf</span></span>
<span data-ttu-id="f86ff-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f86ff-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f86ff-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f86ff-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f86ff-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f86ff-128">CommonParameters</span></span>
<span data-ttu-id="f86ff-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f86ff-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f86ff-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f86ff-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f86ff-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="f86ff-131">INPUTS</span></span>

### <span data-ttu-id="f86ff-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="f86ff-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="f86ff-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f86ff-133">OUTPUTS</span></span>

### <span data-ttu-id="f86ff-134">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="f86ff-134">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="f86ff-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="f86ff-135">NOTES</span></span>

## <span data-ttu-id="f86ff-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f86ff-136">RELATED LINKS</span></span>
