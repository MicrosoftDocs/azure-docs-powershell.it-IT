---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotkeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotKeyEncryptionKey.md
ms.openlocfilehash: c8a3ce4f0e21ac12f73fbcef6a4cb6c3b6b65bad
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199190"
---
# <span data-ttu-id="0144d-101">Set-AzSnapshotKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="0144d-101">Set-AzSnapshotKeyEncryptionKey</span></span>

## <span data-ttu-id="0144d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0144d-102">SYNOPSIS</span></span>
<span data-ttu-id="0144d-103">Imposta le proprietà della chiave di crittografia su un oggetto snapshot.</span><span class="sxs-lookup"><span data-stu-id="0144d-103">Sets the key encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="0144d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0144d-104">SYNTAX</span></span>

```
Set-AzSnapshotKeyEncryptionKey [-Snapshot] <PSSnapshot> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0144d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0144d-105">DESCRIPTION</span></span>
<span data-ttu-id="0144d-106">Il cmdlet **Set-AzSnapshotKeyEncryptionKey** imposta le proprietà della chiave di crittografia su un oggetto snapshot.</span><span class="sxs-lookup"><span data-stu-id="0144d-106">The **Set-AzSnapshotKeyEncryptionKey** cmdlet sets the key encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="0144d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0144d-107">EXAMPLES</span></span>

### <span data-ttu-id="0144d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0144d-108">Example 1</span></span>
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

<span data-ttu-id="0144d-109">Il primo comando crea un oggetto snapshot vuoto locale con dimensioni di 5 GB Standard_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="0144d-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="0144d-110">Configura anche il tipo di sistema operativo Windows e abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="0144d-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="0144d-111">Il secondo e il terzo comando impostano la chiave di crittografia disco e le relative impostazioni per l'oggetto snapshot.</span><span class="sxs-lookup"><span data-stu-id="0144d-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="0144d-112">L'ultimo comando accetta l'oggetto snapshot e crea uno snapshot con il nome 'Snapshot01' nel gruppo di risorse 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="0144d-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="0144d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0144d-113">PARAMETERS</span></span>

### <span data-ttu-id="0144d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0144d-114">-DefaultProfile</span></span>
<span data-ttu-id="0144d-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0144d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0144d-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="0144d-116">-KeyUrl</span></span>
<span data-ttu-id="0144d-117">Specifica l'URL della chiave.</span><span class="sxs-lookup"><span data-stu-id="0144d-117">Specifies the key Url.</span></span>

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

### <span data-ttu-id="0144d-118">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="0144d-118">-Snapshot</span></span>
<span data-ttu-id="0144d-119">Specifica un oggetto snapshot locale.</span><span class="sxs-lookup"><span data-stu-id="0144d-119">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0144d-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="0144d-120">-SourceVaultId</span></span>
<span data-ttu-id="0144d-121">Specifica l'ID del vault di origine.</span><span class="sxs-lookup"><span data-stu-id="0144d-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="0144d-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0144d-122">-Confirm</span></span>
<span data-ttu-id="0144d-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0144d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0144d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0144d-124">-WhatIf</span></span>
<span data-ttu-id="0144d-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0144d-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0144d-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0144d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0144d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0144d-127">CommonParameters</span></span>
<span data-ttu-id="0144d-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0144d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0144d-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0144d-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0144d-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="0144d-130">INPUTS</span></span>

### <span data-ttu-id="0144d-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="0144d-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="0144d-132">System.String</span><span class="sxs-lookup"><span data-stu-id="0144d-132">System.String</span></span>

## <span data-ttu-id="0144d-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0144d-133">OUTPUTS</span></span>

### <span data-ttu-id="0144d-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="0144d-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="0144d-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="0144d-135">NOTES</span></span>

## <span data-ttu-id="0144d-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0144d-136">RELATED LINKS</span></span>
