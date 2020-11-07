---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermsnapshotconfig
schema: 2.0.0
ms.openlocfilehash: a18eb8513e419d174efac9179cb65fe175d12dd1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866913"
---
# <span data-ttu-id="36b24-101">New-AzureRmSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="36b24-101">New-AzureRmSnapshotConfig</span></span>

## <span data-ttu-id="36b24-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="36b24-102">SYNOPSIS</span></span>
<span data-ttu-id="36b24-103">Crea un oggetto snapshot configurabile.</span><span class="sxs-lookup"><span data-stu-id="36b24-103">Creates a configurable snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36b24-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="36b24-104">SYNTAX</span></span>

```
New-AzureRmSnapshotConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Tag <Hashtable>] [-CreateOption <DiskCreateOption>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36b24-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="36b24-105">DESCRIPTION</span></span>
<span data-ttu-id="36b24-106">Il cmdlet **New-AzureRmSnapshotConfig** crea un oggetto snapshot configurabile.</span><span class="sxs-lookup"><span data-stu-id="36b24-106">The **New-AzureRmSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="36b24-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="36b24-107">EXAMPLES</span></span>

### <span data-ttu-id="36b24-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="36b24-108">Example 1</span></span>
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

<span data-ttu-id="36b24-109">Il primo comando crea un oggetto snapshot locale vuoto con la dimensione 5GB in Standard_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="36b24-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="36b24-110">Imposta anche il tipo di sistema operativo Windows e Abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="36b24-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="36b24-111">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia del disco e della chiave di crittografia per l'oggetto snapshot.</span><span class="sxs-lookup"><span data-stu-id="36b24-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="36b24-112">L'ultimo comando accetta l'oggetto snapshot e crea uno snapshot con il nome "Snapshot01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="36b24-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="36b24-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="36b24-113">PARAMETERS</span></span>

### <span data-ttu-id="36b24-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="36b24-114">-CreateOption</span></span>
<span data-ttu-id="36b24-115">Specifica se questo cmdlet crea un disco nella macchina virtuale da una piattaforma o da un'immagine utente, crea un disco vuoto o allega un disco esistente.</span><span class="sxs-lookup"><span data-stu-id="36b24-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

```yaml
Type: DiskCreateOption
Parameter Sets: (All)
Aliases: 
Accepted values: Empty, Attach, FromImage, Import, Copy

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36b24-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36b24-116">-DefaultProfile</span></span>
<span data-ttu-id="36b24-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="36b24-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36b24-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="36b24-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="36b24-119">Specifica l'oggetto chiave di crittografia del disco in uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="36b24-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="36b24-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="36b24-120">-DiskSizeGB</span></span>
<span data-ttu-id="36b24-121">Specifica le dimensioni del disco in GB.</span><span class="sxs-lookup"><span data-stu-id="36b24-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="36b24-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="36b24-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="36b24-123">Abilitare le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="36b24-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="36b24-124">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="36b24-124">-ImageReference</span></span>
<span data-ttu-id="36b24-125">Specifica il riferimento alle immagini in uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="36b24-125">Specifies the image reference on a snapshot.</span></span>

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

### <span data-ttu-id="36b24-126">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="36b24-126">-KeyEncryptionKey</span></span>
<span data-ttu-id="36b24-127">Specifica la chiave di crittografia chiave in uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="36b24-127">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="36b24-128">-Posizione</span><span class="sxs-lookup"><span data-stu-id="36b24-128">-Location</span></span>
<span data-ttu-id="36b24-129">Specifica una posizione.</span><span class="sxs-lookup"><span data-stu-id="36b24-129">Specifies a location.</span></span>

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

### <span data-ttu-id="36b24-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="36b24-130">-OsType</span></span>
<span data-ttu-id="36b24-131">Specifica il tipo di sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="36b24-131">Specifies the OS type.</span></span>

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

### <span data-ttu-id="36b24-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="36b24-132">-SkuName</span></span>
<span data-ttu-id="36b24-133">Specifica il nome SKU dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="36b24-133">Specifies the Sku name of the storage account.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: AccountType
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36b24-134">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="36b24-134">-SourceResourceId</span></span>
<span data-ttu-id="36b24-135">Specifica l'ID risorsa di origine.</span><span class="sxs-lookup"><span data-stu-id="36b24-135">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="36b24-136">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="36b24-136">-SourceUri</span></span>
<span data-ttu-id="36b24-137">Specifica l'URI di origine.</span><span class="sxs-lookup"><span data-stu-id="36b24-137">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="36b24-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="36b24-138">-StorageAccountId</span></span>
<span data-ttu-id="36b24-139">Specifica l'ID account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="36b24-139">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="36b24-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="36b24-140">-Tag</span></span>
<span data-ttu-id="36b24-141">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="36b24-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="36b24-142">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="36b24-142">For example:</span></span>

<span data-ttu-id="36b24-143">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="36b24-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="36b24-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="36b24-144">-Confirm</span></span>
<span data-ttu-id="36b24-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36b24-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36b24-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36b24-146">-WhatIf</span></span>
<span data-ttu-id="36b24-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="36b24-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36b24-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="36b24-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36b24-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36b24-149">CommonParameters</span></span>
<span data-ttu-id="36b24-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36b24-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36b24-151">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36b24-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36b24-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="36b24-152">INPUTS</span></span>

### <span data-ttu-id="36b24-153">Nessuno</span><span class="sxs-lookup"><span data-stu-id="36b24-153">None</span></span>
<span data-ttu-id="36b24-154">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="36b24-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="36b24-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="36b24-155">OUTPUTS</span></span>

### <span data-ttu-id="36b24-156">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="36b24-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="36b24-157">Note</span><span class="sxs-lookup"><span data-stu-id="36b24-157">NOTES</span></span>

## <span data-ttu-id="36b24-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="36b24-158">RELATED LINKS</span></span>

