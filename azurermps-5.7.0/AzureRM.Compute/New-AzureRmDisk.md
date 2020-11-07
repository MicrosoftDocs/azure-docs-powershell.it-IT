---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDisk.md
ms.openlocfilehash: 04106c91e99372b985c0a10ac12a7944fdcb4e41
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687933"
---
# <span data-ttu-id="4139a-101">New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="4139a-101">New-AzureRmDisk</span></span>

## <span data-ttu-id="4139a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4139a-102">SYNOPSIS</span></span>
<span data-ttu-id="4139a-103">Crea un disco gestito.</span><span class="sxs-lookup"><span data-stu-id="4139a-103">Creates a managed disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4139a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4139a-104">SYNTAX</span></span>

```
New-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <Disk> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4139a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4139a-105">DESCRIPTION</span></span>
<span data-ttu-id="4139a-106">Il cmdlet **New-AzureRmDisk** crea un disco gestito.</span><span class="sxs-lookup"><span data-stu-id="4139a-106">The **New-AzureRmDisk** cmdlet creates a managed disk.</span></span>

## <span data-ttu-id="4139a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4139a-107">EXAMPLES</span></span>

### <span data-ttu-id="4139a-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4139a-108">Example 1</span></span>
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

<span data-ttu-id="4139a-109">Il primo comando crea un oggetto disco locale vuoto con la dimensione 5GB in Standard_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="4139a-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="4139a-110">Imposta anche il tipo di sistema operativo Windows e Abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="4139a-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="4139a-111">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia del disco e della chiave di crittografia per l'oggetto disco.</span><span class="sxs-lookup"><span data-stu-id="4139a-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="4139a-112">L'ultimo comando accetta l'oggetto disk e crea un disco con il nome "Disk01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="4139a-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="4139a-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4139a-113">PARAMETERS</span></span>

### <span data-ttu-id="4139a-114">-Disco</span><span class="sxs-lookup"><span data-stu-id="4139a-114">-Disk</span></span>
<span data-ttu-id="4139a-115">Specifica un oggetto disco locale.</span><span class="sxs-lookup"><span data-stu-id="4139a-115">Specifies a local disk object.</span></span>

```yaml
Type: Disk
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4139a-116">-Diskname</span><span class="sxs-lookup"><span data-stu-id="4139a-116">-DiskName</span></span>
<span data-ttu-id="4139a-117">Specifica il nome di un disco.</span><span class="sxs-lookup"><span data-stu-id="4139a-117">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="4139a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4139a-118">-ResourceGroupName</span></span>
<span data-ttu-id="4139a-119">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4139a-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="4139a-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4139a-120">-Confirm</span></span>
<span data-ttu-id="4139a-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4139a-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4139a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4139a-122">-WhatIf</span></span>
<span data-ttu-id="4139a-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4139a-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4139a-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4139a-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4139a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4139a-125">CommonParameters</span></span>
<span data-ttu-id="4139a-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4139a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4139a-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4139a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4139a-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4139a-128">INPUTS</span></span>

### <span data-ttu-id="4139a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="4139a-129">System.String</span></span>
<span data-ttu-id="4139a-130">Microsoft. Azure. Management. Compute. Models. disk</span><span class="sxs-lookup"><span data-stu-id="4139a-130">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="4139a-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4139a-131">OUTPUTS</span></span>

### <span data-ttu-id="4139a-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="4139a-132">System.Object</span></span>

## <span data-ttu-id="4139a-133">Note</span><span class="sxs-lookup"><span data-stu-id="4139a-133">NOTES</span></span>

## <span data-ttu-id="4139a-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4139a-134">RELATED LINKS</span></span>

