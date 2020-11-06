---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: a71aed4703158c68d3b156ff1e37d438e5413782
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513799"
---
# <span data-ttu-id="b3ae4-101">Set-AzureKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="b3ae4-101">Set-AzureKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="b3ae4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b3ae4-102">SYNOPSIS</span></span>
<span data-ttu-id="b3ae4-103">Imposta la definizione di una firma di accesso condiviso con Key Vault per un account di archiviazione di Azure Key in un archivio chiave specifico.</span><span class="sxs-lookup"><span data-stu-id="b3ae4-103">Sets a Shared Access Signature (SAS) definition with Key Vault for a given Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3ae4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b3ae4-104">SYNTAX</span></span>

### <span data-ttu-id="b3ae4-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b3ae4-105">Default (Default)</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>] -ValidityPeriod <TimeSpan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3ae4-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b3ae4-106">ByInputObject</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-Name] <String> [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>]
 -ValidityPeriod <TimeSpan> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b3ae4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3ae4-107">DESCRIPTION</span></span>
<span data-ttu-id="b3ae4-108">Imposta una definizione di una firma di accesso condiviso (SAS) con un account di archiviazione di Azure Key in un archivio chiave specifico.</span><span class="sxs-lookup"><span data-stu-id="b3ae4-108">Sets a Shared Access Signature (SAS) definition with a given Key Vault managed Azure Storage Account.</span></span> <span data-ttu-id="b3ae4-109">Questo imposta anche un segreto che può essere usato per ottenere il token SAS per la definizione SAS.</span><span class="sxs-lookup"><span data-stu-id="b3ae4-109">This also sets a secret which can be used to get the SAS token per this SAS definition.</span></span>
<span data-ttu-id="b3ae4-110">Il token SAS viene generato usando questi parametri e la chiave attiva dell'account di archiviazione di Azure Key Vault Managed.</span><span class="sxs-lookup"><span data-stu-id="b3ae4-110">SAS token is generated using these parameters and the active key of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="b3ae4-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b3ae4-111">EXAMPLES</span></span>

### <span data-ttu-id="b3ae4-112">Esempio 1: impostare una definizione SAS di tipo account e ottenere un token SAS corrente basato su</span><span class="sxs-lookup"><span data-stu-id="b3ae4-112">Example 1 : Set an account-type SAS definition, and obtain a current SAS token based on it</span></span>
```powershell
PS C:\> $sa = Get-AzureRmStorageAccount -Name mysa -ResourceGroupName myrg
PS C:\> $kv = Get-AzureRmKeyVault -VaultName mykv
PS C:\> Add-AzureKeyVaultManagedStorageAccount -VaultName $kv.VaultName -AccountName $sa.StorageAccountName -AccountResourceId $sa.Id -ActiveKeyName key1 -RegenerationPeriod 180
PS C:\> $sctx = New-AzureStorageContext -StorageAccountName $sa.StorageAccountName -Protocol Https -StorageAccountKey Key1
PS C:\> $start = [System.DateTime]::Now.AddDays(-1)
PS C:\> $end = [System.DateTime]::Now.AddMonths(1)
PS C:\> $at = New-AzureStorageAccountSasToken -Service blob,file,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -StartTime $start -ExpiryTime $end -Context $sctx
PS C:\> $sas = Set-AzureKeyVaultManagedStorageSasDefinition -AccountName $sa.StorageAccountName -VaultName $kv.VaultName -Name accountsas -TemplateUri $at -SasType 'account' -ValidityPeriod ([System.Timespan]::FromDays(30))
PS C:\> Get-AzureKeyVaultSecret -VaultName $kv.VaultName -Name $sas.Sid.Substring($sas.Sid.LastIndexOf('/')+1)
```

<span data-ttu-id="b3ae4-113">Imposta un account di definizione SAS "Accounts" in un account di archiviazione gestito da un Mysa in un caveau "mykv".</span><span class="sxs-lookup"><span data-stu-id="b3ae4-113">Sets an account SAS definition 'accountsas' on a KeyVault-managed storage account 'mysa' in vault 'mykv'.</span></span> <span data-ttu-id="b3ae4-114">In particolare, la sequenza precedente esegue le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="b3ae4-114">Specifically, the sequence above performs the following:</span></span>
  - <span data-ttu-id="b3ae4-115">Ottiene un account di archiviazione (preesistente)</span><span class="sxs-lookup"><span data-stu-id="b3ae4-115">gets a (pre-existing) storage account</span></span>
  - <span data-ttu-id="b3ae4-116">Ottiene un Vault della chiave (preesistente)</span><span class="sxs-lookup"><span data-stu-id="b3ae4-116">gets a (pre-existing) key vault</span></span>
  - <span data-ttu-id="b3ae4-117">aggiunge un account di archiviazione gestito da Key Vault al Vault, impostando Key1 come chiave attiva e con un periodo di rigenerazione di 180 giorni</span><span class="sxs-lookup"><span data-stu-id="b3ae4-117">adds a KeyVault-managed storage account to the vault, setting Key1 as the active key, and with a regeneration period of 180 days</span></span>
  - <span data-ttu-id="b3ae4-118">imposta un contesto di archiviazione per l'account di archiviazione specificato, con Key1</span><span class="sxs-lookup"><span data-stu-id="b3ae4-118">sets a storage context for the specified storage account, with Key1</span></span>
  - <span data-ttu-id="b3ae4-119">Crea un token SAS per l'account per i servizi BLOB, file, tabelle e code, per i tipi di risorse, il contenitore e l'oggetto, con tutte le autorizzazioni, tramite HTTPS e le date di inizio e di fine specificate</span><span class="sxs-lookup"><span data-stu-id="b3ae4-119">creates an account SAS token for services Blob, File, Table and Queue, for resource types Service, Container and Object, with all permissions, over https and with the specified start and end dates</span></span>
  - <span data-ttu-id="b3ae4-120">imposta una definizione SAS di archiviazione gestita da un Vault nel Vault, con l'URI del modello come token SAS creato in precedenza, di tipo SAS "account" e valido per 30 giorni</span><span class="sxs-lookup"><span data-stu-id="b3ae4-120">sets a KeyVault-managed storage SAS definition in the vault, with the template uri as the SAS token created above, of SAS type 'account' and valid for 30 days</span></span>
  - <span data-ttu-id="b3ae4-121">Recupera il token di accesso effettivo dal segreto del Vault, corrispondente alla definizione SAS</span><span class="sxs-lookup"><span data-stu-id="b3ae4-121">retrieves the actual access token from the KeyVault secret corresponding to the SAS definition</span></span>

## <span data-ttu-id="b3ae4-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b3ae4-122">PARAMETERS</span></span>

### <span data-ttu-id="b3ae4-123">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b3ae4-123">-AccountName</span></span>
<span data-ttu-id="b3ae4-124">Nome dell'account di archiviazione gestito Key Vault.</span><span class="sxs-lookup"><span data-stu-id="b3ae4-124">Key Vault managed storage account name.</span></span> <span data-ttu-id="b3ae4-125">Cmdlet crea l'FQDN di un nome di account di archiviazione gestito dal nome del Vault, dall'ambiente selezionato e dal nome dell'account di archiviazione modificato.</span><span class="sxs-lookup"><span data-stu-id="b3ae4-125">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3ae4-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3ae4-126">-DefaultProfile</span></span>
<span data-ttu-id="b3ae4-127">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b3ae4-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3ae4-128">-Disable</span><span class="sxs-lookup"><span data-stu-id="b3ae4-128">-Disable</span></span>
<span data-ttu-id="b3ae4-129">Disabilita l'uso della definizione SAS per la generazione di token SAS.</span><span class="sxs-lookup"><span data-stu-id="b3ae4-129">Disables the use of sas definition for generation of sas token.</span></span>

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

### <span data-ttu-id="b3ae4-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3ae4-130">-InputObject</span></span>
<span data-ttu-id="b3ae4-131">Oggetto ManagedStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="b3ae4-131">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="b3ae4-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="b3ae4-132">-Name</span></span>
<span data-ttu-id="b3ae4-133">Nome della definizione di archiviazione SAS.</span><span class="sxs-lookup"><span data-stu-id="b3ae4-133">Storage sas definition name.</span></span> <span data-ttu-id="b3ae4-134">Cmdlet costruisce il nome di dominio completo di una definizione SAS di archiviazione dal nome della volta, dall'ambiente attualmente selezionato, dal nome dell'account di archiviazione e dalla definizione SAS.</span><span class="sxs-lookup"><span data-stu-id="b3ae4-134">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3ae4-135">-SasType</span><span class="sxs-lookup"><span data-stu-id="b3ae4-135">-SasType</span></span>
<span data-ttu-id="b3ae4-136">Tipo SAS di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="b3ae4-136">Storage SAS type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3ae4-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="b3ae4-137">-Tag</span></span>
<span data-ttu-id="b3ae4-138">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="b3ae4-138">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b3ae4-139">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="b3ae4-139">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3ae4-140">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="b3ae4-140">-TemplateUri</span></span>
<span data-ttu-id="b3ae4-141">URI del modello di definizione SAS di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="b3ae4-141">Storage SAS definition template uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3ae4-142">-ValidityPeriod</span><span class="sxs-lookup"><span data-stu-id="b3ae4-142">-ValidityPeriod</span></span>
<span data-ttu-id="b3ae4-143">Periodo di validità che verrà usato per impostare l'ora di scadenza del token SAS dal momento in cui viene generato</span><span class="sxs-lookup"><span data-stu-id="b3ae4-143">Validity period that will get used to set the expiry time of sas token from the time it gets generated</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3ae4-144">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="b3ae4-144">-VaultName</span></span>
<span data-ttu-id="b3ae4-145">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="b3ae4-145">Vault name.</span></span>
<span data-ttu-id="b3ae4-146">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="b3ae4-146">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3ae4-147">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b3ae4-147">-Confirm</span></span>
<span data-ttu-id="b3ae4-148">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3ae4-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3ae4-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3ae4-149">-WhatIf</span></span>
<span data-ttu-id="b3ae4-150">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b3ae4-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3ae4-151">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b3ae4-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3ae4-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3ae4-152">CommonParameters</span></span>
<span data-ttu-id="b3ae4-153">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3ae4-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3ae4-154">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3ae4-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3ae4-155">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b3ae4-155">INPUTS</span></span>

### <span data-ttu-id="b3ae4-156">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="b3ae4-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>
<span data-ttu-id="b3ae4-157">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b3ae4-157">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="b3ae4-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b3ae4-158">OUTPUTS</span></span>

### <span data-ttu-id="b3ae4-159">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="b3ae4-159">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="b3ae4-160">Note</span><span class="sxs-lookup"><span data-stu-id="b3ae4-160">NOTES</span></span>

## <span data-ttu-id="b3ae4-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b3ae4-161">RELATED LINKS</span></span>

[<span data-ttu-id="b3ae4-162">Azureâ € ‹ RM. â € ‹ keyâ € ‹ volta</span><span class="sxs-lookup"><span data-stu-id="b3ae4-162">Azureâ€‹RM.â€‹Keyâ€‹Vault</span></span>](/powershell/module/azurerm.keyvault/)