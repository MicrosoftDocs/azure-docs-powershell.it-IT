---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: ab126ee6bfc6a19f4a3a9997a75a01277437e42d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952510"
---
# <span data-ttu-id="01734-101">Remove-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="01734-101">Remove-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="01734-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01734-102">SYNOPSIS</span></span>
<span data-ttu-id="01734-103">Rimuove un account di archiviazione di Azure gestito da Vault della chiave e tutte le definizioni di firma di accesso condiviso associate.</span><span class="sxs-lookup"><span data-stu-id="01734-103">Removes a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>

## <span data-ttu-id="01734-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="01734-104">SYNTAX</span></span>

### <span data-ttu-id="01734-105">ByDefinitionName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="01734-105">ByDefinitionName (Default)</span></span>
```
Remove-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-InRemovedState] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01734-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="01734-106">ByInputObject</span></span>
```
Remove-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-InRemovedState] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="01734-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="01734-107">DESCRIPTION</span></span>
<span data-ttu-id="01734-108">L'associazione di un account di archiviazione di Azure al Vault chiave viene disassociata.</span><span class="sxs-lookup"><span data-stu-id="01734-108">Disassociates an Azure Storage Account from Key Vault.</span></span> <span data-ttu-id="01734-109">In questo modo non viene rimosso un account di archiviazione di Azure, ma le chiavi dell'account non vengono gestite dal Vault delle chiavi di Azure.</span><span class="sxs-lookup"><span data-stu-id="01734-109">This does not remove an Azure Storage Account but removes the account keys from being managed by Azure Key Vault.</span></span> <span data-ttu-id="01734-110">Vengono rimosse anche tutte le definizioni della firma di accesso condiviso gestito da Vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="01734-110">All associated Key Vault managed Storage SAS definitions are also removed.</span></span>

## <span data-ttu-id="01734-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="01734-111">EXAMPLES</span></span>

### <span data-ttu-id="01734-112">Esempio 1: Rimuovere un account di archiviazione di Azure gestito dal Vault della chiave e tutte le definizioni di firma di accesso condiviso associate.</span><span class="sxs-lookup"><span data-stu-id="01734-112">Example 1: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>
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

<span data-ttu-id="01734-113">L'associazione dell'account di archiviazione di Azure 'mystorageaccount' al Vault delle chiavi 'myvault' interrompe la gestione delle chiavi da parte di Vault.</span><span class="sxs-lookup"><span data-stu-id="01734-113">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="01734-114">L'account 'mystorageaccount' non verrà rimosso.</span><span class="sxs-lookup"><span data-stu-id="01734-114">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="01734-115">Tutte le definizioni della firma di accesso condiviso gestite da Vault chiave associate all'account verranno rimosse.</span><span class="sxs-lookup"><span data-stu-id="01734-115">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="01734-116">Esempio 2: rimuovere un account di archiviazione di Azure gestito dal Vault della chiave e tutte le definizioni di firma di accesso condiviso associate senza conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="01734-116">Example 2: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions without user confirmation.</span></span>
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

<span data-ttu-id="01734-117">L'associazione dell'account di archiviazione di Azure 'mystorageaccount' al Vault delle chiavi 'myvault' interrompe la gestione delle chiavi da parte di Vault.</span><span class="sxs-lookup"><span data-stu-id="01734-117">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="01734-118">L'account 'mystorageaccount' non verrà rimosso.</span><span class="sxs-lookup"><span data-stu-id="01734-118">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="01734-119">Tutte le definizioni della firma di accesso condiviso gestite da Vault chiave associate all'account verranno rimosse.</span><span class="sxs-lookup"><span data-stu-id="01734-119">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="01734-120">Esempio 3: Eliminare definitivamente (ripulire) un account di archiviazione di Azure gestito da Vault della chiave e tutte le definizioni di firma di accesso condiviso associate da un vault abilitato per l'eliminazione reverscita.</span><span class="sxs-lookup"><span data-stu-id="01734-120">Example 3: Permanently delete (purge) a Key Vault managed Azure Storage Account and all associated SAS definitions from a soft-delete-enabled vault.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' 
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
```

<span data-ttu-id="01734-121">L'esempio presuppone che l'eliminazione rescisa sia abilitata per il vault.</span><span class="sxs-lookup"><span data-stu-id="01734-121">The example assumes that soft-delete is enabled for this vault.</span></span> <span data-ttu-id="01734-122">Verificare se è questo il caso esaminando le proprietà del vault o l'attributo RecoveryLevel di un'entità nel vault.</span><span class="sxs-lookup"><span data-stu-id="01734-122">Verify whether that is the case by examining the vault properties, or the RecoveryLevel attribute of an entity in the vault.</span></span>
<span data-ttu-id="01734-123">Il primo cmdlet disassocia l'account di archiviazione di Azure 'mystorageaccount' dal Vault delle chiavi 'myvault' e impedisce a Vault delle chiavi di gestire le relative chiavi.</span><span class="sxs-lookup"><span data-stu-id="01734-123">The first cmdlet disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="01734-124">L'account 'mystorageaccount' non verrà rimosso.</span><span class="sxs-lookup"><span data-stu-id="01734-124">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="01734-125">Tutte le definizioni della firma di accesso condiviso gestite da Vault chiave associate all'account verranno rimosse.</span><span class="sxs-lookup"><span data-stu-id="01734-125">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>
<span data-ttu-id="01734-126">Il secondo cmdlet verifica che l'account di archiviazione sia in stato eliminato, ma ripristinabile.</span><span class="sxs-lookup"><span data-stu-id="01734-126">The second cmdlet verifies that the storage account is in a deleted, but recoverable state.</span></span> <span data-ttu-id="01734-127">Per raggiungere questo stato può essere necessario del tempo, consenti circa 30s prima di tentare.</span><span class="sxs-lookup"><span data-stu-id="01734-127">Reaching this state may require some time, please allow ~30s before attempting.</span></span>
<span data-ttu-id="01734-128">Il terzo cmdlet rimuove definitivamente l'account di archiviazione: il ripristino non sarà più possibile.</span><span class="sxs-lookup"><span data-stu-id="01734-128">The third cmdlet permanently removes the storage account - recovery will no longer be possible.</span></span>

## <span data-ttu-id="01734-129">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01734-129">PARAMETERS</span></span>

### <span data-ttu-id="01734-130">-AccountName</span><span class="sxs-lookup"><span data-stu-id="01734-130">-AccountName</span></span>
<span data-ttu-id="01734-131">Nome dell'account di archiviazione gestito dal Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="01734-131">Key Vault managed storage account name.</span></span> <span data-ttu-id="01734-132">Il cmdlet crea l'FQDN di un account di archiviazione gestito dal nome del vault, dall'ambiente attualmente selezionato e dal nome dell'account di archiviazione gestito.</span><span class="sxs-lookup"><span data-stu-id="01734-132">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="01734-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01734-133">-DefaultProfile</span></span>
<span data-ttu-id="01734-134">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="01734-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="01734-135">-Force</span><span class="sxs-lookup"><span data-stu-id="01734-135">-Force</span></span>
<span data-ttu-id="01734-136">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="01734-136">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="01734-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01734-137">-InputObject</span></span>
<span data-ttu-id="01734-138">Oggetto ManagedStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="01734-138">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="01734-139">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="01734-139">-InRemovedState</span></span>
<span data-ttu-id="01734-140">Rimuovere definitivamente l'account di archiviazione gestito eliminato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="01734-140">Permanently remove the previously deleted managed storage account.</span></span>

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

### <span data-ttu-id="01734-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01734-141">-PassThru</span></span>
<span data-ttu-id="01734-142">Il cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="01734-142">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="01734-143">Se si specifica questa opzione, il cmdlet restituisce l'account di archiviazione gestito eliminato.</span><span class="sxs-lookup"><span data-stu-id="01734-143">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="01734-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="01734-144">-VaultName</span></span>
<span data-ttu-id="01734-145">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="01734-145">Vault name.</span></span>
<span data-ttu-id="01734-146">Il cmdlet crea l'FQDN di un vault in base al nome e all'ambiente attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="01734-146">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="01734-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01734-147">-Confirm</span></span>
<span data-ttu-id="01734-148">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01734-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01734-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01734-149">-WhatIf</span></span>
<span data-ttu-id="01734-150">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="01734-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01734-151">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="01734-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01734-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01734-152">CommonParameters</span></span>
<span data-ttu-id="01734-153">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01734-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01734-154">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="01734-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01734-155">INPUT</span><span class="sxs-lookup"><span data-stu-id="01734-155">INPUTS</span></span>

### <span data-ttu-id="01734-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="01734-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="01734-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="01734-157">OUTPUTS</span></span>

### <span data-ttu-id="01734-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="01734-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="01734-159">NOTE</span><span class="sxs-lookup"><span data-stu-id="01734-159">NOTES</span></span>

## <span data-ttu-id="01734-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="01734-160">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

