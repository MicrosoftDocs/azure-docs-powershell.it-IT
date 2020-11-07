---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermsnapshotupdatekeyencryptionkey
schema: 2.0.0
ms.openlocfilehash: 10dde05cb4be4672f81c656ffcb4f2ae732f0916
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865932"
---
# <span data-ttu-id="0c321-101">Set-AzureRmSnapshotUpdateKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="0c321-101">Set-AzureRmSnapshotUpdateKeyEncryptionKey</span></span>

## <span data-ttu-id="0c321-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0c321-102">SYNOPSIS</span></span>
<span data-ttu-id="0c321-103">Imposta le proprietà chiave di crittografia chiave in un oggetto Update di snapshot.</span><span class="sxs-lookup"><span data-stu-id="0c321-103">Sets the key encryption key properties on a snapshot update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c321-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0c321-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotUpdateKeyEncryptionKey [-SnapshotUpdate] <PSSnapshotUpdate> [[-KeyUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0c321-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c321-105">DESCRIPTION</span></span>
<span data-ttu-id="0c321-106">Il cmdlet **set-AzureRmSnapshotUpdateKeyEncryptionKey** imposta le proprietà chiave di crittografia chiave in un oggetto Update snapshot.</span><span class="sxs-lookup"><span data-stu-id="0c321-106">The **Set-AzureRmSnapshotUpdateKeyEncryptionKey** cmdlet sets the key encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="0c321-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0c321-107">EXAMPLES</span></span>

### <span data-ttu-id="0c321-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0c321-108">Example 1</span></span>
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

<span data-ttu-id="0c321-109">Il primo comando crea un oggetto aggiornamento snapshot locale vuoto con dimensioni 10GB in Premium_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="0c321-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="0c321-110">Imposta anche il tipo di sistema operativo Windows e Abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="0c321-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="0c321-111">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia del disco e della chiave di crittografia per l'oggetto aggiornamento snapshot.</span><span class="sxs-lookup"><span data-stu-id="0c321-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="0c321-112">L'ultimo comando accetta l'oggetto Update dello snapshot e aggiorna uno snapshot esistente con il nome "Snapshot01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="0c321-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="0c321-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0c321-113">PARAMETERS</span></span>

### <span data-ttu-id="0c321-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c321-114">-DefaultProfile</span></span>
<span data-ttu-id="0c321-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0c321-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c321-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="0c321-116">-KeyUrl</span></span>
<span data-ttu-id="0c321-117">Specifica l'URL della chiave.</span><span class="sxs-lookup"><span data-stu-id="0c321-117">Specifes the key Url.</span></span>

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

### <span data-ttu-id="0c321-118">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="0c321-118">-SnapshotUpdate</span></span>
<span data-ttu-id="0c321-119">Specifica un oggetto di aggiornamento snapshot locale.</span><span class="sxs-lookup"><span data-stu-id="0c321-119">Specifies a local snapshot update object.</span></span>

```yaml
Type: PSSnapshotUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c321-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="0c321-120">-SourceVaultId</span></span>
<span data-ttu-id="0c321-121">Specifica l'ID del Vault di origine.</span><span class="sxs-lookup"><span data-stu-id="0c321-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="0c321-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0c321-122">-Confirm</span></span>
<span data-ttu-id="0c321-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c321-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c321-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c321-124">-WhatIf</span></span>
<span data-ttu-id="0c321-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0c321-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0c321-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0c321-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c321-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c321-127">CommonParameters</span></span>
<span data-ttu-id="0c321-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c321-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c321-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c321-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c321-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0c321-130">INPUTS</span></span>

### <span data-ttu-id="0c321-131">Microsoft. Azure. Management. Compute. Models. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="0c321-131">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>
<span data-ttu-id="0c321-132">System. String</span><span class="sxs-lookup"><span data-stu-id="0c321-132">System.String</span></span>

## <span data-ttu-id="0c321-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0c321-133">OUTPUTS</span></span>

### <span data-ttu-id="0c321-134">Microsoft. Azure. Management. Compute. Models. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="0c321-134">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>

## <span data-ttu-id="0c321-135">Note</span><span class="sxs-lookup"><span data-stu-id="0c321-135">NOTES</span></span>

## <span data-ttu-id="0c321-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0c321-136">RELATED LINKS</span></span>

