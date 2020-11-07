---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
ms.openlocfilehash: c37ed947441789951d8523f38e7950ad6d9d2066
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675343"
---
# <span data-ttu-id="60280-101">New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="60280-101">New-AzDiskConfig</span></span>

## <span data-ttu-id="60280-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="60280-102">SYNOPSIS</span></span>
<span data-ttu-id="60280-103">Crea un oggetto disco configurabile.</span><span class="sxs-lookup"><span data-stu-id="60280-103">Creates a configurable disk object.</span></span>

## <span data-ttu-id="60280-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="60280-104">SYNTAX</span></span>

```
New-AzDiskConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-Zone <String[]>] [-HyperVGeneration <String>] [-DiskIOPSReadWrite <Int32>]
 [-DiskMBpsReadWrite <Int32>] [-Tag <Hashtable>] [-CreateOption <String>] [-StorageAccountId <String>]
 [-ImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-UploadSizeInBytes <Int64>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60280-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60280-105">DESCRIPTION</span></span>
<span data-ttu-id="60280-106">Il cmdlet **New-AzDiskConfig** crea un oggetto disco configurabile.</span><span class="sxs-lookup"><span data-stu-id="60280-106">The **New-AzDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="60280-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="60280-107">EXAMPLES</span></span>

### <span data-ttu-id="60280-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="60280-108">Example 1</span></span>
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

<span data-ttu-id="60280-109">Il primo comando crea un oggetto disco locale vuoto con la dimensione 5GB in Standard_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="60280-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="60280-110">Imposta anche il tipo di sistema operativo Windows e Abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="60280-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="60280-111">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia del disco e della chiave di crittografia per l'oggetto disco.</span><span class="sxs-lookup"><span data-stu-id="60280-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="60280-112">L'ultimo comando accetta l'oggetto disk e crea un disco con il nome "Disk01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="60280-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="60280-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="60280-113">Example 2</span></span>
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

<span data-ttu-id="60280-114">Il primo comando crea un oggetto disco locale per il caricamento.</span><span class="sxs-lookup"><span data-stu-id="60280-114">The first command creates a local disk object for Upload.</span></span>
<span data-ttu-id="60280-115">Il secondo comando accetta l'oggetto disk e crea un disco con il nome "Disk01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="60280-115">The second command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>
<span data-ttu-id="60280-116">Il terzo comando ottiene l'URL SAS per il disco.</span><span class="sxs-lookup"><span data-stu-id="60280-116">The third command gets SAS Url for the disk.</span></span>
<span data-ttu-id="60280-117">Il quarto comando ottiene lo stato del disco.</span><span class="sxs-lookup"><span data-stu-id="60280-117">The fourth command gets the state of the disk.</span></span>
<span data-ttu-id="60280-118">Se lo stato del disco è "ReadyToUpload", un utente può caricare un disco dallo spazio di archiviazione BLOB all'URL SAS del disco usando AzCopy.</span><span class="sxs-lookup"><span data-stu-id="60280-118">If the disk state is 'ReadyToUpload', a user can upload a disk from blob storage to the disk SAS Url using AzCopy.</span></span>
<span data-ttu-id="60280-119">Durante il caricamento, lo stato del disco viene modificato in "ActiveUpload".</span><span class="sxs-lookup"><span data-stu-id="60280-119">During uploading, the disk state is changed to 'ActiveUpload'.</span></span>
<span data-ttu-id="60280-120">L'ultimo comando revoca l'accesso al disco per l'URL SAS.</span><span class="sxs-lookup"><span data-stu-id="60280-120">The last command revokes the disk access for the SAS Url.</span></span>

## <span data-ttu-id="60280-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="60280-121">PARAMETERS</span></span>

### <span data-ttu-id="60280-122">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="60280-122">-CreateOption</span></span>
<span data-ttu-id="60280-123">Specifica se questo cmdlet crea un disco nella macchina virtuale da una piattaforma o da un'immagine utente, crea un disco vuoto o allega un disco esistente.</span><span class="sxs-lookup"><span data-stu-id="60280-123">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="60280-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60280-124">-DefaultProfile</span></span>
<span data-ttu-id="60280-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="60280-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60280-126">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="60280-126">-DiskEncryptionKey</span></span>
<span data-ttu-id="60280-127">Specifica l'oggetto chiave di crittografia del disco in un disco.</span><span class="sxs-lookup"><span data-stu-id="60280-127">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="60280-128">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="60280-128">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="60280-129">Numero di IOPS consentiti per il disco; impostabile solo per i dischi UltraSSD.</span><span class="sxs-lookup"><span data-stu-id="60280-129">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="60280-130">Un'operazione può essere trasferita tra 4K e 256K byte.</span><span class="sxs-lookup"><span data-stu-id="60280-130">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="60280-131">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="60280-131">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="60280-132">Larghezza di banda consentita per questo disco; impostabile solo per i dischi UltraSSD.</span><span class="sxs-lookup"><span data-stu-id="60280-132">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="60280-133">MBps significa milioni di byte al secondo MB Usa la notazione ISO, di poteri di 10.</span><span class="sxs-lookup"><span data-stu-id="60280-133">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="60280-134">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="60280-134">-DiskSizeGB</span></span>
<span data-ttu-id="60280-135">Specifica le dimensioni del disco in GB.</span><span class="sxs-lookup"><span data-stu-id="60280-135">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="60280-136">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="60280-136">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="60280-137">Abilitare le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="60280-137">Enable encryption settings.</span></span>

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

### <span data-ttu-id="60280-138">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="60280-138">-HyperVGeneration</span></span>
<span data-ttu-id="60280-139">Generazione di hypervisor della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="60280-139">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="60280-140">Applicabile solo ai dischi del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="60280-140">Applicable to OS disks only.</span></span>  <span data-ttu-id="60280-141">I valori consentiti sono V1 e V2.</span><span class="sxs-lookup"><span data-stu-id="60280-141">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="60280-142">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="60280-142">-ImageReference</span></span>
<span data-ttu-id="60280-143">Specifica il riferimento alle immagini in un disco.</span><span class="sxs-lookup"><span data-stu-id="60280-143">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="60280-144">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="60280-144">-KeyEncryptionKey</span></span>
<span data-ttu-id="60280-145">Specifica la chiave di crittografia chiave in un disco.</span><span class="sxs-lookup"><span data-stu-id="60280-145">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="60280-146">-Posizione</span><span class="sxs-lookup"><span data-stu-id="60280-146">-Location</span></span>
<span data-ttu-id="60280-147">Specifica una posizione.</span><span class="sxs-lookup"><span data-stu-id="60280-147">Specifies a location.</span></span>

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

### <span data-ttu-id="60280-148">-OsType</span><span class="sxs-lookup"><span data-stu-id="60280-148">-OsType</span></span>
<span data-ttu-id="60280-149">Specifica il tipo di sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="60280-149">Specifies the OS type.</span></span>

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

### <span data-ttu-id="60280-150">-SkuName</span><span class="sxs-lookup"><span data-stu-id="60280-150">-SkuName</span></span>
<span data-ttu-id="60280-151">Specifica il nome SKU dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="60280-151">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="60280-152">I valori disponibili sono Standard_LRS, Premium_LRS, StandardSSD_LRS e UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="60280-152">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="60280-153">UltraSSD_LRS può essere usato solo con il valore Empty per il parametro CreateOption.</span><span class="sxs-lookup"><span data-stu-id="60280-153">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="60280-154">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="60280-154">-SourceResourceId</span></span>
<span data-ttu-id="60280-155">Specifica l'ID risorsa di origine.</span><span class="sxs-lookup"><span data-stu-id="60280-155">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="60280-156">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="60280-156">-SourceUri</span></span>
<span data-ttu-id="60280-157">Specifica l'URI di origine.</span><span class="sxs-lookup"><span data-stu-id="60280-157">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="60280-158">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="60280-158">-StorageAccountId</span></span>
<span data-ttu-id="60280-159">Specifica l'ID account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="60280-159">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="60280-160">-Tag</span><span class="sxs-lookup"><span data-stu-id="60280-160">-Tag</span></span>
<span data-ttu-id="60280-161">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="60280-161">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="60280-162">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="60280-162">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="60280-163">-UploadSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="60280-163">-UploadSizeInBytes</span></span>
<span data-ttu-id="60280-164">Specifica le dimensioni del contenuto del caricamento, incluso il piè di pagina VHD quando CreateOption è caricato.</span><span class="sxs-lookup"><span data-stu-id="60280-164">Specifies the size of the contents of the upload including the VHD footer when CreateOption is Upload.</span></span>  <span data-ttu-id="60280-165">Questo valore deve essere compreso tra 20972032 (20 MiB + 512 byte per il piè di pagina VHD) e 35183298347520 byte (32 TiB + 512 byte per il piè di pagina VHD).</span><span class="sxs-lookup"><span data-stu-id="60280-165">This value should be between 20972032 (20 MiB + 512 bytes for the VHD footer) and 35183298347520 bytes (32 TiB + 512 bytes for the VHD footer).</span></span>

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

### <span data-ttu-id="60280-166">-Zona</span><span class="sxs-lookup"><span data-stu-id="60280-166">-Zone</span></span>
<span data-ttu-id="60280-167">Specifica l'elenco delle aree logiche per il disco.</span><span class="sxs-lookup"><span data-stu-id="60280-167">Specifies the logical zone list for Disk.</span></span>

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

### <span data-ttu-id="60280-168">-Confermare</span><span class="sxs-lookup"><span data-stu-id="60280-168">-Confirm</span></span>
<span data-ttu-id="60280-169">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60280-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60280-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60280-170">-WhatIf</span></span>
<span data-ttu-id="60280-171">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60280-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="60280-172">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60280-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60280-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60280-173">CommonParameters</span></span>
<span data-ttu-id="60280-174">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60280-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60280-175">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60280-175">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60280-176">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="60280-176">INPUTS</span></span>

### <span data-ttu-id="60280-177">System. String</span><span class="sxs-lookup"><span data-stu-id="60280-177">System.String</span></span>

### <span data-ttu-id="60280-178">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="60280-178">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="60280-179">System. Int32</span><span class="sxs-lookup"><span data-stu-id="60280-179">System.Int32</span></span>

### <span data-ttu-id="60280-180">System. String []</span><span class="sxs-lookup"><span data-stu-id="60280-180">System.String[]</span></span>

### <span data-ttu-id="60280-181">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="60280-181">System.Collections.Hashtable</span></span>

### <span data-ttu-id="60280-182">Microsoft. Azure. Management. Compute. Models. ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="60280-182">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="60280-183">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="60280-183">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="60280-184">Microsoft. Azure. Management. Compute. Models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="60280-184">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="60280-185">Microsoft. Azure. Management. Compute. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="60280-185">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="60280-186">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="60280-186">OUTPUTS</span></span>

### <span data-ttu-id="60280-187">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="60280-187">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="60280-188">Note</span><span class="sxs-lookup"><span data-stu-id="60280-188">NOTES</span></span>

## <span data-ttu-id="60280-189">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="60280-189">RELATED LINKS</span></span>
