---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImageType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImageType.md
ms.openlocfilehash: 15b1316940c42534844245eaaf1aee3e450adc4b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510004"
---
# <span data-ttu-id="73a91-101">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="73a91-101">Get-AzureRmVMExtensionImageType</span></span>

## <span data-ttu-id="73a91-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="73a91-102">SYNOPSIS</span></span>
<span data-ttu-id="73a91-103">Ottiene il tipo di un'estensione di Azure.</span><span class="sxs-lookup"><span data-stu-id="73a91-103">Gets the type of an Azure extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73a91-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="73a91-104">SYNTAX</span></span>

```
Get-AzureRmVMExtensionImageType -Location <String> -PublisherName <String> [<CommonParameters>]
```

## <span data-ttu-id="73a91-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="73a91-105">DESCRIPTION</span></span>
<span data-ttu-id="73a91-106">Il cmdlet **Get-AzureRmVMExtensionImageType** ottiene il tipo di un'estensione di Azure.</span><span class="sxs-lookup"><span data-stu-id="73a91-106">The **Get-AzureRmVMExtensionImageType** cmdlet gets the type of an Azure extension.</span></span>

## <span data-ttu-id="73a91-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="73a91-107">EXAMPLES</span></span>

### <span data-ttu-id="73a91-108">Esempio 1: ottenere un tipo di immagine dell'estensione</span><span class="sxs-lookup"><span data-stu-id="73a91-108">Example 1: Get an extension image type</span></span>
```
PS C:\> Get-AzureRmVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="73a91-109">Questo comando ottiene il tipo di immagine dell'estensione per l'editore e la posizione specificati.</span><span class="sxs-lookup"><span data-stu-id="73a91-109">This command gets the extension image type for the specified publisher and location.</span></span>

## <span data-ttu-id="73a91-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="73a91-110">PARAMETERS</span></span>

### <span data-ttu-id="73a91-111">-Posizione</span><span class="sxs-lookup"><span data-stu-id="73a91-111">-Location</span></span>
<span data-ttu-id="73a91-112">Specifica la posizione di un'estensione.</span><span class="sxs-lookup"><span data-stu-id="73a91-112">Specifies the location of an extension.</span></span>
<span data-ttu-id="73a91-113">Questo cmdlet ottiene il tipo per un'estensione nella posizione specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="73a91-113">This cmdlet gets the type for an extension at the location that this parameter specifies.</span></span>

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

### <span data-ttu-id="73a91-114">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="73a91-114">-PublisherName</span></span>
<span data-ttu-id="73a91-115">Specifica il nome di un autore di un'estensione.</span><span class="sxs-lookup"><span data-stu-id="73a91-115">Specifies the name of a publisher of an extension.</span></span>
<span data-ttu-id="73a91-116">Per ottenere un Publisher di estensione, usare il cmdlet Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="73a91-116">To obtain an extension publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>
<span data-ttu-id="73a91-117">Questo cmdlet ottiene il tipo per un'estensione dall'editore specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="73a91-117">This cmdlet gets the type for an extension from the publisher that this parameter specifies.</span></span>

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

### <span data-ttu-id="73a91-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73a91-118">CommonParameters</span></span>
<span data-ttu-id="73a91-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73a91-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73a91-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73a91-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73a91-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="73a91-121">INPUTS</span></span>

### <span data-ttu-id="73a91-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="73a91-122">None</span></span>
<span data-ttu-id="73a91-123">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="73a91-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="73a91-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="73a91-124">OUTPUTS</span></span>

## <span data-ttu-id="73a91-125">Note</span><span class="sxs-lookup"><span data-stu-id="73a91-125">NOTES</span></span>

## <span data-ttu-id="73a91-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="73a91-126">RELATED LINKS</span></span>

[<span data-ttu-id="73a91-127">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="73a91-127">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="73a91-128">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="73a91-128">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)


