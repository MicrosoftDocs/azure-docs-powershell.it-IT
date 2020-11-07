---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermdiskkeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmDiskKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmDiskKeyEncryptionKey.md
ms.openlocfilehash: 82dd6ed116c1b04790d792cac1aac8f9d7708525
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518820"
---
# <span data-ttu-id="53fd7-101">Set-AzureRmDiskKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="53fd7-101">Set-AzureRmDiskKeyEncryptionKey</span></span>

## <span data-ttu-id="53fd7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="53fd7-102">SYNOPSIS</span></span>
<span data-ttu-id="53fd7-103">Imposta le proprietà chiave di crittografia chiave in un oggetto disco.</span><span class="sxs-lookup"><span data-stu-id="53fd7-103">Sets the key encryption key properties on a disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53fd7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="53fd7-104">SYNTAX</span></span>

```
Set-AzureRmDiskKeyEncryptionKey [-Disk] <PSDisk> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53fd7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="53fd7-105">DESCRIPTION</span></span>
<span data-ttu-id="53fd7-106">Il cmdlet **set-AzureRmDiskKeyEncryptionKey** imposta le proprietà chiave di crittografia chiave su un oggetto disco.</span><span class="sxs-lookup"><span data-stu-id="53fd7-106">The **Set-AzureRmDiskKeyEncryptionKey** cmdlet sets the key encryption key properties on a disk object.</span></span>

## <span data-ttu-id="53fd7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="53fd7-107">EXAMPLES</span></span>

### <span data-ttu-id="53fd7-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="53fd7-108">Example 1</span></span>
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

<span data-ttu-id="53fd7-109">Il primo comando crea un oggetto disco locale vuoto con la dimensione 5GB in Standard_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="53fd7-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="53fd7-110">Imposta anche il tipo di sistema operativo Windows e Abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="53fd7-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="53fd7-111">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia del disco e della chiave di crittografia per l'oggetto disco.</span><span class="sxs-lookup"><span data-stu-id="53fd7-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="53fd7-112">L'ultimo comando accetta l'oggetto disk e crea un disco con il nome "Disk01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="53fd7-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="53fd7-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="53fd7-113">PARAMETERS</span></span>

### <span data-ttu-id="53fd7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53fd7-114">-DefaultProfile</span></span>
<span data-ttu-id="53fd7-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="53fd7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53fd7-116">-Disco</span><span class="sxs-lookup"><span data-stu-id="53fd7-116">-Disk</span></span>
<span data-ttu-id="53fd7-117">Specifica un oggetto disco locale.</span><span class="sxs-lookup"><span data-stu-id="53fd7-117">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53fd7-118">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="53fd7-118">-KeyUrl</span></span>
<span data-ttu-id="53fd7-119">Specifica l'URL della chiave.</span><span class="sxs-lookup"><span data-stu-id="53fd7-119">Specifes the key Url.</span></span>

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

### <span data-ttu-id="53fd7-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="53fd7-120">-SourceVaultId</span></span>
<span data-ttu-id="53fd7-121">Specifica l'ID del Vault di origine.</span><span class="sxs-lookup"><span data-stu-id="53fd7-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="53fd7-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="53fd7-122">-Confirm</span></span>
<span data-ttu-id="53fd7-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53fd7-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53fd7-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53fd7-124">-WhatIf</span></span>
<span data-ttu-id="53fd7-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="53fd7-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="53fd7-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="53fd7-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53fd7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53fd7-127">CommonParameters</span></span>
<span data-ttu-id="53fd7-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53fd7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53fd7-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53fd7-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53fd7-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="53fd7-130">INPUTS</span></span>

### <span data-ttu-id="53fd7-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="53fd7-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

### <span data-ttu-id="53fd7-132">System. String</span><span class="sxs-lookup"><span data-stu-id="53fd7-132">System.String</span></span>

## <span data-ttu-id="53fd7-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="53fd7-133">OUTPUTS</span></span>

### <span data-ttu-id="53fd7-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="53fd7-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="53fd7-135">Note</span><span class="sxs-lookup"><span data-stu-id="53fd7-135">NOTES</span></span>

## <span data-ttu-id="53fd7-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="53fd7-136">RELATED LINKS</span></span>