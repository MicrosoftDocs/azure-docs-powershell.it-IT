---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 91B2DE2F-442D-4428-8A6F-9C2CEC181CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsourceimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMSourceImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMSourceImage.md
ms.openlocfilehash: 88a6431d0a59c4dcd875abb0569a0280325cda18
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863350"
---
# <span data-ttu-id="2f30f-101">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="2f30f-101">Set-AzVMSourceImage</span></span>

## <span data-ttu-id="2f30f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2f30f-102">SYNOPSIS</span></span>
<span data-ttu-id="2f30f-103">Specifica l'immagine per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2f30f-103">Specifies the image for a virtual machine.</span></span>

## <span data-ttu-id="2f30f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2f30f-104">SYNTAX</span></span>

### <span data-ttu-id="2f30f-105">ImageReferenceSkuParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2f30f-105">ImageReferenceSkuParameterSet (Default)</span></span>
```
Set-AzVMSourceImage [-VM] <PSVirtualMachine> [-PublisherName] <String> [-Offer] <String> [-Skus] <String>
 [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f30f-106">ImageReferenceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f30f-106">ImageReferenceIdParameterSet</span></span>
```
Set-AzVMSourceImage [-VM] <PSVirtualMachine> [-Id] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2f30f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2f30f-107">DESCRIPTION</span></span>
<span data-ttu-id="2f30f-108">Il cmdlet **set-AzVMSourceImage** specifica l'immagine della piattaforma da usare per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2f30f-108">The **Set-AzVMSourceImage** cmdlet specifies the platform image to use for a virtual machine.</span></span>

## <span data-ttu-id="2f30f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2f30f-109">EXAMPLES</span></span>

### <span data-ttu-id="2f30f-110">Esempio 1: impostare i valori per un'immagine</span><span class="sxs-lookup"><span data-stu-id="2f30f-110">Example 1: Set values for an image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzVMSourceImage -VM $VirtualMachine -PublisherName "MicrosoftWindowsServer" -Offer "WindowsServer" -Skus "2012-R2-Datacenter" -Version "latest"
```

<span data-ttu-id="2f30f-111">Il primo comando ottiene il set di disponibilità denominato AvailablitySet03 nel gruppo di risorse denominato ResourceGroup11 e quindi archivia tale oggetto nella variabile $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="2f30f-111">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="2f30f-112">Il secondo comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="2f30f-112">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="2f30f-113">Il comando assegna un nome e una dimensione alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2f30f-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="2f30f-114">La macchina virtuale appartiene al set di disponibilità archiviato in $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="2f30f-114">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="2f30f-115">Il comando Final imposta i valori per nome editore, offerta, SKU e versione.</span><span class="sxs-lookup"><span data-stu-id="2f30f-115">The final command sets values for publisher name, offer, SKU, and version.</span></span>
<span data-ttu-id="2f30f-116">I cmdlet Get- **AzVMImagePublisher** , **Get-AzVMImageOffer** , **Get-AzVMImageSku** e **Get-AzVMImage** possono individuare queste impostazioni.</span><span class="sxs-lookup"><span data-stu-id="2f30f-116">The **Get-AzVMImagePublisher** , **Get-AzVMImageOffer** , **Get-AzVMImageSku** , and **Get-AzVMImage** cmdlets can discover these settings.</span></span>

## <span data-ttu-id="2f30f-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2f30f-117">PARAMETERS</span></span>

### <span data-ttu-id="2f30f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f30f-118">-DefaultProfile</span></span>
<span data-ttu-id="2f30f-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2f30f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f30f-120">-ID</span><span class="sxs-lookup"><span data-stu-id="2f30f-120">-Id</span></span>
<span data-ttu-id="2f30f-121">Specifica l'ID.</span><span class="sxs-lookup"><span data-stu-id="2f30f-121">Specifies the ID.</span></span>

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

### <span data-ttu-id="2f30f-122">-Offerta</span><span class="sxs-lookup"><span data-stu-id="2f30f-122">-Offer</span></span>
<span data-ttu-id="2f30f-123">Specifica il tipo di offerta VMImage.</span><span class="sxs-lookup"><span data-stu-id="2f30f-123">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="2f30f-124">Per ottenere un'offerta di immagine, usare il cmdlet Get-AzVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="2f30f-124">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="2f30f-125">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="2f30f-125">-PublisherName</span></span>
<span data-ttu-id="2f30f-126">Specifica il nome di un autore di un VMImage.</span><span class="sxs-lookup"><span data-stu-id="2f30f-126">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="2f30f-127">Per ottenere un autore, usare il cmdlet Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="2f30f-127">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="2f30f-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="2f30f-128">-Skus</span></span>
<span data-ttu-id="2f30f-129">Specifica una SKU di VMImage.</span><span class="sxs-lookup"><span data-stu-id="2f30f-129">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="2f30f-130">Per ottenere SKU, usare il cmdlet Get-AzVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="2f30f-130">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="2f30f-131">-Versione</span><span class="sxs-lookup"><span data-stu-id="2f30f-131">-Version</span></span>
<span data-ttu-id="2f30f-132">Specifica una versione di VMImage.</span><span class="sxs-lookup"><span data-stu-id="2f30f-132">Specifies a version of a VMImage.</span></span>
<span data-ttu-id="2f30f-133">Per usare la versione più recente, specificare il valore più recente invece di una determinata versione.</span><span class="sxs-lookup"><span data-stu-id="2f30f-133">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="2f30f-134">-VM</span><span class="sxs-lookup"><span data-stu-id="2f30f-134">-VM</span></span>
<span data-ttu-id="2f30f-135">Specifica l'oggetto macchina virtuale locale da configurare.</span><span class="sxs-lookup"><span data-stu-id="2f30f-135">Specifies the local virtual machine object to configure.</span></span>

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

### <span data-ttu-id="2f30f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f30f-136">CommonParameters</span></span>
<span data-ttu-id="2f30f-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f30f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f30f-138">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f30f-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f30f-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2f30f-139">INPUTS</span></span>

### <span data-ttu-id="2f30f-140">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="2f30f-140">PSVirtualMachine</span></span>
<span data-ttu-id="2f30f-141">Il parametro ' VM ' accetta il valore di tipo ' PSVirtualMachine ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="2f30f-141">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="2f30f-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2f30f-142">OUTPUTS</span></span>

### <span data-ttu-id="2f30f-143">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="2f30f-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="2f30f-144">Note</span><span class="sxs-lookup"><span data-stu-id="2f30f-144">NOTES</span></span>

## <span data-ttu-id="2f30f-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2f30f-145">RELATED LINKS</span></span>

[<span data-ttu-id="2f30f-146">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2f30f-146">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="2f30f-147">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="2f30f-147">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="2f30f-148">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="2f30f-148">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="2f30f-149">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="2f30f-149">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="2f30f-150">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="2f30f-150">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="2f30f-151">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="2f30f-151">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


