---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDiskConfig.md
ms.openlocfilehash: b2c922a1dcce683636d61b68c66ab8cfb82535c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514504"
---
# <span data-ttu-id="ff8bd-101">New-AzureRmDiskConfig</span><span class="sxs-lookup"><span data-stu-id="ff8bd-101">New-AzureRmDiskConfig</span></span>

## <span data-ttu-id="ff8bd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ff8bd-102">SYNOPSIS</span></span>
<span data-ttu-id="ff8bd-103">Crea un oggetto disco configurabile.</span><span class="sxs-lookup"><span data-stu-id="ff8bd-103">Creates a configurable disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff8bd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ff8bd-104">SYNTAX</span></span>

```
New-AzureRmDiskConfig [-SkuName <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Tag <Hashtable>] [-CreateOption <DiskCreateOption>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff8bd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ff8bd-105">DESCRIPTION</span></span>
<span data-ttu-id="ff8bd-106">Il cmdlet **New-AzureRmDiskConfig** crea un oggetto disco configurabile.</span><span class="sxs-lookup"><span data-stu-id="ff8bd-106">The **New-AzureRmDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="ff8bd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ff8bd-107">EXAMPLES</span></span>

### <span data-ttu-id="ff8bd-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ff8bd-108">Example 1</span></span>
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

<span data-ttu-id="ff8bd-109">Il primo comando crea un oggetto disco locale vuoto con la dimensione 5GB in Standard_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ff8bd-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="ff8bd-110">Imposta anche il tipo di sistema operativo Windows e Abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="ff8bd-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="ff8bd-111">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia del disco e della chiave di crittografia per l'oggetto disco.</span><span class="sxs-lookup"><span data-stu-id="ff8bd-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="ff8bd-112">L'ultimo comando accetta l'oggetto disk e crea un disco con il nome "Disk01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="ff8bd-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="ff8bd-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ff8bd-113">PARAMETERS</span></span>

### <span data-ttu-id="ff8bd-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="ff8bd-114">-CreateOption</span></span>
<span data-ttu-id="ff8bd-115">Specifica se questo cmdlet crea un disco nella macchina virtuale da una piattaforma o da un'immagine utente, crea un disco vuoto o allega un disco esistente.</span><span class="sxs-lookup"><span data-stu-id="ff8bd-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="ff8bd-116">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="ff8bd-116">-DiskEncryptionKey</span></span>
<span data-ttu-id="ff8bd-117">Specifica l'oggetto chiave di crittografia del disco in un disco.</span><span class="sxs-lookup"><span data-stu-id="ff8bd-117">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="ff8bd-118">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="ff8bd-118">-DiskSizeGB</span></span>
<span data-ttu-id="ff8bd-119">Specifica le dimensioni del disco in GB.</span><span class="sxs-lookup"><span data-stu-id="ff8bd-119">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="ff8bd-120">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="ff8bd-120">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="ff8bd-121">Abilitare le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="ff8bd-121">Enable encryption settings.</span></span>

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

### <span data-ttu-id="ff8bd-122">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="ff8bd-122">-ImageReference</span></span>
<span data-ttu-id="ff8bd-123">Specifica il riferimento alle immagini in un disco.</span><span class="sxs-lookup"><span data-stu-id="ff8bd-123">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="ff8bd-124">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="ff8bd-124">-KeyEncryptionKey</span></span>
<span data-ttu-id="ff8bd-125">Specifica la chiave di crittografia chiave in un disco.</span><span class="sxs-lookup"><span data-stu-id="ff8bd-125">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="ff8bd-126">-Posizione</span><span class="sxs-lookup"><span data-stu-id="ff8bd-126">-Location</span></span>
<span data-ttu-id="ff8bd-127">Specifica una posizione.</span><span class="sxs-lookup"><span data-stu-id="ff8bd-127">Specifies a location.</span></span>

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

### <span data-ttu-id="ff8bd-128">-OsType</span><span class="sxs-lookup"><span data-stu-id="ff8bd-128">-OsType</span></span>
<span data-ttu-id="ff8bd-129">Specifica il tipo di sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ff8bd-129">Specifies the OS type.</span></span>

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

### <span data-ttu-id="ff8bd-130">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ff8bd-130">-SkuName</span></span>
<span data-ttu-id="ff8bd-131">Specifica il nome SKU dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ff8bd-131">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="ff8bd-132">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="ff8bd-132">-SourceResourceId</span></span>
<span data-ttu-id="ff8bd-133">Specifica l'ID risorsa di origine.</span><span class="sxs-lookup"><span data-stu-id="ff8bd-133">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="ff8bd-134">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="ff8bd-134">-SourceUri</span></span>
<span data-ttu-id="ff8bd-135">Specifica l'URI di origine.</span><span class="sxs-lookup"><span data-stu-id="ff8bd-135">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="ff8bd-136">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="ff8bd-136">-StorageAccountId</span></span>
<span data-ttu-id="ff8bd-137">Specifica l'ID account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ff8bd-137">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="ff8bd-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="ff8bd-138">-Tag</span></span>
<span data-ttu-id="ff8bd-139">Specifica che le risorse e i gruppi di risorse possono essere contrassegnati con un set di coppie nome/valore.</span><span class="sxs-lookup"><span data-stu-id="ff8bd-139">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>

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

### <span data-ttu-id="ff8bd-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ff8bd-140">-Confirm</span></span>
<span data-ttu-id="ff8bd-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff8bd-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff8bd-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff8bd-142">-WhatIf</span></span>
<span data-ttu-id="ff8bd-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ff8bd-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ff8bd-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ff8bd-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff8bd-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff8bd-145">CommonParameters</span></span>
<span data-ttu-id="ff8bd-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff8bd-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff8bd-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff8bd-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff8bd-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ff8bd-148">INPUTS</span></span>

### <span data-ttu-id="ff8bd-149">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. StorageAccountTypes, Microsoft. Azure. Management. Compute, Version = 14.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="ff8bd-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>
<span data-ttu-id="ff8bd-150">System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] System. String System. Collections. Hashtable System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable` 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] Microsoft. Azure. Management. Compute. Models. KeyVaultAndSecretReference Microsoft. Azure. Management. Compute. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="ff8bd-150">System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.String System.Collections.Hashtable System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="ff8bd-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ff8bd-151">OUTPUTS</span></span>

### <span data-ttu-id="ff8bd-152">Microsoft. Azure. Management. Compute. Models. disk</span><span class="sxs-lookup"><span data-stu-id="ff8bd-152">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="ff8bd-153">Note</span><span class="sxs-lookup"><span data-stu-id="ff8bd-153">NOTES</span></span>

## <span data-ttu-id="ff8bd-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ff8bd-154">RELATED LINKS</span></span>

