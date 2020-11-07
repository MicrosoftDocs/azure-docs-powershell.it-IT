---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationTask.md
ms.openlocfilehash: 65330f1024820c725cfb9a6b142000866063dc37
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684502"
---
# <span data-ttu-id="8cfe7-101">Get-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="8cfe7-101">Get-AzDataMigrationTask</span></span>

## <span data-ttu-id="8cfe7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8cfe7-102">SYNOPSIS</span></span>
<span data-ttu-id="8cfe7-103">Recupera l'oggetto PSProjectTask associato a un'attività di migrazione del servizio di migrazione del database di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cfe7-103">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="8cfe7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8cfe7-104">SYNTAX</span></span>

### <span data-ttu-id="8cfe7-105">ListByComponent (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8cfe7-105">ListByComponent (Default)</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-TaskType <TaskTypeEnum>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8cfe7-106">ListByInputObject</span><span class="sxs-lookup"><span data-stu-id="8cfe7-106">ListByInputObject</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8cfe7-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="8cfe7-107">GetByInputObject</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8cfe7-108">GetByInputObjectResultType</span><span class="sxs-lookup"><span data-stu-id="8cfe7-108">GetByInputObjectResultType</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8cfe7-109">ListByResourceId</span><span class="sxs-lookup"><span data-stu-id="8cfe7-109">ListByResourceId</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8cfe7-110">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8cfe7-110">GetByResourceId</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8cfe7-111">GetByResourceIdResultType</span><span class="sxs-lookup"><span data-stu-id="8cfe7-111">GetByResourceIdResultType</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8cfe7-112">GetByComponent</span><span class="sxs-lookup"><span data-stu-id="8cfe7-112">GetByComponent</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-Name <String>] [-Expand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8cfe7-113">GetByComponentResultType</span><span class="sxs-lookup"><span data-stu-id="8cfe7-113">GetByComponentResultType</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String> -Name <String>
 [-Expand] -ResultType <ResultTypeEnum> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8cfe7-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8cfe7-114">DESCRIPTION</span></span>
<span data-ttu-id="8cfe7-115">Il cmdlet Get-AzDataMigrationTask recupera le proprietà associate a un'attività di migrazione del servizio di migrazione del database di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cfe7-115">The Get-AzDataMigrationTask cmdlet retrieves the properties associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="8cfe7-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8cfe7-116">EXAMPLES</span></span>

### <span data-ttu-id="8cfe7-117">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8cfe7-117">Example 1</span></span>
```
PS C:\> Get -AzDataMigrationTask -TaskName myTestTask -ServiceName myTestService -ProjectName MyTestProject -ResourceGroupName MyResourceGroup -Expand
```

<span data-ttu-id="8cfe7-118">Nell'esempio precedente viene illustrato l'uso del cmdlet Get-AzDataMigrationTask per recuperare le proprietà associate a un'attività di migrazione del servizio di migrazione del database di Azure in base al nome dell'attività passato come parametro di input</span><span class="sxs-lookup"><span data-stu-id="8cfe7-118">The above example illustrates the use of Get-AzDataMigrationTask cmdlet to retrieve the properties associated with an Azure Database Migration Service migration task based on task name passed in as input parameter</span></span>

### <span data-ttu-id="8cfe7-119">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="8cfe7-119">Example 2</span></span>
```
PS C:\> Get -AzDataMigrationTask -Project $myProject
```

<span data-ttu-id="8cfe7-120">Nell'esempio precedente viene illustrato l'uso del cmdlet Get-AzDataMigrationTask per recuperare tutte le attività di migrazione associate all'oggetto PSProject passato come parametro di input</span><span class="sxs-lookup"><span data-stu-id="8cfe7-120">The above example illustrates the use of Get-AzDataMigrationTask cmdlet to retrieve all of the migration tasks associated with PSProject object passed in as input parameter</span></span>

## <span data-ttu-id="8cfe7-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8cfe7-121">PARAMETERS</span></span>

### <span data-ttu-id="8cfe7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cfe7-122">-DefaultProfile</span></span>
<span data-ttu-id="8cfe7-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8cfe7-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8cfe7-124">-Espandi</span><span class="sxs-lookup"><span data-stu-id="8cfe7-124">-Expand</span></span>
<span data-ttu-id="8cfe7-125">Espandi output</span><span class="sxs-lookup"><span data-stu-id="8cfe7-125">Expand output</span></span>

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

### <span data-ttu-id="8cfe7-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8cfe7-126">-InputObject</span></span>
<span data-ttu-id="8cfe7-127">Oggetto PSProject.</span><span class="sxs-lookup"><span data-stu-id="8cfe7-127">PSProject Object.</span></span>

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

### <span data-ttu-id="8cfe7-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="8cfe7-128">-Name</span></span>
<span data-ttu-id="8cfe7-129">Nome dell'attività.</span><span class="sxs-lookup"><span data-stu-id="8cfe7-129">The name of the task.</span></span>

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

### <span data-ttu-id="8cfe7-130">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="8cfe7-130">-ProjectName</span></span>
<span data-ttu-id="8cfe7-131">Nome del progetto.</span><span class="sxs-lookup"><span data-stu-id="8cfe7-131">The name of the project.</span></span>

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

### <span data-ttu-id="8cfe7-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cfe7-132">-ResourceGroupName</span></span>
<span data-ttu-id="8cfe7-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8cfe7-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="8cfe7-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8cfe7-134">-ResourceId</span></span>
<span data-ttu-id="8cfe7-135">ID risorsa progetto.</span><span class="sxs-lookup"><span data-stu-id="8cfe7-135">Project Resource Id.</span></span>

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

### <span data-ttu-id="8cfe7-136">-ResultType</span><span class="sxs-lookup"><span data-stu-id="8cfe7-136">-ResultType</span></span>
<span data-ttu-id="8cfe7-137">Espandere l'output di un tipo di risultato specifico.</span><span class="sxs-lookup"><span data-stu-id="8cfe7-137">Expand output of given result type.</span></span>

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

### <span data-ttu-id="8cfe7-138">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="8cfe7-138">-ServiceName</span></span>
<span data-ttu-id="8cfe7-139">Nome del servizio di migrazione del database.</span><span class="sxs-lookup"><span data-stu-id="8cfe7-139">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="8cfe7-140">-TaskType</span><span class="sxs-lookup"><span data-stu-id="8cfe7-140">-TaskType</span></span>
<span data-ttu-id="8cfe7-141">Filtrare in base a TaskType.</span><span class="sxs-lookup"><span data-stu-id="8cfe7-141">Filter by TaskType.</span></span>

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

### <span data-ttu-id="8cfe7-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cfe7-142">CommonParameters</span></span>
<span data-ttu-id="8cfe7-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cfe7-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cfe7-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cfe7-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cfe7-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8cfe7-145">INPUTS</span></span>

### <span data-ttu-id="8cfe7-146">Microsoft. Azure. Commands. DataMigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="8cfe7-146">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="8cfe7-147">System. String</span><span class="sxs-lookup"><span data-stu-id="8cfe7-147">System.String</span></span>

## <span data-ttu-id="8cfe7-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8cfe7-148">OUTPUTS</span></span>

### <span data-ttu-id="8cfe7-149">Microsoft. Azure. Commands. DataMigration. Models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="8cfe7-149">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="8cfe7-150">Note</span><span class="sxs-lookup"><span data-stu-id="8cfe7-150">NOTES</span></span>

## <span data-ttu-id="8cfe7-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8cfe7-151">RELATED LINKS</span></span>