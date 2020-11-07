---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmDisk.md
ms.openlocfilehash: 743319688381963df54827de241d1c366bc6420e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687341"
---
# <span data-ttu-id="d0e4a-101">Update-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="d0e4a-101">Update-AzureRmDisk</span></span>

## <span data-ttu-id="d0e4a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d0e4a-102">SYNOPSIS</span></span>
<span data-ttu-id="d0e4a-103">Aggiorna un disco.</span><span class="sxs-lookup"><span data-stu-id="d0e4a-103">Updates a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0e4a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d0e4a-104">SYNTAX</span></span>

### <span data-ttu-id="d0e4a-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d0e4a-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-DiskUpdate] <PSDiskUpdate> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0e4a-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="d0e4a-106">FriendMethod</span></span>
```
Update-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0e4a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d0e4a-107">DESCRIPTION</span></span>
<span data-ttu-id="d0e4a-108">Il cmdlet **Update-AzureRmDisk** aggiorna un disco.</span><span class="sxs-lookup"><span data-stu-id="d0e4a-108">The **Update-AzureRmDisk** cmdlet updates a disk.</span></span>

## <span data-ttu-id="d0e4a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d0e4a-109">EXAMPLES</span></span>

### <span data-ttu-id="d0e4a-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d0e4a-110">Example 1</span></span>
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

<span data-ttu-id="d0e4a-111">Il primo comando crea un oggetto di aggiornamento del disco vuoto locale con dimensioni 10GB in Premium_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d0e4a-111">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="d0e4a-112">Imposta anche il tipo di sistema operativo Windows e Abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="d0e4a-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="d0e4a-113">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia del disco e della chiave di crittografia per l'oggetto aggiornamento disco.</span><span class="sxs-lookup"><span data-stu-id="d0e4a-113">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="d0e4a-114">L'ultimo comando accetta l'oggetto Update del disco e aggiorna un disco esistente con il nome "Disk01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="d0e4a-114">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="d0e4a-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="d0e4a-115">Example 2</span></span>
```
PS C:\> New-AzureRmDiskUpdateConfig -DiskSizeGB 10 | Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="d0e4a-116">Questo comando aggiorna un disco esistente con il nome "Disk01" nel gruppo di risorse "ResourceGroup01" in dimensioni del disco di 10 GB.</span><span class="sxs-lookup"><span data-stu-id="d0e4a-116">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="d0e4a-117">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="d0e4a-117">Example 3</span></span>
```
PS C:\> $disk = Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
PS C:\> $disk.DiskSizeGB = 10;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $disk;
```

<span data-ttu-id="d0e4a-118">Questi comandi aggiornano anche un disco esistente con il nome "Disk01" nel gruppo di risorse "ResourceGroup01" in dimensioni del disco di 10 GB.</span><span class="sxs-lookup"><span data-stu-id="d0e4a-118">These commands also update an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="d0e4a-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d0e4a-119">PARAMETERS</span></span>

### <span data-ttu-id="d0e4a-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0e4a-120">-AsJob</span></span>
<span data-ttu-id="d0e4a-121">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="d0e4a-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d0e4a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0e4a-122">-DefaultProfile</span></span>
<span data-ttu-id="d0e4a-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d0e4a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0e4a-124">-Disco</span><span class="sxs-lookup"><span data-stu-id="d0e4a-124">-Disk</span></span>
<span data-ttu-id="d0e4a-125">Specifica un oggetto disco locale.</span><span class="sxs-lookup"><span data-stu-id="d0e4a-125">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0e4a-126">-Diskname</span><span class="sxs-lookup"><span data-stu-id="d0e4a-126">-DiskName</span></span>
<span data-ttu-id="d0e4a-127">Specifica il nome di un disco.</span><span class="sxs-lookup"><span data-stu-id="d0e4a-127">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0e4a-128">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="d0e4a-128">-DiskUpdate</span></span>
<span data-ttu-id="d0e4a-129">Specifica un oggetto di aggiornamento del disco locale.</span><span class="sxs-lookup"><span data-stu-id="d0e4a-129">Specifies a local disk update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0e4a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0e4a-130">-ResourceGroupName</span></span>
<span data-ttu-id="d0e4a-131">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d0e4a-131">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0e4a-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d0e4a-132">-Confirm</span></span>
<span data-ttu-id="d0e4a-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0e4a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0e4a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0e4a-134">-WhatIf</span></span>
<span data-ttu-id="d0e4a-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d0e4a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0e4a-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d0e4a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0e4a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0e4a-137">CommonParameters</span></span>
<span data-ttu-id="d0e4a-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0e4a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0e4a-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0e4a-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0e4a-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d0e4a-140">INPUTS</span></span>

### <span data-ttu-id="d0e4a-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d0e4a-141">System.String</span></span>

### <span data-ttu-id="d0e4a-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="d0e4a-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>
<span data-ttu-id="d0e4a-143">Parametri: DiskUpdate (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d0e4a-143">Parameters: DiskUpdate (ByValue)</span></span>

### <span data-ttu-id="d0e4a-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="d0e4a-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>
<span data-ttu-id="d0e4a-145">Parametri: disco (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d0e4a-145">Parameters: Disk (ByValue)</span></span>

## <span data-ttu-id="d0e4a-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d0e4a-146">OUTPUTS</span></span>

### <span data-ttu-id="d0e4a-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="d0e4a-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="d0e4a-148">Note</span><span class="sxs-lookup"><span data-stu-id="d0e4a-148">NOTES</span></span>

## <span data-ttu-id="d0e4a-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d0e4a-149">RELATED LINKS</span></span>