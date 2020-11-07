---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobtargetexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetExecution.md
ms.openlocfilehash: 566bfb8caae85c6f4e6ef75a38bdd5363ddb1eaa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93865397"
---
# <span data-ttu-id="0c763-101">Get-AzSqlElasticJobTargetExecution</span><span class="sxs-lookup"><span data-stu-id="0c763-101">Get-AzSqlElasticJobTargetExecution</span></span>

## <span data-ttu-id="0c763-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0c763-102">SYNOPSIS</span></span>
<span data-ttu-id="0c763-103">Ottiene una o più esecuzioni di destinazione processo</span><span class="sxs-lookup"><span data-stu-id="0c763-103">Gets one or more job target executions</span></span>

## <span data-ttu-id="0c763-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0c763-104">SYNTAX</span></span>

### <span data-ttu-id="0c763-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0c763-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> -Count <Int32> [-StepName <String>] [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c763-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="0c763-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> -Count <Int32>
 [-StepName <String>] [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>]
 [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c763-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0c763-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ParentResourceId] <String> -Count <Int32> [-StepName <String>]
 [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>]
 [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c763-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c763-108">DESCRIPTION</span></span>
<span data-ttu-id="0c763-109">Il cmdlet Get-AzSqlElasticJobTargetExecution ottiene una o più esecuzioni di destinazione processo da un'esecuzione del processo</span><span class="sxs-lookup"><span data-stu-id="0c763-109">The Get-AzSqlElasticJobTargetExecution cmdlet gets one or more job target executions from a job execution</span></span>

## <span data-ttu-id="0c763-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0c763-110">EXAMPLES</span></span>

### <span data-ttu-id="0c763-111">Esempio 1: ottiene una o più esecuzioni di destinazioni di lavoro da un'esecuzione di processi</span><span class="sxs-lookup"><span data-stu-id="0c763-111">Example 1 - Gets one or more job target executions from a job executions</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobTargetExecution -Count 2
JobName JobVersion StepName StepId JobExecutionId                       Lifecycle       TargetServerName TargetDatabaseName StartTime            EndTime
------- ---------- -------- ------ --------------                       ---------       ---------------- ------------------ ---------            -------
job1    1          step2    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db2                6/1/2018 10:11:47 PM 6/1/2018 10:11:50 PM
job1    1          step1    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db1                6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

### <span data-ttu-id="0c763-112">Esempio 2: ottiene una o più esecuzioni di destinazione processo da un processo di esecuzione-filtro in base al nome del passaggio</span><span class="sxs-lookup"><span data-stu-id="0c763-112">Example 2 - Gets one or more job target executions from a job executions - filtering by step name</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobTargetExecution -Count 2 -StepName step2
JobName JobVersion StepName StepId JobExecutionId                       Lifecycle       TargetServerName TargetDatabaseName StartTime            EndTime
------- ---------- -------- ------ --------------                       ---------       ---------------- ------------------ ---------            -------
job1    1          step2    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db2                6/1/2018 10:11:47 PM 6/1/2018 10:11:50 PM
```

<span data-ttu-id="0c763-113">Ottiene una o più esecuzioni di destinazione processo</span><span class="sxs-lookup"><span data-stu-id="0c763-113">Gets one or more job target executions</span></span>

## <span data-ttu-id="0c763-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0c763-114">PARAMETERS</span></span>

### <span data-ttu-id="0c763-115">-Active</span><span class="sxs-lookup"><span data-stu-id="0c763-115">-Active</span></span>
<span data-ttu-id="0c763-116">Contrassegna per filtrare in base alle esecuzioni attive.</span><span class="sxs-lookup"><span data-stu-id="0c763-116">Flag to filter by active executions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c763-117">-AgentName</span><span class="sxs-lookup"><span data-stu-id="0c763-117">-AgentName</span></span>
<span data-ttu-id="0c763-118">Nome dell'agente.</span><span class="sxs-lookup"><span data-stu-id="0c763-118">The agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c763-119">-Conteggio</span><span class="sxs-lookup"><span data-stu-id="0c763-119">-Count</span></span>
<span data-ttu-id="0c763-120">Count restituisce il numero di esecuzioni principali.</span><span class="sxs-lookup"><span data-stu-id="0c763-120">Count returns the top number of executions.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c763-121">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="0c763-121">-CreateTimeMax</span></span>
<span data-ttu-id="0c763-122">Filtra per crea tempo max</span><span class="sxs-lookup"><span data-stu-id="0c763-122">Filter by create time max</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c763-123">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="0c763-123">-CreateTimeMin</span></span>
<span data-ttu-id="0c763-124">Filtrare per creare il tempo min</span><span class="sxs-lookup"><span data-stu-id="0c763-124">Filter by create time min</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c763-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c763-125">-DefaultProfile</span></span>
<span data-ttu-id="0c763-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0c763-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c763-127">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="0c763-127">-EndTimeMax</span></span>
<span data-ttu-id="0c763-128">Filtrare per ora di fine max.</span><span class="sxs-lookup"><span data-stu-id="0c763-128">Filter by end time max.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c763-129">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="0c763-129">-EndTimeMin</span></span>
<span data-ttu-id="0c763-130">Filtrare per ora di fine min.</span><span class="sxs-lookup"><span data-stu-id="0c763-130">Filter by end time min.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c763-131">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="0c763-131">-JobExecutionId</span></span>
<span data-ttu-id="0c763-132">ID esecuzione processo.</span><span class="sxs-lookup"><span data-stu-id="0c763-132">The job execution id.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c763-133">-JobName</span><span class="sxs-lookup"><span data-stu-id="0c763-133">-JobName</span></span>
<span data-ttu-id="0c763-134">Il nome del processo.</span><span class="sxs-lookup"><span data-stu-id="0c763-134">The job name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c763-135">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0c763-135">-ParentObject</span></span>
<span data-ttu-id="0c763-136">L'oggetto di esecuzione del processo.</span><span class="sxs-lookup"><span data-stu-id="0c763-136">The job execution object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c763-137">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="0c763-137">-ParentResourceId</span></span>
<span data-ttu-id="0c763-138">ID risorsa di esecuzione processo.</span><span class="sxs-lookup"><span data-stu-id="0c763-138">The job execution resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c763-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c763-139">-ResourceGroupName</span></span>
<span data-ttu-id="0c763-140">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0c763-140">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c763-141">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="0c763-141">-ServerName</span></span>
<span data-ttu-id="0c763-142">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="0c763-142">The server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c763-143">-Stepname</span><span class="sxs-lookup"><span data-stu-id="0c763-143">-StepName</span></span>
<span data-ttu-id="0c763-144">Nome del passaggio del processo.</span><span class="sxs-lookup"><span data-stu-id="0c763-144">The job step name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c763-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c763-145">CommonParameters</span></span>
<span data-ttu-id="0c763-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c763-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c763-147">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c763-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c763-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0c763-148">INPUTS</span></span>

### <span data-ttu-id="0c763-149">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="0c763-149">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="0c763-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0c763-150">OUTPUTS</span></span>

### <span data-ttu-id="0c763-151">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="0c763-151">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="0c763-152">Note</span><span class="sxs-lookup"><span data-stu-id="0c763-152">NOTES</span></span>

## <span data-ttu-id="0c763-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0c763-153">RELATED LINKS</span></span>
