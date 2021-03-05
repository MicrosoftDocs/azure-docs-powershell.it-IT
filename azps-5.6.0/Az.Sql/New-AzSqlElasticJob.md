---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
ms.openlocfilehash: 961f37db94cff87952b2811a528a94cc71ffabff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010158"
---
# <span data-ttu-id="2e837-101">New-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="2e837-101">New-AzSqlElasticJob</span></span>

## <span data-ttu-id="2e837-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e837-102">SYNOPSIS</span></span>
<span data-ttu-id="2e837-103">Crea un nuovo processo</span><span class="sxs-lookup"><span data-stu-id="2e837-103">Creates a new job</span></span>

## <span data-ttu-id="2e837-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2e837-104">SYNTAX</span></span>

### <span data-ttu-id="2e837-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2e837-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2e837-106">RunOnce</span><span class="sxs-lookup"><span data-stu-id="2e837-106">RunOnce</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e837-107">Ricorrente</span><span class="sxs-lookup"><span data-stu-id="2e837-107">Recurring</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2e837-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="2e837-108">ObjectSet</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-Description <String>]
 [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e837-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="2e837-109">RunOnceUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-RunOnce]
 [-StartTime <DateTime>] [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e837-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="2e837-110">RecurringUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e837-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2e837-111">ResourceIdSet</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e837-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="2e837-112">RunOnceUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-RunOnce] [-StartTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2e837-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="2e837-113">RecurringUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e837-114">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2e837-114">DESCRIPTION</span></span>
<span data-ttu-id="2e837-115">Il cmdlet New-AzSqlElasticJob crea un nuovo processo</span><span class="sxs-lookup"><span data-stu-id="2e837-115">The New-AzSqlElasticJob cmdlet creates a new job</span></span>

## <span data-ttu-id="2e837-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2e837-116">EXAMPLES</span></span>

### <span data-ttu-id="2e837-117">Esempio 1: Creare un nuovo processo</span><span class="sxs-lookup"><span data-stu-id="2e837-117">Example 1: Creates a new job</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="2e837-118">Crea un nuovo processo</span><span class="sxs-lookup"><span data-stu-id="2e837-118">Creates a new job</span></span>

### <span data-ttu-id="2e837-119">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="2e837-119">Example 2</span></span>

<span data-ttu-id="2e837-120">Crea un nuovo processo.</span><span class="sxs-lookup"><span data-stu-id="2e837-120">Creates a new job.</span></span> <span data-ttu-id="2e837-121">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="2e837-121">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlElasticJob -Name job1 -RunOnce
```

## <span data-ttu-id="2e837-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e837-122">PARAMETERS</span></span>

### <span data-ttu-id="2e837-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="2e837-123">-AgentName</span></span>
<span data-ttu-id="2e837-124">Il nome dell'agente</span><span class="sxs-lookup"><span data-stu-id="2e837-124">The agent name</span></span>

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

### <span data-ttu-id="2e837-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e837-125">-DefaultProfile</span></span>
<span data-ttu-id="2e837-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2e837-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e837-127">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="2e837-127">-Description</span></span>
<span data-ttu-id="2e837-128">Descrizione dell'incarico</span><span class="sxs-lookup"><span data-stu-id="2e837-128">The job description</span></span>

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

### <span data-ttu-id="2e837-129">-Enable</span><span class="sxs-lookup"><span data-stu-id="2e837-129">-Enable</span></span>
<span data-ttu-id="2e837-130">Il contrassegno per indicare che il cliente vuole che il processo sia abilitato.</span><span class="sxs-lookup"><span data-stu-id="2e837-130">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="2e837-131">-EndTime</span><span class="sxs-lookup"><span data-stu-id="2e837-131">-EndTime</span></span>
<span data-ttu-id="2e837-132">Ora di fine della pianificazione del processo</span><span class="sxs-lookup"><span data-stu-id="2e837-132">The job schedule end time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: Recurring, RecurringUsingParentObject, RecurringUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e837-133">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="2e837-133">-IntervalCount</span></span>
<span data-ttu-id="2e837-134">Il numero di intervalli di pianificazione ricorrente</span><span class="sxs-lookup"><span data-stu-id="2e837-134">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="2e837-135">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="2e837-135">-IntervalType</span></span>
<span data-ttu-id="2e837-136">Il tipo di intervallo di pianificazione ricorrente può essere Minuto, Ora, Giorno, Settimana, Mese</span><span class="sxs-lookup"><span data-stu-id="2e837-136">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="2e837-137">-Name</span><span class="sxs-lookup"><span data-stu-id="2e837-137">-Name</span></span>
<span data-ttu-id="2e837-138">Nome del processo</span><span class="sxs-lookup"><span data-stu-id="2e837-138">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: JobName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e837-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="2e837-139">-ParentObject</span></span>
<span data-ttu-id="2e837-140">Oggetto di input agente</span><span class="sxs-lookup"><span data-stu-id="2e837-140">The agent input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel
Parameter Sets: ObjectSet, RunOnceUsingParentObject, RecurringUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e837-141">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="2e837-141">-ParentResourceId</span></span>
<span data-ttu-id="2e837-142">ID risorsa agente</span><span class="sxs-lookup"><span data-stu-id="2e837-142">The agent resource id</span></span>

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

### <span data-ttu-id="2e837-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e837-143">-ResourceGroupName</span></span>
<span data-ttu-id="2e837-144">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="2e837-144">The resource group name</span></span>

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

### <span data-ttu-id="2e837-145">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="2e837-145">-RunOnce</span></span>
<span data-ttu-id="2e837-146">Il contrassegno per indicare che il processo verrà eseguito una sola volta</span><span class="sxs-lookup"><span data-stu-id="2e837-146">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="2e837-147">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2e837-147">-ServerName</span></span>
<span data-ttu-id="2e837-148">Il nome del server</span><span class="sxs-lookup"><span data-stu-id="2e837-148">The server name</span></span>

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

### <span data-ttu-id="2e837-149">-StartTime</span><span class="sxs-lookup"><span data-stu-id="2e837-149">-StartTime</span></span>
<span data-ttu-id="2e837-150">Ora di inizio della pianificazione del processo</span><span class="sxs-lookup"><span data-stu-id="2e837-150">The job schedule start time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: RunOnce, Recurring, RunOnceUsingParentObject, RecurringUsingParentObject, RunOnceUsingParentResourceId, RecurringUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e837-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2e837-151">-Confirm</span></span>
<span data-ttu-id="2e837-152">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e837-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e837-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e837-153">-WhatIf</span></span>
<span data-ttu-id="2e837-154">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2e837-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e837-155">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2e837-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e837-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e837-156">CommonParameters</span></span>
<span data-ttu-id="2e837-157">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e837-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e837-158">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2e837-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e837-159">INPUT</span><span class="sxs-lookup"><span data-stu-id="2e837-159">INPUTS</span></span>

### <span data-ttu-id="2e837-160">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="2e837-160">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="2e837-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2e837-161">OUTPUTS</span></span>

### <span data-ttu-id="2e837-162">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="2e837-162">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="2e837-163">NOTE</span><span class="sxs-lookup"><span data-stu-id="2e837-163">NOTES</span></span>

## <span data-ttu-id="2e837-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2e837-164">RELATED LINKS</span></span>
