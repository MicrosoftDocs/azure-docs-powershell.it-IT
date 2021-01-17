---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationorderid
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
ms.openlocfilehash: 31cccc3c2bde38593bcc1b54d86940f07716a0db
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377985"
---
# <span data-ttu-id="83dc8-101">Get-AzReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="83dc8-101">Get-AzReservationOrderId</span></span>

## <span data-ttu-id="83dc8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="83dc8-102">SYNOPSIS</span></span>
<span data-ttu-id="83dc8-103">Ottenere l'elenco degli `ReservationOrder` ID applicabili.</span><span class="sxs-lookup"><span data-stu-id="83dc8-103">Get list of applicable `ReservationOrder` Ids.</span></span>

## <span data-ttu-id="83dc8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="83dc8-104">SYNTAX</span></span>

```
Get-AzReservationOrderId [-SubscriptionId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="83dc8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="83dc8-105">DESCRIPTION</span></span>
<span data-ttu-id="83dc8-106">Ottenere gli ID di `ReservationOrder` s applicabili che possono essere applicati a questo abbonamento.</span><span class="sxs-lookup"><span data-stu-id="83dc8-106">Get Ids of applicable `ReservationOrder`s that can be applied to this subscription.</span></span>

## <span data-ttu-id="83dc8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="83dc8-107">EXAMPLES</span></span>

### <span data-ttu-id="83dc8-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="83dc8-108">Example 1</span></span>
```
PS C:\> Get-AzReservationOrderId
```

<span data-ttu-id="83dc8-109">Ottenere l'applicazione `ReservationOrder` per l'abbonamento predefinito</span><span class="sxs-lookup"><span data-stu-id="83dc8-109">Get applied `ReservationOrder` for default subscription</span></span>

### <span data-ttu-id="83dc8-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="83dc8-110">Example 2</span></span>
```
PS C:\> Get-AzReservationOrderId -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="83dc8-111">Ottenere l'applicazione `ReservationOrder` per l'abbonamento specificato</span><span class="sxs-lookup"><span data-stu-id="83dc8-111">Get applied `ReservationOrder` for specified subscription</span></span>

## <span data-ttu-id="83dc8-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="83dc8-112">PARAMETERS</span></span>

### <span data-ttu-id="83dc8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83dc8-113">-DefaultProfile</span></span>
<span data-ttu-id="83dc8-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="83dc8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83dc8-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="83dc8-115">-SubscriptionId</span></span>
<span data-ttu-id="83dc8-116">ID dell'abbonamento per ottenere la s applicata `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="83dc8-116">Id of the subscription to get the applied `ReservationOrder`s</span></span>

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

### <span data-ttu-id="83dc8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83dc8-117">CommonParameters</span></span>
<span data-ttu-id="83dc8-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83dc8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83dc8-119">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83dc8-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83dc8-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="83dc8-120">INPUTS</span></span>

### <span data-ttu-id="83dc8-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="83dc8-121">None</span></span>

## <span data-ttu-id="83dc8-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="83dc8-122">OUTPUTS</span></span>

### <span data-ttu-id="83dc8-123">Microsoft. Azure. Management. reservations. Models. AppliedReservations</span><span class="sxs-lookup"><span data-stu-id="83dc8-123">Microsoft.Azure.Management.Reservations.Models.AppliedReservations</span></span>

## <span data-ttu-id="83dc8-124">Note</span><span class="sxs-lookup"><span data-stu-id="83dc8-124">NOTES</span></span>

## <span data-ttu-id="83dc8-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="83dc8-125">RELATED LINKS</span></span>
