---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
ms.openlocfilehash: 273a4388665e12cf58d1fe2d7e067648862bf4ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684781"
---
# <span data-ttu-id="2ef6b-101">New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="2ef6b-101">New-AzDiskConfig</span></span>

## <span data-ttu-id="2ef6b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2ef6b-102">SYNOPSIS</span></span>
<span data-ttu-id="2ef6b-103">Crea un oggetto disco configurabile.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-103">Creates a configurable disk object.</span></span>

## <span data-ttu-id="2ef6b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2ef6b-104">SYNTAX</span></span>

```
New-AzDiskConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-Zone <String[]>] [-HyperVGeneration <String>] [-DiskIOPSReadWrite <Int32>]
 [-DiskMBpsReadWrite <Int32>] [-Tag <Hashtable>] [-CreateOption <String>] [-StorageAccountId <String>]
 [-ImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2ef6b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2ef6b-105">DESCRIPTION</span></span>
<span data-ttu-id="2ef6b-106">Il cmdlet **New-AzDiskConfig** crea un oggetto disco configurabile.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-106">The **New-AzDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="2ef6b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2ef6b-107">EXAMPLES</span></span>

### <span data-ttu-id="2ef6b-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2ef6b-108">Example 1</span></span>
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

<span data-ttu-id="2ef6b-109">Il primo comando crea un oggetto disco locale vuoto con la dimensione 5GB in Standard_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="2ef6b-110">Imposta anche il tipo di sistema operativo Windows e Abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="2ef6b-111">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia del disco e della chiave di crittografia per l'oggetto disco.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="2ef6b-112">L'ultimo comando accetta l'oggetto disk e crea un disco con il nome "Disk01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="2ef6b-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="2ef6b-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="2ef6b-113">Example 2</span></span>
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

<span data-ttu-id="2ef6b-114">Il primo comando crea un oggetto disco locale per il caricamento.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-114">The first command creates a local disk object for Upload.</span></span>
<span data-ttu-id="2ef6b-115">Il secondo comando accetta l'oggetto disk e crea un disco con il nome "Disk01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="2ef6b-115">The second command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>
<span data-ttu-id="2ef6b-116">Il terzo comando ottiene l'URL SAS per il disco.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-116">The third command gets SAS Url for the disk.</span></span>
<span data-ttu-id="2ef6b-117">Il quarto comando ottiene lo stato del disco.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-117">The fourth command gets the state of the disk.</span></span>
<span data-ttu-id="2ef6b-118">Se lo stato del disco è "ReadyToUpload", un utente può caricare un disco dallo spazio di archiviazione BLOB all'URL SAS del disco usando AzCopy.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-118">If the disk state is 'ReadyToUpload', a user can upload a disk from blob storage to the disk SAS Url using AzCopy.</span></span>
<span data-ttu-id="2ef6b-119">Durante il caricamento, lo stato del disco viene modificato in "ActiveUpload".</span><span class="sxs-lookup"><span data-stu-id="2ef6b-119">During uploading, the disk state is changed to 'ActiveUpload'.</span></span>
<span data-ttu-id="2ef6b-120">L'ultimo comando revoca l'accesso al disco per l'URL SAS.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-120">The last command revokes the disk access for the SAS Url.</span></span>

## <span data-ttu-id="2ef6b-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2ef6b-121">PARAMETERS</span></span>

### <span data-ttu-id="2ef6b-122">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="2ef6b-122">-CreateOption</span></span>
<span data-ttu-id="2ef6b-123">Specifica se questo cmdlet crea un disco nella macchina virtuale da una piattaforma o da un'immagine utente, crea un disco vuoto o allega un disco esistente.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-123">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="2ef6b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ef6b-124">-DefaultProfile</span></span>
<span data-ttu-id="2ef6b-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ef6b-126">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="2ef6b-126">-DiskEncryptionKey</span></span>
<span data-ttu-id="2ef6b-127">Specifica l'oggetto chiave di crittografia del disco in un disco.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-127">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="2ef6b-128">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="2ef6b-128">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="2ef6b-129">Numero di IOPS consentiti per il disco; impostabile solo per i dischi UltraSSD.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-129">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="2ef6b-130">Un'operazione può essere trasferita tra 4K e 256K byte.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-130">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="2ef6b-131">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="2ef6b-131">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="2ef6b-132">Larghezza di banda consentita per questo disco; impostabile solo per i dischi UltraSSD.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-132">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="2ef6b-133">MBps significa milioni di byte al secondo MB Usa la notazione ISO, di poteri di 10.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-133">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="2ef6b-134">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="2ef6b-134">-DiskSizeGB</span></span>
<span data-ttu-id="2ef6b-135">Specifica le dimensioni del disco in GB.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-135">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="2ef6b-136">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="2ef6b-136">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="2ef6b-137">Abilitare le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-137">Enable encryption settings.</span></span>

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

### <span data-ttu-id="2ef6b-138">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="2ef6b-138">-HyperVGeneration</span></span>
<span data-ttu-id="2ef6b-139">Generazione di hypervisor della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-139">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="2ef6b-140">Applicabile solo ai dischi del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-140">Applicable to OS disks only.</span></span>  <span data-ttu-id="2ef6b-141">I valori consentiti sono V1 e V2.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-141">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="2ef6b-142">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="2ef6b-142">-ImageReference</span></span>
<span data-ttu-id="2ef6b-143">Specifica il riferimento alle immagini in un disco.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-143">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="2ef6b-144">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="2ef6b-144">-KeyEncryptionKey</span></span>
<span data-ttu-id="2ef6b-145">Specifica la chiave di crittografia chiave in un disco.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-145">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="2ef6b-146">-Posizione</span><span class="sxs-lookup"><span data-stu-id="2ef6b-146">-Location</span></span>
<span data-ttu-id="2ef6b-147">Specifica una posizione.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-147">Specifies a location.</span></span>

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

### <span data-ttu-id="2ef6b-148">-OsType</span><span class="sxs-lookup"><span data-stu-id="2ef6b-148">-OsType</span></span>
<span data-ttu-id="2ef6b-149">Specifica il tipo di sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-149">Specifies the OS type.</span></span>

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

### <span data-ttu-id="2ef6b-150">-SkuName</span><span class="sxs-lookup"><span data-stu-id="2ef6b-150">-SkuName</span></span>
<span data-ttu-id="2ef6b-151">Specifica il nome SKU dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-151">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="2ef6b-152">I valori disponibili sono Standard_LRS, Premium_LRS, StandardSSD_LRS e UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-152">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="2ef6b-153">UltraSSD_LRS può essere usato solo con il valore Empty per il parametro CreateOption.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-153">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="2ef6b-154">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="2ef6b-154">-SourceResourceId</span></span>
<span data-ttu-id="2ef6b-155">Specifica l'ID risorsa di origine.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-155">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="2ef6b-156">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="2ef6b-156">-SourceUri</span></span>
<span data-ttu-id="2ef6b-157">Specifica l'URI di origine.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-157">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="2ef6b-158">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="2ef6b-158">-StorageAccountId</span></span>
<span data-ttu-id="2ef6b-159">Specifica l'ID account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-159">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="2ef6b-160">-Tag</span><span class="sxs-lookup"><span data-stu-id="2ef6b-160">-Tag</span></span>
<span data-ttu-id="2ef6b-161">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-161">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2ef6b-162">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="2ef6b-162">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2ef6b-163">-Zona</span><span class="sxs-lookup"><span data-stu-id="2ef6b-163">-Zone</span></span>
<span data-ttu-id="2ef6b-164">Specifica l'elenco delle aree logiche per il disco.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-164">Specifies the logical zone list for Disk.</span></span>

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

### <span data-ttu-id="2ef6b-165">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2ef6b-165">-Confirm</span></span>
<span data-ttu-id="2ef6b-166">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ef6b-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ef6b-167">-WhatIf</span></span>
<span data-ttu-id="2ef6b-168">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-168">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2ef6b-169">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ef6b-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ef6b-170">CommonParameters</span></span>
<span data-ttu-id="2ef6b-171">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ef6b-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ef6b-172">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ef6b-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ef6b-173">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2ef6b-173">INPUTS</span></span>

### <span data-ttu-id="2ef6b-174">System. String</span><span class="sxs-lookup"><span data-stu-id="2ef6b-174">System.String</span></span>

### <span data-ttu-id="2ef6b-175">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="2ef6b-175">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="2ef6b-176">System. Int32</span><span class="sxs-lookup"><span data-stu-id="2ef6b-176">System.Int32</span></span>

### <span data-ttu-id="2ef6b-177">System. String []</span><span class="sxs-lookup"><span data-stu-id="2ef6b-177">System.String[]</span></span>

### <span data-ttu-id="2ef6b-178">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2ef6b-178">System.Collections.Hashtable</span></span>

### <span data-ttu-id="2ef6b-179">Microsoft. Azure. Management. Compute. Models. ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="2ef6b-179">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="2ef6b-180">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2ef6b-180">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="2ef6b-181">Microsoft. Azure. Management. Compute. Models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="2ef6b-181">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="2ef6b-182">Microsoft. Azure. Management. Compute. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="2ef6b-182">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="2ef6b-183">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2ef6b-183">OUTPUTS</span></span>

### <span data-ttu-id="2ef6b-184">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="2ef6b-184">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="2ef6b-185">Note</span><span class="sxs-lookup"><span data-stu-id="2ef6b-185">NOTES</span></span>

## <span data-ttu-id="2ef6b-186">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2ef6b-186">RELATED LINKS</span></span>
