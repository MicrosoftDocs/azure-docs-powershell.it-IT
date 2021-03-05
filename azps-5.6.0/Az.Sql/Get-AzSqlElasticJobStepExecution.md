---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/get-Azsqlelasticjobstepexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStepExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStepExecution.md
ms.openlocfilehash: 9918c314d239bf822fa789bcab6a9de923b8c2e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999630"
---
# <span data-ttu-id="4a051-101">Get-AzSqlElasticJobStepExecution</span><span class="sxs-lookup"><span data-stu-id="4a051-101">Get-AzSqlElasticJobStepExecution</span></span>

## <span data-ttu-id="4a051-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a051-102">SYNOPSIS</span></span>
<span data-ttu-id="4a051-103">Ottiene una o più esecuzioni delle passaggi del processo</span><span class="sxs-lookup"><span data-stu-id="4a051-103">Gets one or more job step executions</span></span>

## <span data-ttu-id="4a051-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4a051-104">SYNTAX</span></span>

### <span data-ttu-id="4a051-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4a051-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobStepExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>]
 [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a051-106">WithJobStepName</span><span class="sxs-lookup"><span data-stu-id="4a051-106">WithJobStepName</span></span>
```
Get-AzSqlElasticJobStepExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> -StepName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a051-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="4a051-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a051-108">WithJobStepNameUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="4a051-108">WithJobStepNameUsingParentObject</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> -StepName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a051-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4a051-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentResourceId] <String> [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a051-110">WithJobStepNameUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4a051-110">WithJobStepNameUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentResourceId] <String> -StepName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a051-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4a051-111">DESCRIPTION</span></span>
<span data-ttu-id="4a051-112">Il cmdlet Get-AzSqlElasticJobStepExecution cmdlet ottiene una o più esecuzioni di passaggi di processo da un'esecuzione di un processo</span><span class="sxs-lookup"><span data-stu-id="4a051-112">The Get-AzSqlElasticJobStepExecution cmdlet gets one or more job step executions from a job execution</span></span>

## <span data-ttu-id="4a051-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4a051-113">EXAMPLES</span></span>

### <span data-ttu-id="4a051-114">Esempio 1 - Ottiene una o più esecuzioni di passaggi di processo da esecuzioni di un processo</span><span class="sxs-lookup"><span data-stu-id="4a051-114">Example 1 - Gets one or more job step executions from a job executions</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobStepExecution

JobName JobVersion StepName StepId JobExecutionId                       Lifecycle StartTime            EndTime
------- ---------- -------- ------ --------------                       --------- ---------            -------
job1    1          step1    1      3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

### <span data-ttu-id="4a051-115">Esempio 2 - Ottiene una o più esecuzioni di passaggi di un processo dall'esecuzione di un processo, filtrando in base al nome della fase</span><span class="sxs-lookup"><span data-stu-id="4a051-115">Example 2 - Gets one or more job step executions from a job execution, filtering by step name</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobStepExecution -StepName step1

JobName JobVersion StepName StepId JobExecutionId                       Lifecycle StartTime            EndTime
------- ---------- -------- ------ --------------                       --------- ---------            -------
job1    1          step1    1      3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

<span data-ttu-id="4a051-116">Ottiene una o più esecuzioni delle passaggi del processo</span><span class="sxs-lookup"><span data-stu-id="4a051-116">Gets one or more job step executions</span></span>

## <span data-ttu-id="4a051-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a051-117">PARAMETERS</span></span>

### <span data-ttu-id="4a051-118">-Attivo</span><span class="sxs-lookup"><span data-stu-id="4a051-118">-Active</span></span>
<span data-ttu-id="4a051-119">Contrassegna per filtrare in base alle esecuzioni attive.</span><span class="sxs-lookup"><span data-stu-id="4a051-119">Flag to filter by active executions.</span></span>

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

### <span data-ttu-id="4a051-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="4a051-120">-AgentName</span></span>
<span data-ttu-id="4a051-121">Il nome dell'agente.</span><span class="sxs-lookup"><span data-stu-id="4a051-121">The agent name.</span></span>

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

### <span data-ttu-id="4a051-122">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="4a051-122">-CreateTimeMax</span></span>
<span data-ttu-id="4a051-123">Filtra per data/ora creazione max</span><span class="sxs-lookup"><span data-stu-id="4a051-123">Filter by create time max</span></span>

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

### <span data-ttu-id="4a051-124">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="4a051-124">-CreateTimeMin</span></span>
<span data-ttu-id="4a051-125">Filtrare in base alla data e ora di creazione</span><span class="sxs-lookup"><span data-stu-id="4a051-125">Filter by create time min</span></span>

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

### <span data-ttu-id="4a051-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a051-126">-DefaultProfile</span></span>
<span data-ttu-id="4a051-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4a051-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a051-128">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="4a051-128">-EndTimeMax</span></span>
<span data-ttu-id="4a051-129">Filtrare al massimo in base all'ora di fine.</span><span class="sxs-lookup"><span data-stu-id="4a051-129">Filter by end time max.</span></span>

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

### <span data-ttu-id="4a051-130">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="4a051-130">-EndTimeMin</span></span>
<span data-ttu-id="4a051-131">Filtrare per ora di fine min.</span><span class="sxs-lookup"><span data-stu-id="4a051-131">Filter by end time min.</span></span>

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

### <span data-ttu-id="4a051-132">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="4a051-132">-JobExecutionId</span></span>
<span data-ttu-id="4a051-133">ID di esecuzione del processo.</span><span class="sxs-lookup"><span data-stu-id="4a051-133">The job execution id.</span></span>

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

### <span data-ttu-id="4a051-134">-JobName</span><span class="sxs-lookup"><span data-stu-id="4a051-134">-JobName</span></span>
<span data-ttu-id="4a051-135">Nome del processo.</span><span class="sxs-lookup"><span data-stu-id="4a051-135">The job name.</span></span>

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

### <span data-ttu-id="4a051-136">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4a051-136">-ParentObject</span></span>
<span data-ttu-id="4a051-137">L'oggetto agente.</span><span class="sxs-lookup"><span data-stu-id="4a051-137">The agent object.</span></span>

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

### <span data-ttu-id="4a051-138">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4a051-138">-ParentResourceId</span></span>
<span data-ttu-id="4a051-139">ID della risorsa di esecuzione del processo.</span><span class="sxs-lookup"><span data-stu-id="4a051-139">The job execution resource id.</span></span>

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

### <span data-ttu-id="4a051-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a051-140">-ResourceGroupName</span></span>
<span data-ttu-id="4a051-141">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4a051-141">The resource group name.</span></span>

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

### <span data-ttu-id="4a051-142">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4a051-142">-ServerName</span></span>
<span data-ttu-id="4a051-143">Il nome del server.</span><span class="sxs-lookup"><span data-stu-id="4a051-143">The server name.</span></span>

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

### <span data-ttu-id="4a051-144">-StepName</span><span class="sxs-lookup"><span data-stu-id="4a051-144">-StepName</span></span>
<span data-ttu-id="4a051-145">Nome della fase del processo.</span><span class="sxs-lookup"><span data-stu-id="4a051-145">The job step name.</span></span>

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

### <span data-ttu-id="4a051-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a051-146">CommonParameters</span></span>
<span data-ttu-id="4a051-147">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a051-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a051-148">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4a051-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a051-149">INPUT</span><span class="sxs-lookup"><span data-stu-id="4a051-149">INPUTS</span></span>

### <span data-ttu-id="4a051-150">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="4a051-150">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="4a051-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4a051-151">OUTPUTS</span></span>

### <span data-ttu-id="4a051-152">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="4a051-152">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="4a051-153">NOTE</span><span class="sxs-lookup"><span data-stu-id="4a051-153">NOTES</span></span>

## <span data-ttu-id="4a051-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4a051-154">RELATED LINKS</span></span>
