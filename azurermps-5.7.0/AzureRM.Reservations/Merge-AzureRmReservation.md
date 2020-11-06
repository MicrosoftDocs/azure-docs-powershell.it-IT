---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/merge-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Merge-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Merge-AzureRmReservation.md
ms.openlocfilehash: 1f5b0c6a743c9ed26864144cf8df21917bc2ac45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514151"
---
# <span data-ttu-id="15b61-101">Merge-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="15b61-101">Merge-AzureRmReservation</span></span>

## <span data-ttu-id="15b61-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="15b61-102">SYNOPSIS</span></span>
<span data-ttu-id="15b61-103">Unisce due `Reservation` s.</span><span class="sxs-lookup"><span data-stu-id="15b61-103">Merges two `Reservation`s.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15b61-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="15b61-104">SYNTAX</span></span>

### <span data-ttu-id="15b61-105">CommandLine (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="15b61-105">CommandLine (Default)</span></span>
```
Merge-AzureRmReservation -ReservationOrderId <String> -ReservationId <String[]> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="15b61-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="15b61-106">PipeObject</span></span>
```
Merge-AzureRmReservation -Reservation <PSReservation[]> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15b61-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="15b61-107">DESCRIPTION</span></span>
<span data-ttu-id="15b61-108">Unisci l'oggetto `Reservation` s specificato in un nuovo `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="15b61-108">Merge the specified `Reservation`s into a new `Reservation`.</span></span> <span data-ttu-id="15b61-109">Le due `Reservation` s Unite devono avere le stesse proprietà.</span><span class="sxs-lookup"><span data-stu-id="15b61-109">The two `Reservation`s being merged must have same properties.</span></span>

## <span data-ttu-id="15b61-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="15b61-110">EXAMPLES</span></span>

### <span data-ttu-id="15b61-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="15b61-111">Example 1</span></span>
```
PS C:\> Merge-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111","11111111-0000-0000-0000-1111111111"
```

<span data-ttu-id="15b61-112">Unire i due `Reservation` s specificati in uno `Reservation`</span><span class="sxs-lookup"><span data-stu-id="15b61-112">Merge the two specified `Reservation`s into one `Reservation`</span></span>

## <span data-ttu-id="15b61-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="15b61-113">PARAMETERS</span></span>

### <span data-ttu-id="15b61-114">-Prenotazione</span><span class="sxs-lookup"><span data-stu-id="15b61-114">-Reservation</span></span>
<span data-ttu-id="15b61-115">Stringhe separate da virgole di due ReservationIds da unire</span><span class="sxs-lookup"><span data-stu-id="15b61-115">Comma-separated strings of two ReservationIds to merge</span></span>

```yaml
Type: PSReservation[]
Parameter Sets: PipeObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15b61-116">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="15b61-116">-ReservationId</span></span>
<span data-ttu-id="15b61-117">ReservationOrderId per il `ReservationOrder` che contiene i due `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="15b61-117">ReservationOrderId for the `ReservationOrder` that contains the two `Reservation`s</span></span>

```yaml
Type: String[]
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15b61-118">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="15b61-118">-ReservationOrderId</span></span>
<span data-ttu-id="15b61-119">{{Fill ReservationOrderId Description}}</span><span class="sxs-lookup"><span data-stu-id="15b61-119">{{Fill ReservationOrderId Description}}</span></span>

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

### <span data-ttu-id="15b61-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="15b61-120">-Confirm</span></span>
<span data-ttu-id="15b61-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15b61-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15b61-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15b61-122">-WhatIf</span></span>
<span data-ttu-id="15b61-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="15b61-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="15b61-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="15b61-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15b61-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15b61-125">CommonParameters</span></span>
<span data-ttu-id="15b61-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15b61-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15b61-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15b61-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15b61-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="15b61-128">INPUTS</span></span>

### <span data-ttu-id="15b61-129">Microsoft. Azure. Commands. reservations. Models. PSReservation []</span><span class="sxs-lookup"><span data-stu-id="15b61-129">Microsoft.Azure.Commands.Reservations.Models.PSReservation[]</span></span>

## <span data-ttu-id="15b61-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="15b61-130">OUTPUTS</span></span>

### <span data-ttu-id="15b61-131">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. reservations. Models. PSReservation, Microsoft. Azure. Commands. reservations, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="15b61-131">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Reservations.Models.PSReservation, Microsoft.Azure.Commands.Reservations, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="15b61-132">Note</span><span class="sxs-lookup"><span data-stu-id="15b61-132">NOTES</span></span>

## <span data-ttu-id="15b61-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="15b61-133">RELATED LINKS</span></span>

