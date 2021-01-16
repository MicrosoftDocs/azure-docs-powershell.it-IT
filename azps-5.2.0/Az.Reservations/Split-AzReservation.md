---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/split-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
ms.openlocfilehash: b879b5b47c752a331f0c2d70a6d37e57b113d816
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325819"
---
# <span data-ttu-id="9e7a2-101">Split-AzReservation</span><span class="sxs-lookup"><span data-stu-id="9e7a2-101">Split-AzReservation</span></span>

## <span data-ttu-id="9e7a2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9e7a2-102">SYNOPSIS</span></span>
<span data-ttu-id="9e7a2-103">Suddividere una `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="9e7a2-103">Split a `Reservation`.</span></span>

## <span data-ttu-id="9e7a2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9e7a2-104">SYNTAX</span></span>

### <span data-ttu-id="9e7a2-105">CommandLine (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9e7a2-105">CommandLine (Default)</span></span>
```
Split-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -Quantity <Int32[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e7a2-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="9e7a2-106">PipeObject</span></span>
```
Split-AzReservation -Quantity <Int32[]> -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e7a2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e7a2-107">DESCRIPTION</span></span>
<span data-ttu-id="9e7a2-108">Suddividere una `Reservation` in due `Reservation` s con la distribuzione di quantità specificata.</span><span class="sxs-lookup"><span data-stu-id="9e7a2-108">Split a `Reservation` into two `Reservation`s with specified quantity distribution.</span></span>

## <span data-ttu-id="9e7a2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9e7a2-109">EXAMPLES</span></span>

### <span data-ttu-id="9e7a2-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9e7a2-110">Example 1</span></span>
```
PS C:\> Split-AzReservation -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111" -Quantities 2,3
```

<span data-ttu-id="9e7a2-111">Suddividere il parametro specificato `Reservation` in due `Reservation` s con le quantità corrispondenti</span><span class="sxs-lookup"><span data-stu-id="9e7a2-111">Split the specified `Reservation` into two `Reservation`s with the corresponding quantities</span></span>

## <span data-ttu-id="9e7a2-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9e7a2-112">PARAMETERS</span></span>

### <span data-ttu-id="9e7a2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e7a2-113">-DefaultProfile</span></span>
<span data-ttu-id="9e7a2-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9e7a2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e7a2-115">-Quantità</span><span class="sxs-lookup"><span data-stu-id="9e7a2-115">-Quantity</span></span>
<span data-ttu-id="9e7a2-116">Numeri interi separati da virgola per il campo quantità delle due `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="9e7a2-116">Comma-separated integers for quantity field of the two `Reservation`s</span></span>

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

### <span data-ttu-id="9e7a2-117">-Prenotazione</span><span class="sxs-lookup"><span data-stu-id="9e7a2-117">-Reservation</span></span>
<span data-ttu-id="9e7a2-118">Parametro oggetto pipe per `Reservation`</span><span class="sxs-lookup"><span data-stu-id="9e7a2-118">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="9e7a2-119">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="9e7a2-119">-ReservationId</span></span>
<span data-ttu-id="9e7a2-120">ID della `Reservation` divisione a</span><span class="sxs-lookup"><span data-stu-id="9e7a2-120">Id of the `Reservation` to split</span></span>

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

### <span data-ttu-id="9e7a2-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="9e7a2-121">-ReservationOrderId</span></span>
<span data-ttu-id="9e7a2-122">ID dell' `ReservationOrder` che contiene l' `Reservation` utente che vuole suddividere</span><span class="sxs-lookup"><span data-stu-id="9e7a2-122">Id of the `ReservationOrder` that contains the `Reservation` that user wants to split</span></span>

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

### <span data-ttu-id="9e7a2-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9e7a2-123">-Confirm</span></span>
<span data-ttu-id="9e7a2-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e7a2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e7a2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e7a2-125">-WhatIf</span></span>
<span data-ttu-id="9e7a2-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9e7a2-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9e7a2-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9e7a2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e7a2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e7a2-128">CommonParameters</span></span>
<span data-ttu-id="9e7a2-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e7a2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e7a2-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e7a2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e7a2-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9e7a2-131">INPUTS</span></span>

### <span data-ttu-id="9e7a2-132">Microsoft. Azure. Commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="9e7a2-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="9e7a2-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9e7a2-133">OUTPUTS</span></span>

### <span data-ttu-id="9e7a2-134">Microsoft. Azure. Commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="9e7a2-134">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="9e7a2-135">Note</span><span class="sxs-lookup"><span data-stu-id="9e7a2-135">NOTES</span></span>

## <span data-ttu-id="9e7a2-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9e7a2-136">RELATED LINKS</span></span>
