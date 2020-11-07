---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azimageosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzImageOsDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzImageOsDisk.md
ms.openlocfilehash: 5bc92ea5aa49cb97be457fd937c7b9deb492bb0e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863438"
---
# <span data-ttu-id="71632-101">Set-AzImageOsDisk</span><span class="sxs-lookup"><span data-stu-id="71632-101">Set-AzImageOsDisk</span></span>

## <span data-ttu-id="71632-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="71632-102">SYNOPSIS</span></span>
<span data-ttu-id="71632-103">Imposta le proprietà del disco del sistema operativo su un oggetto Image.</span><span class="sxs-lookup"><span data-stu-id="71632-103">Sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="71632-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="71632-104">SYNTAX</span></span>

```
Set-AzImageOsDisk [-Image] <PSImage> [[-OsType] <OperatingSystemTypes>]
 [[-OsState] <OperatingSystemStateTypes>] [[-BlobUri] <String>] [-Caching <CachingTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <StorageAccountTypes>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71632-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71632-105">DESCRIPTION</span></span>
<span data-ttu-id="71632-106">Il cmdlet **set-AzImageOsDisk** imposta le proprietà del disco del sistema operativo su un oggetto Image.</span><span class="sxs-lookup"><span data-stu-id="71632-106">The **Set-AzImageOsDisk** cmdlet sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="71632-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="71632-107">EXAMPLES</span></span>

### <span data-ttu-id="71632-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="71632-108">Example 1</span></span>
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

<span data-ttu-id="71632-109">Il primo comando crea un oggetto Image e lo archivia nella variabile $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="71632-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="71632-110">I tre comandi seguenti assegnano percorsi del disco del sistema operativo e due dischi di dati alle variabili $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="71632-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="71632-111">Questo approccio è solo per la leggibilità dei comandi seguenti.</span><span class="sxs-lookup"><span data-stu-id="71632-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="71632-112">I tre comandi seguenti aggiungono un disco del sistema operativo e due dischi di dati all'immagine archiviata in $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="71632-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="71632-113">L'URI di ogni disco è archiviato in $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="71632-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="71632-114">Il comando finale crea un'immagine denominata "ImageName01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="71632-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="71632-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="71632-115">PARAMETERS</span></span>

### <span data-ttu-id="71632-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="71632-116">-BlobUri</span></span>
<span data-ttu-id="71632-117">Specifica l'URI del BLOB.</span><span class="sxs-lookup"><span data-stu-id="71632-117">Specifies the Uri of the blob.</span></span>

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

### <span data-ttu-id="71632-118">-Memorizzazione nella cache</span><span class="sxs-lookup"><span data-stu-id="71632-118">-Caching</span></span>
<span data-ttu-id="71632-119">Specifica la modalità di memorizzazione nella cache del disco.</span><span class="sxs-lookup"><span data-stu-id="71632-119">Specifies the caching mode of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71632-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71632-120">-DefaultProfile</span></span>
<span data-ttu-id="71632-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="71632-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71632-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="71632-122">-DiskSizeGB</span></span>
<span data-ttu-id="71632-123">Specifica le dimensioni del disco in GB.</span><span class="sxs-lookup"><span data-stu-id="71632-123">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="71632-124">-Immagine</span><span class="sxs-lookup"><span data-stu-id="71632-124">-Image</span></span>
<span data-ttu-id="71632-125">Specifica un oggetto Image locale.</span><span class="sxs-lookup"><span data-stu-id="71632-125">Specifies a local image object.</span></span>

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

### <span data-ttu-id="71632-126">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="71632-126">-ManagedDiskId</span></span>
<span data-ttu-id="71632-127">Specifica l'ID di un disco gestito.</span><span class="sxs-lookup"><span data-stu-id="71632-127">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="71632-128">-OsState</span><span class="sxs-lookup"><span data-stu-id="71632-128">-OsState</span></span>
<span data-ttu-id="71632-129">Specifica lo stato del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="71632-129">Specifies the OS state.</span></span>

```yaml
Type: OperatingSystemStateTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Generalized, Specialized

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71632-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="71632-130">-OsType</span></span>
<span data-ttu-id="71632-131">Specifica il tipo di sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="71632-131">Specifies the OS type.</span></span>

```yaml
Type: OperatingSystemTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71632-132">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="71632-132">-SnapshotId</span></span>
<span data-ttu-id="71632-133">Specifica l'ID di uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="71632-133">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="71632-134">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="71632-134">-StorageAccountType</span></span>
<span data-ttu-id="71632-135">Tipo di account di archiviazione del disco di immagine del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="71632-135">The Storage Account type of Os Image Disk</span></span>

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

### <span data-ttu-id="71632-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="71632-136">-Confirm</span></span>
<span data-ttu-id="71632-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71632-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71632-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71632-138">-WhatIf</span></span>
<span data-ttu-id="71632-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="71632-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="71632-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="71632-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71632-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71632-141">CommonParameters</span></span>
<span data-ttu-id="71632-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71632-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71632-143">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71632-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71632-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="71632-144">INPUTS</span></span>

### <span data-ttu-id="71632-145">Microsoft. Azure. Management. Compute. Models. image</span><span class="sxs-lookup"><span data-stu-id="71632-145">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="71632-146">System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[Microsoft. Azure. Management. Compute. Models. OperatingSystemStateTypes, Microsoft. Azure. Management. Compute, Version = 14.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]] System. String System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="71632-146">System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] System.String System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="71632-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="71632-147">OUTPUTS</span></span>

### <span data-ttu-id="71632-148">Microsoft. Azure. Management. Compute. Models. image</span><span class="sxs-lookup"><span data-stu-id="71632-148">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="71632-149">Note</span><span class="sxs-lookup"><span data-stu-id="71632-149">NOTES</span></span>

## <span data-ttu-id="71632-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="71632-150">RELATED LINKS</span></span>

