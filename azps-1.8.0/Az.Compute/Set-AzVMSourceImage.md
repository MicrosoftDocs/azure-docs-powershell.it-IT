---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 91B2DE2F-442D-4428-8A6F-9C2CEC181CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsourceimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSourceImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSourceImage.md
ms.openlocfilehash: af25c6ef380eaadef8c03ee3c7f1f7b37af77fb6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836644"
---
# <span data-ttu-id="424a3-101">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="424a3-101">Set-AzVMSourceImage</span></span>

## <span data-ttu-id="424a3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="424a3-102">SYNOPSIS</span></span>
<span data-ttu-id="424a3-103">Specifica l'immagine per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="424a3-103">Specifies the image for a virtual machine.</span></span>

## <span data-ttu-id="424a3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="424a3-104">SYNTAX</span></span>

### <span data-ttu-id="424a3-105">ImageReferenceSkuParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="424a3-105">ImageReferenceSkuParameterSet (Default)</span></span>
```
Set-AzVMSourceImage [-VM] <PSVirtualMachine> [-PublisherName] <String> [-Offer] <String> [-Skus] <String>
 [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="424a3-106">ImageReferenceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="424a3-106">ImageReferenceIdParameterSet</span></span>
```
Set-AzVMSourceImage [-VM] <PSVirtualMachine> [-Id] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="424a3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="424a3-107">DESCRIPTION</span></span>
<span data-ttu-id="424a3-108">Il cmdlet **set-AzVMSourceImage** specifica l'immagine della piattaforma da usare per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="424a3-108">The **Set-AzVMSourceImage** cmdlet specifies the platform image to use for a virtual machine.</span></span>

## <span data-ttu-id="424a3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="424a3-109">EXAMPLES</span></span>

### <span data-ttu-id="424a3-110">Esempio 1: impostare i valori per un'immagine</span><span class="sxs-lookup"><span data-stu-id="424a3-110">Example 1: Set values for an image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzVMSourceImage -VM $VirtualMachine -PublisherName "MicrosoftWindowsServer" -Offer "WindowsServer" -Skus "2012-R2-Datacenter" -Version "latest"
```

<span data-ttu-id="424a3-111">Il primo comando ottiene il set di disponibilità denominato AvailablitySet03 nel gruppo di risorse denominato ResourceGroup11 e quindi archivia tale oggetto nella variabile $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="424a3-111">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="424a3-112">Il secondo comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="424a3-112">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="424a3-113">Il comando assegna un nome e una dimensione alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="424a3-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="424a3-114">La macchina virtuale appartiene al set di disponibilità archiviato in $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="424a3-114">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="424a3-115">Il comando Final imposta i valori per nome editore, offerta, SKU e versione.</span><span class="sxs-lookup"><span data-stu-id="424a3-115">The final command sets values for publisher name, offer, SKU, and version.</span></span>
<span data-ttu-id="424a3-116">I cmdlet Get- **AzVMImagePublisher** , **Get-AzVMImageOffer** , **Get-AzVMImageSku** e **Get-AzVMImage** possono individuare queste impostazioni.</span><span class="sxs-lookup"><span data-stu-id="424a3-116">The **Get-AzVMImagePublisher** , **Get-AzVMImageOffer** , **Get-AzVMImageSku** , and **Get-AzVMImage** cmdlets can discover these settings.</span></span>

## <span data-ttu-id="424a3-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="424a3-117">PARAMETERS</span></span>

### <span data-ttu-id="424a3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="424a3-118">-DefaultProfile</span></span>
<span data-ttu-id="424a3-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="424a3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="424a3-120">-ID</span><span class="sxs-lookup"><span data-stu-id="424a3-120">-Id</span></span>
<span data-ttu-id="424a3-121">Specifica l'ID.</span><span class="sxs-lookup"><span data-stu-id="424a3-121">Specifies the ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="424a3-122">-Offerta</span><span class="sxs-lookup"><span data-stu-id="424a3-122">-Offer</span></span>
<span data-ttu-id="424a3-123">Specifica il tipo di offerta VMImage.</span><span class="sxs-lookup"><span data-stu-id="424a3-123">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="424a3-124">Per ottenere un'offerta di immagine, usare il cmdlet Get-AzVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="424a3-124">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="424a3-125">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="424a3-125">-PublisherName</span></span>
<span data-ttu-id="424a3-126">Specifica il nome di un autore di un VMImage.</span><span class="sxs-lookup"><span data-stu-id="424a3-126">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="424a3-127">Per ottenere un autore, usare il cmdlet Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="424a3-127">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="424a3-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="424a3-128">-Skus</span></span>
<span data-ttu-id="424a3-129">Specifica una SKU di VMImage.</span><span class="sxs-lookup"><span data-stu-id="424a3-129">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="424a3-130">Per ottenere SKU, usare il cmdlet Get-AzVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="424a3-130">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="424a3-131">-Versione</span><span class="sxs-lookup"><span data-stu-id="424a3-131">-Version</span></span>
<span data-ttu-id="424a3-132">Specifica una versione di VMImage.</span><span class="sxs-lookup"><span data-stu-id="424a3-132">Specifies a version of a VMImage.</span></span>
<span data-ttu-id="424a3-133">Per usare la versione più recente, specificare il valore più recente invece di una determinata versione.</span><span class="sxs-lookup"><span data-stu-id="424a3-133">To use the latest version, specify a value of latest instead of a particular version.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="424a3-134">-VM</span><span class="sxs-lookup"><span data-stu-id="424a3-134">-VM</span></span>
<span data-ttu-id="424a3-135">Specifica l'oggetto macchina virtuale locale da configurare.</span><span class="sxs-lookup"><span data-stu-id="424a3-135">Specifies the local virtual machine object to configure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="424a3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="424a3-136">CommonParameters</span></span>
<span data-ttu-id="424a3-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="424a3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="424a3-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="424a3-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="424a3-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="424a3-139">INPUTS</span></span>

### <span data-ttu-id="424a3-140">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="424a3-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="424a3-141">System. String</span><span class="sxs-lookup"><span data-stu-id="424a3-141">System.String</span></span>

## <span data-ttu-id="424a3-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="424a3-142">OUTPUTS</span></span>

### <span data-ttu-id="424a3-143">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="424a3-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="424a3-144">Note</span><span class="sxs-lookup"><span data-stu-id="424a3-144">NOTES</span></span>

## <span data-ttu-id="424a3-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="424a3-145">RELATED LINKS</span></span>

[<span data-ttu-id="424a3-146">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="424a3-146">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="424a3-147">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="424a3-147">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="424a3-148">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="424a3-148">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="424a3-149">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="424a3-149">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="424a3-150">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="424a3-150">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="424a3-151">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="424a3-151">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


