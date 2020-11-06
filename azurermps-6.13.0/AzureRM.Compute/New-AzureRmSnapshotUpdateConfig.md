---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermsnapshotupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmSnapshotUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmSnapshotUpdateConfig.md
ms.openlocfilehash: 31c3ca819619f791f706fe93ce4977508fb28d27
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518843"
---
# <span data-ttu-id="01dc3-101">New-AzureRmSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="01dc3-101">New-AzureRmSnapshotUpdateConfig</span></span>

## <span data-ttu-id="01dc3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="01dc3-102">SYNOPSIS</span></span>
<span data-ttu-id="01dc3-103">Crea un oggetto di aggiornamento istantaneo configurabile.</span><span class="sxs-lookup"><span data-stu-id="01dc3-103">Creates a configurable snapshot update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01dc3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="01dc3-104">SYNTAX</span></span>

```
New-AzureRmSnapshotUpdateConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01dc3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="01dc3-105">DESCRIPTION</span></span>
<span data-ttu-id="01dc3-106">Il cmdlet **New-AzureRmSnapshotUpdateConfig** crea un oggetto di aggiornamento istantaneo configurabile.</span><span class="sxs-lookup"><span data-stu-id="01dc3-106">The **New-AzureRmSnapshotUpdateConfig** cmdlet creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="01dc3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="01dc3-107">EXAMPLES</span></span>

### <span data-ttu-id="01dc3-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="01dc3-108">Example 1</span></span>
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

<span data-ttu-id="01dc3-109">Il primo comando crea un oggetto aggiornamento snapshot locale vuoto con dimensioni 10GB in Premium_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="01dc3-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="01dc3-110">Imposta anche il tipo di sistema operativo Windows e Abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="01dc3-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="01dc3-111">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia del disco e della chiave di crittografia per l'oggetto aggiornamento snapshot.</span><span class="sxs-lookup"><span data-stu-id="01dc3-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span> <span data-ttu-id="01dc3-112">L'ultimo comando accetta l'oggetto Update dello snapshot e aggiorna uno snapshot esistente con il nome "Snapshot01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="01dc3-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="01dc3-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="01dc3-113">Example 2</span></span>
```
PS C:\> New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="01dc3-114">Questo comando Aggiorna uno snapshot esistente con il nome "Snapshot01" nel gruppo di risorse "ResourceGroup01" in dimensioni del disco di 10 GB.</span><span class="sxs-lookup"><span data-stu-id="01dc3-114">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="01dc3-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="01dc3-115">PARAMETERS</span></span>

### <span data-ttu-id="01dc3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01dc3-116">-DefaultProfile</span></span>
<span data-ttu-id="01dc3-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="01dc3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01dc3-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="01dc3-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="01dc3-119">Specifica l'oggetto chiave di crittografia del disco in uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="01dc3-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="01dc3-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="01dc3-120">-DiskSizeGB</span></span>
<span data-ttu-id="01dc3-121">Specifica le dimensioni del disco in GB.</span><span class="sxs-lookup"><span data-stu-id="01dc3-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="01dc3-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="01dc3-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="01dc3-123">Abilitare le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="01dc3-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="01dc3-124">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="01dc3-124">-KeyEncryptionKey</span></span>
<span data-ttu-id="01dc3-125">Specifica la chiave di crittografia chiave in uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="01dc3-125">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="01dc3-126">-OsType</span><span class="sxs-lookup"><span data-stu-id="01dc3-126">-OsType</span></span>
<span data-ttu-id="01dc3-127">Specifica il tipo di sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="01dc3-127">Specifies the OS type.</span></span>

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

### <span data-ttu-id="01dc3-128">-SkuName</span><span class="sxs-lookup"><span data-stu-id="01dc3-128">-SkuName</span></span>
<span data-ttu-id="01dc3-129">Specifica il nome SKU dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="01dc3-129">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="01dc3-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="01dc3-130">-Tag</span></span>
<span data-ttu-id="01dc3-131">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="01dc3-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="01dc3-132">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="01dc3-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="01dc3-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="01dc3-133">-Confirm</span></span>
<span data-ttu-id="01dc3-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01dc3-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01dc3-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01dc3-135">-WhatIf</span></span>
<span data-ttu-id="01dc3-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="01dc3-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="01dc3-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="01dc3-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01dc3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01dc3-138">CommonParameters</span></span>
<span data-ttu-id="01dc3-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01dc3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01dc3-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01dc3-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01dc3-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="01dc3-141">INPUTS</span></span>

### <span data-ttu-id="01dc3-142">System. String</span><span class="sxs-lookup"><span data-stu-id="01dc3-142">System.String</span></span>

### <span data-ttu-id="01dc3-143">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes, Microsoft. Azure. Management. Compute, Version = 21.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="01dc3-143">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="01dc3-144">System. Int32</span><span class="sxs-lookup"><span data-stu-id="01dc3-144">System.Int32</span></span>

### <span data-ttu-id="01dc3-145">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="01dc3-145">System.Collections.Hashtable</span></span>

### <span data-ttu-id="01dc3-146">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="01dc3-146">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="01dc3-147">Microsoft. Azure. Management. Compute. Models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="01dc3-147">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="01dc3-148">Microsoft. Azure. Management. Compute. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="01dc3-148">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="01dc3-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="01dc3-149">OUTPUTS</span></span>

### <span data-ttu-id="01dc3-150">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="01dc3-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="01dc3-151">Note</span><span class="sxs-lookup"><span data-stu-id="01dc3-151">NOTES</span></span>

## <span data-ttu-id="01dc3-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="01dc3-152">RELATED LINKS</span></span>
