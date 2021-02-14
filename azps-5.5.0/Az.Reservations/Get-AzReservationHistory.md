---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationHistory.md
ms.openlocfilehash: cfc7ab08904f007f874e1b45fd6d27a5712abee9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183735"
---
# <span data-ttu-id="3d4db-101">Get-AzReservationHistory</span><span class="sxs-lookup"><span data-stu-id="3d4db-101">Get-AzReservationHistory</span></span>

## <span data-ttu-id="3d4db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d4db-102">SYNOPSIS</span></span>
<span data-ttu-id="3d4db-103">Ottenere la `Reservation` cronologia delle revisioni.</span><span class="sxs-lookup"><span data-stu-id="3d4db-103">Get `Reservation` revision history.</span></span>

## <span data-ttu-id="3d4db-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3d4db-104">SYNTAX</span></span>

### <span data-ttu-id="3d4db-105">CommandLine (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3d4db-105">CommandLine (Default)</span></span>
```
Get-AzReservationHistory -ReservationOrderId <Guid> -ReservationId <Guid>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d4db-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="3d4db-106">PipeObject</span></span>
```
Get-AzReservationHistory -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3d4db-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3d4db-107">DESCRIPTION</span></span>
<span data-ttu-id="3d4db-108">Elenco di tutte le revisioni per `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="3d4db-108">List of all the revisions for the `Reservation`.</span></span>

## <span data-ttu-id="3d4db-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3d4db-109">EXAMPLES</span></span>

### <span data-ttu-id="3d4db-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3d4db-110">Example 1</span></span>
```
PS C:\> Get-AzReservationHistory -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="3d4db-111">Ottenere la cronologia delle revisioni della prenotazione specifica</span><span class="sxs-lookup"><span data-stu-id="3d4db-111">Get the revision history of the specific reservation</span></span>

## <span data-ttu-id="3d4db-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d4db-112">PARAMETERS</span></span>

### <span data-ttu-id="3d4db-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d4db-113">-DefaultProfile</span></span>
<span data-ttu-id="3d4db-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3d4db-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d4db-115">-Prenotazione</span><span class="sxs-lookup"><span data-stu-id="3d4db-115">-Reservation</span></span>
<span data-ttu-id="3d4db-116">Parametro per l'oggetto pipe `Reservation` per s</span><span class="sxs-lookup"><span data-stu-id="3d4db-116">Pipe object parameter for `Reservation`s</span></span>

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

### <span data-ttu-id="3d4db-117">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="3d4db-117">-ReservationId</span></span>
<span data-ttu-id="3d4db-118">ReservationId della `Reservation` cronologia di cui deve essere visualizzata la cronologia</span><span class="sxs-lookup"><span data-stu-id="3d4db-118">ReservationId of the `Reservation` of which history is to be shown</span></span>

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

### <span data-ttu-id="3d4db-119">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="3d4db-119">-ReservationOrderId</span></span>
<span data-ttu-id="3d4db-120">ReservationOrderId per `ReservationOrder` l'elemento che contiene l'elemento `Reservation`</span><span class="sxs-lookup"><span data-stu-id="3d4db-120">ReservationOrderId for the `ReservationOrder` that contains the `Reservation`</span></span>

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

### <span data-ttu-id="3d4db-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d4db-121">CommonParameters</span></span>
<span data-ttu-id="3d4db-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d4db-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d4db-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3d4db-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d4db-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="3d4db-124">INPUTS</span></span>

### <span data-ttu-id="3d4db-125">System.Guid</span><span class="sxs-lookup"><span data-stu-id="3d4db-125">System.Guid</span></span>

### <span data-ttu-id="3d4db-126">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="3d4db-126">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="3d4db-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3d4db-127">OUTPUTS</span></span>

### <span data-ttu-id="3d4db-128">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="3d4db-128">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

## <span data-ttu-id="3d4db-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="3d4db-129">NOTES</span></span>

## <span data-ttu-id="3d4db-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3d4db-130">RELATED LINKS</span></span>
