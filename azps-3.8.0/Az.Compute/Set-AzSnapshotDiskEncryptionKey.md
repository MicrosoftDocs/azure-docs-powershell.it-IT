---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotdiskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotDiskEncryptionKey.md
ms.openlocfilehash: e4ecb281382af308176f47462e086f69c18e6163
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018815"
---
# <span data-ttu-id="52db1-101">Set-AzSnapshotDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="52db1-101">Set-AzSnapshotDiskEncryptionKey</span></span>

## <span data-ttu-id="52db1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="52db1-102">SYNOPSIS</span></span>
<span data-ttu-id="52db1-103">Imposta le proprietà della chiave di crittografia del disco in un oggetto snapshot.</span><span class="sxs-lookup"><span data-stu-id="52db1-103">Sets the disk encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="52db1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="52db1-104">SYNTAX</span></span>

```
Set-AzSnapshotDiskEncryptionKey [-Snapshot] <PSSnapshot> [[-SecretUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52db1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="52db1-105">DESCRIPTION</span></span>
<span data-ttu-id="52db1-106">Il cmdlet **set-AzSnapshotDiskEncryptionKey** imposta le proprietà della chiave di crittografia del disco in un oggetto snapshot.</span><span class="sxs-lookup"><span data-stu-id="52db1-106">The **Set-AzSnapshotDiskEncryptionKey** cmdlet sets the disk encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="52db1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="52db1-107">EXAMPLES</span></span>

### <span data-ttu-id="52db1-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="52db1-108">Example 1</span></span>
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

<span data-ttu-id="52db1-109">Il primo comando crea un oggetto snapshot locale vuoto con la dimensione 5GB in Standard_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="52db1-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="52db1-110">Imposta anche il tipo di sistema operativo Windows e Abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="52db1-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="52db1-111">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia del disco e della chiave di crittografia per l'oggetto snapshot.</span><span class="sxs-lookup"><span data-stu-id="52db1-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="52db1-112">L'ultimo comando accetta l'oggetto snapshot e crea uno snapshot con il nome "Snapshot01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="52db1-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="52db1-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="52db1-113">PARAMETERS</span></span>

### <span data-ttu-id="52db1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52db1-114">-DefaultProfile</span></span>
<span data-ttu-id="52db1-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="52db1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52db1-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="52db1-116">-SecretUrl</span></span>
<span data-ttu-id="52db1-117">Specifica l'URL segreto.</span><span class="sxs-lookup"><span data-stu-id="52db1-117">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="52db1-118">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="52db1-118">-Snapshot</span></span>
<span data-ttu-id="52db1-119">Specifica un oggetto snapshot locale.</span><span class="sxs-lookup"><span data-stu-id="52db1-119">Specifies a local snapshot object.</span></span>

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

### <span data-ttu-id="52db1-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="52db1-120">-SourceVaultId</span></span>
<span data-ttu-id="52db1-121">Specifica l'ID del Vault di origine.</span><span class="sxs-lookup"><span data-stu-id="52db1-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="52db1-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="52db1-122">-Confirm</span></span>
<span data-ttu-id="52db1-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52db1-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52db1-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52db1-124">-WhatIf</span></span>
<span data-ttu-id="52db1-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="52db1-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="52db1-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="52db1-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52db1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52db1-127">CommonParameters</span></span>
<span data-ttu-id="52db1-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52db1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52db1-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52db1-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52db1-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="52db1-130">INPUTS</span></span>

### <span data-ttu-id="52db1-131">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="52db1-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="52db1-132">System. String</span><span class="sxs-lookup"><span data-stu-id="52db1-132">System.String</span></span>

## <span data-ttu-id="52db1-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="52db1-133">OUTPUTS</span></span>

### <span data-ttu-id="52db1-134">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="52db1-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="52db1-135">Note</span><span class="sxs-lookup"><span data-stu-id="52db1-135">NOTES</span></span>

## <span data-ttu-id="52db1-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="52db1-136">RELATED LINKS</span></span>
