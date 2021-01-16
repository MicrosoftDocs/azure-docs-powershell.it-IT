---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
ms.openlocfilehash: e6853c3b4fa32a10e93ee281aab0b97755403671
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325200"
---
# <span data-ttu-id="5e3fc-101">New-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="5e3fc-101">New-AzSqlElasticJob</span></span>

## <span data-ttu-id="5e3fc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5e3fc-102">SYNOPSIS</span></span>
<span data-ttu-id="5e3fc-103">Crea un nuovo processo</span><span class="sxs-lookup"><span data-stu-id="5e3fc-103">Creates a new job</span></span>

## <span data-ttu-id="5e3fc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5e3fc-104">SYNTAX</span></span>

### <span data-ttu-id="5e3fc-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5e3fc-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5e3fc-106">RunOnce</span><span class="sxs-lookup"><span data-stu-id="5e3fc-106">RunOnce</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e3fc-107">Ricorrenti</span><span class="sxs-lookup"><span data-stu-id="5e3fc-107">Recurring</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5e3fc-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="5e3fc-108">ObjectSet</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-Description <String>]
 [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e3fc-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="5e3fc-109">RunOnceUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-RunOnce]
 [-StartTime <DateTime>] [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e3fc-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="5e3fc-110">RecurringUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e3fc-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5e3fc-111">ResourceIdSet</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e3fc-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5e3fc-112">RunOnceUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-RunOnce] [-StartTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5e3fc-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5e3fc-113">RecurringUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e3fc-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e3fc-114">DESCRIPTION</span></span>
<span data-ttu-id="5e3fc-115">Il cmdlet New-AzSqlElasticJob crea un nuovo processo</span><span class="sxs-lookup"><span data-stu-id="5e3fc-115">The New-AzSqlElasticJob cmdlet creates a new job</span></span>

## <span data-ttu-id="5e3fc-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5e3fc-116">EXAMPLES</span></span>

### <span data-ttu-id="5e3fc-117">Esempio 1: crea un nuovo processo</span><span class="sxs-lookup"><span data-stu-id="5e3fc-117">Example 1: Creates a new job</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="5e3fc-118">Crea un nuovo processo</span><span class="sxs-lookup"><span data-stu-id="5e3fc-118">Creates a new job</span></span>

### <span data-ttu-id="5e3fc-119">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="5e3fc-119">Example 2</span></span>

<span data-ttu-id="5e3fc-120">Crea un nuovo processo.</span><span class="sxs-lookup"><span data-stu-id="5e3fc-120">Creates a new job.</span></span> <span data-ttu-id="5e3fc-121">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="5e3fc-121">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlElasticJob -Name job1 -RunOnce
```

## <span data-ttu-id="5e3fc-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5e3fc-122">PARAMETERS</span></span>

### <span data-ttu-id="5e3fc-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="5e3fc-123">-AgentName</span></span>
<span data-ttu-id="5e3fc-124">Nome dell'agente</span><span class="sxs-lookup"><span data-stu-id="5e3fc-124">The agent name</span></span>

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

### <span data-ttu-id="5e3fc-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e3fc-125">-DefaultProfile</span></span>
<span data-ttu-id="5e3fc-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5e3fc-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e3fc-127">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e3fc-127">-Description</span></span>
<span data-ttu-id="5e3fc-128">Descrizione del processo</span><span class="sxs-lookup"><span data-stu-id="5e3fc-128">The job description</span></span>

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

### <span data-ttu-id="5e3fc-129">-Enable</span><span class="sxs-lookup"><span data-stu-id="5e3fc-129">-Enable</span></span>
<span data-ttu-id="5e3fc-130">Il contrassegno per indicare che il cliente vuole che questo processo sia abilitato.</span><span class="sxs-lookup"><span data-stu-id="5e3fc-130">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="5e3fc-131">-EndTime</span><span class="sxs-lookup"><span data-stu-id="5e3fc-131">-EndTime</span></span>
<span data-ttu-id="5e3fc-132">Ora di fine pianificazione processo</span><span class="sxs-lookup"><span data-stu-id="5e3fc-132">The job schedule end time</span></span>

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

### <span data-ttu-id="5e3fc-133">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="5e3fc-133">-IntervalCount</span></span>
<span data-ttu-id="5e3fc-134">Conteggio intervalli di programmazione ricorrente</span><span class="sxs-lookup"><span data-stu-id="5e3fc-134">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="5e3fc-135">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="5e3fc-135">-IntervalType</span></span>
<span data-ttu-id="5e3fc-136">Il tipo di intervallo di programmazione ricorrente-può essere minuto, ora, giorno, settimana, mese</span><span class="sxs-lookup"><span data-stu-id="5e3fc-136">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="5e3fc-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="5e3fc-137">-Name</span></span>
<span data-ttu-id="5e3fc-138">Il nome del processo</span><span class="sxs-lookup"><span data-stu-id="5e3fc-138">The job name</span></span>

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

### <span data-ttu-id="5e3fc-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5e3fc-139">-ParentObject</span></span>
<span data-ttu-id="5e3fc-140">Oggetto di input dell'agente</span><span class="sxs-lookup"><span data-stu-id="5e3fc-140">The agent input object</span></span>

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

### <span data-ttu-id="5e3fc-141">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5e3fc-141">-ParentResourceId</span></span>
<span data-ttu-id="5e3fc-142">ID risorsa agente</span><span class="sxs-lookup"><span data-stu-id="5e3fc-142">The agent resource id</span></span>

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

### <span data-ttu-id="5e3fc-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e3fc-143">-ResourceGroupName</span></span>
<span data-ttu-id="5e3fc-144">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="5e3fc-144">The resource group name</span></span>

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

### <span data-ttu-id="5e3fc-145">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="5e3fc-145">-RunOnce</span></span>
<span data-ttu-id="5e3fc-146">Il contrassegno per indicare il processo verrà eseguito una sola volta</span><span class="sxs-lookup"><span data-stu-id="5e3fc-146">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="5e3fc-147">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="5e3fc-147">-ServerName</span></span>
<span data-ttu-id="5e3fc-148">Nome del server</span><span class="sxs-lookup"><span data-stu-id="5e3fc-148">The server name</span></span>

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

### <span data-ttu-id="5e3fc-149">-StartTime</span><span class="sxs-lookup"><span data-stu-id="5e3fc-149">-StartTime</span></span>
<span data-ttu-id="5e3fc-150">Orario di inizio pianificazione processo</span><span class="sxs-lookup"><span data-stu-id="5e3fc-150">The job schedule start time</span></span>

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

### <span data-ttu-id="5e3fc-151">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5e3fc-151">-Confirm</span></span>
<span data-ttu-id="5e3fc-152">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e3fc-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e3fc-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e3fc-153">-WhatIf</span></span>
<span data-ttu-id="5e3fc-154">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5e3fc-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e3fc-155">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5e3fc-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e3fc-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e3fc-156">CommonParameters</span></span>
<span data-ttu-id="5e3fc-157">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e3fc-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e3fc-158">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e3fc-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e3fc-159">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5e3fc-159">INPUTS</span></span>

### <span data-ttu-id="5e3fc-160">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="5e3fc-160">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="5e3fc-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5e3fc-161">OUTPUTS</span></span>

### <span data-ttu-id="5e3fc-162">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="5e3fc-162">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="5e3fc-163">Note</span><span class="sxs-lookup"><span data-stu-id="5e3fc-163">NOTES</span></span>

## <span data-ttu-id="5e3fc-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5e3fc-164">RELATED LINKS</span></span>
