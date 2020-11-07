---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
ms.openlocfilehash: 04f182cb410e77a9ca61aa6f80da14c08e517406
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857129"
---
# <span data-ttu-id="b9785-101">Set-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="b9785-101">Set-AzSqlElasticJob</span></span>

## <span data-ttu-id="b9785-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b9785-102">SYNOPSIS</span></span>
<span data-ttu-id="b9785-103">Aggiorna un processo</span><span class="sxs-lookup"><span data-stu-id="b9785-103">Updates a job</span></span>

## <span data-ttu-id="b9785-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b9785-104">SYNTAX</span></span>

### <span data-ttu-id="b9785-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b9785-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9785-106">RunOnce</span><span class="sxs-lookup"><span data-stu-id="b9785-106">RunOnce</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9785-107">Ricorrenti</span><span class="sxs-lookup"><span data-stu-id="b9785-107">Recurring</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9785-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="b9785-108">ObjectSet</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b9785-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="b9785-109">RunOnceUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-RunOnce] [-StartTime <DateTime>]
 [-EndTime <DateTime>] [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9785-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="b9785-110">RecurringUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9785-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b9785-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9785-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b9785-112">RunOnceUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9785-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b9785-113">RecurringUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9785-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9785-114">DESCRIPTION</span></span>
<span data-ttu-id="b9785-115">Il cmdlet Set-AzSqlElasticJob aggiorna un processo</span><span class="sxs-lookup"><span data-stu-id="b9785-115">The Set-AzSqlElasticJob cmdlet updates a job</span></span>

## <span data-ttu-id="b9785-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b9785-116">EXAMPLES</span></span>

### <span data-ttu-id="b9785-117">Esempio 1-aggiorna un processo per iniziare un'ora da ora e ripetere ogni 1 ora</span><span class="sxs-lookup"><span data-stu-id="b9785-117">Example 1 - Updates a job to start an hour from now and repeat every 1 hour</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Set-AzSqlElasticJob -IntervalType Hour -IntervalCount 1 -StartTime (Get-Date).AddHours(1) -Enable

JobName Version Description StartTime            EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------            -------                ------------ -------- -------
job1    0                   6/1/2018 10:50:15 PM 12/31/9999 11:59:59 AM Recurring    PT1H     True
```

<span data-ttu-id="b9785-118">Aggiorna un processo</span><span class="sxs-lookup"><span data-stu-id="b9785-118">Updates a job</span></span>

## <span data-ttu-id="b9785-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b9785-119">PARAMETERS</span></span>

### <span data-ttu-id="b9785-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="b9785-120">-AgentName</span></span>
<span data-ttu-id="b9785-121">Nome dell'agente</span><span class="sxs-lookup"><span data-stu-id="b9785-121">The agent name</span></span>

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

### <span data-ttu-id="b9785-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9785-122">-DefaultProfile</span></span>
<span data-ttu-id="b9785-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b9785-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9785-124">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9785-124">-Description</span></span>
<span data-ttu-id="b9785-125">Descrizione del processo</span><span class="sxs-lookup"><span data-stu-id="b9785-125">The job description</span></span>

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

### <span data-ttu-id="b9785-126">-Enable</span><span class="sxs-lookup"><span data-stu-id="b9785-126">-Enable</span></span>
<span data-ttu-id="b9785-127">Il contrassegno per indicare che il cliente vuole che questo processo sia abilitato.</span><span class="sxs-lookup"><span data-stu-id="b9785-127">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="b9785-128">-EndTime</span><span class="sxs-lookup"><span data-stu-id="b9785-128">-EndTime</span></span>
<span data-ttu-id="b9785-129">Ora di fine pianificazione processo</span><span class="sxs-lookup"><span data-stu-id="b9785-129">The job schedule end time</span></span>

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

### <span data-ttu-id="b9785-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b9785-130">-InputObject</span></span>
<span data-ttu-id="b9785-131">Oggetto input processo</span><span class="sxs-lookup"><span data-stu-id="b9785-131">The job input object</span></span>

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

### <span data-ttu-id="b9785-132">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="b9785-132">-IntervalCount</span></span>
<span data-ttu-id="b9785-133">Conteggio intervalli di programmazione ricorrente</span><span class="sxs-lookup"><span data-stu-id="b9785-133">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="b9785-134">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="b9785-134">-IntervalType</span></span>
<span data-ttu-id="b9785-135">Il tipo di intervallo di programmazione ricorrente-può essere minuto, ora, giorno, settimana, mese</span><span class="sxs-lookup"><span data-stu-id="b9785-135">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="b9785-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="b9785-136">-Name</span></span>
<span data-ttu-id="b9785-137">Il nome del processo</span><span class="sxs-lookup"><span data-stu-id="b9785-137">The job name</span></span>

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

### <span data-ttu-id="b9785-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9785-138">-ResourceGroupName</span></span>
<span data-ttu-id="b9785-139">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="b9785-139">The resource group name</span></span>

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

### <span data-ttu-id="b9785-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9785-140">-ResourceId</span></span>
<span data-ttu-id="b9785-141">ID risorsa processo</span><span class="sxs-lookup"><span data-stu-id="b9785-141">The job resource id</span></span>

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

### <span data-ttu-id="b9785-142">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="b9785-142">-RunOnce</span></span>
<span data-ttu-id="b9785-143">Il contrassegno per indicare il processo verrà eseguito una sola volta</span><span class="sxs-lookup"><span data-stu-id="b9785-143">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="b9785-144">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="b9785-144">-ServerName</span></span>
<span data-ttu-id="b9785-145">Nome del server</span><span class="sxs-lookup"><span data-stu-id="b9785-145">The server name</span></span>

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

### <span data-ttu-id="b9785-146">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b9785-146">-StartTime</span></span>
<span data-ttu-id="b9785-147">Orario di inizio pianificazione processo</span><span class="sxs-lookup"><span data-stu-id="b9785-147">The job schedule start time</span></span>

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

### <span data-ttu-id="b9785-148">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b9785-148">-Confirm</span></span>
<span data-ttu-id="b9785-149">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9785-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9785-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9785-150">-WhatIf</span></span>
<span data-ttu-id="b9785-151">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b9785-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9785-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b9785-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9785-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9785-153">CommonParameters</span></span>
<span data-ttu-id="b9785-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9785-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9785-155">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9785-155">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9785-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b9785-156">INPUTS</span></span>

### <span data-ttu-id="b9785-157">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="b9785-157">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="b9785-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b9785-158">OUTPUTS</span></span>

### <span data-ttu-id="b9785-159">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="b9785-159">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="b9785-160">Note</span><span class="sxs-lookup"><span data-stu-id="b9785-160">NOTES</span></span>

## <span data-ttu-id="b9785-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b9785-161">RELATED LINKS</span></span>
