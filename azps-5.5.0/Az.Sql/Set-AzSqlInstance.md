---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
ms.openlocfilehash: f16e6f2dcbcf3ebd16926784ca84eef02740df7b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195966"
---
# <span data-ttu-id="49d31-101">Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="49d31-101">Set-AzSqlInstance</span></span>

## <span data-ttu-id="49d31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49d31-102">SYNOPSIS</span></span>
<span data-ttu-id="49d31-103">Imposta le proprietà per un'istanza gestita SQL database di Azure.</span><span class="sxs-lookup"><span data-stu-id="49d31-103">Sets properties for an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="49d31-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="49d31-104">SYNTAX</span></span>

### <span data-ttu-id="49d31-105">SetInstanceFromInputParameters (Default)</span><span class="sxs-lookup"><span data-stu-id="49d31-105">SetInstanceFromInputParameters (Default)</span></span>
```
Set-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49d31-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="49d31-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Set-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49d31-107">SetInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="49d31-107">SetInstanceFromAzureResourceId</span></span>
```
Set-AzSqlInstance [-ResourceId] <String> [-AdministratorPassword <SecureString>] [-Edition <String>]
 [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-PublicDataEndpointEnabled <Boolean>]
 [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-InstancePoolName <String>]
 [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>] [-MaintenanceConfigurationId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49d31-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="49d31-108">DESCRIPTION</span></span>
<span data-ttu-id="49d31-109">Il cmdlet **Set-AzSqlInstance** modifica le proprietà di un'istanza gestita SQL database di Azure.</span><span class="sxs-lookup"><span data-stu-id="49d31-109">The **Set-AzSqlInstance** cmdlet modifies properties of an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="49d31-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="49d31-110">EXAMPLES</span></span>

### <span data-ttu-id="49d31-111">Esempio 1: Impostare un'istanza esistente usando i nuovi valori per -AdministratorPassword, -LicenseType, -StorageSizeInGB, -VCore ed -Edition</span><span class="sxs-lookup"><span data-stu-id="49d31-111">Example 1: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB, -VCore and -Edition</span></span>
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

### <span data-ttu-id="49d31-112">Esempio 2: Modificare la generazione di hardware di istanza esistente usando il nuovo valore per -ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="49d31-112">Example 2: Change existing instance hardware generation using new value for -ComputeGeneration</span></span>
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

<span data-ttu-id="49d31-113">Questo comando imposta l'istanza esistente usando i nuovi valori per -AdministratorPassword, -LicenseType, -StorageSizeInGB e -VCore</span><span class="sxs-lookup"><span data-stu-id="49d31-113">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>

### <span data-ttu-id="49d31-114">Esempio 3: Impostare un'istanza esistente usando i nuovi valori per -AdministratorPassword, -LicenseType, -StorageSizeInGB e -VCore per un'istanza all'interno di un pool di istanze</span><span class="sxs-lookup"><span data-stu-id="49d31-114">Example 3: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>
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

<span data-ttu-id="49d31-115">Questo comando imposta un'istanza esistente usando i nuovi valori per -AdministratorPassword, -LicenseType, -StorageSizeInGB e -VCore per un'istanza all'interno di un pool di istanze</span><span class="sxs-lookup"><span data-stu-id="49d31-115">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>

## <span data-ttu-id="49d31-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49d31-116">PARAMETERS</span></span>

### <span data-ttu-id="49d31-117">-AdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="49d31-117">-AdministratorPassword</span></span>
<span data-ttu-id="49d31-118">La nuova SQL password dell'amministratore per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="49d31-118">The new SQL administrator password for the instance.</span></span>

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

### <span data-ttu-id="49d31-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="49d31-119">-AsJob</span></span>
<span data-ttu-id="49d31-120">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="49d31-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="49d31-121">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="49d31-121">-AssignIdentity</span></span>
<span data-ttu-id="49d31-122">Generare e assegnare un'identità di Azure Active Directory per questa istanza per l'uso con servizi di gestione delle chiavi come Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="49d31-122">Generate and assign an Azure Active Directory Identity for this instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="49d31-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="49d31-123">-ComputeGeneration</span></span>
<span data-ttu-id="49d31-124">Generazione di calcolo per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="49d31-124">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="49d31-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49d31-125">-DefaultProfile</span></span>
<span data-ttu-id="49d31-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="49d31-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49d31-127">-Edition</span><span class="sxs-lookup"><span data-stu-id="49d31-127">-Edition</span></span>
<span data-ttu-id="49d31-128">L'edizione da assegnare all'istanza.</span><span class="sxs-lookup"><span data-stu-id="49d31-128">The edition to assign to the instance.</span></span>

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

### <span data-ttu-id="49d31-129">-Force</span><span class="sxs-lookup"><span data-stu-id="49d31-129">-Force</span></span>
<span data-ttu-id="49d31-130">Ignora messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="49d31-130">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="49d31-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49d31-131">-InputObject</span></span>
<span data-ttu-id="49d31-132">Oggetto AzureSqlManagedInstanceModel da rimuovere</span><span class="sxs-lookup"><span data-stu-id="49d31-132">The AzureSqlManagedInstanceModel object to remove</span></span>

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

### <span data-ttu-id="49d31-133">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="49d31-133">-InstancePoolName</span></span>
<span data-ttu-id="49d31-134">Nome del pool di istanze.</span><span class="sxs-lookup"><span data-stu-id="49d31-134">The instance pool name.</span></span>

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

### <span data-ttu-id="49d31-135">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="49d31-135">-LicenseType</span></span>
<span data-ttu-id="49d31-136">Determina il tipo di licenza da usare.</span><span class="sxs-lookup"><span data-stu-id="49d31-136">Determines which License Type to use.</span></span> <span data-ttu-id="49d31-137">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="49d31-137">Possible values are:</span></span>
- <span data-ttu-id="49d31-138">BasePrice - Viene applicato un prezzo scontato per Azure Hybrid Benefit (AHB) per i proprietari di licenze SQL Server licenze di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="49d31-138">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="49d31-139">Il prezzo del servizio Istanza gestita verrà scontato per i proprietari SQL Server licenze esistenti.</span><span class="sxs-lookup"><span data-stu-id="49d31-139">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="49d31-140">LicenseIncluded - Il prezzo di sconto AHB (Azure Hybrid Benefit) per i proprietari SQL Server licenze non viene applicato.</span><span class="sxs-lookup"><span data-stu-id="49d31-140">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="49d31-141">Il prezzo del servizio Istanza gestita includerà un nuovo costo SQL Server licenze.</span><span class="sxs-lookup"><span data-stu-id="49d31-141">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="49d31-142">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="49d31-142">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="49d31-143">ID configurazione manutenzione per l'istanza gestita di Sql Azure.</span><span class="sxs-lookup"><span data-stu-id="49d31-143">The Maintenance configuration id for the Sql Azure Managed Instance.</span></span>

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

### <span data-ttu-id="49d31-144">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="49d31-144">-MinimalTlsVersion</span></span>
<span data-ttu-id="49d31-145">Versione minima di TLS da applicare per l'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="49d31-145">The minimal TLS version to enforce for Managed instance</span></span> 

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

### <span data-ttu-id="49d31-146">-Name</span><span class="sxs-lookup"><span data-stu-id="49d31-146">-Name</span></span>
<span data-ttu-id="49d31-147">Nome dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="49d31-147">Instance name.</span></span>

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

### <span data-ttu-id="49d31-148">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="49d31-148">-ProxyOverride</span></span>
<span data-ttu-id="49d31-149">Tipo di connessione usato per la connessione all'istanza.</span><span class="sxs-lookup"><span data-stu-id="49d31-149">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="49d31-150">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="49d31-150">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="49d31-151">Se l'endpoint dati pubblico è abilitato o meno per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="49d31-151">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="49d31-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49d31-152">-ResourceGroupName</span></span>
<span data-ttu-id="49d31-153">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="49d31-153">The name of the resource group.</span></span>

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

### <span data-ttu-id="49d31-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="49d31-154">-ResourceId</span></span>
<span data-ttu-id="49d31-155">ID risorsa dell'istanza da rimuovere</span><span class="sxs-lookup"><span data-stu-id="49d31-155">The resource id of instance to remove</span></span>

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

### <span data-ttu-id="49d31-156">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="49d31-156">-StorageSizeInGB</span></span>
<span data-ttu-id="49d31-157">Determina la quantità di dimensioni dello spazio di archiviazione da associare all'istanza</span><span class="sxs-lookup"><span data-stu-id="49d31-157">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="49d31-158">-Tag</span><span class="sxs-lookup"><span data-stu-id="49d31-158">-Tag</span></span>
<span data-ttu-id="49d31-159">Tag da associare all'istanza.</span><span class="sxs-lookup"><span data-stu-id="49d31-159">The tags to associate with the instance.</span></span>

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

### <span data-ttu-id="49d31-160">-VCore</span><span class="sxs-lookup"><span data-stu-id="49d31-160">-VCore</span></span>
<span data-ttu-id="49d31-161">Determina la quantità di VCore da associare all'istanza</span><span class="sxs-lookup"><span data-stu-id="49d31-161">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="49d31-162">-Confirm</span><span class="sxs-lookup"><span data-stu-id="49d31-162">-Confirm</span></span>
<span data-ttu-id="49d31-163">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49d31-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49d31-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49d31-164">-WhatIf</span></span>
<span data-ttu-id="49d31-165">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="49d31-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49d31-166">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="49d31-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49d31-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49d31-167">CommonParameters</span></span>
<span data-ttu-id="49d31-168">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49d31-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49d31-169">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="49d31-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49d31-170">INPUT</span><span class="sxs-lookup"><span data-stu-id="49d31-170">INPUTS</span></span>

### <span data-ttu-id="49d31-171">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="49d31-171">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="49d31-172">System.String</span><span class="sxs-lookup"><span data-stu-id="49d31-172">System.String</span></span>

## <span data-ttu-id="49d31-173">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="49d31-173">OUTPUTS</span></span>

### <span data-ttu-id="49d31-174">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="49d31-174">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="49d31-175">NOTE</span><span class="sxs-lookup"><span data-stu-id="49d31-175">NOTES</span></span>

## <span data-ttu-id="49d31-176">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="49d31-176">RELATED LINKS</span></span>
