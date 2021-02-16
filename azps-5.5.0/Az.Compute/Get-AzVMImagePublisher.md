---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagepublisher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
ms.openlocfilehash: 947c792c68a314fcfbdc81595f2035c1da539966
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199287"
---
# <span data-ttu-id="977b8-101">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="977b8-101">Get-AzVMImagePublisher</span></span>

## <span data-ttu-id="977b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="977b8-102">SYNOPSIS</span></span>
<span data-ttu-id="977b8-103">Ottiene gli editori VMImage.</span><span class="sxs-lookup"><span data-stu-id="977b8-103">Gets the VMImage publishers.</span></span>

## <span data-ttu-id="977b8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="977b8-104">SYNTAX</span></span>

```
Get-AzVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="977b8-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="977b8-105">DESCRIPTION</span></span>
<span data-ttu-id="977b8-106">Il **cmdlet Get-AzVMImagePublisher** ottiene gli editori VMImage.</span><span class="sxs-lookup"><span data-stu-id="977b8-106">The **Get-AzVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="977b8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="977b8-107">EXAMPLES</span></span>

### <span data-ttu-id="977b8-108">Esempio 1: Ottenere gli editori VMImage per un'area geografica</span><span class="sxs-lookup"><span data-stu-id="977b8-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzVMImagePublisher -Location "Central US"
```

<span data-ttu-id="977b8-109">Questo comando recupera gli editori delle istanze di VMImage per l'area geografica Degli Stati Uniti centrali all'interno del profilo di Azure.</span><span class="sxs-lookup"><span data-stu-id="977b8-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="977b8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="977b8-110">PARAMETERS</span></span>

### <span data-ttu-id="977b8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="977b8-111">-DefaultProfile</span></span>
<span data-ttu-id="977b8-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="977b8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="977b8-113">-Location</span><span class="sxs-lookup"><span data-stu-id="977b8-113">-Location</span></span>
<span data-ttu-id="977b8-114">Specifica la posizione dell'immagine VMImage.</span><span class="sxs-lookup"><span data-stu-id="977b8-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="977b8-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="977b8-115">CommonParameters</span></span>
<span data-ttu-id="977b8-116">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="977b8-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="977b8-117">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="977b8-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="977b8-118">INPUT</span><span class="sxs-lookup"><span data-stu-id="977b8-118">INPUTS</span></span>

### <span data-ttu-id="977b8-119">System.String</span><span class="sxs-lookup"><span data-stu-id="977b8-119">System.String</span></span>

## <span data-ttu-id="977b8-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="977b8-120">OUTPUTS</span></span>

### <span data-ttu-id="977b8-121">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span><span class="sxs-lookup"><span data-stu-id="977b8-121">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="977b8-122">NOTE</span><span class="sxs-lookup"><span data-stu-id="977b8-122">NOTES</span></span>

## <span data-ttu-id="977b8-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="977b8-123">RELATED LINKS</span></span>

[<span data-ttu-id="977b8-124">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="977b8-124">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="977b8-125">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="977b8-125">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="977b8-126">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="977b8-126">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="977b8-127">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="977b8-127">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


