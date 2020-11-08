---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azimageosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzImageOsDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzImageOsDisk.md
ms.openlocfilehash: 45f3e8f76e6f8ff3a5684fbd8f9ebf42e7a8e252
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020830"
---
# <span data-ttu-id="c21ef-101">Set-AzImageOsDisk</span><span class="sxs-lookup"><span data-stu-id="c21ef-101">Set-AzImageOsDisk</span></span>

## <span data-ttu-id="c21ef-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c21ef-102">SYNOPSIS</span></span>
<span data-ttu-id="c21ef-103">Imposta le proprietà del disco del sistema operativo su un oggetto Image.</span><span class="sxs-lookup"><span data-stu-id="c21ef-103">Sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="c21ef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c21ef-104">SYNTAX</span></span>

```
Set-AzImageOsDisk [-Image] <PSImage> [[-OsType] <OperatingSystemTypes>]
 [[-OsState] <OperatingSystemStateTypes>] [[-BlobUri] <String>] [-Caching <CachingTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <String>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c21ef-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c21ef-105">DESCRIPTION</span></span>
<span data-ttu-id="c21ef-106">Il cmdlet **set-AzImageOsDisk** imposta le proprietà del disco del sistema operativo su un oggetto Image.</span><span class="sxs-lookup"><span data-stu-id="c21ef-106">The **Set-AzImageOsDisk** cmdlet sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="c21ef-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c21ef-107">EXAMPLES</span></span>

### <span data-ttu-id="c21ef-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c21ef-108">Example 1</span></span>
```
PS C:\> $imageConfig = New-AzImageConfig -Location 'West US';
PS C:\> $osDiskVhdUri = "https://contoso.blob.core.windows.net/test/os.vhd"
PS C:\> $dataDiskVhdUri1 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $dataDiskVhdUri2 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> Set-AzImageOsDisk -Image $imageConfig -OsType 'Windows' -OsState 'Generalized' -BlobUri $osDiskVhdUri;
PS C:\> Add-AzImageDataDisk -Image $imageConfig -Lun 1 -BlobUri $dataDiskVhdUri1;
PS C:\> Add-AzImageDataDisk -Image $imageConfig -Lun 2 -BlobUri $dataDiskVhdUri2;
PS C:\> New-AzImage -Image $imageConfig -ImageName 'ImageName01' -ResourceGroupName 'ResourceGroup01';
```

<span data-ttu-id="c21ef-109">Il primo comando crea un oggetto Image e lo archivia nella variabile $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="c21ef-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="c21ef-110">I tre comandi seguenti assegnano percorsi del disco del sistema operativo e due dischi di dati alle variabili $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="c21ef-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="c21ef-111">Questo approccio è solo per la leggibilità dei comandi seguenti.</span><span class="sxs-lookup"><span data-stu-id="c21ef-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="c21ef-112">I tre comandi seguenti aggiungono un disco del sistema operativo e due dischi di dati all'immagine archiviata in $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="c21ef-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="c21ef-113">L'URI di ogni disco è archiviato in $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="c21ef-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="c21ef-114">Il comando finale crea un'immagine denominata "ImageName01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="c21ef-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="c21ef-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c21ef-115">PARAMETERS</span></span>

### <span data-ttu-id="c21ef-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="c21ef-116">-BlobUri</span></span>
<span data-ttu-id="c21ef-117">Specifica l'URI del BLOB.</span><span class="sxs-lookup"><span data-stu-id="c21ef-117">Specifies the Uri of the blob.</span></span>

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

### <span data-ttu-id="c21ef-118">-Memorizzazione nella cache</span><span class="sxs-lookup"><span data-stu-id="c21ef-118">-Caching</span></span>
<span data-ttu-id="c21ef-119">Specifica la modalità di memorizzazione nella cache del disco.</span><span class="sxs-lookup"><span data-stu-id="c21ef-119">Specifies the caching mode of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c21ef-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c21ef-120">-DefaultProfile</span></span>
<span data-ttu-id="c21ef-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c21ef-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c21ef-122">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="c21ef-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="c21ef-123">Specifica l'ID risorsa del set di crittografia disco gestito dal cliente.</span><span class="sxs-lookup"><span data-stu-id="c21ef-123">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="c21ef-124">Questa operazione può essere specificata solo per il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="c21ef-124">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="c21ef-125">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="c21ef-125">-DiskSizeGB</span></span>
<span data-ttu-id="c21ef-126">Specifica le dimensioni del disco in GB.</span><span class="sxs-lookup"><span data-stu-id="c21ef-126">Specifies the size of the disk in GB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c21ef-127">-Immagine</span><span class="sxs-lookup"><span data-stu-id="c21ef-127">-Image</span></span>
<span data-ttu-id="c21ef-128">Specifica un oggetto Image locale.</span><span class="sxs-lookup"><span data-stu-id="c21ef-128">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c21ef-129">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="c21ef-129">-ManagedDiskId</span></span>
<span data-ttu-id="c21ef-130">Specifica l'ID di un disco gestito.</span><span class="sxs-lookup"><span data-stu-id="c21ef-130">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="c21ef-131">-OsState</span><span class="sxs-lookup"><span data-stu-id="c21ef-131">-OsState</span></span>
<span data-ttu-id="c21ef-132">Specifica lo stato del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c21ef-132">Specifies the OS state.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Generalized, Specialized

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c21ef-133">-OsType</span><span class="sxs-lookup"><span data-stu-id="c21ef-133">-OsType</span></span>
<span data-ttu-id="c21ef-134">Specifica il tipo di sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c21ef-134">Specifies the OS type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c21ef-135">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="c21ef-135">-SnapshotId</span></span>
<span data-ttu-id="c21ef-136">Specifica l'ID di uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="c21ef-136">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="c21ef-137">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="c21ef-137">-StorageAccountType</span></span>
<span data-ttu-id="c21ef-138">Tipo di account di archiviazione del disco di immagine del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="c21ef-138">The Storage Account type of Os Image Disk</span></span>

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

### <span data-ttu-id="c21ef-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c21ef-139">-Confirm</span></span>
<span data-ttu-id="c21ef-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c21ef-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c21ef-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c21ef-141">-WhatIf</span></span>
<span data-ttu-id="c21ef-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c21ef-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c21ef-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c21ef-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c21ef-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c21ef-144">CommonParameters</span></span>
<span data-ttu-id="c21ef-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c21ef-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c21ef-146">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c21ef-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c21ef-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c21ef-147">INPUTS</span></span>

### <span data-ttu-id="c21ef-148">Microsoft. Azure. Commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="c21ef-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="c21ef-149">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="c21ef-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="c21ef-150">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. OperatingSystemStateTypes, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="c21ef-150">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="c21ef-151">System. String</span><span class="sxs-lookup"><span data-stu-id="c21ef-151">System.String</span></span>

### <span data-ttu-id="c21ef-152">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. CachingTypes, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="c21ef-152">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="c21ef-153">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c21ef-153">System.Int32</span></span>

## <span data-ttu-id="c21ef-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c21ef-154">OUTPUTS</span></span>

### <span data-ttu-id="c21ef-155">Microsoft. Azure. Commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="c21ef-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="c21ef-156">Note</span><span class="sxs-lookup"><span data-stu-id="c21ef-156">NOTES</span></span>

## <span data-ttu-id="c21ef-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c21ef-157">RELATED LINKS</span></span>
