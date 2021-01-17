---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
ms.openlocfilehash: a738ec606fc982573c4062879e9da4becee43df2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488419"
---
# <span data-ttu-id="26306-101">New-AzDiskUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="26306-101">New-AzDiskUpdateConfig</span></span>

## <span data-ttu-id="26306-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="26306-102">SYNOPSIS</span></span>
<span data-ttu-id="26306-103">Crea un oggetto di aggiornamento del disco configurabile.</span><span class="sxs-lookup"><span data-stu-id="26306-103">Creates a configurable disk update object.</span></span>

## <span data-ttu-id="26306-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="26306-104">SYNTAX</span></span>

```
New-AzDiskUpdateConfig [[-SkuName] <String>] [-Tier <String>] [-DiskIOPSReadOnly <Int64>]
 [-DiskMBpsReadOnly <Int64>] [-MaxSharesCount <Int32>] [-NetworkAccessPolicy <String>] [-DiskAccessId <String>]
 [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-DiskIOPSReadWrite <Int32>]
 [-DiskMBpsReadWrite <Int32>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26306-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26306-105">DESCRIPTION</span></span>
<span data-ttu-id="26306-106">Il cmdlet **New-AzDiskUpdateConfig** crea un oggetto di aggiornamento del disco configurabile.</span><span class="sxs-lookup"><span data-stu-id="26306-106">The **New-AzDiskUpdateConfig** cmdlet creates a configurable disk update object.</span></span>

## <span data-ttu-id="26306-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="26306-107">EXAMPLES</span></span>

### <span data-ttu-id="26306-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="26306-108">Example 1</span></span>
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

<span data-ttu-id="26306-109">Il primo comando crea un oggetto di aggiornamento del disco vuoto locale con dimensioni 10GB in Premium_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="26306-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="26306-110">Imposta anche il tipo di sistema operativo Windows e Abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="26306-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="26306-111">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia del disco e della chiave di crittografia per l'oggetto aggiornamento disco.</span><span class="sxs-lookup"><span data-stu-id="26306-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="26306-112">L'ultimo comando accetta l'oggetto Update del disco e aggiorna un disco esistente con il nome "Disk01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="26306-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="26306-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="26306-113">Example 2</span></span>
```
PS C:\> New-AzDiskUpdateConfig -DiskSizeGB 10 | Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="26306-114">Questo comando aggiorna un disco esistente con il nome "Disk01" nel gruppo di risorse "ResourceGroup01" in dimensioni del disco di 10 GB.</span><span class="sxs-lookup"><span data-stu-id="26306-114">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="26306-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="26306-115">PARAMETERS</span></span>

### <span data-ttu-id="26306-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26306-116">-DefaultProfile</span></span>
<span data-ttu-id="26306-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="26306-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26306-118">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="26306-118">-DiskAccessId</span></span>
<span data-ttu-id="26306-119">{{Fill DiskAccessId Description}}</span><span class="sxs-lookup"><span data-stu-id="26306-119">{{ Fill DiskAccessId Description }}</span></span>

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

### <span data-ttu-id="26306-120">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="26306-120">-DiskEncryptionKey</span></span>
<span data-ttu-id="26306-121">Specifica l'oggetto chiave di crittografia del disco in un disco.</span><span class="sxs-lookup"><span data-stu-id="26306-121">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="26306-122">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="26306-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="26306-123">Specifica l'ID risorsa del set di crittografia disco da usare per abilitare la crittografia a riposo.</span><span class="sxs-lookup"><span data-stu-id="26306-123">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="26306-124">-DiskIOPSReadOnly</span><span class="sxs-lookup"><span data-stu-id="26306-124">-DiskIOPSReadOnly</span></span>
<span data-ttu-id="26306-125">Numero totale di IOPS che saranno consentiti in tutte le VM che montano il disco condiviso come ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="26306-125">The total number of IOPS that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="26306-126">Un'operazione può essere trasferita tra 4K e 256K byte.</span><span class="sxs-lookup"><span data-stu-id="26306-126">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="26306-127">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="26306-127">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="26306-128">Numero di IOPS consentiti per il disco; impostabile solo per i dischi UltraSSD.</span><span class="sxs-lookup"><span data-stu-id="26306-128">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="26306-129">Un'operazione può essere trasferita tra 4K e 256K byte.</span><span class="sxs-lookup"><span data-stu-id="26306-129">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="26306-130">-DiskMBpsReadOnly</span><span class="sxs-lookup"><span data-stu-id="26306-130">-DiskMBpsReadOnly</span></span>
<span data-ttu-id="26306-131">Il throughput totale (MBps) che sarà consentito in tutte le VM che montano il disco condiviso come ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="26306-131">The total throughput (MBps) that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="26306-132">MBps significa milioni di byte al secondo MB Usa la notazione ISO, di poteri di 10.</span><span class="sxs-lookup"><span data-stu-id="26306-132">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="26306-133">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="26306-133">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="26306-134">Larghezza di banda consentita per questo disco; impostabile solo per i dischi UltraSSD.</span><span class="sxs-lookup"><span data-stu-id="26306-134">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="26306-135">MBps significa milioni di byte al secondo MB Usa la notazione ISO, di poteri di 10.</span><span class="sxs-lookup"><span data-stu-id="26306-135">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="26306-136">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="26306-136">-DiskSizeGB</span></span>
<span data-ttu-id="26306-137">Specifica le dimensioni del disco in GB.</span><span class="sxs-lookup"><span data-stu-id="26306-137">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="26306-138">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="26306-138">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="26306-139">Abilitare le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="26306-139">Enable encryption settings.</span></span>

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

### <span data-ttu-id="26306-140">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="26306-140">-EncryptionType</span></span>
<span data-ttu-id="26306-141">Tipo di chiave utilizzata per crittografare i dati del disco.</span><span class="sxs-lookup"><span data-stu-id="26306-141">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="26306-142">I valori disponibili sono: "EncryptionAtRestWithPlatformKey", "EncryptionAtRestWithCustomerKey"</span><span class="sxs-lookup"><span data-stu-id="26306-142">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="26306-143">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="26306-143">-KeyEncryptionKey</span></span>
<span data-ttu-id="26306-144">Specifica la chiave di crittografia chiave in un disco.</span><span class="sxs-lookup"><span data-stu-id="26306-144">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="26306-145">-MaxSharesCount</span><span class="sxs-lookup"><span data-stu-id="26306-145">-MaxSharesCount</span></span>
<span data-ttu-id="26306-146">Numero massimo di VM che possono essere allegate al disco contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="26306-146">The maximum number of VMs that can attach to the disk at the same time.</span></span> <span data-ttu-id="26306-147">Il valore maggiore di uno indica un disco che può essere montato su più VM contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="26306-147">Value greater than one indicates a disk that can be mounted on multiple VMs at the same time.</span></span>

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

### <span data-ttu-id="26306-148">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="26306-148">-NetworkAccessPolicy</span></span>
<span data-ttu-id="26306-149">{{Fill NetworkAccessPolicy Description}}</span><span class="sxs-lookup"><span data-stu-id="26306-149">{{ Fill NetworkAccessPolicy Description }}</span></span>

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

### <span data-ttu-id="26306-150">-OsType</span><span class="sxs-lookup"><span data-stu-id="26306-150">-OsType</span></span>
<span data-ttu-id="26306-151">Specifica il tipo di sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="26306-151">Specifies the OS type.</span></span>

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

### <span data-ttu-id="26306-152">-SkuName</span><span class="sxs-lookup"><span data-stu-id="26306-152">-SkuName</span></span>
<span data-ttu-id="26306-153">Specifica il nome SKU dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="26306-153">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="26306-154">I valori disponibili sono Standard_LRS, Premium_LRS, StandardSSD_LRS e UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="26306-154">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="26306-155">UltraSSD_LRS può essere usato solo con il valore Empty per il parametro CreateOption.</span><span class="sxs-lookup"><span data-stu-id="26306-155">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="26306-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="26306-156">-Tag</span></span>
<span data-ttu-id="26306-157">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="26306-157">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="26306-158">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="26306-158">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="26306-159">-Tier</span><span class="sxs-lookup"><span data-stu-id="26306-159">-Tier</span></span>
<span data-ttu-id="26306-160">Livello di prestazioni del disco.</span><span class="sxs-lookup"><span data-stu-id="26306-160">Performance tier of the disk.</span></span>

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

### <span data-ttu-id="26306-161">-Confermare</span><span class="sxs-lookup"><span data-stu-id="26306-161">-Confirm</span></span>
<span data-ttu-id="26306-162">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26306-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26306-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26306-163">-WhatIf</span></span>
<span data-ttu-id="26306-164">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="26306-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26306-165">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="26306-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26306-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26306-166">CommonParameters</span></span>
<span data-ttu-id="26306-167">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26306-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26306-168">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26306-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26306-169">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="26306-169">INPUTS</span></span>

### <span data-ttu-id="26306-170">System. String</span><span class="sxs-lookup"><span data-stu-id="26306-170">System.String</span></span>

### <span data-ttu-id="26306-171">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="26306-171">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="26306-172">System. Int32</span><span class="sxs-lookup"><span data-stu-id="26306-172">System.Int32</span></span>

### <span data-ttu-id="26306-173">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="26306-173">System.Collections.Hashtable</span></span>

### <span data-ttu-id="26306-174">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="26306-174">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="26306-175">Microsoft. Azure. Management. Compute. Models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="26306-175">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="26306-176">Microsoft. Azure. Management. Compute. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="26306-176">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="26306-177">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="26306-177">OUTPUTS</span></span>

### <span data-ttu-id="26306-178">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="26306-178">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="26306-179">Note</span><span class="sxs-lookup"><span data-stu-id="26306-179">NOTES</span></span>

## <span data-ttu-id="26306-180">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="26306-180">RELATED LINKS</span></span>
