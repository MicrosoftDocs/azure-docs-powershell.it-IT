---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationorderid
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
ms.openlocfilehash: c969d24a894165e23628b91cda640f676ec3f3d4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677430"
---
# <span data-ttu-id="b0d7d-101">Get-AzReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="b0d7d-101">Get-AzReservationOrderId</span></span>

## <span data-ttu-id="b0d7d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b0d7d-102">SYNOPSIS</span></span>
<span data-ttu-id="b0d7d-103">Ottenere l'elenco degli `ReservationOrder` ID applicabili.</span><span class="sxs-lookup"><span data-stu-id="b0d7d-103">Get list of applicable `ReservationOrder` Ids.</span></span>

## <span data-ttu-id="b0d7d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b0d7d-104">SYNTAX</span></span>

```
Get-AzReservationOrderId [-SubscriptionId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b0d7d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b0d7d-105">DESCRIPTION</span></span>
<span data-ttu-id="b0d7d-106">Ottenere gli ID di `ReservationOrder` s applicabili che possono essere applicati a questo abbonamento.</span><span class="sxs-lookup"><span data-stu-id="b0d7d-106">Get Ids of applicable `ReservationOrder`s that can be applied to this subscription.</span></span>

## <span data-ttu-id="b0d7d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b0d7d-107">EXAMPLES</span></span>

### <span data-ttu-id="b0d7d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b0d7d-108">Example 1</span></span>
```
PS C:\> Get-AzReservationOrderId
```

<span data-ttu-id="b0d7d-109">Ottenere l'applicazione `ReservationOrder` per l'abbonamento predefinito</span><span class="sxs-lookup"><span data-stu-id="b0d7d-109">Get applied `ReservationOrder` for default subscription</span></span>

### <span data-ttu-id="b0d7d-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b0d7d-110">Example 2</span></span>
```
PS C:\> Get-AzReservationOrderId -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="b0d7d-111">Ottenere l'applicazione `ReservationOrder` per l'abbonamento specificato</span><span class="sxs-lookup"><span data-stu-id="b0d7d-111">Get applied `ReservationOrder` for specified subscription</span></span>

## <span data-ttu-id="b0d7d-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b0d7d-112">PARAMETERS</span></span>

### <span data-ttu-id="b0d7d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0d7d-113">-DefaultProfile</span></span>
<span data-ttu-id="b0d7d-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b0d7d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0d7d-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b0d7d-115">-SubscriptionId</span></span>
<span data-ttu-id="b0d7d-116">ID dell'abbonamento per ottenere la s applicata `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="b0d7d-116">Id of the subscription to get the applied `ReservationOrder`s</span></span>

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

### <span data-ttu-id="b0d7d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0d7d-117">CommonParameters</span></span>
<span data-ttu-id="b0d7d-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0d7d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0d7d-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0d7d-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0d7d-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b0d7d-120">INPUTS</span></span>

### <span data-ttu-id="b0d7d-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b0d7d-121">None</span></span>

## <span data-ttu-id="b0d7d-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b0d7d-122">OUTPUTS</span></span>

### <span data-ttu-id="b0d7d-123">Microsoft. Azure. Management. reservations. Models. AppliedReservations</span><span class="sxs-lookup"><span data-stu-id="b0d7d-123">Microsoft.Azure.Management.Reservations.Models.AppliedReservations</span></span>

## <span data-ttu-id="b0d7d-124">Note</span><span class="sxs-lookup"><span data-stu-id="b0d7d-124">NOTES</span></span>

## <span data-ttu-id="b0d7d-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b0d7d-125">RELATED LINKS</span></span>
