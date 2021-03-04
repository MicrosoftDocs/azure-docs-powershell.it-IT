---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azdiskupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
ms.openlocfilehash: e73a6bc0d1bf1d2930396bce779bcb03f91d9936
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957582"
---
# <span data-ttu-id="81575-101">New-AzDiskUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="81575-101">New-AzDiskUpdateConfig</span></span>

## <span data-ttu-id="81575-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81575-102">SYNOPSIS</span></span>
<span data-ttu-id="81575-103">Crea un oggetto di aggiornamento del disco configurabile.</span><span class="sxs-lookup"><span data-stu-id="81575-103">Creates a configurable disk update object.</span></span>

## <span data-ttu-id="81575-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="81575-104">SYNTAX</span></span>

```
New-AzDiskUpdateConfig [[-SkuName] <String>] [-Tier <String>] [-DiskIOPSReadOnly <Int64>]
 [-DiskMBpsReadOnly <Int64>] [-MaxSharesCount <Int32>] [-NetworkAccessPolicy <String>] [-DiskAccessId <String>]
 [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-DiskIOPSReadWrite <Int32>]
 [-DiskMBpsReadWrite <Int32>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [-BurstingEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81575-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="81575-105">DESCRIPTION</span></span>
<span data-ttu-id="81575-106">Il cmdlet **New-AzDiskUpdateConfig crea** un oggetto di aggiornamento del disco configurabile.</span><span class="sxs-lookup"><span data-stu-id="81575-106">The **New-AzDiskUpdateConfig** cmdlet creates a configurable disk update object.</span></span>

## <span data-ttu-id="81575-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="81575-107">EXAMPLES</span></span>

### <span data-ttu-id="81575-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="81575-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzDiskUpdateConfig -DiskSizeGB 10 -SkuName Premium_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="81575-109">Il primo comando crea un oggetto di aggiornamento disco vuoto locale con dimensioni di 10 GB Premium_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="81575-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="81575-110">Configura anche il tipo di sistema operativo Windows e abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="81575-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="81575-111">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia disco e della chiave di crittografia per l'oggetto di aggiornamento del disco.</span><span class="sxs-lookup"><span data-stu-id="81575-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="81575-112">L'ultimo comando accetta l'oggetto di aggiornamento del disco e aggiorna un disco esistente con il nome 'Disco01' nel gruppo di risorse 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="81575-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="81575-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="81575-113">Example 2</span></span>
```
PS C:\> New-AzDiskUpdateConfig -DiskSizeGB 10 | Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="81575-114">Questo comando aggiorna un disco esistente con il nome 'Disk01' nel gruppo di risorse 'ResourceGroup01' a 10 GB.</span><span class="sxs-lookup"><span data-stu-id="81575-114">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="81575-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="81575-115">PARAMETERS</span></span>

### <span data-ttu-id="81575-116">-BurstingEnabled</span><span class="sxs-lookup"><span data-stu-id="81575-116">-BurstingEnabled</span></span>
<span data-ttu-id="81575-117">Abilita lo scatto a raffica oltre la destinazione delle prestazioni di provisioning del disco.</span><span class="sxs-lookup"><span data-stu-id="81575-117">Enables bursting beyond the provisioned performance target of the disk.</span></span> <span data-ttu-id="81575-118">Per impostazione predefinita, la funzionalità Disampazione a sequenza è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="81575-118">Bursting is disabled by default.</span></span> <span data-ttu-id="81575-119">Non si applica ai dischi Ultra.</span><span class="sxs-lookup"><span data-stu-id="81575-119">Does not apply to Ultra disks.</span></span>

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

### <span data-ttu-id="81575-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81575-120">-DefaultProfile</span></span>
<span data-ttu-id="81575-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="81575-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81575-122">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="81575-122">-DiskAccessId</span></span>
<span data-ttu-id="81575-123">{{ Fill DiskAccessId Description }}</span><span class="sxs-lookup"><span data-stu-id="81575-123">{{ Fill DiskAccessId Description }}</span></span>

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

### <span data-ttu-id="81575-124">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="81575-124">-DiskEncryptionKey</span></span>
<span data-ttu-id="81575-125">Specifica l'oggetto chiave di crittografia disco su un disco.</span><span class="sxs-lookup"><span data-stu-id="81575-125">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="81575-126">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="81575-126">-DiskEncryptionSetId</span></span>
<span data-ttu-id="81575-127">Specifica l'ID risorsa del set di crittografia del disco da usare per l'abilitazione della crittografia in fase di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="81575-127">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="81575-128">-DiskIOPSReadOnly</span><span class="sxs-lookup"><span data-stu-id="81575-128">-DiskIOPSReadOnly</span></span>
<span data-ttu-id="81575-129">Numero totale di operazioni di I/O al secondo consentite in tutte le macchine virtuali che montaggio il disco condiviso in sola lettura.</span><span class="sxs-lookup"><span data-stu-id="81575-129">The total number of IOPS that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="81575-130">È possibile trasferire un'operazione tra 4.000 e 256.000 byte.</span><span class="sxs-lookup"><span data-stu-id="81575-130">One operation can transfer between 4k and 256k bytes.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81575-131">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="81575-131">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="81575-132">Numero di operazioni di I/O al secondo consentite per il disco. impostabile solo per dischi UltraSSD.</span><span class="sxs-lookup"><span data-stu-id="81575-132">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="81575-133">È possibile trasferire un'operazione tra 4.000 e 256.000 byte.</span><span class="sxs-lookup"><span data-stu-id="81575-133">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="81575-134">-DiskMBpsReadOnly</span><span class="sxs-lookup"><span data-stu-id="81575-134">-DiskMBpsReadOnly</span></span>
<span data-ttu-id="81575-135">Velocità effettiva totale (MBps) consentita in tutte le macchine virtuali che montaggio del disco condiviso come ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="81575-135">The total throughput (MBps) that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="81575-136">MBps significa milioni di byte al secondo - MB usa la notazione ISO, ovvero potenze di 10.</span><span class="sxs-lookup"><span data-stu-id="81575-136">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81575-137">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="81575-137">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="81575-138">La larghezza di banda consentita per il disco; impostabile solo per dischi UltraSSD.</span><span class="sxs-lookup"><span data-stu-id="81575-138">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="81575-139">MBps significa milioni di byte al secondo - MB usa la notazione ISO, ovvero potenze di 10.</span><span class="sxs-lookup"><span data-stu-id="81575-139">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="81575-140">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="81575-140">-DiskSizeGB</span></span>
<span data-ttu-id="81575-141">Specifica le dimensioni del disco in GB.</span><span class="sxs-lookup"><span data-stu-id="81575-141">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="81575-142">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="81575-142">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="81575-143">Abilitare le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="81575-143">Enable encryption settings.</span></span>

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

### <span data-ttu-id="81575-144">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="81575-144">-EncryptionType</span></span>
<span data-ttu-id="81575-145">Tipo di chiave usata per crittografare i dati del disco.</span><span class="sxs-lookup"><span data-stu-id="81575-145">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="81575-146">I valori disponibili sono: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span><span class="sxs-lookup"><span data-stu-id="81575-146">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="81575-147">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="81575-147">-KeyEncryptionKey</span></span>
<span data-ttu-id="81575-148">Specifica la chiave di crittografia chiave su un disco.</span><span class="sxs-lookup"><span data-stu-id="81575-148">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="81575-149">-MaxSharesCount</span><span class="sxs-lookup"><span data-stu-id="81575-149">-MaxSharesCount</span></span>
<span data-ttu-id="81575-150">Il numero massimo di vm che è possibile collegare al disco contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="81575-150">The maximum number of VMs that can attach to the disk at the same time.</span></span> <span data-ttu-id="81575-151">Il valore maggiore di uno indica un disco che può essere montato su più VM contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="81575-151">Value greater than one indicates a disk that can be mounted on multiple VMs at the same time.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81575-152">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="81575-152">-NetworkAccessPolicy</span></span>
<span data-ttu-id="81575-153">{{ Fill NetworkAccessPolicy Description }}</span><span class="sxs-lookup"><span data-stu-id="81575-153">{{ Fill NetworkAccessPolicy Description }}</span></span>

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

### <span data-ttu-id="81575-154">-OsType</span><span class="sxs-lookup"><span data-stu-id="81575-154">-OsType</span></span>
<span data-ttu-id="81575-155">Specifica il tipo di sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="81575-155">Specifies the OS type.</span></span>

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

### <span data-ttu-id="81575-156">-SKUName</span><span class="sxs-lookup"><span data-stu-id="81575-156">-SkuName</span></span>
<span data-ttu-id="81575-157">Specifica il nome SKU dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="81575-157">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="81575-158">I valori disponibili Standard_LRS, Premium_LRS, StandardSSD_LRS e UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="81575-158">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="81575-159">UltraSSD_LRS possibile usare solo con valori vuoti per il parametro CreateOption.</span><span class="sxs-lookup"><span data-stu-id="81575-159">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="81575-160">-Tag</span><span class="sxs-lookup"><span data-stu-id="81575-160">-Tag</span></span>
<span data-ttu-id="81575-161">Coppie chiave-valore sotto forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="81575-161">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="81575-162">Ad esempio: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="81575-162">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81575-163">-Livello</span><span class="sxs-lookup"><span data-stu-id="81575-163">-Tier</span></span>
<span data-ttu-id="81575-164">Livello delle prestazioni del disco.</span><span class="sxs-lookup"><span data-stu-id="81575-164">Performance tier of the disk.</span></span>

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

### <span data-ttu-id="81575-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="81575-165">-Confirm</span></span>
<span data-ttu-id="81575-166">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81575-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81575-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81575-167">-WhatIf</span></span>
<span data-ttu-id="81575-168">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="81575-168">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="81575-169">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="81575-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81575-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81575-170">CommonParameters</span></span>
<span data-ttu-id="81575-171">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81575-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81575-172">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="81575-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81575-173">INPUT</span><span class="sxs-lookup"><span data-stu-id="81575-173">INPUTS</span></span>

### <span data-ttu-id="81575-174">System.String</span><span class="sxs-lookup"><span data-stu-id="81575-174">System.String</span></span>

### <span data-ttu-id="81575-175">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="81575-175">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="81575-176">System.Int32</span><span class="sxs-lookup"><span data-stu-id="81575-176">System.Int32</span></span>

### <span data-ttu-id="81575-177">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="81575-177">System.Collections.Hashtable</span></span>

### <span data-ttu-id="81575-178">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="81575-178">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="81575-179">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="81575-179">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="81575-180">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="81575-180">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="81575-181">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="81575-181">OUTPUTS</span></span>

### <span data-ttu-id="81575-182">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="81575-182">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="81575-183">NOTE</span><span class="sxs-lookup"><span data-stu-id="81575-183">NOTES</span></span>

## <span data-ttu-id="81575-184">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="81575-184">RELATED LINKS</span></span>
