---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/split-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Split-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Split-AzureRmReservation.md
ms.openlocfilehash: bc1fba5c7fa7e01a3c2461907a214809e175f3ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509104"
---
# <span data-ttu-id="22125-101">Split-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="22125-101">Split-AzureRmReservation</span></span>

## <span data-ttu-id="22125-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="22125-102">SYNOPSIS</span></span>
<span data-ttu-id="22125-103">Suddividere una `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="22125-103">Split a `Reservation`.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22125-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="22125-104">SYNTAX</span></span>

### <span data-ttu-id="22125-105">CommandLine (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="22125-105">CommandLine (Default)</span></span>
```
Split-AzureRmReservation -ReservationOrderId <Guid> -ReservationId <Guid> -Quantity <Int32[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22125-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="22125-106">PipeObject</span></span>
```
Split-AzureRmReservation -Quantity <Int32[]> -Reservation <PSReservation>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22125-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22125-107">DESCRIPTION</span></span>
<span data-ttu-id="22125-108">Suddividere una `Reservation` in due `Reservation` s con la distribuzione di quantità specificata.</span><span class="sxs-lookup"><span data-stu-id="22125-108">Split a `Reservation` into two `Reservation`s with specified quantity distribution.</span></span>

## <span data-ttu-id="22125-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="22125-109">EXAMPLES</span></span>

### <span data-ttu-id="22125-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="22125-110">Example 1</span></span>
```
PS C:\> Split-AzureRmReservation -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111" -Quantities 2,3
```

<span data-ttu-id="22125-111">Suddividere il parametro specificato `Reservation` in due `Reservation` s con le quantità corrispondenti</span><span class="sxs-lookup"><span data-stu-id="22125-111">Split the specified `Reservation` into two `Reservation`s with the corresponding quantities</span></span>

## <span data-ttu-id="22125-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="22125-112">PARAMETERS</span></span>

### <span data-ttu-id="22125-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22125-113">-DefaultProfile</span></span>
<span data-ttu-id="22125-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="22125-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22125-115">-Quantità</span><span class="sxs-lookup"><span data-stu-id="22125-115">-Quantity</span></span>
<span data-ttu-id="22125-116">Numeri interi separati da virgola per il campo quantità delle due `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="22125-116">Comma-separated integers for quantity field of the two `Reservation`s</span></span>

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

### <span data-ttu-id="22125-117">-Prenotazione</span><span class="sxs-lookup"><span data-stu-id="22125-117">-Reservation</span></span>
<span data-ttu-id="22125-118">Parametro oggetto pipe per `Reservation`</span><span class="sxs-lookup"><span data-stu-id="22125-118">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="22125-119">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="22125-119">-ReservationId</span></span>
<span data-ttu-id="22125-120">ID della `Reservation` divisione a</span><span class="sxs-lookup"><span data-stu-id="22125-120">Id of the `Reservation` to split</span></span>

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

### <span data-ttu-id="22125-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="22125-121">-ReservationOrderId</span></span>
<span data-ttu-id="22125-122">ID dell' `ReservationOrder` che contiene l' `Reservation` utente che vuole suddividere</span><span class="sxs-lookup"><span data-stu-id="22125-122">Id of the `ReservationOrder` that contains the `Reservation` that user wants to split</span></span>

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

### <span data-ttu-id="22125-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="22125-123">-Confirm</span></span>
<span data-ttu-id="22125-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22125-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22125-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22125-125">-WhatIf</span></span>
<span data-ttu-id="22125-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="22125-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="22125-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="22125-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22125-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22125-128">CommonParameters</span></span>
<span data-ttu-id="22125-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22125-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22125-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22125-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22125-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="22125-131">INPUTS</span></span>

### <span data-ttu-id="22125-132">Microsoft. Azure. Commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="22125-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>
<span data-ttu-id="22125-133">Parametri: prenotazione (ByValue)</span><span class="sxs-lookup"><span data-stu-id="22125-133">Parameters: Reservation (ByValue)</span></span>

## <span data-ttu-id="22125-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="22125-134">OUTPUTS</span></span>

### <span data-ttu-id="22125-135">Microsoft. Azure. Commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="22125-135">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="22125-136">Note</span><span class="sxs-lookup"><span data-stu-id="22125-136">NOTES</span></span>

## <span data-ttu-id="22125-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="22125-137">RELATED LINKS</span></span>
