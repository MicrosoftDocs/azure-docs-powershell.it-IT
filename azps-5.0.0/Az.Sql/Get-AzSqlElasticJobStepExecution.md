---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobstepexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStepExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStepExecution.md
ms.openlocfilehash: 03c4a6dede1f60e782bbfecdec1fb18894b2ca15
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202910"
---
# <span data-ttu-id="57b6d-101">Get-AzSqlElasticJobStepExecution</span><span class="sxs-lookup"><span data-stu-id="57b6d-101">Get-AzSqlElasticJobStepExecution</span></span>

## <span data-ttu-id="57b6d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="57b6d-102">SYNOPSIS</span></span>
<span data-ttu-id="57b6d-103">Ottiene una o più esecuzioni di passaggi del processo</span><span class="sxs-lookup"><span data-stu-id="57b6d-103">Gets one or more job step executions</span></span>

## <span data-ttu-id="57b6d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="57b6d-104">SYNTAX</span></span>

### <span data-ttu-id="57b6d-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="57b6d-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobStepExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>]
 [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="57b6d-106">WithJobStepName</span><span class="sxs-lookup"><span data-stu-id="57b6d-106">WithJobStepName</span></span>
```
Get-AzSqlElasticJobStepExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> -StepName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="57b6d-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="57b6d-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57b6d-108">WithJobStepNameUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="57b6d-108">WithJobStepNameUsingParentObject</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> -StepName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57b6d-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="57b6d-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentResourceId] <String> [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57b6d-110">WithJobStepNameUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="57b6d-110">WithJobStepNameUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentResourceId] <String> -StepName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57b6d-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="57b6d-111">DESCRIPTION</span></span>
<span data-ttu-id="57b6d-112">Il cmdlet Get-AzSqlElasticJobStepExecution ottiene una o più esecuzioni dei passaggi da un'esecuzione del processo</span><span class="sxs-lookup"><span data-stu-id="57b6d-112">The Get-AzSqlElasticJobStepExecution cmdlet gets one or more job step executions from a job execution</span></span>

## <span data-ttu-id="57b6d-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="57b6d-113">EXAMPLES</span></span>

### <span data-ttu-id="57b6d-114">Esempio 1: ottiene una o più esecuzioni di un passaggio di processo da un processo di esecuzione</span><span class="sxs-lookup"><span data-stu-id="57b6d-114">Example 1 - Gets one or more job step executions from a job executions</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobStepExecution

JobName JobVersion StepName StepId JobExecutionId                       Lifecycle StartTime            EndTime
------- ---------- -------- ------ --------------                       --------- ---------            -------
job1    1          step1    1      3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

### <span data-ttu-id="57b6d-115">Esempio 2: ottiene una o più esecuzioni di passaggi da un'esecuzione del processo, filtrando per nome passaggio</span><span class="sxs-lookup"><span data-stu-id="57b6d-115">Example 2 - Gets one or more job step executions from a job execution, filtering by step name</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobStepExecution -StepName step1

JobName JobVersion StepName StepId JobExecutionId                       Lifecycle StartTime            EndTime
------- ---------- -------- ------ --------------                       --------- ---------            -------
job1    1          step1    1      3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

<span data-ttu-id="57b6d-116">Ottiene una o più esecuzioni di passaggi del processo</span><span class="sxs-lookup"><span data-stu-id="57b6d-116">Gets one or more job step executions</span></span>

## <span data-ttu-id="57b6d-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="57b6d-117">PARAMETERS</span></span>

### <span data-ttu-id="57b6d-118">-Active</span><span class="sxs-lookup"><span data-stu-id="57b6d-118">-Active</span></span>
<span data-ttu-id="57b6d-119">Contrassegna per filtrare in base alle esecuzioni attive.</span><span class="sxs-lookup"><span data-stu-id="57b6d-119">Flag to filter by active executions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57b6d-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="57b6d-120">-AgentName</span></span>
<span data-ttu-id="57b6d-121">Nome dell'agente.</span><span class="sxs-lookup"><span data-stu-id="57b6d-121">The agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57b6d-122">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="57b6d-122">-CreateTimeMax</span></span>
<span data-ttu-id="57b6d-123">Filtra per crea tempo max</span><span class="sxs-lookup"><span data-stu-id="57b6d-123">Filter by create time max</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57b6d-124">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="57b6d-124">-CreateTimeMin</span></span>
<span data-ttu-id="57b6d-125">Filtrare per creare il tempo min</span><span class="sxs-lookup"><span data-stu-id="57b6d-125">Filter by create time min</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57b6d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57b6d-126">-DefaultProfile</span></span>
<span data-ttu-id="57b6d-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="57b6d-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57b6d-128">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="57b6d-128">-EndTimeMax</span></span>
<span data-ttu-id="57b6d-129">Filtrare per ora di fine max.</span><span class="sxs-lookup"><span data-stu-id="57b6d-129">Filter by end time max.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57b6d-130">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="57b6d-130">-EndTimeMin</span></span>
<span data-ttu-id="57b6d-131">Filtrare per ora di fine min.</span><span class="sxs-lookup"><span data-stu-id="57b6d-131">Filter by end time min.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57b6d-132">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="57b6d-132">-JobExecutionId</span></span>
<span data-ttu-id="57b6d-133">ID esecuzione processo.</span><span class="sxs-lookup"><span data-stu-id="57b6d-133">The job execution id.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57b6d-134">-JobName</span><span class="sxs-lookup"><span data-stu-id="57b6d-134">-JobName</span></span>
<span data-ttu-id="57b6d-135">Il nome del processo.</span><span class="sxs-lookup"><span data-stu-id="57b6d-135">The job name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57b6d-136">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="57b6d-136">-ParentObject</span></span>
<span data-ttu-id="57b6d-137">Oggetto Agent.</span><span class="sxs-lookup"><span data-stu-id="57b6d-137">The agent object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel
Parameter Sets: ObjectSet, WithJobStepNameUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57b6d-138">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="57b6d-138">-ParentResourceId</span></span>
<span data-ttu-id="57b6d-139">ID risorsa di esecuzione processo.</span><span class="sxs-lookup"><span data-stu-id="57b6d-139">The job execution resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, WithJobStepNameUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57b6d-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57b6d-140">-ResourceGroupName</span></span>
<span data-ttu-id="57b6d-141">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="57b6d-141">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57b6d-142">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="57b6d-142">-ServerName</span></span>
<span data-ttu-id="57b6d-143">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="57b6d-143">The server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57b6d-144">-Stepname</span><span class="sxs-lookup"><span data-stu-id="57b6d-144">-StepName</span></span>
<span data-ttu-id="57b6d-145">Nome del passaggio del processo.</span><span class="sxs-lookup"><span data-stu-id="57b6d-145">The job step name.</span></span>

```yaml
Type: System.String
Parameter Sets: WithJobStepName, WithJobStepNameUsingParentObject, WithJobStepNameUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57b6d-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57b6d-146">CommonParameters</span></span>
<span data-ttu-id="57b6d-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57b6d-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57b6d-148">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="57b6d-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57b6d-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="57b6d-149">INPUTS</span></span>

### <span data-ttu-id="57b6d-150">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="57b6d-150">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="57b6d-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="57b6d-151">OUTPUTS</span></span>

### <span data-ttu-id="57b6d-152">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="57b6d-152">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="57b6d-153">Note</span><span class="sxs-lookup"><span data-stu-id="57b6d-153">NOTES</span></span>

## <span data-ttu-id="57b6d-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="57b6d-154">RELATED LINKS</span></span>
