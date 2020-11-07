---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssstorageprofile
schema: 2.0.0
ms.openlocfilehash: c96ff571ef1b82e52a313c2044a41b97d46ffa0b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866365"
---
# <span data-ttu-id="7b765-101">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="7b765-101">Set-AzureRmVmssStorageProfile</span></span>

## <span data-ttu-id="7b765-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7b765-102">SYNOPSIS</span></span>
<span data-ttu-id="7b765-103">Imposta le proprietà del profilo di archiviazione per VMSS.</span><span class="sxs-lookup"><span data-stu-id="7b765-103">Sets the storage profile properties for the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b765-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7b765-104">SYNTAX</span></span>

```
Set-AzureRmVmssStorageProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-ImageReferencePublisher] <String>] [[-ImageReferenceOffer] <String>] [[-ImageReferenceSku] <String>]
 [[-ImageReferenceVersion] <String>] [[-OsDiskName] <String>] [[-OsDiskCaching] <CachingTypes>]
 [[-OsDiskCreateOption] <DiskCreateOptionTypes>] [[-OsDiskOsType] <OperatingSystemTypes>] [[-Image] <String>]
 [[-VhdContainer] <String[]>] [-ImageReferenceId <String>] [-OsDiskWriteAccelerator]
 [-ManagedDisk <StorageAccountTypes>] [-DataDisk <VirtualMachineScaleSetDataDisk[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b765-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7b765-105">DESCRIPTION</span></span>
<span data-ttu-id="7b765-106">Il cmdlet **set-AzureRmVmssStorageProfile** imposta le proprietà del profilo di archiviazione per il set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="7b765-106">The **Set-AzureRmVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="7b765-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7b765-107">EXAMPLES</span></span>

### <span data-ttu-id="7b765-108">Esempio 1: impostare le proprietà del profilo di archiviazione per VMSS</span><span class="sxs-lookup"><span data-stu-id="7b765-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzureRmVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="7b765-109">Questo comando imposta le proprietà del profilo di archiviazione per il VMSS denominato ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="7b765-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="7b765-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7b765-110">PARAMETERS</span></span>

### <span data-ttu-id="7b765-111">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="7b765-111">-DataDisk</span></span>
<span data-ttu-id="7b765-112">Specifica l'oggetto disco dati.</span><span class="sxs-lookup"><span data-stu-id="7b765-112">Specifies the data disk object.</span></span>

```yaml
Type: VirtualMachineScaleSetDataDisk[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b765-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b765-113">-DefaultProfile</span></span>
<span data-ttu-id="7b765-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7b765-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b765-115">-Immagine</span><span class="sxs-lookup"><span data-stu-id="7b765-115">-Image</span></span>
<span data-ttu-id="7b765-116">Specifica l'URI BLOB per l'immagine utente.</span><span class="sxs-lookup"><span data-stu-id="7b765-116">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="7b765-117">VMSS crea un disco del sistema operativo nello stesso contenitore dell'immagine utente.</span><span class="sxs-lookup"><span data-stu-id="7b765-117">VMSS creates an operating system disk in the same container of the user image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b765-118">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="7b765-118">-ImageReferenceId</span></span>
<span data-ttu-id="7b765-119">Specifica l'ID riferimento immagine.</span><span class="sxs-lookup"><span data-stu-id="7b765-119">Specifies the image reference ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b765-120">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="7b765-120">-ImageReferenceOffer</span></span>
<span data-ttu-id="7b765-121">Specifica il tipo di offerta VMImage (Virtual Machine Image).</span><span class="sxs-lookup"><span data-stu-id="7b765-121">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="7b765-122">Per ottenere un'offerta di immagine, usare il cmdlet Get-AzureRmVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="7b765-122">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b765-123">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="7b765-123">-ImageReferencePublisher</span></span>
<span data-ttu-id="7b765-124">Specifica il nome di un autore di un VMImage.</span><span class="sxs-lookup"><span data-stu-id="7b765-124">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="7b765-125">Per ottenere un autore, usare il cmdlet Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="7b765-125">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b765-126">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="7b765-126">-ImageReferenceSku</span></span>
<span data-ttu-id="7b765-127">Specifica la SKU VMImage.</span><span class="sxs-lookup"><span data-stu-id="7b765-127">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="7b765-128">Per ottenere SKU, usare il cmdlet Get-AzureRmVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="7b765-128">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b765-129">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="7b765-129">-ImageReferenceVersion</span></span>
<span data-ttu-id="7b765-130">Specifica la versione di VMImage.</span><span class="sxs-lookup"><span data-stu-id="7b765-130">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="7b765-131">Per usare la versione più recente, specificare il valore più recente invece di una determinata versione.</span><span class="sxs-lookup"><span data-stu-id="7b765-131">To use the latest version, specify a value of latest instead of a particular version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b765-132">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="7b765-132">-ManagedDisk</span></span>
<span data-ttu-id="7b765-133">Specifica il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="7b765-133">Specifies the managed disk.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b765-134">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="7b765-134">-OsDiskCaching</span></span>
<span data-ttu-id="7b765-135">Specifica la modalità di memorizzazione nella cache del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="7b765-135">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="7b765-136">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="7b765-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7b765-137">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="7b765-137">ReadOnly</span></span>
- <span data-ttu-id="7b765-138">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7b765-138">ReadWrite</span></span>

<span data-ttu-id="7b765-139">Il valore predefinito è ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="7b765-139">The default value is ReadWrite.</span></span>
<span data-ttu-id="7b765-140">Se si modifica il valore di memorizzazione nella cache, il cmdlet riavvia la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7b765-140">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>

<span data-ttu-id="7b765-141">Questa impostazione influenza la coerenza e le prestazioni del disco.</span><span class="sxs-lookup"><span data-stu-id="7b765-141">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b765-142">-OsDiskCreateOption</span><span class="sxs-lookup"><span data-stu-id="7b765-142">-OsDiskCreateOption</span></span>
<span data-ttu-id="7b765-143">Specifica il modo in cui questo cmdlet crea le macchine virtuali VMSS.</span><span class="sxs-lookup"><span data-stu-id="7b765-143">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>

<span data-ttu-id="7b765-144">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="7b765-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7b765-145">Allega: questo valore viene usato quando si usa un disco specializzato per creare la macchina virtuale VMSS.</span><span class="sxs-lookup"><span data-stu-id="7b765-145">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="7b765-146">FromImage: questo valore viene usato quando si usa un'immagine per creare la macchina virtuale VMSS.</span><span class="sxs-lookup"><span data-stu-id="7b765-146">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="7b765-147">Se si usa un'immagine della piattaforma, si userà anche il parametro *imageReference* .</span><span class="sxs-lookup"><span data-stu-id="7b765-147">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

```yaml
Type: DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b765-148">-OsDiskName</span><span class="sxs-lookup"><span data-stu-id="7b765-148">-OsDiskName</span></span>
<span data-ttu-id="7b765-149">Specifica il nome del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="7b765-149">Specifies the name of the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b765-150">-OsDiskOsType</span><span class="sxs-lookup"><span data-stu-id="7b765-150">-OsDiskOsType</span></span>
<span data-ttu-id="7b765-151">Specifica il tipo di sistema operativo sul disco.</span><span class="sxs-lookup"><span data-stu-id="7b765-151">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="7b765-152">Questa operazione è necessaria solo per scenari di immagini utente e non per un'immagine della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="7b765-152">This is only needed for user image scenarios and not for a platform image.</span></span>

```yaml
Type: OperatingSystemTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Linux

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b765-153">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="7b765-153">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="7b765-154">Specifica se WriteAccelerator deve essere abilitato o disabilitato nel disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="7b765-154">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b765-155">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="7b765-155">-VhdContainer</span></span>
<span data-ttu-id="7b765-156">Specifica gli URL del contenitore usati per archiviare i dischi del sistema operativo per VMSS.</span><span class="sxs-lookup"><span data-stu-id="7b765-156">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b765-157">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="7b765-157">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="7b765-158">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="7b765-158">Specifies the VMSS object.</span></span>
<span data-ttu-id="7b765-159">Per ottenere l'oggetto, usa l'oggetto New-AzureRmVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="7b765-159">To obtain the object, use the New-AzureRmVmssConfig object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b765-160">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7b765-160">-Confirm</span></span>
<span data-ttu-id="7b765-161">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b765-161">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b765-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b765-162">-WhatIf</span></span>
<span data-ttu-id="7b765-163">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7b765-163">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7b765-164">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7b765-164">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b765-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b765-165">CommonParameters</span></span>
<span data-ttu-id="7b765-166">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b765-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b765-167">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b765-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b765-168">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7b765-168">INPUTS</span></span>

###  
<span data-ttu-id="7b765-169">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="7b765-169">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="7b765-170">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7b765-170">OUTPUTS</span></span>

### <span data-ttu-id="7b765-171">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="7b765-171">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="7b765-172">Note</span><span class="sxs-lookup"><span data-stu-id="7b765-172">NOTES</span></span>

## <span data-ttu-id="7b765-173">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7b765-173">RELATED LINKS</span></span>

[<span data-ttu-id="7b765-174">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="7b765-174">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="7b765-175">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="7b765-175">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="7b765-176">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="7b765-176">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="7b765-177">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="7b765-177">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)


