---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/get-azreservationhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationHistory.md
ms.openlocfilehash: c0016eed43fa315a7bb135153c8b00c47248f235
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000301"
---
# <span data-ttu-id="38855-101">Get-AzReservationHistory</span><span class="sxs-lookup"><span data-stu-id="38855-101">Get-AzReservationHistory</span></span>

## <span data-ttu-id="38855-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38855-102">SYNOPSIS</span></span>
<span data-ttu-id="38855-103">Ottenere la `Reservation` cronologia delle revisioni.</span><span class="sxs-lookup"><span data-stu-id="38855-103">Get `Reservation` revision history.</span></span>

## <span data-ttu-id="38855-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="38855-104">SYNTAX</span></span>

### <span data-ttu-id="38855-105">CommandLine (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="38855-105">CommandLine (Default)</span></span>
```
Get-AzReservationHistory -ReservationOrderId <Guid> -ReservationId <Guid>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38855-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="38855-106">PipeObject</span></span>
```
Get-AzReservationHistory -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="38855-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="38855-107">DESCRIPTION</span></span>
<span data-ttu-id="38855-108">Elenco di tutte le revisioni per `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="38855-108">List of all the revisions for the `Reservation`.</span></span>

## <span data-ttu-id="38855-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="38855-109">EXAMPLES</span></span>

### <span data-ttu-id="38855-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="38855-110">Example 1</span></span>
```
PS C:\> Get-AzReservationHistory -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="38855-111">Ottenere la cronologia delle revisioni della prenotazione specifica</span><span class="sxs-lookup"><span data-stu-id="38855-111">Get the revision history of the specific reservation</span></span>

## <span data-ttu-id="38855-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38855-112">PARAMETERS</span></span>

### <span data-ttu-id="38855-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38855-113">-DefaultProfile</span></span>
<span data-ttu-id="38855-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="38855-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38855-115">-Prenotazione</span><span class="sxs-lookup"><span data-stu-id="38855-115">-Reservation</span></span>
<span data-ttu-id="38855-116">Parametro per l'oggetto pipe `Reservation` per s</span><span class="sxs-lookup"><span data-stu-id="38855-116">Pipe object parameter for `Reservation`s</span></span>

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

### <span data-ttu-id="38855-117">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="38855-117">-ReservationId</span></span>
<span data-ttu-id="38855-118">ReservationId della `Reservation` cronologia di cui deve essere visualizzata la cronologia</span><span class="sxs-lookup"><span data-stu-id="38855-118">ReservationId of the `Reservation` of which history is to be shown</span></span>

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

### <span data-ttu-id="38855-119">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="38855-119">-ReservationOrderId</span></span>
<span data-ttu-id="38855-120">ReservationOrderId per `ReservationOrder` l'elemento che contiene l'elemento `Reservation`</span><span class="sxs-lookup"><span data-stu-id="38855-120">ReservationOrderId for the `ReservationOrder` that contains the `Reservation`</span></span>

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

### <span data-ttu-id="38855-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38855-121">CommonParameters</span></span>
<span data-ttu-id="38855-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38855-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38855-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="38855-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38855-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="38855-124">INPUTS</span></span>

### <span data-ttu-id="38855-125">System.Guid</span><span class="sxs-lookup"><span data-stu-id="38855-125">System.Guid</span></span>

### <span data-ttu-id="38855-126">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="38855-126">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="38855-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="38855-127">OUTPUTS</span></span>

### <span data-ttu-id="38855-128">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="38855-128">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

## <span data-ttu-id="38855-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="38855-129">NOTES</span></span>

## <span data-ttu-id="38855-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="38855-130">RELATED LINKS</span></span>
