---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
ms.openlocfilehash: a6dd059b7fdab3c2670e3b8902def148d88124d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015869"
---
# <span data-ttu-id="34648-101">Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="34648-101">Set-AzSqlInstance</span></span>

## <span data-ttu-id="34648-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34648-102">SYNOPSIS</span></span>
<span data-ttu-id="34648-103">Imposta le proprietà per un'istanza gestita SQL database di Azure.</span><span class="sxs-lookup"><span data-stu-id="34648-103">Sets properties for an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="34648-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="34648-104">SYNTAX</span></span>

### <span data-ttu-id="34648-105">SetInstanceFromInputParameters (Default)</span><span class="sxs-lookup"><span data-stu-id="34648-105">SetInstanceFromInputParameters (Default)</span></span>
```
Set-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34648-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="34648-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Set-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34648-107">SetInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="34648-107">SetInstanceFromAzureResourceId</span></span>
```
Set-AzSqlInstance [-ResourceId] <String> [-AdministratorPassword <SecureString>] [-Edition <String>]
 [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-PublicDataEndpointEnabled <Boolean>]
 [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-InstancePoolName <String>]
 [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>] [-MaintenanceConfigurationId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34648-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="34648-108">DESCRIPTION</span></span>
<span data-ttu-id="34648-109">Il cmdlet **Set-AzSqlInstance** modifica le proprietà di un'istanza gestita SQL database di Azure.</span><span class="sxs-lookup"><span data-stu-id="34648-109">The **Set-AzSqlInstance** cmdlet modifies properties of an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="34648-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="34648-110">EXAMPLES</span></span>

### <span data-ttu-id="34648-111">Esempio 1: Impostare un'istanza esistente usando i nuovi valori per -AdministratorPassword, -LicenseType, -StorageSizeInGB, -VCore ed -Edition</span><span class="sxs-lookup"><span data-stu-id="34648-111">Example 1: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB, -VCore and -Edition</span></span>
```powershell
PS C:\>$InstancePassword = "Newpassword1234"
PS C:\> $SecureString = ConvertTo-SecureString $InstancePassword -AsPlainText -Force
PS C:\> Set-AzSqlInstance -Name "managedinstance1" -ResourceGroupName "ResourceGroup01" -AdministratorPassword $SecureString -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -Edition BusinessCritical
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : LicenseIncluded
VCores                   : 16
StorageSizeInGB          : 1024
InstancePoolName         :
```

### <span data-ttu-id="34648-112">Esempio 2: Modificare la generazione di hardware di istanza esistente usando il nuovo valore per -ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="34648-112">Example 2: Change existing instance hardware generation using new value for -ComputeGeneration</span></span>
```powershell
PS C:\> Set-AzSqlInstance -Name "managedinstance1" -ResourceGroupName "ResourceGroup01" -ComputeGeneration Gen5
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : LicenseIncluded
VCores                   : 16
StorageSizeInGB          : 1024
InstancePoolName         :
```

<span data-ttu-id="34648-113">Questo comando imposta l'istanza esistente usando i nuovi valori per -AdministratorPassword, -LicenseType, -StorageSizeInGB e -VCore</span><span class="sxs-lookup"><span data-stu-id="34648-113">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>

### <span data-ttu-id="34648-114">Esempio 3: Impostare un'istanza esistente usando i nuovi valori per -AdministratorPassword, -LicenseType, -StorageSizeInGB e -VCore per un'istanza all'interno di un pool di istanze</span><span class="sxs-lookup"><span data-stu-id="34648-114">Example 3: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>
```powershell
PS C:\>$InstancePassword = "Newpassword1234"
PS C:\> $SecureString = ConvertTo-SecureString $InstancePassword -AsPlainText -Force
PS C:\> Set-AzSqlInstance -Name "managedinstance1" -ResourceGroupName "ResourceGroup01" -AdministratorPassword $SecureString -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 2 -InstancePoolName instancePool0
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : LicenseIncluded
VCores                   : 2
StorageSizeInGB          : 1024
InstancePoolName         : instancePool0
```

<span data-ttu-id="34648-115">Questo comando imposta un'istanza esistente usando i nuovi valori per -AdministratorPassword, -LicenseType, -StorageSizeInGB e -VCore per un'istanza all'interno di un pool di istanze</span><span class="sxs-lookup"><span data-stu-id="34648-115">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>

### <span data-ttu-id="34648-116">Esempio 4: Aggiornare la configurazione di manutenzione per un'istanza esistente</span><span class="sxs-lookup"><span data-stu-id="34648-116">Example 4: Update maintenance configuration for existing instance</span></span>
```powershell
PS C:\> Set-AzSqlInstance -Name "managedInstance1" -ResourceGroupName "resourcegroup01" -MaintenanceConfigurationId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/SQL_WestUS_MI_2"
Location                   : westus
Id                         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName          : resourcegroup01
ManagedInstanceName        : managedInstance1
Tags                       :
Identity                   :
Sku                        : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName   : managedInstance1.wusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin         : adminLogin1
AdministratorPassword      :
SubnetId                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType                : LicenseIncluded
VCores                     : 8
StorageSizeInGB            : 256
Collation                  : SQL_Latin1_General_CP1_CI_AS
PublicDataEndpointEnabled  : False
ProxyOverride              :
TimezoneId                 : UTC
DnsZonePartner             :
DnsZone                    : ad35cna0mw
InstancePoolName           :
MinimalTlsVersion          :
BackupStorageRedundancy    : Geo
MaintenanceConfigurationId : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/SQL_WestUS_MI_2
```

<span data-ttu-id="34648-117">Questo comando aggiorna l'istanza esistente con impostazioni di configurazione di MI_2</span><span class="sxs-lookup"><span data-stu-id="34648-117">This command updates existing instance with maintenance configuration MI_2</span></span>

### <span data-ttu-id="34648-118">Esempio 5: Rimuovere la configurazione di manutenzione dall'istanza esistente</span><span class="sxs-lookup"><span data-stu-id="34648-118">Example 5: Remove maintenance configuration from existing instance</span></span>
```powershell
PS C:\> Set-AzSqlInstance -Name "managediInstance1" -ResourceGroupName "Resourcegroup01" -MaintenanceConfigurationId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/SQL_Default"
Location                   : westus
Id                         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName          : resourcegroup01
ManagedInstanceName        : managedInstance1
Tags                       :
Identity                   :
Sku                        : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName   : managedInstance1.wusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin         : adminLogin1
AdministratorPassword      :
SubnetId                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType                : LicenseIncluded
VCores                     : 8
StorageSizeInGB            : 256
Collation                  : SQL_Latin1_General_CP1_CI_AS
PublicDataEndpointEnabled  : False
ProxyOverride              :
TimezoneId                 : UTC
DnsZonePartner             :
DnsZone                    : ad35cna0mw
InstancePoolName           :
MinimalTlsVersion          :
BackupStorageRedundancy    : Geo
MaintenanceConfigurationId : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/SQL_Default
```

<span data-ttu-id="34648-119">Questo comando reimposta le impostazioni predefinite della configurazione di manutenzione per l'istanza esistente</span><span class="sxs-lookup"><span data-stu-id="34648-119">This command resets maintenance configuration to default for existing instance</span></span>

## <span data-ttu-id="34648-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34648-120">PARAMETERS</span></span>

### <span data-ttu-id="34648-121">-AdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="34648-121">-AdministratorPassword</span></span>
<span data-ttu-id="34648-122">La nuova SQL password dell'amministratore per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="34648-122">The new SQL administrator password for the instance.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34648-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="34648-123">-AsJob</span></span>
<span data-ttu-id="34648-124">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="34648-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="34648-125">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="34648-125">-AssignIdentity</span></span>
<span data-ttu-id="34648-126">Generare e assegnare un'identità di Azure Active Directory per questa istanza per l'uso con servizi di gestione delle chiavi come Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="34648-126">Generate and assign an Azure Active Directory Identity for this instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="34648-127">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="34648-127">-ComputeGeneration</span></span>
<span data-ttu-id="34648-128">Generazione di calcolo per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="34648-128">The compute generation for the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34648-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34648-129">-DefaultProfile</span></span>
<span data-ttu-id="34648-130">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="34648-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34648-131">-Edition</span><span class="sxs-lookup"><span data-stu-id="34648-131">-Edition</span></span>
<span data-ttu-id="34648-132">Edizione da assegnare all'istanza.</span><span class="sxs-lookup"><span data-stu-id="34648-132">The edition to assign to the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34648-133">-Force</span><span class="sxs-lookup"><span data-stu-id="34648-133">-Force</span></span>
<span data-ttu-id="34648-134">Ignora messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="34648-134">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="34648-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34648-135">-InputObject</span></span>
<span data-ttu-id="34648-136">Oggetto AzureSqlManagedInstanceModel da rimuovere</span><span class="sxs-lookup"><span data-stu-id="34648-136">The AzureSqlManagedInstanceModel object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: SqlInstance

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34648-137">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="34648-137">-InstancePoolName</span></span>
<span data-ttu-id="34648-138">Nome del pool di istanze.</span><span class="sxs-lookup"><span data-stu-id="34648-138">The instance pool name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34648-139">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="34648-139">-LicenseType</span></span>
<span data-ttu-id="34648-140">Determina il tipo di licenza da usare.</span><span class="sxs-lookup"><span data-stu-id="34648-140">Determines which License Type to use.</span></span> <span data-ttu-id="34648-141">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="34648-141">Possible values are:</span></span>
- <span data-ttu-id="34648-142">BasePrice - Viene applicato un prezzo scontato per Azure Hybrid Benefit (AHB) per i proprietari di licenze SQL Server licenze di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="34648-142">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="34648-143">Il prezzo del servizio Istanza gestita verrà scontato per i proprietari SQL Server licenze esistenti.</span><span class="sxs-lookup"><span data-stu-id="34648-143">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="34648-144">LicenseIncluded - Il prezzo di sconto AHB (Azure Hybrid Benefit) per i proprietari SQL Server licenze non viene applicato.</span><span class="sxs-lookup"><span data-stu-id="34648-144">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="34648-145">Il prezzo del servizio Istanza gestita includerà un costo SQL Server licenze.</span><span class="sxs-lookup"><span data-stu-id="34648-145">Managed Instance service price will include a new SQL Server license costs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34648-146">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="34648-146">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="34648-147">ID configurazione manutenzione per l'istanza gestita di Sql Azure.</span><span class="sxs-lookup"><span data-stu-id="34648-147">The Maintenance configuration id for the Sql Azure Managed Instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34648-148">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="34648-148">-MinimalTlsVersion</span></span>
<span data-ttu-id="34648-149">Versione minima di TLS da applicare per l'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="34648-149">The minimal TLS version to enforce for Managed instance</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, 1.0, 1.1, 1.2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34648-150">-Name</span><span class="sxs-lookup"><span data-stu-id="34648-150">-Name</span></span>
<span data-ttu-id="34648-151">Nome dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="34648-151">Instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFromInputParameters
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34648-152">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="34648-152">-ProxyOverride</span></span>
<span data-ttu-id="34648-153">Tipo di connessione usato per la connessione all'istanza.</span><span class="sxs-lookup"><span data-stu-id="34648-153">The connection type used for connecting to the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34648-154">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="34648-154">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="34648-155">Se l'endpoint dei dati pubblico è abilitato o meno per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="34648-155">Whether or not the public data endpoint is enabled for the instance.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34648-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34648-156">-ResourceGroupName</span></span>
<span data-ttu-id="34648-157">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="34648-157">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34648-158">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="34648-158">-ResourceId</span></span>
<span data-ttu-id="34648-159">ID risorsa dell'istanza da rimuovere</span><span class="sxs-lookup"><span data-stu-id="34648-159">The resource id of instance to remove</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34648-160">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="34648-160">-StorageSizeInGB</span></span>
<span data-ttu-id="34648-161">Determina la quantità di dimensioni dello spazio di archiviazione da associare all'istanza</span><span class="sxs-lookup"><span data-stu-id="34648-161">Determines how much Storage size to associate with instance</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34648-162">-Tag</span><span class="sxs-lookup"><span data-stu-id="34648-162">-Tag</span></span>
<span data-ttu-id="34648-163">Tag da associare all'istanza.</span><span class="sxs-lookup"><span data-stu-id="34648-163">The tags to associate with the instance.</span></span>

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

### <span data-ttu-id="34648-164">-VCore</span><span class="sxs-lookup"><span data-stu-id="34648-164">-VCore</span></span>
<span data-ttu-id="34648-165">Determina la quantità di VCore da associare all'istanza</span><span class="sxs-lookup"><span data-stu-id="34648-165">Determines how much VCore to associate with instance</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34648-166">-Confirm</span><span class="sxs-lookup"><span data-stu-id="34648-166">-Confirm</span></span>
<span data-ttu-id="34648-167">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34648-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34648-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34648-168">-WhatIf</span></span>
<span data-ttu-id="34648-169">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="34648-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34648-170">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="34648-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34648-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34648-171">CommonParameters</span></span>
<span data-ttu-id="34648-172">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34648-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34648-173">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="34648-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34648-174">INPUT</span><span class="sxs-lookup"><span data-stu-id="34648-174">INPUTS</span></span>

### <span data-ttu-id="34648-175">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="34648-175">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="34648-176">System.String</span><span class="sxs-lookup"><span data-stu-id="34648-176">System.String</span></span>

## <span data-ttu-id="34648-177">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="34648-177">OUTPUTS</span></span>

### <span data-ttu-id="34648-178">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="34648-178">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="34648-179">NOTE</span><span class="sxs-lookup"><span data-stu-id="34648-179">NOTES</span></span>

## <span data-ttu-id="34648-180">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="34648-180">RELATED LINKS</span></span>
