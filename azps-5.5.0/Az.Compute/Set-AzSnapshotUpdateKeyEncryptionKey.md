---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotupdatekeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotUpdateKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotUpdateKeyEncryptionKey.md
ms.openlocfilehash: a7a52aaa97518fd239e35ea7cf8e4d60689d8888
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204746"
---
# <span data-ttu-id="ce9cf-101">Set-AzSnapshotUpdateKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="ce9cf-101">Set-AzSnapshotUpdateKeyEncryptionKey</span></span>

## <span data-ttu-id="ce9cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce9cf-102">SYNOPSIS</span></span>
<span data-ttu-id="ce9cf-103">Imposta le proprietà della chiave di crittografia per un oggetto di aggiornamento snapshot.</span><span class="sxs-lookup"><span data-stu-id="ce9cf-103">Sets the key encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="ce9cf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ce9cf-104">SYNTAX</span></span>

```
Set-AzSnapshotUpdateKeyEncryptionKey [-SnapshotUpdate] <PSSnapshotUpdate> [[-KeyUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ce9cf-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ce9cf-105">DESCRIPTION</span></span>
<span data-ttu-id="ce9cf-106">Il cmdlet **Set-AzSnapshotUpdateKeyEncryptionKey** imposta le proprietà della chiave di crittografia su un oggetto di aggiornamento snapshot.</span><span class="sxs-lookup"><span data-stu-id="ce9cf-106">The **Set-AzSnapshotUpdateKeyEncryptionKey** cmdlet sets the key encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="ce9cf-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ce9cf-107">EXAMPLES</span></span>

### <span data-ttu-id="ce9cf-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ce9cf-108">Example 1</span></span>
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

<span data-ttu-id="ce9cf-109">Il primo comando crea un oggetto di aggiornamento snapshot vuoto locale con dimensioni di 10 GB Premium_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ce9cf-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="ce9cf-110">Configura anche il tipo di sistema operativo Windows e abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="ce9cf-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="ce9cf-111">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia disco e della chiave di crittografia per l'oggetto di aggiornamento snapshot.</span><span class="sxs-lookup"><span data-stu-id="ce9cf-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="ce9cf-112">L'ultimo comando accetta l'oggetto di aggiornamento snapshot e aggiorna uno snapshot esistente con il nome 'Snapshot01' nel gruppo di risorse 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="ce9cf-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="ce9cf-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ce9cf-113">PARAMETERS</span></span>

### <span data-ttu-id="ce9cf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce9cf-114">-DefaultProfile</span></span>
<span data-ttu-id="ce9cf-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ce9cf-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce9cf-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="ce9cf-116">-KeyUrl</span></span>
<span data-ttu-id="ce9cf-117">Specifica l'URL della chiave.</span><span class="sxs-lookup"><span data-stu-id="ce9cf-117">Specifies the key Url.</span></span>

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

### <span data-ttu-id="ce9cf-118">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="ce9cf-118">-SnapshotUpdate</span></span>
<span data-ttu-id="ce9cf-119">Specifica un oggetto di aggiornamento snapshot locale.</span><span class="sxs-lookup"><span data-stu-id="ce9cf-119">Specifies a local snapshot update object.</span></span>

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

### <span data-ttu-id="ce9cf-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="ce9cf-120">-SourceVaultId</span></span>
<span data-ttu-id="ce9cf-121">Specifica l'ID del vault di origine.</span><span class="sxs-lookup"><span data-stu-id="ce9cf-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="ce9cf-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ce9cf-122">-Confirm</span></span>
<span data-ttu-id="ce9cf-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce9cf-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce9cf-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce9cf-124">-WhatIf</span></span>
<span data-ttu-id="ce9cf-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ce9cf-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ce9cf-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ce9cf-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce9cf-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce9cf-127">CommonParameters</span></span>
<span data-ttu-id="ce9cf-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce9cf-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce9cf-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ce9cf-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce9cf-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="ce9cf-130">INPUTS</span></span>

### <span data-ttu-id="ce9cf-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="ce9cf-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

### <span data-ttu-id="ce9cf-132">System.String</span><span class="sxs-lookup"><span data-stu-id="ce9cf-132">System.String</span></span>

## <span data-ttu-id="ce9cf-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ce9cf-133">OUTPUTS</span></span>

### <span data-ttu-id="ce9cf-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="ce9cf-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="ce9cf-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="ce9cf-135">NOTES</span></span>

## <span data-ttu-id="ce9cf-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ce9cf-136">RELATED LINKS</span></span>
