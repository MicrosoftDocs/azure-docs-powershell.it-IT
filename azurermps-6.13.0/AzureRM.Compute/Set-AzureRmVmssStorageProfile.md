---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssstorageprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssStorageProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssStorageProfile.md
ms.openlocfilehash: dc2f8633b303d15f3fe53bfc0be7eda3420e611f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687350"
---
# <span data-ttu-id="2230c-101">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="2230c-101">Set-AzureRmVmssStorageProfile</span></span>

## <span data-ttu-id="2230c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2230c-102">SYNOPSIS</span></span>
<span data-ttu-id="2230c-103">Imposta le proprietà del profilo di archiviazione per VMSS.</span><span class="sxs-lookup"><span data-stu-id="2230c-103">Sets the storage profile properties for the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2230c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2230c-104">SYNTAX</span></span>

```
Set-AzureRmVmssStorageProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-ImageReferencePublisher] <String>] [[-ImageReferenceOffer] <String>] [[-ImageReferenceSku] <String>]
 [[-ImageReferenceVersion] <String>] [[-OsDiskName] <String>] [[-OsDiskCaching] <CachingTypes>]
 [[-OsDiskCreateOption] <String>] [[-OsDiskOsType] <OperatingSystemTypes>] [[-Image] <String>]
 [[-VhdContainer] <String[]>] [-ImageReferenceId <String>] [-OsDiskWriteAccelerator]
 [-DiffDiskSetting <String>] [-ManagedDisk <String>] [-DataDisk <VirtualMachineScaleSetDataDisk[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2230c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2230c-105">DESCRIPTION</span></span>
<span data-ttu-id="2230c-106">Il cmdlet **set-AzureRmVmssStorageProfile** imposta le proprietà del profilo di archiviazione per il set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="2230c-106">The **Set-AzureRmVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="2230c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2230c-107">EXAMPLES</span></span>

### <span data-ttu-id="2230c-108">Esempio 1: impostare le proprietà del profilo di archiviazione per VMSS</span><span class="sxs-lookup"><span data-stu-id="2230c-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzureRmVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="2230c-109">Questo comando imposta le proprietà del profilo di archiviazione per il VMSS denominato ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="2230c-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="2230c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2230c-110">PARAMETERS</span></span>

### <span data-ttu-id="2230c-111">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="2230c-111">-DataDisk</span></span>
<span data-ttu-id="2230c-112">Specifica l'oggetto disco dati.</span><span class="sxs-lookup"><span data-stu-id="2230c-112">Specifies the data disk object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDisk[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2230c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2230c-113">-DefaultProfile</span></span>
<span data-ttu-id="2230c-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2230c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2230c-115">-DiffDiskSetting</span><span class="sxs-lookup"><span data-stu-id="2230c-115">-DiffDiskSetting</span></span>
<span data-ttu-id="2230c-116">Specifica le impostazioni del disco differenze per il disco di sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2230c-116">Specifies the differencing disk settings for operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2230c-117">-Immagine</span><span class="sxs-lookup"><span data-stu-id="2230c-117">-Image</span></span>
<span data-ttu-id="2230c-118">Specifica l'URI BLOB per l'immagine utente.</span><span class="sxs-lookup"><span data-stu-id="2230c-118">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="2230c-119">VMSS crea un disco del sistema operativo nello stesso contenitore dell'immagine utente.</span><span class="sxs-lookup"><span data-stu-id="2230c-119">VMSS creates an operating system disk in the same container of the user image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2230c-120">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="2230c-120">-ImageReferenceId</span></span>
<span data-ttu-id="2230c-121">Specifica l'ID riferimento immagine.</span><span class="sxs-lookup"><span data-stu-id="2230c-121">Specifies the image reference ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2230c-122">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="2230c-122">-ImageReferenceOffer</span></span>
<span data-ttu-id="2230c-123">Specifica il tipo di offerta VMImage (Virtual Machine Image).</span><span class="sxs-lookup"><span data-stu-id="2230c-123">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="2230c-124">Per ottenere un'offerta di immagine, usare il cmdlet Get-AzureRmVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="2230c-124">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2230c-125">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="2230c-125">-ImageReferencePublisher</span></span>
<span data-ttu-id="2230c-126">Specifica il nome di un autore di un VMImage.</span><span class="sxs-lookup"><span data-stu-id="2230c-126">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="2230c-127">Per ottenere un autore, usare il cmdlet Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="2230c-127">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2230c-128">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="2230c-128">-ImageReferenceSku</span></span>
<span data-ttu-id="2230c-129">Specifica la SKU VMImage.</span><span class="sxs-lookup"><span data-stu-id="2230c-129">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="2230c-130">Per ottenere SKU, usare il cmdlet Get-AzureRmVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="2230c-130">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2230c-131">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="2230c-131">-ImageReferenceVersion</span></span>
<span data-ttu-id="2230c-132">Specifica la versione di VMImage.</span><span class="sxs-lookup"><span data-stu-id="2230c-132">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="2230c-133">Per usare la versione più recente, specificare il valore più recente invece di una determinata versione.</span><span class="sxs-lookup"><span data-stu-id="2230c-133">To use the latest version, specify a value of latest instead of a particular version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2230c-134">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="2230c-134">-ManagedDisk</span></span>
<span data-ttu-id="2230c-135">Specifica il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="2230c-135">Specifies the managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2230c-136">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="2230c-136">-OsDiskCaching</span></span>
<span data-ttu-id="2230c-137">Specifica la modalità di memorizzazione nella cache del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2230c-137">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="2230c-138">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="2230c-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2230c-139">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="2230c-139">ReadOnly</span></span>
- <span data-ttu-id="2230c-140">ReadWrite il valore predefinito è ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="2230c-140">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="2230c-141">Se si modifica il valore di memorizzazione nella cache, il cmdlet riavvia la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2230c-141">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="2230c-142">Questa impostazione influenza la coerenza e le prestazioni del disco.</span><span class="sxs-lookup"><span data-stu-id="2230c-142">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2230c-143">-OsDiskCreateOption</span><span class="sxs-lookup"><span data-stu-id="2230c-143">-OsDiskCreateOption</span></span>
<span data-ttu-id="2230c-144">Specifica il modo in cui questo cmdlet crea le macchine virtuali VMSS.</span><span class="sxs-lookup"><span data-stu-id="2230c-144">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>
<span data-ttu-id="2230c-145">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="2230c-145">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2230c-146">Allega: questo valore viene usato quando si usa un disco specializzato per creare la macchina virtuale VMSS.</span><span class="sxs-lookup"><span data-stu-id="2230c-146">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="2230c-147">FromImage: questo valore viene usato quando si usa un'immagine per creare la macchina virtuale VMSS.</span><span class="sxs-lookup"><span data-stu-id="2230c-147">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="2230c-148">Se si usa un'immagine della piattaforma, si userà anche il parametro *imageReference* .</span><span class="sxs-lookup"><span data-stu-id="2230c-148">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2230c-149">-OsDiskName</span><span class="sxs-lookup"><span data-stu-id="2230c-149">-OsDiskName</span></span>
<span data-ttu-id="2230c-150">Specifica il nome del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2230c-150">Specifies the name of the operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2230c-151">-OsDiskOsType</span><span class="sxs-lookup"><span data-stu-id="2230c-151">-OsDiskOsType</span></span>
<span data-ttu-id="2230c-152">Specifica il tipo di sistema operativo sul disco.</span><span class="sxs-lookup"><span data-stu-id="2230c-152">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="2230c-153">Questa operazione è necessaria solo per scenari di immagini utente e non per un'immagine della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="2230c-153">This is only needed for user image scenarios and not for a platform image.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2230c-154">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="2230c-154">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="2230c-155">Specifica se WriteAccelerator deve essere abilitato o disabilitato nel disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2230c-155">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2230c-156">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="2230c-156">-VhdContainer</span></span>
<span data-ttu-id="2230c-157">Specifica gli URL del contenitore usati per archiviare i dischi del sistema operativo per VMSS.</span><span class="sxs-lookup"><span data-stu-id="2230c-157">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2230c-158">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2230c-158">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="2230c-159">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="2230c-159">Specifies the VMSS object.</span></span>
<span data-ttu-id="2230c-160">Per ottenere l'oggetto, usa l'oggetto New-AzureRmVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="2230c-160">To obtain the object, use the New-AzureRmVmssConfig object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2230c-161">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2230c-161">-Confirm</span></span>
<span data-ttu-id="2230c-162">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2230c-162">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2230c-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2230c-163">-WhatIf</span></span>
<span data-ttu-id="2230c-164">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2230c-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2230c-165">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2230c-165">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2230c-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2230c-166">CommonParameters</span></span>
<span data-ttu-id="2230c-167">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2230c-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2230c-168">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2230c-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2230c-169">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2230c-169">INPUTS</span></span>

### <span data-ttu-id="2230c-170">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2230c-170">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="2230c-171">System. String</span><span class="sxs-lookup"><span data-stu-id="2230c-171">System.String</span></span>

### <span data-ttu-id="2230c-172">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. CachingTypes, Microsoft. Azure. Management. Compute, Version = 21.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="2230c-172">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="2230c-173">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes, Microsoft. Azure. Management. Compute, Version = 21.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="2230c-173">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="2230c-174">System. String []</span><span class="sxs-lookup"><span data-stu-id="2230c-174">System.String[]</span></span>

### <span data-ttu-id="2230c-175">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetDataDisk []</span><span class="sxs-lookup"><span data-stu-id="2230c-175">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDisk[]</span></span>

## <span data-ttu-id="2230c-176">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2230c-176">OUTPUTS</span></span>

### <span data-ttu-id="2230c-177">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2230c-177">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="2230c-178">Note</span><span class="sxs-lookup"><span data-stu-id="2230c-178">NOTES</span></span>

## <span data-ttu-id="2230c-179">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2230c-179">RELATED LINKS</span></span>

[<span data-ttu-id="2230c-180">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="2230c-180">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="2230c-181">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="2230c-181">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="2230c-182">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="2230c-182">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="2230c-183">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="2230c-183">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)


