---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 57e195f1d42b4d1df26344133c10d7c0d40e1f8a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490822"
---
# <span data-ttu-id="59928-101">Get-AzsDelegatedProviderManagedOffer</span><span class="sxs-lookup"><span data-stu-id="59928-101">Get-AzsDelegatedProviderManagedOffer</span></span>

## <span data-ttu-id="59928-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="59928-102">SYNOPSIS</span></span>
<span data-ttu-id="59928-103">Ottenere l'elenco dei provider delegati offerti.</span><span class="sxs-lookup"><span data-stu-id="59928-103">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="59928-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="59928-104">SYNTAX</span></span>

### <span data-ttu-id="59928-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="59928-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderId <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="59928-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="59928-106">Get</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderId <String> -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="59928-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="59928-107">ResourceId</span></span>
```
Get-AzsDelegatedProviderManagedOffer -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="59928-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59928-108">DESCRIPTION</span></span>
<span data-ttu-id="59928-109">Ottenere l'elenco dei provider delegati offerti.</span><span class="sxs-lookup"><span data-stu-id="59928-109">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="59928-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="59928-110">EXAMPLES</span></span>

### <span data-ttu-id="59928-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="59928-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProvider "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="59928-112">Ottenere l'elenco dei provider delegati offerti.</span><span class="sxs-lookup"><span data-stu-id="59928-112">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="59928-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="59928-113">PARAMETERS</span></span>

### <span data-ttu-id="59928-114">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="59928-114">-DelegatedProviderId</span></span>
<span data-ttu-id="59928-115">Identificatore DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="59928-115">DelegatedProvider identifier.</span></span>

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

### <span data-ttu-id="59928-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="59928-116">-Name</span></span>
<span data-ttu-id="59928-117">Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="59928-117">Name of an offer.</span></span>

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

### <span data-ttu-id="59928-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59928-118">-ResourceId</span></span>
<span data-ttu-id="59928-119">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="59928-119">The resource id.</span></span>

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

### <span data-ttu-id="59928-120">-Skip</span><span class="sxs-lookup"><span data-stu-id="59928-120">-Skip</span></span>
<span data-ttu-id="59928-121">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="59928-121">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="59928-122">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="59928-122">-Top</span></span>
<span data-ttu-id="59928-123">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="59928-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="59928-124">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="59928-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="59928-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59928-125">CommonParameters</span></span>
<span data-ttu-id="59928-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59928-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59928-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59928-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59928-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="59928-128">INPUTS</span></span>

## <span data-ttu-id="59928-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="59928-129">OUTPUTS</span></span>

### <span data-ttu-id="59928-130">Microsoft. AzureStack. Management. subscriptions. admin. Models. DelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="59928-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.DelegatedProviderOffer</span></span>

## <span data-ttu-id="59928-131">Note</span><span class="sxs-lookup"><span data-stu-id="59928-131">NOTES</span></span>

## <span data-ttu-id="59928-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="59928-132">RELATED LINKS</span></span>

