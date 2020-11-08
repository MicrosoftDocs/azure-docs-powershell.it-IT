---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
ms.openlocfilehash: 5d9a48fbdc323ffdd232d6d961da6564fecc0dff
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033490"
---
# <span data-ttu-id="92b28-101">New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="92b28-101">New-AzSnapshotConfig</span></span>

## <span data-ttu-id="92b28-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="92b28-102">SYNOPSIS</span></span>
<span data-ttu-id="92b28-103">Crea un oggetto snapshot configurabile.</span><span class="sxs-lookup"><span data-stu-id="92b28-103">Creates a configurable snapshot object.</span></span>

## <span data-ttu-id="92b28-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="92b28-104">SYNTAX</span></span>

```
New-AzSnapshotConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-HyperVGeneration <String>] [-Incremental] [-Tag <Hashtable>] [-CreateOption <String>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [DiskAccessId <String>]
 [-NetworkAccessPolicy <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92b28-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="92b28-105">DESCRIPTION</span></span>
<span data-ttu-id="92b28-106">Il cmdlet **New-AzSnapshotConfig** crea un oggetto snapshot configurabile.</span><span class="sxs-lookup"><span data-stu-id="92b28-106">The **New-AzSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="92b28-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="92b28-107">EXAMPLES</span></span>

### <span data-ttu-id="92b28-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="92b28-108">Example 1</span></span>
```powershell
PS C:\> $snapshotconfig = New-AzSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="92b28-109">Il primo comando crea un oggetto snapshot locale vuoto con la dimensione 5GB in Standard_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="92b28-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="92b28-110">Imposta anche il tipo di sistema operativo Windows e Abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="92b28-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="92b28-111">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia del disco e della chiave di crittografia per l'oggetto snapshot.</span><span class="sxs-lookup"><span data-stu-id="92b28-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="92b28-112">L'ultimo comando accetta l'oggetto snapshot e crea uno snapshot con il nome "Snapshot01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="92b28-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="92b28-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="92b28-113">Example 2</span></span>

<span data-ttu-id="92b28-114">Crea un oggetto snapshot configurabile.</span><span class="sxs-lookup"><span data-stu-id="92b28-114">Creates a configurable snapshot object.</span></span> <span data-ttu-id="92b28-115">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="92b28-115">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzSnapshotConfig -CreateOption Empty -Location 'Central US' -SourceUri 'https://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd'
```

## <span data-ttu-id="92b28-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="92b28-116">PARAMETERS</span></span>

### <span data-ttu-id="92b28-117">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="92b28-117">-CreateOption</span></span>
<span data-ttu-id="92b28-118">Specifica se questo cmdlet crea un disco nella macchina virtuale da una piattaforma o da un'immagine utente, crea un disco vuoto o allega un disco esistente.</span><span class="sxs-lookup"><span data-stu-id="92b28-118">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="92b28-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92b28-119">-DefaultProfile</span></span>
<span data-ttu-id="92b28-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="92b28-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92b28-121">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="92b28-121">-DiskEncryptionKey</span></span>
<span data-ttu-id="92b28-122">Specifica l'oggetto chiave di crittografia del disco in uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="92b28-122">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="92b28-123">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="92b28-123">-DiskEncryptionSetId</span></span>
<span data-ttu-id="92b28-124">Specifica l'ID risorsa del set di crittografia disco da usare per abilitare la crittografia a riposo.</span><span class="sxs-lookup"><span data-stu-id="92b28-124">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="92b28-125">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="92b28-125">-DiskSizeGB</span></span>
<span data-ttu-id="92b28-126">Specifica le dimensioni del disco in GB.</span><span class="sxs-lookup"><span data-stu-id="92b28-126">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="92b28-127">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="92b28-127">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="92b28-128">Abilitare le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="92b28-128">Enable encryption settings.</span></span>

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

### <span data-ttu-id="92b28-129">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="92b28-129">-EncryptionType</span></span>
<span data-ttu-id="92b28-130">Tipo di chiave utilizzata per crittografare i dati del disco.</span><span class="sxs-lookup"><span data-stu-id="92b28-130">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="92b28-131">I valori disponibili sono: "EncryptionAtRestWithPlatformKey", "EncryptionAtRestWithCustomerKey"</span><span class="sxs-lookup"><span data-stu-id="92b28-131">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="92b28-132">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="92b28-132">-DiskAccessId</span></span>
<span data-ttu-id="92b28-133">Ottiene o imposta l'ID ARM della risorsa DiskAccess per l'uso di endpoint privati.</span><span class="sxs-lookup"><span data-stu-id="92b28-133">Gets or sets ARM id of the DiskAccess resource for using private endpoints on.</span></span>

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

### <span data-ttu-id="92b28-134">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="92b28-134">-NetworkAccessPolicy</span></span>
<span data-ttu-id="92b28-135">I criteri di accesso alla rete definiscono i criteri di accesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="92b28-135">Network access policy defines the network access policy.</span></span>
<span data-ttu-id="92b28-136">I valori possibili includono: "AllowAll", "AllowPrivate", "valore denyall"</span><span class="sxs-lookup"><span data-stu-id="92b28-136">Possible values include: 'AllowAll', 'AllowPrivate', 'DenyAll'</span></span>

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

### <span data-ttu-id="92b28-137">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="92b28-137">-HyperVGeneration</span></span>
<span data-ttu-id="92b28-138">Generazione di hypervisor della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="92b28-138">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="92b28-139">Applicabile solo ai dischi del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="92b28-139">Applicable to OS disks only.</span></span>  <span data-ttu-id="92b28-140">I valori consentiti sono V1 e V2.</span><span class="sxs-lookup"><span data-stu-id="92b28-140">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="92b28-141">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="92b28-141">-ImageReference</span></span>
<span data-ttu-id="92b28-142">Specifica il riferimento alle immagini in uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="92b28-142">Specifies the image reference on a snapshot.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageDiskReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92b28-143">-Incrementale</span><span class="sxs-lookup"><span data-stu-id="92b28-143">-Incremental</span></span>
<span data-ttu-id="92b28-144">Specifica uno snapshot incrementale.</span><span class="sxs-lookup"><span data-stu-id="92b28-144">Specifies an incremental snapshot.</span></span> <span data-ttu-id="92b28-145">Gli snapshot incrementali nello stesso disco occupano meno spazio degli snapshot completi e possono essere diff.</span><span class="sxs-lookup"><span data-stu-id="92b28-145">Incremental snapshots on the same disk occupy less space than full snapshots and can be diffed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92b28-146">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="92b28-146">-KeyEncryptionKey</span></span>
<span data-ttu-id="92b28-147">Specifica la chiave di crittografia chiave in uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="92b28-147">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="92b28-148">-Posizione</span><span class="sxs-lookup"><span data-stu-id="92b28-148">-Location</span></span>
<span data-ttu-id="92b28-149">Specifica una posizione.</span><span class="sxs-lookup"><span data-stu-id="92b28-149">Specifies a location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92b28-150">-OsType</span><span class="sxs-lookup"><span data-stu-id="92b28-150">-OsType</span></span>
<span data-ttu-id="92b28-151">Specifica il tipo di sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="92b28-151">Specifies the OS type.</span></span>

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

### <span data-ttu-id="92b28-152">-SkuName</span><span class="sxs-lookup"><span data-stu-id="92b28-152">-SkuName</span></span>
<span data-ttu-id="92b28-153">Specifica il nome SKU dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="92b28-153">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="92b28-154">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="92b28-154">-SourceResourceId</span></span>
<span data-ttu-id="92b28-155">Specifica l'ID risorsa di origine.</span><span class="sxs-lookup"><span data-stu-id="92b28-155">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="92b28-156">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="92b28-156">-SourceUri</span></span>
<span data-ttu-id="92b28-157">Specifica l'URI di origine.</span><span class="sxs-lookup"><span data-stu-id="92b28-157">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="92b28-158">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="92b28-158">-StorageAccountId</span></span>
<span data-ttu-id="92b28-159">Specifica l'ID account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="92b28-159">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="92b28-160">-Tag</span><span class="sxs-lookup"><span data-stu-id="92b28-160">-Tag</span></span>
<span data-ttu-id="92b28-161">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="92b28-161">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="92b28-162">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="92b28-162">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92b28-163">-Confermare</span><span class="sxs-lookup"><span data-stu-id="92b28-163">-Confirm</span></span>
<span data-ttu-id="92b28-164">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92b28-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92b28-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92b28-165">-WhatIf</span></span>
<span data-ttu-id="92b28-166">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="92b28-166">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="92b28-167">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="92b28-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92b28-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92b28-168">CommonParameters</span></span>
<span data-ttu-id="92b28-169">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92b28-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92b28-170">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92b28-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92b28-171">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="92b28-171">INPUTS</span></span>

### <span data-ttu-id="92b28-172">System. String</span><span class="sxs-lookup"><span data-stu-id="92b28-172">System.String</span></span>

### <span data-ttu-id="92b28-173">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="92b28-173">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="92b28-174">System. Int32</span><span class="sxs-lookup"><span data-stu-id="92b28-174">System.Int32</span></span>

### <span data-ttu-id="92b28-175">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="92b28-175">System.Collections.Hashtable</span></span>

### <span data-ttu-id="92b28-176">Microsoft. Azure. Management. Compute. Models. ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="92b28-176">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="92b28-177">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="92b28-177">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="92b28-178">Microsoft. Azure. Management. Compute. Models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="92b28-178">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="92b28-179">Microsoft. Azure. Management. Compute. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="92b28-179">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="92b28-180">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="92b28-180">OUTPUTS</span></span>

### <span data-ttu-id="92b28-181">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="92b28-181">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="92b28-182">Note</span><span class="sxs-lookup"><span data-stu-id="92b28-182">NOTES</span></span>

## <span data-ttu-id="92b28-183">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="92b28-183">RELATED LINKS</span></span>
