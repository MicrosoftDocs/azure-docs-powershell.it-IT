---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8034887f8b44bef5c3dd59f73186027af1a1e5eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491205"
---
# <span data-ttu-id="77710-101">Get-AzsDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="77710-101">Get-AzsDelegatedProviderOffer</span></span>

## <span data-ttu-id="77710-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="77710-102">SYNOPSIS</span></span>
<span data-ttu-id="77710-103">Ottenere l'elenco delle offerte per il provider delegato specificato.</span><span class="sxs-lookup"><span data-stu-id="77710-103">Get the list of offers for the specified delegated provider.</span></span>

## <span data-ttu-id="77710-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="77710-104">SYNTAX</span></span>

### <span data-ttu-id="77710-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="77710-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="77710-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="77710-106">Get</span></span>
```
Get-AzsDelegatedProviderOffer -Name <String> -DelegatedProviderId <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="77710-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="77710-107">DESCRIPTION</span></span>
<span data-ttu-id="77710-108">Ottenere l'elenco delle offerte per il provider delegato specificato.</span><span class="sxs-lookup"><span data-stu-id="77710-108">Get the list of offers for the specified delegated provider.</span></span>

## <span data-ttu-id="77710-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="77710-109">EXAMPLES</span></span>

### <span data-ttu-id="77710-110">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="77710-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId 4b763321-23f5-4a45-a44d-9ccfdd705a3d | fl
```

<span data-ttu-id="77710-111">Ottenere l'elenco delle offerte per il provider delegato specificato.</span><span class="sxs-lookup"><span data-stu-id="77710-111">Get the list of offers for the specified delegated provider.</span></span>

## <span data-ttu-id="77710-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="77710-112">PARAMETERS</span></span>

### <span data-ttu-id="77710-113">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="77710-113">-DelegatedProviderId</span></span>
<span data-ttu-id="77710-114">ID del provider delegato.</span><span class="sxs-lookup"><span data-stu-id="77710-114">Id of the delegated provider.</span></span>

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

### <span data-ttu-id="77710-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="77710-115">-Name</span></span>
<span data-ttu-id="77710-116">Nome dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="77710-116">Name of the offer.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: OfferName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77710-117">-Skip</span><span class="sxs-lookup"><span data-stu-id="77710-117">-Skip</span></span>
<span data-ttu-id="77710-118">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="77710-118">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="77710-119">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="77710-119">-Top</span></span>
<span data-ttu-id="77710-120">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="77710-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="77710-121">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="77710-121">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="77710-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77710-122">CommonParameters</span></span>
<span data-ttu-id="77710-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77710-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77710-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77710-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77710-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="77710-125">INPUTS</span></span>

## <span data-ttu-id="77710-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="77710-126">OUTPUTS</span></span>

### <span data-ttu-id="77710-127">Microsoft. AzureStack. Management. Subscription. Models. offer</span><span class="sxs-lookup"><span data-stu-id="77710-127">Microsoft.AzureStack.Management.Subscription.Models.Offer</span></span>

## <span data-ttu-id="77710-128">Note</span><span class="sxs-lookup"><span data-stu-id="77710-128">NOTES</span></span>

## <span data-ttu-id="77710-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="77710-129">RELATED LINKS</span></span>
