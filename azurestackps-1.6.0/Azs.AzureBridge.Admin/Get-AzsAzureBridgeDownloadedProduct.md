---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a9faaa3495e61186cab9d97d04e4d4b8186f152
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/22/2020
ms.locfileid: "93522205"
---
# <span data-ttu-id="e3f3b-101">Get-AzsAzureBridgeDownloadedProduct</span><span class="sxs-lookup"><span data-stu-id="e3f3b-101">Get-AzsAzureBridgeDownloadedProduct</span></span>

## <span data-ttu-id="e3f3b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e3f3b-102">SYNOPSIS</span></span>
<span data-ttu-id="e3f3b-103">Restituisce un elenco di prodotti scaricati da Azure MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="e3f3b-103">Returns a list of products downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="e3f3b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e3f3b-104">SYNTAX</span></span>

### <span data-ttu-id="e3f3b-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e3f3b-105">List (Default)</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ActivationName <String> -ResourceGroupName <String> [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="e3f3b-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="e3f3b-106">Get</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [<CommonParameters>]
```

### <span data-ttu-id="e3f3b-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3f3b-107">ResourceId</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="e3f3b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3f3b-108">DESCRIPTION</span></span>
<span data-ttu-id="e3f3b-109">Restituisce un elenco di prodotti scaricati da Azure MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="e3f3b-109">Returns a list of products downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="e3f3b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e3f3b-110">EXAMPLES</span></span>

### <span data-ttu-id="e3f3b-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e3f3b-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="e3f3b-112">Ottenere un elenco dei prodotti scaricati da Bridge di Azure</span><span class="sxs-lookup"><span data-stu-id="e3f3b-112">Get a list of Azure Bridge Downloaded products</span></span>

### <span data-ttu-id="e3f3b-113">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="e3f3b-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -Name 'microsoft.docker-arm.1.1.0' -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="e3f3b-114">Ottenere un prodotto scaricato da Azure Bridge per nome</span><span class="sxs-lookup"><span data-stu-id="e3f3b-114">Get an Azure Bridge Downloaded Product by Name</span></span>

## <span data-ttu-id="e3f3b-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e3f3b-115">PARAMETERS</span></span>

### <span data-ttu-id="e3f3b-116">-Activationname</span><span class="sxs-lookup"><span data-stu-id="e3f3b-116">-ActivationName</span></span>
<span data-ttu-id="e3f3b-117">Nome dell'attivazione.</span><span class="sxs-lookup"><span data-stu-id="e3f3b-117">Name of the activation.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3f3b-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="e3f3b-118">-Name</span></span>
<span data-ttu-id="e3f3b-119">Nome del prodotto.</span><span class="sxs-lookup"><span data-stu-id="e3f3b-119">Name of the product.</span></span>

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

### <span data-ttu-id="e3f3b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3f3b-120">-ResourceGroupName</span></span>
<span data-ttu-id="e3f3b-121">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="e3f3b-121">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3f3b-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3f3b-122">-ResourceId</span></span>
<span data-ttu-id="e3f3b-123">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="e3f3b-123">The resource id.</span></span>

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

### <span data-ttu-id="e3f3b-124">-Skip</span><span class="sxs-lookup"><span data-stu-id="e3f3b-124">-Skip</span></span>
<span data-ttu-id="e3f3b-125">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="e3f3b-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="e3f3b-126">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="e3f3b-126">-Top</span></span>
<span data-ttu-id="e3f3b-127">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="e3f3b-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="e3f3b-128">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="e3f3b-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="e3f3b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3f3b-129">CommonParameters</span></span>
<span data-ttu-id="e3f3b-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3f3b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3f3b-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3f3b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3f3b-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e3f3b-132">INPUTS</span></span>

## <span data-ttu-id="e3f3b-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3f3b-133">OUTPUTS</span></span>

### <span data-ttu-id="e3f3b-134">Microsoft. AzureStack. Management. AzureBridge. admin. Models. DownloadedProductResource</span><span class="sxs-lookup"><span data-stu-id="e3f3b-134">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.DownloadedProductResource</span></span>

## <span data-ttu-id="e3f3b-135">Note</span><span class="sxs-lookup"><span data-stu-id="e3f3b-135">NOTES</span></span>

## <span data-ttu-id="e3f3b-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e3f3b-136">RELATED LINKS</span></span>

