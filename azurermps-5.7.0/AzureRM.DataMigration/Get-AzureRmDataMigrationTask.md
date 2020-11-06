---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/get-azurermdatamigrationtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationTask.md
ms.openlocfilehash: 5ca6edfa811a1b73cbdaae59e8d3b0e2f76cc15f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514375"
---
# <span data-ttu-id="83297-101">Get-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="83297-101">Get-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="83297-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="83297-102">SYNOPSIS</span></span>
<span data-ttu-id="83297-103">Recupera l'oggetto PSProjectTask associato a un'attività di migrazione del servizio di migrazione del database di Azure.</span><span class="sxs-lookup"><span data-stu-id="83297-103">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83297-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="83297-104">SYNTAX</span></span>

### <span data-ttu-id="83297-105">ListByComponent (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="83297-105">ListByComponent (Default)</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-TaskType <TaskTypeEnum>] [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="83297-106">ListByInputObject</span><span class="sxs-lookup"><span data-stu-id="83297-106">ListByInputObject</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="83297-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="83297-107">GetByInputObject</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="83297-108">GetByInputObjectResultType</span><span class="sxs-lookup"><span data-stu-id="83297-108">GetByInputObjectResultType</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="83297-109">ListByResourceId</span><span class="sxs-lookup"><span data-stu-id="83297-109">ListByResourceId</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="83297-110">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="83297-110">GetByResourceId</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="83297-111">GetByResourceIdResultType</span><span class="sxs-lookup"><span data-stu-id="83297-111">GetByResourceIdResultType</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="83297-112">GetByComponent</span><span class="sxs-lookup"><span data-stu-id="83297-112">GetByComponent</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-Name <String>] [-Expand] [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="83297-113">GetByComponentResultType</span><span class="sxs-lookup"><span data-stu-id="83297-113">GetByComponentResultType</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Expand] -ResultType <ResultTypeEnum> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="83297-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="83297-114">DESCRIPTION</span></span>
<span data-ttu-id="83297-115">Il cmdlet Get-AzureRmDataMigrationTask recupera le proprietà associate a un'attività di migrazione del servizio di migrazione del database di Azure.</span><span class="sxs-lookup"><span data-stu-id="83297-115">The Get-AzureRmDataMigrationTask cmdlet retrieves the properties associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="83297-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="83297-116">EXAMPLES</span></span>

### <span data-ttu-id="83297-117">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="83297-117">Example 1</span></span>
```
PS C:\> Get -AzureRmDataMigrationTask -TaskName myTestTask -ServiceName myTestService -ProjectName MyTestProject -ResourceGroupName MyResourceGroup -Expand
```

<span data-ttu-id="83297-118">Nell'esempio precedente viene illustrato l'uso del cmdlet Get-AzureRmDataMigrationTask per recuperare le proprietà associate a un'attività di migrazione del servizio di migrazione del database di Azure in base al nome dell'attività passato come parametro di input</span><span class="sxs-lookup"><span data-stu-id="83297-118">The above example illustrates the use of Get-AzureRmDataMigrationTask cmdlet to retrieve the properties associated with an Azure Database Migration Service migration task based on task name passed in as input parameter</span></span>

### <span data-ttu-id="83297-119">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="83297-119">Example 2</span></span>
```
PS C:\> Get -AzureRmDataMigrationTask -Project $myProject
```

<span data-ttu-id="83297-120">Nell'esempio precedente viene illustrato l'uso del cmdlet Get-AzureRmDataMigrationTask per recuperare tutte le attività di migrazione associate all'oggetto PSProject passato come parametro di input</span><span class="sxs-lookup"><span data-stu-id="83297-120">The above example illustrates the use of Get-AzureRmDataMigrationTask cmdlet to retrieve all of the migration tasks associated with PSProject object passed in as input parameter</span></span>

## <span data-ttu-id="83297-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="83297-121">PARAMETERS</span></span>

### <span data-ttu-id="83297-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83297-122">-DefaultProfile</span></span>
<span data-ttu-id="83297-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="83297-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83297-124">-Espandi</span><span class="sxs-lookup"><span data-stu-id="83297-124">-Expand</span></span>
<span data-ttu-id="83297-125">Espandi output</span><span class="sxs-lookup"><span data-stu-id="83297-125">Expand output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: GetByInputObject, GetByResourceId, GetByComponent
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: SwitchParameter
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases: 

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83297-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83297-126">-InputObject</span></span>
<span data-ttu-id="83297-127">Oggetto PSProject.</span><span class="sxs-lookup"><span data-stu-id="83297-127">PSProject Object.</span></span>

```yaml
Type: PSProject
Parameter Sets: ListByInputObject
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: PSProject
Parameter Sets: GetByInputObject, GetByInputObjectResultType
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83297-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="83297-128">-Name</span></span>
<span data-ttu-id="83297-129">Nome dell'attività.</span><span class="sxs-lookup"><span data-stu-id="83297-129">The name of the task.</span></span>

```yaml
Type: String
Parameter Sets: GetByInputObject, GetByInputObjectResultType, GetByResourceId, GetByResourceIdResultType, GetByComponentResultType
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetByComponent
Aliases: TaskName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83297-130">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="83297-130">-ProjectName</span></span>
<span data-ttu-id="83297-131">Nome del progetto.</span><span class="sxs-lookup"><span data-stu-id="83297-131">The name of the project.</span></span>

```yaml
Type: String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83297-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83297-132">-ResourceGroupName</span></span>
<span data-ttu-id="83297-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="83297-133">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83297-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="83297-134">-ResourceId</span></span>
<span data-ttu-id="83297-135">ID risorsa progetto.</span><span class="sxs-lookup"><span data-stu-id="83297-135">Project Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ListByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetByResourceId, GetByResourceIdResultType
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83297-136">-ResultType</span><span class="sxs-lookup"><span data-stu-id="83297-136">-ResultType</span></span>
<span data-ttu-id="83297-137">Espandere l'output di un tipo di risultato specifico.</span><span class="sxs-lookup"><span data-stu-id="83297-137">Expand output of given result type.</span></span>

```yaml
Type: ResultTypeEnum
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases: 
Accepted values: MigrationLevelOutput, DatabaseLevelOutput, TableLevelOutput, MigrationValidationOutput, MigrationValidationDatabaseLevelOutput

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83297-138">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="83297-138">-ServiceName</span></span>
<span data-ttu-id="83297-139">Nome del servizio di migrazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="83297-139">Data Migration Service Name.</span></span>

```yaml
Type: String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83297-140">-TaskType</span><span class="sxs-lookup"><span data-stu-id="83297-140">-TaskType</span></span>
<span data-ttu-id="83297-141">Filtrare in base a TaskType.</span><span class="sxs-lookup"><span data-stu-id="83297-141">Filter by TaskType.</span></span>

```yaml
Type: TaskTypeEnum
Parameter Sets: ListByComponent, ListByInputObject, ListByResourceId
Aliases: 
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="83297-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="83297-142">INPUTS</span></span>

### <span data-ttu-id="83297-143">Microsoft. Azure. Commands. DataMigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="83297-143">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="83297-144">System. String</span><span class="sxs-lookup"><span data-stu-id="83297-144">System.String</span></span>

## <span data-ttu-id="83297-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="83297-145">OUTPUTS</span></span>

### <span data-ttu-id="83297-146">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. Commands. DataMigration. Models. PSProjectTask, Microsoft. Azure. Commands. DataMigration, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="83297-146">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask, Microsoft.Azure.Commands.DataMigration, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="83297-147">Note</span><span class="sxs-lookup"><span data-stu-id="83297-147">NOTES</span></span>

## <span data-ttu-id="83297-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="83297-148">RELATED LINKS</span></span>

