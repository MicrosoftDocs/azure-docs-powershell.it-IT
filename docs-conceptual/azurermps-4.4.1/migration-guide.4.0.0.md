# <a name="breaking-changes-for-microsoft-azure-powershell-400"></a><span data-ttu-id="83b9d-101">Modifiche di rilievo in Microsoft Azure PowerShell 4.0.0</span><span class="sxs-lookup"><span data-stu-id="83b9d-101">Breaking changes for Microsoft Azure PowerShell 4.0.0</span></span>

<span data-ttu-id="83b9d-102">Questo documento funge sia da notifica delle modifiche di rilievo che da guida alla migrazione per gli utenti dei cmdlet di Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="83b9d-102">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span> <span data-ttu-id="83b9d-103">Ogni sezione descrive sia l'impulso alla base della modifica di rilievo che il percorso di migrazione più semplice.</span><span class="sxs-lookup"><span data-stu-id="83b9d-103">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span> <span data-ttu-id="83b9d-104">Per un approfondimento del contesto, vedere la richiesta pull associata a ogni modifica.</span><span class="sxs-lookup"><span data-stu-id="83b9d-104">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="83b9d-105">Sommario</span><span class="sxs-lookup"><span data-stu-id="83b9d-105">Table of Contents</span></span>

- [<span data-ttu-id="83b9d-106">Modifiche di rilievo ai cmdlet per le risorse di calcolo</span><span class="sxs-lookup"><span data-stu-id="83b9d-106">Breaking changes to Compute cmdlets</span></span>](#breaking-changes-to-compute-cmdlets)
- [<span data-ttu-id="83b9d-107">Modifiche di rilievo ai cmdlet per Hub eventi</span><span class="sxs-lookup"><span data-stu-id="83b9d-107">Breaking changes to EventHub cmdlets</span></span>](#breaking-changes-to-eventhub-cmdlets)
- [<span data-ttu-id="83b9d-108">Modifiche di rilievo ai cmdlet per Insights</span><span class="sxs-lookup"><span data-stu-id="83b9d-108">Breaking changes to Insights cmdlets</span></span>](#breaking-changes-to-insights-cmdlets)
- [<span data-ttu-id="83b9d-109">Modifiche di rilievo ai cmdlet per le reti</span><span class="sxs-lookup"><span data-stu-id="83b9d-109">Breaking changes to Network cmdlets</span></span>](#breaking-changes-to-network-cmdlets)
- [<span data-ttu-id="83b9d-110">Modifiche di rilievo ai cmdlet per il bus di servizio</span><span class="sxs-lookup"><span data-stu-id="83b9d-110">Breaking changes to ServiceBus cmdlets</span></span>](#breaking-changes-to-servicebus-cmdlets)
- [<span data-ttu-id="83b9d-111">Modifiche di rilievo ai cmdlet per SQL</span><span class="sxs-lookup"><span data-stu-id="83b9d-111">Breaking changes to Sql cmdlets</span></span>](#breaking-changes-to-sql-cmdlets)
- [<span data-ttu-id="83b9d-112">Modifiche di rilievo ai cmdlet per Archiviazione</span><span class="sxs-lookup"><span data-stu-id="83b9d-112">Breaking changes to Storage cmdlets</span></span>](#breaking-changes-to-storage-cmdlets)
- [<span data-ttu-id="83b9d-113">Modifiche di rilievo ai cmdlet per il profilo</span><span class="sxs-lookup"><span data-stu-id="83b9d-113">Breaking Changes to Profile Cmdlets</span></span>](#breaking-changes-to-profile-cmdlets)
## <a name="breaking-changes-to-compute-cmdlets"></a><span data-ttu-id="83b9d-114">Modifiche di rilievo ai cmdlet per le risorse di calcolo</span><span class="sxs-lookup"><span data-stu-id="83b9d-114">Breaking changes to Compute cmdlets</span></span>

<span data-ttu-id="83b9d-115">Questa versione ha interessato i tipi di output seguenti:</span><span class="sxs-lookup"><span data-stu-id="83b9d-115">The following output types were affected this release:</span></span>

### <a name="psvirtualmachine"></a><span data-ttu-id="83b9d-116">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="83b9d-116">PSVirtualMachine</span></span>
- <span data-ttu-id="83b9d-117">Le proprietà di primo livello `DataDiskNames` e `NetworkInterfaceIDs` dell'oggetto `PSVirtualMachine` sono state rimosse dal tipo di output.</span><span class="sxs-lookup"><span data-stu-id="83b9d-117">Top level properties `DataDiskNames` and `NetworkInterfaceIDs` of nthe `PSVirtualMachine` object have been removed from the output type.</span></span> <span data-ttu-id="83b9d-118">Queste proprietà sono sempre state disponibili nelle proprietà `StorageProfile` e `NetworkProfile` dell'oggetto `PSVirtualMachine` e saranno in futuro necessarie per accedervi.</span><span class="sxs-lookup"><span data-stu-id="83b9d-118">These properties have always been available in the `StorageProfile` and `NetworkProfile` properties of the `PSVirtualMachine` object and will be the way they will need to be accessed going forward.</span></span>
- <span data-ttu-id="83b9d-119">Questa modifica interessa i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="83b9d-119">This change affects the following cmdlets:</span></span>
    - `Add-AzureRmVMDataDisk`
    - `Add-AzureRmVMNetworkInterface`
    - `Get-AzureRmVM`
    - `Remove-AzureRmVMDataDisk`
    - `Remove-AzureRmVMNetworkInterface`
    - `Set-AzureRmVMDataDisk`

```powershell
# Old
$vm.DataDiskNames
$vm.NetworkInterfaceIDs

# New
$vm.StorageProfile.DataDisks | Select -Property Name
$vm.NetworkProfile.NetworkInterfaces | Select -Property Id
```

## <a name="breaking-changes-to-eventhub-cmdlets"></a><span data-ttu-id="83b9d-120">Modifiche di rilievo ai cmdlet per Hub eventi</span><span class="sxs-lookup"><span data-stu-id="83b9d-120">Breaking changes to EventHub cmdlets</span></span>

<span data-ttu-id="83b9d-121">Questa versione ha interessato i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="83b9d-121">The following cmdlets were affected this release:</span></span>

### <a name="get-azurermeventhubnamespace"></a><span data-ttu-id="83b9d-122">Get-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="83b9d-122">Get-AzureRmEventHubNamespace</span></span>
- <span data-ttu-id="83b9d-123">La proprietà `ResourceGroupName` è stata rimossa dal tipo di output `NamespaceAttributes`</span><span class="sxs-lookup"><span data-stu-id="83b9d-123">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

### <a name="new-azurermeventhubnamespace"></a><span data-ttu-id="83b9d-124">New-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="83b9d-124">New-AzureRmEventHubNamespace</span></span>
- <span data-ttu-id="83b9d-125">La proprietà `ResourceGroupName` è stata rimossa dal tipo di output `NamespaceAttributes`</span><span class="sxs-lookup"><span data-stu-id="83b9d-125">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

## <a name="breaking-changes-to-insights-cmdlets"></a><span data-ttu-id="83b9d-126">Modifiche di rilievo ai cmdlet per Insights</span><span class="sxs-lookup"><span data-stu-id="83b9d-126">Breaking changes to Insights cmdlets</span></span>

<span data-ttu-id="83b9d-127">Questa versione ha interessato i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="83b9d-127">The following cmdlets were affected this release:</span></span>
    
### <a name="get-azurermusage"></a><span data-ttu-id="83b9d-128">Get-AzureRmUsage</span><span class="sxs-lookup"><span data-stu-id="83b9d-128">Get-AzureRmUsage</span></span>
- <span data-ttu-id="83b9d-129">Questo cmdlet è stato deprecato.</span><span class="sxs-lookup"><span data-stu-id="83b9d-129">This cmdlet has been deprecated.</span></span>

### <a name="remove-azurermalertrule"></a><span data-ttu-id="83b9d-130">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="83b9d-130">Remove-AzureRmAlertRule</span></span>
- <span data-ttu-id="83b9d-131">L'output di questo cmdlet è stato modificato da elenco con un singolo oggetto a singolo oggetto, contenente ID richiesta e codice di stato.</span><span class="sxs-lookup"><span data-stu-id="83b9d-131">The output of this cmdlet has changed from a list with a single object to a single object; this object includes the requestId, and status code.</span></span>
    
```powershell
# Old  
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name chiricutin
if ($s1 -ne $null)
{
    $r = $s1(0).RequestId
    $s = $s1(0).StatusCode
}

# New
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name chiricutin
$r = $s1.RequestId
$s = $s1.StatusCode
```
    
### <a name="add-azurermlogalertrule"></a><span data-ttu-id="83b9d-132">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="83b9d-132">Add-AzureRmLogAlertRule</span></span>
- <span data-ttu-id="83b9d-133">Questo cmdlet è stato deprecato.</span><span class="sxs-lookup"><span data-stu-id="83b9d-133">This cmdlet has been deprecated.</span></span>
    
### <a name="get-azurermalertrule"></a><span data-ttu-id="83b9d-134">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="83b9d-134">Get-AzureRmAlertRule</span></span>
- <span data-ttu-id="83b9d-135">Ogni elemento dell'output di questo cmdlet, che è costituito da un elenco di oggetti, viene reso flat. Anziché oggetti con la struttura `{ Id, Location, Name, Tags, Properties }` verranno quindi restituiti oggetti con la struttura `{ Id, Location, Name, Tags, Type, Description, IsEnabled, Condition, Actions, LastUpdatedTime, ...}`, che include tutti gli attributi di una risorsa di Azure e tutti gli attributi di un oggetto AlertRuleResource al primo livello.</span><span class="sxs-lookup"><span data-stu-id="83b9d-135">Each element of the the output (a list of objects) of this cmdlet is flattened, i.e. instead of returning objects with the structure `{ Id, Location, Name, Tags, Properties }` it will return objects with the structure `{ Id, Location, Name, Tags, Type, Description, IsEnabled, Condition, Actions, LastUpdatedTime, ...}`, which is all of the attributes of an Azure Resource plus all of the attributes of an AlertRuleResource at the top level.</span></span>
    
```powershell
# Old
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -fore red "Error updating alert rule"
      
    Write-Host $rules(0).Id
    Write-Host $rules(0).Properties.IsEnabled
    Write-Host $rules(0).Properties.Condition
}

# New
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -fore red "Error updating alert rule"
 
    Write-Host $rules(0).Id
      
    # Properties will remain for a while
    Write-Host $rules(0).Properties.IsEnabled
      
    # But the properties will be at the top level too. Later Properties will be removed
    Write-Host $rules(0).IsEnabled
    Write-Host $rules(0).Condition
}
```
    
### <a name="get-azurermautoscalesetting"></a><span data-ttu-id="83b9d-136">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="83b9d-136">Get-AzureRmAutoscaleSetting</span></span>
- <span data-ttu-id="83b9d-137">Il campo `AutoscaleSettingResourceName` è deprecato perché ha sempre lo stesso valore del campo `Name`.</span><span class="sxs-lookup"><span data-stu-id="83b9d-137">The `AutoscaleSettingResourceName` field is deprecated since it always has the same value as the `Name` field.</span></span>

```powershell
# Old  
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
if ($s1.AutoscaleSettingResourceName -ne $s1.Name)
{
    Write-Host "There is something wrong with the name"
}

# New
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
    
# There won't be a AutoscaleSettingResourceName
Write-Host $s1.Name
```
    
### <a name="remove-azurermlogprofile"></a><span data-ttu-id="83b9d-138">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="83b9d-138">Remove-AzureRmLogProfile</span></span>
- <span data-ttu-id="83b9d-139">L'output di questo cmdlet verrà modificato da `Boolean` a un oggetto contenente `RequestId` e `StatusCode`</span><span class="sxs-lookup"><span data-stu-id="83b9d-139">The output of this cmdlet will change from `Boolean` to and object containing `RequestId` and `StatusCode`</span></span>

```powershell
# Old  
$s1 = Remove-AzureRmLogProfile -Name myLogProfile
if ($s1 -eq $true)
{
    Write-Host "Removed"
}
else
{
    Write-Host "Failed"
}

# New
$s1 = Remove-AzureRmLogProfile -Name myLogProfile
$r = $s1.RequestId
$s = $s1.StatusCode
```
    
### <a name="add-azurermlogprofile"></a><span data-ttu-id="83b9d-140">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="83b9d-140">Add-AzureRmLogProfile</span></span>
- <span data-ttu-id="83b9d-141">L'output di questo cmdlet verrà modificato in un oggetto contenente ID richiesta, codice di stato e risorsa aggiornata o appena creata</span><span class="sxs-lookup"><span data-stu-id="83b9d-141">The output of this cmdlet will change from an object that includes the requestId, status code, and the updated or newly created resource</span></span>
    
```powershell
# Old  
$s1 = Add-AzureRmLogProfile -Name default -StorageAccountId /subscriptions/df602c9c-7aa0-407d-a6fb-eb20c8bd1192/resourceGroups/JohnKemTest/providers/Microsoft.Storage/storageAccounts/johnkemtest8162 -Locations Global -categ Delete, Write, Action -retention 3
$r = $s1.ServiceBusRuleId

# New
$s1 = Add-AzureRmLogProfile -Name default -StorageAccountId /subscriptions/df602c9c-7aa0-407d-a6fb-eb20c8bd1192/resourceGroups/JohnKemTest/providers/Microsoft.Storage/storageAccounts/johnkemtest8162 -Locations Global -categ Delete, Write, Action -retention 3
$r = $s1.RequestId
$s = $s1.StatusCode
$a = $s1.NewResource.ServiceBusRuleId
    
```
    
### <a name="set-azurermdiagnosticsettings"></a><span data-ttu-id="83b9d-142">Set-AzureRmDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="83b9d-142">Set-AzureRmDiagnosticSettings</span></span>
- <span data-ttu-id="83b9d-143">Il comando verrà rinominato `Update-AzureRmDiagnsoticSettings`</span><span class="sxs-lookup"><span data-stu-id="83b9d-143">The command is going to be renamed to `Update-AzureRmDiagnsoticSettings`</span></span>

```powershell
# Old
Set-AzureRmDiagnosticSettings

# New
Update-AzureRmDiagnosticSettings
```

## <a name="breaking-changes-to-network-cmdlets"></a><span data-ttu-id="83b9d-144">Modifiche di rilievo ai cmdlet per le reti</span><span class="sxs-lookup"><span data-stu-id="83b9d-144">Breaking changes to Network cmdlets</span></span>

<span data-ttu-id="83b9d-145">Questa versione ha interessato i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="83b9d-145">The following cmdlets were affected this release:</span></span>

### <a name="new-azurermvirtualnetworkgatewayconnection"></a><span data-ttu-id="83b9d-146">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="83b9d-146">New-AzureRmVirtualNetworkGatewayConnection</span></span>
- <span data-ttu-id="83b9d-147">Il parametro `EnableBgp` è stato modificato in modo da accettare un valore `boolean` anziché `string`</span><span class="sxs-lookup"><span data-stu-id="83b9d-147">`EnableBgp` parameter has been changed to take a `boolean` instead of a `string`</span></span>

```powershell
# Old
New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName "RG" -name "conn1" -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -SharedKey "key" -EnableBgp "true"

# New
New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName "RG" -name "conn1" -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -SharedKey "key" -EnableBgp $true
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a><span data-ttu-id="83b9d-148">Modifiche di rilievo ai cmdlet per il bus di servizio</span><span class="sxs-lookup"><span data-stu-id="83b9d-148">Breaking changes to ServiceBus cmdlets</span></span>

<span data-ttu-id="83b9d-149">Questa versione ha interessato i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="83b9d-149">The following cmdlets were affected this release:</span></span>

### <a name="get-azurermservicebusnamespace"></a><span data-ttu-id="83b9d-150">Get-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="83b9d-150">Get-AzureRmServiceBusNamespace</span></span>
- <span data-ttu-id="83b9d-151">La proprietà `ResourceGroupName` è stata rimossa dal tipo di output `NamespaceAttributes`</span><span class="sxs-lookup"><span data-stu-id="83b9d-151">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

### <a name="new-azurermservicebusnamespace"></a><span data-ttu-id="83b9d-152">New-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="83b9d-152">New-AzureRmServiceBusNamespace</span></span>

- <span data-ttu-id="83b9d-153">La proprietà `ResourceGroupName` è stata rimossa dal tipo di output `NamespaceAttributes`</span><span class="sxs-lookup"><span data-stu-id="83b9d-153">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

## <a name="breaking-changes-to-sql-cmdlets"></a><span data-ttu-id="83b9d-154">Modifiche di rilievo ai cmdlet per SQL</span><span class="sxs-lookup"><span data-stu-id="83b9d-154">Breaking changes to Sql cmdlets</span></span>

<span data-ttu-id="83b9d-155">Questa versione ha interessato i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="83b9d-155">The following cmdlets were affected this release:</span></span>

### <a name="new-azurermsqldatabasefailovergroup"></a><span data-ttu-id="83b9d-156">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="83b9d-156">New-AzureRmSqlDatabaseFailoverGroup</span></span>
- <span data-ttu-id="83b9d-157">Il parametro `Tag` è stato rimosso</span><span class="sxs-lookup"><span data-stu-id="83b9d-157">`Tag` parameter has been removed</span></span>
- <span data-ttu-id="83b9d-158">Il parametro `GracePeriodWithDataLossHour` è stato rinominato `GracePeriodWithDataLossHours`</span><span class="sxs-lookup"><span data-stu-id="83b9d-158">`GracePeriodWithDataLossHour` parameter has been renamed to `GracePeriodWithDataLossHours`</span></span>

```powershell
# Old
New-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -FailoverPolicy Automatic -GracePeriodWithDataLossHour 1 -Tag @{ Environment="Test" }

# New
New-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

### <a name="set-azurermsqldatabasefailovergroup"></a><span data-ttu-id="83b9d-159">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="83b9d-159">Set-AzureRmSqlDatabaseFailoverGroup</span></span>
- <span data-ttu-id="83b9d-160">Il parametro `Tag` è stato rimosso</span><span class="sxs-lookup"><span data-stu-id="83b9d-160">`Tag` parameter has been removed</span></span>
- <span data-ttu-id="83b9d-161">Il parametro `GracePeriodWithDataLossHour` è stato rinominato `GracePeriodWithDataLossHours`</span><span class="sxs-lookup"><span data-stu-id="83b9d-161">`GracePeriodWithDataLossHour` parameter has been renamed to `GracePeriodWithDataLossHours`</span></span>

```powershell
# Old
Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHour 1 -Tag @{ Environment="Test" }

# New
Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

### <a name="add-azurermsqldatabasetofailovergroup"></a><span data-ttu-id="83b9d-162">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="83b9d-162">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>
- <span data-ttu-id="83b9d-163">Il parametro `Tag` è stato rimosso</span><span class="sxs-lookup"><span data-stu-id="83b9d-163">`Tag` parameter has been removed</span></span>

```powershell
# Old
Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1 -Tag @{ Environment="Test" }

# New
Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1
```

###  <a name="remove-azurermsqldatabasefromfailovergroup"></a><span data-ttu-id="83b9d-164">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="83b9d-164">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>
- <span data-ttu-id="83b9d-165">Il parametro `Tag` è stato rimosso</span><span class="sxs-lookup"><span data-stu-id="83b9d-165">`Tag` parameter has been removed</span></span>

```powershell
# Old
Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1 -Tag @{ Environment="Test" }

# New
Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1
```

### <a name="remove-azurermsqldatabasefailovergroup"></a><span data-ttu-id="83b9d-166">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="83b9d-166">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>
- <span data-ttu-id="83b9d-167">Il parametro `PartnerResourceGroupName` è stato rimosso</span><span class="sxs-lookup"><span data-stu-id="83b9d-167">`PartnerResourceGroupName` parameter has been removed</span></span>
- <span data-ttu-id="83b9d-168">Il parametro `PartnerServerName` è stato rimosso</span><span class="sxs-lookup"><span data-stu-id="83b9d-168">`PartnerServerName` parameter has been removed</span></span>

```powershell
# Old
Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -PartnerResourceGroupName rg

# New
Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg
```

### <a name="set-azurermsqldatabasethreatdetectionpolicy"></a><span data-ttu-id="83b9d-169">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="83b9d-169">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>
- <span data-ttu-id="83b9d-170">Il valore `Usage_Anomaly` non è più valido per il parametro `ExcludedDetectionType`</span><span class="sxs-lookup"><span data-stu-id="83b9d-170">The value `Usage_Anomaly` is no longer valid for the parameter `ExcludedDetectionType`</span></span>

### <a name="set-azurermsqlserverthreatdetectionpolicy"></a><span data-ttu-id="83b9d-171">Set-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="83b9d-171">Set-AzureRmSqlServerThreatDetectionPolicy</span></span>
- <span data-ttu-id="83b9d-172">Il valore `Usage_Anomaly` non è più valido per il parametro `ExcludedDetectionType`</span><span class="sxs-lookup"><span data-stu-id="83b9d-172">The value `Usage_Anomaly` is no longer valid for the parameter `ExcludedDetectionType`</span></span>

## <a name="breaking-changes-to-storage-cmdlets"></a><span data-ttu-id="83b9d-173">Modifiche di rilievo ai cmdlet per Archiviazione</span><span class="sxs-lookup"><span data-stu-id="83b9d-173">Breaking changes to Storage cmdlets</span></span>

<span data-ttu-id="83b9d-174">Questa versione ha interessato le proprietà dei tipi di output seguenti:</span><span class="sxs-lookup"><span data-stu-id="83b9d-174">The following output type properties were affected this release:</span></span>

### <a name="azurestorageblobicloudblobserviceclient"></a><span data-ttu-id="83b9d-175">AzureStorageBlob.ICloudBlob.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="83b9d-175">AzureStorageBlob.ICloudBlob.ServiceClient</span></span>
- <span data-ttu-id="83b9d-176">Da questo tipo sono state rimosse le proprietà seguenti (_ancora presenti_ nella proprietà `DefaultRequestOptions`):</span><span class="sxs-lookup"><span data-stu-id="83b9d-176">The following properties were removed from this type (_note_: they can still be found in `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `ServerTimeout`
    - `ParallelOperationThreadCount`
    - `SingleBlobUploadThresholdInBytes`
- <span data-ttu-id="83b9d-177">Questa modifica interessa i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="83b9d-177">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageBlob`
    - `Get-AzureStorageBlobContent`
    - `Get-AzureStorageBlobCopyState`
    - `Set-AzureStorageBlobContent`
    - `Start-AzureStorageBlobCopy`
    - `Stop-AzureStorageBlobCopy`
    
### <a name="azurestoragecontainercloudblobcontainerserviceclient"></a><span data-ttu-id="83b9d-178">AzureStorageContainer.CloudBlobContainer.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="83b9d-178">AzureStorageContainer.CloudBlobContainer.ServiceClient</span></span>
- <span data-ttu-id="83b9d-179">Da questo tipo sono state rimosse le proprietà seguenti (_ancora presenti_ nella proprietà `DefaultRequestOptions`):</span><span class="sxs-lookup"><span data-stu-id="83b9d-179">The following properties were removed from this type (_note_: they can still be found in the `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `ServerTimeout`
    - `ParallelOperationThreadCount`
    - `SingleBlobUploadThresholdInBytes`
- <span data-ttu-id="83b9d-180">Questa modifica interessa i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="83b9d-180">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageContainer`
    - `New-AzureStorageContainer`
    - `Set-AzureStorageContainerAcl`
    
### <a name="azurestoragequeuecloudqueueserviceclient"></a><span data-ttu-id="83b9d-181">AzureStorageQueue.CloudQueue.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="83b9d-181">AzureStorageQueue.CloudQueue.ServiceClient</span></span>
- <span data-ttu-id="83b9d-182">Da questo tipo sono state rimosse le proprietà seguenti (_ancora presenti_ nella proprietà `DefaultRequestOptions`):</span><span class="sxs-lookup"><span data-stu-id="83b9d-182">The following properties were removed from this type (_note_: they can still be found in the `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `RetryPolicy`
    - `ServerTimeout`
- <span data-ttu-id="83b9d-183">Questa modifica interessa i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="83b9d-183">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageQueue`
    - `New-AzureStorageQueue`
    
### <a name="azurestoragetablecloudtableserviceclient"></a><span data-ttu-id="83b9d-184">AzureStorageTable.CloudTable.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="83b9d-184">AzureStorageTable.CloudTable.ServiceClient</span></span>
- <span data-ttu-id="83b9d-185">Da questo tipo sono state rimosse le proprietà seguenti (_ancora presenti_ nella proprietà `DefaultRequestOptions`):</span><span class="sxs-lookup"><span data-stu-id="83b9d-185">The following properties were removed from this type (_note_: they can still be found in the `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `PayloadFormat`
    - `RetryPolicy`
    - `ServerTimeout`
- <span data-ttu-id="83b9d-186">Questa modifica interessa i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="83b9d-186">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageTable`
    - `New-AzureStorageTable`
    
```powershell
# Old
$LocationMode = (Get-AzureStorageBlob -Container $containername)[0].ICloudBlob.ServiceClient.LocationMode       
$ParallelOperationThreadCount = (Get-AzureStorageContainer -Container $containername).CloudBlobContainer.ServiceClient.ParallelOperationThreadCount
$PayloadFormat = (Get-AzureStorageTable -Name $tablename).CloudTable.ServiceClient.PayloadFormat
$RetryPolicy = (Get-AzureStorageQueue -Name $queuename).CloudQueue.ServiceClient.RetryPolicy

# New
$LocationMode = (Get-AzureStorageBlob -Container $containername)[0].ICloudBlob.ServiceClient.DefaultRequestOptions.LocationMode     
$ParallelOperationThreadCount = (Get-AzureStorageContainer -Container $containername).CloudBlobContainer.ServiceClient.DefaultRequestOptions.ParallelOperationThreadCount
$PayloadFormat = (Get-AzureStorageTable -Name $tablename).CloudTable.ServiceClient.DefaultRequestOptions.PayloadFormat
$RetryPolicy = (Get-AzureStorageQueue -Name $queuename).CloudQueue.ServiceClient.DefaultRequestOptions.RetryPolicy
```

## <a name="breaking-changes-to-profile-cmdlets"></a><span data-ttu-id="83b9d-187">Modifiche di rilievo ai cmdlet per il profilo</span><span class="sxs-lookup"><span data-stu-id="83b9d-187">Breaking Changes to Profile Cmdlets</span></span>

<span data-ttu-id="83b9d-188">In questa versione sono stati modificati i cmdlet e i tipi di output dei cmdlet seguenti.</span><span class="sxs-lookup"><span data-stu-id="83b9d-188">The following cmdlets and cmdlet output types were changed in this release.</span></span>

### <a name="add-azurermaccount-breaking-changes"></a><span data-ttu-id="83b9d-189">Modifiche di rilievo ad Add-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="83b9d-189">Add-AzureRmAccount breaking changes</span></span>

- <span data-ttu-id="83b9d-190">Il parametro ```EnvironmentName``` è stato rimosso e sostituito con ```Environment```. ```Environment``` accetta una stringa e non un oggetto ```AzureEnvironment```</span><span class="sxs-lookup"><span data-stu-id="83b9d-190">```EnvironmentName``` parameter has been removed and replaced with ```Environment```, the ```Environment``` now takes a string and not an ```AzureEnvironment``` object</span></span>

```powershell
# Old
Add-AzureRmAccount -EnvironmentName AzureChinaCloud

# New
Add-AzureRmAccount -Environment AzureChinaCloud
```

### <a name="select-azurermprofile-was-renamed-to-import-azurermcontext"></a><span data-ttu-id="83b9d-191">Ridenominazione di Select-AzureRmProfile in Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="83b9d-191">Select-AzureRmProfile was renamed to Import-AzureRmContext</span></span>

<span data-ttu-id="83b9d-192">```Select-AzureRmProfile``` è stato rinominato ```Import-AzureRmContext```</span><span class="sxs-lookup"><span data-stu-id="83b9d-192">```Select-AzureRmProfile``` was renamed to ```Import-AzureRmContext```</span></span>

```powershell
# Old
Select-AzureRmProfile -Path c:\mydir\myprofile.json

# New
Import-AzureRmContext -Path c:\mydir\myprofile.json
```

### <a name="save-azurermprofile-was-renamed-to-save-azurermcontext"></a><span data-ttu-id="83b9d-193">Ridenominazione di Save-AzureRmProfile in Save-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="83b9d-193">Save-AzureRmProfile was renamed to Save-AzureRmContext</span></span>

<span data-ttu-id="83b9d-194">```Save-AzureRmProfile``` è stato rinominato ```Save-AzureRmContext```</span><span class="sxs-lookup"><span data-stu-id="83b9d-194">```Save-AzureRmProfile``` was renamed to ```Save-AzureRmContext```</span></span>

```powershell
# Old
Save-AzureRmProfile -Path c:\mydir\myprofile.json

# New
Save-AzureRmContext -Path c:\mydir\myprofile.json
```
### <a name="breaking-changes-to-output-psazurecontext-type"></a><span data-ttu-id="83b9d-195">Modifiche di rilievo al tipo di output PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="83b9d-195">Breaking Changes to output PSAzureContext Type</span></span>

- <span data-ttu-id="83b9d-196">La proprietà ```TokenCache``` è stata modificata in un tipo che implementa ```IAzureTokenCache``` anziché ```byte[]```</span><span class="sxs-lookup"><span data-stu-id="83b9d-196">The ```TokenCache``` property changed to a type that implements ```IAzureTokenCache``` instead of a ```byte[]```</span></span>

```powershell
# Old
$bytes = (Get-AzureRmContext).TokenCache
$bytes = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).TokenCache
$bytes = (Add-AzureRmAccount).Context.TokenCache

# New
$bytes = (Get-AzureRmContext).TokenCache.CacheData
$bytes = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).TokenCache.CacheData
$bytes = (Add-AzureRmAccount).Context.TokenCache.CacheData
```

### <a name="breaking-changes-to-the-output-psazureaccount-type"></a><span data-ttu-id="83b9d-197">Modifiche di rilievo al tipo di output PSAzureAccount</span><span class="sxs-lookup"><span data-stu-id="83b9d-197">Breaking Changes to the output PSAzureAccount Type</span></span>

- <span data-ttu-id="83b9d-198">La proprietà ```AccountType``` è stata modificata in ```Type```</span><span class="sxs-lookup"><span data-stu-id="83b9d-198">The ```AccountType``` property was changed to ```Type```</span></span>

```powershell
# Old
$type = (Get-AzureRmContext).Account.AccountType
$type = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).Account.AccountType
$type = (Add-AzureRmAccount).Context.Account.AccountType

# New 
$type = (Get-AzureRmContext).Account.Type
$type = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).Account.Type
$type = (Add-AzureRmAccount).Context.Account.Type
```

### <a name="breaking-changes-to-the-output-psazuresubscription-type"></a><span data-ttu-id="83b9d-199">Modifiche di rilievo al tipo di output PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="83b9d-199">Breaking Changes to the output PSAzureSubscription Type</span></span>
- <span data-ttu-id="83b9d-200">La proprietà ```SubscriptionId``` è stata modificata in ```Id```</span><span class="sxs-lookup"><span data-stu-id="83b9d-200">The ```SubscriptionId``` property was changed to ```Id```</span></span>

```powershell
# Old
$id =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).SubscriptionId
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.SubscriptionId
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionId
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionId

# New
$id =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).Id
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.Id
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Id
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Id
```

- <span data-ttu-id="83b9d-201">La proprietà ```SubscriptionName``` è stata modificata in ```Name```</span><span class="sxs-lookup"><span data-stu-id="83b9d-201">The ```SubscriptionName``` property was changed to ```Name```</span></span>

```powershell
# Old
$name =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).SubscriptionName
$name =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.SubscriptionName
$name =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionName
$name =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionName

# New
$name =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).Name
$name =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.Name
$name =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Name
$name =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Name
```

### <a name="breaking-changes-to-the-output-psazuretenant-type"></a><span data-ttu-id="83b9d-202">Modifiche di rilievo al tipo di output PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="83b9d-202">Breaking Changes to the output PSAzureTenant Type</span></span>

- <span data-ttu-id="83b9d-203">La proprietà ```TenantId``` è stata modificata in ```Id```</span><span class="sxs-lookup"><span data-stu-id="83b9d-203">The ```TenantId``` property was changed to ```Id```</span></span>

```powershell
# Old
$id =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).TenantId
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Tenant.TenantId
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.TenantId
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.TenantId

# New
$id =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Id
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Tenant.Id
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.Id
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.Id
```

- <span data-ttu-id="83b9d-204">La proprietà ```Domain``` è stata modificata in ```Directory```</span><span class="sxs-lookup"><span data-stu-id="83b9d-204">The ```Domain``` property was changed to ```Directory```</span></span>

```powershell
# Old
$tenantName =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Domain

# New
$tenantName =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Directory
```
