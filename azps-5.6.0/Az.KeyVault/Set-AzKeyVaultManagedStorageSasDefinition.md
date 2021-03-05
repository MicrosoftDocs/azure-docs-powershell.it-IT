---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/set-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: b95f47de7fbdcf6b5ed7892cb8deb8656559da27
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991113"
---
# <span data-ttu-id="e0da0-101">Set-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="e0da0-101">Set-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="e0da0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0da0-102">SYNOPSIS</span></span>
<span data-ttu-id="e0da0-103">Imposta una definizione di firma di accesso condiviso con il Vault delle chiavi per un determinato account di archiviazione di Azure gestito dal Vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="e0da0-103">Sets a Shared Access Signature (SAS) definition with Key Vault for a given Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="e0da0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e0da0-104">SYNTAX</span></span>

### <span data-ttu-id="e0da0-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e0da0-105">Default (Default)</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>] -ValidityPeriod <TimeSpan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0da0-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e0da0-106">ByInputObject</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-Name] <String> [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>]
 -ValidityPeriod <TimeSpan> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e0da0-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e0da0-107">DESCRIPTION</span></span>
<span data-ttu-id="e0da0-108">Imposta una definizione di firma di accesso condiviso con un determinato account di archiviazione di Azure gestito dal Vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="e0da0-108">Sets a Shared Access Signature (SAS) definition with a given Key Vault managed Azure Storage Account.</span></span> <span data-ttu-id="e0da0-109">In questo modo viene impostato anche un segreto che può essere usato per ottenere il token di firma di accesso condiviso in base a questa definizione di firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="e0da0-109">This also sets a secret which can be used to get the SAS token per this SAS definition.</span></span>
<span data-ttu-id="e0da0-110">Il token di firma di accesso condiviso viene generato usando questi parametri e la chiave attiva dell'account di archiviazione di Azure gestito da Vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="e0da0-110">SAS token is generated using these parameters and the active key of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="e0da0-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e0da0-111">EXAMPLES</span></span>

### <span data-ttu-id="e0da0-112">Esempio 1: Impostare una definizione di firma di accesso condiviso di tipo account e ottenere un token di firma di accesso condiviso corrente basato su di esso</span><span class="sxs-lookup"><span data-stu-id="e0da0-112">Example 1: Set an account-type SAS definition, and obtain a current SAS token based on it</span></span>
```powershell
PS C:\> $sa = Get-AzStorageAccount -Name mysa -ResourceGroupName myrg
PS C:\> $kv = Get-AzKeyVault -VaultName mykv
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName $kv.VaultName -AccountName $sa.StorageAccountName -AccountResourceId $sa.Id -ActiveKeyName key1 -RegenerationPeriod ([System.Timespan]::FromDays(180))
PS C:\> $sctx = New-AzStorageContext -StorageAccountName $sa.StorageAccountName -Protocol Https -StorageAccountKey Key1
PS C:\> $start = [System.DateTime]::Now.AddDays(-1)
PS C:\> $end = [System.DateTime]::Now.AddMonths(1)
PS C:\> $at = New-AzStorageAccountSasToken -Service blob,file,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -StartTime $start -ExpiryTime $end -Context $sctx
PS C:\> $sas = Set-AzKeyVaultManagedStorageSasDefinition -AccountName $sa.StorageAccountName -VaultName $kv.VaultName -Name accountsas -TemplateUri $at -SasType 'account' -ValidityPeriod ([System.Timespan]::FromDays(30))
PS C:\> Get-AzKeyVaultSecret -VaultName $kv.VaultName -Name $sas.Sid.Substring($sas.Sid.LastIndexOf('/')+1)
```

<span data-ttu-id="e0da0-113">Imposta una definizione di firma di accesso condiviso dell'account "accountsas" in un account di archiviazione gestito da KeyVault 'mysa' nel vault 'mykv'.</span><span class="sxs-lookup"><span data-stu-id="e0da0-113">Sets an account SAS definition 'accountsas' on a KeyVault-managed storage account 'mysa' in vault 'mykv'.</span></span> <span data-ttu-id="e0da0-114">In particolare, la sequenza precedente esegue le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="e0da0-114">Specifically, the sequence above performs the following:</span></span>
  - <span data-ttu-id="e0da0-115">ottiene un account di archiviazione (pre-esistente)</span><span class="sxs-lookup"><span data-stu-id="e0da0-115">gets a (pre-existing) storage account</span></span>
  - <span data-ttu-id="e0da0-116">ottiene un vault delle chiavi (pre-esistente)</span><span class="sxs-lookup"><span data-stu-id="e0da0-116">gets a (pre-existing) key vault</span></span>
  - <span data-ttu-id="e0da0-117">aggiunge un account di archiviazione gestito da KeyVault al Vault, impostando Key1 come chiave attiva e con un periodo di rigenerazione di 180 giorni</span><span class="sxs-lookup"><span data-stu-id="e0da0-117">adds a KeyVault-managed storage account to the vault, setting Key1 as the active key, and with a regeneration period of 180 days</span></span>
  - <span data-ttu-id="e0da0-118">imposta un contesto di archiviazione per l'account di archiviazione specificato, con Key1</span><span class="sxs-lookup"><span data-stu-id="e0da0-118">sets a storage context for the specified storage account, with Key1</span></span>
  - <span data-ttu-id="e0da0-119">crea un token di firma di accesso condiviso dell'account per BLOB, file, tabella e coda dei servizi per i tipi di risorse Servizio, Contenitore e Oggetto, con tutte le autorizzazioni, su https e con le date di inizio e di fine specificate</span><span class="sxs-lookup"><span data-stu-id="e0da0-119">creates an account SAS token for services Blob, File, Table and Queue, for resource types Service, Container and Object, with all permissions, over https and with the specified start and end dates</span></span>
  - <span data-ttu-id="e0da0-120">imposta una definizione di firma di accesso condiviso gestita da KeyVault nel vault, con l'URI modello come token di firma di accesso condiviso creato sopra, di tipo saS 'account' e valido per 30 giorni</span><span class="sxs-lookup"><span data-stu-id="e0da0-120">sets a KeyVault-managed storage SAS definition in the vault, with the template uri as the SAS token created above, of SAS type 'account' and valid for 30 days</span></span>
  - <span data-ttu-id="e0da0-121">recupera il token di accesso effettivo dal segreto KeyVault corrispondente alla definizione di firma di accesso condiviso</span><span class="sxs-lookup"><span data-stu-id="e0da0-121">retrieves the actual access token from the KeyVault secret corresponding to the SAS definition</span></span>

## <span data-ttu-id="e0da0-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0da0-122">PARAMETERS</span></span>

### <span data-ttu-id="e0da0-123">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e0da0-123">-AccountName</span></span>
<span data-ttu-id="e0da0-124">Nome dell'account di archiviazione gestito dal Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="e0da0-124">Key Vault managed storage account name.</span></span> <span data-ttu-id="e0da0-125">Il cmdlet crea l'FQDN di un account di archiviazione gestito dal nome del vault, dall'ambiente attualmente selezionato e dal nome dell'account di archiviazione gestito.</span><span class="sxs-lookup"><span data-stu-id="e0da0-125">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="e0da0-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0da0-126">-DefaultProfile</span></span>
<span data-ttu-id="e0da0-127">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e0da0-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0da0-128">-Disable</span><span class="sxs-lookup"><span data-stu-id="e0da0-128">-Disable</span></span>
<span data-ttu-id="e0da0-129">Disabilita l'uso della definizione sas per la generazione di token sas.</span><span class="sxs-lookup"><span data-stu-id="e0da0-129">Disables the use of sas definition for generation of sas token.</span></span>

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

### <span data-ttu-id="e0da0-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0da0-130">-InputObject</span></span>
<span data-ttu-id="e0da0-131">Oggetto ManagedStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="e0da0-131">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="e0da0-132">-Name</span><span class="sxs-lookup"><span data-stu-id="e0da0-132">-Name</span></span>
<span data-ttu-id="e0da0-133">Nome della definizione della firma di accesso condiviso per l'archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e0da0-133">Storage sas definition name.</span></span> <span data-ttu-id="e0da0-134">Il cmdlet crea l'FQDN di una definizione di firma di accesso condiviso per l'archiviazione dal nome del vault, dall'ambiente attualmente selezionato, dal nome dell'account di archiviazione e dal nome della definizione della firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="e0da0-134">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

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

### <span data-ttu-id="e0da0-135">-SasType</span><span class="sxs-lookup"><span data-stu-id="e0da0-135">-SasType</span></span>
<span data-ttu-id="e0da0-136">Tipo di firma di accesso condiviso per l'archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e0da0-136">Storage SAS type.</span></span>

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

### <span data-ttu-id="e0da0-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="e0da0-137">-Tag</span></span>
<span data-ttu-id="e0da0-138">Coppie chiave-valore sotto forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="e0da0-138">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e0da0-139">Ad esempio: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="e0da0-139">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e0da0-140">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="e0da0-140">-TemplateUri</span></span>
<span data-ttu-id="e0da0-141">URI del modello della definizione della firma di accesso condiviso per l'archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e0da0-141">Storage SAS definition template uri.</span></span>

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

### <span data-ttu-id="e0da0-142">-ValidityPeriod</span><span class="sxs-lookup"><span data-stu-id="e0da0-142">-ValidityPeriod</span></span>
<span data-ttu-id="e0da0-143">Periodo di validità che verrà usato per impostare il tempo di scadenza del token sas dalla data in cui viene generato</span><span class="sxs-lookup"><span data-stu-id="e0da0-143">Validity period that will get used to set the expiry time of sas token from the time it gets generated</span></span>

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

### <span data-ttu-id="e0da0-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e0da0-144">-VaultName</span></span>
<span data-ttu-id="e0da0-145">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="e0da0-145">Vault name.</span></span>
<span data-ttu-id="e0da0-146">Il cmdlet crea l'FQDN di un vault in base al nome e all'ambiente attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="e0da0-146">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="e0da0-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e0da0-147">-Confirm</span></span>
<span data-ttu-id="e0da0-148">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0da0-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0da0-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0da0-149">-WhatIf</span></span>
<span data-ttu-id="e0da0-150">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e0da0-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0da0-151">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e0da0-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0da0-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0da0-152">CommonParameters</span></span>
<span data-ttu-id="e0da0-153">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0da0-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0da0-154">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e0da0-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0da0-155">INPUT</span><span class="sxs-lookup"><span data-stu-id="e0da0-155">INPUTS</span></span>

### <span data-ttu-id="e0da0-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="e0da0-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="e0da0-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e0da0-157">OUTPUTS</span></span>

### <span data-ttu-id="e0da0-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="e0da0-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="e0da0-159">NOTE</span><span class="sxs-lookup"><span data-stu-id="e0da0-159">NOTES</span></span>

## <span data-ttu-id="e0da0-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e0da0-160">RELATED LINKS</span></span>

[<span data-ttu-id="e0da0-161">Azureâ€\RM.â€"Keyâ€-Vault</span><span class="sxs-lookup"><span data-stu-id="e0da0-161">Azureâ€‹RM.â€‹Keyâ€‹Vault</span></span>](/powershell/module/az.keyvault/)
