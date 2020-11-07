---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
ms.openlocfilehash: f299d0f299eaef61ba3655e8ec221cc55f5ab578
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687941"
---
# <span data-ttu-id="9ba4a-101">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="9ba4a-101">Get-AzureRmVMImagePublisher</span></span>

## <span data-ttu-id="9ba4a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9ba4a-102">SYNOPSIS</span></span>
<span data-ttu-id="9ba4a-103">Ottiene gli editori di VMImage.</span><span class="sxs-lookup"><span data-stu-id="9ba4a-103">Gets the VMImage publishers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ba4a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9ba4a-104">SYNTAX</span></span>

```
Get-AzureRmVMImagePublisher -Location <String> [<CommonParameters>]
```

## <span data-ttu-id="9ba4a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9ba4a-105">DESCRIPTION</span></span>
<span data-ttu-id="9ba4a-106">Il cmdlet **Get-AzureRmVMImagePublisher** ottiene gli editori di VMImage.</span><span class="sxs-lookup"><span data-stu-id="9ba4a-106">The **Get-AzureRmVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="9ba4a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9ba4a-107">EXAMPLES</span></span>

### <span data-ttu-id="9ba4a-108">Esempio 1: ottenere gli editori di VMImage per un'area geografica</span><span class="sxs-lookup"><span data-stu-id="9ba4a-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzureRmVMImagePublisher -Location "Central US"
```

<span data-ttu-id="9ba4a-109">Questo comando consente di ottenere gli editori delle istanze di VMImage per l'area centrale degli Stati Uniti all'interno del profilo di Azure.</span><span class="sxs-lookup"><span data-stu-id="9ba4a-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="9ba4a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9ba4a-110">PARAMETERS</span></span>

### <span data-ttu-id="9ba4a-111">-Posizione</span><span class="sxs-lookup"><span data-stu-id="9ba4a-111">-Location</span></span>
<span data-ttu-id="9ba4a-112">Specifica la posizione di VMImage.</span><span class="sxs-lookup"><span data-stu-id="9ba4a-112">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="9ba4a-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ba4a-113">CommonParameters</span></span>
<span data-ttu-id="9ba4a-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ba4a-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ba4a-115">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ba4a-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ba4a-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9ba4a-116">INPUTS</span></span>

### <span data-ttu-id="9ba4a-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="9ba4a-117">None</span></span>
<span data-ttu-id="9ba4a-118">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="9ba4a-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9ba4a-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9ba4a-119">OUTPUTS</span></span>

## <span data-ttu-id="9ba4a-120">Note</span><span class="sxs-lookup"><span data-stu-id="9ba4a-120">NOTES</span></span>

## <span data-ttu-id="9ba4a-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9ba4a-121">RELATED LINKS</span></span>

[<span data-ttu-id="9ba4a-122">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="9ba4a-122">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="9ba4a-123">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="9ba4a-123">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="9ba4a-124">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="9ba4a-124">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="9ba4a-125">Salva-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="9ba4a-125">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


