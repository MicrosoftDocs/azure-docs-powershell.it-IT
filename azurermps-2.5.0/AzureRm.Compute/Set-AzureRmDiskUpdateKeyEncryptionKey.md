---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermdiskupdatekeyencryptionkey
schema: 2.0.0
ms.openlocfilehash: 08f16f7c7cc72623bbb50266403863a10d2fa6f4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866535"
---
# <span data-ttu-id="99dc9-101">Set-AzureRmDiskUpdateKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="99dc9-101">Set-AzureRmDiskUpdateKeyEncryptionKey</span></span>

## <span data-ttu-id="99dc9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="99dc9-102">SYNOPSIS</span></span>
<span data-ttu-id="99dc9-103">Imposta le proprietà chiave di crittografia chiave in un oggetto di aggiornamento del disco.</span><span class="sxs-lookup"><span data-stu-id="99dc9-103">Sets the key encryption key properties on a disk update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99dc9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="99dc9-104">SYNTAX</span></span>

```
Set-AzureRmDiskUpdateKeyEncryptionKey [-DiskUpdate] <PSDiskUpdate> [[-KeyUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="99dc9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="99dc9-105">DESCRIPTION</span></span>
<span data-ttu-id="99dc9-106">Il cmdlet **set-AzureRmDiskUpdateKeyEncryptionKey** imposta le proprietà chiave di crittografia chiave in un oggetto di aggiornamento del disco.</span><span class="sxs-lookup"><span data-stu-id="99dc9-106">The **Set-AzureRmDiskUpdateKeyEncryptionKey** cmdlet sets the key encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="99dc9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="99dc9-107">EXAMPLES</span></span>

### <span data-ttu-id="99dc9-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="99dc9-108">Example 1</span></span>
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

<span data-ttu-id="99dc9-109">Il primo comando crea un oggetto di aggiornamento del disco vuoto locale con dimensioni 10GB in Premium_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="99dc9-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="99dc9-110">Imposta anche il tipo di sistema operativo Windows e Abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="99dc9-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="99dc9-111">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia del disco e della chiave di crittografia per l'oggetto aggiornamento disco.</span><span class="sxs-lookup"><span data-stu-id="99dc9-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="99dc9-112">L'ultimo comando accetta l'oggetto Update del disco e aggiorna un disco esistente con il nome "Disk01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="99dc9-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="99dc9-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="99dc9-113">PARAMETERS</span></span>

### <span data-ttu-id="99dc9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99dc9-114">-DefaultProfile</span></span>
<span data-ttu-id="99dc9-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="99dc9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99dc9-116">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="99dc9-116">-DiskUpdate</span></span>
<span data-ttu-id="99dc9-117">Specifica un oggetto di aggiornamento del disco locale.</span><span class="sxs-lookup"><span data-stu-id="99dc9-117">Specifies a local disk update object.</span></span>

```yaml
Type: PSDiskUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99dc9-118">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="99dc9-118">-KeyUrl</span></span>
<span data-ttu-id="99dc9-119">Specifica l'URL della chiave.</span><span class="sxs-lookup"><span data-stu-id="99dc9-119">Specifes the key Url.</span></span>

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

### <span data-ttu-id="99dc9-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="99dc9-120">-SourceVaultId</span></span>
<span data-ttu-id="99dc9-121">Specifica l'ID del Vault di origine.</span><span class="sxs-lookup"><span data-stu-id="99dc9-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="99dc9-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="99dc9-122">-Confirm</span></span>
<span data-ttu-id="99dc9-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99dc9-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99dc9-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99dc9-124">-WhatIf</span></span>
<span data-ttu-id="99dc9-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="99dc9-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="99dc9-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="99dc9-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99dc9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99dc9-127">CommonParameters</span></span>
<span data-ttu-id="99dc9-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99dc9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99dc9-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99dc9-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99dc9-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="99dc9-130">INPUTS</span></span>

### <span data-ttu-id="99dc9-131">Microsoft. Azure. Management. Compute. Models. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="99dc9-131">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>
<span data-ttu-id="99dc9-132">System. String</span><span class="sxs-lookup"><span data-stu-id="99dc9-132">System.String</span></span>

## <span data-ttu-id="99dc9-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="99dc9-133">OUTPUTS</span></span>

### <span data-ttu-id="99dc9-134">Microsoft. Azure. Management. Compute. Models. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="99dc9-134">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>

## <span data-ttu-id="99dc9-135">Note</span><span class="sxs-lookup"><span data-stu-id="99dc9-135">NOTES</span></span>

## <span data-ttu-id="99dc9-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="99dc9-136">RELATED LINKS</span></span>

