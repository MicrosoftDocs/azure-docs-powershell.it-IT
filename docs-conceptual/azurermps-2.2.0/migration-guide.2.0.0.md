# <a name="table-of-contents"></a>Sommario
1. [Rimozione dei parametri Force](#removal-of-force-parameters)
2. [Modifica dei parametri Tag](#change-of-tag-parameters)
3. [Modifiche di rilievo ai cmdlet per Archiviazione](#breaking-changes-to-storage-cmdlets)
4. [Modifiche di rilievo ai cmdlet per AD](#breaking-changes-to-ad-cmdlets)

## <a name="removal-of-force-parameters"></a>Rimozione dei parametri Force

In questa versione sono stati rimossi tutti i parametri `Force` obsoleti dai cmdlet, nonché i corrispondenti avvisi relativi alla rimozione del parametro in una versione futura.

I cmdlet interessati da questa modifica sono i seguenti:

**Gestione API**
- Remove-AzureRmApiManagement
- Remove-AzureRmApiManagementApi
- Remove-AzureRmApiManagementGroup
- Remove-AzureRmApiManagementLogger
- Remove-AzureRmApiManagementOpenIdConnectProvider
- Remove-AzureRmApiManagementOperation
- Remove-AzureRmApiManagementPolicy
- Remove-AzureRmApiManagementProduct
- Remove-AzureRmApiManagementProperty
- Remove-AzureRmApiManagementSubscription
- Remove-AzureRmApiManagementUser

**Automazione**
- Remove-AzureRmAutomationCertificate
- Remove-AzureRmAutomationCredential
- Remove-AzureRmAutomationVariable
- Remove-AzureRmAutomationWebhook

**Batch**
- Remove-AzureBatchCertificate
- Remove-AzureBatchComputeNode
- Remove-AzureBatchComputeNodeUser

**Data factory**
- Resume-AzureRmDataFactoryPipeline
- Set-AzureRmDataFactoryPipelineActivePeriod
- Suspend-AzureRmDataFactoryPipeline

**Data Lake Store**
- Remove-AzureRmDataLakeStoreItemAclEntry
- Set-AzureRmDataLakeStoreItemAcl
- Set-AzureRmDataLakeStoreItemAclEntry
- Set-AzureRmDataLakeStoreItemOwner

**Operational Insights**
- Remove-AzureRmOperationalInsightsSavedSearch

**Profilo**
- Remove-AzureRmEnvironment

**RedisCache**
- Remove-AzureRmRedisCacheDiagnostics

**Risorse**
- Register-AzureRmProviderFeature
- Register-AzureRmResourceProvider
- Remove-AzureRmADServicePrincipal
- Remove-AzureRmPolicyAssignment
- Remove-AzureRmResourceGroupDeployment
- Remove-AzureRmRoleAssignment
- Stop-AzureRmResourceGroupDeployment
- Unregister-AzureRmResourceProvider

**Archiviazione**
- Remove-AzureStorageContainerStoredAccessPolicy
- Remove-AzureStorageQueueStoredAccessPolicy
- Remove-AzureStorageShareStoredAccessPolicy
- Remove-AzureStorageTableStoredAccessPolicy

**Analisi di flusso**
- Remove-AzureRmStreamAnalyticsFunction
- Remove-AzureRmStreamAnalyticsInput
- Remove-AzureRmStreamAnalyticsJob
- Remove-AzureRmStreamAnalyticsOutput

**Tag**
- Remove-AzureRmTag

<br>

Se si ha uno script che usa uno dei cmdlet elencati sopra, come correzione per questa modifica di rilievo è sufficiente rimuovere il parametro `Force`.

```powershell
# Old
New-AzureRmResourceGroup -Name $resourceGroupName -Location $location -Force

# New
New-AzureRmResourceGroup -Name $resourceGroupName -Location $location
```

<br>

## <a name="change-of-tag-parameters"></a>Modifica dei parametri Tag

In questa versione, il nome del parametro `Tags` è stato modificato in `Tag` e il tipo è stato modificato da `Hashtable[]` a `Hashtable`, cambiando il formato delle coppie chiave-valore.

In precedenza, ogni voce in `Hashtable[]` rappresentava una singola coppia chiave-valore:

```powershell
$tags = @{ Name = "test1"; Value = "testval1" }, @{ Name = "test2", Value = "testval2" }
$tags[0].Name  # Key for the first entry, "test1"
$tags[0].Value # Value for the first entry, "testval1"
$tags[1].Name  # Key for the second entry, "test2"
$tags[1].Value # Value for the second entry, "testval2"
```

Attualmente non sono più necessari `Name` e `Value` ed è possibile creare coppie chiave-valore assegnando `Key = "Value"` in `Hashtable`:

```powershell
$tag = @{ test1 = "testval1"; test2 = "testval2" }
$tag["test1"] # Gets the value associated with the key "test1"
$tag["test2"] # Gets the value associated with the key "test2"
```

I cmdlet interessati da questa modifica sono i seguenti:

**Batch**
- Get-AzureRmBatchAccount
- New-AzureRmBatchAccount
- Set-AzureRmBatchAccount

**Calcolo**
- New-AzureRmVM
- Update-AzureRmVM

**Data Lake Analytics**
- New-AzureRmDataLakeAnalyticsAccount
- Set-AzureRmDataLakeAnalyticsAccount

**Data Lake Store**
- New-AzureRmDataLakeStoreAccount
- Set-AzureRmDataLakeStoreAccount

**DNS**
- New-AzureRmDnsZone
- Set-AzureRmDnsZone

**Insieme di credenziali delle chiavi**
- Get-AzureRmKeyVault
- New-AzureRmKeyVault

**Rete**
- New-AzureRmApplicationGateway
- New-AzureRmExpressRouteCircuit
- New-AzureRmLoadBalancer
- New-AzureRmLocalNetworkGateway
- New-AzureRmNetworkInterface
- New-AzureRmNetworkSecurityGroup
- New-AzureRmPublicIpAddress
- New-AzureRmRouteTable
- New-AzureRmVirtualNetwork
- New-AzureRmVirtualNetworkGateway
- New-AzureRmVirtualNetworkGatewayConnection
- New-AzureRmVirtualNetworkPeering

**Risorse**
- Find-AzureRmResource
- Find-AzureRmResourceGroup
- New-AzureRmResource
- New-AzureRmResourceGroup
- Set-AzureRmResource
- Set-AzureRmResourceGroup

**SQL**
- New-AzureRmSqlDatabase
- New-AzureRmSqlDatabaseCopy
- New-AzureRmSqlDatabaseSecondary
- New-AzureRmSqlElasticPool
- New-AzureRmSqlServer
- Set-AzureRmSqlDatabase
- Set-AzureRmSqlElasticPool
- Set-AzureRmSqlServer

**Archiviazione**
- New-AzureRmStorageAccount
- Set-AzureRmStorageAccount

**Gestione traffico**
- New-AzureRmTrafficManagerProfile

<br>

Se si ha uno script che usa uno dei cmdlet elencati sopra, come correzione per questa modifica di rilievo modificare il parametro `Tags` in `Tag` e modificare `Tag` nel nuovo formato.

```powershell
# Old
New-AzureRmResourceGroup -Name $resourceGroupName -Location -location -Tags @{ Name = "testtag"; Value = "testval" }

# New
New-AzureRmResourceGroup -Name $resourceGroupName -Location -location -Tag @{ testtag = "testval" }
```

<br>

## <a name="breaking-changes-to-storage-cmdlets"></a>Modifiche di rilievo ai cmdlet per Archiviazione

Questa versione ha interessato i cmdlet seguenti:

**Get-AzureRmStorageAccountKey**
- Il cmdlet restituisce ora un elenco di chiavi, anziché un oggetto con le proprietà per ogni chiave

```powershell
# Old
$key = (Get-AzureRmStorageAccountKey -ResourceGroupName $resourceGroupName -Name $accountName).Key1

# New
$key = (Get-AzureRmStorageAccountKey -ResourceGroupName $resourceGroupName -Name $accountName)[0].Value
```

**New-AzureRmStorageAccountKey**
- Il campo `StorageAccountRegenerateKeyResponse` nell'output di questo cmdlet è stato rinominato `StorageAccountListKeysResults`, che è ora un elenco di chiavi anziché un oggetto con le proprietà per ogni chiave

```powershell
# Old
$key = (New-AzureRmStorageAccountKey -ResourceGroupName $resourceGroupName -Name $accountName).StorageAccountKeys.Key1

# New
$key = (New-AzureRmStorageAccountKey -ResourceGroupName $resourceGroupName -Name $accountName).Keys[0].Value
```

**New/Get/Set-AzureRmStorageAccount**
- Il campo `AccountType` nell'output di questo cmdlet è stato rinominato `Sku.Name`
- Il tipo di output per BLOB/tabelle/code/file di endpoint primari/secondari è stato modificato da `Uri` a `String`

```powershell
# Old
$accountType = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).AccountType

# New
$accountType = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).Sku.Name
```

```powershell
# Old 
$blobEndpoint = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).PrimaryEndpoints.Blob.ToString()
$blobEndpoint = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).PrimaryEndpoints.Blob.AbsolutePath

# New
$blobEndpoint = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).PrimaryEndpoints.Blob.ToString()
$blobEndpoint = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).PrimaryEndpoints.Blob
```

<br>

## <a name="breaking-changes-to-ad-cmdlets"></a>Modifiche di rilievo ai cmdlet per AD

Questa versione ha interessato i cmdlet seguenti:

**Get-AzureRMADServicePrincipal**
- Il campo `ServicePrincipalName` nell'output di questo cmdlet è stato rinominato `ServicePrincipalNames` ed è ora una raccolta. `ApplicationId` viene ora visualizzato come uno dei nomi dell'entità servizio, insieme a identifierUri.

```powershell
# Old
$servicePrincipals = Get-AzureRmADServicePrincipal -SearchString $displayName
$spn = $servicePrincipals[0].ServicePrincipalName

# New
$servicePrincipals = Get-AzureRmADServicePrincipal -SearchString $displayName
$spn = $servicePrincipals[0].ServicePrincipalNames[0]
```

**Get-AzureRmADApplication**
- Il parametro `ApplicationObjectId` è stato rinominato `ObjectId`.
- Nell'output di questo cmdlet, `ApplicationObjectId` è stato rinominato `ObjectId`.

```powershell
# Old
$app = Get-AzureRmADApplication -ApplicationObjectId $applicationObjectId
$objectId = $app.ApplicationObjectId

# New
$app = Get-AzureRmADApplication -ObjectId $objectId
$objectId = $app.ObjectId
```

**Remove-AzureRmADApplication**
- Il parametro `ApplicationObjectId` è stato rinominato `ObjectId`.

```powershell
# Old
$app = Remove-AzureRmADApplication -ApplicationObjectId $applicationObjectId -Force

# New
$app = Remove-AzureRmADApplication -ObjectId $objectId -Force
```

**New-AzureRmADApplication**
- Nell'output di questo cmdlet, `ApplicationObjectId` è stato rinominato `ObjectId`.
- I parametri `KeyValue`, `KeyUsage` e `KeyType` sono stati rimossi.

```powershell
# Old
$app = New-AzureRmADApplication -DisplayName $displayName -HomePage $homePage -IdentifierUris $identifierUris -KeyValue $kv -KeyType $kt -KeyUsage $ku
$id = $app.ApplicationObjectId

# New
$app = New-AzureRmADApplication -DisplayName $displayName -HomePage $homePage -IdentifierUris $identifierUris
$id = $app.ObjectId
New-AzureRmADAppCredential -ObjectId $id -Password $kv
```

**Get-AzureRmADGroup**
- Il campo `Mail` è stato rimosso dall'output.

**Get-AzureRmADUser**
- Il campo `Mail` è stato rimosso dall'output.

**New-AzureRmADServicePrincipal**
- Rimozione del parametro `DisableAccount`.

```powershell
# Old
$servicePrincipal = New-AzureRmADServicePrincipal -DisplayName $displayName -Password $password -DisableAccount true

# New
$servicePrincipal = New-AzureRmADServicePrincipal -DisplayName $displayName -Password $password
Remove-AzureRmADServicePrincipal -ObjectId $servicePrincipal.ObjectId
```