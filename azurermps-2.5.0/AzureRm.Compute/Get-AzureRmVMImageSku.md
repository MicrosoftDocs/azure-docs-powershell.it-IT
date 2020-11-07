---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimagesku
schema: 2.0.0
ms.openlocfilehash: 8d2253e20e87a0e6a5d97f2dd0e405412f5a9282
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866763"
---
# <span data-ttu-id="a98fa-101">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="a98fa-101">Get-AzureRmVMImageSku</span></span>

## <span data-ttu-id="a98fa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a98fa-102">SYNOPSIS</span></span>
<span data-ttu-id="a98fa-103">Ottiene SKU di VMImage.</span><span class="sxs-lookup"><span data-stu-id="a98fa-103">Gets VMImage SKUs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a98fa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a98fa-104">SYNTAX</span></span>

```
Get-AzureRmVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a98fa-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a98fa-105">DESCRIPTION</span></span>
<span data-ttu-id="a98fa-106">Il cmdlet **Get-AzureRmVMImageSku** ottiene SKU VMImage.</span><span class="sxs-lookup"><span data-stu-id="a98fa-106">The **Get-AzureRmVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="a98fa-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a98fa-107">EXAMPLES</span></span>

### <span data-ttu-id="a98fa-108">Esempio 1: ottenere SKU di VMImage</span><span class="sxs-lookup"><span data-stu-id="a98fa-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzureRmVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="a98fa-109">Questo comando consente di ottenere gli SKU per l'autore e l'offerta specificati.</span><span class="sxs-lookup"><span data-stu-id="a98fa-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="a98fa-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a98fa-110">PARAMETERS</span></span>

### <span data-ttu-id="a98fa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a98fa-111">-DefaultProfile</span></span>
<span data-ttu-id="a98fa-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a98fa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a98fa-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="a98fa-113">-Location</span></span>
<span data-ttu-id="a98fa-114">Specifica la posizione di VMImage.</span><span class="sxs-lookup"><span data-stu-id="a98fa-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="a98fa-115">-Offerta</span><span class="sxs-lookup"><span data-stu-id="a98fa-115">-Offer</span></span>
<span data-ttu-id="a98fa-116">Specifica il tipo di offerta VMImage.</span><span class="sxs-lookup"><span data-stu-id="a98fa-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="a98fa-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="a98fa-117">-PublisherName</span></span>
<span data-ttu-id="a98fa-118">Specifica l'autore di un VMImage.</span><span class="sxs-lookup"><span data-stu-id="a98fa-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="a98fa-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a98fa-119">CommonParameters</span></span>
<span data-ttu-id="a98fa-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a98fa-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a98fa-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a98fa-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a98fa-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a98fa-122">INPUTS</span></span>

### <span data-ttu-id="a98fa-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a98fa-123">None</span></span>
<span data-ttu-id="a98fa-124">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="a98fa-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a98fa-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a98fa-125">OUTPUTS</span></span>

### <span data-ttu-id="a98fa-126">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineImageSku</span><span class="sxs-lookup"><span data-stu-id="a98fa-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span></span>

## <span data-ttu-id="a98fa-127">Note</span><span class="sxs-lookup"><span data-stu-id="a98fa-127">NOTES</span></span>

## <span data-ttu-id="a98fa-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a98fa-128">RELATED LINKS</span></span>

[<span data-ttu-id="a98fa-129">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="a98fa-129">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="a98fa-130">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="a98fa-130">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="a98fa-131">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="a98fa-131">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="a98fa-132">Salva-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="a98fa-132">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


