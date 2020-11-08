---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
ms.openlocfilehash: 9b67d2973296f1a497f6e22ee2f35e9ff4580b6b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189153"
---
# <span data-ttu-id="42d77-101">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="42d77-101">Get-AzVMImageSku</span></span>

## <span data-ttu-id="42d77-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="42d77-102">SYNOPSIS</span></span>
<span data-ttu-id="42d77-103">Ottiene SKU di VMImage.</span><span class="sxs-lookup"><span data-stu-id="42d77-103">Gets VMImage SKUs.</span></span>

## <span data-ttu-id="42d77-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="42d77-104">SYNTAX</span></span>

```
Get-AzVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42d77-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="42d77-105">DESCRIPTION</span></span>
<span data-ttu-id="42d77-106">Il cmdlet **Get-AzVMImageSku** ottiene SKU VMImage.</span><span class="sxs-lookup"><span data-stu-id="42d77-106">The **Get-AzVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="42d77-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="42d77-107">EXAMPLES</span></span>

### <span data-ttu-id="42d77-108">Esempio 1: ottenere SKU di VMImage</span><span class="sxs-lookup"><span data-stu-id="42d77-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="42d77-109">Questo comando consente di ottenere gli SKU per l'autore e l'offerta specificati.</span><span class="sxs-lookup"><span data-stu-id="42d77-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="42d77-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="42d77-110">PARAMETERS</span></span>

### <span data-ttu-id="42d77-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42d77-111">-DefaultProfile</span></span>
<span data-ttu-id="42d77-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="42d77-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42d77-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="42d77-113">-Location</span></span>
<span data-ttu-id="42d77-114">Specifica la posizione di VMImage.</span><span class="sxs-lookup"><span data-stu-id="42d77-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="42d77-115">-Offerta</span><span class="sxs-lookup"><span data-stu-id="42d77-115">-Offer</span></span>
<span data-ttu-id="42d77-116">Specifica il tipo di offerta VMImage.</span><span class="sxs-lookup"><span data-stu-id="42d77-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="42d77-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="42d77-117">-PublisherName</span></span>
<span data-ttu-id="42d77-118">Specifica l'autore di un VMImage.</span><span class="sxs-lookup"><span data-stu-id="42d77-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="42d77-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42d77-119">CommonParameters</span></span>
<span data-ttu-id="42d77-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42d77-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42d77-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="42d77-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42d77-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="42d77-122">INPUTS</span></span>

### <span data-ttu-id="42d77-123">System. String</span><span class="sxs-lookup"><span data-stu-id="42d77-123">System.String</span></span>

## <span data-ttu-id="42d77-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="42d77-124">OUTPUTS</span></span>

### <span data-ttu-id="42d77-125">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineImageSku</span><span class="sxs-lookup"><span data-stu-id="42d77-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span></span>

## <span data-ttu-id="42d77-126">Note</span><span class="sxs-lookup"><span data-stu-id="42d77-126">NOTES</span></span>

## <span data-ttu-id="42d77-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="42d77-127">RELATED LINKS</span></span>

[<span data-ttu-id="42d77-128">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="42d77-128">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="42d77-129">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="42d77-129">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="42d77-130">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="42d77-130">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="42d77-131">Salva-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="42d77-131">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


