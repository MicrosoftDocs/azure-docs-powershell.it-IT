---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskUpdateDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskUpdateDiskEncryptionKey.md
ms.openlocfilehash: 4d44bc014a3d38a89e6c9a6a6d755aa9353c052e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518163"
---
# <span data-ttu-id="fc4ec-101">Set-AzureRmDiskUpdateDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="fc4ec-101">Set-AzureRmDiskUpdateDiskEncryptionKey</span></span>

## <span data-ttu-id="fc4ec-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fc4ec-102">SYNOPSIS</span></span>
<span data-ttu-id="fc4ec-103">Imposta le proprietà della chiave di crittografia del disco in un oggetto di aggiornamento del disco.</span><span class="sxs-lookup"><span data-stu-id="fc4ec-103">Sets the disk encryption key properties on a disk update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc4ec-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fc4ec-104">SYNTAX</span></span>

```
Set-AzureRmDiskUpdateDiskEncryptionKey [-DiskUpdate] <DiskUpdate> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc4ec-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fc4ec-105">DESCRIPTION</span></span>
<span data-ttu-id="fc4ec-106">Il cmdlet **set-AzureRmDiskUpdateDiskEncryptionKey** imposta le proprietà della chiave di crittografia del disco in un oggetto di aggiornamento del disco.</span><span class="sxs-lookup"><span data-stu-id="fc4ec-106">The **Set-AzureRmDiskUpdateDiskEncryptionKey** cmdlet sets the disk encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="fc4ec-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fc4ec-107">EXAMPLES</span></span>

### <span data-ttu-id="fc4ec-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fc4ec-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzureRmDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="fc4ec-109">Il primo comando crea un oggetto di aggiornamento del disco vuoto locale con dimensioni 10GB in Premium_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="fc4ec-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="fc4ec-110">Imposta anche il tipo di sistema operativo Windows e Abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="fc4ec-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="fc4ec-111">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia del disco e della chiave di crittografia per l'oggetto aggiornamento disco.</span><span class="sxs-lookup"><span data-stu-id="fc4ec-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="fc4ec-112">L'ultimo comando accetta l'oggetto Update del disco e aggiorna un disco esistente con il nome "Disk01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="fc4ec-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="fc4ec-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fc4ec-113">PARAMETERS</span></span>

### <span data-ttu-id="fc4ec-114">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="fc4ec-114">-DiskUpdate</span></span>
<span data-ttu-id="fc4ec-115">Specifica un oggetto di aggiornamento del disco locale.</span><span class="sxs-lookup"><span data-stu-id="fc4ec-115">Specifies a local disk update object.</span></span>

```yaml
Type: DiskUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc4ec-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="fc4ec-116">-SecretUrl</span></span>
<span data-ttu-id="fc4ec-117">Specifica l'URL segreto.</span><span class="sxs-lookup"><span data-stu-id="fc4ec-117">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="fc4ec-118">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="fc4ec-118">-SourceVaultId</span></span>
<span data-ttu-id="fc4ec-119">Specifica l'ID del Vault di origine.</span><span class="sxs-lookup"><span data-stu-id="fc4ec-119">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="fc4ec-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fc4ec-120">-Confirm</span></span>
<span data-ttu-id="fc4ec-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc4ec-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc4ec-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc4ec-122">-WhatIf</span></span>
<span data-ttu-id="fc4ec-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fc4ec-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fc4ec-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fc4ec-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc4ec-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc4ec-125">CommonParameters</span></span>
<span data-ttu-id="fc4ec-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc4ec-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc4ec-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc4ec-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc4ec-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fc4ec-128">INPUTS</span></span>

### <span data-ttu-id="fc4ec-129">Microsoft. Azure. Management. Compute. Models. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="fc4ec-129">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>
<span data-ttu-id="fc4ec-130">System. String</span><span class="sxs-lookup"><span data-stu-id="fc4ec-130">System.String</span></span>

## <span data-ttu-id="fc4ec-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fc4ec-131">OUTPUTS</span></span>

### <span data-ttu-id="fc4ec-132">Microsoft. Azure. Management. Compute. Models. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="fc4ec-132">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>

## <span data-ttu-id="fc4ec-133">Note</span><span class="sxs-lookup"><span data-stu-id="fc4ec-133">NOTES</span></span>

## <span data-ttu-id="fc4ec-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fc4ec-134">RELATED LINKS</span></span>
