---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimagepublisher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
ms.openlocfilehash: 109f55c1afc1c00d26c47d0131d098158010bd70
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "93522190"
---
# <span data-ttu-id="311f1-101">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="311f1-101">Get-AzureRmVMImagePublisher</span></span>

## <span data-ttu-id="311f1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="311f1-102">SYNOPSIS</span></span>
<span data-ttu-id="311f1-103">Ottiene gli editori di VMImage.</span><span class="sxs-lookup"><span data-stu-id="311f1-103">Gets the VMImage publishers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="311f1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="311f1-104">SYNTAX</span></span>

```
Get-AzureRmVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="311f1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="311f1-105">DESCRIPTION</span></span>
<span data-ttu-id="311f1-106">Il cmdlet **Get-AzureRmVMImagePublisher** ottiene gli editori di VMImage.</span><span class="sxs-lookup"><span data-stu-id="311f1-106">The **Get-AzureRmVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="311f1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="311f1-107">EXAMPLES</span></span>

### <span data-ttu-id="311f1-108">Esempio 1: ottenere gli editori di VMImage per un'area geografica</span><span class="sxs-lookup"><span data-stu-id="311f1-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzureRmVMImagePublisher -Location "Central US"
```

<span data-ttu-id="311f1-109">Questo comando consente di ottenere gli editori delle istanze di VMImage per l'area centrale degli Stati Uniti all'interno del profilo di Azure.</span><span class="sxs-lookup"><span data-stu-id="311f1-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="311f1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="311f1-110">PARAMETERS</span></span>

### <span data-ttu-id="311f1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="311f1-111">-DefaultProfile</span></span>
<span data-ttu-id="311f1-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="311f1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="311f1-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="311f1-113">-Location</span></span>
<span data-ttu-id="311f1-114">Specifica la posizione di VMImage.</span><span class="sxs-lookup"><span data-stu-id="311f1-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="311f1-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="311f1-115">CommonParameters</span></span>
<span data-ttu-id="311f1-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="311f1-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="311f1-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="311f1-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="311f1-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="311f1-118">INPUTS</span></span>

### <span data-ttu-id="311f1-119">System. String</span><span class="sxs-lookup"><span data-stu-id="311f1-119">System.String</span></span>

## <span data-ttu-id="311f1-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="311f1-120">OUTPUTS</span></span>

### <span data-ttu-id="311f1-121">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineImagePublisher</span><span class="sxs-lookup"><span data-stu-id="311f1-121">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="311f1-122">Note</span><span class="sxs-lookup"><span data-stu-id="311f1-122">NOTES</span></span>

## <span data-ttu-id="311f1-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="311f1-123">RELATED LINKS</span></span>

[<span data-ttu-id="311f1-124">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="311f1-124">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="311f1-125">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="311f1-125">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="311f1-126">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="311f1-126">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="311f1-127">Salva-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="311f1-127">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


