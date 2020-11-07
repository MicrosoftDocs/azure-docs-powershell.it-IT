---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 5a4c1effd1cbda4399e06f3b6db606cff87d8955
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688169"
---
# <span data-ttu-id="5b4c2-101">Set-AzureKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="5b4c2-101">Set-AzureKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="5b4c2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5b4c2-102">SYNOPSIS</span></span>
<span data-ttu-id="5b4c2-103">Imposta la definizione di una firma di accesso condiviso con Key Vault per un account di archiviazione di Azure Key in un archivio chiave specifico.</span><span class="sxs-lookup"><span data-stu-id="5b4c2-103">Sets a Shared Access Signature (SAS) definition with Key Vault for a given Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b4c2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5b4c2-104">SYNTAX</span></span>

### <span data-ttu-id="5b4c2-105">RawSas (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5b4c2-105">RawSas (Default)</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Parameter] <Hashtable> [-Disable] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b4c2-106">AdhocAccountSas</span><span class="sxs-lookup"><span data-stu-id="5b4c2-106">AdhocAccountSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition -Service <String[]> -ResourceType <String[]>
 [-ApiVersion <String>] [-VaultName] <String> [-AccountName] <String> [-Name] <String> [-Disable]
 [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>] [-IPAddressOrRange <String>]
 -ValidityPeriod <TimeSpan> -Permission <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b4c2-107">AdhocServiceBlobSas</span><span class="sxs-lookup"><span data-stu-id="5b4c2-107">AdhocServiceBlobSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]> -Blob <String>
 -Container <String> [-SharedAccessHeader <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b4c2-108">AdhocServiceContainerSas</span><span class="sxs-lookup"><span data-stu-id="5b4c2-108">AdhocServiceContainerSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]> -Container <String>
 [-SharedAccessHeader <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5b4c2-109">AdhocServiceFileSas</span><span class="sxs-lookup"><span data-stu-id="5b4c2-109">AdhocServiceFileSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]>
 [-SharedAccessHeader <String[]>] -Share <String> -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b4c2-110">AdhocServiceShareSas</span><span class="sxs-lookup"><span data-stu-id="5b4c2-110">AdhocServiceShareSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]>
 [-SharedAccessHeader <String[]>] -Share <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b4c2-111">AdhocServiceQueueSas</span><span class="sxs-lookup"><span data-stu-id="5b4c2-111">AdhocServiceQueueSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]> -Queue <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b4c2-112">AdhocServiceTableSas</span><span class="sxs-lookup"><span data-stu-id="5b4c2-112">AdhocServiceTableSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]> -Table <String>
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b4c2-113">StoredPolicyServiceBlobSas</span><span class="sxs-lookup"><span data-stu-id="5b4c2-113">StoredPolicyServiceBlobSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Blob <String> -Container <String> -Policy <String>
 [-SharedAccessHeader <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5b4c2-114">StoredPolicyServiceContainerSas</span><span class="sxs-lookup"><span data-stu-id="5b4c2-114">StoredPolicyServiceContainerSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Container <String> -Policy <String> [-SharedAccessHeader <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b4c2-115">StoredPolicyServiceFileSas</span><span class="sxs-lookup"><span data-stu-id="5b4c2-115">StoredPolicyServiceFileSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Policy <String> [-SharedAccessHeader <String[]>] -Share <String> -Path <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b4c2-116">StoredPolicyServiceShareSas</span><span class="sxs-lookup"><span data-stu-id="5b4c2-116">StoredPolicyServiceShareSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Policy <String> [-SharedAccessHeader <String[]>] -Share <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b4c2-117">StoredPolicyServiceQueueSas</span><span class="sxs-lookup"><span data-stu-id="5b4c2-117">StoredPolicyServiceQueueSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Policy <String> -Queue <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b4c2-118">StoredPolicyServiceTableSas</span><span class="sxs-lookup"><span data-stu-id="5b4c2-118">StoredPolicyServiceTableSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Policy <String> -Table <String> [-StartPartitionKey <String>]
 [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b4c2-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5b4c2-119">DESCRIPTION</span></span>
<span data-ttu-id="5b4c2-120">Imposta una definizione di una firma di accesso condiviso (SAS) con un account di archiviazione di Azure Key in un archivio chiave specifico.</span><span class="sxs-lookup"><span data-stu-id="5b4c2-120">Sets a Shared Access Signature (SAS) definition with a given Key Vault managed Azure Storage Account.</span></span> <span data-ttu-id="5b4c2-121">Questo imposta anche un segreto che può essere usato per ottenere il token SAS per la definizione SAS.</span><span class="sxs-lookup"><span data-stu-id="5b4c2-121">This also sets a secret which can be used to get the SAS token per this SAS definition.</span></span>
<span data-ttu-id="5b4c2-122">Il token SAS viene generato usando questi parametri e la chiave attiva dell'account di archiviazione di Azure Key Vault Managed.</span><span class="sxs-lookup"><span data-stu-id="5b4c2-122">SAS token is generated using these parameters and the active key of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="5b4c2-123">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5b4c2-123">EXAMPLES</span></span>

### <span data-ttu-id="5b4c2-124">Esempio 1: impostare una definizione SAS Blob Service ad hoc</span><span class="sxs-lookup"><span data-stu-id="5b4c2-124">Example 1 : Set an ad hoc service Blob sas definition</span></span>
```
PS C:\> Set-AzureKeyVaultManagedStorageSasDefinition -Blob 'blob1' -Container 'container1' -VaultName 'vault1' -AccountName 'account1' -Name 'sas1' -ValidityPeriod ([System.Timespan]::FromDays(30)) -Permission Read,Add -SharedAccessHeader CacheControl,ContentDisposition -Protocol HttpsOnly -IPAddressOrRange '168.1.5.60-168.1.5.70'
```

<span data-ttu-id="5b4c2-125">Imposta una definizione SAS BLOB di servizi ad hoc "SAS1" con l'account di archiviazione gestita Key Vault "conto1" in Vault "vault1".</span><span class="sxs-lookup"><span data-stu-id="5b4c2-125">Sets an ad hoc service blob sas definition 'sas1' with key vault managed storage account 'account1' in vault 'vault1'.</span></span>

### <span data-ttu-id="5b4c2-126">Esempio 2: impostare una definizione di un account ad hoc SAS</span><span class="sxs-lookup"><span data-stu-id="5b4c2-126">Example 2 : Set an ad hoc account sas definition</span></span>
```
PS C:\> Set-AzureKeyVaultManagedStorageSasDefinition -Service Blob,File -ResourceType Container,Service -VaultName 'vault1' -AccountName 'account1' -Name 'sas1' -Protocol HttpsOrHttp -IPAddressOrRange '168.1.5.60' -ValidityPeriod ([System.Timespan]::FromDays(30)) -Permission Read,Add
```

<span data-ttu-id="5b4c2-127">Imposta una definizione SAS BLOB ad hoc "SAS1" con l'account di archiviazione gestita Key Vault "conto1" in Vault "vault1".</span><span class="sxs-lookup"><span data-stu-id="5b4c2-127">Sets an ad hoc blob sas definition 'sas1' with key vault managed storage account 'account1' in vault 'vault1'.</span></span>

### <span data-ttu-id="5b4c2-128">Esempio 3: impostare una definizione SAS tramite una tabella hash</span><span class="sxs-lookup"><span data-stu-id="5b4c2-128">Example 3 : Set a sas definition using a hashtable</span></span>
```
PS C:\> $parameters = @{"sasType"="blob";"signedVersion"="2016-05-31";"signedProtocols"="https";"signedIp"="168.1.5.60-168.1.5.70";"validityPeriod"="P30D";"signedPermissions"="ra";"blobName"="blob1";"containerName"="container1";"rscd"="";"rscc"=""}
PS C:\> Set-AzureKeyVaultManagedStorageSasDefinition -VaultName vault1 -AccountName account1 -Name sas1 -Parameter $parameters
```

<span data-ttu-id="5b4c2-129">Imposta una definizione SAS BLOB ad hoc "SAS1" con l'account di archiviazione gestita Key Vault "conto1" in Vault "vault1" con una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="5b4c2-129">Sets an ad hoc blob sas definition 'sas1' with key vault managed storage account 'account1' in vault 'vault1' using a hashtable.</span></span>

## <span data-ttu-id="5b4c2-130">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5b4c2-130">PARAMETERS</span></span>

### <span data-ttu-id="5b4c2-131">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5b4c2-131">-AccountName</span></span>
<span data-ttu-id="5b4c2-132">Nome dell'account di archiviazione gestito Key Vault.</span><span class="sxs-lookup"><span data-stu-id="5b4c2-132">Key Vault managed storage account name.</span></span> <span data-ttu-id="5b4c2-133">Cmdlet crea l'FQDN di un nome di account di archiviazione gestito dal nome del Vault, dall'ambiente selezionato e dal nome dell'account di archiviazione modificato.</span><span class="sxs-lookup"><span data-stu-id="5b4c2-133">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b4c2-134">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5b4c2-134">-ApiVersion</span></span>
<span data-ttu-id="5b4c2-135">Specifica la versione del servizio di archiviazione da usare per eseguire la richiesta effettuata con l'URI di SAS dell'account.</span><span class="sxs-lookup"><span data-stu-id="5b4c2-135">Specifies the storage service version to use to execute the request made using the account SAS URI.</span></span>

```yaml
Type: String
Parameter Sets: AdhocAccountSas
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4c2-136">-BLOB</span><span class="sxs-lookup"><span data-stu-id="5b4c2-136">-Blob</span></span>
<span data-ttu-id="5b4c2-137">Nome BLOB</span><span class="sxs-lookup"><span data-stu-id="5b4c2-137">Blob Name</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceBlobSas, StoredPolicyServiceBlobSas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4c2-138">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="5b4c2-138">-Container</span></span>
<span data-ttu-id="5b4c2-139">Nome contenitore</span><span class="sxs-lookup"><span data-stu-id="5b4c2-139">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceBlobSas, AdhocServiceContainerSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4c2-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b4c2-140">-DefaultProfile</span></span>
<span data-ttu-id="5b4c2-141">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5b4c2-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5b4c2-142">-Disable</span><span class="sxs-lookup"><span data-stu-id="5b4c2-142">-Disable</span></span>
<span data-ttu-id="5b4c2-143">Disabilita l'uso della definizione SAS per la generazione di token SAS.</span><span class="sxs-lookup"><span data-stu-id="5b4c2-143">Disables the use of sas definition for generation of sas token.</span></span>

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

### <span data-ttu-id="5b4c2-144">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="5b4c2-144">-EndPartitionKey</span></span>
<span data-ttu-id="5b4c2-145">Chiave di partizione finale</span><span class="sxs-lookup"><span data-stu-id="5b4c2-145">End Partition Key</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: endpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4c2-146">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="5b4c2-146">-EndRowKey</span></span>
<span data-ttu-id="5b4c2-147">Tasto fine riga</span><span class="sxs-lookup"><span data-stu-id="5b4c2-147">End Row Key</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: endrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4c2-148">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="5b4c2-148">-IPAddressOrRange</span></span>
<span data-ttu-id="5b4c2-149">ACL IP o IP Range (elenco di controllo di accesso) della richiesta che verrebbe accettata da Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="5b4c2-149">IP, or IP range ACL (access control list) of the request that would be accepted by Azure Storage.</span></span>

```yaml
Type: String
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas, StoredPolicyServiceQueueSas, StoredPolicyServiceTableSas
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4c2-150">-Nome</span><span class="sxs-lookup"><span data-stu-id="5b4c2-150">-Name</span></span>
<span data-ttu-id="5b4c2-151">Nome della definizione di archiviazione SAS.</span><span class="sxs-lookup"><span data-stu-id="5b4c2-151">Storage sas definition name.</span></span> <span data-ttu-id="5b4c2-152">Cmdlet costruisce il nome di dominio completo di una definizione SAS di archiviazione dal nome della volta, dall'ambiente attualmente selezionato, dal nome dell'account di archiviazione e dalla definizione SAS.</span><span class="sxs-lookup"><span data-stu-id="5b4c2-152">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b4c2-153">Parametro-</span><span class="sxs-lookup"><span data-stu-id="5b4c2-153">-Parameter</span></span>
<span data-ttu-id="5b4c2-154">Parametri di definizione SAS che verranno usati per creare il token SAS.</span><span class="sxs-lookup"><span data-stu-id="5b4c2-154">Sas definition parameters that will be used to create the sas token.</span></span>

```yaml
Type: Hashtable
Parameter Sets: RawSas
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b4c2-155">-Path</span><span class="sxs-lookup"><span data-stu-id="5b4c2-155">-Path</span></span>
<span data-ttu-id="5b4c2-156">Percorso del file cloud in cui generare il token SAS.</span><span class="sxs-lookup"><span data-stu-id="5b4c2-156">Path to the cloud file to generate sas token against.</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceFileSas, StoredPolicyServiceFileSas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4c2-157">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="5b4c2-157">-Permission</span></span>
<span data-ttu-id="5b4c2-158">Autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="5b4c2-158">Permission.</span></span> <span data-ttu-id="5b4c2-159">I valori includono "query", "Add", "Update", "Process"</span><span class="sxs-lookup"><span data-stu-id="5b4c2-159">Values include 'Query','Add','Update','Process'</span></span>

```yaml
Type: String[]
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas
Aliases:
Accepted values: Add, Create, Delete, List, Process, Read, Query, Update, Write

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4c2-160">-Policy</span><span class="sxs-lookup"><span data-stu-id="5b4c2-160">-Policy</span></span>
<span data-ttu-id="5b4c2-161">Identificatore dei criteri</span><span class="sxs-lookup"><span data-stu-id="5b4c2-161">Policy Identifier</span></span>

```yaml
Type: String
Parameter Sets: StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas, StoredPolicyServiceQueueSas, StoredPolicyServiceTableSas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4c2-162">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="5b4c2-162">-Protocol</span></span>
<span data-ttu-id="5b4c2-163">Il protocollo può essere usato nella richiesta con il token SAS.</span><span class="sxs-lookup"><span data-stu-id="5b4c2-163">Protocol can be used in the request with the SAS token.</span></span>

```yaml
Type: String
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas, StoredPolicyServiceQueueSas, StoredPolicyServiceTableSas
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4c2-164">-Queue</span><span class="sxs-lookup"><span data-stu-id="5b4c2-164">-Queue</span></span>
<span data-ttu-id="5b4c2-165">Nome coda</span><span class="sxs-lookup"><span data-stu-id="5b4c2-165">Queue Name</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceQueueSas, StoredPolicyServiceQueueSas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4c2-166">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="5b4c2-166">-ResourceType</span></span>
<span data-ttu-id="5b4c2-167">Tipi di risorsa a cui si applica questo token SAS.</span><span class="sxs-lookup"><span data-stu-id="5b4c2-167">Resource types that this SAS token applies to.</span></span> <span data-ttu-id="5b4c2-168">I valori includono "servizio", "contenitore", "oggetto"</span><span class="sxs-lookup"><span data-stu-id="5b4c2-168">Values include 'Service','Container','Object'</span></span>

```yaml
Type: String[]
Parameter Sets: AdhocAccountSas
Aliases:
Accepted values: Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4c2-169">-Servizio</span><span class="sxs-lookup"><span data-stu-id="5b4c2-169">-Service</span></span>
<span data-ttu-id="5b4c2-170">Tipi di servizio a cui si applica questo token SAS.</span><span class="sxs-lookup"><span data-stu-id="5b4c2-170">Service types that this SAS token applies to.</span></span> <span data-ttu-id="5b4c2-171">I valori includono "blob", "file", "Queue", "Table"</span><span class="sxs-lookup"><span data-stu-id="5b4c2-171">Values include 'Blob','File','Queue','Table'</span></span>

```yaml
Type: String[]
Parameter Sets: AdhocAccountSas
Aliases:
Accepted values: Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4c2-172">-Condividi</span><span class="sxs-lookup"><span data-stu-id="5b4c2-172">-Share</span></span>
<span data-ttu-id="5b4c2-173">Nome condivisione</span><span class="sxs-lookup"><span data-stu-id="5b4c2-173">Share Name</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceFileSas, AdhocServiceShareSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4c2-174">-SharedAccessHeader</span><span class="sxs-lookup"><span data-stu-id="5b4c2-174">-SharedAccessHeader</span></span>
<span data-ttu-id="5b4c2-175">Specifica i parametri di query per ignorare le intestazioni di risposta.</span><span class="sxs-lookup"><span data-stu-id="5b4c2-175">Specifies the query parameters to override response headers.</span></span>

```yaml
Type: String[]
Parameter Sets: AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas
Aliases:
Accepted values: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentType

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4c2-176">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="5b4c2-176">-StartPartitionKey</span></span>
<span data-ttu-id="5b4c2-177">Inizio chiave di partizione</span><span class="sxs-lookup"><span data-stu-id="5b4c2-177">Start Partition Key</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: startpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4c2-178">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="5b4c2-178">-StartRowKey</span></span>
<span data-ttu-id="5b4c2-179">Tasto inizio riga</span><span class="sxs-lookup"><span data-stu-id="5b4c2-179">Start Row Key</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: startrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4c2-180">-Tabella</span><span class="sxs-lookup"><span data-stu-id="5b4c2-180">-Table</span></span>
<span data-ttu-id="5b4c2-181">Nome tabella</span><span class="sxs-lookup"><span data-stu-id="5b4c2-181">Table Name</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4c2-182">-Tag</span><span class="sxs-lookup"><span data-stu-id="5b4c2-182">-Tag</span></span>
<span data-ttu-id="5b4c2-183">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="5b4c2-183">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5b4c2-184">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="5b4c2-184">For example:</span></span>

<span data-ttu-id="5b4c2-185">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="5b4c2-185">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5b4c2-186">-TargetStorageVersion</span><span class="sxs-lookup"><span data-stu-id="5b4c2-186">-TargetStorageVersion</span></span>
<span data-ttu-id="5b4c2-187">Specifica la versione del servizio di archiviazione firmata da usare per l'autenticazione delle richieste effettuate con il token SAS.</span><span class="sxs-lookup"><span data-stu-id="5b4c2-187">Specifies the signed storage service version to use to authenticate requests made with the SAS token.</span></span>

```yaml
Type: String
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas, StoredPolicyServiceQueueSas, StoredPolicyServiceTableSas
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4c2-188">-ValidityPeriod</span><span class="sxs-lookup"><span data-stu-id="5b4c2-188">-ValidityPeriod</span></span>
<span data-ttu-id="5b4c2-189">Periodo di validità che verrà usato per impostare l'ora di scadenza del token SAS dal momento in cui viene generato</span><span class="sxs-lookup"><span data-stu-id="5b4c2-189">Validity period that will get used to set the expiry time of sas token from the time it gets generated</span></span>

```yaml
Type: TimeSpan
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4c2-190">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="5b4c2-190">-VaultName</span></span>
<span data-ttu-id="5b4c2-191">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="5b4c2-191">Vault name.</span></span>
<span data-ttu-id="5b4c2-192">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="5b4c2-192">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="5b4c2-193">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5b4c2-193">-Confirm</span></span>
<span data-ttu-id="5b4c2-194">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b4c2-194">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b4c2-195">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b4c2-195">-WhatIf</span></span>
<span data-ttu-id="5b4c2-196">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5b4c2-196">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b4c2-197">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5b4c2-197">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b4c2-198">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b4c2-198">CommonParameters</span></span>
<span data-ttu-id="5b4c2-199">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b4c2-199">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b4c2-200">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b4c2-200">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b4c2-201">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5b4c2-201">INPUTS</span></span>

### <span data-ttu-id="5b4c2-202">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5b4c2-202">None</span></span>
<span data-ttu-id="5b4c2-203">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="5b4c2-203">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5b4c2-204">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5b4c2-204">OUTPUTS</span></span>

### <span data-ttu-id="5b4c2-205">Microsoft. Azure. Commands. Vault. Models. ManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="5b4c2-205">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinition</span></span>

## <span data-ttu-id="5b4c2-206">Note</span><span class="sxs-lookup"><span data-stu-id="5b4c2-206">NOTES</span></span>

## <span data-ttu-id="5b4c2-207">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5b4c2-207">RELATED LINKS</span></span>

[<span data-ttu-id="5b4c2-208">Azureâ € ‹ RM. â € ‹ keyâ € ‹ volta</span><span class="sxs-lookup"><span data-stu-id="5b4c2-208">Azureâ€‹RM.â€‹Keyâ€‹Vault</span></span>](/powershell/module/azurerm.keyvault/)