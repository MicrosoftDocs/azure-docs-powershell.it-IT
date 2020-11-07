---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
ms.openlocfilehash: c2c17fe3329170d65d61e5439e614717a8119f26
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863634"
---
# <span data-ttu-id="ea7c2-101">New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="ea7c2-101">New-AzSnapshotUpdateConfig</span></span>

## <span data-ttu-id="ea7c2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ea7c2-102">SYNOPSIS</span></span>
<span data-ttu-id="ea7c2-103">Crea un oggetto di aggiornamento istantaneo configurabile.</span><span class="sxs-lookup"><span data-stu-id="ea7c2-103">Creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="ea7c2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ea7c2-104">SYNTAX</span></span>

```
New-AzSnapshotUpdateConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea7c2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ea7c2-105">DESCRIPTION</span></span>
<span data-ttu-id="ea7c2-106">Il cmdlet **New-AzSnapshotUpdateConfig** crea un oggetto di aggiornamento istantaneo configurabile.</span><span class="sxs-lookup"><span data-stu-id="ea7c2-106">The **New-AzSnapshotUpdateConfig** cmdlet creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="ea7c2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ea7c2-107">EXAMPLES</span></span>

### <span data-ttu-id="ea7c2-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ea7c2-108">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzSnapshotUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateDiskEncryptionKey -SnapshotUpdate $snapshotupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateKeyEncryptionKey -SnapshotUpdate $snapshotupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="ea7c2-109">Il primo comando crea un oggetto aggiornamento snapshot locale vuoto con dimensioni 10GB in Premium_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ea7c2-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="ea7c2-110">Imposta anche il tipo di sistema operativo Windows e Abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="ea7c2-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="ea7c2-111">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia del disco e della chiave di crittografia per l'oggetto aggiornamento snapshot.</span><span class="sxs-lookup"><span data-stu-id="ea7c2-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span> <span data-ttu-id="ea7c2-112">L'ultimo comando accetta l'oggetto Update dello snapshot e aggiorna uno snapshot esistente con il nome "Snapshot01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="ea7c2-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="ea7c2-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ea7c2-113">Example 2</span></span>
```
PS C:\> New-AzSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="ea7c2-114">Questo comando Aggiorna uno snapshot esistente con il nome "Snapshot01" nel gruppo di risorse "ResourceGroup01" in dimensioni del disco di 10 GB.</span><span class="sxs-lookup"><span data-stu-id="ea7c2-114">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="ea7c2-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ea7c2-115">PARAMETERS</span></span>

### <span data-ttu-id="ea7c2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea7c2-116">-DefaultProfile</span></span>
<span data-ttu-id="ea7c2-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ea7c2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea7c2-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="ea7c2-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="ea7c2-119">Specifica l'oggetto chiave di crittografia del disco in uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="ea7c2-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="ea7c2-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="ea7c2-120">-DiskSizeGB</span></span>
<span data-ttu-id="ea7c2-121">Specifica le dimensioni del disco in GB.</span><span class="sxs-lookup"><span data-stu-id="ea7c2-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="ea7c2-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="ea7c2-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="ea7c2-123">Abilitare le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="ea7c2-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="ea7c2-124">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="ea7c2-124">-KeyEncryptionKey</span></span>
<span data-ttu-id="ea7c2-125">Specifica la chiave di crittografia chiave in uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="ea7c2-125">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="ea7c2-126">-OsType</span><span class="sxs-lookup"><span data-stu-id="ea7c2-126">-OsType</span></span>
<span data-ttu-id="ea7c2-127">Specifica il tipo di sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ea7c2-127">Specifies the OS type.</span></span>

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

### <span data-ttu-id="ea7c2-128">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ea7c2-128">-SkuName</span></span>
<span data-ttu-id="ea7c2-129">Specifica il nome SKU dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ea7c2-129">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="ea7c2-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="ea7c2-130">-Tag</span></span>
<span data-ttu-id="ea7c2-131">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="ea7c2-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ea7c2-132">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="ea7c2-132">For example:</span></span>

<span data-ttu-id="ea7c2-133">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="ea7c2-133">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ea7c2-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ea7c2-134">-Confirm</span></span>
<span data-ttu-id="ea7c2-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea7c2-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea7c2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea7c2-136">-WhatIf</span></span>
<span data-ttu-id="ea7c2-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ea7c2-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea7c2-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ea7c2-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea7c2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea7c2-139">CommonParameters</span></span>
<span data-ttu-id="ea7c2-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea7c2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea7c2-141">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea7c2-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea7c2-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ea7c2-142">INPUTS</span></span>

### <span data-ttu-id="ea7c2-143">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ea7c2-143">None</span></span>
<span data-ttu-id="ea7c2-144">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="ea7c2-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ea7c2-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ea7c2-145">OUTPUTS</span></span>

### <span data-ttu-id="ea7c2-146">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="ea7c2-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="ea7c2-147">Note</span><span class="sxs-lookup"><span data-stu-id="ea7c2-147">NOTES</span></span>

## <span data-ttu-id="ea7c2-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ea7c2-148">RELATED LINKS</span></span>

