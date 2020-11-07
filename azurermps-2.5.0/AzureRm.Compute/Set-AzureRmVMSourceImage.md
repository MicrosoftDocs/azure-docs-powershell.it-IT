---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 91B2DE2F-442D-4428-8A6F-9C2CEC181CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmsourceimage
schema: 2.0.0
ms.openlocfilehash: 5e07ba8ffceb42a94c41c0b21c62329f9dbe96a7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866369"
---
# <span data-ttu-id="85242-101">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="85242-101">Set-AzureRmVMSourceImage</span></span>

## <span data-ttu-id="85242-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="85242-102">SYNOPSIS</span></span>
<span data-ttu-id="85242-103">Specifica l'immagine per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="85242-103">Specifies the image for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85242-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="85242-104">SYNTAX</span></span>

### <span data-ttu-id="85242-105">ImageReferenceSkuParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="85242-105">ImageReferenceSkuParameterSet (Default)</span></span>
```
Set-AzureRmVMSourceImage [-VM] <PSVirtualMachine> [-PublisherName] <String> [-Offer] <String> [-Skus] <String>
 [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85242-106">ImageReferenceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="85242-106">ImageReferenceIdParameterSet</span></span>
```
Set-AzureRmVMSourceImage [-VM] <PSVirtualMachine> [-Id] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="85242-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85242-107">DESCRIPTION</span></span>
<span data-ttu-id="85242-108">Il cmdlet **set-AzureRmVMSourceImage** specifica l'immagine della piattaforma da usare per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="85242-108">The **Set-AzureRmVMSourceImage** cmdlet specifies the platform image to use for a virtual machine.</span></span>

## <span data-ttu-id="85242-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="85242-109">EXAMPLES</span></span>

### <span data-ttu-id="85242-110">Esempio 1: impostare i valori per un'immagine</span><span class="sxs-lookup"><span data-stu-id="85242-110">Example 1: Set values for an image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzureRmVMSourceImage -VM $VirtualMachine -PublisherName "MicrosoftWindowsServer" -Offer "WindowsServer" -Skus "2012-R2-Datacenter" -Version "latest"
```

<span data-ttu-id="85242-111">Il primo comando ottiene il set di disponibilità denominato AvailablitySet03 nel gruppo di risorse denominato ResourceGroup11 e quindi archivia tale oggetto nella variabile $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="85242-111">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="85242-112">Il secondo comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="85242-112">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="85242-113">Il comando assegna un nome e una dimensione alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="85242-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="85242-114">La macchina virtuale appartiene al set di disponibilità archiviato in $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="85242-114">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="85242-115">Il comando Final imposta i valori per nome editore, offerta, SKU e versione.</span><span class="sxs-lookup"><span data-stu-id="85242-115">The final command sets values for publisher name, offer, SKU, and version.</span></span>
<span data-ttu-id="85242-116">I cmdlet Get- **AzureRmVMImagePublisher** , **Get-AzureRmVMImageOffer** , **Get-AzureRmVMImageSku** e **Get-AzureRmVMImage** possono individuare queste impostazioni.</span><span class="sxs-lookup"><span data-stu-id="85242-116">The **Get-AzureRmVMImagePublisher** , **Get-AzureRmVMImageOffer** , **Get-AzureRmVMImageSku** , and **Get-AzureRmVMImage** cmdlets can discover these settings.</span></span>

## <span data-ttu-id="85242-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="85242-117">PARAMETERS</span></span>

### <span data-ttu-id="85242-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85242-118">-DefaultProfile</span></span>
<span data-ttu-id="85242-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="85242-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85242-120">-ID</span><span class="sxs-lookup"><span data-stu-id="85242-120">-Id</span></span>
<span data-ttu-id="85242-121">Specifica l'ID.</span><span class="sxs-lookup"><span data-stu-id="85242-121">Specifies the ID.</span></span>

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

### <span data-ttu-id="85242-122">-Offerta</span><span class="sxs-lookup"><span data-stu-id="85242-122">-Offer</span></span>
<span data-ttu-id="85242-123">Specifica il tipo di offerta VMImage.</span><span class="sxs-lookup"><span data-stu-id="85242-123">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="85242-124">Per ottenere un'offerta di immagine, usare il cmdlet Get-AzureRmVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="85242-124">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="85242-125">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="85242-125">-PublisherName</span></span>
<span data-ttu-id="85242-126">Specifica il nome di un autore di un VMImage.</span><span class="sxs-lookup"><span data-stu-id="85242-126">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="85242-127">Per ottenere un autore, usare il cmdlet Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="85242-127">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="85242-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="85242-128">-Skus</span></span>
<span data-ttu-id="85242-129">Specifica una SKU di VMImage.</span><span class="sxs-lookup"><span data-stu-id="85242-129">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="85242-130">Per ottenere SKU, usare il cmdlet Get-AzureRmVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="85242-130">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="85242-131">-Versione</span><span class="sxs-lookup"><span data-stu-id="85242-131">-Version</span></span>
<span data-ttu-id="85242-132">Specifica una versione di VMImage.</span><span class="sxs-lookup"><span data-stu-id="85242-132">Specifies a version of a VMImage.</span></span>
<span data-ttu-id="85242-133">Per usare la versione più recente, specificare il valore più recente invece di una determinata versione.</span><span class="sxs-lookup"><span data-stu-id="85242-133">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="85242-134">-VM</span><span class="sxs-lookup"><span data-stu-id="85242-134">-VM</span></span>
<span data-ttu-id="85242-135">Specifica l'oggetto macchina virtuale locale da configurare.</span><span class="sxs-lookup"><span data-stu-id="85242-135">Specifies the local virtual machine object to configure.</span></span>

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

### <span data-ttu-id="85242-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85242-136">CommonParameters</span></span>
<span data-ttu-id="85242-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85242-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85242-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85242-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85242-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="85242-139">INPUTS</span></span>

### <span data-ttu-id="85242-140">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="85242-140">PSVirtualMachine</span></span>
<span data-ttu-id="85242-141">Il parametro ' VM ' accetta il valore di tipo ' PSVirtualMachine ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="85242-141">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="85242-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="85242-142">OUTPUTS</span></span>

### <span data-ttu-id="85242-143">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="85242-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="85242-144">Note</span><span class="sxs-lookup"><span data-stu-id="85242-144">NOTES</span></span>

## <span data-ttu-id="85242-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="85242-145">RELATED LINKS</span></span>

[<span data-ttu-id="85242-146">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="85242-146">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="85242-147">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="85242-147">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="85242-148">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="85242-148">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="85242-149">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="85242-149">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="85242-150">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="85242-150">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="85242-151">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="85242-151">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


