---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
ms.openlocfilehash: 53bd1b1cd1c2f7ba87df8cb5c27f1b2380db04af
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354703"
---
# <span data-ttu-id="6b7c8-101">Set-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="6b7c8-101">Set-AzSqlElasticJob</span></span>

## <span data-ttu-id="6b7c8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6b7c8-102">SYNOPSIS</span></span>
<span data-ttu-id="6b7c8-103">Aggiorna un processo</span><span class="sxs-lookup"><span data-stu-id="6b7c8-103">Updates a job</span></span>

## <span data-ttu-id="6b7c8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6b7c8-104">SYNTAX</span></span>

### <span data-ttu-id="6b7c8-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6b7c8-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b7c8-106">RunOnce</span><span class="sxs-lookup"><span data-stu-id="6b7c8-106">RunOnce</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b7c8-107">Ricorrenti</span><span class="sxs-lookup"><span data-stu-id="6b7c8-107">Recurring</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b7c8-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="6b7c8-108">ObjectSet</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6b7c8-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="6b7c8-109">RunOnceUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-RunOnce] [-StartTime <DateTime>]
 [-EndTime <DateTime>] [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b7c8-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="6b7c8-110">RecurringUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b7c8-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6b7c8-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b7c8-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="6b7c8-112">RunOnceUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b7c8-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="6b7c8-113">RecurringUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b7c8-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6b7c8-114">DESCRIPTION</span></span>
<span data-ttu-id="6b7c8-115">Il cmdlet Set-AzSqlElasticJob aggiorna un processo</span><span class="sxs-lookup"><span data-stu-id="6b7c8-115">The Set-AzSqlElasticJob cmdlet updates a job</span></span>

## <span data-ttu-id="6b7c8-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6b7c8-116">EXAMPLES</span></span>

### <span data-ttu-id="6b7c8-117">Esempio 1: aggiorna un processo per iniziare un'ora da ora e ripetere ogni 1 ora</span><span class="sxs-lookup"><span data-stu-id="6b7c8-117">Example 1: Updates a job to start an hour from now and repeat every 1 hour</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Set-AzSqlElasticJob -IntervalType Hour -IntervalCount 1 -StartTime (Get-Date).AddHours(1) -Enable

JobName Version Description StartTime            EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------            -------                ------------ -------- -------
job1    0                   6/1/2018 10:50:15 PM 12/31/9999 11:59:59 AM Recurring    PT1H     True
```

<span data-ttu-id="6b7c8-118">Aggiorna un processo</span><span class="sxs-lookup"><span data-stu-id="6b7c8-118">Updates a job</span></span>

### <span data-ttu-id="6b7c8-119">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="6b7c8-119">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticJob -AgentName agent -Enable -IntervalCount 1 -IntervalType Hour -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1 -StartTime '9/16/2016 11:31:12'
```

## <span data-ttu-id="6b7c8-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6b7c8-120">PARAMETERS</span></span>

### <span data-ttu-id="6b7c8-121">-AgentName</span><span class="sxs-lookup"><span data-stu-id="6b7c8-121">-AgentName</span></span>
<span data-ttu-id="6b7c8-122">Nome dell'agente</span><span class="sxs-lookup"><span data-stu-id="6b7c8-122">The agent name</span></span>

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

### <span data-ttu-id="6b7c8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b7c8-123">-DefaultProfile</span></span>
<span data-ttu-id="6b7c8-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6b7c8-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b7c8-125">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="6b7c8-125">-Description</span></span>
<span data-ttu-id="6b7c8-126">Descrizione del processo</span><span class="sxs-lookup"><span data-stu-id="6b7c8-126">The job description</span></span>

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

### <span data-ttu-id="6b7c8-127">-Enable</span><span class="sxs-lookup"><span data-stu-id="6b7c8-127">-Enable</span></span>
<span data-ttu-id="6b7c8-128">Il contrassegno per indicare che il cliente vuole che questo processo sia abilitato.</span><span class="sxs-lookup"><span data-stu-id="6b7c8-128">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="6b7c8-129">-EndTime</span><span class="sxs-lookup"><span data-stu-id="6b7c8-129">-EndTime</span></span>
<span data-ttu-id="6b7c8-130">Ora di fine pianificazione processo</span><span class="sxs-lookup"><span data-stu-id="6b7c8-130">The job schedule end time</span></span>

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

### <span data-ttu-id="6b7c8-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b7c8-131">-InputObject</span></span>
<span data-ttu-id="6b7c8-132">Oggetto input processo</span><span class="sxs-lookup"><span data-stu-id="6b7c8-132">The job input object</span></span>

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

### <span data-ttu-id="6b7c8-133">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="6b7c8-133">-IntervalCount</span></span>
<span data-ttu-id="6b7c8-134">Conteggio intervalli di programmazione ricorrente</span><span class="sxs-lookup"><span data-stu-id="6b7c8-134">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="6b7c8-135">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="6b7c8-135">-IntervalType</span></span>
<span data-ttu-id="6b7c8-136">Il tipo di intervallo di programmazione ricorrente-può essere minuto, ora, giorno, settimana, mese</span><span class="sxs-lookup"><span data-stu-id="6b7c8-136">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="6b7c8-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="6b7c8-137">-Name</span></span>
<span data-ttu-id="6b7c8-138">Il nome del processo</span><span class="sxs-lookup"><span data-stu-id="6b7c8-138">The job name</span></span>

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

### <span data-ttu-id="6b7c8-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b7c8-139">-ResourceGroupName</span></span>
<span data-ttu-id="6b7c8-140">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="6b7c8-140">The resource group name</span></span>

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

### <span data-ttu-id="6b7c8-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b7c8-141">-ResourceId</span></span>
<span data-ttu-id="6b7c8-142">ID risorsa processo</span><span class="sxs-lookup"><span data-stu-id="6b7c8-142">The job resource id</span></span>

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

### <span data-ttu-id="6b7c8-143">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="6b7c8-143">-RunOnce</span></span>
<span data-ttu-id="6b7c8-144">Il contrassegno per indicare il processo verrà eseguito una sola volta</span><span class="sxs-lookup"><span data-stu-id="6b7c8-144">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="6b7c8-145">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="6b7c8-145">-ServerName</span></span>
<span data-ttu-id="6b7c8-146">Nome del server</span><span class="sxs-lookup"><span data-stu-id="6b7c8-146">The server name</span></span>

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

### <span data-ttu-id="6b7c8-147">-StartTime</span><span class="sxs-lookup"><span data-stu-id="6b7c8-147">-StartTime</span></span>
<span data-ttu-id="6b7c8-148">Orario di inizio pianificazione processo</span><span class="sxs-lookup"><span data-stu-id="6b7c8-148">The job schedule start time</span></span>

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

### <span data-ttu-id="6b7c8-149">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6b7c8-149">-Confirm</span></span>
<span data-ttu-id="6b7c8-150">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b7c8-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b7c8-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b7c8-151">-WhatIf</span></span>
<span data-ttu-id="6b7c8-152">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6b7c8-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b7c8-153">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6b7c8-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b7c8-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b7c8-154">CommonParameters</span></span>
<span data-ttu-id="6b7c8-155">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b7c8-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b7c8-156">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b7c8-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b7c8-157">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6b7c8-157">INPUTS</span></span>

### <span data-ttu-id="6b7c8-158">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="6b7c8-158">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="6b7c8-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6b7c8-159">OUTPUTS</span></span>

### <span data-ttu-id="6b7c8-160">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="6b7c8-160">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="6b7c8-161">Note</span><span class="sxs-lookup"><span data-stu-id="6b7c8-161">NOTES</span></span>

## <span data-ttu-id="6b7c8-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6b7c8-162">RELATED LINKS</span></span>
