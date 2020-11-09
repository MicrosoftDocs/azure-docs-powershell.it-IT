---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
ms.openlocfilehash: 15faf94ae7e0afac7200423dcd36d8edf2964c21
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302545"
---
# <span data-ttu-id="fbab0-101">Get-AzReservationOrder</span><span class="sxs-lookup"><span data-stu-id="fbab0-101">Get-AzReservationOrder</span></span>

## <span data-ttu-id="fbab0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fbab0-102">SYNOPSIS</span></span>
<span data-ttu-id="fbab0-103">Ottieni `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="fbab0-103">Get `ReservationOrder`</span></span>

## <span data-ttu-id="fbab0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fbab0-104">SYNTAX</span></span>

```
Get-AzReservationOrder [-ReservationOrderId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fbab0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fbab0-105">DESCRIPTION</span></span>
<span data-ttu-id="fbab0-106">Elenco di tutte le `ReservationOrder` s a cui l'utente ha accesso nel tenant corrente.</span><span class="sxs-lookup"><span data-stu-id="fbab0-106">List of all the `ReservationOrder`s that the user has access to in the current tenant.</span></span> <span data-ttu-id="fbab0-107">Se il parametro ReservationOrderId è impostato, ottenere quello specifico ReservationOrder.</span><span class="sxs-lookup"><span data-stu-id="fbab0-107">If ReservationOrderId parameter is set, get that specific ReservationOrder.</span></span>

## <span data-ttu-id="fbab0-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fbab0-108">EXAMPLES</span></span>

### <span data-ttu-id="fbab0-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fbab0-109">Example 1</span></span>
```
PS C:\> Get-AzReservationOrder
```

<span data-ttu-id="fbab0-110">Elencare tutti `ReservationOrder` gli utenti a cui l'utente ha accesso nel tenant corrente</span><span class="sxs-lookup"><span data-stu-id="fbab0-110">List all `ReservationOrder` that the user has access to in the current tenant</span></span>

### <span data-ttu-id="fbab0-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="fbab0-111">Example 2</span></span>
```
PS C:\> Get-AzReservationOrder -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="fbab0-112">Ottenere `ReservationOrder` con il ReservationOrderId specificato</span><span class="sxs-lookup"><span data-stu-id="fbab0-112">Get `ReservationOrder` with the specified ReservationOrderId</span></span>

## <span data-ttu-id="fbab0-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fbab0-113">PARAMETERS</span></span>

### <span data-ttu-id="fbab0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbab0-114">-DefaultProfile</span></span>
<span data-ttu-id="fbab0-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fbab0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbab0-116">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="fbab0-116">-ReservationOrderId</span></span>
<span data-ttu-id="fbab0-117">ID dello specifico ReservationOrder che l'utente vuole vedere</span><span class="sxs-lookup"><span data-stu-id="fbab0-117">Id of the specific ReservationOrder that user wants to see</span></span>

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

### <span data-ttu-id="fbab0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbab0-118">CommonParameters</span></span>
<span data-ttu-id="fbab0-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbab0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbab0-120">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fbab0-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbab0-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fbab0-121">INPUTS</span></span>

### <span data-ttu-id="fbab0-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="fbab0-122">None</span></span>

## <span data-ttu-id="fbab0-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fbab0-123">OUTPUTS</span></span>

### <span data-ttu-id="fbab0-124">Microsoft. Azure. Commands. reservations. Models. PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="fbab0-124">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

### <span data-ttu-id="fbab0-125">Microsoft. Azure. Commands. reservations. Models. PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="fbab0-125">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

## <span data-ttu-id="fbab0-126">Note</span><span class="sxs-lookup"><span data-stu-id="fbab0-126">NOTES</span></span>

## <span data-ttu-id="fbab0-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fbab0-127">RELATED LINKS</span></span>
