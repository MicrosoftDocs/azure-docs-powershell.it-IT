---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
ms.openlocfilehash: 15faf94ae7e0afac7200423dcd36d8edf2964c21
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201918"
---
# <span data-ttu-id="f0fbc-101">Get-AzReservationOrder</span><span class="sxs-lookup"><span data-stu-id="f0fbc-101">Get-AzReservationOrder</span></span>

## <span data-ttu-id="f0fbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0fbc-102">SYNOPSIS</span></span>
<span data-ttu-id="f0fbc-103">Ottieni `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="f0fbc-103">Get `ReservationOrder`</span></span>

## <span data-ttu-id="f0fbc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f0fbc-104">SYNTAX</span></span>

```
Get-AzReservationOrder [-ReservationOrderId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f0fbc-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f0fbc-105">DESCRIPTION</span></span>
<span data-ttu-id="f0fbc-106">Elenco di tutti `ReservationOrder` i siti a cui l'utente ha accesso nel tenant corrente.</span><span class="sxs-lookup"><span data-stu-id="f0fbc-106">List of all the `ReservationOrder`s that the user has access to in the current tenant.</span></span> <span data-ttu-id="f0fbc-107">Se il parametro ReservationOrderId è impostato, ottenere lo specifico valore di ReservationOrder.</span><span class="sxs-lookup"><span data-stu-id="f0fbc-107">If ReservationOrderId parameter is set, get that specific ReservationOrder.</span></span>

## <span data-ttu-id="f0fbc-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f0fbc-108">EXAMPLES</span></span>

### <span data-ttu-id="f0fbc-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f0fbc-109">Example 1</span></span>
```
PS C:\> Get-AzReservationOrder
```

<span data-ttu-id="f0fbc-110">Elencare `ReservationOrder` tutti gli elementi a cui l'utente ha accesso nel tenant corrente</span><span class="sxs-lookup"><span data-stu-id="f0fbc-110">List all `ReservationOrder` that the user has access to in the current tenant</span></span>

### <span data-ttu-id="f0fbc-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f0fbc-111">Example 2</span></span>
```
PS C:\> Get-AzReservationOrder -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="f0fbc-112">Ottenere `ReservationOrder` con il valore di ReservationOrderId specificato</span><span class="sxs-lookup"><span data-stu-id="f0fbc-112">Get `ReservationOrder` with the specified ReservationOrderId</span></span>

## <span data-ttu-id="f0fbc-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0fbc-113">PARAMETERS</span></span>

### <span data-ttu-id="f0fbc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0fbc-114">-DefaultProfile</span></span>
<span data-ttu-id="f0fbc-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f0fbc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0fbc-116">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="f0fbc-116">-ReservationOrderId</span></span>
<span data-ttu-id="f0fbc-117">ID dello specifico Ordine di prenotazione che l'utente vuole visualizzare</span><span class="sxs-lookup"><span data-stu-id="f0fbc-117">Id of the specific ReservationOrder that user wants to see</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0fbc-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0fbc-118">CommonParameters</span></span>
<span data-ttu-id="f0fbc-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0fbc-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0fbc-120">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f0fbc-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0fbc-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="f0fbc-121">INPUTS</span></span>

### <span data-ttu-id="f0fbc-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f0fbc-122">None</span></span>

## <span data-ttu-id="f0fbc-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f0fbc-123">OUTPUTS</span></span>

### <span data-ttu-id="f0fbc-124">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="f0fbc-124">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

### <span data-ttu-id="f0fbc-125">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="f0fbc-125">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

## <span data-ttu-id="f0fbc-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="f0fbc-126">NOTES</span></span>

## <span data-ttu-id="f0fbc-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f0fbc-127">RELATED LINKS</span></span>
