---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzSnapshot.md
ms.openlocfilehash: 6cfe2fd958d74740195b0bb29d3defa34f1310a2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031562"
---
# <span data-ttu-id="5625a-101">Update-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="5625a-101">Update-AzSnapshot</span></span>

## <span data-ttu-id="5625a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5625a-102">SYNOPSIS</span></span>
<span data-ttu-id="5625a-103">Aggiorna uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="5625a-103">Updates a snapshot.</span></span>

## <span data-ttu-id="5625a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5625a-104">SYNTAX</span></span>

### <span data-ttu-id="5625a-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5625a-105">DefaultParameter (Default)</span></span>
```
Update-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-SnapshotUpdate] <PSSnapshotUpdate>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5625a-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="5625a-106">FriendMethod</span></span>
```
Update-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <PSSnapshot> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5625a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5625a-107">DESCRIPTION</span></span>
<span data-ttu-id="5625a-108">Il cmdlet **Update-AzSnapshot** aggiorna uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="5625a-108">The **Update-AzSnapshot** cmdlet updates a snapshot.</span></span>

## <span data-ttu-id="5625a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5625a-109">EXAMPLES</span></span>

### <span data-ttu-id="5625a-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5625a-110">Example 1</span></span>
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

<span data-ttu-id="5625a-111">Il primo comando crea un oggetto aggiornamento snapshot locale vuoto con dimensioni 10GB in Premium_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="5625a-111">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="5625a-112">Imposta anche il tipo di sistema operativo Windows e Abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="5625a-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="5625a-113">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia del disco e della chiave di crittografia per l'oggetto aggiornamento snapshot.</span><span class="sxs-lookup"><span data-stu-id="5625a-113">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="5625a-114">L'ultimo comando accetta l'oggetto Update dello snapshot e aggiorna uno snapshot esistente con il nome "Snapshot01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="5625a-114">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="5625a-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="5625a-115">Example 2</span></span>
```
PS C:\> New-AzSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="5625a-116">Questo comando Aggiorna uno snapshot esistente con il nome "Snapshot01" nel gruppo di risorse "ResourceGroup01" in dimensioni del disco di 10 GB.</span><span class="sxs-lookup"><span data-stu-id="5625a-116">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="5625a-117">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="5625a-117">Example 3</span></span>
```
PS C:\> $snapshot = Get-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
PS C:\> $snapshot.DiskSizeGB = 10;
PS C:\> Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshot;
```

<span data-ttu-id="5625a-118">Questi comandi aggiornano inoltre uno snapshot esistente con il nome "Snapshot01" nel gruppo di risorse "ResourceGroup01" in dimensioni del disco di 10 GB.</span><span class="sxs-lookup"><span data-stu-id="5625a-118">These commands also update an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="5625a-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5625a-119">PARAMETERS</span></span>

### <span data-ttu-id="5625a-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5625a-120">-AsJob</span></span>
<span data-ttu-id="5625a-121">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="5625a-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="5625a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5625a-122">-DefaultProfile</span></span>
<span data-ttu-id="5625a-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5625a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5625a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5625a-124">-ResourceGroupName</span></span>
<span data-ttu-id="5625a-125">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5625a-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="5625a-126">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="5625a-126">-Snapshot</span></span>
<span data-ttu-id="5625a-127">Specifica un oggetto snapshot locale.</span><span class="sxs-lookup"><span data-stu-id="5625a-127">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5625a-128">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="5625a-128">-SnapshotName</span></span>
<span data-ttu-id="5625a-129">Specifica il nome di uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="5625a-129">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="5625a-130">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="5625a-130">-SnapshotUpdate</span></span>
<span data-ttu-id="5625a-131">Specifica un oggetto di aggiornamento snapshot locale.</span><span class="sxs-lookup"><span data-stu-id="5625a-131">Specifies a local snapshot update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5625a-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5625a-132">-Confirm</span></span>
<span data-ttu-id="5625a-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5625a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5625a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5625a-134">-WhatIf</span></span>
<span data-ttu-id="5625a-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5625a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5625a-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5625a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5625a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5625a-137">CommonParameters</span></span>
<span data-ttu-id="5625a-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5625a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5625a-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5625a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5625a-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5625a-140">INPUTS</span></span>

### <span data-ttu-id="5625a-141">System. String</span><span class="sxs-lookup"><span data-stu-id="5625a-141">System.String</span></span>

### <span data-ttu-id="5625a-142">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="5625a-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

### <span data-ttu-id="5625a-143">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="5625a-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="5625a-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5625a-144">OUTPUTS</span></span>

### <span data-ttu-id="5625a-145">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="5625a-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="5625a-146">Note</span><span class="sxs-lookup"><span data-stu-id="5625a-146">NOTES</span></span>

## <span data-ttu-id="5625a-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5625a-147">RELATED LINKS</span></span>
