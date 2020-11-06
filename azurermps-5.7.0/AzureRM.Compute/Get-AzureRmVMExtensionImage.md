---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImage.md
ms.openlocfilehash: bae8fb04e71700d1572b8742f8cccbb2ebe8e331
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510011"
---
# <span data-ttu-id="3585e-101">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="3585e-101">Get-AzureRmVMExtensionImage</span></span>

## <span data-ttu-id="3585e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3585e-102">SYNOPSIS</span></span>
<span data-ttu-id="3585e-103">Ottiene tutte le versioni per un'estensione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3585e-103">Gets all versions for an Azure extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3585e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3585e-104">SYNTAX</span></span>

```
Get-AzureRmVMExtensionImage -Location <String> -PublisherName <String> -Type <String>
 [-FilterExpression <String>] [-Version <String>] [<CommonParameters>]
```

## <span data-ttu-id="3585e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3585e-105">DESCRIPTION</span></span>
<span data-ttu-id="3585e-106">Il cmdlet **Get-AzureRmVMExtensionImage** ottiene tutte le versioni per un'estensione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3585e-106">The **Get-AzureRmVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="3585e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3585e-107">EXAMPLES</span></span>

### <span data-ttu-id="3585e-108">Esempio 1: ottenere le versioni di un'immagine di estensione</span><span class="sxs-lookup"><span data-stu-id="3585e-108">Example 1: Get the versions of an extension image</span></span>
```
PS C:\> Get-AzureRmVMExtensionImage -Location "Central US" -PublisherName "Fabrikam" -Type "FabrikamEndpointProtection"
```

<span data-ttu-id="3585e-109">Questo comando consente di ottenere tutte le versioni dell'immagine dell'estensione per la posizione, l'editore e il tipo specificati.</span><span class="sxs-lookup"><span data-stu-id="3585e-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

## <span data-ttu-id="3585e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3585e-110">PARAMETERS</span></span>

### <span data-ttu-id="3585e-111">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="3585e-111">-FilterExpression</span></span>
<span data-ttu-id="3585e-112">Specifica un'espressione di filtro.</span><span class="sxs-lookup"><span data-stu-id="3585e-112">Specifies a filter expression.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3585e-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="3585e-113">-Location</span></span>
<span data-ttu-id="3585e-114">Specifica la posizione di un'estensione.</span><span class="sxs-lookup"><span data-stu-id="3585e-114">Specifies the location of an extension.</span></span>

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

### <span data-ttu-id="3585e-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="3585e-115">-PublisherName</span></span>
<span data-ttu-id="3585e-116">Specifica il nome di un Publisher di estensione.</span><span class="sxs-lookup"><span data-stu-id="3585e-116">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="3585e-117">Per ottenere un Publisher di estensione, usare il cmdlet Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="3585e-117">To obtain an extension publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="3585e-118">-Digitare</span><span class="sxs-lookup"><span data-stu-id="3585e-118">-Type</span></span>
<span data-ttu-id="3585e-119">Specifica il tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="3585e-119">Specifies the type of the extension.</span></span>
<span data-ttu-id="3585e-120">Per ottenere un tipo di estensione, usare il cmdlet Get-AzureRmVMExtensionImageType.</span><span class="sxs-lookup"><span data-stu-id="3585e-120">To obtain an extension type, use the Get-AzureRmVMExtensionImageType cmdlet.</span></span>

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

### <span data-ttu-id="3585e-121">-Versione</span><span class="sxs-lookup"><span data-stu-id="3585e-121">-Version</span></span>
<span data-ttu-id="3585e-122">Specifica la versione dell'estensione che questo cmdlet ottiene.</span><span class="sxs-lookup"><span data-stu-id="3585e-122">Specifies the version of the extension that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3585e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3585e-123">CommonParameters</span></span>
<span data-ttu-id="3585e-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3585e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3585e-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3585e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3585e-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3585e-126">INPUTS</span></span>

### <span data-ttu-id="3585e-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3585e-127">None</span></span>
<span data-ttu-id="3585e-128">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="3585e-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3585e-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3585e-129">OUTPUTS</span></span>

## <span data-ttu-id="3585e-130">Note</span><span class="sxs-lookup"><span data-stu-id="3585e-130">NOTES</span></span>

## <span data-ttu-id="3585e-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3585e-131">RELATED LINKS</span></span>

[<span data-ttu-id="3585e-132">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="3585e-132">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="3585e-133">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="3585e-133">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="3585e-134">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="3585e-134">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)


