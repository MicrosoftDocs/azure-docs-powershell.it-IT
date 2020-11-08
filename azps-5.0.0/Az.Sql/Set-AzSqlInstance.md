---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
ms.openlocfilehash: e17c6b226f7ed4fe17842c93d03828d53c0bb22c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193141"
---
# <span data-ttu-id="67d7a-101">Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="67d7a-101">Set-AzSqlInstance</span></span>

## <span data-ttu-id="67d7a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="67d7a-102">SYNOPSIS</span></span>
<span data-ttu-id="67d7a-103">Imposta le proprietà per un'istanza gestita di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="67d7a-103">Sets properties for an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="67d7a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="67d7a-104">SYNTAX</span></span>

### <span data-ttu-id="67d7a-105">SetInstanceFromInputParameters (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="67d7a-105">SetInstanceFromInputParameters (Default)</span></span>
```
Set-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67d7a-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="67d7a-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Set-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67d7a-107">SetInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="67d7a-107">SetInstanceFromAzureResourceId</span></span>
```
Set-AzSqlInstance [-ResourceId] <String> [-AdministratorPassword <SecureString>] [-Edition <String>]
 [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-PublicDataEndpointEnabled <Boolean>]
 [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-InstancePoolName <String>]
 [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67d7a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="67d7a-108">DESCRIPTION</span></span>
<span data-ttu-id="67d7a-109">Il cmdlet **set-AzSqlInstance** modifica le proprietà di un'istanza gestita di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="67d7a-109">The **Set-AzSqlInstance** cmdlet modifies properties of an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="67d7a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="67d7a-110">EXAMPLES</span></span>

### <span data-ttu-id="67d7a-111">Esempio 1: impostare l'istanza esistente usando i nuovi valori per-AdministratorPassword,-LicenseType,-StorageSizeInGB,-VCore e-Edition</span><span class="sxs-lookup"><span data-stu-id="67d7a-111">Example 1: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB, -VCore and -Edition</span></span>
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

### <span data-ttu-id="67d7a-112">Esempio 2: modificare la generazione di hardware dell'istanza esistente con il nuovo valore per-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="67d7a-112">Example 2: Change existing instance hardware generation using new value for -ComputeGeneration</span></span>
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

<span data-ttu-id="67d7a-113">Questo comando imposta l'istanza esistente usando i nuovi valori per-AdministratorPassword,-LicenseType,-StorageSizeInGB e-VCore</span><span class="sxs-lookup"><span data-stu-id="67d7a-113">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>

### <span data-ttu-id="67d7a-114">Esempio 3: impostare l'istanza esistente usando i nuovi valori per-AdministratorPassword,-LicenseType,-StorageSizeInGB e-VCore per un'istanza in un pool di istanze</span><span class="sxs-lookup"><span data-stu-id="67d7a-114">Example 3: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>
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

<span data-ttu-id="67d7a-115">Questo comando imposta l'istanza esistente usando i nuovi valori per-AdministratorPassword,-LicenseType,-StorageSizeInGB e-VCore per un'istanza all'interno di un pool di istanze</span><span class="sxs-lookup"><span data-stu-id="67d7a-115">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>

## <span data-ttu-id="67d7a-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="67d7a-116">PARAMETERS</span></span>

### <span data-ttu-id="67d7a-117">-AdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="67d7a-117">-AdministratorPassword</span></span>
<span data-ttu-id="67d7a-118">La nuova password di amministratore SQL per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="67d7a-118">The new SQL administrator password for the instance.</span></span>

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

### <span data-ttu-id="67d7a-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="67d7a-119">-AsJob</span></span>
<span data-ttu-id="67d7a-120">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="67d7a-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="67d7a-121">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="67d7a-121">-AssignIdentity</span></span>
<span data-ttu-id="67d7a-122">Genera e assegna un'identità di Azure Active Directory per questa istanza per l'uso con i servizi di gestione delle chiavi, ad esempio Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="67d7a-122">Generate and assign an Azure Active Directory Identity for this instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="67d7a-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="67d7a-123">-ComputeGeneration</span></span>
<span data-ttu-id="67d7a-124">Generazione di COMPUTE per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="67d7a-124">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="67d7a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67d7a-125">-DefaultProfile</span></span>
<span data-ttu-id="67d7a-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="67d7a-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67d7a-127">-Edition</span><span class="sxs-lookup"><span data-stu-id="67d7a-127">-Edition</span></span>
<span data-ttu-id="67d7a-128">L'edizione da assegnare all'istanza.</span><span class="sxs-lookup"><span data-stu-id="67d7a-128">The edition to assign to the instance.</span></span>

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

### <span data-ttu-id="67d7a-129">-Force</span><span class="sxs-lookup"><span data-stu-id="67d7a-129">-Force</span></span>
<span data-ttu-id="67d7a-130">Ignorare il messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="67d7a-130">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="67d7a-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67d7a-131">-InputObject</span></span>
<span data-ttu-id="67d7a-132">Oggetto AzureSqlManagedInstanceModel da rimuovere</span><span class="sxs-lookup"><span data-stu-id="67d7a-132">The AzureSqlManagedInstanceModel object to remove</span></span>

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

### <span data-ttu-id="67d7a-133">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="67d7a-133">-InstancePoolName</span></span>
<span data-ttu-id="67d7a-134">Nome del pool di istanze.</span><span class="sxs-lookup"><span data-stu-id="67d7a-134">The instance pool name.</span></span>

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

### <span data-ttu-id="67d7a-135">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="67d7a-135">-LicenseType</span></span>
<span data-ttu-id="67d7a-136">Determina il tipo di licenza da usare.</span><span class="sxs-lookup"><span data-stu-id="67d7a-136">Determines which License Type to use.</span></span> <span data-ttu-id="67d7a-137">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="67d7a-137">Possible values are:</span></span>
- <span data-ttu-id="67d7a-138">BasePrice-Azure Hybrid benefit (AHB) i prezzi scontati per i proprietari di licenze di SQL Server esistenti vengono applicati.</span><span class="sxs-lookup"><span data-stu-id="67d7a-138">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="67d7a-139">Il prezzo del servizio istanza gestito verrà scontato per i proprietari di licenze di SQL Server esistenti.</span><span class="sxs-lookup"><span data-stu-id="67d7a-139">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="67d7a-140">LicenseIncluded-Azure Hybrid benefit (AHB) i prezzi di sconto per i proprietari di licenze di SQL Server esistenti non vengono applicati.</span><span class="sxs-lookup"><span data-stu-id="67d7a-140">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="67d7a-141">Il prezzo del servizio istanza gestito includerà un nuovo costo per la licenza di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="67d7a-141">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="67d7a-142">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="67d7a-142">-MinimalTlsVersion</span></span>
<span data-ttu-id="67d7a-143">Versione TLS minima da applicare per l'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="67d7a-143">The minimal TLS version to enforce for Managed instance</span></span> 

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

### <span data-ttu-id="67d7a-144">-Nome</span><span class="sxs-lookup"><span data-stu-id="67d7a-144">-Name</span></span>
<span data-ttu-id="67d7a-145">Nome istanza.</span><span class="sxs-lookup"><span data-stu-id="67d7a-145">Instance name.</span></span>

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

### <span data-ttu-id="67d7a-146">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="67d7a-146">-ProxyOverride</span></span>
<span data-ttu-id="67d7a-147">Tipo di connessione usato per la connessione all'istanza.</span><span class="sxs-lookup"><span data-stu-id="67d7a-147">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="67d7a-148">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="67d7a-148">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="67d7a-149">Indipendentemente dal fatto che l'endpoint di dati pubblici sia abilitato per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="67d7a-149">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="67d7a-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67d7a-150">-ResourceGroupName</span></span>
<span data-ttu-id="67d7a-151">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="67d7a-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="67d7a-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67d7a-152">-ResourceId</span></span>
<span data-ttu-id="67d7a-153">ID risorsa dell'istanza da rimuovere</span><span class="sxs-lookup"><span data-stu-id="67d7a-153">The resource id of instance to remove</span></span>

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

### <span data-ttu-id="67d7a-154">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="67d7a-154">-StorageSizeInGB</span></span>
<span data-ttu-id="67d7a-155">Determina la quantità di spazio di archiviazione da associare all'istanza</span><span class="sxs-lookup"><span data-stu-id="67d7a-155">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="67d7a-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="67d7a-156">-Tag</span></span>
<span data-ttu-id="67d7a-157">Tag da associare all'istanza.</span><span class="sxs-lookup"><span data-stu-id="67d7a-157">The tags to associate with the instance.</span></span>

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

### <span data-ttu-id="67d7a-158">-VCore</span><span class="sxs-lookup"><span data-stu-id="67d7a-158">-VCore</span></span>
<span data-ttu-id="67d7a-159">Determina la quantità di VCore da associare all'istanza</span><span class="sxs-lookup"><span data-stu-id="67d7a-159">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="67d7a-160">-Confermare</span><span class="sxs-lookup"><span data-stu-id="67d7a-160">-Confirm</span></span>
<span data-ttu-id="67d7a-161">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67d7a-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67d7a-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67d7a-162">-WhatIf</span></span>
<span data-ttu-id="67d7a-163">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="67d7a-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67d7a-164">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="67d7a-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67d7a-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67d7a-165">CommonParameters</span></span>
<span data-ttu-id="67d7a-166">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67d7a-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67d7a-167">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="67d7a-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67d7a-168">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="67d7a-168">INPUTS</span></span>

### <span data-ttu-id="67d7a-169">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="67d7a-169">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="67d7a-170">System. String</span><span class="sxs-lookup"><span data-stu-id="67d7a-170">System.String</span></span>

## <span data-ttu-id="67d7a-171">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="67d7a-171">OUTPUTS</span></span>

### <span data-ttu-id="67d7a-172">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="67d7a-172">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="67d7a-173">Note</span><span class="sxs-lookup"><span data-stu-id="67d7a-173">NOTES</span></span>

## <span data-ttu-id="67d7a-174">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="67d7a-174">RELATED LINKS</span></span>
