---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/merge-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Merge-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Merge-AzReservation.md
ms.openlocfilehash: fc0b04049184334c59a38226e031342fc29207b2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370058"
---
# <span data-ttu-id="3538d-101">Merge-AzReservation</span><span class="sxs-lookup"><span data-stu-id="3538d-101">Merge-AzReservation</span></span>

## <span data-ttu-id="3538d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3538d-102">SYNOPSIS</span></span>
<span data-ttu-id="3538d-103">Unisce due `Reservation` s.</span><span class="sxs-lookup"><span data-stu-id="3538d-103">Merges two `Reservation`s.</span></span>

## <span data-ttu-id="3538d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3538d-104">SYNTAX</span></span>

### <span data-ttu-id="3538d-105">CommandLine (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3538d-105">CommandLine (Default)</span></span>
```
Merge-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3538d-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="3538d-106">PipeObject</span></span>
```
Merge-AzReservation -Reservation <PSReservation[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3538d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3538d-107">DESCRIPTION</span></span>
<span data-ttu-id="3538d-108">Unisci l'oggetto `Reservation` s specificato in un nuovo `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="3538d-108">Merge the specified `Reservation`s into a new `Reservation`.</span></span> <span data-ttu-id="3538d-109">Le due `Reservation` s Unite devono avere le stesse proprietà.</span><span class="sxs-lookup"><span data-stu-id="3538d-109">The two `Reservation`s being merged must have same properties.</span></span>

## <span data-ttu-id="3538d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3538d-110">EXAMPLES</span></span>

### <span data-ttu-id="3538d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3538d-111">Example 1</span></span>
```
PS C:\> Merge-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111","11111111-0000-0000-0000-1111111111"
```

<span data-ttu-id="3538d-112">Unire i due `Reservation` s specificati in uno `Reservation`</span><span class="sxs-lookup"><span data-stu-id="3538d-112">Merge the two specified `Reservation`s into one `Reservation`</span></span>

## <span data-ttu-id="3538d-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3538d-113">PARAMETERS</span></span>

### <span data-ttu-id="3538d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3538d-114">-DefaultProfile</span></span>
<span data-ttu-id="3538d-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3538d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3538d-116">-Prenotazione</span><span class="sxs-lookup"><span data-stu-id="3538d-116">-Reservation</span></span>
<span data-ttu-id="3538d-117">Stringhe separate da virgole di due ReservationIds da unire</span><span class="sxs-lookup"><span data-stu-id="3538d-117">Comma-separated strings of two ReservationIds to merge</span></span>

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

### <span data-ttu-id="3538d-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="3538d-118">-ReservationId</span></span>
<span data-ttu-id="3538d-119">ReservationOrderId per il `ReservationOrder` che contiene i due `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="3538d-119">ReservationOrderId for the `ReservationOrder` that contains the two `Reservation`s</span></span>

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

### <span data-ttu-id="3538d-120">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="3538d-120">-ReservationOrderId</span></span>
<span data-ttu-id="3538d-121">{{Fill ReservationOrderId Description}}</span><span class="sxs-lookup"><span data-stu-id="3538d-121">{{Fill ReservationOrderId Description}}</span></span>

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

### <span data-ttu-id="3538d-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3538d-122">-Confirm</span></span>
<span data-ttu-id="3538d-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3538d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3538d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3538d-124">-WhatIf</span></span>
<span data-ttu-id="3538d-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3538d-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3538d-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3538d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3538d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3538d-127">CommonParameters</span></span>
<span data-ttu-id="3538d-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3538d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3538d-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3538d-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3538d-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3538d-130">INPUTS</span></span>

### <span data-ttu-id="3538d-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3538d-131">None</span></span>

## <span data-ttu-id="3538d-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3538d-132">OUTPUTS</span></span>

### <span data-ttu-id="3538d-133">Microsoft. Azure. Commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="3538d-133">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="3538d-134">Note</span><span class="sxs-lookup"><span data-stu-id="3538d-134">NOTES</span></span>

## <span data-ttu-id="3538d-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3538d-135">RELATED LINKS</span></span>
