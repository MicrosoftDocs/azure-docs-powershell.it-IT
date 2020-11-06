---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotKeyEncryptionKey.md
ms.openlocfilehash: 9c6debcae0aa83dd08374c7e390e3a42c4e5233a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508324"
---
# <span data-ttu-id="03244-101">Set-AzureRmSnapshotKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="03244-101">Set-AzureRmSnapshotKeyEncryptionKey</span></span>

## <span data-ttu-id="03244-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="03244-102">SYNOPSIS</span></span>
<span data-ttu-id="03244-103">Imposta le proprietà chiave di crittografia chiave in un oggetto snapshot.</span><span class="sxs-lookup"><span data-stu-id="03244-103">Sets the key encryption key properties on a snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03244-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="03244-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotKeyEncryptionKey [-Snapshot] <Snapshot> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03244-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="03244-105">DESCRIPTION</span></span>
<span data-ttu-id="03244-106">Il cmdlet **set-AzureRmSnapshotKeyEncryptionKey** imposta le proprietà chiave di crittografia chiave in un oggetto snapshot.</span><span class="sxs-lookup"><span data-stu-id="03244-106">The **Set-AzureRmSnapshotKeyEncryptionKey** cmdlet sets the key encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="03244-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="03244-107">EXAMPLES</span></span>

### <span data-ttu-id="03244-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="03244-108">Example 1</span></span>
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

<span data-ttu-id="03244-109">Il primo comando crea un oggetto snapshot locale vuoto con la dimensione 5GB in Standard_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="03244-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="03244-110">Imposta anche il tipo di sistema operativo Windows e Abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="03244-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="03244-111">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia del disco e della chiave di crittografia per l'oggetto snapshot.</span><span class="sxs-lookup"><span data-stu-id="03244-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="03244-112">L'ultimo comando accetta l'oggetto snapshot e crea uno snapshot con il nome "Snapshot01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="03244-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="03244-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="03244-113">PARAMETERS</span></span>

### <span data-ttu-id="03244-114">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="03244-114">-KeyUrl</span></span>
<span data-ttu-id="03244-115">Specifica l'URL della chiave.</span><span class="sxs-lookup"><span data-stu-id="03244-115">Specifes the key Url.</span></span>

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

### <span data-ttu-id="03244-116">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="03244-116">-Snapshot</span></span>
<span data-ttu-id="03244-117">Specifica un oggetto snapshot locale.</span><span class="sxs-lookup"><span data-stu-id="03244-117">Specifies a local snapshot object.</span></span>

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

### <span data-ttu-id="03244-118">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="03244-118">-SourceVaultId</span></span>
<span data-ttu-id="03244-119">Specifica l'ID del Vault di origine.</span><span class="sxs-lookup"><span data-stu-id="03244-119">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="03244-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="03244-120">-Confirm</span></span>
<span data-ttu-id="03244-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03244-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03244-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03244-122">-WhatIf</span></span>
<span data-ttu-id="03244-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="03244-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="03244-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="03244-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03244-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03244-125">CommonParameters</span></span>
<span data-ttu-id="03244-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03244-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03244-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03244-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03244-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="03244-128">INPUTS</span></span>

### <span data-ttu-id="03244-129">Microsoft. Azure. Management. Compute. Models. snapshot</span><span class="sxs-lookup"><span data-stu-id="03244-129">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>
<span data-ttu-id="03244-130">System. String</span><span class="sxs-lookup"><span data-stu-id="03244-130">System.String</span></span>

## <span data-ttu-id="03244-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="03244-131">OUTPUTS</span></span>

### <span data-ttu-id="03244-132">Microsoft. Azure. Management. Compute. Models. snapshot</span><span class="sxs-lookup"><span data-stu-id="03244-132">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="03244-133">Note</span><span class="sxs-lookup"><span data-stu-id="03244-133">NOTES</span></span>

## <span data-ttu-id="03244-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="03244-134">RELATED LINKS</span></span>

