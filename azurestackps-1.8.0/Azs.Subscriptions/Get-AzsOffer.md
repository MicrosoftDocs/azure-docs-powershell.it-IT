---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 77d6a4861dbdb93dff2d5511faeceac30e3f9cf8
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "93859174"
---
# <span data-ttu-id="aeb09-101">Get-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="aeb09-101">Get-AzsOffer</span></span>

## <span data-ttu-id="aeb09-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aeb09-102">SYNOPSIS</span></span>
<span data-ttu-id="aeb09-103">Ottenere l'elenco delle offerte pubbliche.</span><span class="sxs-lookup"><span data-stu-id="aeb09-103">Get the list of public offers.</span></span>

## <span data-ttu-id="aeb09-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aeb09-104">SYNTAX</span></span>

```
Get-AzsOffer [[-Skip] <Int32>] [[-Top] <Int32>] [[-Provider] <String>] [<CommonParameters>]
```

## <span data-ttu-id="aeb09-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aeb09-105">DESCRIPTION</span></span>
<span data-ttu-id="aeb09-106">Ottenere l'elenco delle offerte pubbliche.</span><span class="sxs-lookup"><span data-stu-id="aeb09-106">Get the list of public offers.</span></span>

## <span data-ttu-id="aeb09-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aeb09-107">EXAMPLES</span></span>

### <span data-ttu-id="aeb09-108">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="aeb09-108">EXAMPLE 1</span></span>
```
Get-AzsOffer | fl
```

<span data-ttu-id="aeb09-109">Ottenere l'elenco delle offerte pubbliche.</span><span class="sxs-lookup"><span data-stu-id="aeb09-109">Get the list of public offers.</span></span>

## <span data-ttu-id="aeb09-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aeb09-110">PARAMETERS</span></span>

### <span data-ttu-id="aeb09-111">-Skip</span><span class="sxs-lookup"><span data-stu-id="aeb09-111">-Skip</span></span>
<span data-ttu-id="aeb09-112">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="aeb09-112">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aeb09-113">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="aeb09-113">-Top</span></span>
<span data-ttu-id="aeb09-114">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="aeb09-114">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="aeb09-115">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="aeb09-115">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aeb09-116">-Provider</span><span class="sxs-lookup"><span data-stu-id="aeb09-116">-Provider</span></span>
<span data-ttu-id="aeb09-117">Parametro facoltativo per specificare il nome del provider delegato.</span><span class="sxs-lookup"><span data-stu-id="aeb09-117">Optional parameter to specify the delegated provider name.</span></span> <span data-ttu-id="aeb09-118">Questo parametro non viene usato e sarà deprecato in futuro.</span><span class="sxs-lookup"><span data-stu-id="aeb09-118">This parameter is not being used and will be deprecated in future.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aeb09-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aeb09-119">CommonParameters</span></span>
<span data-ttu-id="aeb09-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aeb09-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aeb09-121">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aeb09-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aeb09-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aeb09-122">INPUTS</span></span>

## <span data-ttu-id="aeb09-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aeb09-123">OUTPUTS</span></span>

### <span data-ttu-id="aeb09-124">Microsoft. AzureStack. Management. Subscription. Models. offer</span><span class="sxs-lookup"><span data-stu-id="aeb09-124">Microsoft.AzureStack.Management.Subscription.Models.Offer</span></span>

## <span data-ttu-id="aeb09-125">Note</span><span class="sxs-lookup"><span data-stu-id="aeb09-125">NOTES</span></span>

## <span data-ttu-id="aeb09-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aeb09-126">RELATED LINKS</span></span>
