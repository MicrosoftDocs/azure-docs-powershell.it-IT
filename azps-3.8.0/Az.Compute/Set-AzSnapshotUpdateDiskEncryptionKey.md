---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotupdatediskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotUpdateDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotUpdateDiskEncryptionKey.md
ms.openlocfilehash: b43593650e3eaed25e59526a067c4c569d19d28a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018931"
---
# <span data-ttu-id="8b5be-101">Set-AzSnapshotUpdateDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="8b5be-101">Set-AzSnapshotUpdateDiskEncryptionKey</span></span>

## <span data-ttu-id="8b5be-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8b5be-102">SYNOPSIS</span></span>
<span data-ttu-id="8b5be-103">Imposta le proprietà della chiave di crittografia del disco in un oggetto aggiornamento snapshot.</span><span class="sxs-lookup"><span data-stu-id="8b5be-103">Sets the disk encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="8b5be-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8b5be-104">SYNTAX</span></span>

```
Set-AzSnapshotUpdateDiskEncryptionKey [-SnapshotUpdate] <PSSnapshotUpdate> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8b5be-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8b5be-105">DESCRIPTION</span></span>
<span data-ttu-id="8b5be-106">Il cmdlet **set-AzSnapshotUpdateDiskEncryptionKey** imposta le proprietà della chiave di crittografia del disco in un oggetto aggiornamento snapshot.</span><span class="sxs-lookup"><span data-stu-id="8b5be-106">The **Set-AzSnapshotUpdateDiskEncryptionKey** cmdlet sets the disk encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="8b5be-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8b5be-107">EXAMPLES</span></span>

### <span data-ttu-id="8b5be-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8b5be-108">Example 1</span></span>
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

<span data-ttu-id="8b5be-109">Il primo comando crea un oggetto aggiornamento snapshot locale vuoto con dimensioni 10GB in Premium_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="8b5be-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="8b5be-110">Imposta anche il tipo di sistema operativo Windows e Abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="8b5be-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="8b5be-111">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia del disco e della chiave di crittografia per l'oggetto aggiornamento snapshot.</span><span class="sxs-lookup"><span data-stu-id="8b5be-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="8b5be-112">L'ultimo comando accetta l'oggetto Update dello snapshot e aggiorna uno snapshot esistente con il nome "Snapshot01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="8b5be-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="8b5be-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8b5be-113">PARAMETERS</span></span>

### <span data-ttu-id="8b5be-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b5be-114">-DefaultProfile</span></span>
<span data-ttu-id="8b5be-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8b5be-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b5be-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="8b5be-116">-SecretUrl</span></span>
<span data-ttu-id="8b5be-117">Specifica l'URL segreto.</span><span class="sxs-lookup"><span data-stu-id="8b5be-117">Specifies the secret Url.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b5be-118">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="8b5be-118">-SnapshotUpdate</span></span>
<span data-ttu-id="8b5be-119">Specifica un oggetto di aggiornamento snapshot locale.</span><span class="sxs-lookup"><span data-stu-id="8b5be-119">Specifies a local snapshot update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b5be-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="8b5be-120">-SourceVaultId</span></span>
<span data-ttu-id="8b5be-121">Specifica l'ID del Vault di origine.</span><span class="sxs-lookup"><span data-stu-id="8b5be-121">Specifies the source vault ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b5be-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8b5be-122">-Confirm</span></span>
<span data-ttu-id="8b5be-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b5be-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b5be-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b5be-124">-WhatIf</span></span>
<span data-ttu-id="8b5be-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8b5be-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b5be-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8b5be-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b5be-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b5be-127">CommonParameters</span></span>
<span data-ttu-id="8b5be-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b5be-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b5be-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b5be-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b5be-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8b5be-130">INPUTS</span></span>

### <span data-ttu-id="8b5be-131">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="8b5be-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

### <span data-ttu-id="8b5be-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8b5be-132">System.String</span></span>

## <span data-ttu-id="8b5be-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8b5be-133">OUTPUTS</span></span>

### <span data-ttu-id="8b5be-134">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="8b5be-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="8b5be-135">Note</span><span class="sxs-lookup"><span data-stu-id="8b5be-135">NOTES</span></span>

## <span data-ttu-id="8b5be-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8b5be-136">RELATED LINKS</span></span>
