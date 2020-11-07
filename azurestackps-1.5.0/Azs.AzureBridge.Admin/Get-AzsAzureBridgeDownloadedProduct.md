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
ms.locfileid: "93688697"
---
# <span data-ttu-id="3b15f-101">Get-AzsAzureBridgeDownloadedProduct</span><span class="sxs-lookup"><span data-stu-id="3b15f-101">Get-AzsAzureBridgeDownloadedProduct</span></span>

## <span data-ttu-id="3b15f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3b15f-102">SYNOPSIS</span></span>
<span data-ttu-id="3b15f-103">Restituisce un elenco di prodotti scaricati da Azure MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="3b15f-103">Returns a list of products downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="3b15f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3b15f-104">SYNTAX</span></span>

### <span data-ttu-id="3b15f-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3b15f-105">List (Default)</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ActivationName <String> -ResourceGroupName <String> [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="3b15f-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="3b15f-106">Get</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [<CommonParameters>]
```

### <span data-ttu-id="3b15f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b15f-107">ResourceId</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="3b15f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3b15f-108">DESCRIPTION</span></span>
<span data-ttu-id="3b15f-109">Restituisce un elenco di prodotti scaricati da Azure MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="3b15f-109">Returns a list of products downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="3b15f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3b15f-110">EXAMPLES</span></span>

### <span data-ttu-id="3b15f-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3b15f-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="3b15f-112">Ottenere un elenco dei prodotti scaricati da Bridge di Azure</span><span class="sxs-lookup"><span data-stu-id="3b15f-112">Get a list of Azure Bridge Downloaded products</span></span>

### <span data-ttu-id="3b15f-113">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="3b15f-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -Name 'microsoft.docker-arm.1.1.0' -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="3b15f-114">Ottenere un prodotto scaricato da Azure Bridge per nome</span><span class="sxs-lookup"><span data-stu-id="3b15f-114">Get an Azure Bridge Downloaded Product by Name</span></span>

## <span data-ttu-id="3b15f-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3b15f-115">PARAMETERS</span></span>

### <span data-ttu-id="3b15f-116">-Activationname</span><span class="sxs-lookup"><span data-stu-id="3b15f-116">-ActivationName</span></span>
<span data-ttu-id="3b15f-117">Nome dell'attivazione.</span><span class="sxs-lookup"><span data-stu-id="3b15f-117">Name of the activation.</span></span>

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

### <span data-ttu-id="3b15f-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="3b15f-118">-Name</span></span>
<span data-ttu-id="3b15f-119">Nome del prodotto.</span><span class="sxs-lookup"><span data-stu-id="3b15f-119">Name of the product.</span></span>

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

### <span data-ttu-id="3b15f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b15f-120">-ResourceGroupName</span></span>
<span data-ttu-id="3b15f-121">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="3b15f-121">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="3b15f-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b15f-122">-ResourceId</span></span>
<span data-ttu-id="3b15f-123">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="3b15f-123">The resource id.</span></span>

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

### <span data-ttu-id="3b15f-124">-Skip</span><span class="sxs-lookup"><span data-stu-id="3b15f-124">-Skip</span></span>
<span data-ttu-id="3b15f-125">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="3b15f-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="3b15f-126">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="3b15f-126">-Top</span></span>
<span data-ttu-id="3b15f-127">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="3b15f-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="3b15f-128">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="3b15f-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="3b15f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b15f-129">CommonParameters</span></span>
<span data-ttu-id="3b15f-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b15f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b15f-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b15f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b15f-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3b15f-132">INPUTS</span></span>

## <span data-ttu-id="3b15f-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3b15f-133">OUTPUTS</span></span>

### <span data-ttu-id="3b15f-134">Microsoft. AzureStack. Management. AzureBridge. admin. Models. DownloadedProductResource</span><span class="sxs-lookup"><span data-stu-id="3b15f-134">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.DownloadedProductResource</span></span>

## <span data-ttu-id="3b15f-135">Note</span><span class="sxs-lookup"><span data-stu-id="3b15f-135">NOTES</span></span>

## <span data-ttu-id="3b15f-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3b15f-136">RELATED LINKS</span></span>

