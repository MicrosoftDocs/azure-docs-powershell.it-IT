---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsm.md
ms.openlocfilehash: 97e5c836d7d6b209d31851264047c6df894d77a7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203668"
---
# <span data-ttu-id="85216-101">Restore-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="85216-101">Restore-AzManagedHsm</span></span>

## <span data-ttu-id="85216-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="85216-102">SYNOPSIS</span></span>
<span data-ttu-id="85216-103">Ripristina completamente un HSM gestito da backup.</span><span class="sxs-lookup"><span data-stu-id="85216-103">Fully restores a managed HSM from backup.</span></span>

## <span data-ttu-id="85216-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="85216-104">SYNTAX</span></span>

### <span data-ttu-id="85216-105">InteractiveStorageName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="85216-105">InteractiveStorageName (Default)</span></span>
```
Restore-AzManagedHsm -BackupFolder <String> [-PassThru] [-Name] <String> -StorageAccountName <String>
 -StorageContainerName <String> -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85216-106">InteractiveStorageUri</span><span class="sxs-lookup"><span data-stu-id="85216-106">InteractiveStorageUri</span></span>
```
Restore-AzManagedHsm -BackupFolder <String> [-PassThru] [-Name] <String> -StorageContainerUri <Uri>
 -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85216-107">InputObjectStorageUri</span><span class="sxs-lookup"><span data-stu-id="85216-107">InputObjectStorageUri</span></span>
```
Restore-AzManagedHsm -BackupFolder <String> [-PassThru] -StorageContainerUri <Uri> -SasToken <SecureString>
 -HsmObject <PSManagedHsm> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85216-108">InputObjectStorageName</span><span class="sxs-lookup"><span data-stu-id="85216-108">InputObjectStorageName</span></span>
```
Restore-AzManagedHsm -BackupFolder <String> [-PassThru] -StorageAccountName <String>
 -StorageContainerName <String> -SasToken <SecureString> -HsmObject <PSManagedHsm>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85216-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85216-109">DESCRIPTION</span></span>
<span data-ttu-id="85216-110">Ripristina completamente un HSM gestito da un backup archiviato in un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="85216-110">Fully restores a managed HSM from a backup stored in a storage account.</span></span>
<span data-ttu-id="85216-111">Usare `Backup-AzManagedHsm` per eseguire il backup.</span><span class="sxs-lookup"><span data-stu-id="85216-111">Use `Backup-AzManagedHsm` to backup.</span></span>

## <span data-ttu-id="85216-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="85216-112">EXAMPLES</span></span>

### <span data-ttu-id="85216-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="85216-113">Example 1</span></span>
```powershell
PS C:\> $sasToken = ConvertTo-SecureString -AsPlainText -Force "?sv=2019-12-12&ss=bfqt&srt=sco&sp=rwdlacupx&se=2020-10-12T14:42:19Z&st=2020-10-12T06:42:19Z&spr=https&sig=******"
PS C:\> Restore-AzManagedHsm -Name myHsm -StorageContainerUri "https://{accountName}.blob.core.windows.net/{containerName}" -BackupFolder "mhsm-myHsm-2020101308504935" -SasToken $sasToken
```

<span data-ttu-id="85216-114">Nell'esempio viene ripristinato un backup archiviato in una cartella denominata "mhsm-myHsm-2020101308504935" di un contenitore di archiviazione "https://{AccountName}. blob. Core. Windows. NET/{ContainerName}".</span><span class="sxs-lookup"><span data-stu-id="85216-114">The example restores a backup stored in a folder named "mhsm-myHsm-2020101308504935" of a storage container "https://{accountName}.blob.core.windows.net/{containerName}".</span></span>

## <span data-ttu-id="85216-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="85216-115">PARAMETERS</span></span>

### <span data-ttu-id="85216-116">-BackupFolder</span><span class="sxs-lookup"><span data-stu-id="85216-116">-BackupFolder</span></span>
<span data-ttu-id="85216-117">Nome cartella del backup, ad esempio "mhsm- *-2020101309020403". Può anche essere annidato, ad esempio "backups/mhsm-* -2020101309020403".</span><span class="sxs-lookup"><span data-stu-id="85216-117">Folder name of the backup, e.g. 'mhsm- *-2020101309020403'. It can also be nested such as 'backups/mhsm-* -2020101309020403'.</span></span>

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

### <span data-ttu-id="85216-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85216-118">-DefaultProfile</span></span>
<span data-ttu-id="85216-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="85216-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85216-120">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="85216-120">-HsmObject</span></span>
<span data-ttu-id="85216-121">Oggetto HSM gestito</span><span class="sxs-lookup"><span data-stu-id="85216-121">Managed HSM object</span></span>

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

### <span data-ttu-id="85216-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="85216-122">-Name</span></span>
<span data-ttu-id="85216-123">Nome dell'HSM.</span><span class="sxs-lookup"><span data-stu-id="85216-123">Name of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveStorageName, InteractiveStorageUri
Aliases: HsmName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85216-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85216-124">-PassThru</span></span>
<span data-ttu-id="85216-125">Restituisce vero quando l'HSM viene ripristinato.</span><span class="sxs-lookup"><span data-stu-id="85216-125">Return true when the HSM is restored.</span></span>

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

### <span data-ttu-id="85216-126">-SasToken</span><span class="sxs-lookup"><span data-stu-id="85216-126">-SasToken</span></span>
<span data-ttu-id="85216-127">Token SAS (Shared Access Signature) per autenticare l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="85216-127">The shared access signature (SAS) token to authenticate the storage account.</span></span>

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

### <span data-ttu-id="85216-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="85216-128">-StorageAccountName</span></span>
<span data-ttu-id="85216-129">Nome dell'account di archiviazione in cui verrà archiviato il backup.</span><span class="sxs-lookup"><span data-stu-id="85216-129">Name of the storage account where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="85216-130">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="85216-130">-StorageContainerName</span></span>
<span data-ttu-id="85216-131">Nome del contenitore di BLOB in cui verrà archiviato il backup.</span><span class="sxs-lookup"><span data-stu-id="85216-131">Name of the blob container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="85216-132">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="85216-132">-StorageContainerUri</span></span>
<span data-ttu-id="85216-133">URI del contenitore di archiviazione in cui verrà archiviato il backup.</span><span class="sxs-lookup"><span data-stu-id="85216-133">URI of the storage container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="85216-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="85216-134">-Confirm</span></span>
<span data-ttu-id="85216-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85216-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85216-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85216-136">-WhatIf</span></span>
<span data-ttu-id="85216-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="85216-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85216-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="85216-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85216-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85216-139">CommonParameters</span></span>
<span data-ttu-id="85216-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85216-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85216-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85216-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85216-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="85216-142">INPUTS</span></span>

### <span data-ttu-id="85216-143">Nessuno</span><span class="sxs-lookup"><span data-stu-id="85216-143">None</span></span>

## <span data-ttu-id="85216-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="85216-144">OUTPUTS</span></span>

### <span data-ttu-id="85216-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="85216-145">System.Boolean</span></span>

## <span data-ttu-id="85216-146">Note</span><span class="sxs-lookup"><span data-stu-id="85216-146">NOTES</span></span>

## <span data-ttu-id="85216-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="85216-147">RELATED LINKS</span></span>
