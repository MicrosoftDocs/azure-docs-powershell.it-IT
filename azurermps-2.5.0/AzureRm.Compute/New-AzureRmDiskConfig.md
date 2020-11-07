---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermdiskconfig
schema: 2.0.0
ms.openlocfilehash: 8249bbb354d660f335316da503b0f19b6576fea6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866370"
---
# <span data-ttu-id="74ec1-101">New-AzureRmDiskConfig</span><span class="sxs-lookup"><span data-stu-id="74ec1-101">New-AzureRmDiskConfig</span></span>

## <span data-ttu-id="74ec1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="74ec1-102">SYNOPSIS</span></span>
<span data-ttu-id="74ec1-103">Crea un oggetto disco configurabile.</span><span class="sxs-lookup"><span data-stu-id="74ec1-103">Creates a configurable disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74ec1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="74ec1-104">SYNTAX</span></span>

```
New-AzureRmDiskConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Zone <String[]>] [-Tag <Hashtable>]
 [-CreateOption <DiskCreateOption>] [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>]
 [-SourceUri <String>] [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74ec1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74ec1-105">DESCRIPTION</span></span>
<span data-ttu-id="74ec1-106">Il cmdlet **New-AzureRmDiskConfig** crea un oggetto disco configurabile.</span><span class="sxs-lookup"><span data-stu-id="74ec1-106">The **New-AzureRmDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="74ec1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="74ec1-107">EXAMPLES</span></span>

### <span data-ttu-id="74ec1-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="74ec1-108">Example 1</span></span>
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

<span data-ttu-id="74ec1-109">Il primo comando crea un oggetto disco locale vuoto con la dimensione 5GB in Standard_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="74ec1-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="74ec1-110">Imposta anche il tipo di sistema operativo Windows e Abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="74ec1-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="74ec1-111">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia del disco e della chiave di crittografia per l'oggetto disco.</span><span class="sxs-lookup"><span data-stu-id="74ec1-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="74ec1-112">L'ultimo comando accetta l'oggetto disk e crea un disco con il nome "Disk01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="74ec1-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="74ec1-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="74ec1-113">PARAMETERS</span></span>

### <span data-ttu-id="74ec1-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="74ec1-114">-CreateOption</span></span>
<span data-ttu-id="74ec1-115">Specifica se questo cmdlet crea un disco nella macchina virtuale da una piattaforma o da un'immagine utente, crea un disco vuoto o allega un disco esistente.</span><span class="sxs-lookup"><span data-stu-id="74ec1-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="74ec1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74ec1-116">-DefaultProfile</span></span>
<span data-ttu-id="74ec1-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="74ec1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74ec1-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="74ec1-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="74ec1-119">Specifica l'oggetto chiave di crittografia del disco in un disco.</span><span class="sxs-lookup"><span data-stu-id="74ec1-119">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="74ec1-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="74ec1-120">-DiskSizeGB</span></span>
<span data-ttu-id="74ec1-121">Specifica le dimensioni del disco in GB.</span><span class="sxs-lookup"><span data-stu-id="74ec1-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="74ec1-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="74ec1-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="74ec1-123">Abilitare le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="74ec1-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="74ec1-124">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="74ec1-124">-ImageReference</span></span>
<span data-ttu-id="74ec1-125">Specifica il riferimento alle immagini in un disco.</span><span class="sxs-lookup"><span data-stu-id="74ec1-125">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="74ec1-126">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="74ec1-126">-KeyEncryptionKey</span></span>
<span data-ttu-id="74ec1-127">Specifica la chiave di crittografia chiave in un disco.</span><span class="sxs-lookup"><span data-stu-id="74ec1-127">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="74ec1-128">-Posizione</span><span class="sxs-lookup"><span data-stu-id="74ec1-128">-Location</span></span>
<span data-ttu-id="74ec1-129">Specifica una posizione.</span><span class="sxs-lookup"><span data-stu-id="74ec1-129">Specifies a location.</span></span>

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

### <span data-ttu-id="74ec1-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="74ec1-130">-OsType</span></span>
<span data-ttu-id="74ec1-131">Specifica il tipo di sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="74ec1-131">Specifies the OS type.</span></span>

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

### <span data-ttu-id="74ec1-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="74ec1-132">-SkuName</span></span>
<span data-ttu-id="74ec1-133">Specifica il nome SKU dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="74ec1-133">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="74ec1-134">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="74ec1-134">-SourceResourceId</span></span>
<span data-ttu-id="74ec1-135">Specifica l'ID risorsa di origine.</span><span class="sxs-lookup"><span data-stu-id="74ec1-135">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="74ec1-136">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="74ec1-136">-SourceUri</span></span>
<span data-ttu-id="74ec1-137">Specifica l'URI di origine.</span><span class="sxs-lookup"><span data-stu-id="74ec1-137">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="74ec1-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="74ec1-138">-StorageAccountId</span></span>
<span data-ttu-id="74ec1-139">Specifica l'ID account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="74ec1-139">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="74ec1-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="74ec1-140">-Tag</span></span>
<span data-ttu-id="74ec1-141">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="74ec1-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="74ec1-142">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="74ec1-142">For example:</span></span>

<span data-ttu-id="74ec1-143">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="74ec1-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="74ec1-144">-Zona</span><span class="sxs-lookup"><span data-stu-id="74ec1-144">-Zone</span></span>
<span data-ttu-id="74ec1-145">Specifica l'elenco delle aree logiche per il disco.</span><span class="sxs-lookup"><span data-stu-id="74ec1-145">Specifies the logical zone list for Disk.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74ec1-146">-Confermare</span><span class="sxs-lookup"><span data-stu-id="74ec1-146">-Confirm</span></span>
<span data-ttu-id="74ec1-147">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74ec1-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74ec1-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74ec1-148">-WhatIf</span></span>
<span data-ttu-id="74ec1-149">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="74ec1-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="74ec1-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="74ec1-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74ec1-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74ec1-151">CommonParameters</span></span>
<span data-ttu-id="74ec1-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74ec1-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74ec1-153">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74ec1-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74ec1-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="74ec1-154">INPUTS</span></span>

### <span data-ttu-id="74ec1-155">Nessuno</span><span class="sxs-lookup"><span data-stu-id="74ec1-155">None</span></span>
<span data-ttu-id="74ec1-156">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="74ec1-156">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="74ec1-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="74ec1-157">OUTPUTS</span></span>

### <span data-ttu-id="74ec1-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="74ec1-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="74ec1-159">Note</span><span class="sxs-lookup"><span data-stu-id="74ec1-159">NOTES</span></span>

## <span data-ttu-id="74ec1-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="74ec1-160">RELATED LINKS</span></span>

