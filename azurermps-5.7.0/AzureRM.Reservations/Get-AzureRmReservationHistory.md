---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationHistory.md
ms.openlocfilehash: 75ff92efe1a37e55396da7dc6d644408952ed179
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519378"
---
# <span data-ttu-id="d7113-101">Get-AzureRmReservationHistory</span><span class="sxs-lookup"><span data-stu-id="d7113-101">Get-AzureRmReservationHistory</span></span>

## <span data-ttu-id="d7113-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d7113-102">SYNOPSIS</span></span>
<span data-ttu-id="d7113-103">Ottenere la `Reservation` cronologia delle revisioni.</span><span class="sxs-lookup"><span data-stu-id="d7113-103">Get `Reservation` revision history.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7113-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d7113-104">SYNTAX</span></span>

### <span data-ttu-id="d7113-105">CommandLine (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d7113-105">CommandLine (Default)</span></span>
```
Get-AzureRmReservationHistory -ReservationOrderId <String> -ReservationId <String> [<CommonParameters>]
```

### <span data-ttu-id="d7113-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="d7113-106">PipeObject</span></span>
```
Get-AzureRmReservationHistory -Reservation <PSReservation> [<CommonParameters>]
```

## <span data-ttu-id="d7113-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d7113-107">DESCRIPTION</span></span>
<span data-ttu-id="d7113-108">Elenco di tutte le revisioni per `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="d7113-108">List of all the revisions for the `Reservation`.</span></span>

## <span data-ttu-id="d7113-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d7113-109">EXAMPLES</span></span>

### <span data-ttu-id="d7113-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d7113-110">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationHistory -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="d7113-111">Ottenere la cronologia delle revisioni della prenotazione specifica</span><span class="sxs-lookup"><span data-stu-id="d7113-111">Get the revision history of the specific reservation</span></span>

## <span data-ttu-id="d7113-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d7113-112">PARAMETERS</span></span>

### <span data-ttu-id="d7113-113">-Prenotazione</span><span class="sxs-lookup"><span data-stu-id="d7113-113">-Reservation</span></span>
<span data-ttu-id="d7113-114">Parametro oggetto pipe per `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="d7113-114">Pipe object parameter for `Reservation`s</span></span>

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

### <span data-ttu-id="d7113-115">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="d7113-115">-ReservationId</span></span>
<span data-ttu-id="d7113-116">ReservationId di `Reservation` cui deve essere visualizzata la cronologia</span><span class="sxs-lookup"><span data-stu-id="d7113-116">ReservationId of the `Reservation` of which history is to be shown</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7113-117">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="d7113-117">-ReservationOrderId</span></span>
<span data-ttu-id="d7113-118">ReservationOrderId per il `ReservationOrder` che contiene l' `Reservation`</span><span class="sxs-lookup"><span data-stu-id="d7113-118">ReservationOrderId for the `ReservationOrder` that contains the `Reservation`</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7113-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7113-119">CommonParameters</span></span>
<span data-ttu-id="d7113-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7113-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7113-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7113-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7113-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d7113-122">INPUTS</span></span>

### <span data-ttu-id="d7113-123">System. String</span><span class="sxs-lookup"><span data-stu-id="d7113-123">System.String</span></span>
<span data-ttu-id="d7113-124">Microsoft. Azure. Commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="d7113-124">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="d7113-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d7113-125">OUTPUTS</span></span>

### <span data-ttu-id="d7113-126">Microsoft. Azure. Commands. reservations. Models. PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="d7113-126">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

## <span data-ttu-id="d7113-127">Note</span><span class="sxs-lookup"><span data-stu-id="d7113-127">NOTES</span></span>

## <span data-ttu-id="d7113-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d7113-128">RELATED LINKS</span></span>

