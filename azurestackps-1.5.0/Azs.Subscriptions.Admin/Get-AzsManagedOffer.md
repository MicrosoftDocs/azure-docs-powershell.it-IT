---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 66d8deb8551dfee98c15fcc5524c993c741bca0f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490821"
---
# <span data-ttu-id="d00b4-101">Get-AzsManagedOffer</span><span class="sxs-lookup"><span data-stu-id="d00b4-101">Get-AzsManagedOffer</span></span>

## <span data-ttu-id="d00b4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d00b4-102">SYNOPSIS</span></span>
<span data-ttu-id="d00b4-103">Ottenere l'elenco delle offerte come operatore.</span><span class="sxs-lookup"><span data-stu-id="d00b4-103">Get the list of offers as the operator.</span></span>

## <span data-ttu-id="d00b4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d00b4-104">SYNTAX</span></span>

### <span data-ttu-id="d00b4-105">ListAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d00b4-105">ListAll (Default)</span></span>
```
Get-AzsManagedOffer [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="d00b4-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="d00b4-106">Get</span></span>
```
Get-AzsManagedOffer -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="d00b4-107">Elenco</span><span class="sxs-lookup"><span data-stu-id="d00b4-107">List</span></span>
```
Get-AzsManagedOffer -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="d00b4-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d00b4-108">ResourceId</span></span>
```
Get-AzsManagedOffer -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="d00b4-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d00b4-109">DESCRIPTION</span></span>
<span data-ttu-id="d00b4-110">Ottenere l'elenco delle offerte.</span><span class="sxs-lookup"><span data-stu-id="d00b4-110">Get the list of offers.</span></span>

## <span data-ttu-id="d00b4-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d00b4-111">EXAMPLES</span></span>

### <span data-ttu-id="d00b4-112">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d00b4-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsManagedOffer -Name offer -ResourceGroupName offerrg
```

<span data-ttu-id="d00b4-113">Ottenere l'elenco delle offerte come operatore.</span><span class="sxs-lookup"><span data-stu-id="d00b4-113">Get the list of offers as the operator.</span></span>

## <span data-ttu-id="d00b4-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d00b4-114">PARAMETERS</span></span>

### <span data-ttu-id="d00b4-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="d00b4-115">-Name</span></span>
<span data-ttu-id="d00b4-116">Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="d00b4-116">Name of an offer.</span></span>

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

### <span data-ttu-id="d00b4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d00b4-117">-ResourceGroupName</span></span>
<span data-ttu-id="d00b4-118">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="d00b4-118">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d00b4-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d00b4-119">-ResourceId</span></span>
<span data-ttu-id="d00b4-120">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="d00b4-120">The resource id.</span></span>

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

### <span data-ttu-id="d00b4-121">-Skip</span><span class="sxs-lookup"><span data-stu-id="d00b4-121">-Skip</span></span>
<span data-ttu-id="d00b4-122">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="d00b4-122">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: ListAll, List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d00b4-123">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="d00b4-123">-Top</span></span>
<span data-ttu-id="d00b4-124">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="d00b4-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="d00b4-125">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="d00b4-125">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: ListAll, List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d00b4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d00b4-126">CommonParameters</span></span>
<span data-ttu-id="d00b4-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d00b4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d00b4-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d00b4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d00b4-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d00b4-129">INPUTS</span></span>

## <span data-ttu-id="d00b4-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d00b4-130">OUTPUTS</span></span>

### <span data-ttu-id="d00b4-131">Microsoft. AzureStack. Management. subscriptions. admin. Models. offer</span><span class="sxs-lookup"><span data-stu-id="d00b4-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer</span></span>

## <span data-ttu-id="d00b4-132">Note</span><span class="sxs-lookup"><span data-stu-id="d00b4-132">NOTES</span></span>

## <span data-ttu-id="d00b4-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d00b4-133">RELATED LINKS</span></span>

