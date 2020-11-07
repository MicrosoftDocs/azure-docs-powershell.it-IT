---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImage.md
ms.openlocfilehash: 7b7a61c6d3043fcb4687d75ac49400b88361b81b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863745"
---
# <span data-ttu-id="38852-101">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="38852-101">Get-AzVMImage</span></span>

## <span data-ttu-id="38852-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="38852-102">SYNOPSIS</span></span>
<span data-ttu-id="38852-103">Ottiene tutte le versioni di un VMImage.</span><span class="sxs-lookup"><span data-stu-id="38852-103">Gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="38852-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="38852-104">SYNTAX</span></span>

### <span data-ttu-id="38852-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="38852-105">ListVMImage</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38852-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="38852-106">GetVMImageDetail</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38852-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="38852-107">DESCRIPTION</span></span>
<span data-ttu-id="38852-108">Il cmdlet **Get-AzVMImage** ottiene tutte le versioni di un VMImage.</span><span class="sxs-lookup"><span data-stu-id="38852-108">The **Get-AzVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="38852-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="38852-109">EXAMPLES</span></span>

### <span data-ttu-id="38852-110">Esempio 1: ottenere oggetti VMImage</span><span class="sxs-lookup"><span data-stu-id="38852-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.04-DAILY"
```

<span data-ttu-id="38852-111">Questo comando consente di ottenere tutte le versioni di VMImage che corrispondono ai valori specificati.</span><span class="sxs-lookup"><span data-stu-id="38852-111">This command gets all the versions of VMImage that match the specified values.</span></span>

## <span data-ttu-id="38852-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="38852-112">PARAMETERS</span></span>

### <span data-ttu-id="38852-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38852-113">-DefaultProfile</span></span>
<span data-ttu-id="38852-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="38852-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38852-115">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="38852-115">-FilterExpression</span></span>
<span data-ttu-id="38852-116">Specifica un'espressione di filtro.</span><span class="sxs-lookup"><span data-stu-id="38852-116">Specifies a filter expression.</span></span>

```yaml
Type: String
Parameter Sets: ListVMImage
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38852-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="38852-117">-Location</span></span>
<span data-ttu-id="38852-118">Specifica la posizione di un VMImage.</span><span class="sxs-lookup"><span data-stu-id="38852-118">Specifies the location of a VMImage.</span></span>

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

### <span data-ttu-id="38852-119">-Offerta</span><span class="sxs-lookup"><span data-stu-id="38852-119">-Offer</span></span>
<span data-ttu-id="38852-120">Specifica il tipo di offerta VMImage.</span><span class="sxs-lookup"><span data-stu-id="38852-120">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="38852-121">Per ottenere un'offerta di immagine, usare il cmdlet Get-AzVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="38852-121">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="38852-122">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="38852-122">-PublisherName</span></span>
<span data-ttu-id="38852-123">Specifica l'autore di un VMImage.</span><span class="sxs-lookup"><span data-stu-id="38852-123">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="38852-124">Per ottenere un autore di immagini, usare il cmdlet Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="38852-124">To obtain an image publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="38852-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="38852-125">-Skus</span></span>
<span data-ttu-id="38852-126">Specifica una SKU di VMImage.</span><span class="sxs-lookup"><span data-stu-id="38852-126">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="38852-127">Per ottenere un SKU, usare il cmdlet Get-AzVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="38852-127">To obtain an SKU, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="38852-128">-Versione</span><span class="sxs-lookup"><span data-stu-id="38852-128">-Version</span></span>
<span data-ttu-id="38852-129">Specifica la versione di VMImage.</span><span class="sxs-lookup"><span data-stu-id="38852-129">Specifies the version of the VMImage.</span></span>

```yaml
Type: String
Parameter Sets: GetVMImageDetail
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38852-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38852-130">CommonParameters</span></span>
<span data-ttu-id="38852-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38852-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38852-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38852-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38852-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="38852-133">INPUTS</span></span>

### <span data-ttu-id="38852-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="38852-134">None</span></span>
<span data-ttu-id="38852-135">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="38852-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="38852-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="38852-136">OUTPUTS</span></span>

### <span data-ttu-id="38852-137">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineImage</span><span class="sxs-lookup"><span data-stu-id="38852-137">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="38852-138">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineImageDetail</span><span class="sxs-lookup"><span data-stu-id="38852-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="38852-139">Note</span><span class="sxs-lookup"><span data-stu-id="38852-139">NOTES</span></span>

## <span data-ttu-id="38852-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="38852-140">RELATED LINKS</span></span>

[<span data-ttu-id="38852-141">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="38852-141">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="38852-142">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="38852-142">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="38852-143">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="38852-143">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="38852-144">Salva-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="38852-144">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


