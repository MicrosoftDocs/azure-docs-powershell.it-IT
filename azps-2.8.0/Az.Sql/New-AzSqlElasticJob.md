---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
ms.openlocfilehash: 29ae424807b8648238e2cc855fb90734773e870d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93856850"
---
# <span data-ttu-id="37d27-101">New-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="37d27-101">New-AzSqlElasticJob</span></span>

## <span data-ttu-id="37d27-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="37d27-102">SYNOPSIS</span></span>
<span data-ttu-id="37d27-103">Crea un nuovo processo</span><span class="sxs-lookup"><span data-stu-id="37d27-103">Creates a new job</span></span>

## <span data-ttu-id="37d27-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="37d27-104">SYNTAX</span></span>

### <span data-ttu-id="37d27-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="37d27-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="37d27-106">RunOnce</span><span class="sxs-lookup"><span data-stu-id="37d27-106">RunOnce</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37d27-107">Ricorrenti</span><span class="sxs-lookup"><span data-stu-id="37d27-107">Recurring</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="37d27-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="37d27-108">ObjectSet</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-Description <String>]
 [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37d27-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="37d27-109">RunOnceUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-RunOnce]
 [-StartTime <DateTime>] [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37d27-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="37d27-110">RecurringUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37d27-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="37d27-111">ResourceIdSet</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37d27-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="37d27-112">RunOnceUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-RunOnce] [-StartTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="37d27-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="37d27-113">RecurringUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37d27-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="37d27-114">DESCRIPTION</span></span>
<span data-ttu-id="37d27-115">Il cmdlet New-AzSqlElasticJob crea un nuovo processo</span><span class="sxs-lookup"><span data-stu-id="37d27-115">The New-AzSqlElasticJob cmdlet creates a new job</span></span>

## <span data-ttu-id="37d27-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="37d27-116">EXAMPLES</span></span>

### <span data-ttu-id="37d27-117">Esempio 1-crea un nuovo processo</span><span class="sxs-lookup"><span data-stu-id="37d27-117">Example 1 - Creates a new job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="37d27-118">Crea un nuovo processo</span><span class="sxs-lookup"><span data-stu-id="37d27-118">Creates a new job</span></span>

## <span data-ttu-id="37d27-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="37d27-119">PARAMETERS</span></span>

### <span data-ttu-id="37d27-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="37d27-120">-AgentName</span></span>
<span data-ttu-id="37d27-121">Nome dell'agente</span><span class="sxs-lookup"><span data-stu-id="37d27-121">The agent name</span></span>

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

### <span data-ttu-id="37d27-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37d27-122">-DefaultProfile</span></span>
<span data-ttu-id="37d27-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="37d27-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37d27-124">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="37d27-124">-Description</span></span>
<span data-ttu-id="37d27-125">Descrizione del processo</span><span class="sxs-lookup"><span data-stu-id="37d27-125">The job description</span></span>

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

### <span data-ttu-id="37d27-126">-Enable</span><span class="sxs-lookup"><span data-stu-id="37d27-126">-Enable</span></span>
<span data-ttu-id="37d27-127">Il contrassegno per indicare che il cliente vuole che questo processo sia abilitato.</span><span class="sxs-lookup"><span data-stu-id="37d27-127">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="37d27-128">-EndTime</span><span class="sxs-lookup"><span data-stu-id="37d27-128">-EndTime</span></span>
<span data-ttu-id="37d27-129">Ora di fine pianificazione processo</span><span class="sxs-lookup"><span data-stu-id="37d27-129">The job schedule end time</span></span>

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

### <span data-ttu-id="37d27-130">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="37d27-130">-IntervalCount</span></span>
<span data-ttu-id="37d27-131">Conteggio intervalli di programmazione ricorrente</span><span class="sxs-lookup"><span data-stu-id="37d27-131">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="37d27-132">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="37d27-132">-IntervalType</span></span>
<span data-ttu-id="37d27-133">Il tipo di intervallo di programmazione ricorrente-può essere minuto, ora, giorno, settimana, mese</span><span class="sxs-lookup"><span data-stu-id="37d27-133">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="37d27-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="37d27-134">-Name</span></span>
<span data-ttu-id="37d27-135">Il nome del processo</span><span class="sxs-lookup"><span data-stu-id="37d27-135">The job name</span></span>

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

### <span data-ttu-id="37d27-136">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="37d27-136">-ParentObject</span></span>
<span data-ttu-id="37d27-137">Oggetto di input dell'agente</span><span class="sxs-lookup"><span data-stu-id="37d27-137">The agent input object</span></span>

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

### <span data-ttu-id="37d27-138">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="37d27-138">-ParentResourceId</span></span>
<span data-ttu-id="37d27-139">ID risorsa agente</span><span class="sxs-lookup"><span data-stu-id="37d27-139">The agent resource id</span></span>

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

### <span data-ttu-id="37d27-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37d27-140">-ResourceGroupName</span></span>
<span data-ttu-id="37d27-141">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="37d27-141">The resource group name</span></span>

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

### <span data-ttu-id="37d27-142">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="37d27-142">-RunOnce</span></span>
<span data-ttu-id="37d27-143">Il contrassegno per indicare il processo verrà eseguito una sola volta</span><span class="sxs-lookup"><span data-stu-id="37d27-143">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="37d27-144">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="37d27-144">-ServerName</span></span>
<span data-ttu-id="37d27-145">Nome del server</span><span class="sxs-lookup"><span data-stu-id="37d27-145">The server name</span></span>

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

### <span data-ttu-id="37d27-146">-StartTime</span><span class="sxs-lookup"><span data-stu-id="37d27-146">-StartTime</span></span>
<span data-ttu-id="37d27-147">Orario di inizio pianificazione processo</span><span class="sxs-lookup"><span data-stu-id="37d27-147">The job schedule start time</span></span>

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

### <span data-ttu-id="37d27-148">-Confermare</span><span class="sxs-lookup"><span data-stu-id="37d27-148">-Confirm</span></span>
<span data-ttu-id="37d27-149">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37d27-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37d27-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37d27-150">-WhatIf</span></span>
<span data-ttu-id="37d27-151">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="37d27-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37d27-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="37d27-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37d27-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37d27-153">CommonParameters</span></span>
<span data-ttu-id="37d27-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37d27-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37d27-155">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37d27-155">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37d27-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="37d27-156">INPUTS</span></span>

### <span data-ttu-id="37d27-157">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="37d27-157">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="37d27-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="37d27-158">OUTPUTS</span></span>

### <span data-ttu-id="37d27-159">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="37d27-159">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="37d27-160">Note</span><span class="sxs-lookup"><span data-stu-id="37d27-160">NOTES</span></span>

## <span data-ttu-id="37d27-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="37d27-161">RELATED LINKS</span></span>
