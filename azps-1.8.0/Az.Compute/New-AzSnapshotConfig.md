---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
ms.openlocfilehash: 293e894704509fe1b869ca23bd726c49f400de48
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684771"
---
# <span data-ttu-id="63284-101">New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="63284-101">New-AzSnapshotConfig</span></span>

## <span data-ttu-id="63284-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="63284-102">SYNOPSIS</span></span>
<span data-ttu-id="63284-103">Crea un oggetto snapshot configurabile.</span><span class="sxs-lookup"><span data-stu-id="63284-103">Creates a configurable snapshot object.</span></span>

## <span data-ttu-id="63284-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="63284-104">SYNTAX</span></span>

```
New-AzSnapshotConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-HyperVGeneration <String>] [-Tag <Hashtable>] [-CreateOption <String>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63284-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="63284-105">DESCRIPTION</span></span>
<span data-ttu-id="63284-106">Il cmdlet **New-AzSnapshotConfig** crea un oggetto snapshot configurabile.</span><span class="sxs-lookup"><span data-stu-id="63284-106">The **New-AzSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="63284-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="63284-107">EXAMPLES</span></span>

### <span data-ttu-id="63284-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="63284-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="63284-109">Il primo comando crea un oggetto snapshot locale vuoto con la dimensione 5GB in Standard_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="63284-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="63284-110">Imposta anche il tipo di sistema operativo Windows e Abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="63284-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="63284-111">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia del disco e della chiave di crittografia per l'oggetto snapshot.</span><span class="sxs-lookup"><span data-stu-id="63284-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="63284-112">L'ultimo comando accetta l'oggetto snapshot e crea uno snapshot con il nome "Snapshot01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="63284-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="63284-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="63284-113">PARAMETERS</span></span>

### <span data-ttu-id="63284-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="63284-114">-CreateOption</span></span>
<span data-ttu-id="63284-115">Specifica se questo cmdlet crea un disco nella macchina virtuale da una piattaforma o da un'immagine utente, crea un disco vuoto o allega un disco esistente.</span><span class="sxs-lookup"><span data-stu-id="63284-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="63284-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63284-116">-DefaultProfile</span></span>
<span data-ttu-id="63284-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="63284-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63284-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="63284-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="63284-119">Specifica l'oggetto chiave di crittografia del disco in uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="63284-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="63284-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="63284-120">-DiskSizeGB</span></span>
<span data-ttu-id="63284-121">Specifica le dimensioni del disco in GB.</span><span class="sxs-lookup"><span data-stu-id="63284-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="63284-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="63284-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="63284-123">Abilitare le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="63284-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="63284-124">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="63284-124">-HyperVGeneration</span></span>
<span data-ttu-id="63284-125">Generazione di hypervisor della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="63284-125">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="63284-126">Applicabile solo ai dischi del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="63284-126">Applicable to OS disks only.</span></span>  <span data-ttu-id="63284-127">I valori consentiti sono V1 e V2.</span><span class="sxs-lookup"><span data-stu-id="63284-127">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="63284-128">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="63284-128">-ImageReference</span></span>
<span data-ttu-id="63284-129">Specifica il riferimento alle immagini in uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="63284-129">Specifies the image reference on a snapshot.</span></span>

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

### <span data-ttu-id="63284-130">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="63284-130">-KeyEncryptionKey</span></span>
<span data-ttu-id="63284-131">Specifica la chiave di crittografia chiave in uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="63284-131">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="63284-132">-Posizione</span><span class="sxs-lookup"><span data-stu-id="63284-132">-Location</span></span>
<span data-ttu-id="63284-133">Specifica una posizione.</span><span class="sxs-lookup"><span data-stu-id="63284-133">Specifies a location.</span></span>

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

### <span data-ttu-id="63284-134">-OsType</span><span class="sxs-lookup"><span data-stu-id="63284-134">-OsType</span></span>
<span data-ttu-id="63284-135">Specifica il tipo di sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="63284-135">Specifies the OS type.</span></span>

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

### <span data-ttu-id="63284-136">-SkuName</span><span class="sxs-lookup"><span data-stu-id="63284-136">-SkuName</span></span>
<span data-ttu-id="63284-137">Specifica il nome SKU dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="63284-137">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="63284-138">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="63284-138">-SourceResourceId</span></span>
<span data-ttu-id="63284-139">Specifica l'ID risorsa di origine.</span><span class="sxs-lookup"><span data-stu-id="63284-139">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="63284-140">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="63284-140">-SourceUri</span></span>
<span data-ttu-id="63284-141">Specifica l'URI di origine.</span><span class="sxs-lookup"><span data-stu-id="63284-141">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="63284-142">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="63284-142">-StorageAccountId</span></span>
<span data-ttu-id="63284-143">Specifica l'ID account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="63284-143">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="63284-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="63284-144">-Tag</span></span>
<span data-ttu-id="63284-145">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="63284-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="63284-146">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="63284-146">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="63284-147">-Confermare</span><span class="sxs-lookup"><span data-stu-id="63284-147">-Confirm</span></span>
<span data-ttu-id="63284-148">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63284-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63284-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63284-149">-WhatIf</span></span>
<span data-ttu-id="63284-150">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="63284-150">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="63284-151">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="63284-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63284-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63284-152">CommonParameters</span></span>
<span data-ttu-id="63284-153">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63284-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63284-154">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63284-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63284-155">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="63284-155">INPUTS</span></span>

### <span data-ttu-id="63284-156">System. String</span><span class="sxs-lookup"><span data-stu-id="63284-156">System.String</span></span>

### <span data-ttu-id="63284-157">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="63284-157">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="63284-158">System. Int32</span><span class="sxs-lookup"><span data-stu-id="63284-158">System.Int32</span></span>

### <span data-ttu-id="63284-159">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="63284-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="63284-160">Microsoft. Azure. Management. Compute. Models. ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="63284-160">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="63284-161">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="63284-161">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="63284-162">Microsoft. Azure. Management. Compute. Models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="63284-162">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="63284-163">Microsoft. Azure. Management. Compute. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="63284-163">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="63284-164">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="63284-164">OUTPUTS</span></span>

### <span data-ttu-id="63284-165">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="63284-165">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="63284-166">Note</span><span class="sxs-lookup"><span data-stu-id="63284-166">NOTES</span></span>

## <span data-ttu-id="63284-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="63284-167">RELATED LINKS</span></span>
