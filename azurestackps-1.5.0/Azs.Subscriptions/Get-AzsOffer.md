---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 885fef88b1042fb538c4e07b62410943063cb53d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491294"
---
# <span data-ttu-id="4e7a4-101">Get-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="4e7a4-101">Get-AzsOffer</span></span>

## <span data-ttu-id="4e7a4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4e7a4-102">SYNOPSIS</span></span>
<span data-ttu-id="4e7a4-103">Ottenere l'elenco delle offerte pubbliche.</span><span class="sxs-lookup"><span data-stu-id="4e7a4-103">Get the list of public offers.</span></span>

## <span data-ttu-id="4e7a4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4e7a4-104">SYNTAX</span></span>

```
Get-AzsOffer [[-Skip] <Int32>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="4e7a4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4e7a4-105">DESCRIPTION</span></span>
<span data-ttu-id="4e7a4-106">Ottenere l'elenco delle offerte pubbliche.</span><span class="sxs-lookup"><span data-stu-id="4e7a4-106">Get the list of public offers.</span></span>

## <span data-ttu-id="4e7a4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4e7a4-107">EXAMPLES</span></span>

### <span data-ttu-id="4e7a4-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="4e7a4-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOffer | fl
```

<span data-ttu-id="4e7a4-109">Ottenere l'elenco delle offerte pubbliche.</span><span class="sxs-lookup"><span data-stu-id="4e7a4-109">Get the list of public offers.</span></span>

## <span data-ttu-id="4e7a4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4e7a4-110">PARAMETERS</span></span>

### <span data-ttu-id="4e7a4-111">-Skip</span><span class="sxs-lookup"><span data-stu-id="4e7a4-111">-Skip</span></span>
<span data-ttu-id="4e7a4-112">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="4e7a4-112">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="4e7a4-113">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="4e7a4-113">-Top</span></span>
<span data-ttu-id="4e7a4-114">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="4e7a4-114">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="4e7a4-115">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="4e7a4-115">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="4e7a4-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e7a4-116">CommonParameters</span></span>
<span data-ttu-id="4e7a4-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e7a4-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e7a4-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e7a4-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e7a4-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4e7a4-119">INPUTS</span></span>

## <span data-ttu-id="4e7a4-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4e7a4-120">OUTPUTS</span></span>

### <span data-ttu-id="4e7a4-121">Microsoft. AzureStack. Management. Subscription. Models. offer</span><span class="sxs-lookup"><span data-stu-id="4e7a4-121">Microsoft.AzureStack.Management.Subscription.Models.Offer</span></span>

## <span data-ttu-id="4e7a4-122">Note</span><span class="sxs-lookup"><span data-stu-id="4e7a4-122">NOTES</span></span>

## <span data-ttu-id="4e7a4-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4e7a4-123">RELATED LINKS</span></span>

