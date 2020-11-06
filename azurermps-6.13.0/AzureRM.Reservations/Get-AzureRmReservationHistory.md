---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationHistory.md
ms.openlocfilehash: 3149e2fa0ef748d11583919161555805d54f5efc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93522027"
---
# <span data-ttu-id="c36a1-101">Get-AzureRmReservationHistory</span><span class="sxs-lookup"><span data-stu-id="c36a1-101">Get-AzureRmReservationHistory</span></span>

## <span data-ttu-id="c36a1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c36a1-102">SYNOPSIS</span></span>
<span data-ttu-id="c36a1-103">Ottenere la `Reservation` cronologia delle revisioni.</span><span class="sxs-lookup"><span data-stu-id="c36a1-103">Get `Reservation` revision history.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c36a1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c36a1-104">SYNTAX</span></span>

### <span data-ttu-id="c36a1-105">CommandLine (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c36a1-105">CommandLine (Default)</span></span>
```
Get-AzureRmReservationHistory -ReservationOrderId <Guid> -ReservationId <Guid>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c36a1-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="c36a1-106">PipeObject</span></span>
```
Get-AzureRmReservationHistory -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c36a1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c36a1-107">DESCRIPTION</span></span>
<span data-ttu-id="c36a1-108">Elenco di tutte le revisioni per `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="c36a1-108">List of all the revisions for the `Reservation`.</span></span>

## <span data-ttu-id="c36a1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c36a1-109">EXAMPLES</span></span>

### <span data-ttu-id="c36a1-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c36a1-110">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationHistory -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="c36a1-111">Ottenere la cronologia delle revisioni della prenotazione specifica</span><span class="sxs-lookup"><span data-stu-id="c36a1-111">Get the revision history of the specific reservation</span></span>

## <span data-ttu-id="c36a1-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c36a1-112">PARAMETERS</span></span>

### <span data-ttu-id="c36a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c36a1-113">-DefaultProfile</span></span>
<span data-ttu-id="c36a1-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c36a1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c36a1-115">-Prenotazione</span><span class="sxs-lookup"><span data-stu-id="c36a1-115">-Reservation</span></span>
<span data-ttu-id="c36a1-116">Parametro oggetto pipe per `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="c36a1-116">Pipe object parameter for `Reservation`s</span></span>

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

### <span data-ttu-id="c36a1-117">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="c36a1-117">-ReservationId</span></span>
<span data-ttu-id="c36a1-118">ReservationId di `Reservation` cui deve essere visualizzata la cronologia</span><span class="sxs-lookup"><span data-stu-id="c36a1-118">ReservationId of the `Reservation` of which history is to be shown</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c36a1-119">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="c36a1-119">-ReservationOrderId</span></span>
<span data-ttu-id="c36a1-120">ReservationOrderId per il `ReservationOrder` che contiene l' `Reservation`</span><span class="sxs-lookup"><span data-stu-id="c36a1-120">ReservationOrderId for the `ReservationOrder` that contains the `Reservation`</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c36a1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c36a1-121">CommonParameters</span></span>
<span data-ttu-id="c36a1-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c36a1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c36a1-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c36a1-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c36a1-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c36a1-124">INPUTS</span></span>

### <span data-ttu-id="c36a1-125">System. Guid</span><span class="sxs-lookup"><span data-stu-id="c36a1-125">System.Guid</span></span>

### <span data-ttu-id="c36a1-126">Microsoft. Azure. Commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="c36a1-126">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>
<span data-ttu-id="c36a1-127">Parametri: prenotazione (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c36a1-127">Parameters: Reservation (ByValue)</span></span>

## <span data-ttu-id="c36a1-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c36a1-128">OUTPUTS</span></span>

### <span data-ttu-id="c36a1-129">Microsoft. Azure. Commands. reservations. Models. PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="c36a1-129">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

## <span data-ttu-id="c36a1-130">Note</span><span class="sxs-lookup"><span data-stu-id="c36a1-130">NOTES</span></span>

## <span data-ttu-id="c36a1-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c36a1-131">RELATED LINKS</span></span>
