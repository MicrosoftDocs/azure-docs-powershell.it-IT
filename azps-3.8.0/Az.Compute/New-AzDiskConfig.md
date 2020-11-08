---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
ms.openlocfilehash: 7a8c4bc3b875cb9072386784fe1c06730be89405
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019432"
---
# <span data-ttu-id="35f06-101">New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="35f06-101">New-AzDiskConfig</span></span>

## <span data-ttu-id="35f06-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="35f06-102">SYNOPSIS</span></span>
<span data-ttu-id="35f06-103">Crea un oggetto disco configurabile.</span><span class="sxs-lookup"><span data-stu-id="35f06-103">Creates a configurable disk object.</span></span>

## <span data-ttu-id="35f06-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="35f06-104">SYNTAX</span></span>

```
New-AzDiskConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-Zone <String[]>] [-HyperVGeneration <String>] [-DiskIOPSReadWrite <Int64>]
 [-DiskMBpsReadWrite <Int64>] [-DiskIOPSReadOnly <Int64>] [-DiskMBpsReadOnly <Int64>] [-MaxSharesCount <Int32>]
 [-Tag <Hashtable>] [-CreateOption <String>] [-StorageAccountId <String>]
 [-ImageReference <ImageDiskReference>] [-GalleryImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-UploadSizeInBytes <Int64>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35f06-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="35f06-105">DESCRIPTION</span></span>
<span data-ttu-id="35f06-106">Il cmdlet **New-AzDiskConfig** crea un oggetto disco configurabile.</span><span class="sxs-lookup"><span data-stu-id="35f06-106">The **New-AzDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="35f06-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="35f06-107">EXAMPLES</span></span>

### <span data-ttu-id="35f06-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="35f06-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType Standard_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="35f06-109">Il primo comando crea un oggetto disco locale vuoto con la dimensione 5GB in Standard_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="35f06-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="35f06-110">Imposta anche il tipo di sistema operativo Windows e Abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="35f06-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="35f06-111">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia del disco e della chiave di crittografia per l'oggetto disco.</span><span class="sxs-lookup"><span data-stu-id="35f06-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="35f06-112">L'ultimo comando accetta l'oggetto disk e crea un disco con il nome "Disk01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="35f06-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="35f06-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="35f06-113">Example 2</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 1023 -SkuName Standard_LRS -OsType Windows -CreateOption Upload -DiskIOPSReadWrite 500 -DiskMBpsReadWrite 8;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
PS C:\> $diskSas = Grant-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DurationInSecond 86400 -Access 'Write'
PS C:\> $disk = Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
# $disk.DiskState == 'ReadyToUpload'
PS C:\> AzCopy /Source:https://myaccount.blob.core.windows.net/mycontainer1 /Dest:$diskSas
PS C:\> $disk = Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
# $disk.DiskState == 'ActiveUpload'
PS C:\> Revoke-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="35f06-114">Il primo comando crea un oggetto disco locale per il caricamento.</span><span class="sxs-lookup"><span data-stu-id="35f06-114">The first command creates a local disk object for Upload.</span></span>
<span data-ttu-id="35f06-115">Il secondo comando accetta l'oggetto disk e crea un disco con il nome "Disk01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="35f06-115">The second command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>
<span data-ttu-id="35f06-116">Il terzo comando ottiene l'URL SAS per il disco.</span><span class="sxs-lookup"><span data-stu-id="35f06-116">The third command gets SAS Url for the disk.</span></span>
<span data-ttu-id="35f06-117">Il quarto comando ottiene lo stato del disco.</span><span class="sxs-lookup"><span data-stu-id="35f06-117">The fourth command gets the state of the disk.</span></span>
<span data-ttu-id="35f06-118">Se lo stato del disco è "ReadyToUpload", un utente può caricare un disco dallo spazio di archiviazione BLOB all'URL SAS del disco usando AzCopy.</span><span class="sxs-lookup"><span data-stu-id="35f06-118">If the disk state is 'ReadyToUpload', a user can upload a disk from blob storage to the disk SAS Url using AzCopy.</span></span>
<span data-ttu-id="35f06-119">Durante il caricamento, lo stato del disco viene modificato in "ActiveUpload".</span><span class="sxs-lookup"><span data-stu-id="35f06-119">During uploading, the disk state is changed to 'ActiveUpload'.</span></span>
<span data-ttu-id="35f06-120">L'ultimo comando revoca l'accesso al disco per l'URL SAS.</span><span class="sxs-lookup"><span data-stu-id="35f06-120">The last command revokes the disk access for the SAS Url.</span></span>

### <span data-ttu-id="35f06-121">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="35f06-121">Example 3</span></span>
```
PS C:\> $galleryImageReference = @{Id = '/subscriptions/0296790d-427c-48ca-b204-8b729bbd8670/resourceGroups/swaggertests/providers/Microsoft.Compute/galleries/swaggergallery/images/swaggerimagedef/versions/1.0.0'; Lun=1}
PS C:\> $diskConfig = New-AzDiskConfig -Location 'West US' -CreateOption 'FromImage' -GalleryImageReference $galleryImageReference;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskConfig
```

<span data-ttu-id="35f06-122">Creare un disco da una versione di immagine della raccolta condivisa.</span><span class="sxs-lookup"><span data-stu-id="35f06-122">Create a disk from a Shared Gallery Image Version.</span></span>  <span data-ttu-id="35f06-123">ID è l'ID della versione dell'immagine della raccolta condivisa.</span><span class="sxs-lookup"><span data-stu-id="35f06-123">Id is the id of the shared gallery image version.</span></span> <span data-ttu-id="35f06-124">Lun è necessario solo se l'origine è un disco dati.</span><span class="sxs-lookup"><span data-stu-id="35f06-124">Lun is needed only if the source is a data disk.</span></span>

## <span data-ttu-id="35f06-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="35f06-125">PARAMETERS</span></span>

### <span data-ttu-id="35f06-126">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="35f06-126">-CreateOption</span></span>
<span data-ttu-id="35f06-127">Specifica se questo cmdlet crea un disco nella macchina virtuale da una piattaforma o da un'immagine utente, crea un disco vuoto o allega un disco esistente.</span><span class="sxs-lookup"><span data-stu-id="35f06-127">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="35f06-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35f06-128">-DefaultProfile</span></span>
<span data-ttu-id="35f06-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="35f06-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35f06-130">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="35f06-130">-DiskEncryptionKey</span></span>
<span data-ttu-id="35f06-131">Specifica l'oggetto chiave di crittografia del disco in un disco.</span><span class="sxs-lookup"><span data-stu-id="35f06-131">Specifies the disk encryption key object on a disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35f06-132">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="35f06-132">-DiskEncryptionSetId</span></span>
<span data-ttu-id="35f06-133">Specifica l'ID risorsa del set di crittografia disco da usare per abilitare la crittografia a riposo.</span><span class="sxs-lookup"><span data-stu-id="35f06-133">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="35f06-134">-DiskIOPSReadOnly</span><span class="sxs-lookup"><span data-stu-id="35f06-134">-DiskIOPSReadOnly</span></span>
<span data-ttu-id="35f06-135">Numero totale di IOPS che saranno consentiti in tutte le VM che montano il disco condiviso come ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="35f06-135">The total number of IOPS that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="35f06-136">Un'operazione può essere trasferita tra 4K e 256K byte.</span><span class="sxs-lookup"><span data-stu-id="35f06-136">One operation can transfer between 4k and 256k bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35f06-137">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="35f06-137">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="35f06-138">Numero di IOPS consentiti per il disco; impostabile solo per i dischi UltraSSD.</span><span class="sxs-lookup"><span data-stu-id="35f06-138">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="35f06-139">Un'operazione può essere trasferita tra 4K e 256K byte.</span><span class="sxs-lookup"><span data-stu-id="35f06-139">One operation can transfer between 4k and 256k bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35f06-140">-DiskMBpsReadOnly</span><span class="sxs-lookup"><span data-stu-id="35f06-140">-DiskMBpsReadOnly</span></span>
<span data-ttu-id="35f06-141">"Descrizione": "il throughput totale (MBps) che sarà consentito in tutte le VM che monta il disco condiviso come ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="35f06-141">"description": "The total throughput (MBps) that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="35f06-142">MBps significa milioni di byte al secondo MB Usa la notazione ISO, di poteri di 10.</span><span class="sxs-lookup"><span data-stu-id="35f06-142">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35f06-143">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="35f06-143">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="35f06-144">Larghezza di banda consentita per questo disco; impostabile solo per i dischi UltraSSD.</span><span class="sxs-lookup"><span data-stu-id="35f06-144">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="35f06-145">MBps significa milioni di byte al secondo MB Usa la notazione ISO, di poteri di 10.</span><span class="sxs-lookup"><span data-stu-id="35f06-145">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35f06-146">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="35f06-146">-DiskSizeGB</span></span>
<span data-ttu-id="35f06-147">Specifica le dimensioni del disco in GB.</span><span class="sxs-lookup"><span data-stu-id="35f06-147">Specifies the size of the disk in GB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35f06-148">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="35f06-148">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="35f06-149">Abilitare le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="35f06-149">Enable encryption settings.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35f06-150">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="35f06-150">-EncryptionType</span></span>
<span data-ttu-id="35f06-151">Tipo di chiave utilizzata per crittografare i dati del disco.</span><span class="sxs-lookup"><span data-stu-id="35f06-151">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="35f06-152">I valori disponibili sono: "EncryptionAtRestWithPlatformKey", "EncryptionAtRestWithCustomerKey"</span><span class="sxs-lookup"><span data-stu-id="35f06-152">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="35f06-153">-GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="35f06-153">-GalleryImageReference</span></span>
<span data-ttu-id="35f06-154">Oggetto GalleryImageReference.</span><span class="sxs-lookup"><span data-stu-id="35f06-154">The GalleryImageReference object.</span></span>  <span data-ttu-id="35f06-155">Obbligatorio per la creazione da un'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="35f06-155">Required if creating from a Gallery Image.</span></span> <span data-ttu-id="35f06-156">L'ID sarà l'ID ARM della versione condivisa dell'immagine della cambusa da cui creare un disco.</span><span class="sxs-lookup"><span data-stu-id="35f06-156">The id will be the ARM id of the shared galley image version from which to create a disk.</span></span>
<span data-ttu-id="35f06-157">È necessario un lun se l'origine della copia è uno dei dischi di dati nell'immagine della raccolta; Se null, il disco del sistema operativo dell'immagine verrà copiato.</span><span class="sxs-lookup"><span data-stu-id="35f06-157">A lun is needed if the source of the copy is one of the data disks in the gallery image; if null, the OS disk of the image will be copied.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageDiskReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35f06-158">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="35f06-158">-HyperVGeneration</span></span>
<span data-ttu-id="35f06-159">Generazione di hypervisor della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="35f06-159">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="35f06-160">Applicabile solo ai dischi del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="35f06-160">Applicable to OS disks only.</span></span>  <span data-ttu-id="35f06-161">I valori consentiti sono V1 e V2.</span><span class="sxs-lookup"><span data-stu-id="35f06-161">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="35f06-162">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="35f06-162">-ImageReference</span></span>
<span data-ttu-id="35f06-163">Specifica il riferimento alle immagini in un disco.</span><span class="sxs-lookup"><span data-stu-id="35f06-163">Specifies the image reference on a disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageDiskReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35f06-164">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="35f06-164">-KeyEncryptionKey</span></span>
<span data-ttu-id="35f06-165">Specifica la chiave di crittografia chiave in un disco.</span><span class="sxs-lookup"><span data-stu-id="35f06-165">Specifies the Key encryption key on a disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35f06-166">-Posizione</span><span class="sxs-lookup"><span data-stu-id="35f06-166">-Location</span></span>
<span data-ttu-id="35f06-167">Specifica una posizione.</span><span class="sxs-lookup"><span data-stu-id="35f06-167">Specifies a location.</span></span>

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

### <span data-ttu-id="35f06-168">-MaxSharesCount</span><span class="sxs-lookup"><span data-stu-id="35f06-168">-MaxSharesCount</span></span>
<span data-ttu-id="35f06-169">Numero massimo di VM che possono essere allegate al disco contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="35f06-169">The maximum number of VMs that can attach to the disk at the same time.</span></span>
<span data-ttu-id="35f06-170">Il valore maggiore di uno indica un disco che può essere montato su più VM contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="35f06-170">Value greater than one indicates a disk that can be mounted on multiple VMs at the same time.</span></span>

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

### <span data-ttu-id="35f06-171">-OsType</span><span class="sxs-lookup"><span data-stu-id="35f06-171">-OsType</span></span>
<span data-ttu-id="35f06-172">Specifica il tipo di sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="35f06-172">Specifies the OS type.</span></span>

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

### <span data-ttu-id="35f06-173">-SkuName</span><span class="sxs-lookup"><span data-stu-id="35f06-173">-SkuName</span></span>
<span data-ttu-id="35f06-174">Specifica il nome SKU dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="35f06-174">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="35f06-175">I valori disponibili sono Standard_LRS, Premium_LRS, StandardSSD_LRS e UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="35f06-175">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="35f06-176">UltraSSD_LRS può essere usato solo con il valore Empty per il parametro CreateOption.</span><span class="sxs-lookup"><span data-stu-id="35f06-176">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35f06-177">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="35f06-177">-SourceResourceId</span></span>
<span data-ttu-id="35f06-178">Specifica l'ID risorsa di origine.</span><span class="sxs-lookup"><span data-stu-id="35f06-178">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="35f06-179">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="35f06-179">-SourceUri</span></span>
<span data-ttu-id="35f06-180">Specifica l'URI di origine.</span><span class="sxs-lookup"><span data-stu-id="35f06-180">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="35f06-181">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="35f06-181">-StorageAccountId</span></span>
<span data-ttu-id="35f06-182">Specifica l'ID account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="35f06-182">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="35f06-183">-Tag</span><span class="sxs-lookup"><span data-stu-id="35f06-183">-Tag</span></span>
<span data-ttu-id="35f06-184">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="35f06-184">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="35f06-185">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="35f06-185">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35f06-186">-UploadSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="35f06-186">-UploadSizeInBytes</span></span>
<span data-ttu-id="35f06-187">Specifica le dimensioni del contenuto del caricamento, incluso il piè di pagina VHD quando CreateOption è caricato.</span><span class="sxs-lookup"><span data-stu-id="35f06-187">Specifies the size of the contents of the upload including the VHD footer when CreateOption is Upload.</span></span>  <span data-ttu-id="35f06-188">Questo valore deve essere compreso tra 20972032 (20 MiB + 512 byte per il piè di pagina VHD) e 35183298347520 byte (32 TiB + 512 byte per il piè di pagina VHD).</span><span class="sxs-lookup"><span data-stu-id="35f06-188">This value should be between 20972032 (20 MiB + 512 bytes for the VHD footer) and 35183298347520 bytes (32 TiB + 512 bytes for the VHD footer).</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35f06-189">-Zona</span><span class="sxs-lookup"><span data-stu-id="35f06-189">-Zone</span></span>
<span data-ttu-id="35f06-190">Specifica l'elenco delle aree logiche per il disco.</span><span class="sxs-lookup"><span data-stu-id="35f06-190">Specifies the logical zone list for Disk.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35f06-191">-Confermare</span><span class="sxs-lookup"><span data-stu-id="35f06-191">-Confirm</span></span>
<span data-ttu-id="35f06-192">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35f06-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35f06-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35f06-193">-WhatIf</span></span>
<span data-ttu-id="35f06-194">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35f06-194">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="35f06-195">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35f06-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35f06-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35f06-196">CommonParameters</span></span>
<span data-ttu-id="35f06-197">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35f06-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35f06-198">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35f06-198">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35f06-199">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="35f06-199">INPUTS</span></span>

### <span data-ttu-id="35f06-200">System. String</span><span class="sxs-lookup"><span data-stu-id="35f06-200">System.String</span></span>

### <span data-ttu-id="35f06-201">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="35f06-201">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="35f06-202">System. Int32</span><span class="sxs-lookup"><span data-stu-id="35f06-202">System.Int32</span></span>

### <span data-ttu-id="35f06-203">System. String []</span><span class="sxs-lookup"><span data-stu-id="35f06-203">System.String[]</span></span>

### <span data-ttu-id="35f06-204">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="35f06-204">System.Collections.Hashtable</span></span>

### <span data-ttu-id="35f06-205">Microsoft. Azure. Management. Compute. Models. ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="35f06-205">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="35f06-206">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="35f06-206">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="35f06-207">Microsoft. Azure. Management. Compute. Models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="35f06-207">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="35f06-208">Microsoft. Azure. Management. Compute. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="35f06-208">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="35f06-209">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="35f06-209">OUTPUTS</span></span>

### <span data-ttu-id="35f06-210">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="35f06-210">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="35f06-211">Note</span><span class="sxs-lookup"><span data-stu-id="35f06-211">NOTES</span></span>

## <span data-ttu-id="35f06-212">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="35f06-212">RELATED LINKS</span></span>
