---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
ms.openlocfilehash: d80e6ddd7fa420b07a0df30c2718d9c4e96123fe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857385"
---
# <span data-ttu-id="7396b-101">New-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="7396b-101">New-AzSqlInstance</span></span>

## <span data-ttu-id="7396b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7396b-102">SYNOPSIS</span></span>
<span data-ttu-id="7396b-103">Crea un'istanza gestita di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="7396b-103">Creates an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="7396b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7396b-104">SYNTAX</span></span>

### <span data-ttu-id="7396b-105">NewByEditionAndComputeGenerationParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7396b-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-InstancePoolName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7396b-106">NewByInstancePoolParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7396b-106">NewByInstancePoolParentObjectParameterSet</span></span>
```
New-AzSqlInstance [-InstancePool] <AzureSqlInstancePoolModel> [-Name] <String>
 -AdministratorCredential <PSCredential> [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>]
 [-PublicDataEndpointEnabled] [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>]
 [-AssignIdentity] [-DnsZonePartner <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7396b-107">NewByInstancePoolResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7396b-107">NewByInstancePoolResourceIdParameterSet</span></span>
```
New-AzSqlInstance [-InstancePoolResourceId] <String> [-Name] <String> -AdministratorCredential <PSCredential>
 [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7396b-108">NewBySkuNameParameterSetParameter</span><span class="sxs-lookup"><span data-stu-id="7396b-108">NewBySkuNameParameterSetParameter</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -SkuName <String> [-Collation <String>] [-PublicDataEndpointEnabled] [-ProxyOverride <String>]
 [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-DnsZonePartner <String>]
 [-InstancePoolName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7396b-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7396b-109">DESCRIPTION</span></span>
<span data-ttu-id="7396b-110">Il cmdlet **New-AzSqlInstance** crea un'istanza gestita di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="7396b-110">The **New-AzSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="7396b-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7396b-111">EXAMPLES</span></span>

### <span data-ttu-id="7396b-112">Esempio 1: creare una nuova istanza</span><span class="sxs-lookup"><span data-stu-id="7396b-112">Example 1: Create a new instance</span></span>
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

<span data-ttu-id="7396b-113">Questo comando crea una nuova istanza usando il parametro SkuName.</span><span class="sxs-lookup"><span data-stu-id="7396b-113">This command creates a new instance by using the SkuName parameter.</span></span>

### <span data-ttu-id="7396b-114">Esempio 2: creare una nuova istanza</span><span class="sxs-lookup"><span data-stu-id="7396b-114">Example 2: Create a new instance</span></span>
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

<span data-ttu-id="7396b-115">Questo comando crea una nuova istanza usando i parametri Edition e ComputeGeneration.</span><span class="sxs-lookup"><span data-stu-id="7396b-115">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="7396b-116">Esempio 3: creare una nuova istanza in un pool di istanze usando un oggetto pool di istanze</span><span class="sxs-lookup"><span data-stu-id="7396b-116">Example 3: Create a new instance in an instance pool using an instance pool object</span></span>
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

<span data-ttu-id="7396b-117">Questo comando crea una nuova istanza in un pool di istanze usando un oggetto pool di istanze.</span><span class="sxs-lookup"><span data-stu-id="7396b-117">This command creates a new instance in an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="7396b-118">Esempio 4: creare una nuova istanza in un pool di istanze usando un identificatore di risorsa del pool di istanze</span><span class="sxs-lookup"><span data-stu-id="7396b-118">Example 4: Create a new instance in an instance pool using an instance pool resource identifier</span></span>
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

<span data-ttu-id="7396b-119">Questo comando crea una nuova istanza in un pool di istanze usando l'identificatore delle risorse del pool di istanze.</span><span class="sxs-lookup"><span data-stu-id="7396b-119">This command creates a new instance in an instance pool using the instance pool's resource identifier.</span></span>

### <span data-ttu-id="7396b-120">Esempio 5: creare una nuova istanza in un pool di istanze</span><span class="sxs-lookup"><span data-stu-id="7396b-120">Example 5: Create a new instance in an instance pool</span></span>
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

<span data-ttu-id="7396b-121">Questo comando crea una nuova istanza in un pool di istanze con nome instancePool0</span><span class="sxs-lookup"><span data-stu-id="7396b-121">This command creates a new instance in an instance pool with name instancePool0</span></span>

## <span data-ttu-id="7396b-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7396b-122">PARAMETERS</span></span>

### <span data-ttu-id="7396b-123">-AdministratorCredential</span><span class="sxs-lookup"><span data-stu-id="7396b-123">-AdministratorCredential</span></span>
<span data-ttu-id="7396b-124">Credenziali di autenticazione SQL dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="7396b-124">The SQL authentication credential of the instance.</span></span>

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

### <span data-ttu-id="7396b-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7396b-125">-AsJob</span></span>
<span data-ttu-id="7396b-126">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7396b-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7396b-127">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="7396b-127">-AssignIdentity</span></span>
<span data-ttu-id="7396b-128">Genera e assegna un'identità di Azure Active Directory per questa istanza gestita per l'uso con i servizi di gestione delle chiavi, ad esempio Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="7396b-128">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="7396b-129">-Regole di confronto</span><span class="sxs-lookup"><span data-stu-id="7396b-129">-Collation</span></span>
<span data-ttu-id="7396b-130">Regole di confronto dell'istanza gestita di Azure SQL da usare.</span><span class="sxs-lookup"><span data-stu-id="7396b-130">The collation of the Azure SQL Managed Instance to use.</span></span>

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

### <span data-ttu-id="7396b-131">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="7396b-131">-ComputeGeneration</span></span>
<span data-ttu-id="7396b-132">Generazione di COMPUTE per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="7396b-132">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="7396b-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7396b-133">-DefaultProfile</span></span>
<span data-ttu-id="7396b-134">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7396b-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7396b-135">-DnsZonePartner</span><span class="sxs-lookup"><span data-stu-id="7396b-135">-DnsZonePartner</span></span>
<span data-ttu-id="7396b-136">ID risorsa del server gestito partner per ereditare la proprietà DnsZone da per la creazione di istanze gestite</span><span class="sxs-lookup"><span data-stu-id="7396b-136">The resource id of the partner Managed Server to inherit DnsZone property from for Managed instance creation</span></span>

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

### <span data-ttu-id="7396b-137">-Edition</span><span class="sxs-lookup"><span data-stu-id="7396b-137">-Edition</span></span>
<span data-ttu-id="7396b-138">L'edizione per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="7396b-138">The edition for the instance.</span></span>

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

### <span data-ttu-id="7396b-139">-InstancePool</span><span class="sxs-lookup"><span data-stu-id="7396b-139">-InstancePool</span></span>
<span data-ttu-id="7396b-140">Oggetto padre del pool di istanze.</span><span class="sxs-lookup"><span data-stu-id="7396b-140">The instance pool parent object.</span></span>

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

### <span data-ttu-id="7396b-141">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="7396b-141">-InstancePoolName</span></span>
<span data-ttu-id="7396b-142">Pool di istanze in cui inserire l'istanza.</span><span class="sxs-lookup"><span data-stu-id="7396b-142">The instance pool to place this instance in.</span></span>

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

### <span data-ttu-id="7396b-143">-InstancePoolResourceId</span><span class="sxs-lookup"><span data-stu-id="7396b-143">-InstancePoolResourceId</span></span>
<span data-ttu-id="7396b-144">ID risorsa pool di istanze.</span><span class="sxs-lookup"><span data-stu-id="7396b-144">The instance pool resource id.</span></span>

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

### <span data-ttu-id="7396b-145">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="7396b-145">-LicenseType</span></span>
<span data-ttu-id="7396b-146">Determina il tipo di licenza da usare.</span><span class="sxs-lookup"><span data-stu-id="7396b-146">Determines which License Type to use.</span></span> <span data-ttu-id="7396b-147">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="7396b-147">Possible values are:</span></span>
- <span data-ttu-id="7396b-148">BasePrice-Azure Hybrid benefit (AHB) i prezzi scontati per i proprietari di licenze di SQL Server esistenti vengono applicati.</span><span class="sxs-lookup"><span data-stu-id="7396b-148">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="7396b-149">Il prezzo del servizio istanza gestito verrà scontato per i proprietari di licenze di SQL Server esistenti.</span><span class="sxs-lookup"><span data-stu-id="7396b-149">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="7396b-150">LicenseIncluded-Azure Hybrid benefit (AHB) i prezzi di sconto per i proprietari di licenze di SQL Server esistenti non vengono applicati.</span><span class="sxs-lookup"><span data-stu-id="7396b-150">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="7396b-151">Il prezzo del servizio istanza gestito includerà un nuovo costo per la licenza di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7396b-151">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="7396b-152">-Posizione</span><span class="sxs-lookup"><span data-stu-id="7396b-152">-Location</span></span>
<span data-ttu-id="7396b-153">Posizione in cui creare l'istanza</span><span class="sxs-lookup"><span data-stu-id="7396b-153">The location in which to create the instance</span></span>

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

### <span data-ttu-id="7396b-154">-Nome</span><span class="sxs-lookup"><span data-stu-id="7396b-154">-Name</span></span>
<span data-ttu-id="7396b-155">Nome istanza.</span><span class="sxs-lookup"><span data-stu-id="7396b-155">Instance name.</span></span>

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

### <span data-ttu-id="7396b-156">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="7396b-156">-ProxyOverride</span></span>
<span data-ttu-id="7396b-157">Tipo di connessione usato per la connessione all'istanza.</span><span class="sxs-lookup"><span data-stu-id="7396b-157">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="7396b-158">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="7396b-158">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="7396b-159">Indipendentemente dal fatto che l'endpoint di dati pubblici sia abilitato per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="7396b-159">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="7396b-160">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7396b-160">-ResourceGroupName</span></span>
<span data-ttu-id="7396b-161">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7396b-161">The name of the resource group.</span></span>

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

### <span data-ttu-id="7396b-162">-SkuName</span><span class="sxs-lookup"><span data-stu-id="7396b-162">-SkuName</span></span>
<span data-ttu-id="7396b-163">Nome USK per l'istanza, ad esempio "GP_Gen4", "BC_Gen4".</span><span class="sxs-lookup"><span data-stu-id="7396b-163">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

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

### <span data-ttu-id="7396b-164">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="7396b-164">-StorageSizeInGB</span></span>
<span data-ttu-id="7396b-165">Determina la quantità di spazio di archiviazione da associare all'istanza</span><span class="sxs-lookup"><span data-stu-id="7396b-165">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="7396b-166">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="7396b-166">-SubnetId</span></span>
<span data-ttu-id="7396b-167">ID subnet da usare per la creazione di istanze</span><span class="sxs-lookup"><span data-stu-id="7396b-167">The Subnet Id to use for instance creation</span></span>

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

### <span data-ttu-id="7396b-168">-Tag</span><span class="sxs-lookup"><span data-stu-id="7396b-168">-Tag</span></span>
<span data-ttu-id="7396b-169">Tag da associare all'istanza</span><span class="sxs-lookup"><span data-stu-id="7396b-169">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="7396b-170">-TimezoneId</span><span class="sxs-lookup"><span data-stu-id="7396b-170">-TimezoneId</span></span>
<span data-ttu-id="7396b-171">ID del fuso orario per l'istanza da impostare.</span><span class="sxs-lookup"><span data-stu-id="7396b-171">The time zone id for the instance to set.</span></span> <span data-ttu-id="7396b-172">Un elenco di ID fuso orario viene esposto tramite la visualizzazione sys.time_zone_info (Transact-SQL).</span><span class="sxs-lookup"><span data-stu-id="7396b-172">A list of time zone ids is exposed through the sys.time_zone_info (Transact-SQL) view.</span></span>

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

### <span data-ttu-id="7396b-173">-VCore</span><span class="sxs-lookup"><span data-stu-id="7396b-173">-VCore</span></span>
<span data-ttu-id="7396b-174">Determina la quantità di VCore da associare all'istanza</span><span class="sxs-lookup"><span data-stu-id="7396b-174">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="7396b-175">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7396b-175">-Confirm</span></span>
<span data-ttu-id="7396b-176">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7396b-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7396b-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7396b-177">-WhatIf</span></span>
<span data-ttu-id="7396b-178">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7396b-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7396b-179">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7396b-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7396b-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7396b-180">CommonParameters</span></span>
<span data-ttu-id="7396b-181">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7396b-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7396b-182">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7396b-182">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7396b-183">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7396b-183">INPUTS</span></span>

### <span data-ttu-id="7396b-184">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7396b-184">None</span></span>

## <span data-ttu-id="7396b-185">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7396b-185">OUTPUTS</span></span>

### <span data-ttu-id="7396b-186">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="7396b-186">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="7396b-187">Note</span><span class="sxs-lookup"><span data-stu-id="7396b-187">NOTES</span></span>

## <span data-ttu-id="7396b-188">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7396b-188">RELATED LINKS</span></span>
