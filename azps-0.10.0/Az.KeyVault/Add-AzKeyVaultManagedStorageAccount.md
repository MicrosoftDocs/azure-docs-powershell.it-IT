---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 85a0bc0f552688d036dc76ebbc6d15c608ade433
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863054"
---
# <span data-ttu-id="cef46-101">Add-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cef46-101">Add-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="cef46-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cef46-102">SYNOPSIS</span></span>
<span data-ttu-id="cef46-103">Aggiunge un account di archiviazione di Azure esistente al Vault Key specificato in modo che le chiavi vengano gestite dal servizio Key Vault.</span><span class="sxs-lookup"><span data-stu-id="cef46-103">Adds an existing Azure Storage Account to the specified key vault for its keys to be managed by the Key Vault service.</span></span>

## <span data-ttu-id="cef46-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cef46-104">SYNTAX</span></span>

```
Add-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-AccountResourceId] <String> [-ActiveKeyName] <String> [-DisableAutoRegenerateKey]
 [-RegenerationPeriod <TimeSpan>] [-Disable] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cef46-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cef46-105">DESCRIPTION</span></span>
<span data-ttu-id="cef46-106">Configura un account di archiviazione di Azure esistente con Key Vault per i tasti dell'account di archiviazione da gestire tramite Key Vault.</span><span class="sxs-lookup"><span data-stu-id="cef46-106">Sets up an existing Azure Storage Account with Key Vault for Storage Account keys to be managed by Key Vault.</span></span> <span data-ttu-id="cef46-107">L'account di archiviazione deve già esistere.</span><span class="sxs-lookup"><span data-stu-id="cef46-107">The Storage Account must already exist.</span></span> <span data-ttu-id="cef46-108">Le chiavi di archiviazione non vengono mai esposte al chiamante.</span><span class="sxs-lookup"><span data-stu-id="cef46-108">The Storage Keys are never exposed to caller.</span></span>
<span data-ttu-id="cef46-109">Key Vault auto rigenera e commuta la chiave attiva in base al periodo di rigenerazione.</span><span class="sxs-lookup"><span data-stu-id="cef46-109">Key Vault auto regenerates and switches the active key based on the regeneration period.</span></span>

## <span data-ttu-id="cef46-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cef46-110">EXAMPLES</span></span>

### <span data-ttu-id="cef46-111">Esempio 1: impostare un account di archiviazione di Azure con il Vault chiave per gestire le chiavi</span><span class="sxs-lookup"><span data-stu-id="cef46-111">Example 1: Set an Azure Storage Account with Key Vault to manage its keys</span></span>
```
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -ResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount' -ActiveKeyName 'key1' -RegenerationPeriod $regenerationPeriod
```

<span data-ttu-id="cef46-112">Imposta un account di archiviazione con Key Vault per consentire la gestione delle chiavi tramite Key Vault.</span><span class="sxs-lookup"><span data-stu-id="cef46-112">Sets a Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="cef46-113">Il set di tasti attivi è "Key1".</span><span class="sxs-lookup"><span data-stu-id="cef46-113">The active key set is 'key1'.</span></span> <span data-ttu-id="cef46-114">Questa chiave verrà usata per generare i token SAS.</span><span class="sxs-lookup"><span data-stu-id="cef46-114">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="cef46-115">Key Vault rigenererà la chiave "key2" dopo il periodo di rigenerazione dall'ora di questo comando e la imposterà come chiave attiva.</span><span class="sxs-lookup"><span data-stu-id="cef46-115">Key Vault will regenerate 'key2' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="cef46-116">Questo processo di rigenerazione automatica continuerà tra "Key1" e "key2" con una lacuna di 90 giorni.</span><span class="sxs-lookup"><span data-stu-id="cef46-116">This auto regeneration process will continue between 'key1' and 'key2' with a gap of 90 days.</span></span>

### <span data-ttu-id="cef46-117">Esempio 2: impostare un account di archiviazione di Azure classico con il Vault chiave per gestire le chiavi</span><span class="sxs-lookup"><span data-stu-id="cef46-117">Example 2: Set a Classic Azure Storage Account with Key Vault to manage its keys</span></span>
```
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -ResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount' -ActiveKeyName 'Primary' -RegenerationPeriod $regenerationPeriod
```

<span data-ttu-id="cef46-118">Imposta un account di archiviazione classico con Key Vault per consentire la gestione delle chiavi tramite Key Vault.</span><span class="sxs-lookup"><span data-stu-id="cef46-118">Sets a Classic Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="cef46-119">Il set di tasti attivi è "Primary".</span><span class="sxs-lookup"><span data-stu-id="cef46-119">The active key set is 'Primary'.</span></span> <span data-ttu-id="cef46-120">Questa chiave verrà usata per generare i token SAS.</span><span class="sxs-lookup"><span data-stu-id="cef46-120">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="cef46-121">Key Vault rigenererà il codice "secondario" dopo il periodo di rigenerazione dall'ora di questo comando e lo imposterà come chiave attiva.</span><span class="sxs-lookup"><span data-stu-id="cef46-121">Key Vault will regenerate 'Secondary' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="cef46-122">Questo processo di rigenerazione automatica continuerà tra "primario" e "secondario" con una lacuna di 90 giorni.</span><span class="sxs-lookup"><span data-stu-id="cef46-122">This auto regeneration process will continue between 'Primary' and 'Secondary' with a gap of 90 days.</span></span>

## <span data-ttu-id="cef46-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cef46-123">PARAMETERS</span></span>

### <span data-ttu-id="cef46-124">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cef46-124">-AccountName</span></span>
<span data-ttu-id="cef46-125">Nome dell'account di archiviazione gestito Key Vault.</span><span class="sxs-lookup"><span data-stu-id="cef46-125">Key Vault managed storage account name.</span></span> <span data-ttu-id="cef46-126">Cmdlet crea l'FQDN di un nome di account di archiviazione gestito dal nome del Vault, dall'ambiente selezionato e dal nome dell'account di archiviazione modificato.</span><span class="sxs-lookup"><span data-stu-id="cef46-126">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="cef46-127">-AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="cef46-127">-AccountResourceId</span></span>
<span data-ttu-id="cef46-128">ID risorsa Azure dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cef46-128">Azure resource id of the storage account.</span></span>

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

### <span data-ttu-id="cef46-129">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="cef46-129">-ActiveKeyName</span></span>
<span data-ttu-id="cef46-130">Nome della chiave dell'account di archiviazione che deve essere usata per la generazione di token SAS.</span><span class="sxs-lookup"><span data-stu-id="cef46-130">Name of the storage account key that must be used for generating sas tokens.</span></span>

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

### <span data-ttu-id="cef46-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cef46-131">-DefaultProfile</span></span>
<span data-ttu-id="cef46-132">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="cef46-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef46-133">-Disable</span><span class="sxs-lookup"><span data-stu-id="cef46-133">-Disable</span></span>
<span data-ttu-id="cef46-134">Disabilita l'uso della chiave dell'account di archiviazione gestita per la generazione di token SAS.</span><span class="sxs-lookup"><span data-stu-id="cef46-134">Disables the use of managed storage account's key for generation of sas tokens.</span></span>

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

### <span data-ttu-id="cef46-135">-DisableAutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="cef46-135">-DisableAutoRegenerateKey</span></span>
<span data-ttu-id="cef46-136">Chiave di rigenerazione automatica.</span><span class="sxs-lookup"><span data-stu-id="cef46-136">Auto regenerate key.</span></span> <span data-ttu-id="cef46-137">Se true, la chiave inattiva dell'account di archiviazione gestita viene rigenerata automaticamente e diventa la nuova chiave attiva dopo il periodo di rigenerazione.</span><span class="sxs-lookup"><span data-stu-id="cef46-137">If true, then the managed storage account's inactive key gets auto regenerated and becomes the new active key after the regeneration period.</span></span> <span data-ttu-id="cef46-138">Se false, le chiavi dell'account di archiviazione gestita non vengono rigenerate automaticamente.</span><span class="sxs-lookup"><span data-stu-id="cef46-138">If false, then the keys of managed storage account are not auto regenerated.</span></span>

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

### <span data-ttu-id="cef46-139">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="cef46-139">-RegenerationPeriod</span></span>
<span data-ttu-id="cef46-140">Periodo di rigenerazione.</span><span class="sxs-lookup"><span data-stu-id="cef46-140">Regeneration period.</span></span> <span data-ttu-id="cef46-141">Se la chiave di rigenerazione automatica è abilitata, questo valore specifica l'intervallo di valori TimeSpan dopo il quale il tasto inattivo dell'account di archiviazione gestito viene rigenerato automaticamente e diventa la nuova chiave attiva.</span><span class="sxs-lookup"><span data-stu-id="cef46-141">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the new active key.</span></span>

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

### <span data-ttu-id="cef46-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="cef46-142">-Tag</span></span>
<span data-ttu-id="cef46-143">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="cef46-143">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="cef46-144">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="cef46-144">For example:</span></span>

<span data-ttu-id="cef46-145">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="cef46-145">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="cef46-146">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="cef46-146">-VaultName</span></span>
<span data-ttu-id="cef46-147">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="cef46-147">Vault name.</span></span>
<span data-ttu-id="cef46-148">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="cef46-148">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="cef46-149">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cef46-149">-Confirm</span></span>
<span data-ttu-id="cef46-150">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cef46-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cef46-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cef46-151">-WhatIf</span></span>
<span data-ttu-id="cef46-152">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cef46-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cef46-153">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cef46-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cef46-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cef46-154">CommonParameters</span></span>
<span data-ttu-id="cef46-155">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cef46-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cef46-156">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cef46-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cef46-157">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cef46-157">INPUTS</span></span>

### <span data-ttu-id="cef46-158">Nessuno</span><span class="sxs-lookup"><span data-stu-id="cef46-158">None</span></span>
<span data-ttu-id="cef46-159">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="cef46-159">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cef46-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cef46-160">OUTPUTS</span></span>

### <span data-ttu-id="cef46-161">Microsoft. Azure. Commands. Vault. Models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cef46-161">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="cef46-162">Note</span><span class="sxs-lookup"><span data-stu-id="cef46-162">NOTES</span></span>

## <span data-ttu-id="cef46-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cef46-163">RELATED LINKS</span></span>

[<span data-ttu-id="cef46-164">AZ. Vault</span><span class="sxs-lookup"><span data-stu-id="cef46-164">Az.KeyVault</span></span>](/powershell/module/Az.keyvault)
