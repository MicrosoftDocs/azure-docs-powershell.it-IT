---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 90f6347346c0967e29917ffe56e7ba13f7e705de
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93865207"
---
# <span data-ttu-id="7b382-101">Add-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7b382-101">Add-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="7b382-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7b382-102">SYNOPSIS</span></span>
<span data-ttu-id="7b382-103">Aggiunge un account di archiviazione di Azure esistente al Vault Key specificato in modo che le chiavi vengano gestite dal servizio Key Vault.</span><span class="sxs-lookup"><span data-stu-id="7b382-103">Adds an existing Azure Storage Account to the specified key vault for its keys to be managed by the Key Vault service.</span></span>

## <span data-ttu-id="7b382-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7b382-104">SYNTAX</span></span>

```
Add-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-AccountResourceId] <String>
 [-ActiveKeyName] <String> [-DisableAutoRegenerateKey] [-RegenerationPeriod <TimeSpan>] [-Disable]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b382-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7b382-105">DESCRIPTION</span></span>
<span data-ttu-id="7b382-106">Configura un account di archiviazione di Azure esistente con Key Vault per i tasti dell'account di archiviazione da gestire tramite Key Vault.</span><span class="sxs-lookup"><span data-stu-id="7b382-106">Sets up an existing Azure Storage Account with Key Vault for Storage Account keys to be managed by Key Vault.</span></span> <span data-ttu-id="7b382-107">L'account di archiviazione deve già esistere.</span><span class="sxs-lookup"><span data-stu-id="7b382-107">The Storage Account must already exist.</span></span> <span data-ttu-id="7b382-108">Le chiavi di archiviazione non vengono mai esposte al chiamante.</span><span class="sxs-lookup"><span data-stu-id="7b382-108">The Storage Keys are never exposed to caller.</span></span>
<span data-ttu-id="7b382-109">Key Vault auto rigenera e commuta la chiave attiva in base al periodo di rigenerazione.</span><span class="sxs-lookup"><span data-stu-id="7b382-109">Key Vault auto regenerates and switches the active key based on the regeneration period.</span></span> <span data-ttu-id="7b382-110">Vedere l' [account di archiviazione gestita di Azure Key Vault-PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-overview-storage-keys-powershell) per una panoramica di questa caratteristica.</span><span class="sxs-lookup"><span data-stu-id="7b382-110">See [Azure Key Vault managed storage account - PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-overview-storage-keys-powershell) for an overview of this feature.</span></span>

## <span data-ttu-id="7b382-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7b382-111">EXAMPLES</span></span>

### <span data-ttu-id="7b382-112">Esempio 1: impostare un account di archiviazione di Azure con il Vault chiave per gestire le chiavi</span><span class="sxs-lookup"><span data-stu-id="7b382-112">Example 1: Set an Azure Storage Account with Key Vault to manage its keys</span></span>
```powershell
PS C:\> $storage = Get-AzStorageAccount -ResourceGroupName "mystorageResourceGroup" -StorageAccountName "mystorage"
PS C:\> $servicePrincipal = Get-AzADServicePrincipal -ServicePrincipalName cfa8b339-82a2-471a-a3c9-0fc0be7a4093
PS C:\> New-AzRoleAssignment -ObjectId $servicePrincipal.Id -RoleDefinitionName 'Storage Account Key Operator Service Role' -Scope $storage.Id
PS C:\> $userPrincipalId = $(Get-AzADUser -SearchString "developer@contoso.com").Id
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName $keyVaultName -ObjectId $userPrincipalId -PermissionsToStorage get, set
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -AccountResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount' -ActiveKeyName 'key1' -RegenerationPeriod $regenerationPeriod

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key1
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="7b382-113">Imposta un account di archiviazione con Key Vault per consentire la gestione delle chiavi tramite Key Vault.</span><span class="sxs-lookup"><span data-stu-id="7b382-113">Sets a Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="7b382-114">Il set di tasti attivi è "Key1".</span><span class="sxs-lookup"><span data-stu-id="7b382-114">The active key set is 'key1'.</span></span> <span data-ttu-id="7b382-115">Questa chiave verrà usata per generare i token SAS.</span><span class="sxs-lookup"><span data-stu-id="7b382-115">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="7b382-116">Key Vault rigenererà la chiave "key2" dopo il periodo di rigenerazione dall'ora di questo comando e la imposterà come chiave attiva.</span><span class="sxs-lookup"><span data-stu-id="7b382-116">Key Vault will regenerate 'key2' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="7b382-117">Questo processo di rigenerazione automatica continuerà tra "Key1" e "key2" con una lacuna di 90 giorni.</span><span class="sxs-lookup"><span data-stu-id="7b382-117">This auto regeneration process will continue between 'key1' and 'key2' with a gap of 90 days.</span></span>

### <span data-ttu-id="7b382-118">Esempio 2: impostare un account di archiviazione di Azure classico con il Vault chiave per gestire le chiavi</span><span class="sxs-lookup"><span data-stu-id="7b382-118">Example 2: Set a Classic Azure Storage Account with Key Vault to manage its keys</span></span>
```powershell
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -AccountResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount' -ActiveKeyName 'Primary' -RegenerationPeriod $regenerationPeriod

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myvault/providers/Microsoft.Cl
                      assicStorage/storageAccounts/mystorageaccount
Active Key Name     : Primary
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="7b382-119">Imposta un account di archiviazione classico con Key Vault per consentire la gestione delle chiavi tramite Key Vault.</span><span class="sxs-lookup"><span data-stu-id="7b382-119">Sets a Classic Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="7b382-120">Il set di tasti attivi è "Primary".</span><span class="sxs-lookup"><span data-stu-id="7b382-120">The active key set is 'Primary'.</span></span> <span data-ttu-id="7b382-121">Questa chiave verrà usata per generare i token SAS.</span><span class="sxs-lookup"><span data-stu-id="7b382-121">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="7b382-122">Key Vault rigenererà il codice "secondario" dopo il periodo di rigenerazione dall'ora di questo comando e lo imposterà come chiave attiva.</span><span class="sxs-lookup"><span data-stu-id="7b382-122">Key Vault will regenerate 'Secondary' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="7b382-123">Questo processo di rigenerazione automatica continuerà tra "primario" e "secondario" con una lacuna di 90 giorni.</span><span class="sxs-lookup"><span data-stu-id="7b382-123">This auto regeneration process will continue between 'Primary' and 'Secondary' with a gap of 90 days.</span></span>

## <span data-ttu-id="7b382-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7b382-124">PARAMETERS</span></span>

### <span data-ttu-id="7b382-125">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7b382-125">-AccountName</span></span>
<span data-ttu-id="7b382-126">Nome dell'account di archiviazione gestito Key Vault.</span><span class="sxs-lookup"><span data-stu-id="7b382-126">Key Vault managed storage account name.</span></span> <span data-ttu-id="7b382-127">Cmdlet crea l'FQDN di un nome di account di archiviazione gestito dal nome del Vault, dall'ambiente selezionato e dal nome dell'account di archiviazione modificato.</span><span class="sxs-lookup"><span data-stu-id="7b382-127">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b382-128">-AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="7b382-128">-AccountResourceId</span></span>
<span data-ttu-id="7b382-129">ID risorsa Azure dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7b382-129">Azure resource id of the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountResourceId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b382-130">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="7b382-130">-ActiveKeyName</span></span>
<span data-ttu-id="7b382-131">Nome della chiave dell'account di archiviazione che deve essere usata per la generazione di token SAS.</span><span class="sxs-lookup"><span data-stu-id="7b382-131">Name of the storage account key that must be used for generating sas tokens.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b382-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b382-132">-DefaultProfile</span></span>
<span data-ttu-id="7b382-133">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7b382-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7b382-134">-Disable</span><span class="sxs-lookup"><span data-stu-id="7b382-134">-Disable</span></span>
<span data-ttu-id="7b382-135">Disabilita l'uso della chiave dell'account di archiviazione gestita per la generazione di token SAS.</span><span class="sxs-lookup"><span data-stu-id="7b382-135">Disables the use of managed storage account's key for generation of sas tokens.</span></span>

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

### <span data-ttu-id="7b382-136">-DisableAutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="7b382-136">-DisableAutoRegenerateKey</span></span>
<span data-ttu-id="7b382-137">Chiave di rigenerazione automatica.</span><span class="sxs-lookup"><span data-stu-id="7b382-137">Auto regenerate key.</span></span> <span data-ttu-id="7b382-138">Se true, la chiave inattiva dell'account di archiviazione gestita viene rigenerata automaticamente e diventa la nuova chiave attiva dopo il periodo di rigenerazione.</span><span class="sxs-lookup"><span data-stu-id="7b382-138">If true, then the managed storage account's inactive key gets auto regenerated and becomes the new active key after the regeneration period.</span></span> <span data-ttu-id="7b382-139">Se false, le chiavi dell'account di archiviazione gestita non vengono rigenerate automaticamente.</span><span class="sxs-lookup"><span data-stu-id="7b382-139">If false, then the keys of managed storage account are not auto regenerated.</span></span>

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

### <span data-ttu-id="7b382-140">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="7b382-140">-RegenerationPeriod</span></span>
<span data-ttu-id="7b382-141">Periodo di rigenerazione.</span><span class="sxs-lookup"><span data-stu-id="7b382-141">Regeneration period.</span></span> <span data-ttu-id="7b382-142">Se la chiave di rigenerazione automatica è abilitata, questo valore specifica l'intervallo di valori TimeSpan dopo il quale il tasto inattivo dell'account di archiviazione gestito viene rigenerato automaticamente e diventa la nuova chiave attiva.</span><span class="sxs-lookup"><span data-stu-id="7b382-142">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the new active key.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b382-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="7b382-143">-Tag</span></span>
<span data-ttu-id="7b382-144">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="7b382-144">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7b382-145">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="7b382-145">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b382-146">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="7b382-146">-VaultName</span></span>
<span data-ttu-id="7b382-147">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="7b382-147">Vault name.</span></span>
<span data-ttu-id="7b382-148">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="7b382-148">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b382-149">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7b382-149">-Confirm</span></span>
<span data-ttu-id="7b382-150">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b382-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b382-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b382-151">-WhatIf</span></span>
<span data-ttu-id="7b382-152">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7b382-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b382-153">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7b382-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b382-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b382-154">CommonParameters</span></span>
<span data-ttu-id="7b382-155">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b382-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b382-156">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7b382-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b382-157">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7b382-157">INPUTS</span></span>

### <span data-ttu-id="7b382-158">System. String</span><span class="sxs-lookup"><span data-stu-id="7b382-158">System.String</span></span>

### <span data-ttu-id="7b382-159">System. Nullable ' 1 [[System. TimeSpan, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7b382-159">System.Nullable\`1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="7b382-160">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7b382-160">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7b382-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7b382-161">OUTPUTS</span></span>

### <span data-ttu-id="7b382-162">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7b382-162">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="7b382-163">Note</span><span class="sxs-lookup"><span data-stu-id="7b382-163">NOTES</span></span>

## <span data-ttu-id="7b382-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7b382-164">RELATED LINKS</span></span>

[<span data-ttu-id="7b382-165">AZ. Vault</span><span class="sxs-lookup"><span data-stu-id="7b382-165">Az.KeyVault</span></span>](/powershell/module/az.keyvault)
