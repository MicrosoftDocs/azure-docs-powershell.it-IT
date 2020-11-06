---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImage.md
ms.openlocfilehash: 5588d320d63a298fab632ea55d7c3b6c2220db85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508732"
---
# <span data-ttu-id="1bf4b-101">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="1bf4b-101">Get-AzureRmVMImage</span></span>

## <span data-ttu-id="1bf4b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1bf4b-102">SYNOPSIS</span></span>
<span data-ttu-id="1bf4b-103">Ottiene tutte le versioni di un VMImage.</span><span class="sxs-lookup"><span data-stu-id="1bf4b-103">Gets all the versions of a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1bf4b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1bf4b-104">SYNTAX</span></span>

### <span data-ttu-id="1bf4b-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="1bf4b-105">ListVMImage</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1bf4b-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="1bf4b-106">GetVMImageDetail</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1bf4b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1bf4b-107">DESCRIPTION</span></span>
<span data-ttu-id="1bf4b-108">Il cmdlet **Get-AzureRmVMImage** ottiene tutte le versioni di un VMImage.</span><span class="sxs-lookup"><span data-stu-id="1bf4b-108">The **Get-AzureRmVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="1bf4b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1bf4b-109">EXAMPLES</span></span>

### <span data-ttu-id="1bf4b-110">Esempio 1: ottenere oggetti VMImage</span><span class="sxs-lookup"><span data-stu-id="1bf4b-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzureRmVMImage -Location "Central US" -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.04-DAILY"
```

<span data-ttu-id="1bf4b-111">Questo comando consente di ottenere tutte le versioni di VMImage che corrispondono ai valori specificati.</span><span class="sxs-lookup"><span data-stu-id="1bf4b-111">This command gets all the versions of VMImage that match the specified values.</span></span>

## <span data-ttu-id="1bf4b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1bf4b-112">PARAMETERS</span></span>

### <span data-ttu-id="1bf4b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bf4b-113">-DefaultProfile</span></span>
<span data-ttu-id="1bf4b-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1bf4b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bf4b-115">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="1bf4b-115">-FilterExpression</span></span>
<span data-ttu-id="1bf4b-116">Specifica un'espressione di filtro.</span><span class="sxs-lookup"><span data-stu-id="1bf4b-116">Specifies a filter expression.</span></span>

```yaml
Type: System.String
Parameter Sets: ListVMImage
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bf4b-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="1bf4b-117">-Location</span></span>
<span data-ttu-id="1bf4b-118">Specifica la posizione di un VMImage.</span><span class="sxs-lookup"><span data-stu-id="1bf4b-118">Specifies the location of a VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bf4b-119">-Offerta</span><span class="sxs-lookup"><span data-stu-id="1bf4b-119">-Offer</span></span>
<span data-ttu-id="1bf4b-120">Specifica il tipo di offerta VMImage.</span><span class="sxs-lookup"><span data-stu-id="1bf4b-120">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="1bf4b-121">Per ottenere un'offerta di immagine, usare il cmdlet Get-AzureRmVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="1bf4b-121">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bf4b-122">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="1bf4b-122">-PublisherName</span></span>
<span data-ttu-id="1bf4b-123">Specifica l'autore di un VMImage.</span><span class="sxs-lookup"><span data-stu-id="1bf4b-123">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="1bf4b-124">Per ottenere un autore di immagini, usare il cmdlet Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="1bf4b-124">To obtain an image publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bf4b-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="1bf4b-125">-Skus</span></span>
<span data-ttu-id="1bf4b-126">Specifica una SKU di VMImage.</span><span class="sxs-lookup"><span data-stu-id="1bf4b-126">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="1bf4b-127">Per ottenere un SKU, usare il cmdlet Get-AzureRmVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="1bf4b-127">To obtain an SKU, use the Get-AzureRmVMImageSku cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bf4b-128">-Versione</span><span class="sxs-lookup"><span data-stu-id="1bf4b-128">-Version</span></span>
<span data-ttu-id="1bf4b-129">Specifica la versione di VMImage.</span><span class="sxs-lookup"><span data-stu-id="1bf4b-129">Specifies the version of the VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVMImageDetail
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bf4b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bf4b-130">CommonParameters</span></span>
<span data-ttu-id="1bf4b-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bf4b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bf4b-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bf4b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bf4b-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1bf4b-133">INPUTS</span></span>

## <span data-ttu-id="1bf4b-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1bf4b-134">OUTPUTS</span></span>

## <span data-ttu-id="1bf4b-135">Note</span><span class="sxs-lookup"><span data-stu-id="1bf4b-135">NOTES</span></span>

## <span data-ttu-id="1bf4b-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1bf4b-136">RELATED LINKS</span></span>

[<span data-ttu-id="1bf4b-137">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="1bf4b-137">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="1bf4b-138">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="1bf4b-138">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="1bf4b-139">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="1bf4b-139">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="1bf4b-140">Salva-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="1bf4b-140">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


