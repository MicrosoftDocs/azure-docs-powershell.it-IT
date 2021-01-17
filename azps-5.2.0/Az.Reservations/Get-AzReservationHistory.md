---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationHistory.md
ms.openlocfilehash: cfc7ab08904f007f874e1b45fd6d27a5712abee9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370142"
---
# <span data-ttu-id="28f87-101">Get-AzReservationHistory</span><span class="sxs-lookup"><span data-stu-id="28f87-101">Get-AzReservationHistory</span></span>

## <span data-ttu-id="28f87-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="28f87-102">SYNOPSIS</span></span>
<span data-ttu-id="28f87-103">Ottenere la `Reservation` cronologia delle revisioni.</span><span class="sxs-lookup"><span data-stu-id="28f87-103">Get `Reservation` revision history.</span></span>

## <span data-ttu-id="28f87-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="28f87-104">SYNTAX</span></span>

### <span data-ttu-id="28f87-105">CommandLine (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="28f87-105">CommandLine (Default)</span></span>
```
Get-AzReservationHistory -ReservationOrderId <Guid> -ReservationId <Guid>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28f87-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="28f87-106">PipeObject</span></span>
```
Get-AzReservationHistory -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="28f87-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="28f87-107">DESCRIPTION</span></span>
<span data-ttu-id="28f87-108">Elenco di tutte le revisioni per `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="28f87-108">List of all the revisions for the `Reservation`.</span></span>

## <span data-ttu-id="28f87-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="28f87-109">EXAMPLES</span></span>

### <span data-ttu-id="28f87-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="28f87-110">Example 1</span></span>
```
PS C:\> Get-AzReservationHistory -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="28f87-111">Ottenere la cronologia delle revisioni della prenotazione specifica</span><span class="sxs-lookup"><span data-stu-id="28f87-111">Get the revision history of the specific reservation</span></span>

## <span data-ttu-id="28f87-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="28f87-112">PARAMETERS</span></span>

### <span data-ttu-id="28f87-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28f87-113">-DefaultProfile</span></span>
<span data-ttu-id="28f87-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="28f87-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28f87-115">-Prenotazione</span><span class="sxs-lookup"><span data-stu-id="28f87-115">-Reservation</span></span>
<span data-ttu-id="28f87-116">Parametro oggetto pipe per `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="28f87-116">Pipe object parameter for `Reservation`s</span></span>

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

### <span data-ttu-id="28f87-117">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="28f87-117">-ReservationId</span></span>
<span data-ttu-id="28f87-118">ReservationId di `Reservation` cui deve essere visualizzata la cronologia</span><span class="sxs-lookup"><span data-stu-id="28f87-118">ReservationId of the `Reservation` of which history is to be shown</span></span>

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

### <span data-ttu-id="28f87-119">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="28f87-119">-ReservationOrderId</span></span>
<span data-ttu-id="28f87-120">ReservationOrderId per il `ReservationOrder` che contiene l' `Reservation`</span><span class="sxs-lookup"><span data-stu-id="28f87-120">ReservationOrderId for the `ReservationOrder` that contains the `Reservation`</span></span>

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

### <span data-ttu-id="28f87-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28f87-121">CommonParameters</span></span>
<span data-ttu-id="28f87-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28f87-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28f87-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="28f87-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28f87-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="28f87-124">INPUTS</span></span>

### <span data-ttu-id="28f87-125">System. Guid</span><span class="sxs-lookup"><span data-stu-id="28f87-125">System.Guid</span></span>

### <span data-ttu-id="28f87-126">Microsoft. Azure. Commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="28f87-126">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="28f87-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="28f87-127">OUTPUTS</span></span>

### <span data-ttu-id="28f87-128">Microsoft. Azure. Commands. reservations. Models. PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="28f87-128">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

## <span data-ttu-id="28f87-129">Note</span><span class="sxs-lookup"><span data-stu-id="28f87-129">NOTES</span></span>

## <span data-ttu-id="28f87-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="28f87-130">RELATED LINKS</span></span>
