---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstanceDatabase.md
ms.openlocfilehash: 6c8fdc5b54ca802c8c23df577fc0e0e39de0ba16
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197703"
---
# <span data-ttu-id="6146c-101">New-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6146c-101">New-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="6146c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6146c-102">SYNOPSIS</span></span>
<span data-ttu-id="6146c-103">Crea un database SQL istanza gestita di Azure.</span><span class="sxs-lookup"><span data-stu-id="6146c-103">Creates an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="6146c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6146c-104">SYNTAX</span></span>

### <span data-ttu-id="6146c-105">CreateNewInstanceDatabaseFromInputParameters (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6146c-105">CreateNewInstanceDatabaseFromInputParameters (Default)</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-InstanceName] <String> [-ResourceGroupName] <String>
 [-Collation <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6146c-106">CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="6146c-106">CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceObject] <AzureSqlManagedInstanceModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6146c-107">CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="6146c-107">CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6146c-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6146c-108">DESCRIPTION</span></span>
<span data-ttu-id="6146c-109">Il cmdlet **New-AzSqlInstanceDatabase** crea un database SQL istanza gestita di Azure.</span><span class="sxs-lookup"><span data-stu-id="6146c-109">The **New-AzSqlInstanceDatabase** cmdlet creates an Azure SQL Managed instance database.</span></span>

## <span data-ttu-id="6146c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6146c-110">EXAMPLES</span></span>

### <span data-ttu-id="6146c-111">Esempio 1: Creare un database in un'istanza specificata</span><span class="sxs-lookup"><span data-stu-id="6146c-111">Example 1: Create a database on a specified instance</span></span>
```
PS C:\>New-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/Database01
Name                     : Database01
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/27/2018 2:30:07 PM
EarliestRestorePoint     : 4/27/2018 2:40:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :
```

<span data-ttu-id="6146c-112">Questo comando crea un database di istanza denominato Database01 nell'istanza managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="6146c-112">This command creates a instance database named Database01 on instance managedInstance1.</span></span>

## <span data-ttu-id="6146c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6146c-113">PARAMETERS</span></span>

### <span data-ttu-id="6146c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6146c-114">-AsJob</span></span>
<span data-ttu-id="6146c-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="6146c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6146c-116">-Collation</span><span class="sxs-lookup"><span data-stu-id="6146c-116">-Collation</span></span>
<span data-ttu-id="6146c-117">Fascicolazione delle regole di confronto del SQL istanza di Azure da usare.</span><span class="sxs-lookup"><span data-stu-id="6146c-117">The collation of the Azure SQL Instance Database collation to use.</span></span>

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

### <span data-ttu-id="6146c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6146c-118">-DefaultProfile</span></span>
<span data-ttu-id="6146c-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6146c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6146c-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="6146c-120">-InstanceName</span></span>
<span data-ttu-id="6146c-121">Nome dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="6146c-121">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateNewInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6146c-122">-InstanceObject</span><span class="sxs-lookup"><span data-stu-id="6146c-122">-InstanceObject</span></span>
<span data-ttu-id="6146c-123">Oggetto istanza</span><span class="sxs-lookup"><span data-stu-id="6146c-123">The instance object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6146c-124">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="6146c-124">-InstanceResourceId</span></span>
<span data-ttu-id="6146c-125">ID risorsa dell'istanza</span><span class="sxs-lookup"><span data-stu-id="6146c-125">The instance resource id</span></span>

```yaml
Type: System.String
Parameter Sets: CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId
Aliases: ParentResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6146c-126">-Name</span><span class="sxs-lookup"><span data-stu-id="6146c-126">-Name</span></span>
<span data-ttu-id="6146c-127">Nome del database delle istanze SQL Azure da creare.</span><span class="sxs-lookup"><span data-stu-id="6146c-127">The name of the Azure SQL Instance Database to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6146c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6146c-128">-ResourceGroupName</span></span>
<span data-ttu-id="6146c-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6146c-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateNewInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6146c-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="6146c-130">-Tag</span></span>
<span data-ttu-id="6146c-131">I tag da associare al database dell'istanza SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="6146c-131">The tags to associate with the Azure Sql Instance Database</span></span>

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

### <span data-ttu-id="6146c-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6146c-132">-Confirm</span></span>
<span data-ttu-id="6146c-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6146c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6146c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6146c-134">-WhatIf</span></span>
<span data-ttu-id="6146c-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6146c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6146c-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6146c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6146c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6146c-137">CommonParameters</span></span>
<span data-ttu-id="6146c-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6146c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6146c-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6146c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6146c-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="6146c-140">INPUTS</span></span>

### <span data-ttu-id="6146c-141">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="6146c-141">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="6146c-142">System.String</span><span class="sxs-lookup"><span data-stu-id="6146c-142">System.String</span></span>

## <span data-ttu-id="6146c-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6146c-143">OUTPUTS</span></span>

### <span data-ttu-id="6146c-144">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="6146c-144">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="6146c-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="6146c-145">NOTES</span></span>

## <span data-ttu-id="6146c-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6146c-146">RELATED LINKS</span></span>
