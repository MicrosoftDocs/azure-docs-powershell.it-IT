---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
ms.openlocfilehash: 6355ce5cea881f66473ca8d541585187a79fe23e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852109"
---
# <span data-ttu-id="00c42-101">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="00c42-101">Get-AzVMImageSku</span></span>

## <span data-ttu-id="00c42-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="00c42-102">SYNOPSIS</span></span>
<span data-ttu-id="00c42-103">Ottiene SKU di VMImage.</span><span class="sxs-lookup"><span data-stu-id="00c42-103">Gets VMImage SKUs.</span></span>

## <span data-ttu-id="00c42-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="00c42-104">SYNTAX</span></span>

```
Get-AzVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00c42-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="00c42-105">DESCRIPTION</span></span>
<span data-ttu-id="00c42-106">Il cmdlet **Get-AzVMImageSku** ottiene SKU VMImage.</span><span class="sxs-lookup"><span data-stu-id="00c42-106">The **Get-AzVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="00c42-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="00c42-107">EXAMPLES</span></span>

### <span data-ttu-id="00c42-108">Esempio 1: ottenere SKU di VMImage</span><span class="sxs-lookup"><span data-stu-id="00c42-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="00c42-109">Questo comando consente di ottenere gli SKU per l'autore e l'offerta specificati.</span><span class="sxs-lookup"><span data-stu-id="00c42-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="00c42-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="00c42-110">PARAMETERS</span></span>

### <span data-ttu-id="00c42-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00c42-111">-DefaultProfile</span></span>
<span data-ttu-id="00c42-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="00c42-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00c42-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="00c42-113">-Location</span></span>
<span data-ttu-id="00c42-114">Specifica la posizione di VMImage.</span><span class="sxs-lookup"><span data-stu-id="00c42-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="00c42-115">-Offerta</span><span class="sxs-lookup"><span data-stu-id="00c42-115">-Offer</span></span>
<span data-ttu-id="00c42-116">Specifica il tipo di offerta VMImage.</span><span class="sxs-lookup"><span data-stu-id="00c42-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="00c42-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="00c42-117">-PublisherName</span></span>
<span data-ttu-id="00c42-118">Specifica l'autore di un VMImage.</span><span class="sxs-lookup"><span data-stu-id="00c42-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="00c42-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00c42-119">CommonParameters</span></span>
<span data-ttu-id="00c42-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00c42-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00c42-121">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="00c42-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00c42-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="00c42-122">INPUTS</span></span>

### <span data-ttu-id="00c42-123">System. String</span><span class="sxs-lookup"><span data-stu-id="00c42-123">System.String</span></span>

## <span data-ttu-id="00c42-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="00c42-124">OUTPUTS</span></span>

### <span data-ttu-id="00c42-125">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineImageSku</span><span class="sxs-lookup"><span data-stu-id="00c42-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span></span>

## <span data-ttu-id="00c42-126">Note</span><span class="sxs-lookup"><span data-stu-id="00c42-126">NOTES</span></span>

## <span data-ttu-id="00c42-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="00c42-127">RELATED LINKS</span></span>

[<span data-ttu-id="00c42-128">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="00c42-128">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="00c42-129">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="00c42-129">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="00c42-130">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="00c42-130">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="00c42-131">Salva-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="00c42-131">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


