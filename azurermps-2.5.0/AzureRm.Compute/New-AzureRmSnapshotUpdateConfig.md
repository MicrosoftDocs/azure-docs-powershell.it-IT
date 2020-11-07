---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermsnapshotupdateconfig
schema: 2.0.0
ms.openlocfilehash: 033b183c763be266b29aadf47a57e760e2432452
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866753"
---
# <span data-ttu-id="7300d-101">New-AzureRmSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="7300d-101">New-AzureRmSnapshotUpdateConfig</span></span>

## <span data-ttu-id="7300d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7300d-102">SYNOPSIS</span></span>
<span data-ttu-id="7300d-103">Crea un oggetto di aggiornamento istantaneo configurabile.</span><span class="sxs-lookup"><span data-stu-id="7300d-103">Creates a configurable snapshot update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7300d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7300d-104">SYNTAX</span></span>

```
New-AzureRmSnapshotUpdateConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7300d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7300d-105">DESCRIPTION</span></span>
<span data-ttu-id="7300d-106">Il cmdlet **New-AzureRmSnapshotUpdateConfig** crea un oggetto di aggiornamento istantaneo configurabile.</span><span class="sxs-lookup"><span data-stu-id="7300d-106">The **New-AzureRmSnapshotUpdateConfig** cmdlet creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="7300d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7300d-107">EXAMPLES</span></span>

### <span data-ttu-id="7300d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7300d-108">Example 1</span></span>
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

<span data-ttu-id="7300d-109">Il primo comando crea un oggetto aggiornamento snapshot locale vuoto con dimensioni 10GB in Premium_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7300d-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="7300d-110">Imposta anche il tipo di sistema operativo Windows e Abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="7300d-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="7300d-111">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia del disco e della chiave di crittografia per l'oggetto aggiornamento snapshot.</span><span class="sxs-lookup"><span data-stu-id="7300d-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span> <span data-ttu-id="7300d-112">L'ultimo comando accetta l'oggetto Update dello snapshot e aggiorna uno snapshot esistente con il nome "Snapshot01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="7300d-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="7300d-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7300d-113">Example 2</span></span>
```
PS C:\> New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="7300d-114">Questo comando Aggiorna uno snapshot esistente con il nome "Snapshot01" nel gruppo di risorse "ResourceGroup01" in dimensioni del disco di 10 GB.</span><span class="sxs-lookup"><span data-stu-id="7300d-114">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="7300d-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7300d-115">PARAMETERS</span></span>

### <span data-ttu-id="7300d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7300d-116">-DefaultProfile</span></span>
<span data-ttu-id="7300d-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7300d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7300d-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="7300d-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="7300d-119">Specifica l'oggetto chiave di crittografia del disco in uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="7300d-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="7300d-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="7300d-120">-DiskSizeGB</span></span>
<span data-ttu-id="7300d-121">Specifica le dimensioni del disco in GB.</span><span class="sxs-lookup"><span data-stu-id="7300d-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="7300d-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="7300d-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="7300d-123">Abilitare le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="7300d-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="7300d-124">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="7300d-124">-KeyEncryptionKey</span></span>
<span data-ttu-id="7300d-125">Specifica la chiave di crittografia chiave in uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="7300d-125">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="7300d-126">-OsType</span><span class="sxs-lookup"><span data-stu-id="7300d-126">-OsType</span></span>
<span data-ttu-id="7300d-127">Specifica il tipo di sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="7300d-127">Specifies the OS type.</span></span>

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

### <span data-ttu-id="7300d-128">-SkuName</span><span class="sxs-lookup"><span data-stu-id="7300d-128">-SkuName</span></span>
<span data-ttu-id="7300d-129">Specifica il nome SKU dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7300d-129">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="7300d-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="7300d-130">-Tag</span></span>
<span data-ttu-id="7300d-131">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="7300d-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7300d-132">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="7300d-132">For example:</span></span>

<span data-ttu-id="7300d-133">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="7300d-133">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="7300d-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7300d-134">-Confirm</span></span>
<span data-ttu-id="7300d-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7300d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7300d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7300d-136">-WhatIf</span></span>
<span data-ttu-id="7300d-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7300d-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7300d-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7300d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7300d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7300d-139">CommonParameters</span></span>
<span data-ttu-id="7300d-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7300d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7300d-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7300d-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7300d-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7300d-142">INPUTS</span></span>

### <span data-ttu-id="7300d-143">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7300d-143">None</span></span>
<span data-ttu-id="7300d-144">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="7300d-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7300d-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7300d-145">OUTPUTS</span></span>

### <span data-ttu-id="7300d-146">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="7300d-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="7300d-147">Note</span><span class="sxs-lookup"><span data-stu-id="7300d-147">NOTES</span></span>

## <span data-ttu-id="7300d-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7300d-148">RELATED LINKS</span></span>

