---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmSnapshot.md
ms.openlocfilehash: 71407a78dd19f6324370b88be06841918a4c244a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518335"
---
# <span data-ttu-id="033d2-101">Update-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="033d2-101">Update-AzureRmSnapshot</span></span>

## <span data-ttu-id="033d2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="033d2-102">SYNOPSIS</span></span>
<span data-ttu-id="033d2-103">Aggiorna uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="033d2-103">Updates a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="033d2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="033d2-104">SYNTAX</span></span>

### <span data-ttu-id="033d2-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="033d2-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String>
 [-SnapshotUpdate] <PSSnapshotUpdate> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="033d2-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="033d2-106">FriendMethod</span></span>
```
Update-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <PSSnapshot>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="033d2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="033d2-107">DESCRIPTION</span></span>
<span data-ttu-id="033d2-108">Il cmdlet **Update-AzureRmSnapshot** aggiorna uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="033d2-108">The **Update-AzureRmSnapshot** cmdlet updates a snapshot.</span></span>

## <span data-ttu-id="033d2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="033d2-109">EXAMPLES</span></span>

### <span data-ttu-id="033d2-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="033d2-110">Example 1</span></span>
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

<span data-ttu-id="033d2-111">Il primo comando crea un oggetto aggiornamento snapshot locale vuoto con dimensioni 10GB in Premium_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="033d2-111">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="033d2-112">Imposta anche il tipo di sistema operativo Windows e Abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="033d2-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="033d2-113">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia del disco e della chiave di crittografia per l'oggetto aggiornamento snapshot.</span><span class="sxs-lookup"><span data-stu-id="033d2-113">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="033d2-114">L'ultimo comando accetta l'oggetto Update dello snapshot e aggiorna uno snapshot esistente con il nome "Snapshot01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="033d2-114">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="033d2-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="033d2-115">Example 2</span></span>
```
PS C:\> New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="033d2-116">Questo comando Aggiorna uno snapshot esistente con il nome "Snapshot01" nel gruppo di risorse "ResourceGroup01" in dimensioni del disco di 10 GB.</span><span class="sxs-lookup"><span data-stu-id="033d2-116">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="033d2-117">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="033d2-117">Example 3</span></span>
```
PS C:\> $snapshot = Get-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
PS C:\> $snapshot.DiskSizeGB = 10;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshot;
```

<span data-ttu-id="033d2-118">Questi comandi aggiornano inoltre uno snapshot esistente con il nome "Snapshot01" nel gruppo di risorse "ResourceGroup01" in dimensioni del disco di 10 GB.</span><span class="sxs-lookup"><span data-stu-id="033d2-118">These commands also update an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="033d2-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="033d2-119">PARAMETERS</span></span>

### <span data-ttu-id="033d2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="033d2-120">-DefaultProfile</span></span>
<span data-ttu-id="033d2-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="033d2-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="033d2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="033d2-122">-ResourceGroupName</span></span>
<span data-ttu-id="033d2-123">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="033d2-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="033d2-124">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="033d2-124">-Snapshot</span></span>
<span data-ttu-id="033d2-125">Specifica un oggetto snapshot locale.</span><span class="sxs-lookup"><span data-stu-id="033d2-125">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="033d2-126">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="033d2-126">-SnapshotName</span></span>
<span data-ttu-id="033d2-127">Specifica il nome di uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="033d2-127">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="033d2-128">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="033d2-128">-SnapshotUpdate</span></span>
<span data-ttu-id="033d2-129">Specifica un oggetto di aggiornamento snapshot locale.</span><span class="sxs-lookup"><span data-stu-id="033d2-129">Specifies a local snapshot update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="033d2-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="033d2-130">-Confirm</span></span>
<span data-ttu-id="033d2-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="033d2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="033d2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="033d2-132">-WhatIf</span></span>
<span data-ttu-id="033d2-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="033d2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="033d2-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="033d2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="033d2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="033d2-135">CommonParameters</span></span>
<span data-ttu-id="033d2-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="033d2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="033d2-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="033d2-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="033d2-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="033d2-138">INPUTS</span></span>

### <span data-ttu-id="033d2-139">System. String</span><span class="sxs-lookup"><span data-stu-id="033d2-139">System.String</span></span>
<span data-ttu-id="033d2-140">Microsoft. Azure. Management. Compute. Models. SnapshotUpdate Microsoft. Azure. Management. Compute. Models. snapshot</span><span class="sxs-lookup"><span data-stu-id="033d2-140">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="033d2-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="033d2-141">OUTPUTS</span></span>

### <span data-ttu-id="033d2-142">System. Object</span><span class="sxs-lookup"><span data-stu-id="033d2-142">System.Object</span></span>

## <span data-ttu-id="033d2-143">Note</span><span class="sxs-lookup"><span data-stu-id="033d2-143">NOTES</span></span>

## <span data-ttu-id="033d2-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="033d2-144">RELATED LINKS</span></span>

