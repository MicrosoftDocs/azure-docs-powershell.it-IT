---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/get-azreservationorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
ms.openlocfilehash: 1878237544cc1b44b5e47814f455638c168e2412
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000270"
---
# <span data-ttu-id="3bb58-101">Get-AzReservationOrder</span><span class="sxs-lookup"><span data-stu-id="3bb58-101">Get-AzReservationOrder</span></span>

## <span data-ttu-id="3bb58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3bb58-102">SYNOPSIS</span></span>
<span data-ttu-id="3bb58-103">Ottieni `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="3bb58-103">Get `ReservationOrder`</span></span>

## <span data-ttu-id="3bb58-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3bb58-104">SYNTAX</span></span>

```
Get-AzReservationOrder [-ReservationOrderId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3bb58-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3bb58-105">DESCRIPTION</span></span>
<span data-ttu-id="3bb58-106">Elenco di tutti `ReservationOrder` i siti a cui l'utente ha accesso nel tenant corrente.</span><span class="sxs-lookup"><span data-stu-id="3bb58-106">List of all the `ReservationOrder`s that the user has access to in the current tenant.</span></span> <span data-ttu-id="3bb58-107">Se è impostato il parametro ReservationOrderId, ottenere lo specifico valore di ReservationOrder.</span><span class="sxs-lookup"><span data-stu-id="3bb58-107">If ReservationOrderId parameter is set, get that specific ReservationOrder.</span></span>

## <span data-ttu-id="3bb58-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3bb58-108">EXAMPLES</span></span>

### <span data-ttu-id="3bb58-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3bb58-109">Example 1</span></span>
```
PS C:\> Get-AzReservationOrder
```

<span data-ttu-id="3bb58-110">Elencare `ReservationOrder` tutti gli elementi a cui l'utente ha accesso nel tenant corrente</span><span class="sxs-lookup"><span data-stu-id="3bb58-110">List all `ReservationOrder` that the user has access to in the current tenant</span></span>

### <span data-ttu-id="3bb58-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3bb58-111">Example 2</span></span>
```
PS C:\> Get-AzReservationOrder -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="3bb58-112">Ottenere `ReservationOrder` con il valore di ReservationOrderId specificato</span><span class="sxs-lookup"><span data-stu-id="3bb58-112">Get `ReservationOrder` with the specified ReservationOrderId</span></span>

## <span data-ttu-id="3bb58-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3bb58-113">PARAMETERS</span></span>

### <span data-ttu-id="3bb58-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bb58-114">-DefaultProfile</span></span>
<span data-ttu-id="3bb58-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3bb58-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bb58-116">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="3bb58-116">-ReservationOrderId</span></span>
<span data-ttu-id="3bb58-117">ID dello specifico Ordine di prenotazione che l'utente vuole visualizzare</span><span class="sxs-lookup"><span data-stu-id="3bb58-117">Id of the specific ReservationOrder that user wants to see</span></span>

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

### <span data-ttu-id="3bb58-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bb58-118">CommonParameters</span></span>
<span data-ttu-id="3bb58-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bb58-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bb58-120">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3bb58-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bb58-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="3bb58-121">INPUTS</span></span>

### <span data-ttu-id="3bb58-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3bb58-122">None</span></span>

## <span data-ttu-id="3bb58-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3bb58-123">OUTPUTS</span></span>

### <span data-ttu-id="3bb58-124">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="3bb58-124">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

### <span data-ttu-id="3bb58-125">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="3bb58-125">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

## <span data-ttu-id="3bb58-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="3bb58-126">NOTES</span></span>

## <span data-ttu-id="3bb58-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3bb58-127">RELATED LINKS</span></span>
