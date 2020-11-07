---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmDiskConfig.md
ms.openlocfilehash: 693d121bac5a618c5ad588cf4d34f63d8c6d0fd4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686465"
---
# <span data-ttu-id="03fd4-101">New-AzureRmDiskConfig</span><span class="sxs-lookup"><span data-stu-id="03fd4-101">New-AzureRmDiskConfig</span></span>

## <span data-ttu-id="03fd4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="03fd4-102">SYNOPSIS</span></span>
<span data-ttu-id="03fd4-103">Crea un oggetto disco configurabile.</span><span class="sxs-lookup"><span data-stu-id="03fd4-103">Creates a configurable disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03fd4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="03fd4-104">SYNTAX</span></span>

```
New-AzureRmDiskConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-Zone <String[]>] [-DiskIOPSReadWrite <Int32>] [-DiskMBpsReadWrite <Int32>]
 [-Tag <Hashtable>] [-CreateOption <String>] [-StorageAccountId <String>]
 [-ImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="03fd4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="03fd4-105">DESCRIPTION</span></span>
<span data-ttu-id="03fd4-106">Il cmdlet **New-AzureRmDiskConfig** crea un oggetto disco configurabile.</span><span class="sxs-lookup"><span data-stu-id="03fd4-106">The **New-AzureRmDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="03fd4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="03fd4-107">EXAMPLES</span></span>

### <span data-ttu-id="03fd4-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="03fd4-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzureRmDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzureRmDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="03fd4-109">Il primo comando crea un oggetto disco locale vuoto con la dimensione 5GB in Standard_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="03fd4-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="03fd4-110">Imposta anche il tipo di sistema operativo Windows e Abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="03fd4-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="03fd4-111">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia del disco e della chiave di crittografia per l'oggetto disco.</span><span class="sxs-lookup"><span data-stu-id="03fd4-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="03fd4-112">L'ultimo comando accetta l'oggetto disk e crea un disco con il nome "Disk01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="03fd4-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="03fd4-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="03fd4-113">PARAMETERS</span></span>

### <span data-ttu-id="03fd4-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="03fd4-114">-CreateOption</span></span>
<span data-ttu-id="03fd4-115">Specifica se questo cmdlet crea un disco nella macchina virtuale da una piattaforma o da un'immagine utente, crea un disco vuoto o allega un disco esistente.</span><span class="sxs-lookup"><span data-stu-id="03fd4-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="03fd4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03fd4-116">-DefaultProfile</span></span>
<span data-ttu-id="03fd4-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="03fd4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03fd4-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="03fd4-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="03fd4-119">Specifica l'oggetto chiave di crittografia del disco in un disco.</span><span class="sxs-lookup"><span data-stu-id="03fd4-119">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="03fd4-120">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="03fd4-120">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="03fd4-121">Numero di IOPS consentiti per il disco; impostabile solo per i dischi UltraSSD.</span><span class="sxs-lookup"><span data-stu-id="03fd4-121">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="03fd4-122">Un'operazione può essere trasferita tra 4K e 256K byte.</span><span class="sxs-lookup"><span data-stu-id="03fd4-122">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="03fd4-123">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="03fd4-123">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="03fd4-124">Larghezza di banda consentita per questo disco; impostabile solo per i dischi UltraSSD.</span><span class="sxs-lookup"><span data-stu-id="03fd4-124">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="03fd4-125">MBps significa milioni di byte al secondo MB Usa la notazione ISO, di poteri di 10.</span><span class="sxs-lookup"><span data-stu-id="03fd4-125">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="03fd4-126">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="03fd4-126">-DiskSizeGB</span></span>
<span data-ttu-id="03fd4-127">Specifica le dimensioni del disco in GB.</span><span class="sxs-lookup"><span data-stu-id="03fd4-127">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="03fd4-128">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="03fd4-128">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="03fd4-129">Abilitare le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="03fd4-129">Enable encryption settings.</span></span>

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

### <span data-ttu-id="03fd4-130">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="03fd4-130">-ImageReference</span></span>
<span data-ttu-id="03fd4-131">Specifica il riferimento alle immagini in un disco.</span><span class="sxs-lookup"><span data-stu-id="03fd4-131">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="03fd4-132">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="03fd4-132">-KeyEncryptionKey</span></span>
<span data-ttu-id="03fd4-133">Specifica la chiave di crittografia chiave in un disco.</span><span class="sxs-lookup"><span data-stu-id="03fd4-133">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="03fd4-134">-Posizione</span><span class="sxs-lookup"><span data-stu-id="03fd4-134">-Location</span></span>
<span data-ttu-id="03fd4-135">Specifica una posizione.</span><span class="sxs-lookup"><span data-stu-id="03fd4-135">Specifies a location.</span></span>

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

### <span data-ttu-id="03fd4-136">-OsType</span><span class="sxs-lookup"><span data-stu-id="03fd4-136">-OsType</span></span>
<span data-ttu-id="03fd4-137">Specifica il tipo di sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="03fd4-137">Specifies the OS type.</span></span>

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

### <span data-ttu-id="03fd4-138">-SkuName</span><span class="sxs-lookup"><span data-stu-id="03fd4-138">-SkuName</span></span>
<span data-ttu-id="03fd4-139">Specifica il nome SKU dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="03fd4-139">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="03fd4-140">I valori disponibili sono Standard_LRS, Premium_LRS, StandardSSD_LRS e UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="03fd4-140">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="03fd4-141">UltraSSD_LRS può essere usato solo con il valore Empty per il parametro CreateOption.</span><span class="sxs-lookup"><span data-stu-id="03fd4-141">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="03fd4-142">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="03fd4-142">-SourceResourceId</span></span>
<span data-ttu-id="03fd4-143">Specifica l'ID risorsa di origine.</span><span class="sxs-lookup"><span data-stu-id="03fd4-143">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="03fd4-144">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="03fd4-144">-SourceUri</span></span>
<span data-ttu-id="03fd4-145">Specifica l'URI di origine.</span><span class="sxs-lookup"><span data-stu-id="03fd4-145">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="03fd4-146">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="03fd4-146">-StorageAccountId</span></span>
<span data-ttu-id="03fd4-147">Specifica l'ID account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="03fd4-147">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="03fd4-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="03fd4-148">-Tag</span></span>
<span data-ttu-id="03fd4-149">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="03fd4-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="03fd4-150">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="03fd4-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="03fd4-151">-Zona</span><span class="sxs-lookup"><span data-stu-id="03fd4-151">-Zone</span></span>
<span data-ttu-id="03fd4-152">Specifica l'elenco delle aree logiche per il disco.</span><span class="sxs-lookup"><span data-stu-id="03fd4-152">Specifies the logical zone list for Disk.</span></span>

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

### <span data-ttu-id="03fd4-153">-Confermare</span><span class="sxs-lookup"><span data-stu-id="03fd4-153">-Confirm</span></span>
<span data-ttu-id="03fd4-154">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03fd4-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03fd4-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03fd4-155">-WhatIf</span></span>
<span data-ttu-id="03fd4-156">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="03fd4-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="03fd4-157">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="03fd4-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03fd4-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03fd4-158">CommonParameters</span></span>
<span data-ttu-id="03fd4-159">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03fd4-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03fd4-160">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03fd4-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03fd4-161">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="03fd4-161">INPUTS</span></span>

### <span data-ttu-id="03fd4-162">System. String</span><span class="sxs-lookup"><span data-stu-id="03fd4-162">System.String</span></span>

### <span data-ttu-id="03fd4-163">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes, Microsoft. Azure. Management. Compute, Version = 21.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="03fd4-163">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="03fd4-164">System. Int32</span><span class="sxs-lookup"><span data-stu-id="03fd4-164">System.Int32</span></span>

### <span data-ttu-id="03fd4-165">System. String []</span><span class="sxs-lookup"><span data-stu-id="03fd4-165">System.String[]</span></span>

### <span data-ttu-id="03fd4-166">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="03fd4-166">System.Collections.Hashtable</span></span>

### <span data-ttu-id="03fd4-167">Microsoft. Azure. Management. Compute. Models. ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="03fd4-167">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="03fd4-168">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="03fd4-168">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="03fd4-169">Microsoft. Azure. Management. Compute. Models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="03fd4-169">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="03fd4-170">Microsoft. Azure. Management. Compute. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="03fd4-170">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="03fd4-171">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="03fd4-171">OUTPUTS</span></span>

### <span data-ttu-id="03fd4-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="03fd4-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="03fd4-173">Note</span><span class="sxs-lookup"><span data-stu-id="03fd4-173">NOTES</span></span>

## <span data-ttu-id="03fd4-174">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="03fd4-174">RELATED LINKS</span></span>
