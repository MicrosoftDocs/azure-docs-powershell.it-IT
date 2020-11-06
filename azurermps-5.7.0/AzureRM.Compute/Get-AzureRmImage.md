---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmImage.md
ms.openlocfilehash: 3976418d89076b290500343775ca42e2fb975659
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516887"
---
# <span data-ttu-id="a8cad-101">Get-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="a8cad-101">Get-AzureRmImage</span></span>

## <span data-ttu-id="a8cad-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a8cad-102">SYNOPSIS</span></span>
<span data-ttu-id="a8cad-103">Ottiene le proprietà di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="a8cad-103">Gets the properties of an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8cad-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a8cad-104">SYNTAX</span></span>

```
Get-AzureRmImage [[-ResourceGroupName] <String>] [[-ImageName] <String>] [[-Expand] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="a8cad-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8cad-105">DESCRIPTION</span></span>
<span data-ttu-id="a8cad-106">Il cmdlet **Get-AzureRmImage** ottiene le proprietà di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="a8cad-106">The **Get-AzureRmImage** cmdlet gets the properties of an image.</span></span>

## <span data-ttu-id="a8cad-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a8cad-107">EXAMPLES</span></span>

### <span data-ttu-id="a8cad-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a8cad-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01'
```

<span data-ttu-id="a8cad-109">Questo comando consente di ottenere le proprietà dell'immagine denominata "Image01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="a8cad-109">This command gets the properties of the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="a8cad-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a8cad-110">Example 2</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="a8cad-111">Questo comando consente di ottenere le proprietà di tutte le immagini nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="a8cad-111">This command gets the properties of all images in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="a8cad-112">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="a8cad-112">Example 3</span></span>
```
PS C:\> Get-AzureRmImage
```

<span data-ttu-id="a8cad-113">Questo comando consente di ottenere le proprietà di tutte le immagini sotto l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a8cad-113">This command gets the properties of all images under the subscription.</span></span>

## <span data-ttu-id="a8cad-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a8cad-114">PARAMETERS</span></span>

### <span data-ttu-id="a8cad-115">-Espandi</span><span class="sxs-lookup"><span data-stu-id="a8cad-115">-Expand</span></span>
<span data-ttu-id="a8cad-116">Specifica la query di espressione Expand.</span><span class="sxs-lookup"><span data-stu-id="a8cad-116">Specifies the expand expression query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8cad-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="a8cad-117">-ImageName</span></span>
<span data-ttu-id="a8cad-118">Specifica il nome di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="a8cad-118">Specifies the name of an image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8cad-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8cad-119">-ResourceGroupName</span></span>
<span data-ttu-id="a8cad-120">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a8cad-120">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8cad-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8cad-121">CommonParameters</span></span>
<span data-ttu-id="a8cad-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8cad-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8cad-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8cad-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8cad-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a8cad-124">INPUTS</span></span>

### <span data-ttu-id="a8cad-125">System. String</span><span class="sxs-lookup"><span data-stu-id="a8cad-125">System.String</span></span>

## <span data-ttu-id="a8cad-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a8cad-126">OUTPUTS</span></span>

### <span data-ttu-id="a8cad-127">System. Object</span><span class="sxs-lookup"><span data-stu-id="a8cad-127">System.Object</span></span>

## <span data-ttu-id="a8cad-128">Note</span><span class="sxs-lookup"><span data-stu-id="a8cad-128">NOTES</span></span>

## <span data-ttu-id="a8cad-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a8cad-129">RELATED LINKS</span></span>

