---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzImageDataDisk.md
ms.openlocfilehash: 0a50aa781177adb6ff457c3cc7d0a59ad8b350d0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018255"
---
# <span data-ttu-id="c1ee6-101">Add-AzImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="c1ee6-101">Add-AzImageDataDisk</span></span>

## <span data-ttu-id="c1ee6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c1ee6-102">SYNOPSIS</span></span>
<span data-ttu-id="c1ee6-103">Aggiunge un disco di dati a un oggetto Image.</span><span class="sxs-lookup"><span data-stu-id="c1ee6-103">Adds a data disk to an image object.</span></span>

## <span data-ttu-id="c1ee6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c1ee6-104">SYNTAX</span></span>

```
Add-AzImageDataDisk [-Image] <PSImage> [[-Lun] <Int32>] [[-BlobUri] <String>] [[-Caching] <CachingTypes>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <String>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c1ee6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c1ee6-105">DESCRIPTION</span></span>
<span data-ttu-id="c1ee6-106">Il cmdlet **Add-AzImageDataDisk** aggiunge un disco di dati a un oggetto Image.</span><span class="sxs-lookup"><span data-stu-id="c1ee6-106">The **Add-AzImageDataDisk** cmdlet adds a data disk to an image object.</span></span>

## <span data-ttu-id="c1ee6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c1ee6-107">EXAMPLES</span></span>

### <span data-ttu-id="c1ee6-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c1ee6-108">Example 1</span></span>
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

<span data-ttu-id="c1ee6-109">Il primo comando crea un oggetto Image e lo archivia nella variabile $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="c1ee6-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="c1ee6-110">I tre comandi seguenti assegnano i percorsi del disco del sistema operativo e due dischi di dati alle variabili $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="c1ee6-110">The next three commands assign paths of operating system disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="c1ee6-111">Questo approccio è solo per la leggibilità dei comandi seguenti.</span><span class="sxs-lookup"><span data-stu-id="c1ee6-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="c1ee6-112">I tre comandi seguenti aggiungono un disco di sistema operativo e due dischi di dati all'immagine archiviata in $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="c1ee6-112">The next three commands each adds an operating system disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="c1ee6-113">L'URI di ogni disco è archiviato in $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="c1ee6-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="c1ee6-114">Il comando finale crea un'immagine denominata ImageName01 nel gruppo di risorse ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="c1ee6-114">The final command creates an image named ImageName01 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="c1ee6-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c1ee6-115">PARAMETERS</span></span>

### <span data-ttu-id="c1ee6-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="c1ee6-116">-BlobUri</span></span>
<span data-ttu-id="c1ee6-117">Specifica il collegamento, come URI, del BLOB.</span><span class="sxs-lookup"><span data-stu-id="c1ee6-117">Specifies the link, as a URI, of the blob.</span></span>

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

### <span data-ttu-id="c1ee6-118">-Memorizzazione nella cache</span><span class="sxs-lookup"><span data-stu-id="c1ee6-118">-Caching</span></span>
<span data-ttu-id="c1ee6-119">Specifica la modalità di memorizzazione nella cache del disco.</span><span class="sxs-lookup"><span data-stu-id="c1ee6-119">Specifies the caching mode of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1ee6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1ee6-120">-DefaultProfile</span></span>
<span data-ttu-id="c1ee6-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c1ee6-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1ee6-122">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="c1ee6-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="c1ee6-123">Specifica l'ID risorsa del set di crittografia disco gestito dal cliente.</span><span class="sxs-lookup"><span data-stu-id="c1ee6-123">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="c1ee6-124">Questa operazione può essere specificata solo per il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="c1ee6-124">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="c1ee6-125">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="c1ee6-125">-DiskSizeGB</span></span>
<span data-ttu-id="c1ee6-126">Specifica le dimensioni del disco in gigabyte (GB).</span><span class="sxs-lookup"><span data-stu-id="c1ee6-126">Specifies the size of the disk in Gigabytes (GB).</span></span>

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

### <span data-ttu-id="c1ee6-127">-Immagine</span><span class="sxs-lookup"><span data-stu-id="c1ee6-127">-Image</span></span>
<span data-ttu-id="c1ee6-128">Specifica un oggetto Image locale.</span><span class="sxs-lookup"><span data-stu-id="c1ee6-128">Specifies a local image object.</span></span>

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

### <span data-ttu-id="c1ee6-129">-Lun</span><span class="sxs-lookup"><span data-stu-id="c1ee6-129">-Lun</span></span>
<span data-ttu-id="c1ee6-130">Specifica il numero di unità logica (LUN).</span><span class="sxs-lookup"><span data-stu-id="c1ee6-130">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1ee6-131">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="c1ee6-131">-ManagedDiskId</span></span>
<span data-ttu-id="c1ee6-132">Specifica l'ID di un disco gestito.</span><span class="sxs-lookup"><span data-stu-id="c1ee6-132">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="c1ee6-133">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="c1ee6-133">-SnapshotId</span></span>
<span data-ttu-id="c1ee6-134">Specifica l'ID di uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="c1ee6-134">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="c1ee6-135">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="c1ee6-135">-StorageAccountType</span></span>
<span data-ttu-id="c1ee6-136">Tipo di account di archiviazione del disco immagine dati</span><span class="sxs-lookup"><span data-stu-id="c1ee6-136">The Storage Account type of the data image disk</span></span>

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

### <span data-ttu-id="c1ee6-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c1ee6-137">-Confirm</span></span>
<span data-ttu-id="c1ee6-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1ee6-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1ee6-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1ee6-139">-WhatIf</span></span>
<span data-ttu-id="c1ee6-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c1ee6-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c1ee6-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c1ee6-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1ee6-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1ee6-142">CommonParameters</span></span>
<span data-ttu-id="c1ee6-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1ee6-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1ee6-144">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c1ee6-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1ee6-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c1ee6-145">INPUTS</span></span>

### <span data-ttu-id="c1ee6-146">Microsoft. Azure. Commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="c1ee6-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="c1ee6-147">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c1ee6-147">System.Int32</span></span>

### <span data-ttu-id="c1ee6-148">System. String</span><span class="sxs-lookup"><span data-stu-id="c1ee6-148">System.String</span></span>

### <span data-ttu-id="c1ee6-149">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. CachingTypes, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="c1ee6-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="c1ee6-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c1ee6-150">OUTPUTS</span></span>

### <span data-ttu-id="c1ee6-151">Microsoft. Azure. Commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="c1ee6-151">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="c1ee6-152">Note</span><span class="sxs-lookup"><span data-stu-id="c1ee6-152">NOTES</span></span>

## <span data-ttu-id="c1ee6-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c1ee6-153">RELATED LINKS</span></span>
