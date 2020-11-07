---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotkeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzSnapshotKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzSnapshotKeyEncryptionKey.md
ms.openlocfilehash: 5812bdf70a7661603aad60ece9577926ef10ffb6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863433"
---
# <span data-ttu-id="ce2c4-101">Set-AzSnapshotKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="ce2c4-101">Set-AzSnapshotKeyEncryptionKey</span></span>

## <span data-ttu-id="ce2c4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ce2c4-102">SYNOPSIS</span></span>
<span data-ttu-id="ce2c4-103">Imposta le proprietà chiave di crittografia chiave in un oggetto snapshot.</span><span class="sxs-lookup"><span data-stu-id="ce2c4-103">Sets the key encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="ce2c4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ce2c4-104">SYNTAX</span></span>

```
Set-AzSnapshotKeyEncryptionKey [-Snapshot] <PSSnapshot> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce2c4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ce2c4-105">DESCRIPTION</span></span>
<span data-ttu-id="ce2c4-106">Il cmdlet **set-AzSnapshotKeyEncryptionKey** imposta le proprietà chiave di crittografia chiave in un oggetto snapshot.</span><span class="sxs-lookup"><span data-stu-id="ce2c4-106">The **Set-AzSnapshotKeyEncryptionKey** cmdlet sets the key encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="ce2c4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ce2c4-107">EXAMPLES</span></span>

### <span data-ttu-id="ce2c4-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ce2c4-108">Example 1</span></span>
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

<span data-ttu-id="ce2c4-109">Il primo comando crea un oggetto snapshot locale vuoto con la dimensione 5GB in Standard_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ce2c4-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="ce2c4-110">Imposta anche il tipo di sistema operativo Windows e Abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="ce2c4-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="ce2c4-111">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia del disco e della chiave di crittografia per l'oggetto snapshot.</span><span class="sxs-lookup"><span data-stu-id="ce2c4-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="ce2c4-112">L'ultimo comando accetta l'oggetto snapshot e crea uno snapshot con il nome "Snapshot01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="ce2c4-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="ce2c4-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ce2c4-113">PARAMETERS</span></span>

### <span data-ttu-id="ce2c4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce2c4-114">-DefaultProfile</span></span>
<span data-ttu-id="ce2c4-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ce2c4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce2c4-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="ce2c4-116">-KeyUrl</span></span>
<span data-ttu-id="ce2c4-117">Specifica l'URL della chiave.</span><span class="sxs-lookup"><span data-stu-id="ce2c4-117">Specifes the key Url.</span></span>

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

### <span data-ttu-id="ce2c4-118">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="ce2c4-118">-Snapshot</span></span>
<span data-ttu-id="ce2c4-119">Specifica un oggetto snapshot locale.</span><span class="sxs-lookup"><span data-stu-id="ce2c4-119">Specifies a local snapshot object.</span></span>

```yaml
Type: PSSnapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce2c4-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="ce2c4-120">-SourceVaultId</span></span>
<span data-ttu-id="ce2c4-121">Specifica l'ID del Vault di origine.</span><span class="sxs-lookup"><span data-stu-id="ce2c4-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="ce2c4-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ce2c4-122">-Confirm</span></span>
<span data-ttu-id="ce2c4-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce2c4-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce2c4-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce2c4-124">-WhatIf</span></span>
<span data-ttu-id="ce2c4-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ce2c4-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ce2c4-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ce2c4-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce2c4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce2c4-127">CommonParameters</span></span>
<span data-ttu-id="ce2c4-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce2c4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce2c4-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce2c4-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce2c4-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ce2c4-130">INPUTS</span></span>

### <span data-ttu-id="ce2c4-131">Microsoft. Azure. Management. Compute. Models. snapshot</span><span class="sxs-lookup"><span data-stu-id="ce2c4-131">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>
<span data-ttu-id="ce2c4-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ce2c4-132">System.String</span></span>

## <span data-ttu-id="ce2c4-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ce2c4-133">OUTPUTS</span></span>

### <span data-ttu-id="ce2c4-134">Microsoft. Azure. Management. Compute. Models. snapshot</span><span class="sxs-lookup"><span data-stu-id="ce2c4-134">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="ce2c4-135">Note</span><span class="sxs-lookup"><span data-stu-id="ce2c4-135">NOTES</span></span>

## <span data-ttu-id="ce2c4-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ce2c4-136">RELATED LINKS</span></span>

