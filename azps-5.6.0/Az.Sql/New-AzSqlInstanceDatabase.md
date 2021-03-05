---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstanceDatabase.md
ms.openlocfilehash: 559e23334f9fc98cd51f296aee243152578ba763
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977726"
---
# <span data-ttu-id="6d58d-101">New-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6d58d-101">New-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="6d58d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d58d-102">SYNOPSIS</span></span>
<span data-ttu-id="6d58d-103">Crea un database SQL istanza gestita di Azure.</span><span class="sxs-lookup"><span data-stu-id="6d58d-103">Creates an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="6d58d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6d58d-104">SYNTAX</span></span>

### <span data-ttu-id="6d58d-105">CreateNewInstanceDatabaseFromInputParameters (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6d58d-105">CreateNewInstanceDatabaseFromInputParameters (Default)</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-InstanceName] <String> [-ResourceGroupName] <String>
 [-Collation <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d58d-106">CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="6d58d-106">CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceObject] <AzureSqlManagedInstanceModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d58d-107">CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="6d58d-107">CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6d58d-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6d58d-108">DESCRIPTION</span></span>
<span data-ttu-id="6d58d-109">Il cmdlet **New-AzSqlInstanceDatabase** crea un database SQL istanza gestita di Azure.</span><span class="sxs-lookup"><span data-stu-id="6d58d-109">The **New-AzSqlInstanceDatabase** cmdlet creates an Azure SQL Managed instance database.</span></span>

## <span data-ttu-id="6d58d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6d58d-110">EXAMPLES</span></span>

### <span data-ttu-id="6d58d-111">Esempio 1: Creare un database in un'istanza specificata</span><span class="sxs-lookup"><span data-stu-id="6d58d-111">Example 1: Create a database on a specified instance</span></span>
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

<span data-ttu-id="6d58d-112">Questo comando crea un database di istanza denominato Database01 nell'istanza managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="6d58d-112">This command creates a instance database named Database01 on instance managedInstance1.</span></span>

## <span data-ttu-id="6d58d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d58d-113">PARAMETERS</span></span>

### <span data-ttu-id="6d58d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d58d-114">-AsJob</span></span>
<span data-ttu-id="6d58d-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="6d58d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6d58d-116">-Collation</span><span class="sxs-lookup"><span data-stu-id="6d58d-116">-Collation</span></span>
<span data-ttu-id="6d58d-117">Fascicolazione delle regole di confronto del SQL istanza di Azure da usare.</span><span class="sxs-lookup"><span data-stu-id="6d58d-117">The collation of the Azure SQL Instance Database collation to use.</span></span>

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

### <span data-ttu-id="6d58d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d58d-118">-DefaultProfile</span></span>
<span data-ttu-id="6d58d-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6d58d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d58d-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="6d58d-120">-InstanceName</span></span>
<span data-ttu-id="6d58d-121">Nome dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="6d58d-121">The instance name.</span></span>

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

### <span data-ttu-id="6d58d-122">-InstanceObject</span><span class="sxs-lookup"><span data-stu-id="6d58d-122">-InstanceObject</span></span>
<span data-ttu-id="6d58d-123">Oggetto istanza</span><span class="sxs-lookup"><span data-stu-id="6d58d-123">The instance object</span></span>

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

### <span data-ttu-id="6d58d-124">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="6d58d-124">-InstanceResourceId</span></span>
<span data-ttu-id="6d58d-125">ID risorsa dell'istanza</span><span class="sxs-lookup"><span data-stu-id="6d58d-125">The instance resource id</span></span>

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

### <span data-ttu-id="6d58d-126">-Name</span><span class="sxs-lookup"><span data-stu-id="6d58d-126">-Name</span></span>
<span data-ttu-id="6d58d-127">Nome del database delle istanze SQL Azure da creare.</span><span class="sxs-lookup"><span data-stu-id="6d58d-127">The name of the Azure SQL Instance Database to create.</span></span>

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

### <span data-ttu-id="6d58d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d58d-128">-ResourceGroupName</span></span>
<span data-ttu-id="6d58d-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6d58d-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="6d58d-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="6d58d-130">-Tag</span></span>
<span data-ttu-id="6d58d-131">I tag da associare al database dell'istanza SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="6d58d-131">The tags to associate with the Azure Sql Instance Database</span></span>

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

### <span data-ttu-id="6d58d-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d58d-132">-Confirm</span></span>
<span data-ttu-id="6d58d-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d58d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d58d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d58d-134">-WhatIf</span></span>
<span data-ttu-id="6d58d-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6d58d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d58d-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6d58d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d58d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d58d-137">CommonParameters</span></span>
<span data-ttu-id="6d58d-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d58d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d58d-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6d58d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d58d-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="6d58d-140">INPUTS</span></span>

### <span data-ttu-id="6d58d-141">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="6d58d-141">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="6d58d-142">System.String</span><span class="sxs-lookup"><span data-stu-id="6d58d-142">System.String</span></span>

## <span data-ttu-id="6d58d-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6d58d-143">OUTPUTS</span></span>

### <span data-ttu-id="6d58d-144">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="6d58d-144">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="6d58d-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="6d58d-145">NOTES</span></span>

## <span data-ttu-id="6d58d-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6d58d-146">RELATED LINKS</span></span>
