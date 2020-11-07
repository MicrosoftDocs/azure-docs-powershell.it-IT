---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzImageDataDisk.md
ms.openlocfilehash: b6c1a7e8947a079a864aae31d12aedf244ecb81b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860126"
---
# <span data-ttu-id="3f18a-101">Add-AzImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="3f18a-101">Add-AzImageDataDisk</span></span>

## <span data-ttu-id="3f18a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3f18a-102">SYNOPSIS</span></span>
<span data-ttu-id="3f18a-103">Aggiunge un disco di dati a un Obejct di immagine.</span><span class="sxs-lookup"><span data-stu-id="3f18a-103">Adds a data disk to an image obejct.</span></span>

## <span data-ttu-id="3f18a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3f18a-104">SYNTAX</span></span>

```
Add-AzImageDataDisk [-Image] <PSImage> [[-Lun] <Int32>] [[-BlobUri] <String>] [[-Caching] <CachingTypes>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <StorageAccountTypes>] [-SnapshotId <String>]
 [-ManagedDiskId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f18a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3f18a-105">DESCRIPTION</span></span>
<span data-ttu-id="3f18a-106">Il cmdlet **Add-AzImageDataDisk** aggiunge un disco di dati a un oggetto Image.</span><span class="sxs-lookup"><span data-stu-id="3f18a-106">The **Add-AzImageDataDisk** cmdlet adds a data disk to an image object.</span></span>

## <span data-ttu-id="3f18a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3f18a-107">EXAMPLES</span></span>

### <span data-ttu-id="3f18a-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3f18a-108">Example 1</span></span>
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

<span data-ttu-id="3f18a-109">Il primo comando crea un oggetto Image e lo archivia nella variabile $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="3f18a-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="3f18a-110">I tre comandi seguenti assegnano i percorsi del disco del sistema operativo e due dischi di dati alle variabili $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="3f18a-110">The next three commands assign paths of operating system disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="3f18a-111">Questo approccio è solo per la leggibilità dei comandi seguenti.</span><span class="sxs-lookup"><span data-stu-id="3f18a-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="3f18a-112">I tre comandi seguenti aggiungono un disco di sistema operativo e due dischi di dati all'immagine archiviata in $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="3f18a-112">The next three commands each adds an operating system disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="3f18a-113">L'URI di ogni disco è archiviato in $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="3f18a-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="3f18a-114">Il comando finale crea un'immagine denominata ImageName01 nel gruppo di risorse ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="3f18a-114">The final command creates an image named ImageName01 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="3f18a-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3f18a-115">PARAMETERS</span></span>

### <span data-ttu-id="3f18a-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="3f18a-116">-BlobUri</span></span>
<span data-ttu-id="3f18a-117">Specifica il collegamento, come URI, del BLOB.</span><span class="sxs-lookup"><span data-stu-id="3f18a-117">Specifies the link, as a URI, of the blob.</span></span>

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

### <span data-ttu-id="3f18a-118">-Memorizzazione nella cache</span><span class="sxs-lookup"><span data-stu-id="3f18a-118">-Caching</span></span>
<span data-ttu-id="3f18a-119">Specifica la modalità di memorizzazione nella cache del disco.</span><span class="sxs-lookup"><span data-stu-id="3f18a-119">Specifies the caching mode of the disk.</span></span>

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

### <span data-ttu-id="3f18a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f18a-120">-DefaultProfile</span></span>
<span data-ttu-id="3f18a-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3f18a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f18a-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="3f18a-122">-DiskSizeGB</span></span>
<span data-ttu-id="3f18a-123">Specifica le dimensioni del disco in gigabyte (GB).</span><span class="sxs-lookup"><span data-stu-id="3f18a-123">Specifies the size of the disk in Gigabytes (GB).</span></span>

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

### <span data-ttu-id="3f18a-124">-Immagine</span><span class="sxs-lookup"><span data-stu-id="3f18a-124">-Image</span></span>
<span data-ttu-id="3f18a-125">Specifica un oggetto Image locale.</span><span class="sxs-lookup"><span data-stu-id="3f18a-125">Specifies a local image object.</span></span>

```yaml
Type: PSImage
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f18a-126">-Lun</span><span class="sxs-lookup"><span data-stu-id="3f18a-126">-Lun</span></span>
<span data-ttu-id="3f18a-127">Specifica il numero di unità logica (LUN).</span><span class="sxs-lookup"><span data-stu-id="3f18a-127">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="3f18a-128">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="3f18a-128">-ManagedDiskId</span></span>
<span data-ttu-id="3f18a-129">Specifica l'ID di un disco gestito.</span><span class="sxs-lookup"><span data-stu-id="3f18a-129">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="3f18a-130">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="3f18a-130">-SnapshotId</span></span>
<span data-ttu-id="3f18a-131">Specifica l'ID di uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="3f18a-131">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="3f18a-132">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="3f18a-132">-StorageAccountType</span></span>
<span data-ttu-id="3f18a-133">Tipo di account di archiviazione del disco immagine dati</span><span class="sxs-lookup"><span data-stu-id="3f18a-133">The Storage Account type of the data image disk</span></span>

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

### <span data-ttu-id="3f18a-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3f18a-134">-Confirm</span></span>
<span data-ttu-id="3f18a-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f18a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f18a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f18a-136">-WhatIf</span></span>
<span data-ttu-id="3f18a-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3f18a-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3f18a-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3f18a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f18a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f18a-139">CommonParameters</span></span>
<span data-ttu-id="3f18a-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f18a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f18a-141">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f18a-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f18a-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3f18a-142">INPUTS</span></span>

### <span data-ttu-id="3f18a-143">Microsoft. Azure. Management. Compute. Models. image</span><span class="sxs-lookup"><span data-stu-id="3f18a-143">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="3f18a-144">System. Int32 System. String System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="3f18a-144">System.Int32 System.String System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="3f18a-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3f18a-145">OUTPUTS</span></span>

### <span data-ttu-id="3f18a-146">Microsoft. Azure. Management. Compute. Models. image</span><span class="sxs-lookup"><span data-stu-id="3f18a-146">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="3f18a-147">Note</span><span class="sxs-lookup"><span data-stu-id="3f18a-147">NOTES</span></span>

## <span data-ttu-id="3f18a-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3f18a-148">RELATED LINKS</span></span>

