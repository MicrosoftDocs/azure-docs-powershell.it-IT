---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotDiskEncryptionKey.md
ms.openlocfilehash: 05e48bc312dcbbf317906fadb63b9777765032ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512700"
---
# <span data-ttu-id="39d5d-101">Set-AzureRmSnapshotDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="39d5d-101">Set-AzureRmSnapshotDiskEncryptionKey</span></span>

## <span data-ttu-id="39d5d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="39d5d-102">SYNOPSIS</span></span>
<span data-ttu-id="39d5d-103">Imposta le proprietà della chiave di crittografia del disco in un oggetto snapshot.</span><span class="sxs-lookup"><span data-stu-id="39d5d-103">Sets the disk encryption key properties on a snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39d5d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="39d5d-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotDiskEncryptionKey [-Snapshot] <Snapshot> [[-SecretUrl] <String>] [[-SourceVaultId] <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39d5d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="39d5d-105">DESCRIPTION</span></span>
<span data-ttu-id="39d5d-106">Il cmdlet **set-AzureRmSnapshotDiskEncryptionKey** imposta le proprietà della chiave di crittografia del disco in un oggetto snapshot.</span><span class="sxs-lookup"><span data-stu-id="39d5d-106">The **Set-AzureRmSnapshotDiskEncryptionKey** cmdlet sets the disk encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="39d5d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="39d5d-107">EXAMPLES</span></span>

### <span data-ttu-id="39d5d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="39d5d-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzureRmSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzureRmSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzureRmSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="39d5d-109">Il primo comando crea un oggetto snapshot locale vuoto con la dimensione 5GB in Standard_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="39d5d-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="39d5d-110">Imposta anche il tipo di sistema operativo Windows e Abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="39d5d-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="39d5d-111">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia del disco e della chiave di crittografia per l'oggetto snapshot.</span><span class="sxs-lookup"><span data-stu-id="39d5d-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="39d5d-112">L'ultimo comando accetta l'oggetto snapshot e crea uno snapshot con il nome "Snapshot01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="39d5d-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="39d5d-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="39d5d-113">PARAMETERS</span></span>

### <span data-ttu-id="39d5d-114">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="39d5d-114">-SecretUrl</span></span>
<span data-ttu-id="39d5d-115">Specifica l'URL segreto.</span><span class="sxs-lookup"><span data-stu-id="39d5d-115">Specifies the secret Url.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39d5d-116">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="39d5d-116">-Snapshot</span></span>
<span data-ttu-id="39d5d-117">Specifica un oggetto snapshot locale.</span><span class="sxs-lookup"><span data-stu-id="39d5d-117">Specifies a local snapshot object.</span></span>

```yaml
Type: Snapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39d5d-118">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="39d5d-118">-SourceVaultId</span></span>
<span data-ttu-id="39d5d-119">Specifica l'ID del Vault di origine.</span><span class="sxs-lookup"><span data-stu-id="39d5d-119">Specifies the source vault ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39d5d-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="39d5d-120">-Confirm</span></span>
<span data-ttu-id="39d5d-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39d5d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39d5d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39d5d-122">-WhatIf</span></span>
<span data-ttu-id="39d5d-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="39d5d-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="39d5d-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="39d5d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39d5d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39d5d-125">CommonParameters</span></span>
<span data-ttu-id="39d5d-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39d5d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39d5d-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39d5d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39d5d-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="39d5d-128">INPUTS</span></span>

### <span data-ttu-id="39d5d-129">Microsoft. Azure. Management. Compute. Models. snapshot</span><span class="sxs-lookup"><span data-stu-id="39d5d-129">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>
<span data-ttu-id="39d5d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="39d5d-130">System.String</span></span>

## <span data-ttu-id="39d5d-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="39d5d-131">OUTPUTS</span></span>

### <span data-ttu-id="39d5d-132">Microsoft. Azure. Management. Compute. Models. snapshot</span><span class="sxs-lookup"><span data-stu-id="39d5d-132">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="39d5d-133">Note</span><span class="sxs-lookup"><span data-stu-id="39d5d-133">NOTES</span></span>

## <span data-ttu-id="39d5d-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="39d5d-134">RELATED LINKS</span></span>

