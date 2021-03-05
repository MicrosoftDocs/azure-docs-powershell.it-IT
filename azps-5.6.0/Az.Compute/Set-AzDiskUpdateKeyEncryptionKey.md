---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azdiskupdatekeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskUpdateKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskUpdateKeyEncryptionKey.md
ms.openlocfilehash: 559eb4272296774fa385e83f728d126e1d5a8295
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988313"
---
# <span data-ttu-id="9e2ad-101">Set-AzDiskUpdateKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="9e2ad-101">Set-AzDiskUpdateKeyEncryptionKey</span></span>

## <span data-ttu-id="9e2ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e2ad-102">SYNOPSIS</span></span>
<span data-ttu-id="9e2ad-103">Imposta le proprietà della chiave di crittografia in un oggetto di aggiornamento del disco.</span><span class="sxs-lookup"><span data-stu-id="9e2ad-103">Sets the key encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="9e2ad-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9e2ad-104">SYNTAX</span></span>

```
Set-AzDiskUpdateKeyEncryptionKey [-DiskUpdate] <PSDiskUpdate> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e2ad-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9e2ad-105">DESCRIPTION</span></span>
<span data-ttu-id="9e2ad-106">Il cmdlet **Set-AzDiskUpdateKeyEncryptionKey** imposta le proprietà della chiave di crittografia su un oggetto di aggiornamento del disco.</span><span class="sxs-lookup"><span data-stu-id="9e2ad-106">The **Set-AzDiskUpdateKeyEncryptionKey** cmdlet sets the key encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="9e2ad-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9e2ad-107">EXAMPLES</span></span>

### <span data-ttu-id="9e2ad-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9e2ad-108">Example 1</span></span>
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

<span data-ttu-id="9e2ad-109">Il primo comando crea un oggetto di aggiornamento disco vuoto locale con dimensioni di 10 GB Premium_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="9e2ad-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="9e2ad-110">Configura anche il tipo di sistema operativo Windows e abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="9e2ad-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="9e2ad-111">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia disco e della chiave di crittografia per l'oggetto di aggiornamento del disco.</span><span class="sxs-lookup"><span data-stu-id="9e2ad-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="9e2ad-112">L'ultimo comando accetta l'oggetto di aggiornamento del disco e aggiorna un disco esistente con il nome 'Disco01' nel gruppo di risorse 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="9e2ad-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="9e2ad-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e2ad-113">PARAMETERS</span></span>

### <span data-ttu-id="9e2ad-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e2ad-114">-DefaultProfile</span></span>
<span data-ttu-id="9e2ad-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9e2ad-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e2ad-116">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="9e2ad-116">-DiskUpdate</span></span>
<span data-ttu-id="9e2ad-117">Specifica un oggetto di aggiornamento del disco locale.</span><span class="sxs-lookup"><span data-stu-id="9e2ad-117">Specifies a local disk update object.</span></span>

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

### <span data-ttu-id="9e2ad-118">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="9e2ad-118">-KeyUrl</span></span>
<span data-ttu-id="9e2ad-119">Specifica l'URL della chiave.</span><span class="sxs-lookup"><span data-stu-id="9e2ad-119">Specifies the key Url.</span></span>

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

### <span data-ttu-id="9e2ad-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="9e2ad-120">-SourceVaultId</span></span>
<span data-ttu-id="9e2ad-121">Specifica l'ID del vault di origine.</span><span class="sxs-lookup"><span data-stu-id="9e2ad-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="9e2ad-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9e2ad-122">-Confirm</span></span>
<span data-ttu-id="9e2ad-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e2ad-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e2ad-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e2ad-124">-WhatIf</span></span>
<span data-ttu-id="9e2ad-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9e2ad-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9e2ad-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9e2ad-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e2ad-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e2ad-127">CommonParameters</span></span>
<span data-ttu-id="9e2ad-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e2ad-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e2ad-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9e2ad-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e2ad-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="9e2ad-130">INPUTS</span></span>

### <span data-ttu-id="9e2ad-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="9e2ad-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

### <span data-ttu-id="9e2ad-132">System.String</span><span class="sxs-lookup"><span data-stu-id="9e2ad-132">System.String</span></span>

## <span data-ttu-id="9e2ad-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9e2ad-133">OUTPUTS</span></span>

### <span data-ttu-id="9e2ad-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="9e2ad-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="9e2ad-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="9e2ad-135">NOTES</span></span>

## <span data-ttu-id="9e2ad-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9e2ad-136">RELATED LINKS</span></span>
