---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmimagesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
ms.openlocfilehash: 4eea328b83b4d4ad70ba755e4875168b6b35ecb7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013742"
---
# <span data-ttu-id="a193e-101">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="a193e-101">Get-AzVMImageSku</span></span>

## <span data-ttu-id="a193e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a193e-102">SYNOPSIS</span></span>
<span data-ttu-id="a193e-103">Ottiene SKU VMImage.</span><span class="sxs-lookup"><span data-stu-id="a193e-103">Gets VMImage SKUs.</span></span>

## <span data-ttu-id="a193e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a193e-104">SYNTAX</span></span>

```
Get-AzVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a193e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a193e-105">DESCRIPTION</span></span>
<span data-ttu-id="a193e-106">Il **cmdlet Get-AzVMImageSku** ottiene SKU VMImage.</span><span class="sxs-lookup"><span data-stu-id="a193e-106">The **Get-AzVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="a193e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a193e-107">EXAMPLES</span></span>

### <span data-ttu-id="a193e-108">Esempio 1: Ottenere SKU VMImage</span><span class="sxs-lookup"><span data-stu-id="a193e-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="a193e-109">Questo comando ottiene gli SKU per l'editore e l'offerta specificati.</span><span class="sxs-lookup"><span data-stu-id="a193e-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="a193e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a193e-110">PARAMETERS</span></span>

### <span data-ttu-id="a193e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a193e-111">-DefaultProfile</span></span>
<span data-ttu-id="a193e-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a193e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a193e-113">-Location</span><span class="sxs-lookup"><span data-stu-id="a193e-113">-Location</span></span>
<span data-ttu-id="a193e-114">Specifica la posizione dell'immagine VMImage.</span><span class="sxs-lookup"><span data-stu-id="a193e-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="a193e-115">-Offerta</span><span class="sxs-lookup"><span data-stu-id="a193e-115">-Offer</span></span>
<span data-ttu-id="a193e-116">Specifica il tipo di offerta VMImage.</span><span class="sxs-lookup"><span data-stu-id="a193e-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="a193e-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="a193e-117">-PublisherName</span></span>
<span data-ttu-id="a193e-118">Specifica l'autore di un oggetto VMImage.</span><span class="sxs-lookup"><span data-stu-id="a193e-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="a193e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a193e-119">CommonParameters</span></span>
<span data-ttu-id="a193e-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a193e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a193e-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a193e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a193e-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="a193e-122">INPUTS</span></span>

### <span data-ttu-id="a193e-123">System.String</span><span class="sxs-lookup"><span data-stu-id="a193e-123">System.String</span></span>

## <span data-ttu-id="a193e-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a193e-124">OUTPUTS</span></span>

### <span data-ttu-id="a193e-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span><span class="sxs-lookup"><span data-stu-id="a193e-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span></span>

## <span data-ttu-id="a193e-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="a193e-126">NOTES</span></span>

## <span data-ttu-id="a193e-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a193e-127">RELATED LINKS</span></span>

[<span data-ttu-id="a193e-128">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="a193e-128">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="a193e-129">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="a193e-129">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="a193e-130">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="a193e-130">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="a193e-131">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="a193e-131">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


