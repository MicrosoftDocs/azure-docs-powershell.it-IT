---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskDiskEncryptionKey.md
ms.openlocfilehash: e16b57c4fd674897192714c44620c6913838fc7e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518175"
---
# <span data-ttu-id="875a2-101">Set-AzureRmDiskDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="875a2-101">Set-AzureRmDiskDiskEncryptionKey</span></span>

## <span data-ttu-id="875a2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="875a2-102">SYNOPSIS</span></span>
<span data-ttu-id="875a2-103">Imposta le proprietà della chiave di crittografia del disco in un oggetto disco.</span><span class="sxs-lookup"><span data-stu-id="875a2-103">Sets the disk encryption key properties on a disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="875a2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="875a2-104">SYNTAX</span></span>

```
Set-AzureRmDiskDiskEncryptionKey [-Disk] <Disk> [[-SecretUrl] <String>] [[-SourceVaultId] <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="875a2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="875a2-105">DESCRIPTION</span></span>
<span data-ttu-id="875a2-106">Il cmdlet **set-AzureRmDiskDiskEncryptionKey** imposta le proprietà della chiave di crittografia del disco in un oggetto disco.</span><span class="sxs-lookup"><span data-stu-id="875a2-106">The **Set-AzureRmDiskDiskEncryptionKey** cmdlet sets the disk encryption key properties on a disk object.</span></span>

## <span data-ttu-id="875a2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="875a2-107">EXAMPLES</span></span>

### <span data-ttu-id="875a2-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="875a2-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzureRmDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzureRmDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="875a2-109">Il primo comando crea un oggetto disco locale vuoto con la dimensione 5GB in Standard_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="875a2-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="875a2-110">Imposta anche il tipo di sistema operativo Windows e Abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="875a2-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="875a2-111">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia del disco e della chiave di crittografia per l'oggetto disco.</span><span class="sxs-lookup"><span data-stu-id="875a2-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="875a2-112">L'ultimo comando accetta l'oggetto disk e crea un disco con il nome "Disk01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="875a2-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="875a2-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="875a2-113">PARAMETERS</span></span>

### <span data-ttu-id="875a2-114">-Disco</span><span class="sxs-lookup"><span data-stu-id="875a2-114">-Disk</span></span>
<span data-ttu-id="875a2-115">Specifica un oggetto disco locale.</span><span class="sxs-lookup"><span data-stu-id="875a2-115">Specifies a local disk object.</span></span>

```yaml
Type: Disk
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="875a2-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="875a2-116">-SecretUrl</span></span>
<span data-ttu-id="875a2-117">Specifica l'URL segreto.</span><span class="sxs-lookup"><span data-stu-id="875a2-117">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="875a2-118">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="875a2-118">-SourceVaultId</span></span>
<span data-ttu-id="875a2-119">Specifica l'ID del Vault di origine.</span><span class="sxs-lookup"><span data-stu-id="875a2-119">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="875a2-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="875a2-120">-Confirm</span></span>
<span data-ttu-id="875a2-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="875a2-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="875a2-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="875a2-122">-WhatIf</span></span>
<span data-ttu-id="875a2-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="875a2-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="875a2-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="875a2-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="875a2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="875a2-125">CommonParameters</span></span>
<span data-ttu-id="875a2-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="875a2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="875a2-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="875a2-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="875a2-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="875a2-128">INPUTS</span></span>

### <span data-ttu-id="875a2-129">Microsoft. Azure. Management. Compute. Models. disk</span><span class="sxs-lookup"><span data-stu-id="875a2-129">Microsoft.Azure.Management.Compute.Models.Disk</span></span>
<span data-ttu-id="875a2-130">System. String</span><span class="sxs-lookup"><span data-stu-id="875a2-130">System.String</span></span>

## <span data-ttu-id="875a2-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="875a2-131">OUTPUTS</span></span>

### <span data-ttu-id="875a2-132">Microsoft. Azure. Management. Compute. Models. disk</span><span class="sxs-lookup"><span data-stu-id="875a2-132">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="875a2-133">Note</span><span class="sxs-lookup"><span data-stu-id="875a2-133">NOTES</span></span>

## <span data-ttu-id="875a2-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="875a2-134">RELATED LINKS</span></span>
