---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
ms.openlocfilehash: c08d2b1a08e76603af7125d0d4671643133699da
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857230"
---
# <span data-ttu-id="f53ea-101">Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f53ea-101">Set-AzSqlInstance</span></span>

## <span data-ttu-id="f53ea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f53ea-102">SYNOPSIS</span></span>
<span data-ttu-id="f53ea-103">Imposta le proprietà per un'istanza gestita di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="f53ea-103">Sets properties for an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="f53ea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f53ea-104">SYNTAX</span></span>

### <span data-ttu-id="f53ea-105">SetInstanceFromInputParameters (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f53ea-105">SetInstanceFromInputParameters (Default)</span></span>
```
Set-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f53ea-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="f53ea-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Set-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f53ea-107">SetInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="f53ea-107">SetInstanceFromAzureResourceId</span></span>
```
Set-AzSqlInstance [-ResourceId] <String> [-AdministratorPassword <SecureString>] [-Edition <String>]
 [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-PublicDataEndpointEnabled <Boolean>]
 [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-InstancePoolName <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f53ea-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f53ea-108">DESCRIPTION</span></span>
<span data-ttu-id="f53ea-109">Il cmdlet **set-AzSqlInstance** modifica le proprietà di un'istanza gestita di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="f53ea-109">The **Set-AzSqlInstance** cmdlet modifies properties of an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="f53ea-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f53ea-110">EXAMPLES</span></span>

### <span data-ttu-id="f53ea-111">Esempio 1: impostare l'istanza esistente usando i nuovi valori per-AdministratorPassword,-LicenseType,-StorageSizeInGB e-VCore</span><span class="sxs-lookup"><span data-stu-id="f53ea-111">Example 1: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>
```powershell
PS C:\>$InstancePassword = "Newpassword1234"
PS C:\> $SecureString = ConvertTo-SecureString $InstancePassword -AsPlainText -Force
PS C:\> Set-AzSqlInstance -Name "managedinstance1" -ResourceGroupName "ResourceGroup01" -AdministratorPassword $SecureString -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16
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

<span data-ttu-id="f53ea-112">Questo comando imposta l'istanza esistente usando i nuovi valori per-AdministratorPassword,-LicenseType,-StorageSizeInGB e-VCore</span><span class="sxs-lookup"><span data-stu-id="f53ea-112">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>

### <span data-ttu-id="f53ea-113">Esempio 2: impostare l'istanza esistente usando i nuovi valori per-AdministratorPassword,-LicenseType,-StorageSizeInGB e-VCore per un'istanza in un pool di istanze</span><span class="sxs-lookup"><span data-stu-id="f53ea-113">Example 2: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>
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

<span data-ttu-id="f53ea-114">Questo comando imposta l'istanza esistente usando i nuovi valori per-AdministratorPassword,-LicenseType,-StorageSizeInGB e-VCore per un'istanza all'interno di un pool di istanze</span><span class="sxs-lookup"><span data-stu-id="f53ea-114">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>

## <span data-ttu-id="f53ea-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f53ea-115">PARAMETERS</span></span>

### <span data-ttu-id="f53ea-116">-AdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="f53ea-116">-AdministratorPassword</span></span>
<span data-ttu-id="f53ea-117">La nuova password di amministratore SQL per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="f53ea-117">The new SQL administrator password for the instance.</span></span>

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

### <span data-ttu-id="f53ea-118">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="f53ea-118">-AssignIdentity</span></span>
<span data-ttu-id="f53ea-119">Genera e assegna un'identità di Azure Active Directory per questa istanza per l'uso con i servizi di gestione delle chiavi, ad esempio Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="f53ea-119">Generate and assign an Azure Active Directory Identity for this instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="f53ea-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f53ea-120">-DefaultProfile</span></span>
<span data-ttu-id="f53ea-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f53ea-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f53ea-122">-Edition</span><span class="sxs-lookup"><span data-stu-id="f53ea-122">-Edition</span></span>
<span data-ttu-id="f53ea-123">L'edizione da assegnare all'istanza.</span><span class="sxs-lookup"><span data-stu-id="f53ea-123">The edition to assign to the instance.</span></span>

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

### <span data-ttu-id="f53ea-124">-Force</span><span class="sxs-lookup"><span data-stu-id="f53ea-124">-Force</span></span>
<span data-ttu-id="f53ea-125">Ignorare il messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="f53ea-125">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="f53ea-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f53ea-126">-InputObject</span></span>
<span data-ttu-id="f53ea-127">Oggetto AzureSqlManagedInstanceModel da rimuovere</span><span class="sxs-lookup"><span data-stu-id="f53ea-127">The AzureSqlManagedInstanceModel object to remove</span></span>

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

### <span data-ttu-id="f53ea-128">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="f53ea-128">-InstancePoolName</span></span>
<span data-ttu-id="f53ea-129">Nome del pool di istanze.</span><span class="sxs-lookup"><span data-stu-id="f53ea-129">The instance pool name.</span></span>

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

### <span data-ttu-id="f53ea-130">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="f53ea-130">-LicenseType</span></span>
<span data-ttu-id="f53ea-131">Determina il tipo di licenza da usare.</span><span class="sxs-lookup"><span data-stu-id="f53ea-131">Determines which License Type to use.</span></span> <span data-ttu-id="f53ea-132">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="f53ea-132">Possible values are:</span></span>
- <span data-ttu-id="f53ea-133">BasePrice-Azure Hybrid benefit (AHB) i prezzi scontati per i proprietari di licenze di SQL Server esistenti vengono applicati.</span><span class="sxs-lookup"><span data-stu-id="f53ea-133">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="f53ea-134">Il prezzo del servizio istanza gestito verrà scontato per i proprietari di licenze di SQL Server esistenti.</span><span class="sxs-lookup"><span data-stu-id="f53ea-134">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="f53ea-135">LicenseIncluded-Azure Hybrid benefit (AHB) i prezzi di sconto per i proprietari di licenze di SQL Server esistenti non vengono applicati.</span><span class="sxs-lookup"><span data-stu-id="f53ea-135">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="f53ea-136">Il prezzo del servizio istanza gestito includerà un nuovo costo per la licenza di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f53ea-136">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="f53ea-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="f53ea-137">-Name</span></span>
<span data-ttu-id="f53ea-138">Nome istanza.</span><span class="sxs-lookup"><span data-stu-id="f53ea-138">Instance name.</span></span>

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

### <span data-ttu-id="f53ea-139">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="f53ea-139">-ProxyOverride</span></span>
<span data-ttu-id="f53ea-140">Tipo di connessione usato per la connessione all'istanza.</span><span class="sxs-lookup"><span data-stu-id="f53ea-140">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="f53ea-141">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="f53ea-141">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="f53ea-142">Indipendentemente dal fatto che l'endpoint di dati pubblici sia abilitato per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="f53ea-142">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="f53ea-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f53ea-143">-ResourceGroupName</span></span>
<span data-ttu-id="f53ea-144">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f53ea-144">The name of the resource group.</span></span>

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

### <span data-ttu-id="f53ea-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f53ea-145">-ResourceId</span></span>
<span data-ttu-id="f53ea-146">ID risorsa dell'istanza da rimuovere</span><span class="sxs-lookup"><span data-stu-id="f53ea-146">The resource id of instance to remove</span></span>

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

### <span data-ttu-id="f53ea-147">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="f53ea-147">-StorageSizeInGB</span></span>
<span data-ttu-id="f53ea-148">Determina la quantità di spazio di archiviazione da associare all'istanza</span><span class="sxs-lookup"><span data-stu-id="f53ea-148">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="f53ea-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="f53ea-149">-Tag</span></span>
<span data-ttu-id="f53ea-150">Tag da associare all'istanza.</span><span class="sxs-lookup"><span data-stu-id="f53ea-150">The tags to associate with the instance.</span></span>

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

### <span data-ttu-id="f53ea-151">-VCore</span><span class="sxs-lookup"><span data-stu-id="f53ea-151">-VCore</span></span>
<span data-ttu-id="f53ea-152">Determina la quantità di VCore da associare all'istanza</span><span class="sxs-lookup"><span data-stu-id="f53ea-152">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="f53ea-153">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f53ea-153">-Confirm</span></span>
<span data-ttu-id="f53ea-154">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f53ea-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f53ea-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f53ea-155">-WhatIf</span></span>
<span data-ttu-id="f53ea-156">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f53ea-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f53ea-157">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f53ea-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f53ea-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f53ea-158">CommonParameters</span></span>
<span data-ttu-id="f53ea-159">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f53ea-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f53ea-160">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f53ea-160">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f53ea-161">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f53ea-161">INPUTS</span></span>

### <span data-ttu-id="f53ea-162">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="f53ea-162">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="f53ea-163">System. String</span><span class="sxs-lookup"><span data-stu-id="f53ea-163">System.String</span></span>

## <span data-ttu-id="f53ea-164">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f53ea-164">OUTPUTS</span></span>

### <span data-ttu-id="f53ea-165">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="f53ea-165">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="f53ea-166">Note</span><span class="sxs-lookup"><span data-stu-id="f53ea-166">NOTES</span></span>

## <span data-ttu-id="f53ea-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f53ea-167">RELATED LINKS</span></span>
