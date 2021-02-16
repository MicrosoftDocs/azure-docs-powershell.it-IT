---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/merge-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Merge-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Merge-AzReservation.md
ms.openlocfilehash: fc0b04049184334c59a38226e031342fc29207b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176446"
---
# <span data-ttu-id="a5ed2-101">Merge-AzReservation</span><span class="sxs-lookup"><span data-stu-id="a5ed2-101">Merge-AzReservation</span></span>

## <span data-ttu-id="a5ed2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5ed2-102">SYNOPSIS</span></span>
<span data-ttu-id="a5ed2-103">Unisce due `Reservation` s.</span><span class="sxs-lookup"><span data-stu-id="a5ed2-103">Merges two `Reservation`s.</span></span>

## <span data-ttu-id="a5ed2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a5ed2-104">SYNTAX</span></span>

### <span data-ttu-id="a5ed2-105">CommandLine (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a5ed2-105">CommandLine (Default)</span></span>
```
Merge-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5ed2-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="a5ed2-106">PipeObject</span></span>
```
Merge-AzReservation -Reservation <PSReservation[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5ed2-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a5ed2-107">DESCRIPTION</span></span>
<span data-ttu-id="a5ed2-108">Unire le s `Reservation` specificate in una `Reservation` nuova.</span><span class="sxs-lookup"><span data-stu-id="a5ed2-108">Merge the specified `Reservation`s into a new `Reservation`.</span></span> <span data-ttu-id="a5ed2-109">Le due `Reservation` unione devono avere le stesse proprietà.</span><span class="sxs-lookup"><span data-stu-id="a5ed2-109">The two `Reservation`s being merged must have same properties.</span></span>

## <span data-ttu-id="a5ed2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a5ed2-110">EXAMPLES</span></span>

### <span data-ttu-id="a5ed2-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a5ed2-111">Example 1</span></span>
```
PS C:\> Merge-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111","11111111-0000-0000-0000-1111111111"
```

<span data-ttu-id="a5ed2-112">Unire le due specificate `Reservation` in una `Reservation`</span><span class="sxs-lookup"><span data-stu-id="a5ed2-112">Merge the two specified `Reservation`s into one `Reservation`</span></span>

## <span data-ttu-id="a5ed2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5ed2-113">PARAMETERS</span></span>

### <span data-ttu-id="a5ed2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5ed2-114">-DefaultProfile</span></span>
<span data-ttu-id="a5ed2-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a5ed2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5ed2-116">-Prenotazione</span><span class="sxs-lookup"><span data-stu-id="a5ed2-116">-Reservation</span></span>
<span data-ttu-id="a5ed2-117">Stringhe separate da virgola di due Id prenotazione da unire</span><span class="sxs-lookup"><span data-stu-id="a5ed2-117">Comma-separated strings of two ReservationIds to merge</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservation[]
Parameter Sets: PipeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5ed2-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="a5ed2-118">-ReservationId</span></span>
<span data-ttu-id="a5ed2-119">ReservationOrderId per `ReservationOrder` il valore che contiene le due `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="a5ed2-119">ReservationOrderId for the `ReservationOrder` that contains the two `Reservation`s</span></span>

```yaml
Type: System.Guid[]
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5ed2-120">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="a5ed2-120">-ReservationOrderId</span></span>
<span data-ttu-id="a5ed2-121">{{Fill ReservationOrderId Description}}</span><span class="sxs-lookup"><span data-stu-id="a5ed2-121">{{Fill ReservationOrderId Description}}</span></span>

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

### <span data-ttu-id="a5ed2-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5ed2-122">-Confirm</span></span>
<span data-ttu-id="a5ed2-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5ed2-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5ed2-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5ed2-124">-WhatIf</span></span>
<span data-ttu-id="a5ed2-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a5ed2-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5ed2-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a5ed2-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5ed2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5ed2-127">CommonParameters</span></span>
<span data-ttu-id="a5ed2-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5ed2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5ed2-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a5ed2-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5ed2-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="a5ed2-130">INPUTS</span></span>

### <span data-ttu-id="a5ed2-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a5ed2-131">None</span></span>

## <span data-ttu-id="a5ed2-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a5ed2-132">OUTPUTS</span></span>

### <span data-ttu-id="a5ed2-133">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="a5ed2-133">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="a5ed2-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="a5ed2-134">NOTES</span></span>

## <span data-ttu-id="a5ed2-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a5ed2-135">RELATED LINKS</span></span>
