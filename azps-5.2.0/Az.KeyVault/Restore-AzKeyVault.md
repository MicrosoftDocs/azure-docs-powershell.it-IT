---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVault.md
ms.openlocfilehash: 8be76f6eb5cf56e5f4612a175c067a7647576a4c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354940"
---
# <span data-ttu-id="a5e9e-101">Restore-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="a5e9e-101">Restore-AzKeyVault</span></span>

## <span data-ttu-id="a5e9e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a5e9e-102">SYNOPSIS</span></span>
<span data-ttu-id="a5e9e-103">Ripristina completamente un HSM gestito da backup.</span><span class="sxs-lookup"><span data-stu-id="a5e9e-103">Fully restores a managed HSM from backup.</span></span>

## <span data-ttu-id="a5e9e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a5e9e-104">SYNTAX</span></span>

### <span data-ttu-id="a5e9e-105">InteractiveStorageName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a5e9e-105">InteractiveStorageName (Default)</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-PassThru] [-HsmName] <String> -StorageAccountName <String>
 -StorageContainerName <String> -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5e9e-106">InteractiveStorageUri</span><span class="sxs-lookup"><span data-stu-id="a5e9e-106">InteractiveStorageUri</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-PassThru] [-HsmName] <String> -StorageContainerUri <Uri>
 -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5e9e-107">InputObjectStorageUri</span><span class="sxs-lookup"><span data-stu-id="a5e9e-107">InputObjectStorageUri</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-PassThru] -StorageContainerUri <Uri> -SasToken <SecureString>
 -HsmObject <PSManagedHsm> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5e9e-108">InputObjectStorageName</span><span class="sxs-lookup"><span data-stu-id="a5e9e-108">InputObjectStorageName</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-PassThru] -StorageAccountName <String>
 -StorageContainerName <String> -SasToken <SecureString> -HsmObject <PSManagedHsm>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5e9e-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a5e9e-109">DESCRIPTION</span></span>
<span data-ttu-id="a5e9e-110">Ripristina completamente un HSM gestito da un backup archiviato in un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a5e9e-110">Fully restores a managed HSM from a backup stored in a storage account.</span></span>
<span data-ttu-id="a5e9e-111">Usare `Backup-AzKeyVault` per eseguire il backup.</span><span class="sxs-lookup"><span data-stu-id="a5e9e-111">Use `Backup-AzKeyVault` to backup.</span></span>

## <span data-ttu-id="a5e9e-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a5e9e-112">EXAMPLES</span></span>

### <span data-ttu-id="a5e9e-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a5e9e-113">Example 1</span></span>
```powershell
PS C:\> $sasToken = ConvertTo-SecureString -AsPlainText -Force "?sv=2019-12-12&ss=bfqt&srt=sco&sp=rwdlacupx&se=2020-10-12T14:42:19Z&st=2020-10-12T06:42:19Z&spr=https&sig=******"
PS C:\> Restore-AzKeyVault -HsmName myHsm -StorageContainerUri "https://{accountName}.blob.core.windows.net/{containerName}" -BackupFolder "mhsm-myHsm-2020101308504935" -SasToken $sasToken
```

<span data-ttu-id="a5e9e-114">Nell'esempio viene ripristinato un backup archiviato in una cartella denominata "mhsm-myHsm-2020101308504935" di un contenitore di archiviazione "https://{AccountName}. blob. Core. Windows. NET/{ContainerName}".</span><span class="sxs-lookup"><span data-stu-id="a5e9e-114">The example restores a backup stored in a folder named "mhsm-myHsm-2020101308504935" of a storage container "https://{accountName}.blob.core.windows.net/{containerName}".</span></span>

## <span data-ttu-id="a5e9e-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a5e9e-115">PARAMETERS</span></span>

### <span data-ttu-id="a5e9e-116">-BackupFolder</span><span class="sxs-lookup"><span data-stu-id="a5e9e-116">-BackupFolder</span></span>
<span data-ttu-id="a5e9e-117">Nome cartella del backup, ad esempio "mhsm-*-2020101309020403". Può anche essere annidato, ad esempio "backups/mhsm-*-2020101309020403".</span><span class="sxs-lookup"><span data-stu-id="a5e9e-117">Folder name of the backup, e.g. 'mhsm-*-2020101309020403'. It can also be nested such as 'backups/mhsm-*-2020101309020403'.</span></span>

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

### <span data-ttu-id="a5e9e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5e9e-118">-DefaultProfile</span></span>
<span data-ttu-id="a5e9e-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a5e9e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5e9e-120">-HsmName</span><span class="sxs-lookup"><span data-stu-id="a5e9e-120">-HsmName</span></span>
<span data-ttu-id="a5e9e-121">Nome dell'HSM.</span><span class="sxs-lookup"><span data-stu-id="a5e9e-121">Name of the HSM.</span></span>

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

### <span data-ttu-id="a5e9e-122">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="a5e9e-122">-HsmObject</span></span>
<span data-ttu-id="a5e9e-123">Oggetto HSM gestito</span><span class="sxs-lookup"><span data-stu-id="a5e9e-123">Managed HSM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: InputObjectStorageUri, InputObjectStorageName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5e9e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5e9e-124">-PassThru</span></span>
<span data-ttu-id="a5e9e-125">Restituisce vero quando l'HSM viene ripristinato.</span><span class="sxs-lookup"><span data-stu-id="a5e9e-125">Return true when the HSM is restored.</span></span>

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

### <span data-ttu-id="a5e9e-126">-SasToken</span><span class="sxs-lookup"><span data-stu-id="a5e9e-126">-SasToken</span></span>
<span data-ttu-id="a5e9e-127">Token SAS (Shared Access Signature) per autenticare l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a5e9e-127">The shared access signature (SAS) token to authenticate the storage account.</span></span>

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

### <span data-ttu-id="a5e9e-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a5e9e-128">-StorageAccountName</span></span>
<span data-ttu-id="a5e9e-129">Nome dell'account di archiviazione in cui verrà archiviato il backup.</span><span class="sxs-lookup"><span data-stu-id="a5e9e-129">Name of the storage account where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="a5e9e-130">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="a5e9e-130">-StorageContainerName</span></span>
<span data-ttu-id="a5e9e-131">Nome del contenitore di BLOB in cui verrà archiviato il backup.</span><span class="sxs-lookup"><span data-stu-id="a5e9e-131">Name of the blob container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="a5e9e-132">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="a5e9e-132">-StorageContainerUri</span></span>
<span data-ttu-id="a5e9e-133">URI del contenitore di archiviazione in cui verrà archiviato il backup.</span><span class="sxs-lookup"><span data-stu-id="a5e9e-133">URI of the storage container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="a5e9e-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a5e9e-134">-Confirm</span></span>
<span data-ttu-id="a5e9e-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5e9e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5e9e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5e9e-136">-WhatIf</span></span>
<span data-ttu-id="a5e9e-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a5e9e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5e9e-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a5e9e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5e9e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5e9e-139">CommonParameters</span></span>
<span data-ttu-id="a5e9e-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5e9e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5e9e-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5e9e-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5e9e-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a5e9e-142">INPUTS</span></span>

### <span data-ttu-id="a5e9e-143">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a5e9e-143">None</span></span>

## <span data-ttu-id="a5e9e-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a5e9e-144">OUTPUTS</span></span>

### <span data-ttu-id="a5e9e-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a5e9e-145">System.Boolean</span></span>

## <span data-ttu-id="a5e9e-146">Note</span><span class="sxs-lookup"><span data-stu-id="a5e9e-146">NOTES</span></span>

## <span data-ttu-id="a5e9e-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a5e9e-147">RELATED LINKS</span></span>
