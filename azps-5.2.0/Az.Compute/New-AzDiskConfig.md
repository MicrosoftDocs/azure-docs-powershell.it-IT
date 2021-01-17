---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
ms.openlocfilehash: ec4d0444ad88fa7536fbf1ee050dc8dcb6a76af3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340624"
---
# <span data-ttu-id="1bf9b-101">New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="1bf9b-101">New-AzDiskConfig</span></span>

## <span data-ttu-id="1bf9b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1bf9b-102">SYNOPSIS</span></span>
<span data-ttu-id="1bf9b-103">Crea un oggetto disco configurabile.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-103">Creates a configurable disk object.</span></span>

## <span data-ttu-id="1bf9b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1bf9b-104">SYNTAX</span></span>

```
New-AzDiskConfig [[-SkuName] <String>] [-Tier <String>] [-LogicalSectorSize <Int32>]
 [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Zone <String[]>]
 [-HyperVGeneration <String>] [-DiskIOPSReadWrite <Int64>] [-DiskMBpsReadWrite <Int64>]
 [-DiskIOPSReadOnly <Int64>] [-DiskMBpsReadOnly <Int64>] [-MaxSharesCount <Int32>] [-Tag <Hashtable>]
 [-CreateOption <String>] [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>]
 [-GalleryImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-UploadSizeInBytes <Int64>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [-DiskAccessId <String>]
 [-NetworkAccessPolicy <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1bf9b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1bf9b-105">DESCRIPTION</span></span>
<span data-ttu-id="1bf9b-106">Il cmdlet **New-AzDiskConfig** crea un oggetto disco configurabile.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-106">The **New-AzDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="1bf9b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1bf9b-107">EXAMPLES</span></span>

### <span data-ttu-id="1bf9b-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1bf9b-108">Example 1</span></span>
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

<span data-ttu-id="1bf9b-109">Il primo comando crea un oggetto disco locale vuoto con la dimensione 5GB in Standard_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="1bf9b-110">Imposta anche il tipo di sistema operativo Windows e Abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="1bf9b-111">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia del disco e della chiave di crittografia per l'oggetto disco.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="1bf9b-112">L'ultimo comando accetta l'oggetto disk e crea un disco con il nome "Disk01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="1bf9b-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="1bf9b-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="1bf9b-113">Example 2</span></span>
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

<span data-ttu-id="1bf9b-114">Il primo comando crea un oggetto disco locale per il caricamento.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-114">The first command creates a local disk object for Upload.</span></span>
<span data-ttu-id="1bf9b-115">Il secondo comando accetta l'oggetto disk e crea un disco con il nome "Disk01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="1bf9b-115">The second command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>
<span data-ttu-id="1bf9b-116">Il terzo comando ottiene l'URL SAS per il disco.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-116">The third command gets SAS Url for the disk.</span></span>
<span data-ttu-id="1bf9b-117">Il quarto comando ottiene lo stato del disco.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-117">The fourth command gets the state of the disk.</span></span>
<span data-ttu-id="1bf9b-118">Se lo stato del disco è "ReadyToUpload", un utente può caricare un disco dallo spazio di archiviazione BLOB all'URL SAS del disco usando AzCopy.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-118">If the disk state is 'ReadyToUpload', a user can upload a disk from blob storage to the disk SAS Url using AzCopy.</span></span>
<span data-ttu-id="1bf9b-119">Durante il caricamento, lo stato del disco viene modificato in "ActiveUpload".</span><span class="sxs-lookup"><span data-stu-id="1bf9b-119">During uploading, the disk state is changed to 'ActiveUpload'.</span></span>
<span data-ttu-id="1bf9b-120">L'ultimo comando revoca l'accesso al disco per l'URL SAS.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-120">The last command revokes the disk access for the SAS Url.</span></span>

### <span data-ttu-id="1bf9b-121">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="1bf9b-121">Example 3</span></span>
```
PS C:\> $galleryImageReference = @{Id = '/subscriptions/0296790d-427c-48ca-b204-8b729bbd8670/resourceGroups/swaggertests/providers/Microsoft.Compute/galleries/swaggergallery/images/swaggerimagedef/versions/1.0.0'; Lun=1}
PS C:\> $diskConfig = New-AzDiskConfig -Location 'West US' -CreateOption 'FromImage' -GalleryImageReference $galleryImageReference;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskConfig
```

<span data-ttu-id="1bf9b-122">Creare un disco da una versione di immagine della raccolta condivisa.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-122">Create a disk from a Shared Gallery Image Version.</span></span>  <span data-ttu-id="1bf9b-123">ID è l'ID della versione dell'immagine della raccolta condivisa.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-123">Id is the id of the shared gallery image version.</span></span> <span data-ttu-id="1bf9b-124">Lun è necessario solo se l'origine è un disco dati.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-124">Lun is needed only if the source is a data disk.</span></span>

## <span data-ttu-id="1bf9b-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1bf9b-125">PARAMETERS</span></span>

### <span data-ttu-id="1bf9b-126">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="1bf9b-126">-CreateOption</span></span>
<span data-ttu-id="1bf9b-127">Specifica se questo cmdlet crea un disco nella macchina virtuale da una piattaforma o da un'immagine utente, crea un disco vuoto o allega un disco esistente.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-127">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="1bf9b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bf9b-128">-DefaultProfile</span></span>
<span data-ttu-id="1bf9b-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1bf9b-130">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="1bf9b-130">-DiskAccessId</span></span>
<span data-ttu-id="1bf9b-131">Ottiene o imposta l'ID ARM della risorsa DiskAccess per l'uso di endpoint privati.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-131">Gets or sets ARM ID of the DiskAccess resource for using private endpoints on.</span></span>


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

### <span data-ttu-id="1bf9b-132">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="1bf9b-132">-DiskEncryptionKey</span></span>
<span data-ttu-id="1bf9b-133">Specifica l'oggetto chiave di crittografia del disco in un disco.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-133">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="1bf9b-134">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="1bf9b-134">-DiskEncryptionSetId</span></span>
<span data-ttu-id="1bf9b-135">Specifica l'ID risorsa del set di crittografia disco da usare per abilitare la crittografia a riposo.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-135">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="1bf9b-136">-DiskIOPSReadOnly</span><span class="sxs-lookup"><span data-stu-id="1bf9b-136">-DiskIOPSReadOnly</span></span>
<span data-ttu-id="1bf9b-137">Numero totale di IOPS che saranno consentiti in tutte le VM che montano il disco condiviso come ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-137">The total number of IOPS that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="1bf9b-138">Un'operazione può essere trasferita tra 4K e 256K byte.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-138">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="1bf9b-139">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="1bf9b-139">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="1bf9b-140">Numero di IOPS consentiti per il disco; impostabile solo per i dischi UltraSSD.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-140">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="1bf9b-141">Un'operazione può essere trasferita tra 4K e 256K byte.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-141">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="1bf9b-142">-DiskMBpsReadOnly</span><span class="sxs-lookup"><span data-stu-id="1bf9b-142">-DiskMBpsReadOnly</span></span>
<span data-ttu-id="1bf9b-143">"Descrizione": "il throughput totale (MBps) che sarà consentito in tutte le VM che monta il disco condiviso come ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-143">"description": "The total throughput (MBps) that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="1bf9b-144">MBps significa milioni di byte al secondo MB Usa la notazione ISO, di poteri di 10.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-144">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="1bf9b-145">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="1bf9b-145">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="1bf9b-146">Larghezza di banda consentita per questo disco; impostabile solo per i dischi UltraSSD.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-146">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="1bf9b-147">MBps significa milioni di byte al secondo MB Usa la notazione ISO, di poteri di 10.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-147">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="1bf9b-148">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="1bf9b-148">-DiskSizeGB</span></span>
<span data-ttu-id="1bf9b-149">Specifica le dimensioni del disco in GB.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-149">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="1bf9b-150">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="1bf9b-150">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="1bf9b-151">Abilitare le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-151">Enable encryption settings.</span></span>

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

### <span data-ttu-id="1bf9b-152">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="1bf9b-152">-EncryptionType</span></span>
<span data-ttu-id="1bf9b-153">Tipo di chiave utilizzata per crittografare i dati del disco.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-153">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="1bf9b-154">I valori disponibili sono: "EncryptionAtRestWithPlatformKey", "EncryptionAtRestWithCustomerKey"</span><span class="sxs-lookup"><span data-stu-id="1bf9b-154">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="1bf9b-155">-GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="1bf9b-155">-GalleryImageReference</span></span>
<span data-ttu-id="1bf9b-156">Oggetto GalleryImageReference.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-156">The GalleryImageReference object.</span></span>  <span data-ttu-id="1bf9b-157">Obbligatorio per la creazione da un'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-157">Required if creating from a Gallery Image.</span></span> <span data-ttu-id="1bf9b-158">L'ID sarà l'ID ARM della versione condivisa dell'immagine della cambusa da cui creare un disco.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-158">The id will be the ARM id of the shared galley image version from which to create a disk.</span></span>
<span data-ttu-id="1bf9b-159">È necessario un lun se l'origine della copia è uno dei dischi di dati nell'immagine della raccolta; Se null, il disco del sistema operativo dell'immagine verrà copiato.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-159">A lun is needed if the source of the copy is one of the data disks in the gallery image; if null, the OS disk of the image will be copied.</span></span>

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

### <span data-ttu-id="1bf9b-160">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="1bf9b-160">-HyperVGeneration</span></span>
<span data-ttu-id="1bf9b-161">Generazione di hypervisor della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-161">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="1bf9b-162">Applicabile solo ai dischi del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-162">Applicable to OS disks only.</span></span>  <span data-ttu-id="1bf9b-163">I valori consentiti sono V1 e V2.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-163">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="1bf9b-164">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="1bf9b-164">-ImageReference</span></span>
<span data-ttu-id="1bf9b-165">Specifica il riferimento alle immagini in un disco.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-165">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="1bf9b-166">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="1bf9b-166">-KeyEncryptionKey</span></span>
<span data-ttu-id="1bf9b-167">Specifica la chiave di crittografia chiave in un disco.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-167">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="1bf9b-168">-Posizione</span><span class="sxs-lookup"><span data-stu-id="1bf9b-168">-Location</span></span>
<span data-ttu-id="1bf9b-169">Specifica una posizione.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-169">Specifies a location.</span></span>

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

### <span data-ttu-id="1bf9b-170">-LogicalSectorSize</span><span class="sxs-lookup"><span data-stu-id="1bf9b-170">-LogicalSectorSize</span></span>
<span data-ttu-id="1bf9b-171">Dimensioni del settore logico in byte per dischi Ultra.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-171">Logical sector size in bytes for Ultra disks.</span></span> 

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

### <span data-ttu-id="1bf9b-172">-MaxSharesCount</span><span class="sxs-lookup"><span data-stu-id="1bf9b-172">-MaxSharesCount</span></span>
<span data-ttu-id="1bf9b-173">Numero massimo di VM che possono essere allegate al disco contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-173">The maximum number of VMs that can attach to the disk at the same time.</span></span>
<span data-ttu-id="1bf9b-174">Il valore maggiore di uno indica un disco che può essere montato su più VM contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-174">Value greater than one indicates a disk that can be mounted on multiple VMs at the same time.</span></span>

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

### <span data-ttu-id="1bf9b-175">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1bf9b-175">-NetworkAccessPolicy</span></span>
<span data-ttu-id="1bf9b-176">I criteri di accesso alla rete definiscono i criteri di accesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-176">Network access policy defines the network access policy.</span></span>
<span data-ttu-id="1bf9b-177">I valori possibili includono: "AllowAll", "AllowPrivate", "valore denyall"</span><span class="sxs-lookup"><span data-stu-id="1bf9b-177">Possible values include: 'AllowAll', 'AllowPrivate', 'DenyAll'</span></span>

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

### <span data-ttu-id="1bf9b-178">-OsType</span><span class="sxs-lookup"><span data-stu-id="1bf9b-178">-OsType</span></span>
<span data-ttu-id="1bf9b-179">Specifica il tipo di sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-179">Specifies the OS type.</span></span>

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

### <span data-ttu-id="1bf9b-180">-SkuName</span><span class="sxs-lookup"><span data-stu-id="1bf9b-180">-SkuName</span></span>
<span data-ttu-id="1bf9b-181">Specifica il nome SKU dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-181">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="1bf9b-182">I valori disponibili sono Standard_LRS, Premium_LRS, StandardSSD_LRS e UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-182">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="1bf9b-183">UltraSSD_LRS può essere usato solo con il valore Empty per il parametro CreateOption.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-183">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="1bf9b-184">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="1bf9b-184">-SourceResourceId</span></span>
<span data-ttu-id="1bf9b-185">Specifica l'ID risorsa di origine.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-185">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="1bf9b-186">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="1bf9b-186">-SourceUri</span></span>
<span data-ttu-id="1bf9b-187">Specifica l'URI di origine.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-187">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="1bf9b-188">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="1bf9b-188">-StorageAccountId</span></span>
<span data-ttu-id="1bf9b-189">Specifica l'ID account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-189">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="1bf9b-190">-Tag</span><span class="sxs-lookup"><span data-stu-id="1bf9b-190">-Tag</span></span>
<span data-ttu-id="1bf9b-191">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-191">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1bf9b-192">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="1bf9b-192">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1bf9b-193">-Tier</span><span class="sxs-lookup"><span data-stu-id="1bf9b-193">-Tier</span></span>
<span data-ttu-id="1bf9b-194">Livello di prestazioni del disco.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-194">Performance tier of the disk.</span></span>

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

### <span data-ttu-id="1bf9b-195">-UploadSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="1bf9b-195">-UploadSizeInBytes</span></span>
<span data-ttu-id="1bf9b-196">Specifica le dimensioni del contenuto del caricamento, incluso il piè di pagina VHD quando CreateOption è caricato.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-196">Specifies the size of the contents of the upload including the VHD footer when CreateOption is Upload.</span></span>  <span data-ttu-id="1bf9b-197">Questo valore deve essere compreso tra 20972032 (20 MiB + 512 byte per il piè di pagina VHD) e 35183298347520 byte (32 TiB + 512 byte per il piè di pagina VHD).</span><span class="sxs-lookup"><span data-stu-id="1bf9b-197">This value should be between 20972032 (20 MiB + 512 bytes for the VHD footer) and 35183298347520 bytes (32 TiB + 512 bytes for the VHD footer).</span></span>

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

### <span data-ttu-id="1bf9b-198">-Zona</span><span class="sxs-lookup"><span data-stu-id="1bf9b-198">-Zone</span></span>
<span data-ttu-id="1bf9b-199">Specifica l'elenco delle aree logiche per il disco.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-199">Specifies the logical zone list for Disk.</span></span>

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

### <span data-ttu-id="1bf9b-200">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1bf9b-200">-Confirm</span></span>
<span data-ttu-id="1bf9b-201">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-201">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bf9b-202">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bf9b-202">-WhatIf</span></span>
<span data-ttu-id="1bf9b-203">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-203">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1bf9b-204">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-204">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bf9b-205">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bf9b-205">CommonParameters</span></span>
<span data-ttu-id="1bf9b-206">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bf9b-206">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bf9b-207">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1bf9b-207">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bf9b-208">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1bf9b-208">INPUTS</span></span>

### <span data-ttu-id="1bf9b-209">System. String</span><span class="sxs-lookup"><span data-stu-id="1bf9b-209">System.String</span></span>

### <span data-ttu-id="1bf9b-210">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="1bf9b-210">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="1bf9b-211">System. Int32</span><span class="sxs-lookup"><span data-stu-id="1bf9b-211">System.Int32</span></span>

### <span data-ttu-id="1bf9b-212">System. String []</span><span class="sxs-lookup"><span data-stu-id="1bf9b-212">System.String[]</span></span>

### <span data-ttu-id="1bf9b-213">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1bf9b-213">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1bf9b-214">Microsoft. Azure. Management. Compute. Models. ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="1bf9b-214">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="1bf9b-215">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1bf9b-215">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="1bf9b-216">Microsoft. Azure. Management. Compute. Models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="1bf9b-216">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="1bf9b-217">Microsoft. Azure. Management. Compute. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="1bf9b-217">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="1bf9b-218">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1bf9b-218">OUTPUTS</span></span>

### <span data-ttu-id="1bf9b-219">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="1bf9b-219">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="1bf9b-220">Note</span><span class="sxs-lookup"><span data-stu-id="1bf9b-220">NOTES</span></span>

## <span data-ttu-id="1bf9b-221">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1bf9b-221">RELATED LINKS</span></span>
