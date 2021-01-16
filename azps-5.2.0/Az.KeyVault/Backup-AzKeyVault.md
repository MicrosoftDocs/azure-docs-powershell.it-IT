---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVault.md
ms.openlocfilehash: 7e5aa5091376b8c80d71bdeb2bbad7bd8d22c3a2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357220"
---
# <span data-ttu-id="95409-101">Backup-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="95409-101">Backup-AzKeyVault</span></span>

## <span data-ttu-id="95409-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="95409-102">SYNOPSIS</span></span>
<span data-ttu-id="95409-103">Eseguire il backup completo di un HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="95409-103">Fully backup a managed HSM.</span></span>

## <span data-ttu-id="95409-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="95409-104">SYNTAX</span></span>

### <span data-ttu-id="95409-105">InteractiveStorageName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="95409-105">InteractiveStorageName (Default)</span></span>
```
Backup-AzKeyVault [-HsmName] <String> -StorageAccountName <String> -StorageContainerName <String>
 -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95409-106">InteractiveStorageUri</span><span class="sxs-lookup"><span data-stu-id="95409-106">InteractiveStorageUri</span></span>
```
Backup-AzKeyVault [-HsmName] <String> -StorageContainerUri <Uri> -SasToken <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95409-107">InputObjectStorageUri</span><span class="sxs-lookup"><span data-stu-id="95409-107">InputObjectStorageUri</span></span>
```
Backup-AzKeyVault -StorageContainerUri <Uri> -SasToken <SecureString> -HsmObject <PSManagedHsm>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95409-108">InputObjectStorageName</span><span class="sxs-lookup"><span data-stu-id="95409-108">InputObjectStorageName</span></span>
```
Backup-AzKeyVault -StorageAccountName <String> -StorageContainerName <String> -SasToken <SecureString>
 -HsmObject <PSManagedHsm> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95409-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="95409-109">DESCRIPTION</span></span>
<span data-ttu-id="95409-110">Eseguire il backup completo di un HSM gestito in un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="95409-110">Fully backup a managed HSM to a storage account.</span></span>
<span data-ttu-id="95409-111">Consente `Restore-AzKeyVault` di ripristinare il backup.</span><span class="sxs-lookup"><span data-stu-id="95409-111">Use `Restore-AzKeyVault` to restore the backup.</span></span>

## <span data-ttu-id="95409-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="95409-112">EXAMPLES</span></span>

### <span data-ttu-id="95409-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="95409-113">Example 1</span></span>
```powershell
PS C:\> $sasToken = ConvertTo-SecureString -AsPlainText -Force "?sv=2019-12-12&ss=bfqt&srt=sco&sp=rwdlacupx&se=2020-10-12T14:42:19Z&st=2020-10-12T06:42:19Z&spr=https&sig=******"

PS C:\> Backup-AzKeyVault -HsmName myHsm -StorageContainerUri "https://{accountName}.blob.core.windows.net/{containerName}" -SasToken $sasToken

https://{accountName}.blob.core.windows.net/{containerName}/{backupFolder}
```

<span data-ttu-id="95409-114">Il cmdlet creerà una cartella (in genere denominata `mhsm-{name}-{timestamp}` ) nel contenitore di archiviazione, archivierà il backup nella cartella e restituirà l'URI della cartella.</span><span class="sxs-lookup"><span data-stu-id="95409-114">The cmdlet will create a folder (typically named `mhsm-{name}-{timestamp}`) in the storage container, store the backup in that folder and output the folder URI.</span></span>

## <span data-ttu-id="95409-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="95409-115">PARAMETERS</span></span>

### <span data-ttu-id="95409-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95409-116">-DefaultProfile</span></span>
<span data-ttu-id="95409-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="95409-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95409-118">-HsmName</span><span class="sxs-lookup"><span data-stu-id="95409-118">-HsmName</span></span>
<span data-ttu-id="95409-119">Nome dell'HSM.</span><span class="sxs-lookup"><span data-stu-id="95409-119">Name of the HSM.</span></span>

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

### <span data-ttu-id="95409-120">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="95409-120">-HsmObject</span></span>
<span data-ttu-id="95409-121">Oggetto HSM gestito</span><span class="sxs-lookup"><span data-stu-id="95409-121">Managed HSM object</span></span>

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

### <span data-ttu-id="95409-122">-SasToken</span><span class="sxs-lookup"><span data-stu-id="95409-122">-SasToken</span></span>
<span data-ttu-id="95409-123">Token SAS (Shared Access Signature) per autenticare l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="95409-123">The shared access signature (SAS) token to authenticate the storage account.</span></span>

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

### <span data-ttu-id="95409-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="95409-124">-StorageAccountName</span></span>
<span data-ttu-id="95409-125">Nome dell'account di archiviazione in cui verrà archiviato il backup.</span><span class="sxs-lookup"><span data-stu-id="95409-125">Name of the storage account where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="95409-126">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="95409-126">-StorageContainerName</span></span>
<span data-ttu-id="95409-127">Nome del contenitore di BLOB in cui verrà archiviato il backup.</span><span class="sxs-lookup"><span data-stu-id="95409-127">Name of the blob container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="95409-128">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="95409-128">-StorageContainerUri</span></span>
<span data-ttu-id="95409-129">URI del contenitore di archiviazione in cui verrà archiviato il backup.</span><span class="sxs-lookup"><span data-stu-id="95409-129">URI of the storage container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="95409-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="95409-130">-Confirm</span></span>
<span data-ttu-id="95409-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95409-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95409-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95409-132">-WhatIf</span></span>
<span data-ttu-id="95409-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="95409-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95409-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="95409-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95409-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95409-135">CommonParameters</span></span>
<span data-ttu-id="95409-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95409-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95409-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="95409-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95409-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="95409-138">INPUTS</span></span>

### <span data-ttu-id="95409-139">Nessuno</span><span class="sxs-lookup"><span data-stu-id="95409-139">None</span></span>

## <span data-ttu-id="95409-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="95409-140">OUTPUTS</span></span>

### <span data-ttu-id="95409-141">System. String</span><span class="sxs-lookup"><span data-stu-id="95409-141">System.String</span></span>

## <span data-ttu-id="95409-142">Note</span><span class="sxs-lookup"><span data-stu-id="95409-142">NOTES</span></span>

## <span data-ttu-id="95409-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="95409-143">RELATED LINKS</span></span>
