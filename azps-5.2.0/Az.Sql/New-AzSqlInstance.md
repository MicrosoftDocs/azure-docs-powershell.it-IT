---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
ms.openlocfilehash: ef809acdf8b78eb0d1203a901b3b44028c79733e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336895"
---
# <span data-ttu-id="c5386-101">New-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="c5386-101">New-AzSqlInstance</span></span>

## <span data-ttu-id="c5386-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c5386-102">SYNOPSIS</span></span>
<span data-ttu-id="c5386-103">Crea un'istanza gestita di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="c5386-103">Creates an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="c5386-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c5386-104">SYNTAX</span></span>

### <span data-ttu-id="c5386-105">NewByEditionAndComputeGenerationParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c5386-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-InstancePoolName <String>] [-MinimalTlsVersion <String>]
 [-BackupStorageRedundancy <String>] [-MaintenanceConfigurationId <String>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5386-106">NewByInstancePoolParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5386-106">NewByInstancePoolParentObjectParameterSet</span></span>
```
New-AzSqlInstance [-InstancePool] <AzureSqlInstancePoolModel> [-Name] <String>
 -AdministratorCredential <PSCredential> [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>]
 [-PublicDataEndpointEnabled] [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>]
 [-AssignIdentity] [-DnsZonePartner <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5386-107">NewByInstancePoolResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5386-107">NewByInstancePoolResourceIdParameterSet</span></span>
```
New-AzSqlInstance [-InstancePoolResourceId] <String> [-Name] <String> -AdministratorCredential <PSCredential>
 [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5386-108">NewBySkuNameParameterSetParameter</span><span class="sxs-lookup"><span data-stu-id="c5386-108">NewBySkuNameParameterSetParameter</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -SkuName <String> [-Collation <String>] [-PublicDataEndpointEnabled] [-ProxyOverride <String>]
 [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-DnsZonePartner <String>]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5386-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c5386-109">DESCRIPTION</span></span>
<span data-ttu-id="c5386-110">Il cmdlet **New-AzSqlInstance** crea un'istanza gestita di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="c5386-110">The **New-AzSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="c5386-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c5386-111">EXAMPLES</span></span>

### <span data-ttu-id="c5386-112">Esempio 1: creare una nuova istanza</span><span class="sxs-lookup"><span data-stu-id="c5386-112">Example 1: Create a new instance</span></span>
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

<span data-ttu-id="c5386-113">Questo comando crea una nuova istanza usando il parametro SkuName.</span><span class="sxs-lookup"><span data-stu-id="c5386-113">This command creates a new instance by using the SkuName parameter.</span></span>

### <span data-ttu-id="c5386-114">Esempio 2: creare una nuova istanza</span><span class="sxs-lookup"><span data-stu-id="c5386-114">Example 2: Create a new instance</span></span>
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

<span data-ttu-id="c5386-115">Questo comando crea una nuova istanza usando i parametri Edition e ComputeGeneration.</span><span class="sxs-lookup"><span data-stu-id="c5386-115">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="c5386-116">Esempio 3: creare una nuova istanza in un pool di istanze usando un oggetto pool di istanze</span><span class="sxs-lookup"><span data-stu-id="c5386-116">Example 3: Create a new instance in an instance pool using an instance pool object</span></span>
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

<span data-ttu-id="c5386-117">Questo comando crea una nuova istanza in un pool di istanze usando un oggetto pool di istanze.</span><span class="sxs-lookup"><span data-stu-id="c5386-117">This command creates a new instance in an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="c5386-118">Esempio 4: creare una nuova istanza in un pool di istanze usando un identificatore di risorsa del pool di istanze</span><span class="sxs-lookup"><span data-stu-id="c5386-118">Example 4: Create a new instance in an instance pool using an instance pool resource identifier</span></span>
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

<span data-ttu-id="c5386-119">Questo comando crea una nuova istanza in un pool di istanze usando l'identificatore delle risorse del pool di istanze.</span><span class="sxs-lookup"><span data-stu-id="c5386-119">This command creates a new instance in an instance pool using the instance pool's resource identifier.</span></span>

### <span data-ttu-id="c5386-120">Esempio 5: creare una nuova istanza in un pool di istanze</span><span class="sxs-lookup"><span data-stu-id="c5386-120">Example 5: Create a new instance in an instance pool</span></span>
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

<span data-ttu-id="c5386-121">Questo comando crea una nuova istanza in un pool di istanze con nome instancePool0</span><span class="sxs-lookup"><span data-stu-id="c5386-121">This command creates a new instance in an instance pool with name instancePool0</span></span>

## <span data-ttu-id="c5386-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c5386-122">PARAMETERS</span></span>

### <span data-ttu-id="c5386-123">-AdministratorCredential</span><span class="sxs-lookup"><span data-stu-id="c5386-123">-AdministratorCredential</span></span>
<span data-ttu-id="c5386-124">Credenziali di autenticazione SQL dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="c5386-124">The SQL authentication credential of the instance.</span></span>

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

### <span data-ttu-id="c5386-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c5386-125">-AsJob</span></span>
<span data-ttu-id="c5386-126">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c5386-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c5386-127">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="c5386-127">-AssignIdentity</span></span>
<span data-ttu-id="c5386-128">Genera e assegna un'identità di Azure Active Directory per questa istanza gestita per l'uso con i servizi di gestione delle chiavi, ad esempio Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="c5386-128">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="c5386-129">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="c5386-129">-BackupStorageRedundancy</span></span>
<span data-ttu-id="c5386-130">Ridondanza dello spazio di archiviazione di backup utilizzata per archiviare i backup per l'istanza gestita di SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="c5386-130">The Backup storage redundancy used to store backups for the Sql Azure Managed Instance.</span></span> <span data-ttu-id="c5386-131">Le opzioni disponibili sono: locale, zona e Geo</span><span class="sxs-lookup"><span data-stu-id="c5386-131">Options are: Local, Zone and Geo</span></span>

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

### <span data-ttu-id="c5386-132">-Regole di confronto</span><span class="sxs-lookup"><span data-stu-id="c5386-132">-Collation</span></span>
<span data-ttu-id="c5386-133">Regole di confronto dell'istanza gestita di Azure SQL da usare.</span><span class="sxs-lookup"><span data-stu-id="c5386-133">The collation of the Azure SQL Managed Instance to use.</span></span>

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

### <span data-ttu-id="c5386-134">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="c5386-134">-ComputeGeneration</span></span>
<span data-ttu-id="c5386-135">Generazione di COMPUTE per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="c5386-135">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="c5386-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5386-136">-DefaultProfile</span></span>
<span data-ttu-id="c5386-137">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c5386-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5386-138">-DnsZonePartner</span><span class="sxs-lookup"><span data-stu-id="c5386-138">-DnsZonePartner</span></span>
<span data-ttu-id="c5386-139">ID risorsa del server gestito partner per ereditare la proprietà DnsZone da per la creazione di istanze gestite</span><span class="sxs-lookup"><span data-stu-id="c5386-139">The resource id of the partner Managed Server to inherit DnsZone property from for Managed instance creation</span></span>

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

### <span data-ttu-id="c5386-140">-Edition</span><span class="sxs-lookup"><span data-stu-id="c5386-140">-Edition</span></span>
<span data-ttu-id="c5386-141">L'edizione per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="c5386-141">The edition for the instance.</span></span>

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

### <span data-ttu-id="c5386-142">-Force</span><span class="sxs-lookup"><span data-stu-id="c5386-142">-Force</span></span>
<span data-ttu-id="c5386-143">Ignorare il messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="c5386-143">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="c5386-144">-InstancePool</span><span class="sxs-lookup"><span data-stu-id="c5386-144">-InstancePool</span></span>
<span data-ttu-id="c5386-145">Oggetto padre del pool di istanze.</span><span class="sxs-lookup"><span data-stu-id="c5386-145">The instance pool parent object.</span></span>

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

### <span data-ttu-id="c5386-146">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="c5386-146">-InstancePoolName</span></span>
<span data-ttu-id="c5386-147">Pool di istanze in cui inserire l'istanza.</span><span class="sxs-lookup"><span data-stu-id="c5386-147">The instance pool to place this instance in.</span></span>

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

### <span data-ttu-id="c5386-148">-InstancePoolResourceId</span><span class="sxs-lookup"><span data-stu-id="c5386-148">-InstancePoolResourceId</span></span>
<span data-ttu-id="c5386-149">ID risorsa pool di istanze.</span><span class="sxs-lookup"><span data-stu-id="c5386-149">The instance pool resource id.</span></span>

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

### <span data-ttu-id="c5386-150">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="c5386-150">-LicenseType</span></span>
<span data-ttu-id="c5386-151">Determina il tipo di licenza da usare.</span><span class="sxs-lookup"><span data-stu-id="c5386-151">Determines which License Type to use.</span></span> <span data-ttu-id="c5386-152">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="c5386-152">Possible values are:</span></span>
- <span data-ttu-id="c5386-153">BasePrice-Azure Hybrid benefit (AHB) i prezzi scontati per i proprietari di licenze di SQL Server esistenti vengono applicati.</span><span class="sxs-lookup"><span data-stu-id="c5386-153">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="c5386-154">Il prezzo del servizio istanza gestito verrà scontato per i proprietari di licenze di SQL Server esistenti.</span><span class="sxs-lookup"><span data-stu-id="c5386-154">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="c5386-155">LicenseIncluded-Azure Hybrid benefit (AHB) i prezzi di sconto per i proprietari di licenze di SQL Server esistenti non vengono applicati.</span><span class="sxs-lookup"><span data-stu-id="c5386-155">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="c5386-156">Il prezzo del servizio istanza gestito includerà un nuovo costo per la licenza di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c5386-156">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="c5386-157">-Posizione</span><span class="sxs-lookup"><span data-stu-id="c5386-157">-Location</span></span>
<span data-ttu-id="c5386-158">Posizione in cui creare l'istanza</span><span class="sxs-lookup"><span data-stu-id="c5386-158">The location in which to create the instance</span></span>

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

### <span data-ttu-id="c5386-159">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c5386-159">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="c5386-160">ID configurazione manutenzione per l'istanza gestita di SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="c5386-160">The Maintenance configuration id for the Sql Azure Managed Instance.</span></span>

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

### <span data-ttu-id="c5386-161">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="c5386-161">-MinimalTlsVersion</span></span>
<span data-ttu-id="c5386-162">Versione TLS minima da applicare per l'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="c5386-162">The minimal TLS version to enforce for Managed instance</span></span> 

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

### <span data-ttu-id="c5386-163">-Nome</span><span class="sxs-lookup"><span data-stu-id="c5386-163">-Name</span></span>
<span data-ttu-id="c5386-164">Nome istanza.</span><span class="sxs-lookup"><span data-stu-id="c5386-164">Instance name.</span></span>

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

### <span data-ttu-id="c5386-165">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="c5386-165">-ProxyOverride</span></span>
<span data-ttu-id="c5386-166">Tipo di connessione usato per la connessione all'istanza.</span><span class="sxs-lookup"><span data-stu-id="c5386-166">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="c5386-167">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="c5386-167">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="c5386-168">Indipendentemente dal fatto che l'endpoint di dati pubblici sia abilitato per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="c5386-168">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="c5386-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5386-169">-ResourceGroupName</span></span>
<span data-ttu-id="c5386-170">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c5386-170">The name of the resource group.</span></span>

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

### <span data-ttu-id="c5386-171">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c5386-171">-SkuName</span></span>
<span data-ttu-id="c5386-172">Nome USK per l'istanza, ad esempio "GP_Gen4", "BC_Gen4".</span><span class="sxs-lookup"><span data-stu-id="c5386-172">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

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

### <span data-ttu-id="c5386-173">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="c5386-173">-StorageSizeInGB</span></span>
<span data-ttu-id="c5386-174">Determina la quantità di spazio di archiviazione da associare all'istanza</span><span class="sxs-lookup"><span data-stu-id="c5386-174">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="c5386-175">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="c5386-175">-SubnetId</span></span>
<span data-ttu-id="c5386-176">ID subnet da usare per la creazione di istanze</span><span class="sxs-lookup"><span data-stu-id="c5386-176">The Subnet Id to use for instance creation</span></span>

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

### <span data-ttu-id="c5386-177">-Tag</span><span class="sxs-lookup"><span data-stu-id="c5386-177">-Tag</span></span>
<span data-ttu-id="c5386-178">Tag da associare all'istanza</span><span class="sxs-lookup"><span data-stu-id="c5386-178">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="c5386-179">-TimezoneId</span><span class="sxs-lookup"><span data-stu-id="c5386-179">-TimezoneId</span></span>
<span data-ttu-id="c5386-180">ID del fuso orario per l'istanza da impostare.</span><span class="sxs-lookup"><span data-stu-id="c5386-180">The time zone id for the instance to set.</span></span> <span data-ttu-id="c5386-181">Un elenco di ID fuso orario viene esposto tramite la visualizzazione sys.time_zone_info (Transact-SQL).</span><span class="sxs-lookup"><span data-stu-id="c5386-181">A list of time zone ids is exposed through the sys.time_zone_info (Transact-SQL) view.</span></span>

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

### <span data-ttu-id="c5386-182">-VCore</span><span class="sxs-lookup"><span data-stu-id="c5386-182">-VCore</span></span>
<span data-ttu-id="c5386-183">Determina la quantità di VCore da associare all'istanza</span><span class="sxs-lookup"><span data-stu-id="c5386-183">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="c5386-184">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c5386-184">-Confirm</span></span>
<span data-ttu-id="c5386-185">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5386-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5386-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5386-186">-WhatIf</span></span>
<span data-ttu-id="c5386-187">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c5386-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5386-188">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c5386-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5386-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5386-189">CommonParameters</span></span>
<span data-ttu-id="c5386-190">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5386-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5386-191">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c5386-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5386-192">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c5386-192">INPUTS</span></span>

### <span data-ttu-id="c5386-193">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c5386-193">None</span></span>

## <span data-ttu-id="c5386-194">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c5386-194">OUTPUTS</span></span>

### <span data-ttu-id="c5386-195">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="c5386-195">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="c5386-196">Note</span><span class="sxs-lookup"><span data-stu-id="c5386-196">NOTES</span></span>

## <span data-ttu-id="c5386-197">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c5386-197">RELATED LINKS</span></span>
