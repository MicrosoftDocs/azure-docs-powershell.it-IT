---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageSku.md
ms.openlocfilehash: 7c4b59f97a6cd74da791f090b1c90be72f43a2c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687942"
---
# <span data-ttu-id="e73f6-101">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="e73f6-101">Get-AzureRmVMImageSku</span></span>

## <span data-ttu-id="e73f6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e73f6-102">SYNOPSIS</span></span>
<span data-ttu-id="e73f6-103">Ottiene SKU di VMImage.</span><span class="sxs-lookup"><span data-stu-id="e73f6-103">Gets VMImage SKUs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e73f6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e73f6-104">SYNTAX</span></span>

```
Get-AzureRmVMImageSku -Location <String> -PublisherName <String> -Offer <String> [<CommonParameters>]
```

## <span data-ttu-id="e73f6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e73f6-105">DESCRIPTION</span></span>
<span data-ttu-id="e73f6-106">Il cmdlet **Get-AzureRmVMImageSku** ottiene SKU VMImage.</span><span class="sxs-lookup"><span data-stu-id="e73f6-106">The **Get-AzureRmVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="e73f6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e73f6-107">EXAMPLES</span></span>

### <span data-ttu-id="e73f6-108">Esempio 1: ottenere SKU di VMImage</span><span class="sxs-lookup"><span data-stu-id="e73f6-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzureRmVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="e73f6-109">Questo comando consente di ottenere gli SKU per l'autore e l'offerta specificati.</span><span class="sxs-lookup"><span data-stu-id="e73f6-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="e73f6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e73f6-110">PARAMETERS</span></span>

### <span data-ttu-id="e73f6-111">-Posizione</span><span class="sxs-lookup"><span data-stu-id="e73f6-111">-Location</span></span>
<span data-ttu-id="e73f6-112">Specifica la posizione di VMImage.</span><span class="sxs-lookup"><span data-stu-id="e73f6-112">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="e73f6-113">-Offerta</span><span class="sxs-lookup"><span data-stu-id="e73f6-113">-Offer</span></span>
<span data-ttu-id="e73f6-114">Specifica il tipo di offerta VMImage.</span><span class="sxs-lookup"><span data-stu-id="e73f6-114">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="e73f6-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="e73f6-115">-PublisherName</span></span>
<span data-ttu-id="e73f6-116">Specifica l'autore di un VMImage.</span><span class="sxs-lookup"><span data-stu-id="e73f6-116">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="e73f6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e73f6-117">CommonParameters</span></span>
<span data-ttu-id="e73f6-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e73f6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e73f6-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e73f6-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e73f6-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e73f6-120">INPUTS</span></span>

### <span data-ttu-id="e73f6-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e73f6-121">None</span></span>
<span data-ttu-id="e73f6-122">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="e73f6-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e73f6-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e73f6-123">OUTPUTS</span></span>

## <span data-ttu-id="e73f6-124">Note</span><span class="sxs-lookup"><span data-stu-id="e73f6-124">NOTES</span></span>

## <span data-ttu-id="e73f6-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e73f6-125">RELATED LINKS</span></span>

[<span data-ttu-id="e73f6-126">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="e73f6-126">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="e73f6-127">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="e73f6-127">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="e73f6-128">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="e73f6-128">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="e73f6-129">Salva-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="e73f6-129">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


