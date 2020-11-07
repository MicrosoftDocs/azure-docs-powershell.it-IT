---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDisk.md
ms.openlocfilehash: 4392c1ccf19474e1a8f73c5bccca2c09f53cbea8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688523"
---
# <span data-ttu-id="abe60-101">New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="abe60-101">New-AzureRmDisk</span></span>

## <span data-ttu-id="abe60-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="abe60-102">SYNOPSIS</span></span>
<span data-ttu-id="abe60-103">Crea un disco gestito.</span><span class="sxs-lookup"><span data-stu-id="abe60-103">Creates a managed disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abe60-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="abe60-104">SYNTAX</span></span>

```
New-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abe60-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="abe60-105">DESCRIPTION</span></span>
<span data-ttu-id="abe60-106">Il cmdlet **New-AzureRmDisk** crea un disco gestito.</span><span class="sxs-lookup"><span data-stu-id="abe60-106">The **New-AzureRmDisk** cmdlet creates a managed disk.</span></span>

## <span data-ttu-id="abe60-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="abe60-107">EXAMPLES</span></span>

### <span data-ttu-id="abe60-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="abe60-108">Example 1</span></span>
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

<span data-ttu-id="abe60-109">Il primo comando crea un oggetto disco locale vuoto con la dimensione 5GB in Standard_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="abe60-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="abe60-110">Imposta anche il tipo di sistema operativo Windows e Abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="abe60-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="abe60-111">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia del disco e della chiave di crittografia per l'oggetto disco.</span><span class="sxs-lookup"><span data-stu-id="abe60-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="abe60-112">L'ultimo comando accetta l'oggetto disk e crea un disco con il nome "Disk01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="abe60-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="abe60-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="abe60-113">PARAMETERS</span></span>

### <span data-ttu-id="abe60-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abe60-114">-DefaultProfile</span></span>
<span data-ttu-id="abe60-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="abe60-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abe60-116">-Disco</span><span class="sxs-lookup"><span data-stu-id="abe60-116">-Disk</span></span>
<span data-ttu-id="abe60-117">Specifica un oggetto disco locale.</span><span class="sxs-lookup"><span data-stu-id="abe60-117">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="abe60-118">-Diskname</span><span class="sxs-lookup"><span data-stu-id="abe60-118">-DiskName</span></span>
<span data-ttu-id="abe60-119">Specifica il nome di un disco.</span><span class="sxs-lookup"><span data-stu-id="abe60-119">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abe60-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abe60-120">-ResourceGroupName</span></span>
<span data-ttu-id="abe60-121">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="abe60-121">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abe60-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="abe60-122">-Confirm</span></span>
<span data-ttu-id="abe60-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="abe60-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abe60-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abe60-124">-WhatIf</span></span>
<span data-ttu-id="abe60-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="abe60-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abe60-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="abe60-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abe60-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abe60-127">CommonParameters</span></span>
<span data-ttu-id="abe60-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abe60-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abe60-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abe60-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abe60-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="abe60-130">INPUTS</span></span>

### <span data-ttu-id="abe60-131">System. String</span><span class="sxs-lookup"><span data-stu-id="abe60-131">System.String</span></span>
<span data-ttu-id="abe60-132">Microsoft. Azure. Management. Compute. Models. disk</span><span class="sxs-lookup"><span data-stu-id="abe60-132">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="abe60-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="abe60-133">OUTPUTS</span></span>

### <span data-ttu-id="abe60-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="abe60-134">System.Object</span></span>

## <span data-ttu-id="abe60-135">Note</span><span class="sxs-lookup"><span data-stu-id="abe60-135">NOTES</span></span>

## <span data-ttu-id="abe60-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="abe60-136">RELATED LINKS</span></span>

