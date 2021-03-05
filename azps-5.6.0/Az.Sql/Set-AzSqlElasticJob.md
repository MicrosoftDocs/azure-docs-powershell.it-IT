---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/set-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
ms.openlocfilehash: 9daa42e00d23af96d630795abcc88dbeaceacaff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002958"
---
# <span data-ttu-id="444a5-101">Set-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="444a5-101">Set-AzSqlElasticJob</span></span>

## <span data-ttu-id="444a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="444a5-102">SYNOPSIS</span></span>
<span data-ttu-id="444a5-103">Aggiorna un processo</span><span class="sxs-lookup"><span data-stu-id="444a5-103">Updates a job</span></span>

## <span data-ttu-id="444a5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="444a5-104">SYNTAX</span></span>

### <span data-ttu-id="444a5-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="444a5-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="444a5-106">RunOnce</span><span class="sxs-lookup"><span data-stu-id="444a5-106">RunOnce</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="444a5-107">Ricorrente</span><span class="sxs-lookup"><span data-stu-id="444a5-107">Recurring</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="444a5-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="444a5-108">ObjectSet</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="444a5-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="444a5-109">RunOnceUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-RunOnce] [-StartTime <DateTime>]
 [-EndTime <DateTime>] [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="444a5-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="444a5-110">RecurringUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="444a5-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="444a5-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="444a5-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="444a5-112">RunOnceUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="444a5-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="444a5-113">RecurringUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="444a5-114">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="444a5-114">DESCRIPTION</span></span>
<span data-ttu-id="444a5-115">Il cmdlet Set-AzSqlElasticJob aggiorna un processo</span><span class="sxs-lookup"><span data-stu-id="444a5-115">The Set-AzSqlElasticJob cmdlet updates a job</span></span>

## <span data-ttu-id="444a5-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="444a5-116">EXAMPLES</span></span>

### <span data-ttu-id="444a5-117">Esempio 1: Aggiorna un processo in modo che inizi un'ora da ora e si ripeta ogni 1 ora</span><span class="sxs-lookup"><span data-stu-id="444a5-117">Example 1: Updates a job to start an hour from now and repeat every 1 hour</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Set-AzSqlElasticJob -IntervalType Hour -IntervalCount 1 -StartTime (Get-Date).AddHours(1) -Enable

JobName Version Description StartTime            EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------            -------                ------------ -------- -------
job1    0                   6/1/2018 10:50:15 PM 12/31/9999 11:59:59 AM Recurring    PT1H     True
```

<span data-ttu-id="444a5-118">Aggiorna un processo</span><span class="sxs-lookup"><span data-stu-id="444a5-118">Updates a job</span></span>

### <span data-ttu-id="444a5-119">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="444a5-119">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticJob -AgentName agent -Enable -IntervalCount 1 -IntervalType Hour -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1 -StartTime '9/16/2016 11:31:12'
```

## <span data-ttu-id="444a5-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="444a5-120">PARAMETERS</span></span>

### <span data-ttu-id="444a5-121">-AgentName</span><span class="sxs-lookup"><span data-stu-id="444a5-121">-AgentName</span></span>
<span data-ttu-id="444a5-122">Il nome dell'agente</span><span class="sxs-lookup"><span data-stu-id="444a5-122">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, RunOnce, Recurring
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="444a5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="444a5-123">-DefaultProfile</span></span>
<span data-ttu-id="444a5-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="444a5-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="444a5-125">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="444a5-125">-Description</span></span>
<span data-ttu-id="444a5-126">Descrizione dell'incarico</span><span class="sxs-lookup"><span data-stu-id="444a5-126">The job description</span></span>

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

### <span data-ttu-id="444a5-127">-Enable</span><span class="sxs-lookup"><span data-stu-id="444a5-127">-Enable</span></span>
<span data-ttu-id="444a5-128">Il contrassegno per indicare che il cliente vuole che il processo sia abilitato.</span><span class="sxs-lookup"><span data-stu-id="444a5-128">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="444a5-129">-EndTime</span><span class="sxs-lookup"><span data-stu-id="444a5-129">-EndTime</span></span>
<span data-ttu-id="444a5-130">Ora di fine della pianificazione del processo</span><span class="sxs-lookup"><span data-stu-id="444a5-130">The job schedule end time</span></span>

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

### <span data-ttu-id="444a5-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="444a5-131">-InputObject</span></span>
<span data-ttu-id="444a5-132">Oggetto di input del processo</span><span class="sxs-lookup"><span data-stu-id="444a5-132">The job input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet, RunOnceUsingParentObject, RecurringUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="444a5-133">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="444a5-133">-IntervalCount</span></span>
<span data-ttu-id="444a5-134">Il numero di intervalli di pianificazione ricorrente</span><span class="sxs-lookup"><span data-stu-id="444a5-134">The recurring schedule interval count</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: Recurring, RecurringUsingParentObject, RecurringUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="444a5-135">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="444a5-135">-IntervalType</span></span>
<span data-ttu-id="444a5-136">Il tipo di intervallo di pianificazione ricorrente può essere Minuto, Ora, Giorno, Settimana, Mese</span><span class="sxs-lookup"><span data-stu-id="444a5-136">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

```yaml
Type: System.String
Parameter Sets: Recurring, RecurringUsingParentObject, RecurringUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="444a5-137">-Name</span><span class="sxs-lookup"><span data-stu-id="444a5-137">-Name</span></span>
<span data-ttu-id="444a5-138">Nome del processo</span><span class="sxs-lookup"><span data-stu-id="444a5-138">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, RunOnce, Recurring
Aliases: JobName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="444a5-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="444a5-139">-ResourceGroupName</span></span>
<span data-ttu-id="444a5-140">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="444a5-140">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, RunOnce, Recurring
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="444a5-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="444a5-141">-ResourceId</span></span>
<span data-ttu-id="444a5-142">ID risorsa processo</span><span class="sxs-lookup"><span data-stu-id="444a5-142">The job resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, RunOnceUsingParentResourceId, RecurringUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="444a5-143">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="444a5-143">-RunOnce</span></span>
<span data-ttu-id="444a5-144">Il contrassegno per indicare che il processo verrà eseguito una sola volta</span><span class="sxs-lookup"><span data-stu-id="444a5-144">The flag to indicate job will be run once</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RunOnce, RunOnceUsingParentObject, RunOnceUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="444a5-145">-ServerName</span><span class="sxs-lookup"><span data-stu-id="444a5-145">-ServerName</span></span>
<span data-ttu-id="444a5-146">Il nome del server</span><span class="sxs-lookup"><span data-stu-id="444a5-146">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, RunOnce, Recurring
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="444a5-147">-StartTime</span><span class="sxs-lookup"><span data-stu-id="444a5-147">-StartTime</span></span>
<span data-ttu-id="444a5-148">Ora di inizio della pianificazione del processo</span><span class="sxs-lookup"><span data-stu-id="444a5-148">The job schedule start time</span></span>

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

### <span data-ttu-id="444a5-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="444a5-149">-Confirm</span></span>
<span data-ttu-id="444a5-150">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="444a5-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="444a5-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="444a5-151">-WhatIf</span></span>
<span data-ttu-id="444a5-152">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="444a5-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="444a5-153">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="444a5-153">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="444a5-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="444a5-154">CommonParameters</span></span>
<span data-ttu-id="444a5-155">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="444a5-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="444a5-156">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="444a5-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="444a5-157">INPUT</span><span class="sxs-lookup"><span data-stu-id="444a5-157">INPUTS</span></span>

### <span data-ttu-id="444a5-158">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="444a5-158">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="444a5-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="444a5-159">OUTPUTS</span></span>

### <span data-ttu-id="444a5-160">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="444a5-160">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="444a5-161">NOTE</span><span class="sxs-lookup"><span data-stu-id="444a5-161">NOTES</span></span>

## <span data-ttu-id="444a5-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="444a5-162">RELATED LINKS</span></span>
