---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmDisk.md
ms.openlocfilehash: 30a6ac1a3d74423302cc8b39e8b494e2f1ee2e22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685490"
---
# <span data-ttu-id="19a69-101">Update-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="19a69-101">Update-AzureRmDisk</span></span>

## <span data-ttu-id="19a69-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="19a69-102">SYNOPSIS</span></span>
<span data-ttu-id="19a69-103">Aggiorna un disco.</span><span class="sxs-lookup"><span data-stu-id="19a69-103">Updates a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19a69-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="19a69-104">SYNTAX</span></span>

### <span data-ttu-id="19a69-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="19a69-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-DiskUpdate] <DiskUpdate> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19a69-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="19a69-106">FriendMethod</span></span>
```
Update-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <Disk> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="19a69-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="19a69-107">DESCRIPTION</span></span>
<span data-ttu-id="19a69-108">Il cmdlet **Update-AzureRmDisk** aggiorna un disco.</span><span class="sxs-lookup"><span data-stu-id="19a69-108">The **Update-AzureRmDisk** cmdlet updates a disk.</span></span>

## <span data-ttu-id="19a69-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="19a69-109">EXAMPLES</span></span>

### <span data-ttu-id="19a69-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="19a69-110">Example 1</span></span>
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

<span data-ttu-id="19a69-111">Il primo comando crea un oggetto di aggiornamento del disco vuoto locale con dimensioni 10GB in Premium_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="19a69-111">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="19a69-112">Imposta anche il tipo di sistema operativo Windows e Abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="19a69-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="19a69-113">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia del disco e della chiave di crittografia per l'oggetto aggiornamento disco.</span><span class="sxs-lookup"><span data-stu-id="19a69-113">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="19a69-114">L'ultimo comando accetta l'oggetto Update del disco e aggiorna un disco esistente con il nome "Disk01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="19a69-114">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="19a69-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="19a69-115">Example 2</span></span>
```
PS C:\> New-AzureRmDiskUpdateConfig -DiskSizeGB 10 | Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="19a69-116">Questo comando aggiorna un disco esistente con il nome "Disk01" nel gruppo di risorse "ResourceGroup01" in dimensioni del disco di 10 GB.</span><span class="sxs-lookup"><span data-stu-id="19a69-116">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="19a69-117">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="19a69-117">Example 3</span></span>
```
PS C:\> $disk = Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
PS C:\> $disk.DiskSizeGB = 10;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $disk;
```

<span data-ttu-id="19a69-118">Questi comandi aggiornano anche un disco esistente con il nome "Disk01" nel gruppo di risorse "ResourceGroup01" in dimensioni del disco di 10 GB.</span><span class="sxs-lookup"><span data-stu-id="19a69-118">These commands also update an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="19a69-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="19a69-119">PARAMETERS</span></span>

### <span data-ttu-id="19a69-120">-Disco</span><span class="sxs-lookup"><span data-stu-id="19a69-120">-Disk</span></span>
<span data-ttu-id="19a69-121">Specifica un oggetto disco locale.</span><span class="sxs-lookup"><span data-stu-id="19a69-121">Specifies a local disk object.</span></span>

```yaml
Type: Disk
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19a69-122">-Diskname</span><span class="sxs-lookup"><span data-stu-id="19a69-122">-DiskName</span></span>
<span data-ttu-id="19a69-123">Specifica il nome di un disco.</span><span class="sxs-lookup"><span data-stu-id="19a69-123">Specifies the name of a disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19a69-124">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="19a69-124">-DiskUpdate</span></span>
<span data-ttu-id="19a69-125">Specifica un oggetto di aggiornamento del disco locale.</span><span class="sxs-lookup"><span data-stu-id="19a69-125">Specifies a local disk update object.</span></span>

```yaml
Type: DiskUpdate
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19a69-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19a69-126">-ResourceGroupName</span></span>
<span data-ttu-id="19a69-127">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="19a69-127">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19a69-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="19a69-128">-Confirm</span></span>
<span data-ttu-id="19a69-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19a69-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19a69-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19a69-130">-WhatIf</span></span>
<span data-ttu-id="19a69-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="19a69-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19a69-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="19a69-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19a69-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19a69-133">CommonParameters</span></span>
<span data-ttu-id="19a69-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19a69-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19a69-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19a69-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19a69-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="19a69-136">INPUTS</span></span>

### <span data-ttu-id="19a69-137">System. String</span><span class="sxs-lookup"><span data-stu-id="19a69-137">System.String</span></span>
<span data-ttu-id="19a69-138">Microsoft. Azure. Management. Compute. Models. DiskUpdate Microsoft. Azure. Management. Compute. Models. disk</span><span class="sxs-lookup"><span data-stu-id="19a69-138">Microsoft.Azure.Management.Compute.Models.DiskUpdate Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="19a69-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="19a69-139">OUTPUTS</span></span>

### <span data-ttu-id="19a69-140">System. Object</span><span class="sxs-lookup"><span data-stu-id="19a69-140">System.Object</span></span>

## <span data-ttu-id="19a69-141">Note</span><span class="sxs-lookup"><span data-stu-id="19a69-141">NOTES</span></span>

## <span data-ttu-id="19a69-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="19a69-142">RELATED LINKS</span></span>

