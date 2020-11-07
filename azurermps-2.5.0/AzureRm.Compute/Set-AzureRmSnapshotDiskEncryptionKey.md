---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermsnapshotdiskencryptionkey
schema: 2.0.0
ms.openlocfilehash: f78b680f5872301236c5d001ce9920d2edd61f02
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865943"
---
# <span data-ttu-id="ebdf8-101">Set-AzureRmSnapshotDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="ebdf8-101">Set-AzureRmSnapshotDiskEncryptionKey</span></span>

## <span data-ttu-id="ebdf8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ebdf8-102">SYNOPSIS</span></span>
<span data-ttu-id="ebdf8-103">Imposta le proprietà della chiave di crittografia del disco in un oggetto snapshot.</span><span class="sxs-lookup"><span data-stu-id="ebdf8-103">Sets the disk encryption key properties on a snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ebdf8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ebdf8-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotDiskEncryptionKey [-Snapshot] <PSSnapshot> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ebdf8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ebdf8-105">DESCRIPTION</span></span>
<span data-ttu-id="ebdf8-106">Il cmdlet **set-AzureRmSnapshotDiskEncryptionKey** imposta le proprietà della chiave di crittografia del disco in un oggetto snapshot.</span><span class="sxs-lookup"><span data-stu-id="ebdf8-106">The **Set-AzureRmSnapshotDiskEncryptionKey** cmdlet sets the disk encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="ebdf8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ebdf8-107">EXAMPLES</span></span>

### <span data-ttu-id="ebdf8-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ebdf8-108">Example 1</span></span>
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

<span data-ttu-id="ebdf8-109">Il primo comando crea un oggetto snapshot locale vuoto con la dimensione 5GB in Standard_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ebdf8-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="ebdf8-110">Imposta anche il tipo di sistema operativo Windows e Abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="ebdf8-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="ebdf8-111">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia del disco e della chiave di crittografia per l'oggetto snapshot.</span><span class="sxs-lookup"><span data-stu-id="ebdf8-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="ebdf8-112">L'ultimo comando accetta l'oggetto snapshot e crea uno snapshot con il nome "Snapshot01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="ebdf8-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="ebdf8-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ebdf8-113">PARAMETERS</span></span>

### <span data-ttu-id="ebdf8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebdf8-114">-DefaultProfile</span></span>
<span data-ttu-id="ebdf8-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ebdf8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ebdf8-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="ebdf8-116">-SecretUrl</span></span>
<span data-ttu-id="ebdf8-117">Specifica l'URL segreto.</span><span class="sxs-lookup"><span data-stu-id="ebdf8-117">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="ebdf8-118">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="ebdf8-118">-Snapshot</span></span>
<span data-ttu-id="ebdf8-119">Specifica un oggetto snapshot locale.</span><span class="sxs-lookup"><span data-stu-id="ebdf8-119">Specifies a local snapshot object.</span></span>

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

### <span data-ttu-id="ebdf8-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="ebdf8-120">-SourceVaultId</span></span>
<span data-ttu-id="ebdf8-121">Specifica l'ID del Vault di origine.</span><span class="sxs-lookup"><span data-stu-id="ebdf8-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="ebdf8-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ebdf8-122">-Confirm</span></span>
<span data-ttu-id="ebdf8-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebdf8-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebdf8-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebdf8-124">-WhatIf</span></span>
<span data-ttu-id="ebdf8-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ebdf8-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ebdf8-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ebdf8-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebdf8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebdf8-127">CommonParameters</span></span>
<span data-ttu-id="ebdf8-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebdf8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebdf8-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebdf8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebdf8-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ebdf8-130">INPUTS</span></span>

### <span data-ttu-id="ebdf8-131">Microsoft. Azure. Management. Compute. Models. snapshot</span><span class="sxs-lookup"><span data-stu-id="ebdf8-131">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>
<span data-ttu-id="ebdf8-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ebdf8-132">System.String</span></span>

## <span data-ttu-id="ebdf8-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ebdf8-133">OUTPUTS</span></span>

### <span data-ttu-id="ebdf8-134">Microsoft. Azure. Management. Compute. Models. snapshot</span><span class="sxs-lookup"><span data-stu-id="ebdf8-134">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="ebdf8-135">Note</span><span class="sxs-lookup"><span data-stu-id="ebdf8-135">NOTES</span></span>

## <span data-ttu-id="ebdf8-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ebdf8-136">RELATED LINKS</span></span>

