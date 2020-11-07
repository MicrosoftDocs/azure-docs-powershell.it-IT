---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermsnapshotconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmSnapshotConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmSnapshotConfig.md
ms.openlocfilehash: 2050536a39c8ebcd5a1269709d25af100cc251b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686464"
---
# <span data-ttu-id="fcffb-101">New-AzureRmSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="fcffb-101">New-AzureRmSnapshotConfig</span></span>

## <span data-ttu-id="fcffb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fcffb-102">SYNOPSIS</span></span>
<span data-ttu-id="fcffb-103">Crea un oggetto snapshot configurabile.</span><span class="sxs-lookup"><span data-stu-id="fcffb-103">Creates a configurable snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fcffb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fcffb-104">SYNTAX</span></span>

```
New-AzureRmSnapshotConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-Tag <Hashtable>] [-CreateOption <String>] [-StorageAccountId <String>]
 [-ImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fcffb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fcffb-105">DESCRIPTION</span></span>
<span data-ttu-id="fcffb-106">Il cmdlet **New-AzureRmSnapshotConfig** crea un oggetto snapshot configurabile.</span><span class="sxs-lookup"><span data-stu-id="fcffb-106">The **New-AzureRmSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="fcffb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fcffb-107">EXAMPLES</span></span>

### <span data-ttu-id="fcffb-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fcffb-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzureRmSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzureRmSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzureRmSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="fcffb-109">Il primo comando crea un oggetto snapshot locale vuoto con la dimensione 5GB in Standard_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="fcffb-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="fcffb-110">Imposta anche il tipo di sistema operativo Windows e Abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="fcffb-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="fcffb-111">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia del disco e della chiave di crittografia per l'oggetto snapshot.</span><span class="sxs-lookup"><span data-stu-id="fcffb-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="fcffb-112">L'ultimo comando accetta l'oggetto snapshot e crea uno snapshot con il nome "Snapshot01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="fcffb-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="fcffb-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fcffb-113">PARAMETERS</span></span>

### <span data-ttu-id="fcffb-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="fcffb-114">-CreateOption</span></span>
<span data-ttu-id="fcffb-115">Specifica se questo cmdlet crea un disco nella macchina virtuale da una piattaforma o da un'immagine utente, crea un disco vuoto o allega un disco esistente.</span><span class="sxs-lookup"><span data-stu-id="fcffb-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="fcffb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcffb-116">-DefaultProfile</span></span>
<span data-ttu-id="fcffb-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fcffb-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fcffb-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="fcffb-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="fcffb-119">Specifica l'oggetto chiave di crittografia del disco in uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="fcffb-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="fcffb-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="fcffb-120">-DiskSizeGB</span></span>
<span data-ttu-id="fcffb-121">Specifica le dimensioni del disco in GB.</span><span class="sxs-lookup"><span data-stu-id="fcffb-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="fcffb-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="fcffb-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="fcffb-123">Abilitare le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="fcffb-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="fcffb-124">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="fcffb-124">-ImageReference</span></span>
<span data-ttu-id="fcffb-125">Specifica il riferimento alle immagini in uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="fcffb-125">Specifies the image reference on a snapshot.</span></span>

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

### <span data-ttu-id="fcffb-126">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="fcffb-126">-KeyEncryptionKey</span></span>
<span data-ttu-id="fcffb-127">Specifica la chiave di crittografia chiave in uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="fcffb-127">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="fcffb-128">-Posizione</span><span class="sxs-lookup"><span data-stu-id="fcffb-128">-Location</span></span>
<span data-ttu-id="fcffb-129">Specifica una posizione.</span><span class="sxs-lookup"><span data-stu-id="fcffb-129">Specifies a location.</span></span>

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

### <span data-ttu-id="fcffb-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="fcffb-130">-OsType</span></span>
<span data-ttu-id="fcffb-131">Specifica il tipo di sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="fcffb-131">Specifies the OS type.</span></span>

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

### <span data-ttu-id="fcffb-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="fcffb-132">-SkuName</span></span>
<span data-ttu-id="fcffb-133">Specifica il nome SKU dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="fcffb-133">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="fcffb-134">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="fcffb-134">-SourceResourceId</span></span>
<span data-ttu-id="fcffb-135">Specifica l'ID risorsa di origine.</span><span class="sxs-lookup"><span data-stu-id="fcffb-135">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="fcffb-136">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="fcffb-136">-SourceUri</span></span>
<span data-ttu-id="fcffb-137">Specifica l'URI di origine.</span><span class="sxs-lookup"><span data-stu-id="fcffb-137">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="fcffb-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="fcffb-138">-StorageAccountId</span></span>
<span data-ttu-id="fcffb-139">Specifica l'ID account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="fcffb-139">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="fcffb-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="fcffb-140">-Tag</span></span>
<span data-ttu-id="fcffb-141">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="fcffb-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="fcffb-142">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="fcffb-142">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="fcffb-143">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fcffb-143">-Confirm</span></span>
<span data-ttu-id="fcffb-144">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fcffb-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcffb-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcffb-145">-WhatIf</span></span>
<span data-ttu-id="fcffb-146">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fcffb-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fcffb-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fcffb-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcffb-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcffb-148">CommonParameters</span></span>
<span data-ttu-id="fcffb-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcffb-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcffb-150">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcffb-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcffb-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fcffb-151">INPUTS</span></span>

### <span data-ttu-id="fcffb-152">System. String</span><span class="sxs-lookup"><span data-stu-id="fcffb-152">System.String</span></span>

### <span data-ttu-id="fcffb-153">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes, Microsoft. Azure. Management. Compute, Version = 21.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="fcffb-153">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="fcffb-154">System. Int32</span><span class="sxs-lookup"><span data-stu-id="fcffb-154">System.Int32</span></span>

### <span data-ttu-id="fcffb-155">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="fcffb-155">System.Collections.Hashtable</span></span>

### <span data-ttu-id="fcffb-156">Microsoft. Azure. Management. Compute. Models. ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="fcffb-156">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="fcffb-157">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="fcffb-157">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="fcffb-158">Microsoft. Azure. Management. Compute. Models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="fcffb-158">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="fcffb-159">Microsoft. Azure. Management. Compute. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="fcffb-159">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="fcffb-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fcffb-160">OUTPUTS</span></span>

### <span data-ttu-id="fcffb-161">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="fcffb-161">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="fcffb-162">Note</span><span class="sxs-lookup"><span data-stu-id="fcffb-162">NOTES</span></span>

## <span data-ttu-id="fcffb-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fcffb-163">RELATED LINKS</span></span>
