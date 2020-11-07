---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmSnapshotConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmSnapshotConfig.md
ms.openlocfilehash: ee3dd849a8f3877ac19ce86a7257d28fc18575c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686217"
---
# <span data-ttu-id="148d6-101">New-AzureRmSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="148d6-101">New-AzureRmSnapshotConfig</span></span>

## <span data-ttu-id="148d6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="148d6-102">SYNOPSIS</span></span>
<span data-ttu-id="148d6-103">Crea un oggetto snapshot configurabile.</span><span class="sxs-lookup"><span data-stu-id="148d6-103">Creates a configurable snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="148d6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="148d6-104">SYNTAX</span></span>

```
New-AzureRmSnapshotConfig [-SkuName <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Tag <Hashtable>] [-CreateOption <DiskCreateOption>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="148d6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="148d6-105">DESCRIPTION</span></span>
<span data-ttu-id="148d6-106">Il cmdlet **New-AzureRmSnapshotConfig** crea un oggetto snapshot configurabile.</span><span class="sxs-lookup"><span data-stu-id="148d6-106">The **New-AzureRmSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="148d6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="148d6-107">EXAMPLES</span></span>

### <span data-ttu-id="148d6-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="148d6-108">Example 1</span></span>
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

<span data-ttu-id="148d6-109">Il primo comando crea un oggetto snapshot locale vuoto con la dimensione 5GB in Standard_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="148d6-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="148d6-110">Imposta anche il tipo di sistema operativo Windows e Abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="148d6-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="148d6-111">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia del disco e della chiave di crittografia per l'oggetto snapshot.</span><span class="sxs-lookup"><span data-stu-id="148d6-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="148d6-112">L'ultimo comando accetta l'oggetto snapshot e crea uno snapshot con il nome "Snapshot01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="148d6-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="148d6-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="148d6-113">PARAMETERS</span></span>

### <span data-ttu-id="148d6-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="148d6-114">-CreateOption</span></span>
<span data-ttu-id="148d6-115">Specifica se questo cmdlet crea un disco nella macchina virtuale da una piattaforma o da un'immagine utente, crea un disco vuoto o allega un disco esistente.</span><span class="sxs-lookup"><span data-stu-id="148d6-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

```yaml
Type: DiskCreateOption
Parameter Sets: (All)
Aliases: 
Accepted values: Empty, Attach, FromImage, Import, Copy, Restore

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="148d6-116">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="148d6-116">-DiskEncryptionKey</span></span>
<span data-ttu-id="148d6-117">Specifica l'oggetto chiave di crittografia del disco in uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="148d6-117">Specifies the disk encryption key object on a snapshot.</span></span>

```yaml
Type: KeyVaultAndSecretReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="148d6-118">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="148d6-118">-DiskSizeGB</span></span>
<span data-ttu-id="148d6-119">Specifica le dimensioni del disco in GB.</span><span class="sxs-lookup"><span data-stu-id="148d6-119">Specifies the size of the disk in GB.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="148d6-120">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="148d6-120">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="148d6-121">Abilitare le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="148d6-121">Enable encryption settings.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="148d6-122">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="148d6-122">-ImageReference</span></span>
<span data-ttu-id="148d6-123">Specifica il riferimento alle immagini in uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="148d6-123">Specifies the image reference on a snapshot.</span></span>

```yaml
Type: ImageDiskReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="148d6-124">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="148d6-124">-KeyEncryptionKey</span></span>
<span data-ttu-id="148d6-125">Specifica la chiave di crittografia chiave in uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="148d6-125">Specifies the Key encryption key on a snapshot.</span></span>

```yaml
Type: KeyVaultAndKeyReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="148d6-126">-Posizione</span><span class="sxs-lookup"><span data-stu-id="148d6-126">-Location</span></span>
<span data-ttu-id="148d6-127">Specifica una posizione.</span><span class="sxs-lookup"><span data-stu-id="148d6-127">Specifies a location.</span></span>

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

### <span data-ttu-id="148d6-128">-OsType</span><span class="sxs-lookup"><span data-stu-id="148d6-128">-OsType</span></span>
<span data-ttu-id="148d6-129">Specifica il tipo di sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="148d6-129">Specifies the OS type.</span></span>

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

### <span data-ttu-id="148d6-130">-SkuName</span><span class="sxs-lookup"><span data-stu-id="148d6-130">-SkuName</span></span>
<span data-ttu-id="148d6-131">Specifica il nome SKU dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="148d6-131">Specifies the Sku name of the storage account.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="148d6-132">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="148d6-132">-SourceResourceId</span></span>
<span data-ttu-id="148d6-133">Specifica l'ID risorsa di origine.</span><span class="sxs-lookup"><span data-stu-id="148d6-133">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="148d6-134">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="148d6-134">-SourceUri</span></span>
<span data-ttu-id="148d6-135">Specifica l'URI di origine.</span><span class="sxs-lookup"><span data-stu-id="148d6-135">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="148d6-136">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="148d6-136">-StorageAccountId</span></span>
<span data-ttu-id="148d6-137">Specifica l'ID account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="148d6-137">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="148d6-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="148d6-138">-Tag</span></span>
<span data-ttu-id="148d6-139">Specifica che le risorse e i gruppi di risorse possono essere contrassegnati con un set di coppie nome/valore.</span><span class="sxs-lookup"><span data-stu-id="148d6-139">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="148d6-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="148d6-140">-Confirm</span></span>
<span data-ttu-id="148d6-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="148d6-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="148d6-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="148d6-142">-WhatIf</span></span>
<span data-ttu-id="148d6-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="148d6-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="148d6-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="148d6-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="148d6-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="148d6-145">CommonParameters</span></span>
<span data-ttu-id="148d6-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="148d6-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="148d6-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="148d6-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="148d6-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="148d6-148">INPUTS</span></span>

### <span data-ttu-id="148d6-149">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. StorageAccountTypes, Microsoft. Azure. Management. Compute, Version = 14.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="148d6-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>
<span data-ttu-id="148d6-150">System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] System. String System. Collections. Hashtable System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable` 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] Microsoft. Azure. Management. Compute. Models. KeyVaultAndSecretReference Microsoft. Azure. Management. Compute. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="148d6-150">System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.String System.Collections.Hashtable System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="148d6-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="148d6-151">OUTPUTS</span></span>

### <span data-ttu-id="148d6-152">Microsoft. Azure. Management. Compute. Models. snapshot</span><span class="sxs-lookup"><span data-stu-id="148d6-152">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="148d6-153">Note</span><span class="sxs-lookup"><span data-stu-id="148d6-153">NOTES</span></span>

## <span data-ttu-id="148d6-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="148d6-154">RELATED LINKS</span></span>

