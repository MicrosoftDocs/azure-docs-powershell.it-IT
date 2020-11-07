---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermsnapshot
schema: 2.0.0
ms.openlocfilehash: 2e8b538e9a6f5f9fce2fb768bc0c77d0c82c55f0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93867115"
---
# <span data-ttu-id="0390e-101">Update-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="0390e-101">Update-AzureRmSnapshot</span></span>

## <span data-ttu-id="0390e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0390e-102">SYNOPSIS</span></span>
<span data-ttu-id="0390e-103">Aggiorna uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="0390e-103">Updates a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0390e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0390e-104">SYNTAX</span></span>

### <span data-ttu-id="0390e-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0390e-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String>
 [-SnapshotUpdate] <PSSnapshotUpdate> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0390e-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="0390e-106">FriendMethod</span></span>
```
Update-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <PSSnapshot> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0390e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0390e-107">DESCRIPTION</span></span>
<span data-ttu-id="0390e-108">Il cmdlet **Update-AzureRmSnapshot** aggiorna uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="0390e-108">The **Update-AzureRmSnapshot** cmdlet updates a snapshot.</span></span>

## <span data-ttu-id="0390e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0390e-109">EXAMPLES</span></span>

### <span data-ttu-id="0390e-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0390e-110">Example 1</span></span>
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

<span data-ttu-id="0390e-111">Il primo comando crea un oggetto aggiornamento snapshot locale vuoto con dimensioni 10GB in Premium_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="0390e-111">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="0390e-112">Imposta anche il tipo di sistema operativo Windows e Abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="0390e-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="0390e-113">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia del disco e della chiave di crittografia per l'oggetto aggiornamento snapshot.</span><span class="sxs-lookup"><span data-stu-id="0390e-113">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="0390e-114">L'ultimo comando accetta l'oggetto Update dello snapshot e aggiorna uno snapshot esistente con il nome "Snapshot01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="0390e-114">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="0390e-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="0390e-115">Example 2</span></span>
```
PS C:\> New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="0390e-116">Questo comando Aggiorna uno snapshot esistente con il nome "Snapshot01" nel gruppo di risorse "ResourceGroup01" in dimensioni del disco di 10 GB.</span><span class="sxs-lookup"><span data-stu-id="0390e-116">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="0390e-117">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="0390e-117">Example 3</span></span>
```
PS C:\> $snapshot = Get-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
PS C:\> $snapshot.DiskSizeGB = 10;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshot;
```

<span data-ttu-id="0390e-118">Questi comandi aggiornano inoltre uno snapshot esistente con il nome "Snapshot01" nel gruppo di risorse "ResourceGroup01" in dimensioni del disco di 10 GB.</span><span class="sxs-lookup"><span data-stu-id="0390e-118">These commands also update an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="0390e-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0390e-119">PARAMETERS</span></span>

### <span data-ttu-id="0390e-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0390e-120">-AsJob</span></span>
<span data-ttu-id="0390e-121">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="0390e-121">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0390e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0390e-122">-DefaultProfile</span></span>
<span data-ttu-id="0390e-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0390e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0390e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0390e-124">-ResourceGroupName</span></span>
<span data-ttu-id="0390e-125">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0390e-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="0390e-126">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="0390e-126">-Snapshot</span></span>
<span data-ttu-id="0390e-127">Specifica un oggetto snapshot locale.</span><span class="sxs-lookup"><span data-stu-id="0390e-127">Specifies a local snapshot object.</span></span>

```yaml
Type: PSSnapshot
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0390e-128">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="0390e-128">-SnapshotName</span></span>
<span data-ttu-id="0390e-129">Specifica il nome di uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="0390e-129">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="0390e-130">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="0390e-130">-SnapshotUpdate</span></span>
<span data-ttu-id="0390e-131">Specifica un oggetto di aggiornamento snapshot locale.</span><span class="sxs-lookup"><span data-stu-id="0390e-131">Specifies a local snapshot update object.</span></span>

```yaml
Type: PSSnapshotUpdate
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0390e-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0390e-132">-Confirm</span></span>
<span data-ttu-id="0390e-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0390e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0390e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0390e-134">-WhatIf</span></span>
<span data-ttu-id="0390e-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0390e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0390e-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0390e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0390e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0390e-137">CommonParameters</span></span>
<span data-ttu-id="0390e-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0390e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0390e-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0390e-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0390e-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0390e-140">INPUTS</span></span>

### <span data-ttu-id="0390e-141">System. String</span><span class="sxs-lookup"><span data-stu-id="0390e-141">System.String</span></span>
<span data-ttu-id="0390e-142">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshotUpdate Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="0390e-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="0390e-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0390e-143">OUTPUTS</span></span>

### <span data-ttu-id="0390e-144">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="0390e-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="0390e-145">Note</span><span class="sxs-lookup"><span data-stu-id="0390e-145">NOTES</span></span>

## <span data-ttu-id="0390e-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0390e-146">RELATED LINKS</span></span>

