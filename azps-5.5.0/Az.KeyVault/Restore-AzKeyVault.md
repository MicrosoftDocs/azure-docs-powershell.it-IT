---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVault.md
ms.openlocfilehash: d1cf3757596a56336c25c46bd6c4e38687888d6e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209282"
---
# <span data-ttu-id="3cac4-101">Restore-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="3cac4-101">Restore-AzKeyVault</span></span>

## <span data-ttu-id="3cac4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cac4-102">SYNOPSIS</span></span>
<span data-ttu-id="3cac4-103">Ripristina completamente un HSM gestito dal backup.</span><span class="sxs-lookup"><span data-stu-id="3cac4-103">Fully restores a managed HSM from backup.</span></span>

## <span data-ttu-id="3cac4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3cac4-104">SYNTAX</span></span>

### <span data-ttu-id="3cac4-105">InteractiveStorageName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3cac4-105">InteractiveStorageName (Default)</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] [-HsmName] <String>
 -StorageAccountName <String> -StorageContainerName <String> -SasToken <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cac4-106">InteractiveStorageUri</span><span class="sxs-lookup"><span data-stu-id="3cac4-106">InteractiveStorageUri</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] [-HsmName] <String>
 -StorageContainerUri <Uri> -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cac4-107">InputObjectStorageUri</span><span class="sxs-lookup"><span data-stu-id="3cac4-107">InputObjectStorageUri</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] -StorageContainerUri <Uri>
 -SasToken <SecureString> -HsmObject <PSManagedHsm> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cac4-108">InputObjectStorageName</span><span class="sxs-lookup"><span data-stu-id="3cac4-108">InputObjectStorageName</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] -StorageAccountName <String>
 -StorageContainerName <String> -SasToken <SecureString> -HsmObject <PSManagedHsm>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cac4-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3cac4-109">DESCRIPTION</span></span>
<span data-ttu-id="3cac4-110">Ripristina completamente un HSM gestito da un backup archiviato in un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3cac4-110">Fully restores a managed HSM from a backup stored in a storage account.</span></span>
<span data-ttu-id="3cac4-111">Da `Backup-AzKeyVault` usare per il backup.</span><span class="sxs-lookup"><span data-stu-id="3cac4-111">Use `Backup-AzKeyVault` to backup.</span></span>

## <span data-ttu-id="3cac4-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3cac4-112">EXAMPLES</span></span>

### <span data-ttu-id="3cac4-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3cac4-113">Example 1</span></span>
```powershell
PS C:\> $sasToken = ConvertTo-SecureString -AsPlainText -Force "?sv=2019-12-12&ss=bfqt&srt=sco&sp=rwdlacupx&se=2020-10-12T14:42:19Z&st=2020-10-12T06:42:19Z&spr=https&sig=******"
PS C:\> Restore-AzKeyVault -HsmName myHsm -StorageContainerUri "https://{accountName}.blob.core.windows.net/{containerName}" -BackupFolder "mhsm-myHsm-2020101308504935" -SasToken $sasToken
```

<span data-ttu-id="3cac4-114">L'esempio ripristina un backup archiviato in una cartella denominata "mhsm-myHsm-2020101308504935" di un contenitore di archiviazione "https://{accountName}.blob.core.windows.net/{containerName}".</span><span class="sxs-lookup"><span data-stu-id="3cac4-114">The example restores a backup stored in a folder named "mhsm-myHsm-2020101308504935" of a storage container "https://{accountName}.blob.core.windows.net/{containerName}".</span></span>

## <span data-ttu-id="3cac4-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3cac4-115">PARAMETERS</span></span>

### <span data-ttu-id="3cac4-116">-BackupFolder</span><span class="sxs-lookup"><span data-stu-id="3cac4-116">-BackupFolder</span></span>
<span data-ttu-id="3cac4-117">Nome della cartella del backup, ad esempio "mhsm-*-2020101309020403". Può anche essere annidata, ad esempio "backup/mhsm-*-2020101309020403".</span><span class="sxs-lookup"><span data-stu-id="3cac4-117">Folder name of the backup, e.g. 'mhsm-*-2020101309020403'. It can also be nested such as 'backups/mhsm-*-2020101309020403'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cac4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cac4-118">-DefaultProfile</span></span>
<span data-ttu-id="3cac4-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3cac4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cac4-120">-HsmName</span><span class="sxs-lookup"><span data-stu-id="3cac4-120">-HsmName</span></span>
<span data-ttu-id="3cac4-121">Nome dell'HSM.</span><span class="sxs-lookup"><span data-stu-id="3cac4-121">Name of the HSM.</span></span>

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

### <span data-ttu-id="3cac4-122">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="3cac4-122">-HsmObject</span></span>
<span data-ttu-id="3cac4-123">Oggetto HSM gestito</span><span class="sxs-lookup"><span data-stu-id="3cac4-123">Managed HSM object</span></span>

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

### <span data-ttu-id="3cac4-124">-KeyName</span><span class="sxs-lookup"><span data-stu-id="3cac4-124">-KeyName</span></span>
<span data-ttu-id="3cac4-125">Nome della chiave da ripristinare.</span><span class="sxs-lookup"><span data-stu-id="3cac4-125">Key name to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cac4-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3cac4-126">-PassThru</span></span>
<span data-ttu-id="3cac4-127">Restituisce true quando il servizio HSM viene ripristinato.</span><span class="sxs-lookup"><span data-stu-id="3cac4-127">Return true when the HSM is restored.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cac4-128">-SasToken</span><span class="sxs-lookup"><span data-stu-id="3cac4-128">-SasToken</span></span>
<span data-ttu-id="3cac4-129">Token della firma di accesso condiviso per autenticare l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3cac4-129">The shared access signature (SAS) token to authenticate the storage account.</span></span>

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

### <span data-ttu-id="3cac4-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3cac4-130">-StorageAccountName</span></span>
<span data-ttu-id="3cac4-131">Nome dell'account di archiviazione in cui verrà archiviato il backup.</span><span class="sxs-lookup"><span data-stu-id="3cac4-131">Name of the storage account where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="3cac4-132">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="3cac4-132">-StorageContainerName</span></span>
<span data-ttu-id="3cac4-133">Nome del contenitore BLOB in cui verrà archiviato il backup.</span><span class="sxs-lookup"><span data-stu-id="3cac4-133">Name of the blob container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="3cac4-134">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="3cac4-134">-StorageContainerUri</span></span>
<span data-ttu-id="3cac4-135">URI del contenitore di archiviazione in cui verrà archiviato il backup.</span><span class="sxs-lookup"><span data-stu-id="3cac4-135">URI of the storage container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="3cac4-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3cac4-136">-Confirm</span></span>
<span data-ttu-id="3cac4-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cac4-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cac4-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cac4-138">-WhatIf</span></span>
<span data-ttu-id="3cac4-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3cac4-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cac4-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3cac4-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cac4-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cac4-141">CommonParameters</span></span>
<span data-ttu-id="3cac4-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cac4-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cac4-143">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3cac4-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cac4-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="3cac4-144">INPUTS</span></span>

### <span data-ttu-id="3cac4-145">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3cac4-145">None</span></span>

## <span data-ttu-id="3cac4-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3cac4-146">OUTPUTS</span></span>

### <span data-ttu-id="3cac4-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3cac4-147">System.Boolean</span></span>

## <span data-ttu-id="3cac4-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="3cac4-148">NOTES</span></span>

## <span data-ttu-id="3cac4-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3cac4-149">RELATED LINKS</span></span>
