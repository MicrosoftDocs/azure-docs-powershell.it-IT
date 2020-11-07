---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88c19285ee7188dab272eeab7a668f5f5dfe22a4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673782"
---
# <span data-ttu-id="a6f0c-101">Get-AzsDelegatedProvider</span><span class="sxs-lookup"><span data-stu-id="a6f0c-101">Get-AzsDelegatedProvider</span></span>

## <span data-ttu-id="a6f0c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a6f0c-102">SYNOPSIS</span></span>
<span data-ttu-id="a6f0c-103">Ottenere l'elenco di delegatedProviders.</span><span class="sxs-lookup"><span data-stu-id="a6f0c-103">Get the list of delegatedProviders.</span></span>

## <span data-ttu-id="a6f0c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a6f0c-104">SYNTAX</span></span>

### <span data-ttu-id="a6f0c-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a6f0c-105">List (Default)</span></span>
```
Get-AzsDelegatedProvider [<CommonParameters>]
```

### <span data-ttu-id="a6f0c-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="a6f0c-106">Get</span></span>
```
Get-AzsDelegatedProvider [-DelegatedProviderId] <Guid> [<CommonParameters>]
```

## <span data-ttu-id="a6f0c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a6f0c-107">DESCRIPTION</span></span>
<span data-ttu-id="a6f0c-108">Ottenere l'elenco di delegatedProviders.</span><span class="sxs-lookup"><span data-stu-id="a6f0c-108">Get the list of delegatedProviders.</span></span>

## <span data-ttu-id="a6f0c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a6f0c-109">EXAMPLES</span></span>

### <span data-ttu-id="a6f0c-110">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a6f0c-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDelegatedProvider
```

<span data-ttu-id="a6f0c-111">Ottenere un elenco di provider delegati.</span><span class="sxs-lookup"><span data-stu-id="a6f0c-111">Get a list of delegated providers.</span></span>

### <span data-ttu-id="a6f0c-112">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="a6f0c-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsDelegatedProvider -DelegatedProviderId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="a6f0c-113">Ottenere un provider delegato specifico.</span><span class="sxs-lookup"><span data-stu-id="a6f0c-113">Get the a specific delegated provider.</span></span>

## <span data-ttu-id="a6f0c-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a6f0c-114">PARAMETERS</span></span>

### <span data-ttu-id="a6f0c-115">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="a6f0c-115">-DelegatedProviderId</span></span>
<span data-ttu-id="a6f0c-116">Identificatore DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="a6f0c-116">DelegatedProvider identifier.</span></span>

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

### <span data-ttu-id="a6f0c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6f0c-117">CommonParameters</span></span>
<span data-ttu-id="a6f0c-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6f0c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6f0c-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6f0c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6f0c-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a6f0c-120">INPUTS</span></span>

## <span data-ttu-id="a6f0c-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a6f0c-121">OUTPUTS</span></span>

### <span data-ttu-id="a6f0c-122">Microsoft. AzureStack. Management. abbonamenti. admin. Models. Subscription</span><span class="sxs-lookup"><span data-stu-id="a6f0c-122">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="a6f0c-123">Note</span><span class="sxs-lookup"><span data-stu-id="a6f0c-123">NOTES</span></span>

## <span data-ttu-id="a6f0c-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a6f0c-124">RELATED LINKS</span></span>

