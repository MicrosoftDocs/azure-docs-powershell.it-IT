---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlInstance.md
ms.openlocfilehash: 025a9acc53405aeb1e211473b5f8f13066791714
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521305"
---
# <span data-ttu-id="cd0f2-101">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="cd0f2-101">New-AzureRmSqlInstance</span></span>

## <span data-ttu-id="cd0f2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cd0f2-102">SYNOPSIS</span></span>
<span data-ttu-id="cd0f2-103">Crea un'istanza gestita di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="cd0f2-103">Creates an Azure SQL Database Managed Instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd0f2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cd0f2-104">SYNTAX</span></span>

### <span data-ttu-id="cd0f2-105">NewByEditionAndComputeGenerationParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cd0f2-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzureRmSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> -LicenseType <String> -StorageSizeInGB <Int32> -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Tag <Hashtable>] [-AssignIdentity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd0f2-106">NewBySkuNameParameterSetParameter</span><span class="sxs-lookup"><span data-stu-id="cd0f2-106">NewBySkuNameParameterSetParameter</span></span>
```
New-AzureRmSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> -LicenseType <String> -StorageSizeInGB <Int32> -VCore <Int32>
 -SkuName <String> [-Tag <Hashtable>] [-AssignIdentity] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd0f2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd0f2-107">DESCRIPTION</span></span>
<span data-ttu-id="cd0f2-108">Il cmdlet **New-AzureRmSqlInstance** crea un'istanza gestita di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="cd0f2-108">The **New-AzureRmSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="cd0f2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cd0f2-109">EXAMPLES</span></span>

### <span data-ttu-id="cd0f2-110">Esempio 1: creare una nuova istanza</span><span class="sxs-lookup"><span data-stu-id="cd0f2-110">Example 1: Create a new instance</span></span>
```
PS C:\>New-AzureRmSqlInstance -Name managedInstance1 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -SkuName GP_Gen4
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

<span data-ttu-id="cd0f2-111">Questo comando crea una nuova istanza usando i parametri Edition e ComputeGeneration.</span><span class="sxs-lookup"><span data-stu-id="cd0f2-111">This command creates a new instance by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="cd0f2-112">Esempio 2: creare una nuova istanza</span><span class="sxs-lookup"><span data-stu-id="cd0f2-112">Example 2: Create a new instance</span></span>
```
PS C:\>New-AzureRmSqlInstance -Name managedInstance2 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -Edition "GeneralPurpose" -ComputeGeneration Gen4
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

<span data-ttu-id="cd0f2-113">Questo comando crea una nuova istanza usando i parametri Edition e ComputeGeneration.</span><span class="sxs-lookup"><span data-stu-id="cd0f2-113">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

## <span data-ttu-id="cd0f2-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cd0f2-114">PARAMETERS</span></span>

### <span data-ttu-id="cd0f2-115">-AdministratorCredential</span><span class="sxs-lookup"><span data-stu-id="cd0f2-115">-AdministratorCredential</span></span>
<span data-ttu-id="cd0f2-116">Credenziali di autenticazione SQL dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="cd0f2-116">The SQL authentication credential of the instance.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd0f2-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd0f2-117">-AsJob</span></span>
<span data-ttu-id="cd0f2-118">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="cd0f2-118">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd0f2-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="cd0f2-119">-AssignIdentity</span></span>
<span data-ttu-id="cd0f2-120">Genera e assegna un'identità di Azure Active Directory per questa istanza gestita per l'uso con i servizi di gestione delle chiavi, ad esempio Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="cd0f2-120">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd0f2-121">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="cd0f2-121">-ComputeGeneration</span></span>
<span data-ttu-id="cd0f2-122">Generazione di COMPUTE per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="cd0f2-122">The compute generation for the instance.</span></span>

```yaml
Type: String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd0f2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd0f2-123">-DefaultProfile</span></span>
<span data-ttu-id="cd0f2-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cd0f2-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd0f2-125">-Edition</span><span class="sxs-lookup"><span data-stu-id="cd0f2-125">-Edition</span></span>
<span data-ttu-id="cd0f2-126">L'edizione per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="cd0f2-126">The edition for the instance.</span></span>

```yaml
Type: String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd0f2-127">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="cd0f2-127">-LicenseType</span></span>
<span data-ttu-id="cd0f2-128">Determina il tipo di licenza di istanza da usare</span><span class="sxs-lookup"><span data-stu-id="cd0f2-128">Determines which License Type of instance to use</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd0f2-129">-Posizione</span><span class="sxs-lookup"><span data-stu-id="cd0f2-129">-Location</span></span>
<span data-ttu-id="cd0f2-130">Posizione in cui creare l'istanza</span><span class="sxs-lookup"><span data-stu-id="cd0f2-130">The location in which to create the instance</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd0f2-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="cd0f2-131">-Name</span></span>
<span data-ttu-id="cd0f2-132">Nome istanza.</span><span class="sxs-lookup"><span data-stu-id="cd0f2-132">Instance name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd0f2-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd0f2-133">-ResourceGroupName</span></span>
<span data-ttu-id="cd0f2-134">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cd0f2-134">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd0f2-135">-SkuName</span><span class="sxs-lookup"><span data-stu-id="cd0f2-135">-SkuName</span></span>
<span data-ttu-id="cd0f2-136">Nome USK per l'istanza, ad esempio "GP_Gen4", "BC_Gen4".</span><span class="sxs-lookup"><span data-stu-id="cd0f2-136">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

```yaml
Type: String
Parameter Sets: NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd0f2-137">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="cd0f2-137">-StorageSizeInGB</span></span>
<span data-ttu-id="cd0f2-138">Determina la quantità di spazio di archiviazione da associare all'istanza</span><span class="sxs-lookup"><span data-stu-id="cd0f2-138">Determines how much Storage size to associate with instance</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd0f2-139">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="cd0f2-139">-SubnetId</span></span>
<span data-ttu-id="cd0f2-140">ID subnet da usare per la creazione di istanze</span><span class="sxs-lookup"><span data-stu-id="cd0f2-140">The Subnet Id to use for instance creation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd0f2-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="cd0f2-141">-Tag</span></span>
<span data-ttu-id="cd0f2-142">Tag da associare all'istanza</span><span class="sxs-lookup"><span data-stu-id="cd0f2-142">The tags to associate with the instance</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd0f2-143">-VCore</span><span class="sxs-lookup"><span data-stu-id="cd0f2-143">-VCore</span></span>
<span data-ttu-id="cd0f2-144">Determina la quantità di VCore da associare all'istanza</span><span class="sxs-lookup"><span data-stu-id="cd0f2-144">Determines how much VCore to associate with instance</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd0f2-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cd0f2-145">-Confirm</span></span>
<span data-ttu-id="cd0f2-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd0f2-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd0f2-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd0f2-147">-WhatIf</span></span>
<span data-ttu-id="cd0f2-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd0f2-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd0f2-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd0f2-149">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd0f2-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd0f2-150">CommonParameters</span></span>
<span data-ttu-id="cd0f2-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd0f2-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd0f2-152">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd0f2-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd0f2-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cd0f2-153">INPUTS</span></span>

### <span data-ttu-id="cd0f2-154">Nessuno</span><span class="sxs-lookup"><span data-stu-id="cd0f2-154">None</span></span>

## <span data-ttu-id="cd0f2-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cd0f2-155">OUTPUTS</span></span>

### <span data-ttu-id="cd0f2-156">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="cd0f2-156">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="cd0f2-157">Note</span><span class="sxs-lookup"><span data-stu-id="cd0f2-157">NOTES</span></span>

## <span data-ttu-id="cd0f2-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cd0f2-158">RELATED LINKS</span></span>
