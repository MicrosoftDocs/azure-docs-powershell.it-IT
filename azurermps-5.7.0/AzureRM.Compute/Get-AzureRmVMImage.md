---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImage.md
ms.openlocfilehash: f9e8eb9441604e3c07453f1e387ba17bd4623d55
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510000"
---
# <span data-ttu-id="28aba-101">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="28aba-101">Get-AzureRmVMImage</span></span>

## <span data-ttu-id="28aba-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="28aba-102">SYNOPSIS</span></span>
<span data-ttu-id="28aba-103">Ottiene tutte le versioni di un VMImage.</span><span class="sxs-lookup"><span data-stu-id="28aba-103">Gets all the versions of a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28aba-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="28aba-104">SYNTAX</span></span>

### <span data-ttu-id="28aba-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="28aba-105">ListVMImage</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [<CommonParameters>]
```

### <span data-ttu-id="28aba-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="28aba-106">GetVMImageDetail</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [<CommonParameters>]
```

## <span data-ttu-id="28aba-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="28aba-107">DESCRIPTION</span></span>
<span data-ttu-id="28aba-108">Il cmdlet **Get-AzureRmVMImage** ottiene tutte le versioni di un VMImage.</span><span class="sxs-lookup"><span data-stu-id="28aba-108">The **Get-AzureRmVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="28aba-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="28aba-109">EXAMPLES</span></span>

### <span data-ttu-id="28aba-110">Esempio 1: ottenere oggetti VMImage</span><span class="sxs-lookup"><span data-stu-id="28aba-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzureRmVMImage -Location "Central US" -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.04-DAILY"
```

<span data-ttu-id="28aba-111">Questo comando consente di ottenere tutte le versioni di VMImage che corrispondono ai valori specificati.</span><span class="sxs-lookup"><span data-stu-id="28aba-111">This command gets all the versions of VMImage that match the specified values.</span></span>

## <span data-ttu-id="28aba-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="28aba-112">PARAMETERS</span></span>

### <span data-ttu-id="28aba-113">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="28aba-113">-FilterExpression</span></span>
<span data-ttu-id="28aba-114">Specifica un'espressione di filtro.</span><span class="sxs-lookup"><span data-stu-id="28aba-114">Specifies a filter expression.</span></span>

```yaml
Type: String
Parameter Sets: ListVMImage
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28aba-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="28aba-115">-Location</span></span>
<span data-ttu-id="28aba-116">Specifica la posizione di un VMImage.</span><span class="sxs-lookup"><span data-stu-id="28aba-116">Specifies the location of a VMImage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28aba-117">-Offerta</span><span class="sxs-lookup"><span data-stu-id="28aba-117">-Offer</span></span>
<span data-ttu-id="28aba-118">Specifica il tipo di offerta VMImage.</span><span class="sxs-lookup"><span data-stu-id="28aba-118">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="28aba-119">Per ottenere un'offerta di immagine, usare il cmdlet Get-AzureRmVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="28aba-119">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28aba-120">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="28aba-120">-PublisherName</span></span>
<span data-ttu-id="28aba-121">Specifica l'autore di un VMImage.</span><span class="sxs-lookup"><span data-stu-id="28aba-121">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="28aba-122">Per ottenere un autore di immagini, usare il cmdlet Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="28aba-122">To obtain an image publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28aba-123">-SKU</span><span class="sxs-lookup"><span data-stu-id="28aba-123">-Skus</span></span>
<span data-ttu-id="28aba-124">Specifica una SKU di VMImage.</span><span class="sxs-lookup"><span data-stu-id="28aba-124">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="28aba-125">Per ottenere un SKU, usare il cmdlet Get-AzureRmVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="28aba-125">To obtain an SKU, use the Get-AzureRmVMImageSku cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28aba-126">-Versione</span><span class="sxs-lookup"><span data-stu-id="28aba-126">-Version</span></span>
<span data-ttu-id="28aba-127">Specifica la versione di VMImage.</span><span class="sxs-lookup"><span data-stu-id="28aba-127">Specifies the version of the VMImage.</span></span>

```yaml
Type: String
Parameter Sets: GetVMImageDetail
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28aba-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28aba-128">CommonParameters</span></span>
<span data-ttu-id="28aba-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28aba-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28aba-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28aba-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28aba-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="28aba-131">INPUTS</span></span>

### <span data-ttu-id="28aba-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="28aba-132">None</span></span>
<span data-ttu-id="28aba-133">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="28aba-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="28aba-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="28aba-134">OUTPUTS</span></span>

## <span data-ttu-id="28aba-135">Note</span><span class="sxs-lookup"><span data-stu-id="28aba-135">NOTES</span></span>

## <span data-ttu-id="28aba-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="28aba-136">RELATED LINKS</span></span>

[<span data-ttu-id="28aba-137">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="28aba-137">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="28aba-138">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="28aba-138">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="28aba-139">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="28aba-139">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="28aba-140">Salva-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="28aba-140">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


