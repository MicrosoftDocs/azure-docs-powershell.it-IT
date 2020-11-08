---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: edf7b9135bc1f2d614f9fc516acadbc31821c45e
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030371"
---
# <span data-ttu-id="b4bc1-101">Get-AzsDelegatedProviderManagedOffer</span><span class="sxs-lookup"><span data-stu-id="b4bc1-101">Get-AzsDelegatedProviderManagedOffer</span></span>

## <span data-ttu-id="b4bc1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b4bc1-102">SYNOPSIS</span></span>
<span data-ttu-id="b4bc1-103">Ottenere l'elenco dei provider delegati offerti.</span><span class="sxs-lookup"><span data-stu-id="b4bc1-103">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="b4bc1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b4bc1-104">SYNTAX</span></span>

### <span data-ttu-id="b4bc1-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b4bc1-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderId <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="b4bc1-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="b4bc1-106">Get</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderId <String> -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="b4bc1-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4bc1-107">ResourceId</span></span>
```
Get-AzsDelegatedProviderManagedOffer -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="b4bc1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b4bc1-108">DESCRIPTION</span></span>
<span data-ttu-id="b4bc1-109">Ottenere l'elenco dei provider delegati offerti.</span><span class="sxs-lookup"><span data-stu-id="b4bc1-109">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="b4bc1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b4bc1-110">EXAMPLES</span></span>

### <span data-ttu-id="b4bc1-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b4bc1-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProvider "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="b4bc1-112">Ottenere l'elenco dei provider delegati offerti.</span><span class="sxs-lookup"><span data-stu-id="b4bc1-112">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="b4bc1-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b4bc1-113">PARAMETERS</span></span>

### <span data-ttu-id="b4bc1-114">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="b4bc1-114">-DelegatedProviderId</span></span>
<span data-ttu-id="b4bc1-115">Identificatore DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="b4bc1-115">DelegatedProvider identifier.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: DelegatedProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4bc1-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="b4bc1-116">-Name</span></span>
<span data-ttu-id="b4bc1-117">Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="b4bc1-117">Name of an offer.</span></span>

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

### <span data-ttu-id="b4bc1-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4bc1-118">-ResourceId</span></span>
<span data-ttu-id="b4bc1-119">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="b4bc1-119">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4bc1-120">-Skip</span><span class="sxs-lookup"><span data-stu-id="b4bc1-120">-Skip</span></span>
<span data-ttu-id="b4bc1-121">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="b4bc1-121">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4bc1-122">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="b4bc1-122">-Top</span></span>
<span data-ttu-id="b4bc1-123">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="b4bc1-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="b4bc1-124">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="b4bc1-124">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4bc1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4bc1-125">CommonParameters</span></span>
<span data-ttu-id="b4bc1-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4bc1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4bc1-127">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4bc1-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4bc1-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b4bc1-128">INPUTS</span></span>

## <span data-ttu-id="b4bc1-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b4bc1-129">OUTPUTS</span></span>

### <span data-ttu-id="b4bc1-130">Microsoft. AzureStack. Management. subscriptions. admin. Models. DelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="b4bc1-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.DelegatedProviderOffer</span></span>

## <span data-ttu-id="b4bc1-131">Note</span><span class="sxs-lookup"><span data-stu-id="b4bc1-131">NOTES</span></span>

## <span data-ttu-id="b4bc1-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b4bc1-132">RELATED LINKS</span></span>

