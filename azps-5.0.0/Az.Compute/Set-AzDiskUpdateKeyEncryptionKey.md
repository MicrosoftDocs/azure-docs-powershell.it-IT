---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskupdatekeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskUpdateKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskUpdateKeyEncryptionKey.md
ms.openlocfilehash: 73c765d35238d960a95b86c90ad2ff7f2cd5db11
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200965"
---
# <span data-ttu-id="77ec5-101">Set-AzDiskUpdateKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="77ec5-101">Set-AzDiskUpdateKeyEncryptionKey</span></span>

## <span data-ttu-id="77ec5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="77ec5-102">SYNOPSIS</span></span>
<span data-ttu-id="77ec5-103">Imposta le proprietà chiave di crittografia chiave in un oggetto di aggiornamento del disco.</span><span class="sxs-lookup"><span data-stu-id="77ec5-103">Sets the key encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="77ec5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="77ec5-104">SYNTAX</span></span>

```
Set-AzDiskUpdateKeyEncryptionKey [-DiskUpdate] <PSDiskUpdate> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77ec5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="77ec5-105">DESCRIPTION</span></span>
<span data-ttu-id="77ec5-106">Il cmdlet **set-AzDiskUpdateKeyEncryptionKey** imposta le proprietà chiave di crittografia chiave in un oggetto di aggiornamento del disco.</span><span class="sxs-lookup"><span data-stu-id="77ec5-106">The **Set-AzDiskUpdateKeyEncryptionKey** cmdlet sets the key encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="77ec5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="77ec5-107">EXAMPLES</span></span>

### <span data-ttu-id="77ec5-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="77ec5-108">Example 1</span></span>
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

<span data-ttu-id="77ec5-109">Il primo comando crea un oggetto di aggiornamento del disco vuoto locale con dimensioni 10GB in Premium_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="77ec5-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="77ec5-110">Imposta anche il tipo di sistema operativo Windows e Abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="77ec5-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="77ec5-111">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia del disco e della chiave di crittografia per l'oggetto aggiornamento disco.</span><span class="sxs-lookup"><span data-stu-id="77ec5-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="77ec5-112">L'ultimo comando accetta l'oggetto Update del disco e aggiorna un disco esistente con il nome "Disk01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="77ec5-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="77ec5-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="77ec5-113">PARAMETERS</span></span>

### <span data-ttu-id="77ec5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77ec5-114">-DefaultProfile</span></span>
<span data-ttu-id="77ec5-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="77ec5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77ec5-116">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="77ec5-116">-DiskUpdate</span></span>
<span data-ttu-id="77ec5-117">Specifica un oggetto di aggiornamento del disco locale.</span><span class="sxs-lookup"><span data-stu-id="77ec5-117">Specifies a local disk update object.</span></span>

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

### <span data-ttu-id="77ec5-118">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="77ec5-118">-KeyUrl</span></span>
<span data-ttu-id="77ec5-119">Specifica l'URL della chiave.</span><span class="sxs-lookup"><span data-stu-id="77ec5-119">Specifies the key Url.</span></span>

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

### <span data-ttu-id="77ec5-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="77ec5-120">-SourceVaultId</span></span>
<span data-ttu-id="77ec5-121">Specifica l'ID del Vault di origine.</span><span class="sxs-lookup"><span data-stu-id="77ec5-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="77ec5-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="77ec5-122">-Confirm</span></span>
<span data-ttu-id="77ec5-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77ec5-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77ec5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77ec5-124">-WhatIf</span></span>
<span data-ttu-id="77ec5-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="77ec5-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="77ec5-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="77ec5-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77ec5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77ec5-127">CommonParameters</span></span>
<span data-ttu-id="77ec5-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77ec5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77ec5-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77ec5-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77ec5-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="77ec5-130">INPUTS</span></span>

### <span data-ttu-id="77ec5-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="77ec5-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

### <span data-ttu-id="77ec5-132">System. String</span><span class="sxs-lookup"><span data-stu-id="77ec5-132">System.String</span></span>

## <span data-ttu-id="77ec5-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="77ec5-133">OUTPUTS</span></span>

### <span data-ttu-id="77ec5-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="77ec5-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="77ec5-135">Note</span><span class="sxs-lookup"><span data-stu-id="77ec5-135">NOTES</span></span>

## <span data-ttu-id="77ec5-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="77ec5-136">RELATED LINKS</span></span>
