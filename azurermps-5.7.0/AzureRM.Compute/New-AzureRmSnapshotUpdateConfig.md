---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmSnapshotUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmSnapshotUpdateConfig.md
ms.openlocfilehash: 97bfd93babc75b09f87e53f62c60cd4fb08ea599
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516867"
---
# <span data-ttu-id="2d8a3-101">New-AzureRmSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="2d8a3-101">New-AzureRmSnapshotUpdateConfig</span></span>

## <span data-ttu-id="2d8a3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2d8a3-102">SYNOPSIS</span></span>
<span data-ttu-id="2d8a3-103">Crea un oggetto di aggiornamento istantaneo configurabile.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-103">Creates a configurable snapshot update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d8a3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2d8a3-104">SYNTAX</span></span>

```
New-AzureRmSnapshotUpdateConfig [-SkuName <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-CreateOption <DiskCreateOption>] [-StorageAccountId <String>]
 [-ImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d8a3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2d8a3-105">DESCRIPTION</span></span>
<span data-ttu-id="2d8a3-106">Il cmdlet **New-AzureRmSnapshotUpdateConfig** crea un oggetto di aggiornamento istantaneo configurabile.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-106">The **New-AzureRmSnapshotUpdateConfig** cmdlet creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="2d8a3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2d8a3-107">EXAMPLES</span></span>

### <span data-ttu-id="2d8a3-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2d8a3-108">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateDiskEncryptionKey -SnapshotUpdate $snapshotupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateKeyEncryptionKey -SnapshotUpdate $snapshotupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="2d8a3-109">Il primo comando crea un oggetto aggiornamento snapshot locale vuoto con dimensioni 10GB in Premium_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="2d8a3-110">Imposta anche il tipo di sistema operativo Windows e Abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="2d8a3-111">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia del disco e della chiave di crittografia per l'oggetto aggiornamento snapshot.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="2d8a3-112">L'ultimo comando accetta l'oggetto Update dello snapshot e aggiorna uno snapshot esistente con il nome "Snapshot01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="2d8a3-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="2d8a3-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="2d8a3-113">Example 2</span></span>
```
PS C:\> New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="2d8a3-114">Questo comando Aggiorna uno snapshot esistente con il nome "Snapshot01" nel gruppo di risorse "ResourceGroup01" in dimensioni del disco di 10 GB.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-114">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="2d8a3-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2d8a3-115">PARAMETERS</span></span>

### <span data-ttu-id="2d8a3-116">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="2d8a3-116">-CreateOption</span></span>
<span data-ttu-id="2d8a3-117">Specifica se questo cmdlet crea uno snapshot nella macchina virtuale da una piattaforma o da un'immagine utente, crea un disco vuoto o allega un disco esistente.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-117">Specifies whether this cmdlet creates a snapshot in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="2d8a3-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="2d8a3-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="2d8a3-119">Specifica l'oggetto chiave di crittografia del disco in uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="2d8a3-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="2d8a3-120">-DiskSizeGB</span></span>
<span data-ttu-id="2d8a3-121">Specifica le dimensioni del disco in GB.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="2d8a3-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="2d8a3-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="2d8a3-123">Abilitare le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="2d8a3-124">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="2d8a3-124">-ImageReference</span></span>
<span data-ttu-id="2d8a3-125">Specifica il riferimento alle immagini in uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-125">Specifies the image reference on a snapshot.</span></span>

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

### <span data-ttu-id="2d8a3-126">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="2d8a3-126">-KeyEncryptionKey</span></span>
<span data-ttu-id="2d8a3-127">Specifica la chiave di crittografia chiave in uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-127">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="2d8a3-128">-OsType</span><span class="sxs-lookup"><span data-stu-id="2d8a3-128">-OsType</span></span>
<span data-ttu-id="2d8a3-129">Specifica il tipo di sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-129">Specifies the OS type.</span></span>

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

### <span data-ttu-id="2d8a3-130">-SkuName</span><span class="sxs-lookup"><span data-stu-id="2d8a3-130">-SkuName</span></span>
<span data-ttu-id="2d8a3-131">Specifica il nome SKU dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-131">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="2d8a3-132">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="2d8a3-132">-SourceResourceId</span></span>
<span data-ttu-id="2d8a3-133">Specifica l'ID risorsa di origine.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-133">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="2d8a3-134">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="2d8a3-134">-SourceUri</span></span>
<span data-ttu-id="2d8a3-135">Specifica l'URI di origine.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-135">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="2d8a3-136">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="2d8a3-136">-StorageAccountId</span></span>
<span data-ttu-id="2d8a3-137">Specifica l'ID account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-137">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="2d8a3-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="2d8a3-138">-Tag</span></span>
<span data-ttu-id="2d8a3-139">Specifica che le risorse e i gruppi di risorse possono essere contrassegnati con un set di coppie nome/valore.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-139">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d8a3-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2d8a3-140">-Confirm</span></span>
<span data-ttu-id="2d8a3-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d8a3-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d8a3-142">-WhatIf</span></span>
<span data-ttu-id="2d8a3-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2d8a3-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d8a3-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d8a3-145">CommonParameters</span></span>
<span data-ttu-id="2d8a3-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d8a3-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d8a3-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d8a3-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d8a3-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2d8a3-148">INPUTS</span></span>

### <span data-ttu-id="2d8a3-149">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. StorageAccountTypes, Microsoft. Azure. Management. Compute, Version = 14.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="2d8a3-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>
<span data-ttu-id="2d8a3-150">Sistema. Nullable `1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] System. Collections. Hashtable System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.String
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable` 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] Microsoft. Azure. Management. Compute. Models. KeyVaultAndSecretReference Microsoft. Azure. Management. Compute. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="2d8a3-150">System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.Collections.Hashtable System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.String
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="2d8a3-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2d8a3-151">OUTPUTS</span></span>

### <span data-ttu-id="2d8a3-152">Microsoft. Azure. Management. Compute. Models. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="2d8a3-152">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>

## <span data-ttu-id="2d8a3-153">Note</span><span class="sxs-lookup"><span data-stu-id="2d8a3-153">NOTES</span></span>

## <span data-ttu-id="2d8a3-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2d8a3-154">RELATED LINKS</span></span>

