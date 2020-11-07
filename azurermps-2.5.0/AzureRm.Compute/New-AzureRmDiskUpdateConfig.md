---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermdiskupdateconfig
schema: 2.0.0
ms.openlocfilehash: 790d366ced8b9466a906df2d3f1717ad9277ca9f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866757"
---
# <span data-ttu-id="1ed0f-101">New-AzureRmDiskUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="1ed0f-101">New-AzureRmDiskUpdateConfig</span></span>

## <span data-ttu-id="1ed0f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1ed0f-102">SYNOPSIS</span></span>
<span data-ttu-id="1ed0f-103">Crea un oggetto di aggiornamento del disco configurabile.</span><span class="sxs-lookup"><span data-stu-id="1ed0f-103">Creates a configurable disk update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ed0f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1ed0f-104">SYNTAX</span></span>

```
New-AzureRmDiskUpdateConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ed0f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1ed0f-105">DESCRIPTION</span></span>
<span data-ttu-id="1ed0f-106">Il cmdlet **New-AzureRmDiskUpdateConfig** crea un oggetto di aggiornamento del disco configurabile.</span><span class="sxs-lookup"><span data-stu-id="1ed0f-106">The **New-AzureRmDiskUpdateConfig** cmdlet creates a configurable disk update object.</span></span>

## <span data-ttu-id="1ed0f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1ed0f-107">EXAMPLES</span></span>

### <span data-ttu-id="1ed0f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1ed0f-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzureRmDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="1ed0f-109">Il primo comando crea un oggetto di aggiornamento del disco vuoto locale con dimensioni 10GB in Premium_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1ed0f-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="1ed0f-110">Imposta anche il tipo di sistema operativo Windows e Abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="1ed0f-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="1ed0f-111">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia del disco e della chiave di crittografia per l'oggetto aggiornamento disco.</span><span class="sxs-lookup"><span data-stu-id="1ed0f-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="1ed0f-112">L'ultimo comando accetta l'oggetto Update del disco e aggiorna un disco esistente con il nome "Disk01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="1ed0f-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="1ed0f-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="1ed0f-113">Example 2</span></span>
```
PS C:\> New-AzureRmDiskUpdateConfig -DiskSizeGB 10 | Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="1ed0f-114">Questo comando aggiorna un disco esistente con il nome "Disk01" nel gruppo di risorse "ResourceGroup01" in dimensioni del disco di 10 GB.</span><span class="sxs-lookup"><span data-stu-id="1ed0f-114">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="1ed0f-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1ed0f-115">PARAMETERS</span></span>

### <span data-ttu-id="1ed0f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ed0f-116">-DefaultProfile</span></span>
<span data-ttu-id="1ed0f-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1ed0f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ed0f-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="1ed0f-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="1ed0f-119">Specifica l'oggetto chiave di crittografia del disco in un disco.</span><span class="sxs-lookup"><span data-stu-id="1ed0f-119">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="1ed0f-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="1ed0f-120">-DiskSizeGB</span></span>
<span data-ttu-id="1ed0f-121">Specifica le dimensioni del disco in GB.</span><span class="sxs-lookup"><span data-stu-id="1ed0f-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="1ed0f-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="1ed0f-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="1ed0f-123">Abilitare le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="1ed0f-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="1ed0f-124">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="1ed0f-124">-KeyEncryptionKey</span></span>
<span data-ttu-id="1ed0f-125">Specifica la chiave di crittografia chiave in un disco.</span><span class="sxs-lookup"><span data-stu-id="1ed0f-125">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="1ed0f-126">-OsType</span><span class="sxs-lookup"><span data-stu-id="1ed0f-126">-OsType</span></span>
<span data-ttu-id="1ed0f-127">Specifica il tipo di sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="1ed0f-127">Specifies the OS type.</span></span>

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

### <span data-ttu-id="1ed0f-128">-SkuName</span><span class="sxs-lookup"><span data-stu-id="1ed0f-128">-SkuName</span></span>
<span data-ttu-id="1ed0f-129">Specifica il nome SKU dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1ed0f-129">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="1ed0f-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="1ed0f-130">-Tag</span></span>
<span data-ttu-id="1ed0f-131">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="1ed0f-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1ed0f-132">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="1ed0f-132">For example:</span></span>

<span data-ttu-id="1ed0f-133">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="1ed0f-133">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1ed0f-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1ed0f-134">-Confirm</span></span>
<span data-ttu-id="1ed0f-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ed0f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ed0f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ed0f-136">-WhatIf</span></span>
<span data-ttu-id="1ed0f-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1ed0f-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1ed0f-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1ed0f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ed0f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ed0f-139">CommonParameters</span></span>
<span data-ttu-id="1ed0f-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ed0f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ed0f-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ed0f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ed0f-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1ed0f-142">INPUTS</span></span>

### <span data-ttu-id="1ed0f-143">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1ed0f-143">None</span></span>
<span data-ttu-id="1ed0f-144">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="1ed0f-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1ed0f-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1ed0f-145">OUTPUTS</span></span>

### <span data-ttu-id="1ed0f-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="1ed0f-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="1ed0f-147">Note</span><span class="sxs-lookup"><span data-stu-id="1ed0f-147">NOTES</span></span>

## <span data-ttu-id="1ed0f-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1ed0f-148">RELATED LINKS</span></span>

