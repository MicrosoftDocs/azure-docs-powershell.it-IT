---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 66e8e58b84c0ea1ca0e71999dad56bcf464d6a0f
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859806"
---
# <span data-ttu-id="7b60c-101">Get-AzsDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="7b60c-101">Get-AzsDelegatedProviderOffer</span></span>

## <span data-ttu-id="7b60c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7b60c-102">SYNOPSIS</span></span>
<span data-ttu-id="7b60c-103">Ottenere l'elenco delle offerte per il provider delegato specificato.</span><span class="sxs-lookup"><span data-stu-id="7b60c-103">Get the list of offers for the specified delegated provider.</span></span>

## <span data-ttu-id="7b60c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7b60c-104">SYNTAX</span></span>

### <span data-ttu-id="7b60c-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7b60c-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="7b60c-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="7b60c-106">Get</span></span>
```
Get-AzsDelegatedProviderOffer -OfferName <String> -DelegatedProviderId <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="7b60c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7b60c-107">DESCRIPTION</span></span>
<span data-ttu-id="7b60c-108">Ottenere l'elenco delle offerte per il provider delegato specificato.</span><span class="sxs-lookup"><span data-stu-id="7b60c-108">Get the list of offers for the specified delegated provider.</span></span>

## <span data-ttu-id="7b60c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7b60c-109">EXAMPLES</span></span>

### <span data-ttu-id="7b60c-110">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="7b60c-110">EXAMPLE 1</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId 4b763321-23f5-4a45-a44d-9ccfdd705a3d | fl
```

<span data-ttu-id="7b60c-111">Ottenere l'elenco delle offerte per il provider delegato specificato.</span><span class="sxs-lookup"><span data-stu-id="7b60c-111">Get the list of offers for the specified delegated provider.</span></span>

## <span data-ttu-id="7b60c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7b60c-112">PARAMETERS</span></span>

### <span data-ttu-id="7b60c-113">-Offername</span><span class="sxs-lookup"><span data-stu-id="7b60c-113">-OfferName</span></span>
<span data-ttu-id="7b60c-114">Nome dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="7b60c-114">Name of the offer.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b60c-115">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="7b60c-115">-DelegatedProviderId</span></span>
<span data-ttu-id="7b60c-116">ID del provider delegato.</span><span class="sxs-lookup"><span data-stu-id="7b60c-116">Id of the delegated provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b60c-117">-Skip</span><span class="sxs-lookup"><span data-stu-id="7b60c-117">-Skip</span></span>
<span data-ttu-id="7b60c-118">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="7b60c-118">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b60c-119">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="7b60c-119">-Top</span></span>
<span data-ttu-id="7b60c-120">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="7b60c-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="7b60c-121">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="7b60c-121">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b60c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b60c-122">CommonParameters</span></span>
<span data-ttu-id="7b60c-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b60c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b60c-124">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b60c-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b60c-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7b60c-125">INPUTS</span></span>

## <span data-ttu-id="7b60c-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7b60c-126">OUTPUTS</span></span>

### <span data-ttu-id="7b60c-127">Microsoft. AzureStack. Management. Subscription. Models. offer</span><span class="sxs-lookup"><span data-stu-id="7b60c-127">Microsoft.AzureStack.Management.Subscription.Models.Offer</span></span>

## <span data-ttu-id="7b60c-128">Note</span><span class="sxs-lookup"><span data-stu-id="7b60c-128">NOTES</span></span>

## <span data-ttu-id="7b60c-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7b60c-129">RELATED LINKS</span></span>
