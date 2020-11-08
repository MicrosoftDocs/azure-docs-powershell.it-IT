---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
ms.openlocfilehash: d5583e5d7c0984b36679517859cc5a109b808a1a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190092"
---
# <span data-ttu-id="60d7c-101">Get-AzSqlElasticJobExecution</span><span class="sxs-lookup"><span data-stu-id="60d7c-101">Get-AzSqlElasticJobExecution</span></span>

## <span data-ttu-id="60d7c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="60d7c-102">SYNOPSIS</span></span>
<span data-ttu-id="60d7c-103">Ottiene una o più esecuzioni di processi</span><span class="sxs-lookup"><span data-stu-id="60d7c-103">Gets one or more job executions</span></span>

## <span data-ttu-id="60d7c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="60d7c-104">SYNTAX</span></span>

### <span data-ttu-id="60d7c-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="60d7c-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName <String>] [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>]
 [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="60d7c-106">WithJobExecutionId</span><span class="sxs-lookup"><span data-stu-id="60d7c-106">WithJobExecutionId</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 -JobName <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60d7c-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="60d7c-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> [-JobName <String>]
 [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>]
 [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60d7c-108">WithJobExecutionIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="60d7c-108">WithJobExecutionIdUsingParentObject</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> -JobName <String>
 -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60d7c-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="60d7c-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> [-JobName <String>] [-Count] <Int32>
 [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>]
 [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60d7c-110">WithJobExecutionIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="60d7c-110">WithJobExecutionIdUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> -JobName <String> -JobExecutionId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60d7c-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60d7c-111">DESCRIPTION</span></span>
<span data-ttu-id="60d7c-112">Il cmdlet Get-AzSqlElasticJobExecution ottiene una o più esecuzioni dei processi</span><span class="sxs-lookup"><span data-stu-id="60d7c-112">The Get-AzSqlElasticJobExecution cmdlet gets one or more job executions</span></span>

## <span data-ttu-id="60d7c-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="60d7c-113">EXAMPLES</span></span>

### <span data-ttu-id="60d7c-114">Esempio 1: ottiene una o più esecuzioni processi in tutti i processi</span><span class="sxs-lookup"><span data-stu-id="60d7c-114">Example 1: Gets one or more job executions across all jobs</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b Canceled  6/1/2018 10:13:56 PM 6/1/2018 10:13:59 PM
job1    3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:43 PM 6/1/2018 10:11:47 PM
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

### <span data-ttu-id="60d7c-115">Esempio 2: ottiene una o più esecuzioni di processi per un processo</span><span class="sxs-lookup"><span data-stu-id="60d7c-115">Example 2: Gets one or more job executions for a job</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3 -JobName job2

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

<span data-ttu-id="60d7c-116">Ottiene una o più esecuzioni di processi</span><span class="sxs-lookup"><span data-stu-id="60d7c-116">Gets one or more job executions</span></span>

### <span data-ttu-id="60d7c-117">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="60d7c-117">Example 3</span></span>

<span data-ttu-id="60d7c-118">Ottiene una o più esecuzioni di processi.</span><span class="sxs-lookup"><span data-stu-id="60d7c-118">Gets one or more job executions.</span></span> <span data-ttu-id="60d7c-119">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="60d7c-119">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Get-AzSqlElasticJobExecution -JobExecutionId 00000000-0000-0000-0000-000000000000 -JobName job1
```

## <span data-ttu-id="60d7c-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="60d7c-120">PARAMETERS</span></span>

### <span data-ttu-id="60d7c-121">-Active</span><span class="sxs-lookup"><span data-stu-id="60d7c-121">-Active</span></span>
<span data-ttu-id="60d7c-122">Filtrare per creare il tempo min</span><span class="sxs-lookup"><span data-stu-id="60d7c-122">Filter by create time min</span></span>

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

### <span data-ttu-id="60d7c-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="60d7c-123">-AgentName</span></span>
<span data-ttu-id="60d7c-124">Nome dell'agente.</span><span class="sxs-lookup"><span data-stu-id="60d7c-124">The agent name.</span></span>

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

### <span data-ttu-id="60d7c-125">-Conteggio</span><span class="sxs-lookup"><span data-stu-id="60d7c-125">-Count</span></span>
<span data-ttu-id="60d7c-126">Count restituisce il numero di esecuzioni principali.</span><span class="sxs-lookup"><span data-stu-id="60d7c-126">Count returns the top number of executions.</span></span>

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

### <span data-ttu-id="60d7c-127">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="60d7c-127">-CreateTimeMax</span></span>
<span data-ttu-id="60d7c-128">Filtrare per creare il tempo min</span><span class="sxs-lookup"><span data-stu-id="60d7c-128">Filter by create time min</span></span>

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

### <span data-ttu-id="60d7c-129">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="60d7c-129">-CreateTimeMin</span></span>
<span data-ttu-id="60d7c-130">Filtrare per creare il tempo min</span><span class="sxs-lookup"><span data-stu-id="60d7c-130">Filter by create time min</span></span>

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

### <span data-ttu-id="60d7c-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60d7c-131">-DefaultProfile</span></span>
<span data-ttu-id="60d7c-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="60d7c-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60d7c-133">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="60d7c-133">-EndTimeMax</span></span>
<span data-ttu-id="60d7c-134">Filtrare per creare il tempo min</span><span class="sxs-lookup"><span data-stu-id="60d7c-134">Filter by create time min</span></span>

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

### <span data-ttu-id="60d7c-135">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="60d7c-135">-EndTimeMin</span></span>
<span data-ttu-id="60d7c-136">Filtrare per creare il tempo min</span><span class="sxs-lookup"><span data-stu-id="60d7c-136">Filter by create time min</span></span>

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

### <span data-ttu-id="60d7c-137">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="60d7c-137">-JobExecutionId</span></span>
<span data-ttu-id="60d7c-138">ID esecuzione processo.</span><span class="sxs-lookup"><span data-stu-id="60d7c-138">The job execution id.</span></span>

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

### <span data-ttu-id="60d7c-139">-JobName</span><span class="sxs-lookup"><span data-stu-id="60d7c-139">-JobName</span></span>
<span data-ttu-id="60d7c-140">Il nome del processo.</span><span class="sxs-lookup"><span data-stu-id="60d7c-140">The job name.</span></span>

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

### <span data-ttu-id="60d7c-141">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="60d7c-141">-ParentObject</span></span>
<span data-ttu-id="60d7c-142">ID esecuzione processo.</span><span class="sxs-lookup"><span data-stu-id="60d7c-142">The job execution id.</span></span>

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

### <span data-ttu-id="60d7c-143">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="60d7c-143">-ParentResourceId</span></span>
<span data-ttu-id="60d7c-144">ID risorsa agente.</span><span class="sxs-lookup"><span data-stu-id="60d7c-144">The agent resource id.</span></span>

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

### <span data-ttu-id="60d7c-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60d7c-145">-ResourceGroupName</span></span>
<span data-ttu-id="60d7c-146">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="60d7c-146">The resource group name.</span></span>

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

### <span data-ttu-id="60d7c-147">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="60d7c-147">-ServerName</span></span>
<span data-ttu-id="60d7c-148">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="60d7c-148">The server name.</span></span>

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

### <span data-ttu-id="60d7c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60d7c-149">CommonParameters</span></span>
<span data-ttu-id="60d7c-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60d7c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60d7c-151">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60d7c-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60d7c-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="60d7c-152">INPUTS</span></span>

### <span data-ttu-id="60d7c-153">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="60d7c-153">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="60d7c-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="60d7c-154">OUTPUTS</span></span>

### <span data-ttu-id="60d7c-155">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="60d7c-155">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="60d7c-156">Note</span><span class="sxs-lookup"><span data-stu-id="60d7c-156">NOTES</span></span>

## <span data-ttu-id="60d7c-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="60d7c-157">RELATED LINKS</span></span>
