---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: c415a7b80609a9e8794df183b2ae1cea73a7f1cd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864812"
---
# <span data-ttu-id="50fc2-101">Remove-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="50fc2-101">Remove-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="50fc2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="50fc2-102">SYNOPSIS</span></span>
<span data-ttu-id="50fc2-103">Consente di rimuovere un account di archiviazione di Azure Key Vault gestito e tutte le definizioni SAS associate.</span><span class="sxs-lookup"><span data-stu-id="50fc2-103">Removes a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>

## <span data-ttu-id="50fc2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="50fc2-104">SYNTAX</span></span>

### <span data-ttu-id="50fc2-105">ByDefinitionName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="50fc2-105">ByDefinitionName (Default)</span></span>
```
Remove-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-InRemovedState] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50fc2-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="50fc2-106">ByInputObject</span></span>
```
Remove-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-InRemovedState] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="50fc2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50fc2-107">DESCRIPTION</span></span>
<span data-ttu-id="50fc2-108">Dissocia un account di archiviazione di Azure da Key Vault.</span><span class="sxs-lookup"><span data-stu-id="50fc2-108">Disassociates an Azure Storage Account from Key Vault.</span></span> <span data-ttu-id="50fc2-109">In questo modo non viene rimosso un account di archiviazione di Azure, ma i tasti account vengono rimossi dall'archivio chiavi di Azure.</span><span class="sxs-lookup"><span data-stu-id="50fc2-109">This does not remove an Azure Storage Account but removes the account keys from being managed by Azure Key Vault.</span></span> <span data-ttu-id="50fc2-110">Vengono rimosse anche tutte le definizioni di archiviazione gestite di Key Vault associate.</span><span class="sxs-lookup"><span data-stu-id="50fc2-110">All associated Key Vault managed Storage SAS definitions are also removed.</span></span>

## <span data-ttu-id="50fc2-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="50fc2-111">EXAMPLES</span></span>

### <span data-ttu-id="50fc2-112">Esempio 1: rimuovere un account di archiviazione di Azure Key Vault gestito e tutte le definizioni SAS associate.</span><span class="sxs-lookup"><span data-stu-id="50fc2-112">Example 1: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -PassThru

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="50fc2-113">Annulla l'associazione dell'account di archiviazione di Azure "mystorageaccount" dal Vault Key "Vault" e interrompe la gestione delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="50fc2-113">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="50fc2-114">L'account "mystorageaccount" non verrà rimosso.</span><span class="sxs-lookup"><span data-stu-id="50fc2-114">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="50fc2-115">Verranno rimosse tutte le definizioni SAS di archiviazione gestite di Key Vault associate a questo account.</span><span class="sxs-lookup"><span data-stu-id="50fc2-115">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="50fc2-116">Esempio 2: rimuovere un account di archiviazione di Azure Key Vault gestito e tutte le definizioni SAS associate senza la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="50fc2-116">Example 2: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions without user confirmation.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -PassThru -Force

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="50fc2-117">Annulla l'associazione dell'account di archiviazione di Azure "mystorageaccount" dal Vault Key "Vault" e interrompe la gestione delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="50fc2-117">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="50fc2-118">L'account "mystorageaccount" non verrà rimosso.</span><span class="sxs-lookup"><span data-stu-id="50fc2-118">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="50fc2-119">Verranno rimosse tutte le definizioni SAS di archiviazione gestite di Key Vault associate a questo account.</span><span class="sxs-lookup"><span data-stu-id="50fc2-119">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="50fc2-120">Esempio 3: Elimina definitivamente (Purge) un account di archiviazione di Azure con chiave archiviata Key e tutte le definizioni SAS associate da un Vault abilitato per l'eliminazione soft.</span><span class="sxs-lookup"><span data-stu-id="50fc2-120">Example 3: Permanently delete (purge) a Key Vault managed Azure Storage Account and all associated SAS definitions from a soft-delete-enabled vault.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' 
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
```

<span data-ttu-id="50fc2-121">L'esempio presuppone che l'eliminazione morbida sia abilitata per il Vault.</span><span class="sxs-lookup"><span data-stu-id="50fc2-121">The example assumes that soft-delete is enabled for this vault.</span></span> <span data-ttu-id="50fc2-122">Verificare se questo è il caso esaminando le proprietà del Vault o l'attributo RecoveryLevel di un'entità nel Vault.</span><span class="sxs-lookup"><span data-stu-id="50fc2-122">Verify whether that is the case by examining the vault properties, or the RecoveryLevel attribute of an entity in the vault.</span></span>
<span data-ttu-id="50fc2-123">Il primo cmdlet Annulla l'associazione dell'account di archiviazione di Azure "mystorageaccount" dal Vault chiave "Vault" e interrompe la gestione delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="50fc2-123">The first cmdlet disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="50fc2-124">L'account "mystorageaccount" non verrà rimosso.</span><span class="sxs-lookup"><span data-stu-id="50fc2-124">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="50fc2-125">Verranno rimosse tutte le definizioni SAS di archiviazione gestite di Key Vault associate a questo account.</span><span class="sxs-lookup"><span data-stu-id="50fc2-125">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>
<span data-ttu-id="50fc2-126">Il secondo cmdlet verifica che l'account di archiviazione si trovi in uno stato eliminato, ma ripristinabile.</span><span class="sxs-lookup"><span data-stu-id="50fc2-126">The second cmdlet verifies that the storage account is in a deleted, but recoverable state.</span></span> <span data-ttu-id="50fc2-127">Il raggiungimento di questo stato può richiedere un po' di tempo, attendere 30 anni prima di tentare.</span><span class="sxs-lookup"><span data-stu-id="50fc2-127">Reaching this state may require some time, please allow ~30s before attempting.</span></span>
<span data-ttu-id="50fc2-128">Il terzo cmdlet rimuove definitivamente l'account di archiviazione-il ripristino non sarà più possibile.</span><span class="sxs-lookup"><span data-stu-id="50fc2-128">The third cmdlet permanently removes the storage account - recovery will no longer be possible.</span></span>

## <span data-ttu-id="50fc2-129">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="50fc2-129">PARAMETERS</span></span>

### <span data-ttu-id="50fc2-130">-AccountName</span><span class="sxs-lookup"><span data-stu-id="50fc2-130">-AccountName</span></span>
<span data-ttu-id="50fc2-131">Nome dell'account di archiviazione gestito Key Vault.</span><span class="sxs-lookup"><span data-stu-id="50fc2-131">Key Vault managed storage account name.</span></span> <span data-ttu-id="50fc2-132">Cmdlet crea l'FQDN di un nome di account di archiviazione gestito dal nome del Vault, dall'ambiente selezionato e dal nome dell'account di archiviazione modificato.</span><span class="sxs-lookup"><span data-stu-id="50fc2-132">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50fc2-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50fc2-133">-DefaultProfile</span></span>
<span data-ttu-id="50fc2-134">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="50fc2-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50fc2-135">-Force</span><span class="sxs-lookup"><span data-stu-id="50fc2-135">-Force</span></span>
<span data-ttu-id="50fc2-136">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="50fc2-136">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="50fc2-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50fc2-137">-InputObject</span></span>
<span data-ttu-id="50fc2-138">Oggetto ManagedStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="50fc2-138">ManagedStorageAccount object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50fc2-139">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="50fc2-139">-InRemovedState</span></span>
<span data-ttu-id="50fc2-140">Rimuovere definitivamente l'account di archiviazione gestita precedentemente eliminata.</span><span class="sxs-lookup"><span data-stu-id="50fc2-140">Permanently remove the previously deleted managed storage account.</span></span>

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

### <span data-ttu-id="50fc2-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="50fc2-141">-PassThru</span></span>
<span data-ttu-id="50fc2-142">Cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="50fc2-142">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="50fc2-143">Se questa opzione è specificata, cmdlet restituisce l'account di archiviazione gestita che è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="50fc2-143">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="50fc2-144">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="50fc2-144">-VaultName</span></span>
<span data-ttu-id="50fc2-145">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="50fc2-145">Vault name.</span></span>
<span data-ttu-id="50fc2-146">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="50fc2-146">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50fc2-147">-Confermare</span><span class="sxs-lookup"><span data-stu-id="50fc2-147">-Confirm</span></span>
<span data-ttu-id="50fc2-148">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50fc2-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50fc2-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50fc2-149">-WhatIf</span></span>
<span data-ttu-id="50fc2-150">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="50fc2-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50fc2-151">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="50fc2-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50fc2-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50fc2-152">CommonParameters</span></span>
<span data-ttu-id="50fc2-153">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50fc2-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50fc2-154">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="50fc2-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50fc2-155">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="50fc2-155">INPUTS</span></span>

### <span data-ttu-id="50fc2-156">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="50fc2-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="50fc2-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="50fc2-157">OUTPUTS</span></span>

### <span data-ttu-id="50fc2-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="50fc2-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="50fc2-159">Note</span><span class="sxs-lookup"><span data-stu-id="50fc2-159">NOTES</span></span>

## <span data-ttu-id="50fc2-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="50fc2-160">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

