---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/merge-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Merge-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Merge-AzureRmReservation.md
ms.openlocfilehash: 6428e4df850d2806939f5d9f8d4e115698e91fb1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685751"
---
# <span data-ttu-id="76051-101">Merge-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="76051-101">Merge-AzureRmReservation</span></span>

## <span data-ttu-id="76051-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="76051-102">SYNOPSIS</span></span>
<span data-ttu-id="76051-103">Unisce due `Reservation` s.</span><span class="sxs-lookup"><span data-stu-id="76051-103">Merges two `Reservation`s.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76051-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="76051-104">SYNTAX</span></span>

### <span data-ttu-id="76051-105">CommandLine (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="76051-105">CommandLine (Default)</span></span>
```
Merge-AzureRmReservation -ReservationOrderId <Guid> -ReservationId <Guid[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76051-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="76051-106">PipeObject</span></span>
```
Merge-AzureRmReservation -Reservation <PSReservation[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76051-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="76051-107">DESCRIPTION</span></span>
<span data-ttu-id="76051-108">Unisci l'oggetto `Reservation` s specificato in un nuovo `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="76051-108">Merge the specified `Reservation`s into a new `Reservation`.</span></span> <span data-ttu-id="76051-109">Le due `Reservation` s Unite devono avere le stesse proprietà.</span><span class="sxs-lookup"><span data-stu-id="76051-109">The two `Reservation`s being merged must have same properties.</span></span>

## <span data-ttu-id="76051-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="76051-110">EXAMPLES</span></span>

### <span data-ttu-id="76051-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="76051-111">Example 1</span></span>
```
PS C:\> Merge-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111","11111111-0000-0000-0000-1111111111"
```

<span data-ttu-id="76051-112">Unire i due `Reservation` s specificati in uno `Reservation`</span><span class="sxs-lookup"><span data-stu-id="76051-112">Merge the two specified `Reservation`s into one `Reservation`</span></span>

## <span data-ttu-id="76051-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="76051-113">PARAMETERS</span></span>

### <span data-ttu-id="76051-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76051-114">-DefaultProfile</span></span>
<span data-ttu-id="76051-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="76051-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76051-116">-Prenotazione</span><span class="sxs-lookup"><span data-stu-id="76051-116">-Reservation</span></span>
<span data-ttu-id="76051-117">Stringhe separate da virgole di due ReservationIds da unire</span><span class="sxs-lookup"><span data-stu-id="76051-117">Comma-separated strings of two ReservationIds to merge</span></span>

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

### <span data-ttu-id="76051-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="76051-118">-ReservationId</span></span>
<span data-ttu-id="76051-119">ReservationOrderId per il `ReservationOrder` che contiene i due `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="76051-119">ReservationOrderId for the `ReservationOrder` that contains the two `Reservation`s</span></span>

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

### <span data-ttu-id="76051-120">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="76051-120">-ReservationOrderId</span></span>
<span data-ttu-id="76051-121">{{Fill ReservationOrderId Description}}</span><span class="sxs-lookup"><span data-stu-id="76051-121">{{Fill ReservationOrderId Description}}</span></span>

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

### <span data-ttu-id="76051-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="76051-122">-Confirm</span></span>
<span data-ttu-id="76051-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76051-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76051-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76051-124">-WhatIf</span></span>
<span data-ttu-id="76051-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="76051-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="76051-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="76051-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76051-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76051-127">CommonParameters</span></span>
<span data-ttu-id="76051-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76051-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76051-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76051-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76051-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="76051-130">INPUTS</span></span>

### <span data-ttu-id="76051-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="76051-131">None</span></span>

## <span data-ttu-id="76051-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="76051-132">OUTPUTS</span></span>

### <span data-ttu-id="76051-133">Microsoft. Azure. Commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="76051-133">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="76051-134">Note</span><span class="sxs-lookup"><span data-stu-id="76051-134">NOTES</span></span>

## <span data-ttu-id="76051-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="76051-135">RELATED LINKS</span></span>
