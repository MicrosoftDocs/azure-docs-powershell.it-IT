# <a name="breaking-changes-for-microsoft-azure-powershell-300"></a>Modifiche di rilievo in Microsoft Azure PowerShell 3.0.0

Questo documento funge sia da notifica delle modifiche di rilievo che da guida alla migrazione per gli utenti dei cmdlet di Microsoft Azure PowerShell.  Ogni sezione descrive sia l'impulso alla base della modifica di rilievo che il percorso di migrazione più semplice.  Per un approfondimento del contesto, vedere la richiesta pull associata a ogni modifica.

## <a name="table-of-contents"></a>Sommario
1. [Modifiche di rilievo ai cmdlet per Data Lake Store](#breaking-changes-to-data-lake-store-cmdlets)
2. [Modifiche di rilievo ai cmdlet per Gestione API](#breaking-changes-to-apimanagement-cmdlets)
3. [Modifiche di rilievo ai cmdlet per le reti](#breaking-changes-to-network-cmdlets)

## <a name="breaking-changes-to-data-lake-store-cmdlets"></a>Modifiche di rilievo ai cmdlet per Data Lake Store

Questa versione ha interessato i cmdlet seguenti ([richiesta pull 2965](https://github.com/Azure/azure-powershell/pull/2965)):

**Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)**
- Questo cmdlet è stato rimosso e sostituito con ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)``.
- Il cmdlet precedente restituiva un oggetto complesso che rappresentava l'elenco di controllo di accesso. Il nuovo cmdlet restituisce un elenco semplice di voci dell'elenco di controllo di accesso del percorso scelto.

```powershell
# Old
Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo

# New
Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
```

**Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)**
- Questo cmdlet sostituisce il precedente cmdlet ``Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)``.
- Il nuovo cmdlet restituisce un elenco semplice di voci dell'elenco di controllo di accesso del percorso scelto, di tipo ``DataLakeStoreItemAce[]``.
- L'output di questo cmdlet può essere passato al parametro ``-Acl`` dei cmdlet seguenti:
   - ``Remove-AzureRmDataLakeStoreItemAcl``
   - ``Set-AzureRmDataLakeStoreItemAcl``
   - ``Set-AzureRmDataLakeStoreItemAclEntry``

```powershell
# Old
Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo

# New
Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
```

**Remove-AzureRmDataLakeStoreItemAcl (Remove-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAcl (Set-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAclEntry (Set-AdlStoreItemAclEntry)**
- Questi cmdlet accettano ora ``DataLakeStoreItemAce[]`` per il parametro ``-Acl``.
- ``DataLakeStoreItemAce[]`` viene restituito da ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)``.

```powershell
# Old
$acl = Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo
Set-AdlStoreItemAcl -Account myadlsaccount -Path /foo -Acl $acl

# New
$aclEntries = Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
Set-AdlStoreItemAcl -Account myadlsaccount -Path /foo -Acl $aclEntries
```

## <a name="breaking-changes-to-apimanagement-cmdlets"></a>Modifiche di rilievo ai cmdlet per Gestione API

Questa versione ha interessato i cmdlet seguenti ([richiesta pull 2971](https://github.com/Azure/azure-powershell/pull/2971)):

**New-AzureRmApiManagementVirtualNetwork**
- I parametri obbligatori per fare riferimento a una rete virtuale sono stati modificati. Anziché SubnetName e VnetId è ora obbligatorio SubnetResourceId, nel formato ``/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ClassicNetwork/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}``

```powershell
# Old
$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetName <String> -VnetId <Guid>

# New
$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>

```

**Deprecazione del cmdlet Set-AzureRmApiManagementVirtualNetworks**
- Il cmdlet verrà deprecato perché esistevano più modi per impostare la rete virtuale associata alla distribuzione di Gestione API.

```powershell
# Old
$networksList = @()
$networksList += New-AzureRmApiManagementVirtualNetwork -Location $vnetLocation -VnetId $vnetId -SubnetName $subnetName
Set-AzureRmApiManagementVirtualNetworks -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetworks $networksList

# New
$masterRegionVirtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $masterRegionVirtualNetwork
```

## <a name="breaking-changes-to-network-cmdlets"></a>Modifiche di rilievo ai cmdlet per le reti

Questa versione ha interessato i cmdlet seguenti ([richiesta pull 2982](https://github.com/Azure/azure-powershell/pull/2982)):

**New-AzureRmVirtualNetworkGateway**
- La descrizione della modifica di ``:- Bool parameter:-ActiveActive`` è stata rimossa ed è stato aggiunto ``SwitchParameter:-EnableActiveActiveFeature`` per abilitare la funzionalità attivo-attivo per il gateway di rete virtuale che viene creato.

```powershell
# Old 
# Sample of how the cmdlet was previously called
New-AzureRmVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -Location $location -IpConfigurations $vnetIpConfig1,$vnetIpConfig2 -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku HighPerformance -ActiveActive $true

# New
# Sample of how the cmdlet should now be called
New-AzureRmVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -Location $location -IpConfigurations $vnetIpConfig1,$vnetIpConfig2 -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku HighPerformance -EnableActiveActiveFeature
```

Set-AzureRmVirtualNetworkGateway
- La descrizione della modifica di ``:- Bool parameter:-ActiveActive`` è stata rimossa e sono stati aggiunti 2 ``SwitchParameters:-EnableActiveActiveFeature`` / ``DisableActiveActiveFeature`` per abilitare e disabilitare la funzionalità attivo-attivo per il gateway di rete virtuale.

```powershell
# Old
# Sample of how the cmdlet was previously called
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $gw -ActiveActive $true
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $gw -ActiveActive $false  

# New
# Sample of how the cmdlet should now be called
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $gw -EnableActiveActiveFeature
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $gw -DisableActiveActiveFeature
```