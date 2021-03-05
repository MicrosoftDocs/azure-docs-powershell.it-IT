---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/backup-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 75f5e487c7cb1d434d12d6c02122991195c01066
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991142"
---
# <span data-ttu-id="2040c-101">Backup-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2040c-101">Backup-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="2040c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2040c-102">SYNOPSIS</span></span>
<span data-ttu-id="2040c-103">Backup di un account di archiviazione gestito da KeyVault.</span><span class="sxs-lookup"><span data-stu-id="2040c-103">Backs up a KeyVault-managed storage account.</span></span>

## <span data-ttu-id="2040c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2040c-104">SYNTAX</span></span>

### <span data-ttu-id="2040c-105">ByStorageAccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2040c-105">ByStorageAccountName (Default)</span></span>
```
Backup-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2040c-106">ByStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2040c-106">ByStorageAccount</span></span>
```
Backup-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-OutputFile] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2040c-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2040c-107">DESCRIPTION</span></span>
<span data-ttu-id="2040c-108">Il cmdlet **Backup-AzKeyVaultManagedStorageAccount** consente di eseguire il backup di un account di archiviazione gestito specificato in un vault delle chiavi scaricarlo e archiviarlo in un file.</span><span class="sxs-lookup"><span data-stu-id="2040c-108">The **Backup-AzKeyVaultManagedStorageAccount** cmdlet backs up a specified managed storage account in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="2040c-109">Poiché il contenuto scaricato è crittografato, non può essere usato all'esterno del Vault delle chiavi di Azure.</span><span class="sxs-lookup"><span data-stu-id="2040c-109">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="2040c-110">È possibile ripristinare un account di archiviazione di cui è stato eseguito il backup in qualsiasi vault chiave nell'abbonamento da cui è stato eseguito il backup, purché il vault si trova nella stessa area geografica di Azure.</span><span class="sxs-lookup"><span data-stu-id="2040c-110">You can restore a backed-up storage account to any key vault in the subscription that it was backed up from, as long as the vault is in the same Azure geography.</span></span>
<span data-ttu-id="2040c-111">I motivi tipici per usare questo cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="2040c-111">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="2040c-112">Si vuole conservare una copia offline dell'account di archiviazione nel caso in cui si elimini accidentalmente l'originale dal Vault.</span><span class="sxs-lookup"><span data-stu-id="2040c-112">You want to retain an offline copy of the storage account in case you accidentally delete the original from the vault.</span></span>
 
- <span data-ttu-id="2040c-113">È stato creato un account di archiviazione gestito con il Vault delle chiavi e ora si vuole clonare l'oggetto in un'area di Azure diversa, in modo da poterlo usare da tutte le istanze dell'applicazione distribuita.</span><span class="sxs-lookup"><span data-stu-id="2040c-113">You created a managed storage account using Key Vault and now want to clone the object into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="2040c-114">Usare il cmdlet **Backup-AzKeyVaultManagedStorageAccount** per recuperare l'account di archiviazione gestito in formato crittografato e quindi usare il cmdlet **Restore-AzKeyVaultManagedStorageAccount** e specificare un vault delle chiavi nella seconda area geografica.</span><span class="sxs-lookup"><span data-stu-id="2040c-114">Use the **Backup-AzKeyVaultManagedStorageAccount** cmdlet to retrieve the managed storage account in encrypted format and then use the **Restore-AzKeyVaultManagedStorageAccount** cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="2040c-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2040c-115">EXAMPLES</span></span>

### <span data-ttu-id="2040c-116">Esempio 1: Eseguire il backup di un account di archiviazione gestito con un nome file generato automaticamente</span><span class="sxs-lookup"><span data-stu-id="2040c-116">Example 1: Back up a managed storage account with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'

C:\Users\username\mykeyvault-mymsak-1527029447.01191
```

<span data-ttu-id="2040c-117">Questo comando recupera l'account di archiviazione gestito denominato MyMSAK dalla chiave vault denominata MyKeyVault e salva una copia di backup dell'account di archiviazione gestito in un file denominato automaticamente e visualizza il nome del file.</span><span class="sxs-lookup"><span data-stu-id="2040c-117">This command retrieves the managed storage account named MyMSAK from the key vault named MyKeyVault and saves a backup of that managed storage account to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="2040c-118">Esempio 2: Eseguire il backup di un account di archiviazione gestito con un nome file specificato</span><span class="sxs-lookup"><span data-stu-id="2040c-118">Example 2: Back up a managed storage account to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyMSAK' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="2040c-119">Questo comando recupera l'account di archiviazione gestito denominato MyMSAK dalla chiave vault denominata MyKeyVault e salva un backup dell'account di archiviazione gestito in un file denominato Backup.BLOB.</span><span class="sxs-lookup"><span data-stu-id="2040c-119">This command retrieves the managed storage account named MyMSAK from the key vault named MyKeyVault and saves a backup of that managed storage account to a file named Backup.blob.</span></span>

### <span data-ttu-id="2040c-120">Esempio 3: Eseguire il backup di un account di archiviazione gestito recuperato in precedenza con un nome file specificato, sovrascrivendo il file di destinazione senza chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="2040c-120">Example 3: Back up a previously retrieved managed storage account to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $msak = Get-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'
PS C:\> Backup-AzKeyVaultManagedStorageAccount -StorageAccount $msak -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="2040c-121">Questo comando crea un backup dell'account di archiviazione gestito denominato $msak. Nome nel vault denominato $msak. VaultName in un file denominato Backup.BLOB, sovrascrivendo automaticamente il file, se esiste già.</span><span class="sxs-lookup"><span data-stu-id="2040c-121">This command creates a backup of the managed storage account named $msak.Name in the vault named $msak.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="2040c-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2040c-122">PARAMETERS</span></span>

### <span data-ttu-id="2040c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2040c-123">-DefaultProfile</span></span>
<span data-ttu-id="2040c-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2040c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2040c-125">-Force</span><span class="sxs-lookup"><span data-stu-id="2040c-125">-Force</span></span>
<span data-ttu-id="2040c-126">Sovrascrivere il file specificato, se esistente</span><span class="sxs-lookup"><span data-stu-id="2040c-126">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="2040c-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2040c-127">-InputObject</span></span>
<span data-ttu-id="2040c-128">Bundle di account di archiviazione di cui eseguire il backup, pipelined in seguito all'output di una chiamata di recupero.</span><span class="sxs-lookup"><span data-stu-id="2040c-128">Storage account bundle to be backed up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByStorageAccount
Aliases: StorageAccount

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2040c-129">-Name</span><span class="sxs-lookup"><span data-stu-id="2040c-129">-Name</span></span>
<span data-ttu-id="2040c-130">Nome segreto.</span><span class="sxs-lookup"><span data-stu-id="2040c-130">Secret name.</span></span>
<span data-ttu-id="2040c-131">Il cmdlet crea l'FQDN di un segreto dal nome del vault, l'ambiente attualmente selezionato e il nome del segreto.</span><span class="sxs-lookup"><span data-stu-id="2040c-131">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByStorageAccountName
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2040c-132">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="2040c-132">-OutputFile</span></span>
<span data-ttu-id="2040c-133">File di output.</span><span class="sxs-lookup"><span data-stu-id="2040c-133">Output file.</span></span>
<span data-ttu-id="2040c-134">Il file di output per archiviare il backup dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2040c-134">The output file to store the storage account backup.</span></span>
<span data-ttu-id="2040c-135">Se non viene specificato, verrà generato un nome file predefinito.</span><span class="sxs-lookup"><span data-stu-id="2040c-135">If not specified, a default filename will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2040c-136">-VaultName</span><span class="sxs-lookup"><span data-stu-id="2040c-136">-VaultName</span></span>
<span data-ttu-id="2040c-137">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="2040c-137">Vault name.</span></span>
<span data-ttu-id="2040c-138">Il cmdlet crea l'FQDN di un vault in base al nome e all'ambiente attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="2040c-138">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByStorageAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2040c-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2040c-139">-Confirm</span></span>
<span data-ttu-id="2040c-140">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2040c-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2040c-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2040c-141">-WhatIf</span></span>
<span data-ttu-id="2040c-142">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2040c-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2040c-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2040c-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2040c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2040c-144">CommonParameters</span></span>
<span data-ttu-id="2040c-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2040c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2040c-146">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2040c-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2040c-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="2040c-147">INPUTS</span></span>

### <span data-ttu-id="2040c-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="2040c-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="2040c-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2040c-149">OUTPUTS</span></span>

### <span data-ttu-id="2040c-150">System.String</span><span class="sxs-lookup"><span data-stu-id="2040c-150">System.String</span></span>

## <span data-ttu-id="2040c-151">NOTE</span><span class="sxs-lookup"><span data-stu-id="2040c-151">NOTES</span></span>

## <span data-ttu-id="2040c-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2040c-152">RELATED LINKS</span></span>
