---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVault.md
ms.openlocfilehash: 7d2bb9d961b5fba7ecd5e0d83f8d86ac1a930c75
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180494"
---
# <span data-ttu-id="081ed-101">Backup-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="081ed-101">Backup-AzKeyVault</span></span>

## <span data-ttu-id="081ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="081ed-102">SYNOPSIS</span></span>
<span data-ttu-id="081ed-103">Eseguire il backup completo di un HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="081ed-103">Fully backup a managed HSM.</span></span>

## <span data-ttu-id="081ed-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="081ed-104">SYNTAX</span></span>

### <span data-ttu-id="081ed-105">InteractiveStorageName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="081ed-105">InteractiveStorageName (Default)</span></span>
```
Backup-AzKeyVault [-HsmName] <String> -StorageAccountName <String> -StorageContainerName <String>
 -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="081ed-106">InteractiveStorageUri</span><span class="sxs-lookup"><span data-stu-id="081ed-106">InteractiveStorageUri</span></span>
```
Backup-AzKeyVault [-HsmName] <String> -StorageContainerUri <Uri> -SasToken <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="081ed-107">InputObjectStorageUri</span><span class="sxs-lookup"><span data-stu-id="081ed-107">InputObjectStorageUri</span></span>
```
Backup-AzKeyVault -StorageContainerUri <Uri> -SasToken <SecureString> -HsmObject <PSManagedHsm>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="081ed-108">InputObjectStorageName</span><span class="sxs-lookup"><span data-stu-id="081ed-108">InputObjectStorageName</span></span>
```
Backup-AzKeyVault -StorageAccountName <String> -StorageContainerName <String> -SasToken <SecureString>
 -HsmObject <PSManagedHsm> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="081ed-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="081ed-109">DESCRIPTION</span></span>
<span data-ttu-id="081ed-110">Eseguire il backup completo di un HSM gestito in un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="081ed-110">Fully backup a managed HSM to a storage account.</span></span>
<span data-ttu-id="081ed-111">Usare `Restore-AzKeyVault` per ripristinare il backup.</span><span class="sxs-lookup"><span data-stu-id="081ed-111">Use `Restore-AzKeyVault` to restore the backup.</span></span>

## <span data-ttu-id="081ed-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="081ed-112">EXAMPLES</span></span>

### <span data-ttu-id="081ed-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="081ed-113">Example 1</span></span>
```powershell
PS C:\> $sasToken = ConvertTo-SecureString -AsPlainText -Force "?sv=2019-12-12&ss=bfqt&srt=sco&sp=rwdlacupx&se=2020-10-12T14:42:19Z&st=2020-10-12T06:42:19Z&spr=https&sig=******"

PS C:\> Backup-AzKeyVault -HsmName myHsm -StorageContainerUri "https://{accountName}.blob.core.windows.net/{containerName}" -SasToken $sasToken

https://{accountName}.blob.core.windows.net/{containerName}/{backupFolder}
```

<span data-ttu-id="081ed-114">Il cmdlet crea una cartella (in genere denominata ) nel contenitore di archiviazione, archivia il backup in tale cartella e restituisce `mhsm-{name}-{timestamp}` l'URI della cartella.</span><span class="sxs-lookup"><span data-stu-id="081ed-114">The cmdlet will create a folder (typically named `mhsm-{name}-{timestamp}`) in the storage container, store the backup in that folder and output the folder URI.</span></span>

## <span data-ttu-id="081ed-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="081ed-115">PARAMETERS</span></span>

### <span data-ttu-id="081ed-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="081ed-116">-DefaultProfile</span></span>
<span data-ttu-id="081ed-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="081ed-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="081ed-118">-HsmName</span><span class="sxs-lookup"><span data-stu-id="081ed-118">-HsmName</span></span>
<span data-ttu-id="081ed-119">Nome dell'HSM.</span><span class="sxs-lookup"><span data-stu-id="081ed-119">Name of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveStorageName, InteractiveStorageUri
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="081ed-120">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="081ed-120">-HsmObject</span></span>
<span data-ttu-id="081ed-121">Oggetto HSM gestito</span><span class="sxs-lookup"><span data-stu-id="081ed-121">Managed HSM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: InputObjectStorageUri, InputObjectStorageName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="081ed-122">-SasToken</span><span class="sxs-lookup"><span data-stu-id="081ed-122">-SasToken</span></span>
<span data-ttu-id="081ed-123">Token della firma di accesso condiviso per autenticare l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="081ed-123">The shared access signature (SAS) token to authenticate the storage account.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="081ed-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="081ed-124">-StorageAccountName</span></span>
<span data-ttu-id="081ed-125">Nome dell'account di archiviazione in cui verrà archiviato il backup.</span><span class="sxs-lookup"><span data-stu-id="081ed-125">Name of the storage account where the backup is going to be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveStorageName, InputObjectStorageName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="081ed-126">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="081ed-126">-StorageContainerName</span></span>
<span data-ttu-id="081ed-127">Nome del contenitore BLOB in cui verrà archiviato il backup.</span><span class="sxs-lookup"><span data-stu-id="081ed-127">Name of the blob container where the backup is going to be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveStorageName, InputObjectStorageName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="081ed-128">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="081ed-128">-StorageContainerUri</span></span>
<span data-ttu-id="081ed-129">URI del contenitore di archiviazione in cui verrà archiviato il backup.</span><span class="sxs-lookup"><span data-stu-id="081ed-129">URI of the storage container where the backup is going to be stored.</span></span>

```yaml
Type: System.Uri
Parameter Sets: InteractiveStorageUri, InputObjectStorageUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="081ed-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="081ed-130">-Confirm</span></span>
<span data-ttu-id="081ed-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="081ed-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="081ed-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="081ed-132">-WhatIf</span></span>
<span data-ttu-id="081ed-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="081ed-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="081ed-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="081ed-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="081ed-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="081ed-135">CommonParameters</span></span>
<span data-ttu-id="081ed-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="081ed-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="081ed-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="081ed-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="081ed-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="081ed-138">INPUTS</span></span>

### <span data-ttu-id="081ed-139">Nessuno</span><span class="sxs-lookup"><span data-stu-id="081ed-139">None</span></span>

## <span data-ttu-id="081ed-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="081ed-140">OUTPUTS</span></span>

### <span data-ttu-id="081ed-141">System.String</span><span class="sxs-lookup"><span data-stu-id="081ed-141">System.String</span></span>

## <span data-ttu-id="081ed-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="081ed-142">NOTES</span></span>

## <span data-ttu-id="081ed-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="081ed-143">RELATED LINKS</span></span>
