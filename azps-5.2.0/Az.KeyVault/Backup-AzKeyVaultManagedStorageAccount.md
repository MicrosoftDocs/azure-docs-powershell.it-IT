---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: c01d07f9408804b229921394c24e444b2a4deb8b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372791"
---
# <span data-ttu-id="62b01-101">Backup-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="62b01-101">Backup-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="62b01-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="62b01-102">SYNOPSIS</span></span>
<span data-ttu-id="62b01-103">Eseguire il backup di un account di archiviazione gestito con il Vault.</span><span class="sxs-lookup"><span data-stu-id="62b01-103">Backs up a KeyVault-managed storage account.</span></span>

## <span data-ttu-id="62b01-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="62b01-104">SYNTAX</span></span>

### <span data-ttu-id="62b01-105">ByStorageAccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="62b01-105">ByStorageAccountName (Default)</span></span>
```
Backup-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62b01-106">ByStorageAccount</span><span class="sxs-lookup"><span data-stu-id="62b01-106">ByStorageAccount</span></span>
```
Backup-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-OutputFile] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="62b01-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="62b01-107">DESCRIPTION</span></span>
<span data-ttu-id="62b01-108">Il cmdlet **backup-AzKeyVaultManagedStorageAccount** consente di eseguire il backup di un account di archiviazione gestita specificato in un Vault chiave, scaricarlo e archiviarlo in un file.</span><span class="sxs-lookup"><span data-stu-id="62b01-108">The **Backup-AzKeyVaultManagedStorageAccount** cmdlet backs up a specified managed storage account in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="62b01-109">Poiché il contenuto scaricato è crittografato, non può essere usato all'esterno dell'archivio di chiavi di Azure.</span><span class="sxs-lookup"><span data-stu-id="62b01-109">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="62b01-110">È possibile ripristinare un account di archiviazione di cui è stato eseguito il backup in qualsiasi volta chiave nell'abbonamento a cui è stato eseguito il backup, purché il Vault si trovi nella stessa geografia di Azure.</span><span class="sxs-lookup"><span data-stu-id="62b01-110">You can restore a backed-up storage account to any key vault in the subscription that it was backed up from, as long as the vault is in the same Azure geography.</span></span>
<span data-ttu-id="62b01-111">I motivi tipici per usare questo cmdlet sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="62b01-111">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="62b01-112">Si vuole mantenere una copia offline dell'account di archiviazione se si elimina accidentalmente l'originale dall'archivio.</span><span class="sxs-lookup"><span data-stu-id="62b01-112">You want to retain an offline copy of the storage account in case you accidentally delete the original from the vault.</span></span>
 
- <span data-ttu-id="62b01-113">È stato creato un account di archiviazione gestita con Key Vault e ora si vuole clonare l'oggetto in un'area di Azure diversa, in modo da poterlo usare in tutte le istanze dell'applicazione distribuita.</span><span class="sxs-lookup"><span data-stu-id="62b01-113">You created a managed storage account using Key Vault and now want to clone the object into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="62b01-114">Usa il cmdlet **backup-AzKeyVaultManagedStorageAccount** per recuperare l'account di archiviazione gestita in formato crittografato e quindi usa il cmdlet **Restore-AzKeyVaultManagedStorageAccount** e specifica un Vault chiave nella seconda area.</span><span class="sxs-lookup"><span data-stu-id="62b01-114">Use the **Backup-AzKeyVaultManagedStorageAccount** cmdlet to retrieve the managed storage account in encrypted format and then use the **Restore-AzKeyVaultManagedStorageAccount** cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="62b01-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="62b01-115">EXAMPLES</span></span>

### <span data-ttu-id="62b01-116">Esempio 1: eseguire il backup di un account di archiviazione gestita con un nome file generato automaticamente</span><span class="sxs-lookup"><span data-stu-id="62b01-116">Example 1: Back up a managed storage account with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'

C:\Users\username\mykeyvault-mymsak-1527029447.01191
```

<span data-ttu-id="62b01-117">Questo comando Recupera l'account di archiviazione gestita denominato MyMSAK dal Vault chiave denominato MyKeyVault e salva una copia di backup dell'account di archiviazione gestita in un file denominato automaticamente e visualizza il nome del file.</span><span class="sxs-lookup"><span data-stu-id="62b01-117">This command retrieves the managed storage account named MyMSAK from the key vault named MyKeyVault and saves a backup of that managed storage account to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="62b01-118">Esempio 2: eseguire il backup di un account di archiviazione gestita in un nome file specificato</span><span class="sxs-lookup"><span data-stu-id="62b01-118">Example 2: Back up a managed storage account to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyMSAK' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="62b01-119">Questo comando Recupera l'account di archiviazione gestita denominato MyMSAK dal Vault chiave denominato MyKeyVault e salva una copia di backup dell'account di archiviazione gestita in un file denominato backup. blob.</span><span class="sxs-lookup"><span data-stu-id="62b01-119">This command retrieves the managed storage account named MyMSAK from the key vault named MyKeyVault and saves a backup of that managed storage account to a file named Backup.blob.</span></span>

### <span data-ttu-id="62b01-120">Esempio 3: eseguire il backup di un account di archiviazione gestita precedentemente recuperato in un nome file specificato, sovrascrivendo il file di destinazione senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="62b01-120">Example 3: Back up a previously retrieved managed storage account to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $msak = Get-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'
PS C:\> Backup-AzKeyVaultManagedStorageAccount -StorageAccount $msak -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="62b01-121">Questo comando crea una copia di backup dell'account di archiviazione gestita denominato $msak. Nome nel Vault denominato $msak. VAULTNAME in un file denominato backup. blob, sovrascrivendo automaticamente il file se esiste già.</span><span class="sxs-lookup"><span data-stu-id="62b01-121">This command creates a backup of the managed storage account named $msak.Name in the vault named $msak.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="62b01-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="62b01-122">PARAMETERS</span></span>

### <span data-ttu-id="62b01-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62b01-123">-DefaultProfile</span></span>
<span data-ttu-id="62b01-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="62b01-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62b01-125">-Force</span><span class="sxs-lookup"><span data-stu-id="62b01-125">-Force</span></span>
<span data-ttu-id="62b01-126">Sovrascrivere il file assegnato se esiste</span><span class="sxs-lookup"><span data-stu-id="62b01-126">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="62b01-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62b01-127">-InputObject</span></span>
<span data-ttu-id="62b01-128">Bundle account di archiviazione di cui eseguire il backup, tramite pipeline nell'output di una chiamata di recupero.</span><span class="sxs-lookup"><span data-stu-id="62b01-128">Storage account bundle to be backed up, pipelined in from the output of a retrieval call.</span></span>

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

### <span data-ttu-id="62b01-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="62b01-129">-Name</span></span>
<span data-ttu-id="62b01-130">Nome segreto.</span><span class="sxs-lookup"><span data-stu-id="62b01-130">Secret name.</span></span>
<span data-ttu-id="62b01-131">Cmdlet costruisce il nome di dominio completo di un segreto dal nome della volta, dall'ambiente selezionato e da quello segreto.</span><span class="sxs-lookup"><span data-stu-id="62b01-131">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="62b01-132">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="62b01-132">-OutputFile</span></span>
<span data-ttu-id="62b01-133">File di output.</span><span class="sxs-lookup"><span data-stu-id="62b01-133">Output file.</span></span>
<span data-ttu-id="62b01-134">Il file di output per archiviare il backup dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="62b01-134">The output file to store the storage account backup.</span></span>
<span data-ttu-id="62b01-135">Se non specificato, verrà generato un nome file predefinito.</span><span class="sxs-lookup"><span data-stu-id="62b01-135">If not specified, a default filename will be generated.</span></span>

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

### <span data-ttu-id="62b01-136">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="62b01-136">-VaultName</span></span>
<span data-ttu-id="62b01-137">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="62b01-137">Vault name.</span></span>
<span data-ttu-id="62b01-138">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="62b01-138">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="62b01-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="62b01-139">-Confirm</span></span>
<span data-ttu-id="62b01-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62b01-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62b01-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62b01-141">-WhatIf</span></span>
<span data-ttu-id="62b01-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="62b01-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62b01-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="62b01-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62b01-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62b01-144">CommonParameters</span></span>
<span data-ttu-id="62b01-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62b01-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62b01-146">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="62b01-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62b01-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="62b01-147">INPUTS</span></span>

### <span data-ttu-id="62b01-148">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="62b01-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="62b01-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="62b01-149">OUTPUTS</span></span>

### <span data-ttu-id="62b01-150">System. String</span><span class="sxs-lookup"><span data-stu-id="62b01-150">System.String</span></span>

## <span data-ttu-id="62b01-151">Note</span><span class="sxs-lookup"><span data-stu-id="62b01-151">NOTES</span></span>

## <span data-ttu-id="62b01-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="62b01-152">RELATED LINKS</span></span>
