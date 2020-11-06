---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/split-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Split-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Split-AzureRmReservation.md
ms.openlocfilehash: 89c19f2c61604f3c38ba8cc9679f956d68df3179
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514152"
---
# <span data-ttu-id="e35ee-101">Split-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="e35ee-101">Split-AzureRmReservation</span></span>

## <span data-ttu-id="e35ee-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e35ee-102">SYNOPSIS</span></span>
<span data-ttu-id="e35ee-103">Suddividere una `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="e35ee-103">Split a `Reservation`.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e35ee-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e35ee-104">SYNTAX</span></span>

### <span data-ttu-id="e35ee-105">CommandLine (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e35ee-105">CommandLine (Default)</span></span>
```
Split-AzureRmReservation -ReservationOrderId <String> -ReservationId <String> -Quantity <Nullable`1[]>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e35ee-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="e35ee-106">PipeObject</span></span>
```
Split-AzureRmReservation -Quantity <Nullable`1[]> -Reservation <PSReservation> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e35ee-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e35ee-107">DESCRIPTION</span></span>
<span data-ttu-id="e35ee-108">Suddividere una `Reservation` in due `Reservation` s con la distribuzione di quantità specificata.</span><span class="sxs-lookup"><span data-stu-id="e35ee-108">Split a `Reservation` into two `Reservation`s with specified quantity distribution.</span></span>

## <span data-ttu-id="e35ee-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e35ee-109">EXAMPLES</span></span>

### <span data-ttu-id="e35ee-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e35ee-110">Example 1</span></span>
```
PS C:\> Split-AzureRmReservation -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111" -Quantities 2,3
```

<span data-ttu-id="e35ee-111">Suddividere il parametro specificato `Reservation` in due `Reservation` s con le quantità corrispondenti</span><span class="sxs-lookup"><span data-stu-id="e35ee-111">Split the specified `Reservation` into two `Reservation`s with the corresponding quantities</span></span>

## <span data-ttu-id="e35ee-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e35ee-112">PARAMETERS</span></span>

### <span data-ttu-id="e35ee-113">-Quantità</span><span class="sxs-lookup"><span data-stu-id="e35ee-113">-Quantity</span></span>
<span data-ttu-id="e35ee-114">Numeri interi separati da virgola per il campo quantità delle due `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="e35ee-114">Comma-separated integers for quantity field of the two `Reservation`s</span></span>

```yaml
Type: Nullable`1[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e35ee-115">-Prenotazione</span><span class="sxs-lookup"><span data-stu-id="e35ee-115">-Reservation</span></span>
<span data-ttu-id="e35ee-116">Parametro oggetto pipe per `Reservation`</span><span class="sxs-lookup"><span data-stu-id="e35ee-116">Pipe object parameter for `Reservation`</span></span>

```yaml
Type: PSReservation
Parameter Sets: PipeObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e35ee-117">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="e35ee-117">-ReservationId</span></span>
<span data-ttu-id="e35ee-118">ID della `Reservation` divisione a</span><span class="sxs-lookup"><span data-stu-id="e35ee-118">Id of the `Reservation` to split</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e35ee-119">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="e35ee-119">-ReservationOrderId</span></span>
<span data-ttu-id="e35ee-120">ID dell' `ReservationOrder` che contiene l' `Reservation` utente che vuole suddividere</span><span class="sxs-lookup"><span data-stu-id="e35ee-120">Id of the `ReservationOrder` that contains the `Reservation` that user wants to split</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e35ee-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e35ee-121">-Confirm</span></span>
<span data-ttu-id="e35ee-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e35ee-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e35ee-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e35ee-123">-WhatIf</span></span>
<span data-ttu-id="e35ee-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e35ee-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e35ee-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e35ee-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e35ee-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e35ee-126">CommonParameters</span></span>
<span data-ttu-id="e35ee-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e35ee-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e35ee-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e35ee-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e35ee-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e35ee-129">INPUTS</span></span>

### <span data-ttu-id="e35ee-130">Microsoft. Azure. Commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="e35ee-130">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="e35ee-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e35ee-131">OUTPUTS</span></span>

### <span data-ttu-id="e35ee-132">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. reservations. Models. PSReservation, Microsoft. Azure. Commands. reservations, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e35ee-132">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Reservations.Models.PSReservation, Microsoft.Azure.Commands.Reservations, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e35ee-133">Note</span><span class="sxs-lookup"><span data-stu-id="e35ee-133">NOTES</span></span>

## <span data-ttu-id="e35ee-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e35ee-134">RELATED LINKS</span></span>

