---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Get-AzureRmDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationTask.md
ms.openlocfilehash: caab43824c63e73e7011c0377d0bd7665befe5dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518700"
---
# <span data-ttu-id="3dedf-101">Get-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="3dedf-101">Get-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="3dedf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3dedf-102">SYNOPSIS</span></span>
<span data-ttu-id="3dedf-103">Recupera l'oggetto PSProjectTask associato a un'attività di migrazione del servizio di migrazione del database di Azure.</span><span class="sxs-lookup"><span data-stu-id="3dedf-103">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3dedf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3dedf-104">SYNTAX</span></span>

### <span data-ttu-id="3dedf-105">ListByComponent (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3dedf-105">ListByComponent (Default)</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-TaskType <TaskTypeEnum>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3dedf-106">ListByInputObject</span><span class="sxs-lookup"><span data-stu-id="3dedf-106">ListByInputObject</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3dedf-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="3dedf-107">GetByInputObject</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3dedf-108">GetByInputObjectResultType</span><span class="sxs-lookup"><span data-stu-id="3dedf-108">GetByInputObjectResultType</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3dedf-109">ListByResourceId</span><span class="sxs-lookup"><span data-stu-id="3dedf-109">ListByResourceId</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3dedf-110">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3dedf-110">GetByResourceId</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3dedf-111">GetByResourceIdResultType</span><span class="sxs-lookup"><span data-stu-id="3dedf-111">GetByResourceIdResultType</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3dedf-112">GetByComponent</span><span class="sxs-lookup"><span data-stu-id="3dedf-112">GetByComponent</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-Name <String>] [-Expand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3dedf-113">GetByComponentResultType</span><span class="sxs-lookup"><span data-stu-id="3dedf-113">GetByComponentResultType</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Expand] -ResultType <ResultTypeEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3dedf-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3dedf-114">DESCRIPTION</span></span>
<span data-ttu-id="3dedf-115">Il cmdlet Get-AzureRmDataMigrationTask recupera le proprietà associate a un'attività di migrazione del servizio di migrazione del database di Azure.</span><span class="sxs-lookup"><span data-stu-id="3dedf-115">The Get-AzureRmDataMigrationTask cmdlet retrieves the properties associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="3dedf-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3dedf-116">EXAMPLES</span></span>

### <span data-ttu-id="3dedf-117">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3dedf-117">Example 1</span></span>
```
PS C:\> Get -AzureRmDataMigrationTask -TaskName myTestTask -ServiceName myTestService -ProjectName MyTestProject -ResourceGroupName MyResourceGroup -Expand
```

<span data-ttu-id="3dedf-118">Nell'esempio precedente viene illustrato l'uso del cmdlet Get-AzureRmDataMigrationTask per recuperare le proprietà associate a un'attività di migrazione del servizio di migrazione del database di Azure in base al nome dell'attività passato come parametro di input</span><span class="sxs-lookup"><span data-stu-id="3dedf-118">The above example illustrates the use of Get-AzureRmDataMigrationTask cmdlet to retrieve the properties associated with an Azure Database Migration Service migration task based on task name passed in as input parameter</span></span>

### <span data-ttu-id="3dedf-119">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3dedf-119">Example 2</span></span>
```
PS C:\> Get -AzureRmDataMigrationTask -Project $myProject
```

<span data-ttu-id="3dedf-120">Nell'esempio precedente viene illustrato l'uso del cmdlet Get-AzureRmDataMigrationTask per recuperare tutte le attività di migrazione associate all'oggetto PSProject passato come parametro di input</span><span class="sxs-lookup"><span data-stu-id="3dedf-120">The above example illustrates the use of Get-AzureRmDataMigrationTask cmdlet to retrieve all of the migration tasks associated with PSProject object passed in as input parameter</span></span>

## <span data-ttu-id="3dedf-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3dedf-121">PARAMETERS</span></span>

### <span data-ttu-id="3dedf-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dedf-122">-DefaultProfile</span></span>
<span data-ttu-id="3dedf-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3dedf-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dedf-124">-Espandi</span><span class="sxs-lookup"><span data-stu-id="3dedf-124">-Expand</span></span>
<span data-ttu-id="3dedf-125">Espandi output</span><span class="sxs-lookup"><span data-stu-id="3dedf-125">Expand output</span></span>

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

### <span data-ttu-id="3dedf-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3dedf-126">-InputObject</span></span>
<span data-ttu-id="3dedf-127">Oggetto PSProject.</span><span class="sxs-lookup"><span data-stu-id="3dedf-127">PSProject Object.</span></span>

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

### <span data-ttu-id="3dedf-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="3dedf-128">-Name</span></span>
<span data-ttu-id="3dedf-129">Nome dell'attività.</span><span class="sxs-lookup"><span data-stu-id="3dedf-129">The name of the task.</span></span>

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

### <span data-ttu-id="3dedf-130">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="3dedf-130">-ProjectName</span></span>
<span data-ttu-id="3dedf-131">Nome del progetto.</span><span class="sxs-lookup"><span data-stu-id="3dedf-131">The name of the project.</span></span>

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

### <span data-ttu-id="3dedf-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dedf-132">-ResourceGroupName</span></span>
<span data-ttu-id="3dedf-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3dedf-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="3dedf-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3dedf-134">-ResourceId</span></span>
<span data-ttu-id="3dedf-135">ID risorsa progetto.</span><span class="sxs-lookup"><span data-stu-id="3dedf-135">Project Resource Id.</span></span>

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

### <span data-ttu-id="3dedf-136">-ResultType</span><span class="sxs-lookup"><span data-stu-id="3dedf-136">-ResultType</span></span>
<span data-ttu-id="3dedf-137">Espandere l'output di un tipo di risultato specifico.</span><span class="sxs-lookup"><span data-stu-id="3dedf-137">Expand output of given result type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.ResultTypeEnum
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases:
Accepted values: MigrationLevelOutput, DatabaseLevelOutput, TableLevelOutput, MigrationValidationOutput, MigrationValidationDatabaseLevelOutput, LoginLevelOutput, AgentJobLevelOutput

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dedf-138">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="3dedf-138">-ServiceName</span></span>
<span data-ttu-id="3dedf-139">Nome del servizio di migrazione del database.</span><span class="sxs-lookup"><span data-stu-id="3dedf-139">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="3dedf-140">-TaskType</span><span class="sxs-lookup"><span data-stu-id="3dedf-140">-TaskType</span></span>
<span data-ttu-id="3dedf-141">Filtrare in base a TaskType.</span><span class="sxs-lookup"><span data-stu-id="3dedf-141">Filter by TaskType.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.DataMigration.Models.TaskTypeEnum]
Parameter Sets: ListByComponent, ListByInputObject, ListByResourceId
Aliases:
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql, ConnectToTargetSqlDbMi, MigrateSqlServerSqlDbMi, ValidateSqlServerSqlDbMi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dedf-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dedf-142">CommonParameters</span></span>
<span data-ttu-id="3dedf-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dedf-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dedf-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3dedf-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dedf-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3dedf-145">INPUTS</span></span>

### <span data-ttu-id="3dedf-146">Microsoft. Azure. Commands. DataMigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="3dedf-146">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="3dedf-147">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3dedf-147">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="3dedf-148">System. String</span><span class="sxs-lookup"><span data-stu-id="3dedf-148">System.String</span></span>

## <span data-ttu-id="3dedf-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3dedf-149">OUTPUTS</span></span>

### <span data-ttu-id="3dedf-150">Microsoft. Azure. Commands. DataMigration. Models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="3dedf-150">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="3dedf-151">Note</span><span class="sxs-lookup"><span data-stu-id="3dedf-151">NOTES</span></span>

## <span data-ttu-id="3dedf-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3dedf-152">RELATED LINKS</span></span>
