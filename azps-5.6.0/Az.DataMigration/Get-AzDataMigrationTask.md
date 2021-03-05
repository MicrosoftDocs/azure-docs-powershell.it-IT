---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/Get-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationTask.md
ms.openlocfilehash: 08f87d40eec10f10b12f568cae8e899f5b7468d4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964750"
---
# <span data-ttu-id="7c7c3-101">Get-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="7c7c3-101">Get-AzDataMigrationTask</span></span>

## <span data-ttu-id="7c7c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c7c3-102">SYNOPSIS</span></span>
<span data-ttu-id="7c7c3-103">Recupera l'oggetto PSProjectTask associato a un'attività di migrazione del servizio di migrazione del database di Azure.</span><span class="sxs-lookup"><span data-stu-id="7c7c3-103">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="7c7c3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7c7c3-104">SYNTAX</span></span>

### <span data-ttu-id="7c7c3-105">ListByBy(impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7c7c3-105">ListByComponent (Default)</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-TaskType <TaskTypeEnum>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c7c3-106">ListByInputObject</span><span class="sxs-lookup"><span data-stu-id="7c7c3-106">ListByInputObject</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c7c3-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="7c7c3-107">GetByInputObject</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c7c3-108">GetByInputObjectResultType</span><span class="sxs-lookup"><span data-stu-id="7c7c3-108">GetByInputObjectResultType</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c7c3-109">ListByResourceId</span><span class="sxs-lookup"><span data-stu-id="7c7c3-109">ListByResourceId</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c7c3-110">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7c7c3-110">GetByResourceId</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c7c3-111">GetByResourceIdResultType</span><span class="sxs-lookup"><span data-stu-id="7c7c3-111">GetByResourceIdResultType</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c7c3-112">GetByByBy</span><span class="sxs-lookup"><span data-stu-id="7c7c3-112">GetByComponent</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-Name <String>] [-Expand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c7c3-113">GetByResultType</span><span class="sxs-lookup"><span data-stu-id="7c7c3-113">GetByComponentResultType</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String> -Name <String>
 [-Expand] -ResultType <ResultTypeEnum> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c7c3-114">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7c7c3-114">DESCRIPTION</span></span>
<span data-ttu-id="7c7c3-115">Il Get-AzDataMigrationTask cmdlet recupera le proprietà associate a un'attività di migrazione del servizio di migrazione del database di Azure.</span><span class="sxs-lookup"><span data-stu-id="7c7c3-115">The Get-AzDataMigrationTask cmdlet retrieves the properties associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="7c7c3-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7c7c3-116">EXAMPLES</span></span>

### <span data-ttu-id="7c7c3-117">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7c7c3-117">Example 1</span></span>
```
PS C:\> Get -AzDataMigrationTask -TaskName myTestTask -ServiceName myTestService -ProjectName MyTestProject -ResourceGroupName MyResourceGroup -Expand
```

<span data-ttu-id="7c7c3-118">L'esempio precedente illustra l'uso del cmdlet Get-AzDataMigrationTask per recuperare le proprietà associate a un'attività di migrazione del servizio di migrazione di database di Azure in base al nome dell'attività passato come parametro di input</span><span class="sxs-lookup"><span data-stu-id="7c7c3-118">The above example illustrates the use of Get-AzDataMigrationTask cmdlet to retrieve the properties associated with an Azure Database Migration Service migration task based on task name passed in as input parameter</span></span>

### <span data-ttu-id="7c7c3-119">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7c7c3-119">Example 2</span></span>
```
PS C:\> Get -AzDataMigrationTask -Project $myProject
```

<span data-ttu-id="7c7c3-120">L'esempio precedente illustra l'uso Get-AzDataMigrationTask cmdlet per recuperare tutte le attività di migrazione associate all'oggetto PSProject passato come parametro di input</span><span class="sxs-lookup"><span data-stu-id="7c7c3-120">The above example illustrates the use of Get-AzDataMigrationTask cmdlet to retrieve all of the migration tasks associated with PSProject object passed in as input parameter</span></span>

## <span data-ttu-id="7c7c3-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c7c3-121">PARAMETERS</span></span>

### <span data-ttu-id="7c7c3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c7c3-122">-DefaultProfile</span></span>
<span data-ttu-id="7c7c3-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7c7c3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c7c3-124">-Expand</span><span class="sxs-lookup"><span data-stu-id="7c7c3-124">-Expand</span></span>
<span data-ttu-id="7c7c3-125">Espandere l'output</span><span class="sxs-lookup"><span data-stu-id="7c7c3-125">Expand output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByInputObject, GetByResourceId, GetByComponent
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c7c3-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c7c3-126">-InputObject</span></span>
<span data-ttu-id="7c7c3-127">Oggetto PSProject.</span><span class="sxs-lookup"><span data-stu-id="7c7c3-127">PSProject Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProject
Parameter Sets: ListByInputObject
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProject
Parameter Sets: GetByInputObject, GetByInputObjectResultType
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c7c3-128">-Name</span><span class="sxs-lookup"><span data-stu-id="7c7c3-128">-Name</span></span>
<span data-ttu-id="7c7c3-129">Nome dell'attività.</span><span class="sxs-lookup"><span data-stu-id="7c7c3-129">The name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByInputObject, GetByInputObjectResultType, GetByResourceId, GetByResourceIdResultType, GetByComponentResultType
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByComponent
Aliases: TaskName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c7c3-130">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="7c7c3-130">-ProjectName</span></span>
<span data-ttu-id="7c7c3-131">Nome del progetto.</span><span class="sxs-lookup"><span data-stu-id="7c7c3-131">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c7c3-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c7c3-132">-ResourceGroupName</span></span>
<span data-ttu-id="7c7c3-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7c7c3-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c7c3-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c7c3-134">-ResourceId</span></span>
<span data-ttu-id="7c7c3-135">ID risorsa progetto.</span><span class="sxs-lookup"><span data-stu-id="7c7c3-135">Project Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceId, GetByResourceIdResultType
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c7c3-136">-ResultType</span><span class="sxs-lookup"><span data-stu-id="7c7c3-136">-ResultType</span></span>
<span data-ttu-id="7c7c3-137">Espandere l'output del tipo di risultato specificato.</span><span class="sxs-lookup"><span data-stu-id="7c7c3-137">Expand output of given result type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.ResultTypeEnum
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases:
Accepted values: MigrationLevelOutput, DatabaseLevelOutput, TableLevelOutput, MigrationValidationOutput, MigrationValidationDatabaseLevelOutput, LoginLevelOutput, AgentJobLevelOutput, Command

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c7c3-138">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="7c7c3-138">-ServiceName</span></span>
<span data-ttu-id="7c7c3-139">Nome del servizio di migrazione del database.</span><span class="sxs-lookup"><span data-stu-id="7c7c3-139">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c7c3-140">-TaskType</span><span class="sxs-lookup"><span data-stu-id="7c7c3-140">-TaskType</span></span>
<span data-ttu-id="7c7c3-141">Filtrare in base a TaskType.</span><span class="sxs-lookup"><span data-stu-id="7c7c3-141">Filter by TaskType.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.DataMigration.Models.TaskTypeEnum]
Parameter Sets: ListByComponent, ListByInputObject, ListByResourceId
Aliases:
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql, ConnectToTargetSqlDbMi, MigrateSqlServerSqlDbMi, ValidateSqlServerSqlDbMi, MigrateSqlServerSqlDbSync, ConnectToSourceSqlServerSync, ConnectToTargetSqlSync, GetUserTablesSqlSync, ValidateSqlServerSqlDbSync

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c7c3-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c7c3-142">CommonParameters</span></span>
<span data-ttu-id="7c7c3-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c7c3-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c7c3-144">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c7c3-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c7c3-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="7c7c3-145">INPUTS</span></span>

### <span data-ttu-id="7c7c3-146">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span><span class="sxs-lookup"><span data-stu-id="7c7c3-146">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="7c7c3-147">System.String</span><span class="sxs-lookup"><span data-stu-id="7c7c3-147">System.String</span></span>

## <span data-ttu-id="7c7c3-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7c7c3-148">OUTPUTS</span></span>

### <span data-ttu-id="7c7c3-149">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="7c7c3-149">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="7c7c3-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="7c7c3-150">NOTES</span></span>

## <span data-ttu-id="7c7c3-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7c7c3-151">RELATED LINKS</span></span>
