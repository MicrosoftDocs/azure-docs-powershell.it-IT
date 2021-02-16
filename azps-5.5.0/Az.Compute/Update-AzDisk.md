---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDisk.md
ms.openlocfilehash: 18f013643ad65bd4f7c70f3181e5950e10aa08ac
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177407"
---
# <span data-ttu-id="13f09-101">Update-AzDisk</span><span class="sxs-lookup"><span data-stu-id="13f09-101">Update-AzDisk</span></span>

## <span data-ttu-id="13f09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13f09-102">SYNOPSIS</span></span>
<span data-ttu-id="13f09-103">Aggiorna un disco.</span><span class="sxs-lookup"><span data-stu-id="13f09-103">Updates a disk.</span></span>

## <span data-ttu-id="13f09-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="13f09-104">SYNTAX</span></span>

### <span data-ttu-id="13f09-105">DefaultParameter (Default)</span><span class="sxs-lookup"><span data-stu-id="13f09-105">DefaultParameter (Default)</span></span>
```
Update-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-DiskUpdate] <PSDiskUpdate> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13f09-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="13f09-106">FriendMethod</span></span>
```
Update-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13f09-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="13f09-107">DESCRIPTION</span></span>
<span data-ttu-id="13f09-108">Il cmdlet **Update-AzDisk** aggiorna un disco.</span><span class="sxs-lookup"><span data-stu-id="13f09-108">The **Update-AzDisk** cmdlet updates a disk.</span></span>

## <span data-ttu-id="13f09-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="13f09-109">EXAMPLES</span></span>

### <span data-ttu-id="13f09-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="13f09-110">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzDiskUpdateConfig -DiskSizeGB 10 -SkuName Premium_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="13f09-111">Il primo comando crea un oggetto di aggiornamento disco vuoto locale con dimensioni di 10 GB Premium_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="13f09-111">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="13f09-112">Configura anche il tipo di sistema operativo Windows e abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="13f09-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="13f09-113">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia disco e della chiave di crittografia per l'oggetto di aggiornamento del disco.</span><span class="sxs-lookup"><span data-stu-id="13f09-113">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="13f09-114">L'ultimo comando accetta l'oggetto di aggiornamento del disco e aggiorna un disco esistente con il nome 'Disco01' nel gruppo di risorse 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="13f09-114">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="13f09-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="13f09-115">Example 2</span></span>
```
PS C:\> New-AzDiskUpdateConfig -DiskSizeGB 10 | Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="13f09-116">Questo comando aggiorna un disco esistente con il nome 'Disk01' nel gruppo di risorse 'ResourceGroup01' a 10 GB.</span><span class="sxs-lookup"><span data-stu-id="13f09-116">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="13f09-117">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="13f09-117">Example 3</span></span>
```
PS C:\> $disk = Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
PS C:\> $disk.DiskSizeGB = 10;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $disk;
```

<span data-ttu-id="13f09-118">Questi comandi aggiornano anche un disco esistente con il nome "Disco01" nel gruppo di risorse "ResourceGroup01" a 10 GB.</span><span class="sxs-lookup"><span data-stu-id="13f09-118">These commands also update an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="13f09-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13f09-119">PARAMETERS</span></span>

### <span data-ttu-id="13f09-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13f09-120">-AsJob</span></span>
<span data-ttu-id="13f09-121">Eseguire il cmdlet in background e restituire un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="13f09-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="13f09-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13f09-122">-DefaultProfile</span></span>
<span data-ttu-id="13f09-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="13f09-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13f09-124">-Disco</span><span class="sxs-lookup"><span data-stu-id="13f09-124">-Disk</span></span>
<span data-ttu-id="13f09-125">Specifica un oggetto disco locale.</span><span class="sxs-lookup"><span data-stu-id="13f09-125">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13f09-126">-DiskName</span><span class="sxs-lookup"><span data-stu-id="13f09-126">-DiskName</span></span>
<span data-ttu-id="13f09-127">Specifica il nome di un disco.</span><span class="sxs-lookup"><span data-stu-id="13f09-127">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="13f09-128">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="13f09-128">-DiskUpdate</span></span>
<span data-ttu-id="13f09-129">Specifica un oggetto di aggiornamento del disco locale.</span><span class="sxs-lookup"><span data-stu-id="13f09-129">Specifies a local disk update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13f09-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13f09-130">-ResourceGroupName</span></span>
<span data-ttu-id="13f09-131">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="13f09-131">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="13f09-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="13f09-132">-Confirm</span></span>
<span data-ttu-id="13f09-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13f09-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13f09-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13f09-134">-WhatIf</span></span>
<span data-ttu-id="13f09-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="13f09-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13f09-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="13f09-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13f09-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13f09-137">CommonParameters</span></span>
<span data-ttu-id="13f09-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13f09-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13f09-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="13f09-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13f09-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="13f09-140">INPUTS</span></span>

### <span data-ttu-id="13f09-141">System.String</span><span class="sxs-lookup"><span data-stu-id="13f09-141">System.String</span></span>

### <span data-ttu-id="13f09-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="13f09-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

### <span data-ttu-id="13f09-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="13f09-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="13f09-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="13f09-144">OUTPUTS</span></span>

### <span data-ttu-id="13f09-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="13f09-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="13f09-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="13f09-146">NOTES</span></span>

## <span data-ttu-id="13f09-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="13f09-147">RELATED LINKS</span></span>
