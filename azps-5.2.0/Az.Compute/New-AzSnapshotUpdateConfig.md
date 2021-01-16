---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
ms.openlocfilehash: 1a90a1ff260d143cf4df52ad160b4c05e781bd2e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348748"
---
# <span data-ttu-id="e9ed3-101">New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="e9ed3-101">New-AzSnapshotUpdateConfig</span></span>

## <span data-ttu-id="e9ed3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e9ed3-102">SYNOPSIS</span></span>
<span data-ttu-id="e9ed3-103">Crea un oggetto di aggiornamento istantaneo configurabile.</span><span class="sxs-lookup"><span data-stu-id="e9ed3-103">Creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="e9ed3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e9ed3-104">SYNTAX</span></span>

```
New-AzSnapshotUpdateConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-DiskEncryptionSetId <String>] [-EncryptionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9ed3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e9ed3-105">DESCRIPTION</span></span>
<span data-ttu-id="e9ed3-106">Il cmdlet **New-AzSnapshotUpdateConfig** crea un oggetto di aggiornamento istantaneo configurabile.</span><span class="sxs-lookup"><span data-stu-id="e9ed3-106">The **New-AzSnapshotUpdateConfig** cmdlet creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="e9ed3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e9ed3-107">EXAMPLES</span></span>

### <span data-ttu-id="e9ed3-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e9ed3-108">Example 1</span></span>
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

<span data-ttu-id="e9ed3-109">Il primo comando crea un oggetto aggiornamento snapshot locale vuoto con dimensioni 10GB in Premium_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e9ed3-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="e9ed3-110">Imposta anche il tipo di sistema operativo Windows e Abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="e9ed3-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="e9ed3-111">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia del disco e della chiave di crittografia per l'oggetto aggiornamento snapshot.</span><span class="sxs-lookup"><span data-stu-id="e9ed3-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span> <span data-ttu-id="e9ed3-112">L'ultimo comando accetta l'oggetto Update dello snapshot e aggiorna uno snapshot esistente con il nome "Snapshot01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="e9ed3-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="e9ed3-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e9ed3-113">Example 2</span></span>
```
PS C:\> New-AzSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="e9ed3-114">Questo comando Aggiorna uno snapshot esistente con il nome "Snapshot01" nel gruppo di risorse "ResourceGroup01" in dimensioni del disco di 10 GB.</span><span class="sxs-lookup"><span data-stu-id="e9ed3-114">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="e9ed3-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e9ed3-115">PARAMETERS</span></span>

### <span data-ttu-id="e9ed3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9ed3-116">-DefaultProfile</span></span>
<span data-ttu-id="e9ed3-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e9ed3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9ed3-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="e9ed3-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="e9ed3-119">Specifica l'oggetto chiave di crittografia del disco in uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="e9ed3-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="e9ed3-120">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="e9ed3-120">-DiskEncryptionSetId</span></span>
<span data-ttu-id="e9ed3-121">Specifica l'ID risorsa del set di crittografia disco da usare per abilitare la crittografia a riposo.</span><span class="sxs-lookup"><span data-stu-id="e9ed3-121">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="e9ed3-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="e9ed3-122">-DiskSizeGB</span></span>
<span data-ttu-id="e9ed3-123">Specifica le dimensioni del disco in GB.</span><span class="sxs-lookup"><span data-stu-id="e9ed3-123">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="e9ed3-124">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="e9ed3-124">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="e9ed3-125">Abilitare le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="e9ed3-125">Enable encryption settings.</span></span>

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

### <span data-ttu-id="e9ed3-126">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="e9ed3-126">-EncryptionType</span></span>
<span data-ttu-id="e9ed3-127">Tipo di chiave utilizzata per crittografare i dati del disco.</span><span class="sxs-lookup"><span data-stu-id="e9ed3-127">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="e9ed3-128">I valori disponibili sono: "EncryptionAtRestWithPlatformKey", "EncryptionAtRestWithCustomerKey"</span><span class="sxs-lookup"><span data-stu-id="e9ed3-128">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="e9ed3-129">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="e9ed3-129">-KeyEncryptionKey</span></span>
<span data-ttu-id="e9ed3-130">Specifica la chiave di crittografia chiave in uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="e9ed3-130">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="e9ed3-131">-OsType</span><span class="sxs-lookup"><span data-stu-id="e9ed3-131">-OsType</span></span>
<span data-ttu-id="e9ed3-132">Specifica il tipo di sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e9ed3-132">Specifies the OS type.</span></span>

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

### <span data-ttu-id="e9ed3-133">-SkuName</span><span class="sxs-lookup"><span data-stu-id="e9ed3-133">-SkuName</span></span>
<span data-ttu-id="e9ed3-134">Specifica il nome SKU dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e9ed3-134">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="e9ed3-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="e9ed3-135">-Tag</span></span>
<span data-ttu-id="e9ed3-136">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="e9ed3-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e9ed3-137">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="e9ed3-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9ed3-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e9ed3-138">-Confirm</span></span>
<span data-ttu-id="e9ed3-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9ed3-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9ed3-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9ed3-140">-WhatIf</span></span>
<span data-ttu-id="e9ed3-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e9ed3-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e9ed3-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e9ed3-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9ed3-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9ed3-143">CommonParameters</span></span>
<span data-ttu-id="e9ed3-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9ed3-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9ed3-145">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e9ed3-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9ed3-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e9ed3-146">INPUTS</span></span>

### <span data-ttu-id="e9ed3-147">System. String</span><span class="sxs-lookup"><span data-stu-id="e9ed3-147">System.String</span></span>

### <span data-ttu-id="e9ed3-148">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="e9ed3-148">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="e9ed3-149">System. Int32</span><span class="sxs-lookup"><span data-stu-id="e9ed3-149">System.Int32</span></span>

### <span data-ttu-id="e9ed3-150">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e9ed3-150">System.Collections.Hashtable</span></span>

### <span data-ttu-id="e9ed3-151">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e9ed3-151">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="e9ed3-152">Microsoft. Azure. Management. Compute. Models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="e9ed3-152">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="e9ed3-153">Microsoft. Azure. Management. Compute. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="e9ed3-153">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="e9ed3-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e9ed3-154">OUTPUTS</span></span>

### <span data-ttu-id="e9ed3-155">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="e9ed3-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="e9ed3-156">Note</span><span class="sxs-lookup"><span data-stu-id="e9ed3-156">NOTES</span></span>

## <span data-ttu-id="e9ed3-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e9ed3-157">RELATED LINKS</span></span>
