---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
ms.openlocfilehash: 98c019c8dedf767fc2b75bb2133f7c545ffd03ce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864378"
---
# <span data-ttu-id="61d75-101">New-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="61d75-101">New-AzSqlElasticJob</span></span>

## <span data-ttu-id="61d75-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="61d75-102">SYNOPSIS</span></span>
<span data-ttu-id="61d75-103">Crea un nuovo processo</span><span class="sxs-lookup"><span data-stu-id="61d75-103">Creates a new job</span></span>

## <span data-ttu-id="61d75-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="61d75-104">SYNTAX</span></span>

### <span data-ttu-id="61d75-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="61d75-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="61d75-106">RunOnce</span><span class="sxs-lookup"><span data-stu-id="61d75-106">RunOnce</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61d75-107">Ricorrenti</span><span class="sxs-lookup"><span data-stu-id="61d75-107">Recurring</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="61d75-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="61d75-108">ObjectSet</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-Description <String>]
 [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61d75-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="61d75-109">RunOnceUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-RunOnce]
 [-StartTime <DateTime>] [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61d75-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="61d75-110">RecurringUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61d75-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="61d75-111">ResourceIdSet</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61d75-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="61d75-112">RunOnceUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-RunOnce] [-StartTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="61d75-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="61d75-113">RecurringUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61d75-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61d75-114">DESCRIPTION</span></span>
<span data-ttu-id="61d75-115">Il cmdlet New-AzSqlElasticJob crea un nuovo processo</span><span class="sxs-lookup"><span data-stu-id="61d75-115">The New-AzSqlElasticJob cmdlet creates a new job</span></span>

## <span data-ttu-id="61d75-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="61d75-116">EXAMPLES</span></span>

### <span data-ttu-id="61d75-117">Esempio 1-crea un nuovo processo</span><span class="sxs-lookup"><span data-stu-id="61d75-117">Example 1 - Creates a new job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="61d75-118">Crea un nuovo processo</span><span class="sxs-lookup"><span data-stu-id="61d75-118">Creates a new job</span></span>

## <span data-ttu-id="61d75-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="61d75-119">PARAMETERS</span></span>

### <span data-ttu-id="61d75-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="61d75-120">-AgentName</span></span>
<span data-ttu-id="61d75-121">Nome dell'agente</span><span class="sxs-lookup"><span data-stu-id="61d75-121">The agent name</span></span>

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

### <span data-ttu-id="61d75-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61d75-122">-DefaultProfile</span></span>
<span data-ttu-id="61d75-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="61d75-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61d75-124">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="61d75-124">-Description</span></span>
<span data-ttu-id="61d75-125">Descrizione del processo</span><span class="sxs-lookup"><span data-stu-id="61d75-125">The job description</span></span>

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

### <span data-ttu-id="61d75-126">-Enable</span><span class="sxs-lookup"><span data-stu-id="61d75-126">-Enable</span></span>
<span data-ttu-id="61d75-127">Il contrassegno per indicare che il cliente vuole che questo processo sia abilitato.</span><span class="sxs-lookup"><span data-stu-id="61d75-127">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="61d75-128">-EndTime</span><span class="sxs-lookup"><span data-stu-id="61d75-128">-EndTime</span></span>
<span data-ttu-id="61d75-129">Ora di fine pianificazione processo</span><span class="sxs-lookup"><span data-stu-id="61d75-129">The job schedule end time</span></span>

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

### <span data-ttu-id="61d75-130">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="61d75-130">-IntervalCount</span></span>
<span data-ttu-id="61d75-131">Conteggio intervalli di programmazione ricorrente</span><span class="sxs-lookup"><span data-stu-id="61d75-131">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="61d75-132">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="61d75-132">-IntervalType</span></span>
<span data-ttu-id="61d75-133">Il tipo di intervallo di programmazione ricorrente-può essere minuto, ora, giorno, settimana, mese</span><span class="sxs-lookup"><span data-stu-id="61d75-133">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="61d75-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="61d75-134">-Name</span></span>
<span data-ttu-id="61d75-135">Il nome del processo</span><span class="sxs-lookup"><span data-stu-id="61d75-135">The job name</span></span>

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

### <span data-ttu-id="61d75-136">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="61d75-136">-ParentObject</span></span>
<span data-ttu-id="61d75-137">Oggetto di input dell'agente</span><span class="sxs-lookup"><span data-stu-id="61d75-137">The agent input object</span></span>

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

### <span data-ttu-id="61d75-138">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="61d75-138">-ParentResourceId</span></span>
<span data-ttu-id="61d75-139">ID risorsa agente</span><span class="sxs-lookup"><span data-stu-id="61d75-139">The agent resource id</span></span>

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

### <span data-ttu-id="61d75-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61d75-140">-ResourceGroupName</span></span>
<span data-ttu-id="61d75-141">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="61d75-141">The resource group name</span></span>

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

### <span data-ttu-id="61d75-142">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="61d75-142">-RunOnce</span></span>
<span data-ttu-id="61d75-143">Il contrassegno per indicare il processo verrà eseguito una sola volta</span><span class="sxs-lookup"><span data-stu-id="61d75-143">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="61d75-144">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="61d75-144">-ServerName</span></span>
<span data-ttu-id="61d75-145">Nome del server</span><span class="sxs-lookup"><span data-stu-id="61d75-145">The server name</span></span>

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

### <span data-ttu-id="61d75-146">-StartTime</span><span class="sxs-lookup"><span data-stu-id="61d75-146">-StartTime</span></span>
<span data-ttu-id="61d75-147">Orario di inizio pianificazione processo</span><span class="sxs-lookup"><span data-stu-id="61d75-147">The job schedule start time</span></span>

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

### <span data-ttu-id="61d75-148">-Confermare</span><span class="sxs-lookup"><span data-stu-id="61d75-148">-Confirm</span></span>
<span data-ttu-id="61d75-149">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61d75-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61d75-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61d75-150">-WhatIf</span></span>
<span data-ttu-id="61d75-151">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="61d75-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61d75-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="61d75-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61d75-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61d75-153">CommonParameters</span></span>
<span data-ttu-id="61d75-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61d75-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61d75-155">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="61d75-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61d75-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="61d75-156">INPUTS</span></span>

### <span data-ttu-id="61d75-157">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="61d75-157">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="61d75-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="61d75-158">OUTPUTS</span></span>

### <span data-ttu-id="61d75-159">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="61d75-159">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="61d75-160">Note</span><span class="sxs-lookup"><span data-stu-id="61d75-160">NOTES</span></span>

## <span data-ttu-id="61d75-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="61d75-161">RELATED LINKS</span></span>
