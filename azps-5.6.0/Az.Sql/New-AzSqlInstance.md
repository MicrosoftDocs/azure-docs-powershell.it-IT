---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
ms.openlocfilehash: 9f648f0e2ab15919f3caa849041846570d627df5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970205"
---
# <span data-ttu-id="d5627-101">New-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d5627-101">New-AzSqlInstance</span></span>

## <span data-ttu-id="d5627-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5627-102">SYNOPSIS</span></span>
<span data-ttu-id="d5627-103">Crea un'istanza gestita SQL database di Azure.</span><span class="sxs-lookup"><span data-stu-id="d5627-103">Creates an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="d5627-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d5627-104">SYNTAX</span></span>

### <span data-ttu-id="d5627-105">NewByEditionAndComputeGenerationParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d5627-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-InstancePoolName <String>] [-MinimalTlsVersion <String>]
 [-BackupStorageRedundancy <String>] [-MaintenanceConfigurationId <String>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5627-106">NewByInstancePoolParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5627-106">NewByInstancePoolParentObjectParameterSet</span></span>
```
New-AzSqlInstance [-InstancePool] <AzureSqlInstancePoolModel> [-Name] <String>
 -AdministratorCredential <PSCredential> [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>]
 [-PublicDataEndpointEnabled] [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>]
 [-AssignIdentity] [-DnsZonePartner <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5627-107">NewByInstancePoolResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5627-107">NewByInstancePoolResourceIdParameterSet</span></span>
```
New-AzSqlInstance [-InstancePoolResourceId] <String> [-Name] <String> -AdministratorCredential <PSCredential>
 [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5627-108">NewBySkuNameParameterSetParameter</span><span class="sxs-lookup"><span data-stu-id="d5627-108">NewBySkuNameParameterSetParameter</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -SkuName <String> [-Collation <String>] [-PublicDataEndpointEnabled] [-ProxyOverride <String>]
 [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-DnsZonePartner <String>]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5627-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d5627-109">DESCRIPTION</span></span>
<span data-ttu-id="d5627-110">Il cmdlet **New-AzSqlInstance** crea un'istanza gestita SQL database di Azure.</span><span class="sxs-lookup"><span data-stu-id="d5627-110">The **New-AzSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="d5627-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d5627-111">EXAMPLES</span></span>

### <span data-ttu-id="d5627-112">Esempio 1: Creare una nuova istanza</span><span class="sxs-lookup"><span data-stu-id="d5627-112">Example 1: Create a new instance</span></span>
```powershell
PS C:\>New-AzSqlInstance -Name managedInstance1 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -SkuName GP_Gen4 -DnsZonePartner "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/partnerServerForDnsZone"
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
DnsZone                  : ad35cna0mw
InstancePoolName         :
```

<span data-ttu-id="d5627-113">Questo comando crea una nuova istanza usando il parametro SKUName.</span><span class="sxs-lookup"><span data-stu-id="d5627-113">This command creates a new instance by using the SkuName parameter.</span></span>

### <span data-ttu-id="d5627-114">Esempio 2: Creare una nuova istanza</span><span class="sxs-lookup"><span data-stu-id="d5627-114">Example 2: Create a new instance</span></span>
```powershell
PS C:\>New-AzSqlInstance -Name managedInstance2 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -Edition "GeneralPurpose" -ComputeGeneration Gen4
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
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
DnsZone                  : ad35cna0mw
InstancePoolName         :
```

<span data-ttu-id="d5627-115">Questo comando crea una nuova istanza usando i parametri Edition e ComputeGeneration.</span><span class="sxs-lookup"><span data-stu-id="d5627-115">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="d5627-116">Esempio 3: Creare una nuova istanza in un pool di istanze usando un oggetto pool di istanze</span><span class="sxs-lookup"><span data-stu-id="d5627-116">Example 3: Create a new instance in an instance pool using an instance pool object</span></span>
```powershell
PS C:\> $instancePool = Get-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancepool0
PS C:\> $instancePool | New-AzSqlInstance -Name managedInstance2 -AdministratorCredential (Get-Credential) -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 2
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
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
DnsZone                  : ad35cna0mw
InstancePoolName         : instancepool0
```

<span data-ttu-id="d5627-117">Questo comando crea una nuova istanza in un pool di istanze usando un oggetto pool di istanze.</span><span class="sxs-lookup"><span data-stu-id="d5627-117">This command creates a new instance in an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="d5627-118">Esempio 4: Creare una nuova istanza in un pool di istanze usando un identificatore di risorsa del pool di istanze</span><span class="sxs-lookup"><span data-stu-id="d5627-118">Example 4: Create a new instance in an instance pool using an instance pool resource identifier</span></span>
```powershell
PS C:\> $instancePool | New-AzSqlInstance -Name managedInstance2 -AdministratorCredential (Get-Credential) -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 2 -InstancePoolResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
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
DnsZone                  : ad35cna0mw
InstancePoolName         : instancepool0
```

<span data-ttu-id="d5627-119">Questo comando crea una nuova istanza in un pool di istanze usando l'identificatore di risorsa del pool di istanze.</span><span class="sxs-lookup"><span data-stu-id="d5627-119">This command creates a new instance in an instance pool using the instance pool's resource identifier.</span></span>

### <span data-ttu-id="d5627-120">Esempio 5: Creare una nuova istanza in un pool di istanze</span><span class="sxs-lookup"><span data-stu-id="d5627-120">Example 5: Create a new instance in an instance pool</span></span>
```powershell
PS C:\>New-AzSqlInstance -Name managedInstance1 -ResourceGroupName resourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 32 -VCore 2 -ComputeGeneration Gen5 -Edition GeneralPurpose -InstancePoolName instancePool0
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
StorageSizeInGB          : 32
DnsZone                  : ad35cna0mw
InstancePoolName         : instancePool0
```

<span data-ttu-id="d5627-121">Questo comando crea una nuova istanza in un pool di istanze con il nome instancePool0</span><span class="sxs-lookup"><span data-stu-id="d5627-121">This command creates a new instance in an instance pool with name instancePool0</span></span>

### <span data-ttu-id="d5627-122">Esempio 6: Creare una nuova istanza con configurazione di manutenzione</span><span class="sxs-lookup"><span data-stu-id="d5627-122">Example 6: Create a new instance with maintenance configuration</span></span>
```powershell
PS C:\>New-AzSqlInstance -Name managedInstance1 -ResourceGroupName resourcegroup01 -Location "westus" -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -VCore 8 -ComputeGeneration Gen5 -Edition GeneralPurpose -MaintenanceConfigurationId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/SQL_WestUS_MI_2"
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

<span data-ttu-id="d5627-123">Questo comando crea una nuova istanza con impostazioni di configurazione di manutenzione MI_2</span><span class="sxs-lookup"><span data-stu-id="d5627-123">This command creates a new instance with maintenance configuration MI_2</span></span>

## <span data-ttu-id="d5627-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5627-124">PARAMETERS</span></span>

### <span data-ttu-id="d5627-125">-AdministratorCredential</span><span class="sxs-lookup"><span data-stu-id="d5627-125">-AdministratorCredential</span></span>
<span data-ttu-id="d5627-126">L SQL credenziali di autenticazione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="d5627-126">The SQL authentication credential of the instance.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5627-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d5627-127">-AsJob</span></span>
<span data-ttu-id="d5627-128">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d5627-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d5627-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="d5627-129">-AssignIdentity</span></span>
<span data-ttu-id="d5627-130">Generare e assegnare un'identità di Azure Active Directory per questa istanza gestita da usare con servizi di gestione delle chiavi come Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="d5627-130">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="d5627-131">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="d5627-131">-BackupStorageRedundancy</span></span>
<span data-ttu-id="d5627-132">Ridondanza di archiviazione di backup usata per archiviare i backup per l'istanza gestita di Sql Azure.</span><span class="sxs-lookup"><span data-stu-id="d5627-132">The Backup storage redundancy used to store backups for the Sql Azure Managed Instance.</span></span> <span data-ttu-id="d5627-133">Le opzioni disponibili sono: Locale, Area e Geo</span><span class="sxs-lookup"><span data-stu-id="d5627-133">Options are: Local, Zone and Geo</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Local, Zone, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5627-134">-Collation</span><span class="sxs-lookup"><span data-stu-id="d5627-134">-Collation</span></span>
<span data-ttu-id="d5627-135">La fascicolazione dell'istanza SQL Azure da usare.</span><span class="sxs-lookup"><span data-stu-id="d5627-135">The collation of the Azure SQL Managed Instance to use.</span></span>

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

### <span data-ttu-id="d5627-136">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="d5627-136">-ComputeGeneration</span></span>
<span data-ttu-id="d5627-137">Generazione di calcolo per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="d5627-137">The compute generation for the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5627-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5627-138">-DefaultProfile</span></span>
<span data-ttu-id="d5627-139">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d5627-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5627-140">-DnsZonePartner</span><span class="sxs-lookup"><span data-stu-id="d5627-140">-DnsZonePartner</span></span>
<span data-ttu-id="d5627-141">ID risorsa del server gestito del partner da cui ereditare la proprietà DnsZone per la creazione di istanze gestite</span><span class="sxs-lookup"><span data-stu-id="d5627-141">The resource id of the partner Managed Server to inherit DnsZone property from for Managed instance creation</span></span>

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

### <span data-ttu-id="d5627-142">-Edition</span><span class="sxs-lookup"><span data-stu-id="d5627-142">-Edition</span></span>
<span data-ttu-id="d5627-143">Edizione per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="d5627-143">The edition for the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5627-144">-Force</span><span class="sxs-lookup"><span data-stu-id="d5627-144">-Force</span></span>
<span data-ttu-id="d5627-145">Ignora messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="d5627-145">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="d5627-146">-InstancePool</span><span class="sxs-lookup"><span data-stu-id="d5627-146">-InstancePool</span></span>
<span data-ttu-id="d5627-147">Oggetto padre del pool di istanze.</span><span class="sxs-lookup"><span data-stu-id="d5627-147">The instance pool parent object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel
Parameter Sets: NewByInstancePoolParentObjectParameterSet
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5627-148">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="d5627-148">-InstancePoolName</span></span>
<span data-ttu-id="d5627-149">Pool di istanze in cui inserire questa istanza.</span><span class="sxs-lookup"><span data-stu-id="d5627-149">The instance pool to place this instance in.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5627-150">-InstancePoolResourceId</span><span class="sxs-lookup"><span data-stu-id="d5627-150">-InstancePoolResourceId</span></span>
<span data-ttu-id="d5627-151">ID risorsa pool di istanze.</span><span class="sxs-lookup"><span data-stu-id="d5627-151">The instance pool resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByInstancePoolResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5627-152">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="d5627-152">-LicenseType</span></span>
<span data-ttu-id="d5627-153">Determina il tipo di licenza da usare.</span><span class="sxs-lookup"><span data-stu-id="d5627-153">Determines which License Type to use.</span></span> <span data-ttu-id="d5627-154">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="d5627-154">Possible values are:</span></span>
- <span data-ttu-id="d5627-155">BasePrice - Viene applicato un prezzo scontato per Azure Hybrid Benefit (AHB) per i proprietari di licenze SQL Server licenze di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="d5627-155">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="d5627-156">Il prezzo del servizio Istanza gestita verrà scontato per i proprietari SQL Server licenze esistenti.</span><span class="sxs-lookup"><span data-stu-id="d5627-156">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="d5627-157">LicenseIncluded - Il prezzo di sconto AHB (Azure Hybrid Benefit) per i proprietari SQL Server licenze non viene applicato.</span><span class="sxs-lookup"><span data-stu-id="d5627-157">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="d5627-158">Il prezzo del servizio Istanza gestita includerà un costo SQL Server licenze.</span><span class="sxs-lookup"><span data-stu-id="d5627-158">Managed Instance service price will include a new SQL Server license costs.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5627-159">-Location</span><span class="sxs-lookup"><span data-stu-id="d5627-159">-Location</span></span>
<span data-ttu-id="d5627-160">Posizione in cui creare l'istanza</span><span class="sxs-lookup"><span data-stu-id="d5627-160">The location in which to create the instance</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5627-161">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d5627-161">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="d5627-162">ID configurazione manutenzione per l'istanza gestita di Sql Azure.</span><span class="sxs-lookup"><span data-stu-id="d5627-162">The Maintenance configuration id for the Sql Azure Managed Instance.</span></span>

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

### <span data-ttu-id="d5627-163">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="d5627-163">-MinimalTlsVersion</span></span>
<span data-ttu-id="d5627-164">Versione minima di TLS da applicare per l'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="d5627-164">The minimal TLS version to enforce for Managed instance</span></span> 

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

### <span data-ttu-id="d5627-165">-Name</span><span class="sxs-lookup"><span data-stu-id="d5627-165">-Name</span></span>
<span data-ttu-id="d5627-166">Nome dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="d5627-166">Instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5627-167">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="d5627-167">-ProxyOverride</span></span>
<span data-ttu-id="d5627-168">Tipo di connessione usato per la connessione all'istanza.</span><span class="sxs-lookup"><span data-stu-id="d5627-168">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="d5627-169">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="d5627-169">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="d5627-170">Se l'endpoint dei dati pubblico è abilitato o meno per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="d5627-170">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="d5627-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5627-171">-ResourceGroupName</span></span>
<span data-ttu-id="d5627-172">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d5627-172">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5627-173">-SKUName</span><span class="sxs-lookup"><span data-stu-id="d5627-173">-SkuName</span></span>
<span data-ttu-id="d5627-174">Nome SKU per l'istanza, ad esempio "GP_Gen4", "BC_Gen4".</span><span class="sxs-lookup"><span data-stu-id="d5627-174">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

```yaml
Type: System.String
Parameter Sets: NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5627-175">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="d5627-175">-StorageSizeInGB</span></span>
<span data-ttu-id="d5627-176">Determina la quantità di dimensioni dello spazio di archiviazione da associare all'istanza</span><span class="sxs-lookup"><span data-stu-id="d5627-176">Determines how much Storage size to associate with instance</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5627-177">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="d5627-177">-SubnetId</span></span>
<span data-ttu-id="d5627-178">ID subnet da usare per la creazione dell'istanza</span><span class="sxs-lookup"><span data-stu-id="d5627-178">The Subnet Id to use for instance creation</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5627-179">-Tag</span><span class="sxs-lookup"><span data-stu-id="d5627-179">-Tag</span></span>
<span data-ttu-id="d5627-180">I tag da associare all'istanza</span><span class="sxs-lookup"><span data-stu-id="d5627-180">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="d5627-181">-TimezoneId</span><span class="sxs-lookup"><span data-stu-id="d5627-181">-TimezoneId</span></span>
<span data-ttu-id="d5627-182">ID del fuso orario per l'istanza da impostare.</span><span class="sxs-lookup"><span data-stu-id="d5627-182">The time zone id for the instance to set.</span></span> <span data-ttu-id="d5627-183">Un elenco di ID di fuso orario viene esposto tramite la visualizzazione sys.time_zone_info (Transact-SQL).</span><span class="sxs-lookup"><span data-stu-id="d5627-183">A list of time zone ids is exposed through the sys.time_zone_info (Transact-SQL) view.</span></span>

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

### <span data-ttu-id="d5627-184">-VCore</span><span class="sxs-lookup"><span data-stu-id="d5627-184">-VCore</span></span>
<span data-ttu-id="d5627-185">Determina la quantità di VCore da associare all'istanza</span><span class="sxs-lookup"><span data-stu-id="d5627-185">Determines how much VCore to associate with instance</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5627-186">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d5627-186">-Confirm</span></span>
<span data-ttu-id="d5627-187">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5627-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5627-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5627-188">-WhatIf</span></span>
<span data-ttu-id="d5627-189">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d5627-189">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5627-190">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d5627-190">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5627-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5627-191">CommonParameters</span></span>
<span data-ttu-id="d5627-192">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5627-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5627-193">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d5627-193">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5627-194">INPUT</span><span class="sxs-lookup"><span data-stu-id="d5627-194">INPUTS</span></span>

### <span data-ttu-id="d5627-195">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d5627-195">None</span></span>

## <span data-ttu-id="d5627-196">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d5627-196">OUTPUTS</span></span>

### <span data-ttu-id="d5627-197">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="d5627-197">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="d5627-198">NOTE</span><span class="sxs-lookup"><span data-stu-id="d5627-198">NOTES</span></span>

## <span data-ttu-id="d5627-199">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d5627-199">RELATED LINKS</span></span>
