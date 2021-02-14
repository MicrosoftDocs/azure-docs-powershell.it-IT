---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationorderid
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
ms.openlocfilehash: 31cccc3c2bde38593bcc1b54d86940f07716a0db
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183734"
---
# <span data-ttu-id="cb9e9-101">Get-AzReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="cb9e9-101">Get-AzReservationOrderId</span></span>

## <span data-ttu-id="cb9e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb9e9-102">SYNOPSIS</span></span>
<span data-ttu-id="cb9e9-103">Ottieni l'elenco degli `ReservationOrder` ID applicabili.</span><span class="sxs-lookup"><span data-stu-id="cb9e9-103">Get list of applicable `ReservationOrder` Ids.</span></span>

## <span data-ttu-id="cb9e9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cb9e9-104">SYNTAX</span></span>

```
Get-AzReservationOrderId [-SubscriptionId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cb9e9-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cb9e9-105">DESCRIPTION</span></span>
<span data-ttu-id="cb9e9-106">Ottenere gli ID delle s `ReservationOrder` applicabili che possono essere applicati all'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="cb9e9-106">Get Ids of applicable `ReservationOrder`s that can be applied to this subscription.</span></span>

## <span data-ttu-id="cb9e9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cb9e9-107">EXAMPLES</span></span>

### <span data-ttu-id="cb9e9-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cb9e9-108">Example 1</span></span>
```
PS C:\> Get-AzReservationOrderId
```

<span data-ttu-id="cb9e9-109">Essere applicati `ReservationOrder` all'abbonamento predefinito</span><span class="sxs-lookup"><span data-stu-id="cb9e9-109">Get applied `ReservationOrder` for default subscription</span></span>

### <span data-ttu-id="cb9e9-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="cb9e9-110">Example 2</span></span>
```
PS C:\> Get-AzReservationOrderId -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="cb9e9-111">Viene applicata `ReservationOrder` per l'abbonamento specificato</span><span class="sxs-lookup"><span data-stu-id="cb9e9-111">Get applied `ReservationOrder` for specified subscription</span></span>

## <span data-ttu-id="cb9e9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb9e9-112">PARAMETERS</span></span>

### <span data-ttu-id="cb9e9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb9e9-113">-DefaultProfile</span></span>
<span data-ttu-id="cb9e9-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cb9e9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb9e9-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cb9e9-115">-SubscriptionId</span></span>
<span data-ttu-id="cb9e9-116">ID della sottoscrizione per ottenere le sottoscrizioni `ReservationOrder` applicate</span><span class="sxs-lookup"><span data-stu-id="cb9e9-116">Id of the subscription to get the applied `ReservationOrder`s</span></span>

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

### <span data-ttu-id="cb9e9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb9e9-117">CommonParameters</span></span>
<span data-ttu-id="cb9e9-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb9e9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb9e9-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cb9e9-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb9e9-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="cb9e9-120">INPUTS</span></span>

### <span data-ttu-id="cb9e9-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="cb9e9-121">None</span></span>

## <span data-ttu-id="cb9e9-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cb9e9-122">OUTPUTS</span></span>

### <span data-ttu-id="cb9e9-123">Microsoft.Azure.Management.Reservations.Models.AppliedReservations</span><span class="sxs-lookup"><span data-stu-id="cb9e9-123">Microsoft.Azure.Management.Reservations.Models.AppliedReservations</span></span>

## <span data-ttu-id="cb9e9-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="cb9e9-124">NOTES</span></span>

## <span data-ttu-id="cb9e9-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cb9e9-125">RELATED LINKS</span></span>
