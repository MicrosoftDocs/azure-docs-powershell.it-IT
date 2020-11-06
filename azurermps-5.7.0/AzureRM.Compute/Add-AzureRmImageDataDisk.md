---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmImageDataDisk.md
ms.openlocfilehash: 13f98e0e0b34e4e192f108e20bcb6f52047b7611
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518200"
---
# <span data-ttu-id="c0fa7-101">Add-AzureRmImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="c0fa7-101">Add-AzureRmImageDataDisk</span></span>

## <span data-ttu-id="c0fa7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c0fa7-102">SYNOPSIS</span></span>
<span data-ttu-id="c0fa7-103">Aggiunge un disco di dati a un oggetto Image.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-103">Adds a data disk to an image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0fa7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c0fa7-104">SYNTAX</span></span>

```
Add-AzureRmImageDataDisk [-Image] <Image> [[-Lun] <Int32>] [[-BlobUri] <String>] [[-Caching] <CachingTypes>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <StorageAccountTypes>] [-SnapshotId <String>]
 [-ManagedDiskId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0fa7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c0fa7-105">DESCRIPTION</span></span>
<span data-ttu-id="c0fa7-106">Il cmdlet **Add-AzureRmImageDataDisk** aggiunge un disco di dati a un oggetto Image.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-106">The **Add-AzureRmImageDataDisk** cmdlet adds a data disk to an image object.</span></span>

## <span data-ttu-id="c0fa7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c0fa7-107">EXAMPLES</span></span>

### <span data-ttu-id="c0fa7-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c0fa7-108">Example 1</span></span>
```
PS C:\> $imageConfig = New-AzureRmImageConfig -Location 'West US';
PS C:\> $osDiskVhdUri = "https://contoso.blob.core.windows.net/test/os.vhd"
PS C:\> $dataDiskVhdUri1 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $dataDiskVhdUri2 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> Set-AzureRmImageOsDisk -Image $imageConfig -OsType 'Windows' -OsState 'Generalized' -BlobUri $osDiskVhdUri;
PS C:\> Add-AzureRmImageDataDisk -Image $imageConfig -Lun 1 -BlobUri $dataDiskVhdUri1;
PS C:\> Add-AzureRmImageDataDisk -Image $imageConfig -Lun 2 -BlobUri $dataDiskVhdUri2;
PS C:\> New-AzureRmImage -Image $imageConfig -ImageName 'ImageName01' -ResourceGroupName 'ResourceGroup01';
```

<span data-ttu-id="c0fa7-109">Il primo comando crea un oggetto Image e lo archivia nella variabile $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="c0fa7-110">I tre comandi seguenti assegnano i percorsi del disco del sistema operativo e due dischi di dati alle variabili $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-110">The next three commands assign paths of operating system disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="c0fa7-111">Questo approccio è solo per la leggibilità dei comandi seguenti.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="c0fa7-112">I tre comandi seguenti aggiungono un disco di sistema operativo e due dischi di dati all'immagine archiviata in $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-112">The next three commands each adds an operating system disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="c0fa7-113">L'URI di ogni disco è archiviato in $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="c0fa7-114">Il comando finale crea un'immagine denominata ImageName01 nel gruppo di risorse ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-114">The final command creates an image named ImageName01 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="c0fa7-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c0fa7-115">PARAMETERS</span></span>

### <span data-ttu-id="c0fa7-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="c0fa7-116">-BlobUri</span></span>
<span data-ttu-id="c0fa7-117">Specifica il collegamento, come URI, del BLOB.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-117">Specifies the link, as a URI, of the blob.</span></span>

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

### <span data-ttu-id="c0fa7-118">-Memorizzazione nella cache</span><span class="sxs-lookup"><span data-stu-id="c0fa7-118">-Caching</span></span>
<span data-ttu-id="c0fa7-119">Specifica la modalità di memorizzazione nella cache del disco.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-119">Specifies the caching mode of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0fa7-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="c0fa7-120">-DiskSizeGB</span></span>
<span data-ttu-id="c0fa7-121">Specifica le dimensioni del disco in gigabyte (GB).</span><span class="sxs-lookup"><span data-stu-id="c0fa7-121">Specifies the size of the disk in Gigabytes (GB).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0fa7-122">-Immagine</span><span class="sxs-lookup"><span data-stu-id="c0fa7-122">-Image</span></span>
<span data-ttu-id="c0fa7-123">Specifica un oggetto Image locale.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-123">Specifies a local image object.</span></span>

```yaml
Type: Image
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0fa7-124">-Lun</span><span class="sxs-lookup"><span data-stu-id="c0fa7-124">-Lun</span></span>
<span data-ttu-id="c0fa7-125">Specifica il numero di unità logica (LUN).</span><span class="sxs-lookup"><span data-stu-id="c0fa7-125">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0fa7-126">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="c0fa7-126">-ManagedDiskId</span></span>
<span data-ttu-id="c0fa7-127">Specifica l'ID di un disco gestito.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-127">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="c0fa7-128">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="c0fa7-128">-SnapshotId</span></span>
<span data-ttu-id="c0fa7-129">Specifica l'ID di uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-129">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="c0fa7-130">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="c0fa7-130">-StorageAccountType</span></span>
<span data-ttu-id="c0fa7-131">Tipo di account di archiviazione del disco immagine dati</span><span class="sxs-lookup"><span data-stu-id="c0fa7-131">The Storage Account type of the data image disk</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0fa7-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c0fa7-132">-Confirm</span></span>
<span data-ttu-id="c0fa7-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0fa7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0fa7-134">-WhatIf</span></span>
<span data-ttu-id="c0fa7-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c0fa7-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0fa7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0fa7-137">CommonParameters</span></span>
<span data-ttu-id="c0fa7-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0fa7-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0fa7-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0fa7-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c0fa7-140">INPUTS</span></span>

### <span data-ttu-id="c0fa7-141">Microsoft. Azure. Management. Compute. Models. image</span><span class="sxs-lookup"><span data-stu-id="c0fa7-141">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="c0fa7-142">System. Int32 System. String System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="c0fa7-142">System.Int32 System.String System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="c0fa7-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c0fa7-143">OUTPUTS</span></span>

### <span data-ttu-id="c0fa7-144">Microsoft. Azure. Management. Compute. Models. image</span><span class="sxs-lookup"><span data-stu-id="c0fa7-144">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="c0fa7-145">Note</span><span class="sxs-lookup"><span data-stu-id="c0fa7-145">NOTES</span></span>

## <span data-ttu-id="c0fa7-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c0fa7-146">RELATED LINKS</span></span>
