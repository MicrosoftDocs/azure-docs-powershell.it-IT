---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskupdatediskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskUpdateDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskUpdateDiskEncryptionKey.md
ms.openlocfilehash: 51a501e2b01ef044685f4172d42bad5342cb462c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364892"
---
# <span data-ttu-id="8a8f3-101">Set-AzDiskUpdateDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="8a8f3-101">Set-AzDiskUpdateDiskEncryptionKey</span></span>

## <span data-ttu-id="8a8f3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8a8f3-102">SYNOPSIS</span></span>
<span data-ttu-id="8a8f3-103">Imposta le proprietà della chiave di crittografia del disco in un oggetto di aggiornamento del disco.</span><span class="sxs-lookup"><span data-stu-id="8a8f3-103">Sets the disk encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="8a8f3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8a8f3-104">SYNTAX</span></span>

```
Set-AzDiskUpdateDiskEncryptionKey [-DiskUpdate] <PSDiskUpdate> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8a8f3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8a8f3-105">DESCRIPTION</span></span>
<span data-ttu-id="8a8f3-106">Il cmdlet **set-AzDiskUpdateDiskEncryptionKey** imposta le proprietà della chiave di crittografia del disco in un oggetto di aggiornamento del disco.</span><span class="sxs-lookup"><span data-stu-id="8a8f3-106">The **Set-AzDiskUpdateDiskEncryptionKey** cmdlet sets the disk encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="8a8f3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8a8f3-107">EXAMPLES</span></span>

### <span data-ttu-id="8a8f3-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8a8f3-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzDiskUpdateConfig -DiskSizeGB 10 -SkuName Premium_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="8a8f3-109">Il primo comando crea un oggetto di aggiornamento del disco vuoto locale con dimensioni 10GB in Premium_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="8a8f3-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="8a8f3-110">Imposta anche il tipo di sistema operativo Windows e Abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="8a8f3-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="8a8f3-111">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia del disco e della chiave di crittografia per l'oggetto aggiornamento disco.</span><span class="sxs-lookup"><span data-stu-id="8a8f3-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="8a8f3-112">L'ultimo comando accetta l'oggetto Update del disco e aggiorna un disco esistente con il nome "Disk01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="8a8f3-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="8a8f3-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8a8f3-113">PARAMETERS</span></span>

### <span data-ttu-id="8a8f3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a8f3-114">-DefaultProfile</span></span>
<span data-ttu-id="8a8f3-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8a8f3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a8f3-116">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="8a8f3-116">-DiskUpdate</span></span>
<span data-ttu-id="8a8f3-117">Specifica un oggetto di aggiornamento del disco locale.</span><span class="sxs-lookup"><span data-stu-id="8a8f3-117">Specifies a local disk update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a8f3-118">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="8a8f3-118">-SecretUrl</span></span>
<span data-ttu-id="8a8f3-119">Specifica l'URL segreto.</span><span class="sxs-lookup"><span data-stu-id="8a8f3-119">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="8a8f3-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="8a8f3-120">-SourceVaultId</span></span>
<span data-ttu-id="8a8f3-121">Specifica l'ID del Vault di origine.</span><span class="sxs-lookup"><span data-stu-id="8a8f3-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="8a8f3-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8a8f3-122">-Confirm</span></span>
<span data-ttu-id="8a8f3-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a8f3-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a8f3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a8f3-124">-WhatIf</span></span>
<span data-ttu-id="8a8f3-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8a8f3-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8a8f3-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8a8f3-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a8f3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a8f3-127">CommonParameters</span></span>
<span data-ttu-id="8a8f3-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a8f3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a8f3-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a8f3-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a8f3-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8a8f3-130">INPUTS</span></span>

### <span data-ttu-id="8a8f3-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="8a8f3-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

### <span data-ttu-id="8a8f3-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8a8f3-132">System.String</span></span>

## <span data-ttu-id="8a8f3-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8a8f3-133">OUTPUTS</span></span>

### <span data-ttu-id="8a8f3-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="8a8f3-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="8a8f3-135">Note</span><span class="sxs-lookup"><span data-stu-id="8a8f3-135">NOTES</span></span>

## <span data-ttu-id="8a8f3-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8a8f3-136">RELATED LINKS</span></span>
