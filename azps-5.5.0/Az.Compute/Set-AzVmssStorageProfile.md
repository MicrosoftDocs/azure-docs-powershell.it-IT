---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssstorageprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
ms.openlocfilehash: 7bf5e6b765fee14ca9ba12a289d6445e063ff9df
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204683"
---
# <span data-ttu-id="dbd1f-101">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="dbd1f-101">Set-AzVmssStorageProfile</span></span>

## <span data-ttu-id="dbd1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbd1f-102">SYNOPSIS</span></span>
<span data-ttu-id="dbd1f-103">Imposta le proprietà del profilo di archiviazione per il sistema VMSS.</span><span class="sxs-lookup"><span data-stu-id="dbd1f-103">Sets the storage profile properties for the VMSS.</span></span>

## <span data-ttu-id="dbd1f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dbd1f-104">SYNTAX</span></span>

```
Set-AzVmssStorageProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-ImageReferencePublisher] <String>] [[-ImageReferenceOffer] <String>] [[-ImageReferenceSku] <String>]
 [[-ImageReferenceVersion] <String>] [[-OsDiskName] <String>] [[-OsDiskCaching] <CachingTypes>]
 [[-OsDiskCreateOption] <String>] [[-OsDiskOsType] <OperatingSystemTypes>] [[-Image] <String>]
 [[-VhdContainer] <String[]>] [-ImageReferenceId <String>] [-OsDiskWriteAccelerator]
 [-DiffDiskSetting <String>] [-ManagedDisk <String>] [-DiskEncryptionSetId <String>]
 [-DataDisk <VirtualMachineScaleSetDataDisk[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dbd1f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="dbd1f-105">DESCRIPTION</span></span>
<span data-ttu-id="dbd1f-106">Il cmdlet **Set-AzVmssStorageProfile** imposta le proprietà del profilo di archiviazione per il set di scalabilità delle macchine virtuali (VMSS).</span><span class="sxs-lookup"><span data-stu-id="dbd1f-106">The **Set-AzVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="dbd1f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dbd1f-107">EXAMPLES</span></span>

### <span data-ttu-id="dbd1f-108">Esempio 1: Impostare le proprietà del profilo di archiviazione per VMSS</span><span class="sxs-lookup"><span data-stu-id="dbd1f-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="dbd1f-109">Questo comando imposta le proprietà del profilo di archiviazione per i sistemi VMS denominati ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="dbd1f-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="dbd1f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dbd1f-110">PARAMETERS</span></span>

### <span data-ttu-id="dbd1f-111">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="dbd1f-111">-DataDisk</span></span>
<span data-ttu-id="dbd1f-112">Specifica l'oggetto disco dati.</span><span class="sxs-lookup"><span data-stu-id="dbd1f-112">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="dbd1f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbd1f-113">-DefaultProfile</span></span>
<span data-ttu-id="dbd1f-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dbd1f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbd1f-115">-DiffDiskSetting</span><span class="sxs-lookup"><span data-stu-id="dbd1f-115">-DiffDiskSetting</span></span>
<span data-ttu-id="dbd1f-116">Specifica le impostazioni disco diverse per il disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dbd1f-116">Specifies the differencing disk settings for operating system disk.</span></span>

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

### <span data-ttu-id="dbd1f-117">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="dbd1f-117">-DiskEncryptionSetId</span></span>
<span data-ttu-id="dbd1f-118">Specifica l'ID risorsa del set di crittografia del disco gestito dal cliente.</span><span class="sxs-lookup"><span data-stu-id="dbd1f-118">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="dbd1f-119">Può essere specificato solo per il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="dbd1f-119">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="dbd1f-120">-Image</span><span class="sxs-lookup"><span data-stu-id="dbd1f-120">-Image</span></span>
<span data-ttu-id="dbd1f-121">Specifica l'URI BLOB per l'immagine dell'utente.</span><span class="sxs-lookup"><span data-stu-id="dbd1f-121">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="dbd1f-122">VMSS crea un disco del sistema operativo nello stesso contenitore dell'immagine utente.</span><span class="sxs-lookup"><span data-stu-id="dbd1f-122">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="dbd1f-123">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="dbd1f-123">-ImageReferenceId</span></span>
<span data-ttu-id="dbd1f-124">Specifica l'ID di riferimento dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="dbd1f-124">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="dbd1f-125">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="dbd1f-125">-ImageReferenceOffer</span></span>
<span data-ttu-id="dbd1f-126">Specifica il tipo di offerta dell'immagine della macchina virtuale (VMImage).</span><span class="sxs-lookup"><span data-stu-id="dbd1f-126">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="dbd1f-127">Per ottenere un'offerta per l'immagine, usare Get-AzVMImageOffer cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbd1f-127">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="dbd1f-128">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="dbd1f-128">-ImageReferencePublisher</span></span>
<span data-ttu-id="dbd1f-129">Specifica il nome di un autore di un'immagine VMImage.</span><span class="sxs-lookup"><span data-stu-id="dbd1f-129">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="dbd1f-130">Per ottenere un autore, usare il cmdlet Get-AzVMImagePublisher pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="dbd1f-130">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="dbd1f-131">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="dbd1f-131">-ImageReferenceSku</span></span>
<span data-ttu-id="dbd1f-132">Specifica lo SKU VMImage.</span><span class="sxs-lookup"><span data-stu-id="dbd1f-132">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="dbd1f-133">Per ottenere SKU, usare il cmdlet Get-AzVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="dbd1f-133">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="dbd1f-134">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="dbd1f-134">-ImageReferenceVersion</span></span>
<span data-ttu-id="dbd1f-135">Specifica la versione di VMImage.</span><span class="sxs-lookup"><span data-stu-id="dbd1f-135">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="dbd1f-136">Per usare l'ultima versione, specificare un valore relativo alla versione più recente invece di una specifica versione.</span><span class="sxs-lookup"><span data-stu-id="dbd1f-136">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="dbd1f-137">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="dbd1f-137">-ManagedDisk</span></span>
<span data-ttu-id="dbd1f-138">Specifica il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="dbd1f-138">Specifies the managed disk.</span></span>

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

### <span data-ttu-id="dbd1f-139">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="dbd1f-139">-OsDiskCaching</span></span>
<span data-ttu-id="dbd1f-140">Specifica la modalità di memorizzazione nella cache del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dbd1f-140">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="dbd1f-141">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="dbd1f-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dbd1f-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="dbd1f-142">ReadOnly</span></span>
- <span data-ttu-id="dbd1f-143">ReadWrite Il valore predefinito è ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="dbd1f-143">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="dbd1f-144">Se si modifica il valore della cache, il cmdlet riavvierà la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dbd1f-144">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="dbd1f-145">Questa impostazione influisce sulla coerenza e sulle prestazioni del disco.</span><span class="sxs-lookup"><span data-stu-id="dbd1f-145">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="dbd1f-146">-OsDiskCreateOption</span><span class="sxs-lookup"><span data-stu-id="dbd1f-146">-OsDiskCreateOption</span></span>
<span data-ttu-id="dbd1f-147">Specifica in che modo questo cmdlet crea le macchine virtuali VMSS.</span><span class="sxs-lookup"><span data-stu-id="dbd1f-147">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>
<span data-ttu-id="dbd1f-148">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="dbd1f-148">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dbd1f-149">Attach: questo valore viene usato quando si usa un disco specializzato per creare la macchina virtuale VMSS.</span><span class="sxs-lookup"><span data-stu-id="dbd1f-149">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="dbd1f-150">FromImage: questo valore viene usato quando si usa un'immagine per creare la macchina virtuale VMSS.</span><span class="sxs-lookup"><span data-stu-id="dbd1f-150">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="dbd1f-151">Se si usa un'immagine della piattaforma, si userà anche il *parametro imageReference.*</span><span class="sxs-lookup"><span data-stu-id="dbd1f-151">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

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

### <span data-ttu-id="dbd1f-152">-OsDiskName</span><span class="sxs-lookup"><span data-stu-id="dbd1f-152">-OsDiskName</span></span>
<span data-ttu-id="dbd1f-153">Specifica il nome del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dbd1f-153">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="dbd1f-154">-OsDiskOsType</span><span class="sxs-lookup"><span data-stu-id="dbd1f-154">-OsDiskOsType</span></span>
<span data-ttu-id="dbd1f-155">Specifica il tipo di sistema operativo sul disco.</span><span class="sxs-lookup"><span data-stu-id="dbd1f-155">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="dbd1f-156">Questa operazione è necessaria solo per scenari con immagini utente e non per un'immagine della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="dbd1f-156">This is only needed for user image scenarios and not for a platform image.</span></span>

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

### <span data-ttu-id="dbd1f-157">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="dbd1f-157">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="dbd1f-158">Specifica se WriteAccelerator deve essere abilitato o disabilitato nel disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dbd1f-158">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="dbd1f-159">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="dbd1f-159">-VhdContainer</span></span>
<span data-ttu-id="dbd1f-160">Specifica gli URL del contenitore usati per archiviare i dischi del sistema operativo per VMSS.</span><span class="sxs-lookup"><span data-stu-id="dbd1f-160">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="dbd1f-161">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="dbd1f-161">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="dbd1f-162">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="dbd1f-162">Specifies the VMSS object.</span></span>
<span data-ttu-id="dbd1f-163">Per ottenere l'oggetto, usare l'New-AzVmssConfig o object.</span><span class="sxs-lookup"><span data-stu-id="dbd1f-163">To obtain the object, use the New-AzVmssConfig object.</span></span>

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

### <span data-ttu-id="dbd1f-164">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dbd1f-164">-Confirm</span></span>
<span data-ttu-id="dbd1f-165">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbd1f-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbd1f-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbd1f-166">-WhatIf</span></span>
<span data-ttu-id="dbd1f-167">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dbd1f-167">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dbd1f-168">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dbd1f-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbd1f-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbd1f-169">CommonParameters</span></span>
<span data-ttu-id="dbd1f-170">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbd1f-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbd1f-171">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dbd1f-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbd1f-172">INPUT</span><span class="sxs-lookup"><span data-stu-id="dbd1f-172">INPUTS</span></span>

### <span data-ttu-id="dbd1f-173">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="dbd1f-173">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="dbd1f-174">System.String</span><span class="sxs-lookup"><span data-stu-id="dbd1f-174">System.String</span></span>

### <span data-ttu-id="dbd1f-175">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="dbd1f-175">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="dbd1f-176">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="dbd1f-176">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="dbd1f-177">System.String[]</span><span class="sxs-lookup"><span data-stu-id="dbd1f-177">System.String[]</span></span>

### <span data-ttu-id="dbd1f-178">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDisk[]</span><span class="sxs-lookup"><span data-stu-id="dbd1f-178">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDisk[]</span></span>

## <span data-ttu-id="dbd1f-179">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dbd1f-179">OUTPUTS</span></span>

### <span data-ttu-id="dbd1f-180">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="dbd1f-180">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="dbd1f-181">NOTE</span><span class="sxs-lookup"><span data-stu-id="dbd1f-181">NOTES</span></span>

## <span data-ttu-id="dbd1f-182">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dbd1f-182">RELATED LINKS</span></span>

[<span data-ttu-id="dbd1f-183">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="dbd1f-183">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="dbd1f-184">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="dbd1f-184">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="dbd1f-185">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="dbd1f-185">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="dbd1f-186">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="dbd1f-186">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


