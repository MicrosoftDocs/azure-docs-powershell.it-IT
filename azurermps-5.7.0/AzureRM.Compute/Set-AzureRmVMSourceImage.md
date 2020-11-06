---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 91B2DE2F-442D-4428-8A6F-9C2CEC181CA7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMSourceImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMSourceImage.md
ms.openlocfilehash: d96d583f871e0d037c72018339d44952562bac35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509948"
---
# <span data-ttu-id="fecff-101">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="fecff-101">Set-AzureRmVMSourceImage</span></span>

## <span data-ttu-id="fecff-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fecff-102">SYNOPSIS</span></span>
<span data-ttu-id="fecff-103">Specifica l'immagine per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fecff-103">Specifies the image for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fecff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fecff-104">SYNTAX</span></span>

### <span data-ttu-id="fecff-105">ImageReferenceSkuParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fecff-105">ImageReferenceSkuParameterSet (Default)</span></span>
```
Set-AzureRmVMSourceImage [-VM] <PSVirtualMachine> [-PublisherName] <String> [-Offer] <String> [-Skus] <String>
 [-Version] <String> [<CommonParameters>]
```

### <span data-ttu-id="fecff-106">ImageReferenceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fecff-106">ImageReferenceIdParameterSet</span></span>
```
Set-AzureRmVMSourceImage [-VM] <PSVirtualMachine> [-Id] <String> [<CommonParameters>]
```

## <span data-ttu-id="fecff-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fecff-107">DESCRIPTION</span></span>
<span data-ttu-id="fecff-108">Il cmdlet **set-AzureRmVMSourceImage** specifica l'immagine della piattaforma da usare per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fecff-108">The **Set-AzureRmVMSourceImage** cmdlet specifies the platform image to use for a virtual machine.</span></span>

## <span data-ttu-id="fecff-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fecff-109">EXAMPLES</span></span>

### <span data-ttu-id="fecff-110">Esempio 1: impostare i valori per un'immagine</span><span class="sxs-lookup"><span data-stu-id="fecff-110">Example 1: Set values for an image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzureRmVMSourceImage -VM $VirtualMachine -PublisherName "MicrosoftWindowsServer" -Offer "WindowsServer" -Skus "2012-R2-Datacenter" -Version "latest"
```

<span data-ttu-id="fecff-111">Il primo comando ottiene il set di disponibilità denominato AvailablitySet03 nel gruppo di risorse denominato ResourceGroup11 e quindi archivia tale oggetto nella variabile $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="fecff-111">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="fecff-112">Il secondo comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="fecff-112">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="fecff-113">Il comando assegna un nome e una dimensione alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fecff-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="fecff-114">La macchina virtuale appartiene al set di disponibilità archiviato in $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="fecff-114">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="fecff-115">Il comando Final imposta i valori per nome editore, offerta, SKU e versione.</span><span class="sxs-lookup"><span data-stu-id="fecff-115">The final command sets values for publisher name, offer, SKU, and version.</span></span>
<span data-ttu-id="fecff-116">I cmdlet Get- **AzureRmVMImagePublisher** , **Get-AzureRmVMImageOffer** , **Get-AzureRmVMImageSku** e **Get-AzureRmVMImage** possono individuare queste impostazioni.</span><span class="sxs-lookup"><span data-stu-id="fecff-116">The **Get-AzureRmVMImagePublisher** , **Get-AzureRmVMImageOffer** , **Get-AzureRmVMImageSku** , and **Get-AzureRmVMImage** cmdlets can discover these settings.</span></span>

## <span data-ttu-id="fecff-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fecff-117">PARAMETERS</span></span>

### <span data-ttu-id="fecff-118">-ID</span><span class="sxs-lookup"><span data-stu-id="fecff-118">-Id</span></span>
<span data-ttu-id="fecff-119">Specifica l'ID.</span><span class="sxs-lookup"><span data-stu-id="fecff-119">Specifies the ID.</span></span>

```yaml
Type: String
Parameter Sets: ImageReferenceIdParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fecff-120">-Offerta</span><span class="sxs-lookup"><span data-stu-id="fecff-120">-Offer</span></span>
<span data-ttu-id="fecff-121">Specifica il tipo di offerta VMImage.</span><span class="sxs-lookup"><span data-stu-id="fecff-121">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="fecff-122">Per ottenere un'offerta di immagine, usare il cmdlet Get-AzureRmVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="fecff-122">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fecff-123">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="fecff-123">-PublisherName</span></span>
<span data-ttu-id="fecff-124">Specifica il nome di un autore di un VMImage.</span><span class="sxs-lookup"><span data-stu-id="fecff-124">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="fecff-125">Per ottenere un autore, usare il cmdlet Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="fecff-125">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fecff-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="fecff-126">-Skus</span></span>
<span data-ttu-id="fecff-127">Specifica una SKU di VMImage.</span><span class="sxs-lookup"><span data-stu-id="fecff-127">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="fecff-128">Per ottenere SKU, usare il cmdlet Get-AzureRmVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="fecff-128">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fecff-129">-Versione</span><span class="sxs-lookup"><span data-stu-id="fecff-129">-Version</span></span>
<span data-ttu-id="fecff-130">Specifica una versione di VMImage.</span><span class="sxs-lookup"><span data-stu-id="fecff-130">Specifies a version of a VMImage.</span></span>
<span data-ttu-id="fecff-131">Per usare la versione più recente, specificare il valore più recente invece di una determinata versione.</span><span class="sxs-lookup"><span data-stu-id="fecff-131">To use the latest version, specify a value of latest instead of a particular version.</span></span>

```yaml
Type: String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fecff-132">-VM</span><span class="sxs-lookup"><span data-stu-id="fecff-132">-VM</span></span>
<span data-ttu-id="fecff-133">Specifica l'oggetto macchina virtuale locale da configurare.</span><span class="sxs-lookup"><span data-stu-id="fecff-133">Specifies the local virtual machine object to configure.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fecff-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fecff-134">CommonParameters</span></span>
<span data-ttu-id="fecff-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fecff-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fecff-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fecff-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fecff-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fecff-137">INPUTS</span></span>

### <span data-ttu-id="fecff-138">Nessuno</span><span class="sxs-lookup"><span data-stu-id="fecff-138">None</span></span>
<span data-ttu-id="fecff-139">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="fecff-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fecff-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fecff-140">OUTPUTS</span></span>

## <span data-ttu-id="fecff-141">Note</span><span class="sxs-lookup"><span data-stu-id="fecff-141">NOTES</span></span>

## <span data-ttu-id="fecff-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fecff-142">RELATED LINKS</span></span>

[<span data-ttu-id="fecff-143">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="fecff-143">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="fecff-144">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="fecff-144">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="fecff-145">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="fecff-145">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="fecff-146">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="fecff-146">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="fecff-147">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="fecff-147">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="fecff-148">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="fecff-148">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


