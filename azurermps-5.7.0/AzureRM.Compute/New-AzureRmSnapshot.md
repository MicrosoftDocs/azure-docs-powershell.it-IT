---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmSnapshot.md
ms.openlocfilehash: 2b135efcd36a838bd4fa3c1a907fe7385e2b179c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516875"
---
# <span data-ttu-id="1768e-101">New-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="1768e-101">New-AzureRmSnapshot</span></span>

## <span data-ttu-id="1768e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1768e-102">SYNOPSIS</span></span>
<span data-ttu-id="1768e-103">Crea uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="1768e-103">Creates a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1768e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1768e-104">SYNTAX</span></span>

```
New-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <Snapshot> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1768e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1768e-105">DESCRIPTION</span></span>
<span data-ttu-id="1768e-106">Il cmdlet **New-AzureRmSnapshot** crea uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="1768e-106">The **New-AzureRmSnapshot** cmdlet creates a snapshot.</span></span>

## <span data-ttu-id="1768e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1768e-107">EXAMPLES</span></span>

### <span data-ttu-id="1768e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1768e-108">Example 1</span></span>
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

<span data-ttu-id="1768e-109">Il primo comando crea un oggetto snapshot locale vuoto con la dimensione 5GB in Standard_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1768e-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="1768e-110">Imposta anche il tipo di sistema operativo Windows e Abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="1768e-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="1768e-111">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia del disco e della chiave di crittografia per l'oggetto snapshot.</span><span class="sxs-lookup"><span data-stu-id="1768e-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="1768e-112">L'ultimo comando accetta l'oggetto snapshot e crea uno snapshot con il nome "Snapshot01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="1768e-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="1768e-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1768e-113">PARAMETERS</span></span>

### <span data-ttu-id="1768e-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1768e-114">-ResourceGroupName</span></span>
<span data-ttu-id="1768e-115">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1768e-115">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1768e-116">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="1768e-116">-Snapshot</span></span>
<span data-ttu-id="1768e-117">Specifica un oggetto snapshot locale.</span><span class="sxs-lookup"><span data-stu-id="1768e-117">Specifies a local snapshot object.</span></span>

```yaml
Type: Snapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1768e-118">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="1768e-118">-SnapshotName</span></span>
<span data-ttu-id="1768e-119">Specifica il nome di uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="1768e-119">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="1768e-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1768e-120">-Confirm</span></span>
<span data-ttu-id="1768e-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1768e-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1768e-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1768e-122">-WhatIf</span></span>
<span data-ttu-id="1768e-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1768e-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1768e-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1768e-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1768e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1768e-125">CommonParameters</span></span>
<span data-ttu-id="1768e-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1768e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1768e-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1768e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1768e-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1768e-128">INPUTS</span></span>

### <span data-ttu-id="1768e-129">System. String</span><span class="sxs-lookup"><span data-stu-id="1768e-129">System.String</span></span>
<span data-ttu-id="1768e-130">Microsoft. Azure. Management. Compute. Models. snapshot</span><span class="sxs-lookup"><span data-stu-id="1768e-130">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="1768e-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1768e-131">OUTPUTS</span></span>

### <span data-ttu-id="1768e-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="1768e-132">System.Object</span></span>

## <span data-ttu-id="1768e-133">Note</span><span class="sxs-lookup"><span data-stu-id="1768e-133">NOTES</span></span>

## <span data-ttu-id="1768e-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1768e-134">RELATED LINKS</span></span>

