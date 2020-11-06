---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationorderid
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrderId.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrderId.md
ms.openlocfilehash: ce6132c7c9b782969b78094de4a055415f3f30ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514148"
---
# <span data-ttu-id="7d228-101">Get-AzureRmReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="7d228-101">Get-AzureRmReservationOrderId</span></span>

## <span data-ttu-id="7d228-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7d228-102">SYNOPSIS</span></span>
<span data-ttu-id="7d228-103">Ottenere l'elenco degli `ReservationOrder` ID applicabili.</span><span class="sxs-lookup"><span data-stu-id="7d228-103">Get list of applicable `ReservationOrder` Ids.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d228-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7d228-104">SYNTAX</span></span>

```
Get-AzureRmReservationOrderId [-SubscriptionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="7d228-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7d228-105">DESCRIPTION</span></span>
<span data-ttu-id="7d228-106">Ottenere gli ID di `ReservationOrder` s applicabili che possono essere applicati a questo abbonamento.</span><span class="sxs-lookup"><span data-stu-id="7d228-106">Get Ids of applicable `ReservationOrder`s that can be applied to this subscription.</span></span>

## <span data-ttu-id="7d228-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7d228-107">EXAMPLES</span></span>

### <span data-ttu-id="7d228-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7d228-108">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationOrderId
```

<span data-ttu-id="7d228-109">Ottenere l'applicazione `ReservationOrder` per l'abbonamento predefinito</span><span class="sxs-lookup"><span data-stu-id="7d228-109">Get applied `ReservationOrder` for default subscription</span></span>

### <span data-ttu-id="7d228-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7d228-110">Example 2</span></span>
```
PS C:\> Get-AzureRmReservationOrderId -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="7d228-111">Ottenere l'applicazione `ReservationOrder` per l'abbonamento specificato</span><span class="sxs-lookup"><span data-stu-id="7d228-111">Get applied `ReservationOrder` for specified subscription</span></span>

## <span data-ttu-id="7d228-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7d228-112">PARAMETERS</span></span>

### <span data-ttu-id="7d228-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7d228-113">-SubscriptionId</span></span>
<span data-ttu-id="7d228-114">ID dell'abbonamento per ottenere la s applicata `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="7d228-114">Id of the subscription to get the applied `ReservationOrder`s</span></span>

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

### <span data-ttu-id="7d228-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d228-115">CommonParameters</span></span>
<span data-ttu-id="7d228-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d228-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d228-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d228-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d228-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7d228-118">INPUTS</span></span>

### <span data-ttu-id="7d228-119">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7d228-119">None</span></span>

## <span data-ttu-id="7d228-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7d228-120">OUTPUTS</span></span>

### <span data-ttu-id="7d228-121">Microsoft. Azure. Commands. reservations. Models. PSAppliedReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="7d228-121">Microsoft.Azure.Commands.Reservations.Models.PSAppliedReservationOrderId</span></span>

## <span data-ttu-id="7d228-122">Note</span><span class="sxs-lookup"><span data-stu-id="7d228-122">NOTES</span></span>

## <span data-ttu-id="7d228-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7d228-123">RELATED LINKS</span></span>

