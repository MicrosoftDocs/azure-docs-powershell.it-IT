---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationcatalog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationCatalog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationCatalog.md
ms.openlocfilehash: 4714b97773583197807d6ca54152ee25ab520909
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514159"
---
# <span data-ttu-id="e9c06-101">Get-AzureRmReservationCatalog</span><span class="sxs-lookup"><span data-stu-id="e9c06-101">Get-AzureRmReservationCatalog</span></span>

## <span data-ttu-id="e9c06-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e9c06-102">SYNOPSIS</span></span>
<span data-ttu-id="e9c06-103">Ottenere il catalogo della prenotazione disponibile</span><span class="sxs-lookup"><span data-stu-id="e9c06-103">Get the catalog of available reservation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9c06-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e9c06-104">SYNTAX</span></span>

```
Get-AzureRmReservationCatalog [-SubscriptionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="e9c06-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e9c06-105">DESCRIPTION</span></span>
<span data-ttu-id="e9c06-106">Ottenere le aree geografiche e le SKU disponibili per l'acquisto di istanze riservate per l'abbonamento Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="e9c06-106">Get the regions and skus that are available for Reserved Instance purchase for the specified Azure subscription.</span></span>

## <span data-ttu-id="e9c06-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e9c06-107">EXAMPLES</span></span>

### <span data-ttu-id="e9c06-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e9c06-108">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationCatalog
```

<span data-ttu-id="e9c06-109">Ottenere il catalogo per l'abbonamento predefinito</span><span class="sxs-lookup"><span data-stu-id="e9c06-109">Get the catalog for the default subscription</span></span>

### <span data-ttu-id="e9c06-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e9c06-110">Example 2</span></span>
```
PS C:\> Get-AzureRmReservationCatalog -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="e9c06-111">Ottenere il catalogo per l'abbonamento specificato</span><span class="sxs-lookup"><span data-stu-id="e9c06-111">Get the catalog for the specified subscription</span></span>

## <span data-ttu-id="e9c06-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e9c06-112">PARAMETERS</span></span>

### <span data-ttu-id="e9c06-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e9c06-113">-SubscriptionId</span></span>
<span data-ttu-id="e9c06-114">ID dell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="e9c06-114">Id of the subscription</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9c06-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9c06-115">CommonParameters</span></span>
<span data-ttu-id="e9c06-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9c06-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9c06-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9c06-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9c06-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e9c06-118">INPUTS</span></span>

### <span data-ttu-id="e9c06-119">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e9c06-119">None</span></span>

## <span data-ttu-id="e9c06-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e9c06-120">OUTPUTS</span></span>

### <span data-ttu-id="e9c06-121">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. reservations. Models. PSCatalog, Microsoft. Azure. Commands. reservations, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e9c06-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Reservations.Models.PSCatalog, Microsoft.Azure.Commands.Reservations, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e9c06-122">Note</span><span class="sxs-lookup"><span data-stu-id="e9c06-122">NOTES</span></span>

## <span data-ttu-id="e9c06-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e9c06-123">RELATED LINKS</span></span>

