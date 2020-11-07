---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermimage
schema: 2.0.0
ms.openlocfilehash: 8508a7353924342449324588e90abf3807d7f7ac
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866387"
---
# <span data-ttu-id="6532a-101">Get-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="6532a-101">Get-AzureRmImage</span></span>

## <span data-ttu-id="6532a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6532a-102">SYNOPSIS</span></span>
<span data-ttu-id="6532a-103">Ottiene le proprietà di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="6532a-103">Gets the properties of an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6532a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6532a-104">SYNTAX</span></span>

```
Get-AzureRmImage [[-ResourceGroupName] <String>] [[-ImageName] <String>] [[-Expand] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6532a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6532a-105">DESCRIPTION</span></span>
<span data-ttu-id="6532a-106">Il cmdlet **Get-AzureRmImage** ottiene le proprietà di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="6532a-106">The **Get-AzureRmImage** cmdlet gets the properties of an image.</span></span>

## <span data-ttu-id="6532a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6532a-107">EXAMPLES</span></span>

### <span data-ttu-id="6532a-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6532a-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01'
```

<span data-ttu-id="6532a-109">Questo comando consente di ottenere le proprietà dell'immagine denominata "Image01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="6532a-109">This command gets the properties of the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="6532a-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="6532a-110">Example 2</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="6532a-111">Questo comando consente di ottenere le proprietà di tutte le immagini nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="6532a-111">This command gets the properties of all images in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="6532a-112">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="6532a-112">Example 3</span></span>
```
PS C:\> Get-AzureRmImage
```

<span data-ttu-id="6532a-113">Questo comando consente di ottenere le proprietà di tutte le immagini sotto l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="6532a-113">This command gets the properties of all images under the subscription.</span></span>

## <span data-ttu-id="6532a-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6532a-114">PARAMETERS</span></span>

### <span data-ttu-id="6532a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6532a-115">-DefaultProfile</span></span>
<span data-ttu-id="6532a-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6532a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6532a-117">-Espandi</span><span class="sxs-lookup"><span data-stu-id="6532a-117">-Expand</span></span>
<span data-ttu-id="6532a-118">Specifica la query di espressione Expand.</span><span class="sxs-lookup"><span data-stu-id="6532a-118">Specifies the expand expression query.</span></span>

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

### <span data-ttu-id="6532a-119">-ImageName</span><span class="sxs-lookup"><span data-stu-id="6532a-119">-ImageName</span></span>
<span data-ttu-id="6532a-120">Specifica il nome di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="6532a-120">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="6532a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6532a-121">-ResourceGroupName</span></span>
<span data-ttu-id="6532a-122">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6532a-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="6532a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6532a-123">CommonParameters</span></span>
<span data-ttu-id="6532a-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6532a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6532a-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6532a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6532a-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6532a-126">INPUTS</span></span>

### <span data-ttu-id="6532a-127">System. String</span><span class="sxs-lookup"><span data-stu-id="6532a-127">System.String</span></span>

## <span data-ttu-id="6532a-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6532a-128">OUTPUTS</span></span>

### <span data-ttu-id="6532a-129">Microsoft. Azure. Commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="6532a-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="6532a-130">Note</span><span class="sxs-lookup"><span data-stu-id="6532a-130">NOTES</span></span>

## <span data-ttu-id="6532a-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6532a-131">RELATED LINKS</span></span>

