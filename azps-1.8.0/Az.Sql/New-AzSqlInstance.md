---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
ms.openlocfilehash: bfa1785004e13400395bd6a6fc93bdec29a69809
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676849"
---
# <span data-ttu-id="0c6de-101">New-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="0c6de-101">New-AzSqlInstance</span></span>

## <span data-ttu-id="0c6de-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0c6de-102">SYNOPSIS</span></span>
<span data-ttu-id="0c6de-103">Crea un'istanza gestita di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="0c6de-103">Creates an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="0c6de-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0c6de-104">SYNTAX</span></span>

### <span data-ttu-id="0c6de-105">NewByEditionAndComputeGenerationParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0c6de-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> -LicenseType <String> -StorageSizeInGB <Int32> -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c6de-106">NewBySkuNameParameterSetParameter</span><span class="sxs-lookup"><span data-stu-id="0c6de-106">NewBySkuNameParameterSetParameter</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> -LicenseType <String> -StorageSizeInGB <Int32> -VCore <Int32>
 -SkuName <String> [-Collation <String>] [-PublicDataEndpointEnabled] [-ProxyOverride <String>]
 [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c6de-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c6de-107">DESCRIPTION</span></span>
<span data-ttu-id="0c6de-108">Il cmdlet **New-AzSqlInstance** crea un'istanza gestita di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="0c6de-108">The **New-AzSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="0c6de-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0c6de-109">EXAMPLES</span></span>

### <span data-ttu-id="0c6de-110">Esempio 1: creare una nuova istanza</span><span class="sxs-lookup"><span data-stu-id="0c6de-110">Example 1: Create a new instance</span></span>
```
PS C:\>New-AzSqlInstance -Name managedInstance1 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -SkuName GP_Gen4
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
```

<span data-ttu-id="0c6de-111">Questo comando crea una nuova istanza usando i parametri Edition e ComputeGeneration.</span><span class="sxs-lookup"><span data-stu-id="0c6de-111">This command creates a new instance by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="0c6de-112">Esempio 2: creare una nuova istanza</span><span class="sxs-lookup"><span data-stu-id="0c6de-112">Example 2: Create a new instance</span></span>
```
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
```

<span data-ttu-id="0c6de-113">Questo comando crea una nuova istanza usando i parametri Edition e ComputeGeneration.</span><span class="sxs-lookup"><span data-stu-id="0c6de-113">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

## <span data-ttu-id="0c6de-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0c6de-114">PARAMETERS</span></span>

### <span data-ttu-id="0c6de-115">-AdministratorCredential</span><span class="sxs-lookup"><span data-stu-id="0c6de-115">-AdministratorCredential</span></span>
<span data-ttu-id="0c6de-116">Credenziali di autenticazione SQL dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="0c6de-116">The SQL authentication credential of the instance.</span></span>

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

### <span data-ttu-id="0c6de-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0c6de-117">-AsJob</span></span>
<span data-ttu-id="0c6de-118">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="0c6de-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0c6de-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="0c6de-119">-AssignIdentity</span></span>
<span data-ttu-id="0c6de-120">Genera e assegna un'identità di Azure Active Directory per questa istanza gestita per l'uso con i servizi di gestione delle chiavi, ad esempio Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="0c6de-120">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="0c6de-121">-Regole di confronto</span><span class="sxs-lookup"><span data-stu-id="0c6de-121">-Collation</span></span>
<span data-ttu-id="0c6de-122">Regole di confronto dell'istanza gestita di Azure SQL da usare.</span><span class="sxs-lookup"><span data-stu-id="0c6de-122">The collation of the Azure SQL Managed Instance to use.</span></span>

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

### <span data-ttu-id="0c6de-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="0c6de-123">-ComputeGeneration</span></span>
<span data-ttu-id="0c6de-124">Generazione di COMPUTE per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="0c6de-124">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="0c6de-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c6de-125">-DefaultProfile</span></span>
<span data-ttu-id="0c6de-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0c6de-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c6de-127">-Edition</span><span class="sxs-lookup"><span data-stu-id="0c6de-127">-Edition</span></span>
<span data-ttu-id="0c6de-128">L'edizione per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="0c6de-128">The edition for the instance.</span></span>

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

### <span data-ttu-id="0c6de-129">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="0c6de-129">-LicenseType</span></span>
<span data-ttu-id="0c6de-130">Determina il tipo di licenza da usare.</span><span class="sxs-lookup"><span data-stu-id="0c6de-130">Determines which License Type to use.</span></span> <span data-ttu-id="0c6de-131">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="0c6de-131">Possible values are:</span></span>
- <span data-ttu-id="0c6de-132">BasePrice-Azure Hybrid benefit (AHB) i prezzi scontati per i proprietari di licenze di SQL Server esistenti vengono applicati.</span><span class="sxs-lookup"><span data-stu-id="0c6de-132">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="0c6de-133">Il prezzo del servizio istanza gestito verrà scontato per i proprietari di licenze di SQL Server esistenti.</span><span class="sxs-lookup"><span data-stu-id="0c6de-133">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="0c6de-134">LicenseIncluded-Azure Hybrid benefit (AHB) i prezzi di sconto per i proprietari di licenze di SQL Server esistenti non vengono applicati.</span><span class="sxs-lookup"><span data-stu-id="0c6de-134">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="0c6de-135">Il prezzo del servizio istanza gestito includerà un nuovo costo per la licenza di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0c6de-135">Managed Instance service price will include a new SQL Server license costs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c6de-136">-Posizione</span><span class="sxs-lookup"><span data-stu-id="0c6de-136">-Location</span></span>
<span data-ttu-id="0c6de-137">Posizione in cui creare l'istanza</span><span class="sxs-lookup"><span data-stu-id="0c6de-137">The location in which to create the instance</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c6de-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="0c6de-138">-Name</span></span>
<span data-ttu-id="0c6de-139">Nome istanza.</span><span class="sxs-lookup"><span data-stu-id="0c6de-139">Instance name.</span></span>

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

### <span data-ttu-id="0c6de-140">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="0c6de-140">-ProxyOverride</span></span>
<span data-ttu-id="0c6de-141">Tipo di connessione usato per la connessione all'istanza.</span><span class="sxs-lookup"><span data-stu-id="0c6de-141">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="0c6de-142">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="0c6de-142">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="0c6de-143">Indipendentemente dal fatto che l'endpoint di dati pubblici sia abilitato per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="0c6de-143">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="0c6de-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c6de-144">-ResourceGroupName</span></span>
<span data-ttu-id="0c6de-145">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0c6de-145">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c6de-146">-SkuName</span><span class="sxs-lookup"><span data-stu-id="0c6de-146">-SkuName</span></span>
<span data-ttu-id="0c6de-147">Nome USK per l'istanza, ad esempio "GP_Gen4", "BC_Gen4".</span><span class="sxs-lookup"><span data-stu-id="0c6de-147">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

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

### <span data-ttu-id="0c6de-148">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="0c6de-148">-StorageSizeInGB</span></span>
<span data-ttu-id="0c6de-149">Determina la quantità di spazio di archiviazione da associare all'istanza</span><span class="sxs-lookup"><span data-stu-id="0c6de-149">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="0c6de-150">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="0c6de-150">-SubnetId</span></span>
<span data-ttu-id="0c6de-151">ID subnet da usare per la creazione di istanze</span><span class="sxs-lookup"><span data-stu-id="0c6de-151">The Subnet Id to use for instance creation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c6de-152">-Tag</span><span class="sxs-lookup"><span data-stu-id="0c6de-152">-Tag</span></span>
<span data-ttu-id="0c6de-153">Tag da associare all'istanza</span><span class="sxs-lookup"><span data-stu-id="0c6de-153">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="0c6de-154">-TimezoneId</span><span class="sxs-lookup"><span data-stu-id="0c6de-154">-TimezoneId</span></span>
<span data-ttu-id="0c6de-155">ID del fuso orario per l'istanza da impostare.</span><span class="sxs-lookup"><span data-stu-id="0c6de-155">The time zone id for the instance to set.</span></span> <span data-ttu-id="0c6de-156">Un elenco di ID fuso orario viene esposto tramite la visualizzazione sys.time_zone_info (Transact-SQL).</span><span class="sxs-lookup"><span data-stu-id="0c6de-156">A list of time zone ids is exposed through the sys.time_zone_info (Transact-SQL) view.</span></span>

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

### <span data-ttu-id="0c6de-157">-VCore</span><span class="sxs-lookup"><span data-stu-id="0c6de-157">-VCore</span></span>
<span data-ttu-id="0c6de-158">Determina la quantità di VCore da associare all'istanza</span><span class="sxs-lookup"><span data-stu-id="0c6de-158">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="0c6de-159">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0c6de-159">-Confirm</span></span>
<span data-ttu-id="0c6de-160">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c6de-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c6de-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c6de-161">-WhatIf</span></span>
<span data-ttu-id="0c6de-162">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0c6de-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c6de-163">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0c6de-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c6de-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c6de-164">CommonParameters</span></span>
<span data-ttu-id="0c6de-165">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c6de-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c6de-166">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c6de-166">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c6de-167">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0c6de-167">INPUTS</span></span>

### <span data-ttu-id="0c6de-168">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0c6de-168">None</span></span>

## <span data-ttu-id="0c6de-169">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0c6de-169">OUTPUTS</span></span>

### <span data-ttu-id="0c6de-170">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="0c6de-170">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="0c6de-171">Note</span><span class="sxs-lookup"><span data-stu-id="0c6de-171">NOTES</span></span>

## <span data-ttu-id="0c6de-172">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0c6de-172">RELATED LINKS</span></span>
