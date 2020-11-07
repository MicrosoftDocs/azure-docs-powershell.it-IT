---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimage
schema: 2.0.0
ms.openlocfilehash: c69474929fa91b2e4ae1c7f4e50d5961a9322f66
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866374"
---
# <span data-ttu-id="2474c-101">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="2474c-101">Get-AzureRmVMImage</span></span>

## <span data-ttu-id="2474c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2474c-102">SYNOPSIS</span></span>
<span data-ttu-id="2474c-103">Ottiene tutte le versioni di un VMImage.</span><span class="sxs-lookup"><span data-stu-id="2474c-103">Gets all the versions of a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2474c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2474c-104">SYNTAX</span></span>

### <span data-ttu-id="2474c-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="2474c-105">ListVMImage</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2474c-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="2474c-106">GetVMImageDetail</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2474c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2474c-107">DESCRIPTION</span></span>
<span data-ttu-id="2474c-108">Il cmdlet **Get-AzureRmVMImage** ottiene tutte le versioni di un VMImage.</span><span class="sxs-lookup"><span data-stu-id="2474c-108">The **Get-AzureRmVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="2474c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2474c-109">EXAMPLES</span></span>

### <span data-ttu-id="2474c-110">Esempio 1: ottenere oggetti VMImage</span><span class="sxs-lookup"><span data-stu-id="2474c-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzureRmVMImage -Location "Central US" -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.04-DAILY"
```

<span data-ttu-id="2474c-111">Questo comando consente di ottenere tutte le versioni di VMImage che corrispondono ai valori specificati.</span><span class="sxs-lookup"><span data-stu-id="2474c-111">This command gets all the versions of VMImage that match the specified values.</span></span>

## <span data-ttu-id="2474c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2474c-112">PARAMETERS</span></span>

### <span data-ttu-id="2474c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2474c-113">-DefaultProfile</span></span>
<span data-ttu-id="2474c-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2474c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2474c-115">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="2474c-115">-FilterExpression</span></span>
<span data-ttu-id="2474c-116">Specifica un'espressione di filtro.</span><span class="sxs-lookup"><span data-stu-id="2474c-116">Specifies a filter expression.</span></span>

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

### <span data-ttu-id="2474c-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="2474c-117">-Location</span></span>
<span data-ttu-id="2474c-118">Specifica la posizione di un VMImage.</span><span class="sxs-lookup"><span data-stu-id="2474c-118">Specifies the location of a VMImage.</span></span>

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

### <span data-ttu-id="2474c-119">-Offerta</span><span class="sxs-lookup"><span data-stu-id="2474c-119">-Offer</span></span>
<span data-ttu-id="2474c-120">Specifica il tipo di offerta VMImage.</span><span class="sxs-lookup"><span data-stu-id="2474c-120">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="2474c-121">Per ottenere un'offerta di immagine, usare il cmdlet Get-AzureRmVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="2474c-121">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="2474c-122">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="2474c-122">-PublisherName</span></span>
<span data-ttu-id="2474c-123">Specifica l'autore di un VMImage.</span><span class="sxs-lookup"><span data-stu-id="2474c-123">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="2474c-124">Per ottenere un autore di immagini, usare il cmdlet Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="2474c-124">To obtain an image publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="2474c-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="2474c-125">-Skus</span></span>
<span data-ttu-id="2474c-126">Specifica una SKU di VMImage.</span><span class="sxs-lookup"><span data-stu-id="2474c-126">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="2474c-127">Per ottenere un SKU, usare il cmdlet Get-AzureRmVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="2474c-127">To obtain an SKU, use the Get-AzureRmVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="2474c-128">-Versione</span><span class="sxs-lookup"><span data-stu-id="2474c-128">-Version</span></span>
<span data-ttu-id="2474c-129">Specifica la versione di VMImage.</span><span class="sxs-lookup"><span data-stu-id="2474c-129">Specifies the version of the VMImage.</span></span>

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

### <span data-ttu-id="2474c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2474c-130">CommonParameters</span></span>
<span data-ttu-id="2474c-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2474c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2474c-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2474c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2474c-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2474c-133">INPUTS</span></span>

### <span data-ttu-id="2474c-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2474c-134">None</span></span>
<span data-ttu-id="2474c-135">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="2474c-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2474c-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2474c-136">OUTPUTS</span></span>

### <span data-ttu-id="2474c-137">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineImage</span><span class="sxs-lookup"><span data-stu-id="2474c-137">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="2474c-138">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineImageDetail</span><span class="sxs-lookup"><span data-stu-id="2474c-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="2474c-139">Note</span><span class="sxs-lookup"><span data-stu-id="2474c-139">NOTES</span></span>

## <span data-ttu-id="2474c-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2474c-140">RELATED LINKS</span></span>

[<span data-ttu-id="2474c-141">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="2474c-141">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="2474c-142">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="2474c-142">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="2474c-143">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="2474c-143">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="2474c-144">Salva-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="2474c-144">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


