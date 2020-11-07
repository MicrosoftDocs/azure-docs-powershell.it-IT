---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: afc99afebed095da96d826918cc6912f197d1899
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "93859286"
---
# <span data-ttu-id="ef440-101">Get-AzsDelegatedProvider</span><span class="sxs-lookup"><span data-stu-id="ef440-101">Get-AzsDelegatedProvider</span></span>

## <span data-ttu-id="ef440-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ef440-102">SYNOPSIS</span></span>
<span data-ttu-id="ef440-103">Ottenere l'elenco di delegatedProviders.</span><span class="sxs-lookup"><span data-stu-id="ef440-103">Get the list of delegatedProviders.</span></span>

## <span data-ttu-id="ef440-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ef440-104">SYNTAX</span></span>

### <span data-ttu-id="ef440-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ef440-105">List (Default)</span></span>
```
Get-AzsDelegatedProvider [<CommonParameters>]
```

### <span data-ttu-id="ef440-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="ef440-106">Get</span></span>
```
Get-AzsDelegatedProvider [-DelegatedProviderId] <Guid> [<CommonParameters>]
```

## <span data-ttu-id="ef440-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ef440-107">DESCRIPTION</span></span>
<span data-ttu-id="ef440-108">Ottenere l'elenco di delegatedProviders.</span><span class="sxs-lookup"><span data-stu-id="ef440-108">Get the list of delegatedProviders.</span></span>

## <span data-ttu-id="ef440-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ef440-109">EXAMPLES</span></span>

### <span data-ttu-id="ef440-110">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ef440-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDelegatedProvider
```

<span data-ttu-id="ef440-111">Ottenere un elenco di provider delegati.</span><span class="sxs-lookup"><span data-stu-id="ef440-111">Get a list of delegated providers.</span></span>

### <span data-ttu-id="ef440-112">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="ef440-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsDelegatedProvider -DelegatedProviderId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="ef440-113">Ottenere un provider delegato specifico.</span><span class="sxs-lookup"><span data-stu-id="ef440-113">Get the a specific delegated provider.</span></span>

## <span data-ttu-id="ef440-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ef440-114">PARAMETERS</span></span>

### <span data-ttu-id="ef440-115">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="ef440-115">-DelegatedProviderId</span></span>
<span data-ttu-id="ef440-116">{{Fill DelegatedProviderId Description}}</span><span class="sxs-lookup"><span data-stu-id="ef440-116">{{Fill DelegatedProviderId Description}}</span></span>

```yaml
Type: Guid
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef440-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef440-117">CommonParameters</span></span>
<span data-ttu-id="ef440-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef440-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef440-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef440-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef440-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ef440-120">INPUTS</span></span>

## <span data-ttu-id="ef440-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ef440-121">OUTPUTS</span></span>

### <span data-ttu-id="ef440-122">Microsoft. AzureStack. Management. abbonamenti. admin. Models. Subscription</span><span class="sxs-lookup"><span data-stu-id="ef440-122">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="ef440-123">Note</span><span class="sxs-lookup"><span data-stu-id="ef440-123">NOTES</span></span>

## <span data-ttu-id="ef440-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ef440-124">RELATED LINKS</span></span>

