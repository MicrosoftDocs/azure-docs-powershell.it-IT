---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
ms.openlocfilehash: 34caab92645f610ed6ed71d907639060cf0c456a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957614"
---
# <span data-ttu-id="92ed1-101">New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="92ed1-101">New-AzDiskConfig</span></span>

## <span data-ttu-id="92ed1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92ed1-102">SYNOPSIS</span></span>
<span data-ttu-id="92ed1-103">Crea un oggetto disco configurabile.</span><span class="sxs-lookup"><span data-stu-id="92ed1-103">Creates a configurable disk object.</span></span>

## <span data-ttu-id="92ed1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="92ed1-104">SYNTAX</span></span>

```
New-AzDiskConfig [[-SkuName] <String>] [-Tier <String>] [-LogicalSectorSize <Int32>]
 [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>] [[-Location] <String>]
 [-Zone <String[]>] [-HyperVGeneration <String>] [-DiskIOPSReadWrite <Int64>] [-DiskMBpsReadWrite <Int64>]
 [-DiskIOPSReadOnly <Int64>] [-DiskMBpsReadOnly <Int64>] [-MaxSharesCount <Int32>] [-Tag <Hashtable>]
 [-CreateOption <String>] [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>]
 [-GalleryImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-UploadSizeInBytes <Int64>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [-DiskAccessId <String>]
 [-NetworkAccessPolicy <String>] [-BurstingEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="92ed1-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="92ed1-105">DESCRIPTION</span></span>
<span data-ttu-id="92ed1-106">Il cmdlet **New-AzDiskConfig** crea un oggetto disco configurabile.</span><span class="sxs-lookup"><span data-stu-id="92ed1-106">The **New-AzDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="92ed1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="92ed1-107">EXAMPLES</span></span>

### <span data-ttu-id="92ed1-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="92ed1-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -SkuName Standard_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="92ed1-109">Il primo comando crea un oggetto disco vuoto locale con dimensioni di 5 GB Standard_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="92ed1-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="92ed1-110">Configura anche il tipo di sistema operativo Windows e abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="92ed1-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="92ed1-111">Il secondo e il terzo comando impostano la chiave di crittografia disco e le relative impostazioni per l'oggetto disco.</span><span class="sxs-lookup"><span data-stu-id="92ed1-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="92ed1-112">L'ultimo comando accetta l'oggetto disco e crea un disco con il nome 'Disk01' nel gruppo di risorse 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="92ed1-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="92ed1-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="92ed1-113">Example 2</span></span>
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

<span data-ttu-id="92ed1-114">Il primo comando crea un oggetto disco locale per Carica.</span><span class="sxs-lookup"><span data-stu-id="92ed1-114">The first command creates a local disk object for Upload.</span></span>
<span data-ttu-id="92ed1-115">Il secondo comando accetta l'oggetto disco e crea un disco con il nome 'Disk01' nel gruppo di risorse 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="92ed1-115">The second command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>
<span data-ttu-id="92ed1-116">Il terzo comando ottiene l'URL della firma di accesso condiviso per il disco.</span><span class="sxs-lookup"><span data-stu-id="92ed1-116">The third command gets SAS Url for the disk.</span></span>
<span data-ttu-id="92ed1-117">Il quarto comando ottiene lo stato del disco.</span><span class="sxs-lookup"><span data-stu-id="92ed1-117">The fourth command gets the state of the disk.</span></span>
<span data-ttu-id="92ed1-118">Se lo stato del disco è "ReadyToUpload", un utente può caricare un disco dall'archiviazione BLOB all'URL della firma di accesso condiviso del disco con AzCopy.</span><span class="sxs-lookup"><span data-stu-id="92ed1-118">If the disk state is 'ReadyToUpload', a user can upload a disk from blob storage to the disk SAS Url using AzCopy.</span></span>
<span data-ttu-id="92ed1-119">Durante il caricamento, lo stato del disco viene modificato in "ActiveUpload".</span><span class="sxs-lookup"><span data-stu-id="92ed1-119">During uploading, the disk state is changed to 'ActiveUpload'.</span></span>
<span data-ttu-id="92ed1-120">L'ultimo comando revoca l'accesso al disco per l'URL di firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="92ed1-120">The last command revokes the disk access for the SAS Url.</span></span>

### <span data-ttu-id="92ed1-121">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="92ed1-121">Example 3</span></span>
```
PS C:\> $galleryImageReference = @{Id = '/subscriptions/0296790d-427c-48ca-b204-8b729bbd8670/resourceGroups/swaggertests/providers/Microsoft.Compute/galleries/swaggergallery/images/swaggerimagedef/versions/1.0.0'; Lun=1}
PS C:\> $diskConfig = New-AzDiskConfig -Location 'West US' -CreateOption 'FromImage' -GalleryImageReference $galleryImageReference;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskConfig
```

<span data-ttu-id="92ed1-122">Creare un disco da una versione immagine raccolta condivisa.</span><span class="sxs-lookup"><span data-stu-id="92ed1-122">Create a disk from a Shared Gallery Image Version.</span></span>  <span data-ttu-id="92ed1-123">ID è l'ID della versione dell'immagine della raccolta condivisa.</span><span class="sxs-lookup"><span data-stu-id="92ed1-123">Id is the id of the shared gallery image version.</span></span> <span data-ttu-id="92ed1-124">Lun è necessario solo se l'origine è un disco dati.</span><span class="sxs-lookup"><span data-stu-id="92ed1-124">Lun is needed only if the source is a data disk.</span></span>

## <span data-ttu-id="92ed1-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92ed1-125">PARAMETERS</span></span>

### <span data-ttu-id="92ed1-126">-BurstingEnabled</span><span class="sxs-lookup"><span data-stu-id="92ed1-126">-BurstingEnabled</span></span>
<span data-ttu-id="92ed1-127">Abilita lo scatto a raffica oltre la destinazione delle prestazioni di provisioning del disco.</span><span class="sxs-lookup"><span data-stu-id="92ed1-127">Enables bursting beyond the provisioned performance target of the disk.</span></span> <span data-ttu-id="92ed1-128">Per impostazione predefinita, lo scatto a scatto a scatto è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="92ed1-128">Bursting is disabled by default.</span></span> <span data-ttu-id="92ed1-129">Non si applica ai dischi Ultra.</span><span class="sxs-lookup"><span data-stu-id="92ed1-129">Does not apply to Ultra disks.</span></span>

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

### <span data-ttu-id="92ed1-130">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="92ed1-130">-CreateOption</span></span>
<span data-ttu-id="92ed1-131">Specifica se questo cmdlet crea un disco nella macchina virtuale da una piattaforma o un'immagine utente, crea un disco vuoto o collega un disco esistente.</span><span class="sxs-lookup"><span data-stu-id="92ed1-131">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="92ed1-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92ed1-132">-DefaultProfile</span></span>
<span data-ttu-id="92ed1-133">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="92ed1-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92ed1-134">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="92ed1-134">-DiskAccessId</span></span>
<span data-ttu-id="92ed1-135">Ottiene o imposta ARM ID della risorsa DiskAccess per l'uso di endpoint privati.</span><span class="sxs-lookup"><span data-stu-id="92ed1-135">Gets or sets ARM ID of the DiskAccess resource for using private endpoints on.</span></span>


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

### <span data-ttu-id="92ed1-136">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="92ed1-136">-DiskEncryptionKey</span></span>
<span data-ttu-id="92ed1-137">Specifica l'oggetto chiave di crittografia disco su un disco.</span><span class="sxs-lookup"><span data-stu-id="92ed1-137">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="92ed1-138">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="92ed1-138">-DiskEncryptionSetId</span></span>
<span data-ttu-id="92ed1-139">Specifica l'ID risorsa del set di crittografia del disco da usare per l'abilitazione della crittografia in fase di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="92ed1-139">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="92ed1-140">-DiskIOPSReadOnly</span><span class="sxs-lookup"><span data-stu-id="92ed1-140">-DiskIOPSReadOnly</span></span>
<span data-ttu-id="92ed1-141">Numero totale di operazioni di I/O al secondo consentite in tutte le macchine virtuali che montaggio il disco condiviso in sola lettura.</span><span class="sxs-lookup"><span data-stu-id="92ed1-141">The total number of IOPS that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="92ed1-142">È possibile trasferire un'operazione tra 4.000 e 256.000 byte.</span><span class="sxs-lookup"><span data-stu-id="92ed1-142">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="92ed1-143">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="92ed1-143">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="92ed1-144">Il numero di operazioni di I/O al secondo consentite per il disco; impostabile solo per dischi UltraSSD.</span><span class="sxs-lookup"><span data-stu-id="92ed1-144">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="92ed1-145">È possibile trasferire un'operazione tra 4.000 e 256.000 byte.</span><span class="sxs-lookup"><span data-stu-id="92ed1-145">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="92ed1-146">-DiskMBpsReadOnly</span><span class="sxs-lookup"><span data-stu-id="92ed1-146">-DiskMBpsReadOnly</span></span>
<span data-ttu-id="92ed1-147">"descrizione": "Velocità effettiva totale (MBps) consentita in tutte le macchine virtuali che montaggio il disco condiviso come ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="92ed1-147">"description": "The total throughput (MBps) that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="92ed1-148">MBps significa milioni di byte al secondo - MB usa la notazione ISO, ovvero potenze di 10.</span><span class="sxs-lookup"><span data-stu-id="92ed1-148">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="92ed1-149">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="92ed1-149">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="92ed1-150">La larghezza di banda consentita per il disco; impostabile solo per dischi UltraSSD.</span><span class="sxs-lookup"><span data-stu-id="92ed1-150">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="92ed1-151">MBps significa milioni di byte al secondo - MB usa la notazione ISO, ovvero potenze di 10.</span><span class="sxs-lookup"><span data-stu-id="92ed1-151">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="92ed1-152">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="92ed1-152">-DiskSizeGB</span></span>
<span data-ttu-id="92ed1-153">Specifica le dimensioni del disco in GB.</span><span class="sxs-lookup"><span data-stu-id="92ed1-153">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="92ed1-154">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="92ed1-154">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="92ed1-155">Abilitare le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="92ed1-155">Enable encryption settings.</span></span>

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

### <span data-ttu-id="92ed1-156">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="92ed1-156">-EncryptionType</span></span>
<span data-ttu-id="92ed1-157">Tipo di chiave usata per crittografare i dati del disco.</span><span class="sxs-lookup"><span data-stu-id="92ed1-157">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="92ed1-158">I valori disponibili sono: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span><span class="sxs-lookup"><span data-stu-id="92ed1-158">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="92ed1-159">-GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="92ed1-159">-GalleryImageReference</span></span>
<span data-ttu-id="92ed1-160">Oggetto GalleryImageReference.</span><span class="sxs-lookup"><span data-stu-id="92ed1-160">The GalleryImageReference object.</span></span>  <span data-ttu-id="92ed1-161">Obbligatorio se si crea da un'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="92ed1-161">Required if creating from a Gallery Image.</span></span> <span data-ttu-id="92ed1-162">L'ID sarà l ARM ID della versione dell'immagine galley condivisa da cui creare un disco.</span><span class="sxs-lookup"><span data-stu-id="92ed1-162">The id will be the ARM id of the shared galley image version from which to create a disk.</span></span>
<span data-ttu-id="92ed1-163">Una lun è necessaria se l'origine della copia è uno dei dischi dati nell'immagine della raccolta; se Null, verrà copiato il disco del sistema operativo dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="92ed1-163">A lun is needed if the source of the copy is one of the data disks in the gallery image; if null, the OS disk of the image will be copied.</span></span>

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

### <span data-ttu-id="92ed1-164">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="92ed1-164">-HyperVGeneration</span></span>
<span data-ttu-id="92ed1-165">La generazione hypervisor della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="92ed1-165">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="92ed1-166">Applicabile solo ai dischi del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="92ed1-166">Applicable to OS disks only.</span></span>  <span data-ttu-id="92ed1-167">I valori consentiti sono V1 e V2.</span><span class="sxs-lookup"><span data-stu-id="92ed1-167">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="92ed1-168">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="92ed1-168">-ImageReference</span></span>
<span data-ttu-id="92ed1-169">Specifica il riferimento di immagine su un disco.</span><span class="sxs-lookup"><span data-stu-id="92ed1-169">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="92ed1-170">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="92ed1-170">-KeyEncryptionKey</span></span>
<span data-ttu-id="92ed1-171">Specifica la chiave di crittografia chiave su un disco.</span><span class="sxs-lookup"><span data-stu-id="92ed1-171">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="92ed1-172">-Location</span><span class="sxs-lookup"><span data-stu-id="92ed1-172">-Location</span></span>
<span data-ttu-id="92ed1-173">Specifica una posizione.</span><span class="sxs-lookup"><span data-stu-id="92ed1-173">Specifies a location.</span></span>

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

### <span data-ttu-id="92ed1-174">-LogicalSectorSize</span><span class="sxs-lookup"><span data-stu-id="92ed1-174">-LogicalSectorSize</span></span>
<span data-ttu-id="92ed1-175">Dimensione del settore logico in byte per i dischi Ultra.</span><span class="sxs-lookup"><span data-stu-id="92ed1-175">Logical sector size in bytes for Ultra disks.</span></span> 

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

### <span data-ttu-id="92ed1-176">-MaxSharesCount</span><span class="sxs-lookup"><span data-stu-id="92ed1-176">-MaxSharesCount</span></span>
<span data-ttu-id="92ed1-177">Il numero massimo di vm che è possibile collegare al disco contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="92ed1-177">The maximum number of VMs that can attach to the disk at the same time.</span></span>
<span data-ttu-id="92ed1-178">Il valore maggiore di uno indica un disco che può essere montato su più VM contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="92ed1-178">Value greater than one indicates a disk that can be mounted on multiple VMs at the same time.</span></span>

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

### <span data-ttu-id="92ed1-179">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="92ed1-179">-NetworkAccessPolicy</span></span>
<span data-ttu-id="92ed1-180">I criteri di accesso di rete definiscono i criteri di accesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="92ed1-180">Network access policy defines the network access policy.</span></span>
<span data-ttu-id="92ed1-181">I valori possibili includono: 'AllowAll', 'AllowPrivate', 'DenyAll'</span><span class="sxs-lookup"><span data-stu-id="92ed1-181">Possible values include: 'AllowAll', 'AllowPrivate', 'DenyAll'</span></span>

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

### <span data-ttu-id="92ed1-182">-OsType</span><span class="sxs-lookup"><span data-stu-id="92ed1-182">-OsType</span></span>
<span data-ttu-id="92ed1-183">Specifica il tipo di sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="92ed1-183">Specifies the OS type.</span></span>

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

### <span data-ttu-id="92ed1-184">-SKUName</span><span class="sxs-lookup"><span data-stu-id="92ed1-184">-SkuName</span></span>
<span data-ttu-id="92ed1-185">Specifica il nome SKU dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="92ed1-185">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="92ed1-186">I valori disponibili Standard_LRS, Premium_LRS, StandardSSD_LRS e UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="92ed1-186">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="92ed1-187">UltraSSD_LRS può essere usato solo con valori vuoti per il parametro CreateOption.</span><span class="sxs-lookup"><span data-stu-id="92ed1-187">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="92ed1-188">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="92ed1-188">-SourceResourceId</span></span>
<span data-ttu-id="92ed1-189">Specifica l'ID risorsa di origine.</span><span class="sxs-lookup"><span data-stu-id="92ed1-189">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="92ed1-190">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="92ed1-190">-SourceUri</span></span>
<span data-ttu-id="92ed1-191">Specifica l'URI di origine.</span><span class="sxs-lookup"><span data-stu-id="92ed1-191">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="92ed1-192">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="92ed1-192">-StorageAccountId</span></span>
<span data-ttu-id="92ed1-193">Specifica l'ID dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="92ed1-193">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="92ed1-194">-Tag</span><span class="sxs-lookup"><span data-stu-id="92ed1-194">-Tag</span></span>
<span data-ttu-id="92ed1-195">Coppie chiave-valore sotto forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="92ed1-195">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="92ed1-196">Ad esempio: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="92ed1-196">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="92ed1-197">-Tier</span><span class="sxs-lookup"><span data-stu-id="92ed1-197">-Tier</span></span>
<span data-ttu-id="92ed1-198">Livello delle prestazioni del disco.</span><span class="sxs-lookup"><span data-stu-id="92ed1-198">Performance tier of the disk.</span></span>

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

### <span data-ttu-id="92ed1-199">-UploadSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="92ed1-199">-UploadSizeInBytes</span></span>
<span data-ttu-id="92ed1-200">Specifica le dimensioni del contenuto del caricamento, incluso il piè di pagina VHD quando CreateOption è Upload.</span><span class="sxs-lookup"><span data-stu-id="92ed1-200">Specifies the size of the contents of the upload including the VHD footer when CreateOption is Upload.</span></span>  <span data-ttu-id="92ed1-201">Questo valore deve essere compreso tra 20972032 (20 MiB + 512 byte per il piè di pagina VHD) e 35183298347520 byte (32 TIB + 512 byte per il piè di pagina VHD).</span><span class="sxs-lookup"><span data-stu-id="92ed1-201">This value should be between 20972032 (20 MiB + 512 bytes for the VHD footer) and 35183298347520 bytes (32 TiB + 512 bytes for the VHD footer).</span></span>

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

### <span data-ttu-id="92ed1-202">-Zone</span><span class="sxs-lookup"><span data-stu-id="92ed1-202">-Zone</span></span>
<span data-ttu-id="92ed1-203">Specifica l'elenco di aree logiche per il disco.</span><span class="sxs-lookup"><span data-stu-id="92ed1-203">Specifies the logical zone list for Disk.</span></span>

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

### <span data-ttu-id="92ed1-204">-Confirm</span><span class="sxs-lookup"><span data-stu-id="92ed1-204">-Confirm</span></span>
<span data-ttu-id="92ed1-205">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92ed1-205">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92ed1-206">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92ed1-206">-WhatIf</span></span>
<span data-ttu-id="92ed1-207">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="92ed1-207">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="92ed1-208">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="92ed1-208">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92ed1-209">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92ed1-209">CommonParameters</span></span>
<span data-ttu-id="92ed1-210">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92ed1-210">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92ed1-211">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="92ed1-211">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92ed1-212">INPUT</span><span class="sxs-lookup"><span data-stu-id="92ed1-212">INPUTS</span></span>

### <span data-ttu-id="92ed1-213">System.String</span><span class="sxs-lookup"><span data-stu-id="92ed1-213">System.String</span></span>

### <span data-ttu-id="92ed1-214">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="92ed1-214">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="92ed1-215">System.Int32</span><span class="sxs-lookup"><span data-stu-id="92ed1-215">System.Int32</span></span>

### <span data-ttu-id="92ed1-216">System.String[]</span><span class="sxs-lookup"><span data-stu-id="92ed1-216">System.String[]</span></span>

### <span data-ttu-id="92ed1-217">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="92ed1-217">System.Collections.Hashtable</span></span>

### <span data-ttu-id="92ed1-218">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="92ed1-218">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="92ed1-219">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="92ed1-219">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="92ed1-220">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="92ed1-220">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="92ed1-221">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="92ed1-221">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="92ed1-222">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="92ed1-222">OUTPUTS</span></span>

### <span data-ttu-id="92ed1-223">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="92ed1-223">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="92ed1-224">NOTE</span><span class="sxs-lookup"><span data-stu-id="92ed1-224">NOTES</span></span>

## <span data-ttu-id="92ed1-225">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="92ed1-225">RELATED LINKS</span></span>
