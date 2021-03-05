---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDisk.md
ms.openlocfilehash: 1337482e880bca353e4824a00b73aef831db6b32
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983326"
---
# <span data-ttu-id="30fb6-101">New-AzDisk</span><span class="sxs-lookup"><span data-stu-id="30fb6-101">New-AzDisk</span></span>

## <span data-ttu-id="30fb6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30fb6-102">SYNOPSIS</span></span>
<span data-ttu-id="30fb6-103">Crea un disco gestito.</span><span class="sxs-lookup"><span data-stu-id="30fb6-103">Creates a managed disk.</span></span>

## <span data-ttu-id="30fb6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="30fb6-104">SYNTAX</span></span>

```
New-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30fb6-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="30fb6-105">DESCRIPTION</span></span>
<span data-ttu-id="30fb6-106">Il cmdlet **New-AzDisk** crea un disco gestito.</span><span class="sxs-lookup"><span data-stu-id="30fb6-106">The **New-AzDisk** cmdlet creates a managed disk.</span></span>

## <span data-ttu-id="30fb6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="30fb6-107">EXAMPLES</span></span>

### <span data-ttu-id="30fb6-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="30fb6-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -SkuName Standard_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="30fb6-109">Il primo comando crea un oggetto disco vuoto locale con dimensioni di 5 GB Standard_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="30fb6-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="30fb6-110">Configura anche il tipo di sistema operativo Windows e abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="30fb6-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="30fb6-111">Il secondo e il terzo comando impostano la chiave di crittografia disco e le relative impostazioni per l'oggetto disco.</span><span class="sxs-lookup"><span data-stu-id="30fb6-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="30fb6-112">L'ultimo comando accetta l'oggetto disco e crea un disco con il nome 'Disk01' nel gruppo di risorse 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="30fb6-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="30fb6-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="30fb6-113">Example 2</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -SkuName Standard_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $diskConfig.EncryptionSettingsCollection = New-Object Microsoft.Azure.Management.Compute.Models.EncryptionSettingsCollection

PS C:\> $encryptionSettingsElement1 = New-Object Microsoft.Azure.Management.Compute.Models.EncryptionSettingsElement
PS C:\> $encryptionSettingsElement1.DiskEncryptionKey = New-Object Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference
PS C:\> $encryptionSettingsElement1.DiskEncryptionKey.SourceVault = New-Object Microsoft.Azure.Management.Compute.Models.SourceVault
PS C:\> $encryptionSettingsElement1.DiskEncryptionKey.SourceVault.Id = $disk_encryption_key_id_1
PS C:\> $encryptionSettingsElement1.DiskEncryptionKey.SecretUrl = $disk_encryption_secret_url_1
PS C:\> $encryptionSettingsElement1.KeyEncryptionKey = New-Object Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PS C:\> $encryptionSettingsElement1.KeyEncryptionKey.SourceVault = New-Object Microsoft.Azure.Management.Compute.Models.SourceVault
PS C:\> $encryptionSettingsElement1.KeyEncryptionKey.SourceVault.Id = $key_encryption_key_id_1
PS C:\> $encryptionSettingsElement1.KeyEncryptionKey.KeyUrl = $key_encryption_key_url_1

PS C:\> $encryptionSettingsElement2 = New-Object Microsoft.Azure.Management.Compute.Models.EncryptionSettingsElement
PS C:\> $encryptionSettingsElement2.DiskEncryptionKey = New-Object Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference
PS C:\> $encryptionSettingsElement2.DiskEncryptionKey.SourceVault = New-Object Microsoft.Azure.Management.Compute.Models.SourceVault
PS C:\> $encryptionSettingsElement2.DiskEncryptionKey.SourceVault.Id = $disk_encryption_key_id_2
PS C:\> $encryptionSettingsElement2.DiskEncryptionKey.SecretUrl = $disk_encryption_secret_url_2
PS C:\> $encryptionSettingsElement2.KeyEncryptionKey = New-Object Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PS C:\> $encryptionSettingsElement2.KeyEncryptionKey.SourceVault = New-Object Microsoft.Azure.Management.Compute.Models.SourceVault
PS C:\> $encryptionSettingsElement2.KeyEncryptionKey.SourceVault.Id = $key_encryption_key_id_2
PS C:\> $encryptionSettingsElement2.KeyEncryptionKey.KeyUrl = $key_encryption_key_url_2

PS C:\> $diskConfig.EncryptionSettingsCollection.EncryptionSettings += $encryptionSettingsElement1
PS C:\> $diskConfig.EncryptionSettingsCollection.EncryptionSettings += $encryptionSettingsElement2
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="30fb6-114">Il comando precedente crea un disco con due impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="30fb6-114">The above command creates a disk with two encryption settings.</span></span>

## <span data-ttu-id="30fb6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30fb6-115">PARAMETERS</span></span>

### <span data-ttu-id="30fb6-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="30fb6-116">-AsJob</span></span>
<span data-ttu-id="30fb6-117">Eseguire il cmdlet in background e restituire un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="30fb6-117">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30fb6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30fb6-118">-DefaultProfile</span></span>
<span data-ttu-id="30fb6-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="30fb6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30fb6-120">-Disco</span><span class="sxs-lookup"><span data-stu-id="30fb6-120">-Disk</span></span>
<span data-ttu-id="30fb6-121">Specifica un oggetto disco locale.</span><span class="sxs-lookup"><span data-stu-id="30fb6-121">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30fb6-122">-DiskName</span><span class="sxs-lookup"><span data-stu-id="30fb6-122">-DiskName</span></span>
<span data-ttu-id="30fb6-123">Specifica il nome di un disco.</span><span class="sxs-lookup"><span data-stu-id="30fb6-123">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30fb6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30fb6-124">-ResourceGroupName</span></span>
<span data-ttu-id="30fb6-125">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="30fb6-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30fb6-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="30fb6-126">-Confirm</span></span>
<span data-ttu-id="30fb6-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30fb6-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30fb6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30fb6-128">-WhatIf</span></span>
<span data-ttu-id="30fb6-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="30fb6-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30fb6-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="30fb6-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30fb6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30fb6-131">CommonParameters</span></span>
<span data-ttu-id="30fb6-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30fb6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30fb6-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="30fb6-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30fb6-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="30fb6-134">INPUTS</span></span>

### <span data-ttu-id="30fb6-135">System.String</span><span class="sxs-lookup"><span data-stu-id="30fb6-135">System.String</span></span>

### <span data-ttu-id="30fb6-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="30fb6-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="30fb6-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="30fb6-137">OUTPUTS</span></span>

### <span data-ttu-id="30fb6-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="30fb6-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="30fb6-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="30fb6-139">NOTES</span></span>

## <span data-ttu-id="30fb6-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="30fb6-140">RELATED LINKS</span></span>
