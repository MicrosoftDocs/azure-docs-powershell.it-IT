---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrder.md
ms.openlocfilehash: 0dc5eba8b498be7814ae74eca6953a5cadb01f22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514155"
---
# <span data-ttu-id="d50fe-101">Get-AzureRmReservationOrder</span><span class="sxs-lookup"><span data-stu-id="d50fe-101">Get-AzureRmReservationOrder</span></span>

## <span data-ttu-id="d50fe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d50fe-102">SYNOPSIS</span></span>
<span data-ttu-id="d50fe-103">Ottieni `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="d50fe-103">Get `ReservationOrder`</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d50fe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d50fe-104">SYNTAX</span></span>

```
Get-AzureRmReservationOrder [-ReservationOrderId <String>] [<CommonParameters>]
```

## <span data-ttu-id="d50fe-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d50fe-105">DESCRIPTION</span></span>
<span data-ttu-id="d50fe-106">Elenco di tutte le `ReservationOrder` s a cui l'utente ha accesso nel tenant corrente.</span><span class="sxs-lookup"><span data-stu-id="d50fe-106">List of all the `ReservationOrder`s that the user has access to in the current tenant.</span></span> <span data-ttu-id="d50fe-107">Se il parametro ReservationOrderId è impostato, ottenere quello specifico ReservationOrder.</span><span class="sxs-lookup"><span data-stu-id="d50fe-107">If ReservationOrderId parameter is set, get that specific ReservationOrder.</span></span>

## <span data-ttu-id="d50fe-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d50fe-108">EXAMPLES</span></span>

### <span data-ttu-id="d50fe-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d50fe-109">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationOrder
```

<span data-ttu-id="d50fe-110">Elencare tutti `ReservationOrder` gli utenti a cui l'utente ha accesso nel tenant corrente</span><span class="sxs-lookup"><span data-stu-id="d50fe-110">List all `ReservationOrder` that the user has access to in the current tenant</span></span>

### <span data-ttu-id="d50fe-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="d50fe-111">Example 2</span></span>
```
PS C:\> Get-AzureRmReservationOrder -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="d50fe-112">Ottenere `ReservationOrder` con il ReservationOrderId specificato</span><span class="sxs-lookup"><span data-stu-id="d50fe-112">Get `ReservationOrder` with the specified ReservationOrderId</span></span>

## <span data-ttu-id="d50fe-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d50fe-113">PARAMETERS</span></span>

### <span data-ttu-id="d50fe-114">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="d50fe-114">-ReservationOrderId</span></span>
<span data-ttu-id="d50fe-115">ID dello specifico ReservationOrder che l'utente vuole vedere</span><span class="sxs-lookup"><span data-stu-id="d50fe-115">Id of the specific ReservationOrder that user wants to see</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d50fe-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d50fe-116">CommonParameters</span></span>
<span data-ttu-id="d50fe-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d50fe-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d50fe-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d50fe-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d50fe-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d50fe-119">INPUTS</span></span>

### <span data-ttu-id="d50fe-120">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d50fe-120">None</span></span>

## <span data-ttu-id="d50fe-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d50fe-121">OUTPUTS</span></span>

### <span data-ttu-id="d50fe-122">Microsoft. Azure. Commands. reservations. Models. PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="d50fe-122">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>
<span data-ttu-id="d50fe-123">Microsoft. Azure. Commands. reservations. Models. PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="d50fe-123">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

## <span data-ttu-id="d50fe-124">Note</span><span class="sxs-lookup"><span data-stu-id="d50fe-124">NOTES</span></span>

## <span data-ttu-id="d50fe-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d50fe-125">RELATED LINKS</span></span>

