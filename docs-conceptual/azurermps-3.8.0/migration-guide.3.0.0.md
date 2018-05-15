# <a name="breaking-changes-for-microsoft-azure-powershell-300"></a><span data-ttu-id="09324-101">Modifiche di rilievo in Microsoft Azure PowerShell 3.0.0</span><span class="sxs-lookup"><span data-stu-id="09324-101">Breaking changes for Microsoft Azure PowerShell 3.0.0.</span></span>

<span data-ttu-id="09324-102">Questo documento funge sia da notifica delle modifiche di rilievo che da guida alla migrazione per gli utenti dei cmdlet di Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="09324-102">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span>  <span data-ttu-id="09324-103">Ogni sezione descrive sia l'impulso alla base della modifica di rilievo che il percorso di migrazione più semplice.</span><span class="sxs-lookup"><span data-stu-id="09324-103">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span>  <span data-ttu-id="09324-104">Per un approfondimento del contesto, vedere la richiesta pull associata a ogni modifica.</span><span class="sxs-lookup"><span data-stu-id="09324-104">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="09324-105">Sommario</span><span class="sxs-lookup"><span data-stu-id="09324-105">Table of Contents</span></span>
1. [<span data-ttu-id="09324-106">Modifiche di rilievo ai cmdlet per Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="09324-106">Breaking changes to Data Lake Store cmdlets</span></span>](#breaking-changes-to-data-lake-store-cmdlets)
2. [<span data-ttu-id="09324-107">Modifiche di rilievo ai cmdlet per Gestione API</span><span class="sxs-lookup"><span data-stu-id="09324-107">Breaking changes to ApiManagement cmdlets</span></span>](#breaking-changes-to-apimanagement-cmdlets)
3. [<span data-ttu-id="09324-108">Modifiche di rilievo ai cmdlet per le reti</span><span class="sxs-lookup"><span data-stu-id="09324-108">Breaking changes to Network cmdlets</span></span>](#breaking-changes-to-network-cmdlets)

## <a name="breaking-changes-to-data-lake-store-cmdlets"></a><span data-ttu-id="09324-109">Modifiche di rilievo ai cmdlet per Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="09324-109">Breaking changes to Data Lake Store cmdlets</span></span>

<span data-ttu-id="09324-110">Questa versione ha interessato i cmdlet seguenti ([richiesta pull 2965](https://github.com/Azure/azure-powershell/pull/2965)):</span><span class="sxs-lookup"><span data-stu-id="09324-110">The following cmdlets were affected this release ([PR 2965](https://github.com/Azure/azure-powershell/pull/2965)):</span></span>

<span data-ttu-id="09324-111">**Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)**</span><span class="sxs-lookup"><span data-stu-id="09324-111">**Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)**</span></span>
- <span data-ttu-id="09324-112">Questo cmdlet è stato rimosso e sostituito con ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)``.</span><span class="sxs-lookup"><span data-stu-id="09324-112">This cmdlet was removed and replaced with ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)``.</span></span>
- <span data-ttu-id="09324-113">Il cmdlet precedente restituiva un oggetto complesso che rappresentava l'elenco di controllo di accesso.</span><span class="sxs-lookup"><span data-stu-id="09324-113">The old cmdlet returned a complex object representing the access control list (ACL).</span></span> <span data-ttu-id="09324-114">Il nuovo cmdlet restituisce un elenco semplice di voci dell'elenco di controllo di accesso del percorso scelto.</span><span class="sxs-lookup"><span data-stu-id="09324-114">The new cmdlet returns a simple list of entries in the chosen path's ACL.</span></span>

```powershell
# Old
Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo

# New
Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
```

<span data-ttu-id="09324-115">**Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)**</span><span class="sxs-lookup"><span data-stu-id="09324-115">**Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)**</span></span>
- <span data-ttu-id="09324-116">Questo cmdlet sostituisce il precedente cmdlet ``Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)``.</span><span class="sxs-lookup"><span data-stu-id="09324-116">This cmdlet replaces the old cmdlet ``Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)``.</span></span>
- <span data-ttu-id="09324-117">Il nuovo cmdlet restituisce un elenco semplice di voci dell'elenco di controllo di accesso del percorso scelto, di tipo ``DataLakeStoreItemAce[]``.</span><span class="sxs-lookup"><span data-stu-id="09324-117">This new cmdlet returns a simple list of entries in the chosen path's ACL, with type ``DataLakeStoreItemAce[]``.</span></span>
- <span data-ttu-id="09324-118">L'output di questo cmdlet può essere passato al parametro ``-Acl`` dei cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="09324-118">The output of this cmdlet can be passed in to the ``-Acl`` parameter of the following cmdlets:</span></span>
   - ``Remove-AzureRmDataLakeStoreItemAcl``
   - ``Set-AzureRmDataLakeStoreItemAcl``
   - ``Set-AzureRmDataLakeStoreItemAclEntry``

```powershell
# Old
Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo

# New
Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
```

<span data-ttu-id="09324-119">**Remove-AzureRmDataLakeStoreItemAcl (Remove-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAcl (Set-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAclEntry (Set-AdlStoreItemAclEntry)**</span><span class="sxs-lookup"><span data-stu-id="09324-119">**Remove-AzureRmDataLakeStoreItemAcl (Remove-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAcl (Set-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAclEntry (Set-AdlStoreItemAclEntry)**</span></span>
- <span data-ttu-id="09324-120">Questi cmdlet accettano ora ``DataLakeStoreItemAce[]`` per il parametro ``-Acl``.</span><span class="sxs-lookup"><span data-stu-id="09324-120">These cmdlets now accept ``DataLakeStoreItemAce[]`` for the ``-Acl`` parameter.</span></span>
- <span data-ttu-id="09324-121">``DataLakeStoreItemAce[]`` viene restituito da ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)``.</span><span class="sxs-lookup"><span data-stu-id="09324-121">``DataLakeStoreItemAce[]`` is returned by ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)``.</span></span>

```powershell
# Old
$acl = Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo
Set-AdlStoreItemAcl -Account myadlsaccount -Path /foo -Acl $acl

# New
$aclEntries = Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
Set-AdlStoreItemAcl -Account myadlsaccount -Path /foo -Acl $aclEntries
```

## <a name="breaking-changes-to-apimanagement-cmdlets"></a><span data-ttu-id="09324-122">Modifiche di rilievo ai cmdlet per Gestione API</span><span class="sxs-lookup"><span data-stu-id="09324-122">Breaking changes to ApiManagement cmdlets</span></span>

<span data-ttu-id="09324-123">Questa versione ha interessato i cmdlet seguenti ([richiesta pull 2971](https://github.com/Azure/azure-powershell/pull/2971)):</span><span class="sxs-lookup"><span data-stu-id="09324-123">The following cmdlets were affected this release ([PR 2971](https://github.com/Azure/azure-powershell/pull/2971)):</span></span>

<span data-ttu-id="09324-124">**New-AzureRmApiManagementVirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="09324-124">**New-AzureRmApiManagementVirtualNetwork**</span></span>
- <span data-ttu-id="09324-125">I parametri obbligatori per fare riferimento a una rete virtuale sono stati modificati. Anziché SubnetName e VnetId è ora obbligatorio SubnetResourceId, nel formato ``/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ClassicNetwork/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}``</span><span class="sxs-lookup"><span data-stu-id="09324-125">The required parameters to reference a virtual network changed from requiring SubnetName and VnetId to SubnetResourceId in format ``/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ClassicNetwork/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}``</span></span>

```powershell
# Old
$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetName <String> -VnetId <Guid>

# New
$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>

```

<span data-ttu-id="09324-126">**Deprecazione del cmdlet Set-AzureRmApiManagementVirtualNetworks**</span><span class="sxs-lookup"><span data-stu-id="09324-126">**Deprecating Cmdlet Set-AzureRmApiManagementVirtualNetworks**</span></span>
- <span data-ttu-id="09324-127">Il cmdlet verrà deprecato perché esistevano più modi per impostare la rete virtuale associata alla distribuzione di Gestione API.</span><span class="sxs-lookup"><span data-stu-id="09324-127">The Cmdlet is getting deprecated as there was more than one way to Set Virtual Network associated to ApiManagement deployment.</span></span>

```powershell
# Old
$networksList = @()
$networksList += New-AzureRmApiManagementVirtualNetwork -Location $vnetLocation -VnetId $vnetId -SubnetName $subnetName
Set-AzureRmApiManagementVirtualNetworks -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetworks $networksList

# New
$masterRegionVirtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $masterRegionVirtualNetwork
```

## <a name="breaking-changes-to-network-cmdlets"></a><span data-ttu-id="09324-128">Modifiche di rilievo ai cmdlet per le reti</span><span class="sxs-lookup"><span data-stu-id="09324-128">Breaking changes to Network cmdlets</span></span>

<span data-ttu-id="09324-129">Questa versione ha interessato i cmdlet seguenti ([richiesta pull 2982](https://github.com/Azure/azure-powershell/pull/2982)):</span><span class="sxs-lookup"><span data-stu-id="09324-129">The following cmdlets were affected this release ([PR 2982](https://github.com/Azure/azure-powershell/pull/2982)):</span></span>

<span data-ttu-id="09324-130">**New-AzureRmVirtualNetworkGateway**</span><span class="sxs-lookup"><span data-stu-id="09324-130">**New-AzureRmVirtualNetworkGateway**</span></span>
- <span data-ttu-id="09324-131">La descrizione della modifica di ``:- Bool parameter:-ActiveActive`` è stata rimossa ed è stato aggiunto ``SwitchParameter:-EnableActiveActiveFeature`` per abilitare la funzionalità attivo-attivo per il gateway di rete virtuale che viene creato.</span><span class="sxs-lookup"><span data-stu-id="09324-131">Description of what has changed ``:- Bool parameter:-ActiveActive`` is removed and ``SwitchParameter:-EnableActiveActiveFeature`` is added for enabling Active-Active feature on newly creating virtual network gateway.</span></span>

```powershell
# Old 
# Sample of how the cmdlet was previously called
New-AzureRmVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -Location $location -IpConfigurations $vnetIpConfig1,$vnetIpConfig2 -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku HighPerformance -ActiveActive $true

# New
# Sample of how the cmdlet should now be called
New-AzureRmVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -Location $location -IpConfigurations $vnetIpConfig1,$vnetIpConfig2 -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku HighPerformance -EnableActiveActiveFeature
```

<span data-ttu-id="09324-132">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="09324-132">Set-AzureRmVirtualNetworkGateway</span></span>
- <span data-ttu-id="09324-133">La descrizione della modifica di ``:- Bool parameter:-ActiveActive`` è stata rimossa e sono stati aggiunti 2 ``SwitchParameters:-EnableActiveActiveFeature`` / ``DisableActiveActiveFeature`` per abilitare e disabilitare la funzionalità attivo-attivo per il gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="09324-133">Description of what has changed ``:- Bool parameter:-ActiveActive`` is removed and 2 ``SwitchParameters:-EnableActiveActiveFeature`` / ``DisableActiveActiveFeature`` are added for enabling and disabling Active-Active feature on virtual network gateway.</span></span>

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