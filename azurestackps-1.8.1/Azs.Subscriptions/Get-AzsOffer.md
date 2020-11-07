---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 77d6a4861dbdb93dff2d5511faeceac30e3f9cf8
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859790"
---
# <span data-ttu-id="516fc-101">Get-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="516fc-101">Get-AzsOffer</span></span>

## <span data-ttu-id="516fc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="516fc-102">SYNOPSIS</span></span>
<span data-ttu-id="516fc-103">Ottenere l'elenco delle offerte pubbliche.</span><span class="sxs-lookup"><span data-stu-id="516fc-103">Get the list of public offers.</span></span>

## <span data-ttu-id="516fc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="516fc-104">SYNTAX</span></span>

```
Get-AzsOffer [[-Skip] <Int32>] [[-Top] <Int32>] [[-Provider] <String>] [<CommonParameters>]
```

## <span data-ttu-id="516fc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="516fc-105">DESCRIPTION</span></span>
<span data-ttu-id="516fc-106">Ottenere l'elenco delle offerte pubbliche.</span><span class="sxs-lookup"><span data-stu-id="516fc-106">Get the list of public offers.</span></span>

## <span data-ttu-id="516fc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="516fc-107">EXAMPLES</span></span>

### <span data-ttu-id="516fc-108">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="516fc-108">EXAMPLE 1</span></span>
```
Get-AzsOffer | fl
```

<span data-ttu-id="516fc-109">Ottenere l'elenco delle offerte pubbliche.</span><span class="sxs-lookup"><span data-stu-id="516fc-109">Get the list of public offers.</span></span>

## <span data-ttu-id="516fc-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="516fc-110">PARAMETERS</span></span>

### <span data-ttu-id="516fc-111">-Skip</span><span class="sxs-lookup"><span data-stu-id="516fc-111">-Skip</span></span>
<span data-ttu-id="516fc-112">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="516fc-112">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="516fc-113">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="516fc-113">-Top</span></span>
<span data-ttu-id="516fc-114">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="516fc-114">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="516fc-115">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="516fc-115">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="516fc-116">-Provider</span><span class="sxs-lookup"><span data-stu-id="516fc-116">-Provider</span></span>
<span data-ttu-id="516fc-117">Parametro facoltativo per specificare il nome del provider delegato.</span><span class="sxs-lookup"><span data-stu-id="516fc-117">Optional parameter to specify the delegated provider name.</span></span> <span data-ttu-id="516fc-118">Questo parametro non viene usato e sarà deprecato in futuro.</span><span class="sxs-lookup"><span data-stu-id="516fc-118">This parameter is not being used and will be deprecated in future.</span></span>

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

### <span data-ttu-id="516fc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="516fc-119">CommonParameters</span></span>
<span data-ttu-id="516fc-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="516fc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="516fc-121">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="516fc-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="516fc-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="516fc-122">INPUTS</span></span>

## <span data-ttu-id="516fc-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="516fc-123">OUTPUTS</span></span>

### <span data-ttu-id="516fc-124">Microsoft. AzureStack. Management. Subscription. Models. offer</span><span class="sxs-lookup"><span data-stu-id="516fc-124">Microsoft.AzureStack.Management.Subscription.Models.Offer</span></span>

## <span data-ttu-id="516fc-125">Note</span><span class="sxs-lookup"><span data-stu-id="516fc-125">NOTES</span></span>

## <span data-ttu-id="516fc-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="516fc-126">RELATED LINKS</span></span>
