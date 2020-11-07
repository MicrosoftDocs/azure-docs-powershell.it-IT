---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
ms.openlocfilehash: 2c4d0865ba1fb904e367857702d1344f5fb210cc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93865404"
---
# <span data-ttu-id="b097d-101">Get-AzSqlElasticJobExecution</span><span class="sxs-lookup"><span data-stu-id="b097d-101">Get-AzSqlElasticJobExecution</span></span>

## <span data-ttu-id="b097d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b097d-102">SYNOPSIS</span></span>
<span data-ttu-id="b097d-103">Ottiene una o più esecuzioni di processi</span><span class="sxs-lookup"><span data-stu-id="b097d-103">Gets one or more job executions</span></span>

## <span data-ttu-id="b097d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b097d-104">SYNTAX</span></span>

### <span data-ttu-id="b097d-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b097d-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName <String>] [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>]
 [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b097d-106">WithJobExecutionId</span><span class="sxs-lookup"><span data-stu-id="b097d-106">WithJobExecutionId</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 -JobName <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b097d-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="b097d-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> [-JobName <String>]
 [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>]
 [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b097d-108">WithJobExecutionIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="b097d-108">WithJobExecutionIdUsingParentObject</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> -JobName <String>
 -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b097d-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b097d-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> [-JobName <String>] [-Count] <Int32>
 [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>]
 [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b097d-110">WithJobExecutionIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b097d-110">WithJobExecutionIdUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> -JobName <String> -JobExecutionId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b097d-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b097d-111">DESCRIPTION</span></span>
<span data-ttu-id="b097d-112">Il cmdlet Get-AzSqlElasticJobExecution ottiene una o più esecuzioni dei processi</span><span class="sxs-lookup"><span data-stu-id="b097d-112">The Get-AzSqlElasticJobExecution cmdlet gets one or more job executions</span></span>

## <span data-ttu-id="b097d-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b097d-113">EXAMPLES</span></span>

### <span data-ttu-id="b097d-114">Esempio 1: ottiene una o più esecuzioni di processo in tutti i processi</span><span class="sxs-lookup"><span data-stu-id="b097d-114">Example 1 - Gets one or more job executions across all jobs</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b Canceled  6/1/2018 10:13:56 PM 6/1/2018 10:13:59 PM
job1    3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:43 PM 6/1/2018 10:11:47 PM
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

### <span data-ttu-id="b097d-115">Esempio 2: ottiene una o più esecuzioni di processi per un processo</span><span class="sxs-lookup"><span data-stu-id="b097d-115">Example 2 - Gets one or more job executions for a job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3 -JobName job2

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

<span data-ttu-id="b097d-116">Ottiene una o più esecuzioni di processi</span><span class="sxs-lookup"><span data-stu-id="b097d-116">Gets one or more job executions</span></span>

## <span data-ttu-id="b097d-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b097d-117">PARAMETERS</span></span>

### <span data-ttu-id="b097d-118">-Active</span><span class="sxs-lookup"><span data-stu-id="b097d-118">-Active</span></span>
<span data-ttu-id="b097d-119">Filtrare per creare il tempo min</span><span class="sxs-lookup"><span data-stu-id="b097d-119">Filter by create time min</span></span>

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

### <span data-ttu-id="b097d-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="b097d-120">-AgentName</span></span>
<span data-ttu-id="b097d-121">Nome dell'agente.</span><span class="sxs-lookup"><span data-stu-id="b097d-121">The agent name.</span></span>

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

### <span data-ttu-id="b097d-122">-Conteggio</span><span class="sxs-lookup"><span data-stu-id="b097d-122">-Count</span></span>
<span data-ttu-id="b097d-123">Count restituisce il numero di esecuzioni principali.</span><span class="sxs-lookup"><span data-stu-id="b097d-123">Count returns the top number of executions.</span></span>

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

### <span data-ttu-id="b097d-124">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="b097d-124">-CreateTimeMax</span></span>
<span data-ttu-id="b097d-125">Filtrare per creare il tempo min</span><span class="sxs-lookup"><span data-stu-id="b097d-125">Filter by create time min</span></span>

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

### <span data-ttu-id="b097d-126">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="b097d-126">-CreateTimeMin</span></span>
<span data-ttu-id="b097d-127">Filtrare per creare il tempo min</span><span class="sxs-lookup"><span data-stu-id="b097d-127">Filter by create time min</span></span>

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

### <span data-ttu-id="b097d-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b097d-128">-DefaultProfile</span></span>
<span data-ttu-id="b097d-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b097d-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b097d-130">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="b097d-130">-EndTimeMax</span></span>
<span data-ttu-id="b097d-131">Filtrare per creare il tempo min</span><span class="sxs-lookup"><span data-stu-id="b097d-131">Filter by create time min</span></span>

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

### <span data-ttu-id="b097d-132">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="b097d-132">-EndTimeMin</span></span>
<span data-ttu-id="b097d-133">Filtrare per creare il tempo min</span><span class="sxs-lookup"><span data-stu-id="b097d-133">Filter by create time min</span></span>

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

### <span data-ttu-id="b097d-134">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="b097d-134">-JobExecutionId</span></span>
<span data-ttu-id="b097d-135">ID esecuzione processo.</span><span class="sxs-lookup"><span data-stu-id="b097d-135">The job execution id.</span></span>

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

### <span data-ttu-id="b097d-136">-JobName</span><span class="sxs-lookup"><span data-stu-id="b097d-136">-JobName</span></span>
<span data-ttu-id="b097d-137">Il nome del processo.</span><span class="sxs-lookup"><span data-stu-id="b097d-137">The job name.</span></span>

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

### <span data-ttu-id="b097d-138">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b097d-138">-ParentObject</span></span>
<span data-ttu-id="b097d-139">ID esecuzione processo.</span><span class="sxs-lookup"><span data-stu-id="b097d-139">The job execution id.</span></span>

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

### <span data-ttu-id="b097d-140">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b097d-140">-ParentResourceId</span></span>
<span data-ttu-id="b097d-141">ID risorsa agente.</span><span class="sxs-lookup"><span data-stu-id="b097d-141">The agent resource id.</span></span>

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

### <span data-ttu-id="b097d-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b097d-142">-ResourceGroupName</span></span>
<span data-ttu-id="b097d-143">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b097d-143">The resource group name.</span></span>

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

### <span data-ttu-id="b097d-144">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="b097d-144">-ServerName</span></span>
<span data-ttu-id="b097d-145">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="b097d-145">The server name.</span></span>

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

### <span data-ttu-id="b097d-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b097d-146">CommonParameters</span></span>
<span data-ttu-id="b097d-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b097d-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b097d-148">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b097d-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b097d-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b097d-149">INPUTS</span></span>

### <span data-ttu-id="b097d-150">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="b097d-150">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="b097d-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b097d-151">OUTPUTS</span></span>

### <span data-ttu-id="b097d-152">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="b097d-152">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="b097d-153">Note</span><span class="sxs-lookup"><span data-stu-id="b097d-153">NOTES</span></span>

## <span data-ttu-id="b097d-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b097d-154">RELATED LINKS</span></span>
