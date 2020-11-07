---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermdiskdiskencryptionkey
schema: 2.0.0
ms.openlocfilehash: be8f05b1edd634317fbb7db553e40ab81b28f9c9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866543"
---
# <span data-ttu-id="edd95-101">Set-AzureRmDiskDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="edd95-101">Set-AzureRmDiskDiskEncryptionKey</span></span>

## <span data-ttu-id="edd95-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="edd95-102">SYNOPSIS</span></span>
<span data-ttu-id="edd95-103">Imposta le proprietà della chiave di crittografia del disco in un oggetto disco.</span><span class="sxs-lookup"><span data-stu-id="edd95-103">Sets the disk encryption key properties on a disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="edd95-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="edd95-104">SYNTAX</span></span>

```
Set-AzureRmDiskDiskEncryptionKey [-Disk] <PSDisk> [[-SecretUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edd95-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="edd95-105">DESCRIPTION</span></span>
<span data-ttu-id="edd95-106">Il cmdlet **set-AzureRmDiskDiskEncryptionKey** imposta le proprietà della chiave di crittografia del disco in un oggetto disco.</span><span class="sxs-lookup"><span data-stu-id="edd95-106">The **Set-AzureRmDiskDiskEncryptionKey** cmdlet sets the disk encryption key properties on a disk object.</span></span>

## <span data-ttu-id="edd95-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="edd95-107">EXAMPLES</span></span>

### <span data-ttu-id="edd95-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="edd95-108">Example 1</span></span>
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

<span data-ttu-id="edd95-109">Il primo comando crea un oggetto disco locale vuoto con la dimensione 5GB in Standard_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="edd95-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="edd95-110">Imposta anche il tipo di sistema operativo Windows e Abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="edd95-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="edd95-111">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia del disco e della chiave di crittografia per l'oggetto disco.</span><span class="sxs-lookup"><span data-stu-id="edd95-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="edd95-112">L'ultimo comando accetta l'oggetto disk e crea un disco con il nome "Disk01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="edd95-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="edd95-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="edd95-113">PARAMETERS</span></span>

### <span data-ttu-id="edd95-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edd95-114">-DefaultProfile</span></span>
<span data-ttu-id="edd95-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="edd95-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="edd95-116">-Disco</span><span class="sxs-lookup"><span data-stu-id="edd95-116">-Disk</span></span>
<span data-ttu-id="edd95-117">Specifica un oggetto disco locale.</span><span class="sxs-lookup"><span data-stu-id="edd95-117">Specifies a local disk object.</span></span>

```yaml
Type: PSDisk
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="edd95-118">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="edd95-118">-SecretUrl</span></span>
<span data-ttu-id="edd95-119">Specifica l'URL segreto.</span><span class="sxs-lookup"><span data-stu-id="edd95-119">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="edd95-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="edd95-120">-SourceVaultId</span></span>
<span data-ttu-id="edd95-121">Specifica l'ID del Vault di origine.</span><span class="sxs-lookup"><span data-stu-id="edd95-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="edd95-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="edd95-122">-Confirm</span></span>
<span data-ttu-id="edd95-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="edd95-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edd95-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edd95-124">-WhatIf</span></span>
<span data-ttu-id="edd95-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="edd95-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="edd95-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="edd95-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edd95-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edd95-127">CommonParameters</span></span>
<span data-ttu-id="edd95-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edd95-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edd95-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edd95-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edd95-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="edd95-130">INPUTS</span></span>

### <span data-ttu-id="edd95-131">Microsoft. Azure. Management. Compute. Models. disk</span><span class="sxs-lookup"><span data-stu-id="edd95-131">Microsoft.Azure.Management.Compute.Models.Disk</span></span>
<span data-ttu-id="edd95-132">System. String</span><span class="sxs-lookup"><span data-stu-id="edd95-132">System.String</span></span>

## <span data-ttu-id="edd95-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="edd95-133">OUTPUTS</span></span>

### <span data-ttu-id="edd95-134">Microsoft. Azure. Management. Compute. Models. disk</span><span class="sxs-lookup"><span data-stu-id="edd95-134">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="edd95-135">Note</span><span class="sxs-lookup"><span data-stu-id="edd95-135">NOTES</span></span>

## <span data-ttu-id="edd95-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="edd95-136">RELATED LINKS</span></span>

