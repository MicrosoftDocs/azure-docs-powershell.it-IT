---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermsnapshotkeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmSnapshotKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmSnapshotKeyEncryptionKey.md
ms.openlocfilehash: c50e9c8bbb65ea7887a39080e21a96c975d320f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521396"
---
# <span data-ttu-id="3240c-101">Set-AzureRmSnapshotKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="3240c-101">Set-AzureRmSnapshotKeyEncryptionKey</span></span>

## <span data-ttu-id="3240c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3240c-102">SYNOPSIS</span></span>
<span data-ttu-id="3240c-103">Imposta le proprietà chiave di crittografia chiave in un oggetto snapshot.</span><span class="sxs-lookup"><span data-stu-id="3240c-103">Sets the key encryption key properties on a snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3240c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3240c-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotKeyEncryptionKey [-Snapshot] <PSSnapshot> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3240c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3240c-105">DESCRIPTION</span></span>
<span data-ttu-id="3240c-106">Il cmdlet **set-AzureRmSnapshotKeyEncryptionKey** imposta le proprietà chiave di crittografia chiave in un oggetto snapshot.</span><span class="sxs-lookup"><span data-stu-id="3240c-106">The **Set-AzureRmSnapshotKeyEncryptionKey** cmdlet sets the key encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="3240c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3240c-107">EXAMPLES</span></span>

### <span data-ttu-id="3240c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3240c-108">Example 1</span></span>
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

<span data-ttu-id="3240c-109">Il primo comando crea un oggetto snapshot locale vuoto con la dimensione 5GB in Standard_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3240c-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="3240c-110">Imposta anche il tipo di sistema operativo Windows e Abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="3240c-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="3240c-111">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia del disco e della chiave di crittografia per l'oggetto snapshot.</span><span class="sxs-lookup"><span data-stu-id="3240c-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="3240c-112">L'ultimo comando accetta l'oggetto snapshot e crea uno snapshot con il nome "Snapshot01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="3240c-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="3240c-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3240c-113">PARAMETERS</span></span>

### <span data-ttu-id="3240c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3240c-114">-DefaultProfile</span></span>
<span data-ttu-id="3240c-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3240c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3240c-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="3240c-116">-KeyUrl</span></span>
<span data-ttu-id="3240c-117">Specifica l'URL della chiave.</span><span class="sxs-lookup"><span data-stu-id="3240c-117">Specifes the key Url.</span></span>

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

### <span data-ttu-id="3240c-118">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="3240c-118">-Snapshot</span></span>
<span data-ttu-id="3240c-119">Specifica un oggetto snapshot locale.</span><span class="sxs-lookup"><span data-stu-id="3240c-119">Specifies a local snapshot object.</span></span>

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

### <span data-ttu-id="3240c-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="3240c-120">-SourceVaultId</span></span>
<span data-ttu-id="3240c-121">Specifica l'ID del Vault di origine.</span><span class="sxs-lookup"><span data-stu-id="3240c-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="3240c-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3240c-122">-Confirm</span></span>
<span data-ttu-id="3240c-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3240c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3240c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3240c-124">-WhatIf</span></span>
<span data-ttu-id="3240c-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3240c-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3240c-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3240c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3240c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3240c-127">CommonParameters</span></span>
<span data-ttu-id="3240c-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3240c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3240c-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3240c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3240c-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3240c-130">INPUTS</span></span>

### <span data-ttu-id="3240c-131">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="3240c-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="3240c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="3240c-132">System.String</span></span>

## <span data-ttu-id="3240c-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3240c-133">OUTPUTS</span></span>

### <span data-ttu-id="3240c-134">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="3240c-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="3240c-135">Note</span><span class="sxs-lookup"><span data-stu-id="3240c-135">NOTES</span></span>

## <span data-ttu-id="3240c-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3240c-136">RELATED LINKS</span></span>
