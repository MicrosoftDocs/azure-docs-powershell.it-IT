---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimagepublisher
schema: 2.0.0
ms.openlocfilehash: 1faae0848a96595e71ba96c20f2df9df59cd7ef0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866765"
---
# <span data-ttu-id="bd616-101">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="bd616-101">Get-AzureRmVMImagePublisher</span></span>

## <span data-ttu-id="bd616-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bd616-102">SYNOPSIS</span></span>
<span data-ttu-id="bd616-103">Ottiene gli editori di VMImage.</span><span class="sxs-lookup"><span data-stu-id="bd616-103">Gets the VMImage publishers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd616-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bd616-104">SYNTAX</span></span>

```
Get-AzureRmVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd616-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bd616-105">DESCRIPTION</span></span>
<span data-ttu-id="bd616-106">Il cmdlet **Get-AzureRmVMImagePublisher** ottiene gli editori di VMImage.</span><span class="sxs-lookup"><span data-stu-id="bd616-106">The **Get-AzureRmVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="bd616-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bd616-107">EXAMPLES</span></span>

### <span data-ttu-id="bd616-108">Esempio 1: ottenere gli editori di VMImage per un'area geografica</span><span class="sxs-lookup"><span data-stu-id="bd616-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzureRmVMImagePublisher -Location "Central US"
```

<span data-ttu-id="bd616-109">Questo comando consente di ottenere gli editori delle istanze di VMImage per l'area centrale degli Stati Uniti all'interno del profilo di Azure.</span><span class="sxs-lookup"><span data-stu-id="bd616-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="bd616-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bd616-110">PARAMETERS</span></span>

### <span data-ttu-id="bd616-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd616-111">-DefaultProfile</span></span>
<span data-ttu-id="bd616-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bd616-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd616-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="bd616-113">-Location</span></span>
<span data-ttu-id="bd616-114">Specifica la posizione di VMImage.</span><span class="sxs-lookup"><span data-stu-id="bd616-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="bd616-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd616-115">CommonParameters</span></span>
<span data-ttu-id="bd616-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd616-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd616-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd616-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd616-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bd616-118">INPUTS</span></span>

### <span data-ttu-id="bd616-119">Nessuno</span><span class="sxs-lookup"><span data-stu-id="bd616-119">None</span></span>
<span data-ttu-id="bd616-120">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="bd616-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bd616-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bd616-121">OUTPUTS</span></span>

### <span data-ttu-id="bd616-122">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineImagePublisher</span><span class="sxs-lookup"><span data-stu-id="bd616-122">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="bd616-123">Note</span><span class="sxs-lookup"><span data-stu-id="bd616-123">NOTES</span></span>

## <span data-ttu-id="bd616-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bd616-124">RELATED LINKS</span></span>

[<span data-ttu-id="bd616-125">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="bd616-125">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="bd616-126">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="bd616-126">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="bd616-127">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="bd616-127">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="bd616-128">Salva-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="bd616-128">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


