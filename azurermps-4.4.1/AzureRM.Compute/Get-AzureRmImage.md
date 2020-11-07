---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmImage.md
ms.openlocfilehash: c1d7a7128c0fd4774c99799695e0d041a08c8053
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688036"
---
# <span data-ttu-id="6677c-101">Get-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="6677c-101">Get-AzureRmImage</span></span>

## <span data-ttu-id="6677c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6677c-102">SYNOPSIS</span></span>
<span data-ttu-id="6677c-103">Ottiene le proprietà di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="6677c-103">Gets the properties of an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6677c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6677c-104">SYNTAX</span></span>

```
Get-AzureRmImage [[-ResourceGroupName] <String>] [[-ImageName] <String>] [[-Expand] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6677c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6677c-105">DESCRIPTION</span></span>
<span data-ttu-id="6677c-106">Il cmdlet **Get-AzureRmImage** ottiene le proprietà di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="6677c-106">The **Get-AzureRmImage** cmdlet gets the properties of an image.</span></span>

## <span data-ttu-id="6677c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6677c-107">EXAMPLES</span></span>

### <span data-ttu-id="6677c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6677c-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01'
```

<span data-ttu-id="6677c-109">Questo comando consente di ottenere le proprietà dell'immagine denominata "Image01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="6677c-109">This command gets the properties of the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="6677c-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="6677c-110">Example 2</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="6677c-111">Questo comando consente di ottenere le proprietà di tutte le immagini nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="6677c-111">This command gets the properties of all images in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="6677c-112">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="6677c-112">Example 3</span></span>
```
PS C:\> Get-AzureRmImage
```

<span data-ttu-id="6677c-113">Questo comando consente di ottenere le proprietà di tutte le immagini sotto l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="6677c-113">This command gets the properties of all images under the subscription.</span></span>

## <span data-ttu-id="6677c-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6677c-114">PARAMETERS</span></span>

### <span data-ttu-id="6677c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6677c-115">-DefaultProfile</span></span>
<span data-ttu-id="6677c-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6677c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6677c-117">-Espandi</span><span class="sxs-lookup"><span data-stu-id="6677c-117">-Expand</span></span>
<span data-ttu-id="6677c-118">Specifica la query di espressione Expand.</span><span class="sxs-lookup"><span data-stu-id="6677c-118">Specifies the expand expression query.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6677c-119">-ImageName</span><span class="sxs-lookup"><span data-stu-id="6677c-119">-ImageName</span></span>
<span data-ttu-id="6677c-120">Specifica il nome di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="6677c-120">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6677c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6677c-121">-ResourceGroupName</span></span>
<span data-ttu-id="6677c-122">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6677c-122">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6677c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6677c-123">CommonParameters</span></span>
<span data-ttu-id="6677c-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6677c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6677c-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6677c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6677c-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6677c-126">INPUTS</span></span>

### <span data-ttu-id="6677c-127">System. String</span><span class="sxs-lookup"><span data-stu-id="6677c-127">System.String</span></span>

## <span data-ttu-id="6677c-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6677c-128">OUTPUTS</span></span>

### <span data-ttu-id="6677c-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="6677c-129">System.Object</span></span>

## <span data-ttu-id="6677c-130">Note</span><span class="sxs-lookup"><span data-stu-id="6677c-130">NOTES</span></span>

## <span data-ttu-id="6677c-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6677c-131">RELATED LINKS</span></span>

