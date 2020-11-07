---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssstorageprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
ms.openlocfilehash: d19c039a5038c9327ea35a4f0b385e5472b748a0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863325"
---
# <span data-ttu-id="f7d6c-101">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="f7d6c-101">Set-AzVmssStorageProfile</span></span>

## <span data-ttu-id="f7d6c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f7d6c-102">SYNOPSIS</span></span>
<span data-ttu-id="f7d6c-103">Imposta le proprietà del profilo di archiviazione per VMSS.</span><span class="sxs-lookup"><span data-stu-id="f7d6c-103">Sets the storage profile properties for the VMSS.</span></span>

## <span data-ttu-id="f7d6c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f7d6c-104">SYNTAX</span></span>

```
Set-AzVmssStorageProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-ImageReferencePublisher] <String>] [[-ImageReferenceOffer] <String>] [[-ImageReferenceSku] <String>]
 [[-ImageReferenceVersion] <String>] [[-OsDiskName] <String>] [[-OsDiskCaching] <CachingTypes>]
 [[-OsDiskCreateOption] <DiskCreateOptionTypes>] [[-OsDiskOsType] <OperatingSystemTypes>] [[-Image] <String>]
 [[-VhdContainer] <String[]>] [-ImageReferenceId <String>] [-OsDiskWriteAccelerator]
 [-ManagedDisk <StorageAccountTypes>] [-DataDisk <VirtualMachineScaleSetDataDisk[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7d6c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f7d6c-105">DESCRIPTION</span></span>
<span data-ttu-id="f7d6c-106">Il cmdlet **set-AzVmssStorageProfile** imposta le proprietà del profilo di archiviazione per il set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="f7d6c-106">The **Set-AzVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="f7d6c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f7d6c-107">EXAMPLES</span></span>

### <span data-ttu-id="f7d6c-108">Esempio 1: impostare le proprietà del profilo di archiviazione per VMSS</span><span class="sxs-lookup"><span data-stu-id="f7d6c-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="f7d6c-109">Questo comando imposta le proprietà del profilo di archiviazione per il VMSS denominato ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="f7d6c-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="f7d6c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f7d6c-110">PARAMETERS</span></span>

### <span data-ttu-id="f7d6c-111">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="f7d6c-111">-DataDisk</span></span>
<span data-ttu-id="f7d6c-112">Specifica l'oggetto disco dati.</span><span class="sxs-lookup"><span data-stu-id="f7d6c-112">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="f7d6c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7d6c-113">-DefaultProfile</span></span>
<span data-ttu-id="f7d6c-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f7d6c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7d6c-115">-Immagine</span><span class="sxs-lookup"><span data-stu-id="f7d6c-115">-Image</span></span>
<span data-ttu-id="f7d6c-116">Specifica l'URI BLOB per l'immagine utente.</span><span class="sxs-lookup"><span data-stu-id="f7d6c-116">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="f7d6c-117">VMSS crea un disco del sistema operativo nello stesso contenitore dell'immagine utente.</span><span class="sxs-lookup"><span data-stu-id="f7d6c-117">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="f7d6c-118">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="f7d6c-118">-ImageReferenceId</span></span>
<span data-ttu-id="f7d6c-119">Specifica l'ID riferimento immagine.</span><span class="sxs-lookup"><span data-stu-id="f7d6c-119">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="f7d6c-120">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="f7d6c-120">-ImageReferenceOffer</span></span>
<span data-ttu-id="f7d6c-121">Specifica il tipo di offerta VMImage (Virtual Machine Image).</span><span class="sxs-lookup"><span data-stu-id="f7d6c-121">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="f7d6c-122">Per ottenere un'offerta di immagine, usare il cmdlet Get-AzVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="f7d6c-122">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="f7d6c-123">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="f7d6c-123">-ImageReferencePublisher</span></span>
<span data-ttu-id="f7d6c-124">Specifica il nome di un autore di un VMImage.</span><span class="sxs-lookup"><span data-stu-id="f7d6c-124">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="f7d6c-125">Per ottenere un autore, usare il cmdlet Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="f7d6c-125">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="f7d6c-126">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="f7d6c-126">-ImageReferenceSku</span></span>
<span data-ttu-id="f7d6c-127">Specifica la SKU VMImage.</span><span class="sxs-lookup"><span data-stu-id="f7d6c-127">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="f7d6c-128">Per ottenere SKU, usare il cmdlet Get-AzVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="f7d6c-128">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="f7d6c-129">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="f7d6c-129">-ImageReferenceVersion</span></span>
<span data-ttu-id="f7d6c-130">Specifica la versione di VMImage.</span><span class="sxs-lookup"><span data-stu-id="f7d6c-130">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="f7d6c-131">Per usare la versione più recente, specificare il valore più recente invece di una determinata versione.</span><span class="sxs-lookup"><span data-stu-id="f7d6c-131">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="f7d6c-132">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="f7d6c-132">-ManagedDisk</span></span>
<span data-ttu-id="f7d6c-133">Specifica il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="f7d6c-133">Specifies the managed disk.</span></span>

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

### <span data-ttu-id="f7d6c-134">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="f7d6c-134">-OsDiskCaching</span></span>
<span data-ttu-id="f7d6c-135">Specifica la modalità di memorizzazione nella cache del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f7d6c-135">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="f7d6c-136">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f7d6c-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f7d6c-137">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="f7d6c-137">ReadOnly</span></span>
- <span data-ttu-id="f7d6c-138">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f7d6c-138">ReadWrite</span></span>

<span data-ttu-id="f7d6c-139">Il valore predefinito è ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="f7d6c-139">The default value is ReadWrite.</span></span>
<span data-ttu-id="f7d6c-140">Se si modifica il valore di memorizzazione nella cache, il cmdlet riavvia la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f7d6c-140">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>

<span data-ttu-id="f7d6c-141">Questa impostazione influenza la coerenza e le prestazioni del disco.</span><span class="sxs-lookup"><span data-stu-id="f7d6c-141">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="f7d6c-142">-OsDiskCreateOption</span><span class="sxs-lookup"><span data-stu-id="f7d6c-142">-OsDiskCreateOption</span></span>
<span data-ttu-id="f7d6c-143">Specifica il modo in cui questo cmdlet crea le macchine virtuali VMSS.</span><span class="sxs-lookup"><span data-stu-id="f7d6c-143">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>

<span data-ttu-id="f7d6c-144">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f7d6c-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f7d6c-145">Allega: questo valore viene usato quando si usa un disco specializzato per creare la macchina virtuale VMSS.</span><span class="sxs-lookup"><span data-stu-id="f7d6c-145">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="f7d6c-146">FromImage: questo valore viene usato quando si usa un'immagine per creare la macchina virtuale VMSS.</span><span class="sxs-lookup"><span data-stu-id="f7d6c-146">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="f7d6c-147">Se si usa un'immagine della piattaforma, si userà anche il parametro *imageReference* .</span><span class="sxs-lookup"><span data-stu-id="f7d6c-147">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

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

### <span data-ttu-id="f7d6c-148">-OsDiskName</span><span class="sxs-lookup"><span data-stu-id="f7d6c-148">-OsDiskName</span></span>
<span data-ttu-id="f7d6c-149">Specifica il nome del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f7d6c-149">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="f7d6c-150">-OsDiskOsType</span><span class="sxs-lookup"><span data-stu-id="f7d6c-150">-OsDiskOsType</span></span>
<span data-ttu-id="f7d6c-151">Specifica il tipo di sistema operativo sul disco.</span><span class="sxs-lookup"><span data-stu-id="f7d6c-151">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="f7d6c-152">Questa operazione è necessaria solo per scenari di immagini utente e non per un'immagine della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="f7d6c-152">This is only needed for user image scenarios and not for a platform image.</span></span>

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

### <span data-ttu-id="f7d6c-153">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="f7d6c-153">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="f7d6c-154">Specifica se WriteAccelerator deve essere abilitato o disabilitato nel disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f7d6c-154">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="f7d6c-155">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="f7d6c-155">-VhdContainer</span></span>
<span data-ttu-id="f7d6c-156">Specifica gli URL del contenitore usati per archiviare i dischi del sistema operativo per VMSS.</span><span class="sxs-lookup"><span data-stu-id="f7d6c-156">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="f7d6c-157">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f7d6c-157">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="f7d6c-158">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="f7d6c-158">Specifies the VMSS object.</span></span>
<span data-ttu-id="f7d6c-159">Per ottenere l'oggetto, usa l'oggetto New-AzVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="f7d6c-159">To obtain the object, use the New-AzVmssConfig object.</span></span>

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

### <span data-ttu-id="f7d6c-160">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f7d6c-160">-Confirm</span></span>
<span data-ttu-id="f7d6c-161">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7d6c-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7d6c-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7d6c-162">-WhatIf</span></span>
<span data-ttu-id="f7d6c-163">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f7d6c-163">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f7d6c-164">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f7d6c-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7d6c-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7d6c-165">CommonParameters</span></span>
<span data-ttu-id="f7d6c-166">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7d6c-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7d6c-167">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7d6c-167">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7d6c-168">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f7d6c-168">INPUTS</span></span>

###  
<span data-ttu-id="f7d6c-169">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="f7d6c-169">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="f7d6c-170">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f7d6c-170">OUTPUTS</span></span>

### <span data-ttu-id="f7d6c-171">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f7d6c-171">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="f7d6c-172">Note</span><span class="sxs-lookup"><span data-stu-id="f7d6c-172">NOTES</span></span>

## <span data-ttu-id="f7d6c-173">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f7d6c-173">RELATED LINKS</span></span>

[<span data-ttu-id="f7d6c-174">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="f7d6c-174">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="f7d6c-175">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="f7d6c-175">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="f7d6c-176">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="f7d6c-176">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="f7d6c-177">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="f7d6c-177">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


