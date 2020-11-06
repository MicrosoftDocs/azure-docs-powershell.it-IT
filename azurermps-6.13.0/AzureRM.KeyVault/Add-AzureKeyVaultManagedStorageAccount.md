---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: fcef87b196d07ffd7a4ce43bda2cf1c2372910b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515228"
---
# <span data-ttu-id="1b6be-101">Add-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1b6be-101">Add-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="1b6be-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1b6be-102">SYNOPSIS</span></span>
<span data-ttu-id="1b6be-103">Aggiunge un account di archiviazione di Azure esistente al Vault Key specificato in modo che le chiavi vengano gestite dal servizio Key Vault.</span><span class="sxs-lookup"><span data-stu-id="1b6be-103">Adds an existing Azure Storage Account to the specified key vault for its keys to be managed by the Key Vault service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b6be-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1b6be-104">SYNTAX</span></span>

```
Add-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-AccountResourceId] <String> [-ActiveKeyName] <String> [-DisableAutoRegenerateKey]
 [-RegenerationPeriod <TimeSpan>] [-Disable] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b6be-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b6be-105">DESCRIPTION</span></span>
<span data-ttu-id="1b6be-106">Configura un account di archiviazione di Azure esistente con Key Vault per i tasti dell'account di archiviazione da gestire tramite Key Vault.</span><span class="sxs-lookup"><span data-stu-id="1b6be-106">Sets up an existing Azure Storage Account with Key Vault for Storage Account keys to be managed by Key Vault.</span></span> <span data-ttu-id="1b6be-107">L'account di archiviazione deve già esistere.</span><span class="sxs-lookup"><span data-stu-id="1b6be-107">The Storage Account must already exist.</span></span> <span data-ttu-id="1b6be-108">Le chiavi di archiviazione non vengono mai esposte al chiamante.</span><span class="sxs-lookup"><span data-stu-id="1b6be-108">The Storage Keys are never exposed to caller.</span></span>
<span data-ttu-id="1b6be-109">Key Vault auto rigenera e commuta la chiave attiva in base al periodo di rigenerazione.</span><span class="sxs-lookup"><span data-stu-id="1b6be-109">Key Vault auto regenerates and switches the active key based on the regeneration period.</span></span>

## <span data-ttu-id="1b6be-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1b6be-110">EXAMPLES</span></span>

### <span data-ttu-id="1b6be-111">Esempio 1: impostare un account di archiviazione di Azure con il Vault chiave per gestire le chiavi</span><span class="sxs-lookup"><span data-stu-id="1b6be-111">Example 1: Set an Azure Storage Account with Key Vault to manage its keys</span></span>
```powershell
PS C:\> $storage = Get-AzureRmStorageAccount -ResourceGroupName "mystorageResourceGroup" -StorageAccountName "mystorage"
PS C:\> $servicePrincipal = Get-AzureRmADServicePrincipal -ServicePrincipalName cfa8b339-82a2-471a-a3c9-0fc0be7a4093
PS C:\> New-AzureRmRoleAssignment -ObjectId $servicePrincipal.Id -RoleDefinitionName 'Storage Account Key Operator Service Role' -Scope $storage.Id
PS C:\> $userPrincipalId = $(Get-AzureRmADUser -SearchString "developer@contoso.com").Id
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName $keyVaultName -ObjectId $userPrincipalId -PermissionsToStorage get, set
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -AccountResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount' -ActiveKeyName 'key1' -RegenerationPeriod $regenerationPeriod

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

<span data-ttu-id="1b6be-112">Imposta un account di archiviazione con Key Vault per consentire la gestione delle chiavi tramite Key Vault.</span><span class="sxs-lookup"><span data-stu-id="1b6be-112">Sets a Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="1b6be-113">Il set di tasti attivi è "Key1".</span><span class="sxs-lookup"><span data-stu-id="1b6be-113">The active key set is 'key1'.</span></span> <span data-ttu-id="1b6be-114">Questa chiave verrà usata per generare i token SAS.</span><span class="sxs-lookup"><span data-stu-id="1b6be-114">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="1b6be-115">Key Vault rigenererà la chiave "key2" dopo il periodo di rigenerazione dall'ora di questo comando e la imposterà come chiave attiva.</span><span class="sxs-lookup"><span data-stu-id="1b6be-115">Key Vault will regenerate 'key2' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="1b6be-116">Questo processo di rigenerazione automatica continuerà tra "Key1" e "key2" con una lacuna di 90 giorni.</span><span class="sxs-lookup"><span data-stu-id="1b6be-116">This auto regeneration process will continue between 'key1' and 'key2' with a gap of 90 days.</span></span>

### <span data-ttu-id="1b6be-117">Esempio 2: impostare un account di archiviazione di Azure classico con il Vault chiave per gestire le chiavi</span><span class="sxs-lookup"><span data-stu-id="1b6be-117">Example 2: Set a Classic Azure Storage Account with Key Vault to manage its keys</span></span>
```powershell
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -AccountResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount' -ActiveKeyName 'Primary' -RegenerationPeriod $regenerationPeriod

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

<span data-ttu-id="1b6be-118">Imposta un account di archiviazione classico con Key Vault per consentire la gestione delle chiavi tramite Key Vault.</span><span class="sxs-lookup"><span data-stu-id="1b6be-118">Sets a Classic Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="1b6be-119">Il set di tasti attivi è "Primary".</span><span class="sxs-lookup"><span data-stu-id="1b6be-119">The active key set is 'Primary'.</span></span> <span data-ttu-id="1b6be-120">Questa chiave verrà usata per generare i token SAS.</span><span class="sxs-lookup"><span data-stu-id="1b6be-120">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="1b6be-121">Key Vault rigenererà il codice "secondario" dopo il periodo di rigenerazione dall'ora di questo comando e lo imposterà come chiave attiva.</span><span class="sxs-lookup"><span data-stu-id="1b6be-121">Key Vault will regenerate 'Secondary' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="1b6be-122">Questo processo di rigenerazione automatica continuerà tra "primario" e "secondario" con una lacuna di 90 giorni.</span><span class="sxs-lookup"><span data-stu-id="1b6be-122">This auto regeneration process will continue between 'Primary' and 'Secondary' with a gap of 90 days.</span></span>

## <span data-ttu-id="1b6be-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1b6be-123">PARAMETERS</span></span>

### <span data-ttu-id="1b6be-124">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1b6be-124">-AccountName</span></span>
<span data-ttu-id="1b6be-125">Nome dell'account di archiviazione gestito Key Vault.</span><span class="sxs-lookup"><span data-stu-id="1b6be-125">Key Vault managed storage account name.</span></span> <span data-ttu-id="1b6be-126">Cmdlet crea l'FQDN di un nome di account di archiviazione gestito dal nome del Vault, dall'ambiente selezionato e dal nome dell'account di archiviazione modificato.</span><span class="sxs-lookup"><span data-stu-id="1b6be-126">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="1b6be-127">-AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="1b6be-127">-AccountResourceId</span></span>
<span data-ttu-id="1b6be-128">ID risorsa Azure dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1b6be-128">Azure resource id of the storage account.</span></span>

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

### <span data-ttu-id="1b6be-129">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="1b6be-129">-ActiveKeyName</span></span>
<span data-ttu-id="1b6be-130">Nome della chiave dell'account di archiviazione che deve essere usata per la generazione di token SAS.</span><span class="sxs-lookup"><span data-stu-id="1b6be-130">Name of the storage account key that must be used for generating sas tokens.</span></span>

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

### <span data-ttu-id="1b6be-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b6be-131">-DefaultProfile</span></span>
<span data-ttu-id="1b6be-132">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1b6be-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b6be-133">-Disable</span><span class="sxs-lookup"><span data-stu-id="1b6be-133">-Disable</span></span>
<span data-ttu-id="1b6be-134">Disabilita l'uso della chiave dell'account di archiviazione gestita per la generazione di token SAS.</span><span class="sxs-lookup"><span data-stu-id="1b6be-134">Disables the use of managed storage account's key for generation of sas tokens.</span></span>

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

### <span data-ttu-id="1b6be-135">-DisableAutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="1b6be-135">-DisableAutoRegenerateKey</span></span>
<span data-ttu-id="1b6be-136">Chiave di rigenerazione automatica.</span><span class="sxs-lookup"><span data-stu-id="1b6be-136">Auto regenerate key.</span></span> <span data-ttu-id="1b6be-137">Se true, la chiave inattiva dell'account di archiviazione gestita viene rigenerata automaticamente e diventa la nuova chiave attiva dopo il periodo di rigenerazione.</span><span class="sxs-lookup"><span data-stu-id="1b6be-137">If true, then the managed storage account's inactive key gets auto regenerated and becomes the new active key after the regeneration period.</span></span> <span data-ttu-id="1b6be-138">Se false, le chiavi dell'account di archiviazione gestita non vengono rigenerate automaticamente.</span><span class="sxs-lookup"><span data-stu-id="1b6be-138">If false, then the keys of managed storage account are not auto regenerated.</span></span>

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

### <span data-ttu-id="1b6be-139">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="1b6be-139">-RegenerationPeriod</span></span>
<span data-ttu-id="1b6be-140">Periodo di rigenerazione.</span><span class="sxs-lookup"><span data-stu-id="1b6be-140">Regeneration period.</span></span> <span data-ttu-id="1b6be-141">Se la chiave di rigenerazione automatica è abilitata, questo valore specifica l'intervallo di valori TimeSpan dopo il quale il tasto inattivo dell'account di archiviazione gestito viene rigenerato automaticamente e diventa la nuova chiave attiva.</span><span class="sxs-lookup"><span data-stu-id="1b6be-141">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the new active key.</span></span>

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

### <span data-ttu-id="1b6be-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="1b6be-142">-Tag</span></span>
<span data-ttu-id="1b6be-143">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="1b6be-143">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1b6be-144">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="1b6be-144">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1b6be-145">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="1b6be-145">-VaultName</span></span>
<span data-ttu-id="1b6be-146">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="1b6be-146">Vault name.</span></span>
<span data-ttu-id="1b6be-147">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="1b6be-147">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="1b6be-148">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1b6be-148">-Confirm</span></span>
<span data-ttu-id="1b6be-149">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b6be-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b6be-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b6be-150">-WhatIf</span></span>
<span data-ttu-id="1b6be-151">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1b6be-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b6be-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1b6be-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b6be-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b6be-153">CommonParameters</span></span>
<span data-ttu-id="1b6be-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b6be-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b6be-155">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b6be-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b6be-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1b6be-156">INPUTS</span></span>

### <span data-ttu-id="1b6be-157">System. String</span><span class="sxs-lookup"><span data-stu-id="1b6be-157">System.String</span></span>

### <span data-ttu-id="1b6be-158">System. Nullable ' 1 [[System. TimeSpan, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="1b6be-158">System.Nullable\`1[[System.TimeSpan, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="1b6be-159">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1b6be-159">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1b6be-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1b6be-160">OUTPUTS</span></span>

### <span data-ttu-id="1b6be-161">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1b6be-161">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="1b6be-162">Note</span><span class="sxs-lookup"><span data-stu-id="1b6be-162">NOTES</span></span>

## <span data-ttu-id="1b6be-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1b6be-163">RELATED LINKS</span></span>

[<span data-ttu-id="1b6be-164">AzureRM. Vault</span><span class="sxs-lookup"><span data-stu-id="1b6be-164">AzureRM.KeyVault</span></span>](/powershell/module/azurerm.keyvault)
