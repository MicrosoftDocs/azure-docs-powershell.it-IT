---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 526472514be086118f8c5ed74cefb6983ad67065
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512583"
---
# <span data-ttu-id="cd3aa-101">Add-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd3aa-101">Add-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="cd3aa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cd3aa-102">SYNOPSIS</span></span>
<span data-ttu-id="cd3aa-103">Aggiunge un account di archiviazione di Azure esistente al Vault Key specificato in modo che le chiavi vengano gestite dal servizio Key Vault.</span><span class="sxs-lookup"><span data-stu-id="cd3aa-103">Adds an existing Azure Storage Account to the specified key vault for its keys to be managed by the Key Vault service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd3aa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cd3aa-104">SYNTAX</span></span>

```
Add-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-AccountResourceId] <String> [-ActiveKeyName] <String> [-DisableAutoRegenerateKey]
 [-RegenerationPeriod <TimeSpan>] [-Disable] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd3aa-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd3aa-105">DESCRIPTION</span></span>
<span data-ttu-id="cd3aa-106">Configura un account di archiviazione di Azure esistente con Key Vault per i tasti dell'account di archiviazione da gestire tramite Key Vault.</span><span class="sxs-lookup"><span data-stu-id="cd3aa-106">Sets up an existing Azure Storage Account with Key Vault for Storage Account keys to be managed by Key Vault.</span></span> <span data-ttu-id="cd3aa-107">L'account di archiviazione deve già esistere.</span><span class="sxs-lookup"><span data-stu-id="cd3aa-107">The Storage Account must already exist.</span></span> <span data-ttu-id="cd3aa-108">Le chiavi di archiviazione non vengono mai esposte al chiamante.</span><span class="sxs-lookup"><span data-stu-id="cd3aa-108">The Storage Keys are never exposed to caller.</span></span>
<span data-ttu-id="cd3aa-109">Key Vault auto rigenera e commuta la chiave attiva in base al periodo di rigenerazione.</span><span class="sxs-lookup"><span data-stu-id="cd3aa-109">Key Vault auto regenerates and switches the active key based on the regeneration period.</span></span>

## <span data-ttu-id="cd3aa-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cd3aa-110">EXAMPLES</span></span>

### <span data-ttu-id="cd3aa-111">Esempio 1: impostare un account di archiviazione di Azure con il Vault chiave per gestire le chiavi</span><span class="sxs-lookup"><span data-stu-id="cd3aa-111">Example 1: Set an Azure Storage Account with Key Vault to manage its keys</span></span>
```
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -ResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount' -ActiveKeyName 'key1' -RegenerationPeriod $regenerationPeriod
```

<span data-ttu-id="cd3aa-112">Imposta un account di archiviazione con Key Vault per consentire la gestione delle chiavi tramite Key Vault.</span><span class="sxs-lookup"><span data-stu-id="cd3aa-112">Sets a Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="cd3aa-113">Il set di tasti attivi è "Key1".</span><span class="sxs-lookup"><span data-stu-id="cd3aa-113">The active key set is 'key1'.</span></span> <span data-ttu-id="cd3aa-114">Questa chiave verrà usata per generare i token SAS.</span><span class="sxs-lookup"><span data-stu-id="cd3aa-114">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="cd3aa-115">Key Vault rigenererà la chiave "key2" dopo il periodo di rigenerazione dall'ora di questo comando e la imposterà come chiave attiva.</span><span class="sxs-lookup"><span data-stu-id="cd3aa-115">Key Vault will regenerate 'key2' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="cd3aa-116">Questo processo di rigenerazione automatica continuerà tra "Key1" e "key2" con una lacuna di 90 giorni.</span><span class="sxs-lookup"><span data-stu-id="cd3aa-116">This auto regeneration process will continue between 'key1' and 'key2' with a gap of 90 days.</span></span>

### <span data-ttu-id="cd3aa-117">Esempio 2: impostare un account di archiviazione di Azure classico con il Vault chiave per gestire le chiavi</span><span class="sxs-lookup"><span data-stu-id="cd3aa-117">Example 2: Set a Classic Azure Storage Account with Key Vault to manage its keys</span></span>
```
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -ResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount' -ActiveKeyName 'Primary' -RegenerationPeriod $regenerationPeriod
```

<span data-ttu-id="cd3aa-118">Imposta un account di archiviazione classico con Key Vault per consentire la gestione delle chiavi tramite Key Vault.</span><span class="sxs-lookup"><span data-stu-id="cd3aa-118">Sets a Classic Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="cd3aa-119">Il set di tasti attivi è "Primary".</span><span class="sxs-lookup"><span data-stu-id="cd3aa-119">The active key set is 'Primary'.</span></span> <span data-ttu-id="cd3aa-120">Questa chiave verrà usata per generare i token SAS.</span><span class="sxs-lookup"><span data-stu-id="cd3aa-120">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="cd3aa-121">Key Vault rigenererà il codice "secondario" dopo il periodo di rigenerazione dall'ora di questo comando e lo imposterà come chiave attiva.</span><span class="sxs-lookup"><span data-stu-id="cd3aa-121">Key Vault will regenerate 'Secondary' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="cd3aa-122">Questo processo di rigenerazione automatica continuerà tra "primario" e "secondario" con una lacuna di 90 giorni.</span><span class="sxs-lookup"><span data-stu-id="cd3aa-122">This auto regeneration process will continue between 'Primary' and 'Secondary' with a gap of 90 days.</span></span>

## <span data-ttu-id="cd3aa-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cd3aa-123">PARAMETERS</span></span>

### <span data-ttu-id="cd3aa-124">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cd3aa-124">-AccountName</span></span>
<span data-ttu-id="cd3aa-125">Nome dell'account di archiviazione gestito Key Vault.</span><span class="sxs-lookup"><span data-stu-id="cd3aa-125">Key Vault managed storage account name.</span></span> <span data-ttu-id="cd3aa-126">Cmdlet crea l'FQDN di un nome di account di archiviazione gestito dal nome del Vault, dall'ambiente selezionato e dal nome dell'account di archiviazione modificato.</span><span class="sxs-lookup"><span data-stu-id="cd3aa-126">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd3aa-127">-AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="cd3aa-127">-AccountResourceId</span></span>
<span data-ttu-id="cd3aa-128">ID risorsa Azure dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cd3aa-128">Azure resource id of the storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountResourceId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd3aa-129">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="cd3aa-129">-ActiveKeyName</span></span>
<span data-ttu-id="cd3aa-130">Nome della chiave dell'account di archiviazione che deve essere usata per la generazione di token SAS.</span><span class="sxs-lookup"><span data-stu-id="cd3aa-130">Name of the storage account key that must be used for generating sas tokens.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd3aa-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd3aa-131">-DefaultProfile</span></span>
<span data-ttu-id="cd3aa-132">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="cd3aa-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd3aa-133">-Disable</span><span class="sxs-lookup"><span data-stu-id="cd3aa-133">-Disable</span></span>
<span data-ttu-id="cd3aa-134">Disabilita l'uso della chiave dell'account di archiviazione gestita per la generazione di token SAS.</span><span class="sxs-lookup"><span data-stu-id="cd3aa-134">Disables the use of managed storage account's key for generation of sas tokens.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd3aa-135">-DisableAutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="cd3aa-135">-DisableAutoRegenerateKey</span></span>
<span data-ttu-id="cd3aa-136">Chiave di rigenerazione automatica.</span><span class="sxs-lookup"><span data-stu-id="cd3aa-136">Auto regenerate key.</span></span> <span data-ttu-id="cd3aa-137">Se true, la chiave inattiva dell'account di archiviazione gestita viene rigenerata automaticamente e diventa la nuova chiave attiva dopo il periodo di rigenerazione.</span><span class="sxs-lookup"><span data-stu-id="cd3aa-137">If true, then the managed storage account's inactive key gets auto regenerated and becomes the new active key after the regeneration period.</span></span> <span data-ttu-id="cd3aa-138">Se false, le chiavi dell'account di archiviazione gestita non vengono rigenerate automaticamente.</span><span class="sxs-lookup"><span data-stu-id="cd3aa-138">If false, then the keys of managed storage account are not auto regenerated.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd3aa-139">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="cd3aa-139">-RegenerationPeriod</span></span>
<span data-ttu-id="cd3aa-140">Periodo di rigenerazione.</span><span class="sxs-lookup"><span data-stu-id="cd3aa-140">Regeneration period.</span></span> <span data-ttu-id="cd3aa-141">Se la chiave di rigenerazione automatica è abilitata, questo valore specifica l'intervallo di valori TimeSpan dopo il quale il tasto inattivo dell'account di archiviazione gestito viene rigenerato automaticamente e diventa la nuova chiave attiva.</span><span class="sxs-lookup"><span data-stu-id="cd3aa-141">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the new active key.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd3aa-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="cd3aa-142">-Tag</span></span>
<span data-ttu-id="cd3aa-143">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="cd3aa-143">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="cd3aa-144">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="cd3aa-144">For example:</span></span>

<span data-ttu-id="cd3aa-145">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="cd3aa-145">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd3aa-146">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="cd3aa-146">-VaultName</span></span>
<span data-ttu-id="cd3aa-147">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="cd3aa-147">Vault name.</span></span>
<span data-ttu-id="cd3aa-148">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="cd3aa-148">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd3aa-149">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cd3aa-149">-Confirm</span></span>
<span data-ttu-id="cd3aa-150">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd3aa-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd3aa-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd3aa-151">-WhatIf</span></span>
<span data-ttu-id="cd3aa-152">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd3aa-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd3aa-153">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd3aa-153">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd3aa-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd3aa-154">CommonParameters</span></span>
<span data-ttu-id="cd3aa-155">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd3aa-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd3aa-156">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd3aa-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd3aa-157">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cd3aa-157">INPUTS</span></span>

### <span data-ttu-id="cd3aa-158">Nessuno</span><span class="sxs-lookup"><span data-stu-id="cd3aa-158">None</span></span>
<span data-ttu-id="cd3aa-159">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="cd3aa-159">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cd3aa-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cd3aa-160">OUTPUTS</span></span>

### <span data-ttu-id="cd3aa-161">Microsoft. Azure. Commands. Vault. Models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd3aa-161">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="cd3aa-162">Note</span><span class="sxs-lookup"><span data-stu-id="cd3aa-162">NOTES</span></span>

## <span data-ttu-id="cd3aa-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cd3aa-163">RELATED LINKS</span></span>

[<span data-ttu-id="cd3aa-164">AzureRM. Vault</span><span class="sxs-lookup"><span data-stu-id="cd3aa-164">AzureRM.KeyVault</span></span>](/powershell/module/azurerm.keyvault)
