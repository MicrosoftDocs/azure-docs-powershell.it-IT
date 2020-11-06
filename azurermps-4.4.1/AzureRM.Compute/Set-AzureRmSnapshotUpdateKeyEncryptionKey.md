---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotUpdateKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotUpdateKeyEncryptionKey.md
ms.openlocfilehash: 5fd03c0c262500b79d40063bc1ad35898eda110f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511271"
---
# <span data-ttu-id="fd2aa-101">Set-AzureRmSnapshotUpdateKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="fd2aa-101">Set-AzureRmSnapshotUpdateKeyEncryptionKey</span></span>

## <span data-ttu-id="fd2aa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fd2aa-102">SYNOPSIS</span></span>
<span data-ttu-id="fd2aa-103">Imposta le proprietà chiave di crittografia chiave in un oggetto Update di snapshot.</span><span class="sxs-lookup"><span data-stu-id="fd2aa-103">Sets the key encryption key properties on a snapshot update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd2aa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fd2aa-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotUpdateKeyEncryptionKey [-SnapshotUpdate] <PSSnapshotUpdate> [[-KeyUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fd2aa-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fd2aa-105">DESCRIPTION</span></span>
<span data-ttu-id="fd2aa-106">Il cmdlet **set-AzureRmSnapshotUpdateKeyEncryptionKey** imposta le proprietà chiave di crittografia chiave in un oggetto Update snapshot.</span><span class="sxs-lookup"><span data-stu-id="fd2aa-106">The **Set-AzureRmSnapshotUpdateKeyEncryptionKey** cmdlet sets the key encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="fd2aa-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fd2aa-107">EXAMPLES</span></span>

### <span data-ttu-id="fd2aa-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fd2aa-108">Example 1</span></span>
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

<span data-ttu-id="fd2aa-109">Il primo comando crea un oggetto aggiornamento snapshot locale vuoto con dimensioni 10GB in Premium_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="fd2aa-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="fd2aa-110">Imposta anche il tipo di sistema operativo Windows e Abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="fd2aa-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="fd2aa-111">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia del disco e della chiave di crittografia per l'oggetto aggiornamento snapshot.</span><span class="sxs-lookup"><span data-stu-id="fd2aa-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="fd2aa-112">L'ultimo comando accetta l'oggetto Update dello snapshot e aggiorna uno snapshot esistente con il nome "Snapshot01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="fd2aa-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="fd2aa-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fd2aa-113">PARAMETERS</span></span>

### <span data-ttu-id="fd2aa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd2aa-114">-DefaultProfile</span></span>
<span data-ttu-id="fd2aa-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fd2aa-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd2aa-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="fd2aa-116">-KeyUrl</span></span>
<span data-ttu-id="fd2aa-117">Specifica l'URL della chiave.</span><span class="sxs-lookup"><span data-stu-id="fd2aa-117">Specifes the key Url.</span></span>

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

### <span data-ttu-id="fd2aa-118">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="fd2aa-118">-SnapshotUpdate</span></span>
<span data-ttu-id="fd2aa-119">Specifica un oggetto di aggiornamento snapshot locale.</span><span class="sxs-lookup"><span data-stu-id="fd2aa-119">Specifies a local snapshot update object.</span></span>

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

### <span data-ttu-id="fd2aa-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="fd2aa-120">-SourceVaultId</span></span>
<span data-ttu-id="fd2aa-121">Specifica l'ID del Vault di origine.</span><span class="sxs-lookup"><span data-stu-id="fd2aa-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="fd2aa-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fd2aa-122">-Confirm</span></span>
<span data-ttu-id="fd2aa-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd2aa-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd2aa-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd2aa-124">-WhatIf</span></span>
<span data-ttu-id="fd2aa-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fd2aa-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd2aa-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fd2aa-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd2aa-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd2aa-127">CommonParameters</span></span>
<span data-ttu-id="fd2aa-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd2aa-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd2aa-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd2aa-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd2aa-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fd2aa-130">INPUTS</span></span>

### <span data-ttu-id="fd2aa-131">Microsoft. Azure. Management. Compute. Models. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="fd2aa-131">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>
<span data-ttu-id="fd2aa-132">System. String</span><span class="sxs-lookup"><span data-stu-id="fd2aa-132">System.String</span></span>

## <span data-ttu-id="fd2aa-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fd2aa-133">OUTPUTS</span></span>

### <span data-ttu-id="fd2aa-134">Microsoft. Azure. Management. Compute. Models. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="fd2aa-134">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>

## <span data-ttu-id="fd2aa-135">Note</span><span class="sxs-lookup"><span data-stu-id="fd2aa-135">NOTES</span></span>

## <span data-ttu-id="fd2aa-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fd2aa-136">RELATED LINKS</span></span>

