---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
ms.openlocfilehash: 1a90a1ff260d143cf4df52ad160b4c05e781bd2e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210027"
---
# <span data-ttu-id="0917d-101">New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="0917d-101">New-AzSnapshotUpdateConfig</span></span>

## <span data-ttu-id="0917d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0917d-102">SYNOPSIS</span></span>
<span data-ttu-id="0917d-103">Crea un oggetto di aggiornamento snapshot configurabile.</span><span class="sxs-lookup"><span data-stu-id="0917d-103">Creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="0917d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0917d-104">SYNTAX</span></span>

```
New-AzSnapshotUpdateConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-DiskEncryptionSetId <String>] [-EncryptionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0917d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0917d-105">DESCRIPTION</span></span>
<span data-ttu-id="0917d-106">Il cmdlet **New-AzSnapshotUpdateConfig crea** un oggetto di aggiornamento snapshot configurabile.</span><span class="sxs-lookup"><span data-stu-id="0917d-106">The **New-AzSnapshotUpdateConfig** cmdlet creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="0917d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0917d-107">EXAMPLES</span></span>

### <span data-ttu-id="0917d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0917d-108">Example 1</span></span>
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

<span data-ttu-id="0917d-109">Il primo comando crea un oggetto di aggiornamento snapshot vuoto locale con dimensioni di 10 GB Premium_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="0917d-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="0917d-110">Configura anche il tipo di sistema operativo Windows e abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="0917d-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="0917d-111">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia disco e della chiave di crittografia per l'oggetto di aggiornamento snapshot.</span><span class="sxs-lookup"><span data-stu-id="0917d-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span> <span data-ttu-id="0917d-112">L'ultimo comando accetta l'oggetto di aggiornamento snapshot e aggiorna uno snapshot esistente con il nome 'Snapshot01' nel gruppo di risorse 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="0917d-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="0917d-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="0917d-113">Example 2</span></span>
```
PS C:\> New-AzSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="0917d-114">Questo comando aggiorna uno snapshot esistente con il nome 'Snapshot01' nel gruppo di risorse 'ResourceGroup01' a 10 GB.</span><span class="sxs-lookup"><span data-stu-id="0917d-114">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="0917d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0917d-115">PARAMETERS</span></span>

### <span data-ttu-id="0917d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0917d-116">-DefaultProfile</span></span>
<span data-ttu-id="0917d-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0917d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0917d-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="0917d-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="0917d-119">Specifica l'oggetto chiave di crittografia del disco in uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="0917d-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="0917d-120">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="0917d-120">-DiskEncryptionSetId</span></span>
<span data-ttu-id="0917d-121">Specifica l'ID risorsa del set di crittografia del disco da usare per l'abilitazione della crittografia in fase di disattivazione.</span><span class="sxs-lookup"><span data-stu-id="0917d-121">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="0917d-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="0917d-122">-DiskSizeGB</span></span>
<span data-ttu-id="0917d-123">Specifica le dimensioni del disco in GB.</span><span class="sxs-lookup"><span data-stu-id="0917d-123">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="0917d-124">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="0917d-124">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="0917d-125">Abilitare le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="0917d-125">Enable encryption settings.</span></span>

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

### <span data-ttu-id="0917d-126">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="0917d-126">-EncryptionType</span></span>
<span data-ttu-id="0917d-127">Tipo di chiave usata per crittografare i dati del disco.</span><span class="sxs-lookup"><span data-stu-id="0917d-127">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="0917d-128">I valori disponibili sono: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span><span class="sxs-lookup"><span data-stu-id="0917d-128">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="0917d-129">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="0917d-129">-KeyEncryptionKey</span></span>
<span data-ttu-id="0917d-130">Specifica la chiave di crittografia chiave in uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="0917d-130">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="0917d-131">-OsType</span><span class="sxs-lookup"><span data-stu-id="0917d-131">-OsType</span></span>
<span data-ttu-id="0917d-132">Specifica il tipo di sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0917d-132">Specifies the OS type.</span></span>

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

### <span data-ttu-id="0917d-133">-SKUName</span><span class="sxs-lookup"><span data-stu-id="0917d-133">-SkuName</span></span>
<span data-ttu-id="0917d-134">Specifica il nome SKU dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="0917d-134">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="0917d-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="0917d-135">-Tag</span></span>
<span data-ttu-id="0917d-136">Coppie chiave-valore sotto forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="0917d-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0917d-137">Ad esempio: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="0917d-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="0917d-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0917d-138">-Confirm</span></span>
<span data-ttu-id="0917d-139">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0917d-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0917d-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0917d-140">-WhatIf</span></span>
<span data-ttu-id="0917d-141">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0917d-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0917d-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0917d-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0917d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0917d-143">CommonParameters</span></span>
<span data-ttu-id="0917d-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0917d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0917d-145">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0917d-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0917d-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="0917d-146">INPUTS</span></span>

### <span data-ttu-id="0917d-147">System.String</span><span class="sxs-lookup"><span data-stu-id="0917d-147">System.String</span></span>

### <span data-ttu-id="0917d-148">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="0917d-148">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="0917d-149">System.Int32</span><span class="sxs-lookup"><span data-stu-id="0917d-149">System.Int32</span></span>

### <span data-ttu-id="0917d-150">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="0917d-150">System.Collections.Hashtable</span></span>

### <span data-ttu-id="0917d-151">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0917d-151">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="0917d-152">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="0917d-152">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="0917d-153">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="0917d-153">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="0917d-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0917d-154">OUTPUTS</span></span>

### <span data-ttu-id="0917d-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="0917d-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="0917d-156">NOTE</span><span class="sxs-lookup"><span data-stu-id="0917d-156">NOTES</span></span>

## <span data-ttu-id="0917d-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0917d-157">RELATED LINKS</span></span>
