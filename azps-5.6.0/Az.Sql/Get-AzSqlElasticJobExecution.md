---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/get-Azsqlelasticjobexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
ms.openlocfilehash: 2913c390620e18fb1781b235edca9e4f50715cd0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999662"
---
# <span data-ttu-id="734df-101">Get-AzSqlElasticJobExecution</span><span class="sxs-lookup"><span data-stu-id="734df-101">Get-AzSqlElasticJobExecution</span></span>

## <span data-ttu-id="734df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="734df-102">SYNOPSIS</span></span>
<span data-ttu-id="734df-103">Ottiene una o più esecuzioni di processi</span><span class="sxs-lookup"><span data-stu-id="734df-103">Gets one or more job executions</span></span>

## <span data-ttu-id="734df-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="734df-104">SYNTAX</span></span>

### <span data-ttu-id="734df-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="734df-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName <String>] [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>]
 [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="734df-106">WithJobExecutionId</span><span class="sxs-lookup"><span data-stu-id="734df-106">WithJobExecutionId</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 -JobName <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="734df-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="734df-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> [-JobName <String>]
 [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>]
 [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="734df-108">WithJobExecutionIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="734df-108">WithJobExecutionIdUsingParentObject</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> -JobName <String>
 -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="734df-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="734df-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> [-JobName <String>] [-Count] <Int32>
 [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>]
 [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="734df-110">WithJobExecutionIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="734df-110">WithJobExecutionIdUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> -JobName <String> -JobExecutionId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="734df-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="734df-111">DESCRIPTION</span></span>
<span data-ttu-id="734df-112">Il cmdlet Get-AzSqlElasticJobExecution riceve una o più esecuzioni di processi</span><span class="sxs-lookup"><span data-stu-id="734df-112">The Get-AzSqlElasticJobExecution cmdlet gets one or more job executions</span></span>

## <span data-ttu-id="734df-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="734df-113">EXAMPLES</span></span>

### <span data-ttu-id="734df-114">Esempio 1: ottiene una o più esecuzioni di processo in tutti i processi</span><span class="sxs-lookup"><span data-stu-id="734df-114">Example 1: Gets one or more job executions across all jobs</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b Canceled  6/1/2018 10:13:56 PM 6/1/2018 10:13:59 PM
job1    3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:43 PM 6/1/2018 10:11:47 PM
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

### <span data-ttu-id="734df-115">Esempio 2: ottiene una o più esecuzioni di un processo</span><span class="sxs-lookup"><span data-stu-id="734df-115">Example 2: Gets one or more job executions for a job</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3 -JobName job2

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

<span data-ttu-id="734df-116">Ottiene una o più esecuzioni di processi</span><span class="sxs-lookup"><span data-stu-id="734df-116">Gets one or more job executions</span></span>

### <span data-ttu-id="734df-117">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="734df-117">Example 3</span></span>

<span data-ttu-id="734df-118">Ottiene una o più esecuzioni di processi.</span><span class="sxs-lookup"><span data-stu-id="734df-118">Gets one or more job executions.</span></span> <span data-ttu-id="734df-119">(autogenerati)</span><span class="sxs-lookup"><span data-stu-id="734df-119">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Get-AzSqlElasticJobExecution -JobExecutionId 00000000-0000-0000-0000-000000000000 -JobName job1
```

## <span data-ttu-id="734df-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="734df-120">PARAMETERS</span></span>

### <span data-ttu-id="734df-121">-Attivo</span><span class="sxs-lookup"><span data-stu-id="734df-121">-Active</span></span>
<span data-ttu-id="734df-122">Filtrare in base alla data e ora di creazione</span><span class="sxs-lookup"><span data-stu-id="734df-122">Filter by create time min</span></span>

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

### <span data-ttu-id="734df-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="734df-123">-AgentName</span></span>
<span data-ttu-id="734df-124">Il nome dell'agente.</span><span class="sxs-lookup"><span data-stu-id="734df-124">The agent name.</span></span>

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

### <span data-ttu-id="734df-125">-Count</span><span class="sxs-lookup"><span data-stu-id="734df-125">-Count</span></span>
<span data-ttu-id="734df-126">Count restituisce il numero più alto di esecuzioni.</span><span class="sxs-lookup"><span data-stu-id="734df-126">Count returns the top number of executions.</span></span>

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

### <span data-ttu-id="734df-127">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="734df-127">-CreateTimeMax</span></span>
<span data-ttu-id="734df-128">Filtrare in base alla data e ora di creazione</span><span class="sxs-lookup"><span data-stu-id="734df-128">Filter by create time min</span></span>

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

### <span data-ttu-id="734df-129">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="734df-129">-CreateTimeMin</span></span>
<span data-ttu-id="734df-130">Filtrare in base alla data e ora di creazione</span><span class="sxs-lookup"><span data-stu-id="734df-130">Filter by create time min</span></span>

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

### <span data-ttu-id="734df-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="734df-131">-DefaultProfile</span></span>
<span data-ttu-id="734df-132">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="734df-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="734df-133">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="734df-133">-EndTimeMax</span></span>
<span data-ttu-id="734df-134">Filtrare in base alla data e ora di creazione</span><span class="sxs-lookup"><span data-stu-id="734df-134">Filter by create time min</span></span>

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

### <span data-ttu-id="734df-135">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="734df-135">-EndTimeMin</span></span>
<span data-ttu-id="734df-136">Filtrare in base alla data e ora di creazione</span><span class="sxs-lookup"><span data-stu-id="734df-136">Filter by create time min</span></span>

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

### <span data-ttu-id="734df-137">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="734df-137">-JobExecutionId</span></span>
<span data-ttu-id="734df-138">ID di esecuzione del processo.</span><span class="sxs-lookup"><span data-stu-id="734df-138">The job execution id.</span></span>

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

### <span data-ttu-id="734df-139">-JobName</span><span class="sxs-lookup"><span data-stu-id="734df-139">-JobName</span></span>
<span data-ttu-id="734df-140">Nome del processo.</span><span class="sxs-lookup"><span data-stu-id="734df-140">The job name.</span></span>

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

### <span data-ttu-id="734df-141">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="734df-141">-ParentObject</span></span>
<span data-ttu-id="734df-142">ID di esecuzione del processo.</span><span class="sxs-lookup"><span data-stu-id="734df-142">The job execution id.</span></span>

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

### <span data-ttu-id="734df-143">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="734df-143">-ParentResourceId</span></span>
<span data-ttu-id="734df-144">ID risorsa agente.</span><span class="sxs-lookup"><span data-stu-id="734df-144">The agent resource id.</span></span>

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

### <span data-ttu-id="734df-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="734df-145">-ResourceGroupName</span></span>
<span data-ttu-id="734df-146">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="734df-146">The resource group name.</span></span>

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

### <span data-ttu-id="734df-147">-ServerName</span><span class="sxs-lookup"><span data-stu-id="734df-147">-ServerName</span></span>
<span data-ttu-id="734df-148">Il nome del server.</span><span class="sxs-lookup"><span data-stu-id="734df-148">The server name.</span></span>

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

### <span data-ttu-id="734df-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="734df-149">CommonParameters</span></span>
<span data-ttu-id="734df-150">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="734df-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="734df-151">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="734df-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="734df-152">INPUT</span><span class="sxs-lookup"><span data-stu-id="734df-152">INPUTS</span></span>

### <span data-ttu-id="734df-153">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="734df-153">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="734df-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="734df-154">OUTPUTS</span></span>

### <span data-ttu-id="734df-155">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="734df-155">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="734df-156">NOTE</span><span class="sxs-lookup"><span data-stu-id="734df-156">NOTES</span></span>

## <span data-ttu-id="734df-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="734df-157">RELATED LINKS</span></span>
