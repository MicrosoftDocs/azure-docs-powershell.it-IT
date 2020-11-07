---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
ms.openlocfilehash: 5b5837fb0c5fa56e8e8f9887b6d85bfc3a3a559c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93856969"
---
# <span data-ttu-id="7906f-101">Get-AzSqlElasticJobExecution</span><span class="sxs-lookup"><span data-stu-id="7906f-101">Get-AzSqlElasticJobExecution</span></span>

## <span data-ttu-id="7906f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7906f-102">SYNOPSIS</span></span>
<span data-ttu-id="7906f-103">Ottiene una o più esecuzioni di processi</span><span class="sxs-lookup"><span data-stu-id="7906f-103">Gets one or more job executions</span></span>

## <span data-ttu-id="7906f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7906f-104">SYNTAX</span></span>

### <span data-ttu-id="7906f-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7906f-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName <String>] [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>]
 [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7906f-106">WithJobExecutionId</span><span class="sxs-lookup"><span data-stu-id="7906f-106">WithJobExecutionId</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 -JobName <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7906f-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="7906f-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> [-JobName <String>]
 [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>]
 [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7906f-108">WithJobExecutionIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="7906f-108">WithJobExecutionIdUsingParentObject</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> -JobName <String>
 -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7906f-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7906f-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> [-JobName <String>] [-Count] <Int32>
 [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>]
 [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7906f-110">WithJobExecutionIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="7906f-110">WithJobExecutionIdUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> -JobName <String> -JobExecutionId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7906f-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7906f-111">DESCRIPTION</span></span>
<span data-ttu-id="7906f-112">Il cmdlet Get-AzSqlElasticJobExecution ottiene una o più esecuzioni dei processi</span><span class="sxs-lookup"><span data-stu-id="7906f-112">The Get-AzSqlElasticJobExecution cmdlet gets one or more job executions</span></span>

## <span data-ttu-id="7906f-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7906f-113">EXAMPLES</span></span>

### <span data-ttu-id="7906f-114">Esempio 1: ottiene una o più esecuzioni di processo in tutti i processi</span><span class="sxs-lookup"><span data-stu-id="7906f-114">Example 1 - Gets one or more job executions across all jobs</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b Canceled  6/1/2018 10:13:56 PM 6/1/2018 10:13:59 PM
job1    3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:43 PM 6/1/2018 10:11:47 PM
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

### <span data-ttu-id="7906f-115">Esempio 2: ottiene una o più esecuzioni di processi per un processo</span><span class="sxs-lookup"><span data-stu-id="7906f-115">Example 2 - Gets one or more job executions for a job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3 -JobName job2

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

<span data-ttu-id="7906f-116">Ottiene una o più esecuzioni di processi</span><span class="sxs-lookup"><span data-stu-id="7906f-116">Gets one or more job executions</span></span>

## <span data-ttu-id="7906f-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7906f-117">PARAMETERS</span></span>

### <span data-ttu-id="7906f-118">-Active</span><span class="sxs-lookup"><span data-stu-id="7906f-118">-Active</span></span>
<span data-ttu-id="7906f-119">Filtrare per creare il tempo min</span><span class="sxs-lookup"><span data-stu-id="7906f-119">Filter by create time min</span></span>

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

### <span data-ttu-id="7906f-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="7906f-120">-AgentName</span></span>
<span data-ttu-id="7906f-121">Nome dell'agente.</span><span class="sxs-lookup"><span data-stu-id="7906f-121">The agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobExecutionId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7906f-122">-Conteggio</span><span class="sxs-lookup"><span data-stu-id="7906f-122">-Count</span></span>
<span data-ttu-id="7906f-123">Count restituisce il numero di esecuzioni principali.</span><span class="sxs-lookup"><span data-stu-id="7906f-123">Count returns the top number of executions.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7906f-124">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="7906f-124">-CreateTimeMax</span></span>
<span data-ttu-id="7906f-125">Filtrare per creare il tempo min</span><span class="sxs-lookup"><span data-stu-id="7906f-125">Filter by create time min</span></span>

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

### <span data-ttu-id="7906f-126">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="7906f-126">-CreateTimeMin</span></span>
<span data-ttu-id="7906f-127">Filtrare per creare il tempo min</span><span class="sxs-lookup"><span data-stu-id="7906f-127">Filter by create time min</span></span>

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

### <span data-ttu-id="7906f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7906f-128">-DefaultProfile</span></span>
<span data-ttu-id="7906f-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7906f-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7906f-130">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="7906f-130">-EndTimeMax</span></span>
<span data-ttu-id="7906f-131">Filtrare per creare il tempo min</span><span class="sxs-lookup"><span data-stu-id="7906f-131">Filter by create time min</span></span>

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

### <span data-ttu-id="7906f-132">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="7906f-132">-EndTimeMin</span></span>
<span data-ttu-id="7906f-133">Filtrare per creare il tempo min</span><span class="sxs-lookup"><span data-stu-id="7906f-133">Filter by create time min</span></span>

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

### <span data-ttu-id="7906f-134">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="7906f-134">-JobExecutionId</span></span>
<span data-ttu-id="7906f-135">ID esecuzione processo.</span><span class="sxs-lookup"><span data-stu-id="7906f-135">The job execution id.</span></span>

```yaml
Type: System.String
Parameter Sets: WithJobExecutionId, WithJobExecutionIdUsingParentObject, WithJobExecutionIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7906f-136">-JobName</span><span class="sxs-lookup"><span data-stu-id="7906f-136">-JobName</span></span>
<span data-ttu-id="7906f-137">Il nome del processo.</span><span class="sxs-lookup"><span data-stu-id="7906f-137">The job name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WithJobExecutionId, WithJobExecutionIdUsingParentObject, WithJobExecutionIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7906f-138">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7906f-138">-ParentObject</span></span>
<span data-ttu-id="7906f-139">ID esecuzione processo.</span><span class="sxs-lookup"><span data-stu-id="7906f-139">The job execution id.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel
Parameter Sets: ObjectSet, WithJobExecutionIdUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7906f-140">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="7906f-140">-ParentResourceId</span></span>
<span data-ttu-id="7906f-141">ID risorsa agente.</span><span class="sxs-lookup"><span data-stu-id="7906f-141">The agent resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, WithJobExecutionIdUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7906f-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7906f-142">-ResourceGroupName</span></span>
<span data-ttu-id="7906f-143">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7906f-143">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobExecutionId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7906f-144">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="7906f-144">-ServerName</span></span>
<span data-ttu-id="7906f-145">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="7906f-145">The server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobExecutionId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7906f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7906f-146">CommonParameters</span></span>
<span data-ttu-id="7906f-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7906f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7906f-148">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7906f-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7906f-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7906f-149">INPUTS</span></span>

### <span data-ttu-id="7906f-150">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="7906f-150">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="7906f-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7906f-151">OUTPUTS</span></span>

### <span data-ttu-id="7906f-152">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="7906f-152">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="7906f-153">Note</span><span class="sxs-lookup"><span data-stu-id="7906f-153">NOTES</span></span>

## <span data-ttu-id="7906f-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7906f-154">RELATED LINKS</span></span>
