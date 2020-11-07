---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/start-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlElasticJob.md
ms.openlocfilehash: 13e6a0bd8a4934df4d0426de38d7a56ddd5af19b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857602"
---
# <span data-ttu-id="55a7c-101">Start-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="55a7c-101">Start-AzSqlElasticJob</span></span>

## <span data-ttu-id="55a7c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="55a7c-102">SYNOPSIS</span></span>
<span data-ttu-id="55a7c-103">Avvia un processo, restituendo un ID di esecuzione del processo di cui è possibile eseguire il polling per visualizzarne lo stato</span><span class="sxs-lookup"><span data-stu-id="55a7c-103">Starts a job, returning a job execution id that can be polled to view it's status</span></span>

## <span data-ttu-id="55a7c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="55a7c-104">SYNTAX</span></span>

### <span data-ttu-id="55a7c-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="55a7c-105">DefaultSet (Default)</span></span>
```
Start-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> [-Wait] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="55a7c-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="55a7c-106">ObjectSet</span></span>
```
Start-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobModel> [-Wait] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55a7c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="55a7c-107">ResourceIdSet</span></span>
```
Start-AzSqlElasticJob [-ParentResourceId] <String> [-Wait] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55a7c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="55a7c-108">DESCRIPTION</span></span>
<span data-ttu-id="55a7c-109">Il cmdlet Start-AzSqlElasticJob avvia un processo che restituisce una nuova esecuzione del processo</span><span class="sxs-lookup"><span data-stu-id="55a7c-109">The Start-AzSqlElasticJob cmdlet starts a job returning a new job execution</span></span>

## <span data-ttu-id="55a7c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="55a7c-110">EXAMPLES</span></span>

### <span data-ttu-id="55a7c-111">Esempio 1-avvia un processo restituendo una nuova esecuzione del processo</span><span class="sxs-lookup"><span data-stu-id="55a7c-111">Example 1 - Starts a job returning a new job execution</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Start-AzSqlElasticJob

JobName JobExecutionId                       Lifecycle StartTime EndTime
------- --------------                       --------- --------- -------
job1    b93b3a90-987b-4565-b3d3-5fa1751fa9bc Created
```

<span data-ttu-id="55a7c-112">Avvia un processo restituendo una nuova esecuzione del processo</span><span class="sxs-lookup"><span data-stu-id="55a7c-112">Starts a job returning a new job execution</span></span>

## <span data-ttu-id="55a7c-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="55a7c-113">PARAMETERS</span></span>

### <span data-ttu-id="55a7c-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="55a7c-114">-AgentName</span></span>
<span data-ttu-id="55a7c-115">Nome dell'agente</span><span class="sxs-lookup"><span data-stu-id="55a7c-115">The agent name</span></span>

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

### <span data-ttu-id="55a7c-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55a7c-116">-AsJob</span></span>
<span data-ttu-id="55a7c-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="55a7c-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="55a7c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55a7c-118">-DefaultProfile</span></span>
<span data-ttu-id="55a7c-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="55a7c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55a7c-120">-JobName</span><span class="sxs-lookup"><span data-stu-id="55a7c-120">-JobName</span></span>
<span data-ttu-id="55a7c-121">Il nome del processo</span><span class="sxs-lookup"><span data-stu-id="55a7c-121">The job name</span></span>

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

### <span data-ttu-id="55a7c-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="55a7c-122">-ParentObject</span></span>
<span data-ttu-id="55a7c-123">Oggetto processo</span><span class="sxs-lookup"><span data-stu-id="55a7c-123">The job object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55a7c-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="55a7c-124">-ParentResourceId</span></span>
<span data-ttu-id="55a7c-125">ID risorsa processo</span><span class="sxs-lookup"><span data-stu-id="55a7c-125">The job resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55a7c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55a7c-126">-ResourceGroupName</span></span>
<span data-ttu-id="55a7c-127">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="55a7c-127">The resource group name</span></span>

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

### <span data-ttu-id="55a7c-128">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="55a7c-128">-ServerName</span></span>
<span data-ttu-id="55a7c-129">Nome del server</span><span class="sxs-lookup"><span data-stu-id="55a7c-129">The server name</span></span>

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

### <span data-ttu-id="55a7c-130">-Wait</span><span class="sxs-lookup"><span data-stu-id="55a7c-130">-Wait</span></span>
<span data-ttu-id="55a7c-131">Il contrassegno di attesa per indicare di attendere l'esecuzione del processo</span><span class="sxs-lookup"><span data-stu-id="55a7c-131">The wait flag to indicate to wait until the job's execution is done</span></span>

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

### <span data-ttu-id="55a7c-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="55a7c-132">-Confirm</span></span>
<span data-ttu-id="55a7c-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55a7c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55a7c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55a7c-134">-WhatIf</span></span>
<span data-ttu-id="55a7c-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="55a7c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55a7c-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="55a7c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55a7c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55a7c-137">CommonParameters</span></span>
<span data-ttu-id="55a7c-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55a7c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55a7c-139">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="55a7c-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55a7c-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="55a7c-140">INPUTS</span></span>

### <span data-ttu-id="55a7c-141">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="55a7c-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="55a7c-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="55a7c-142">OUTPUTS</span></span>

### <span data-ttu-id="55a7c-143">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="55a7c-143">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="55a7c-144">Note</span><span class="sxs-lookup"><span data-stu-id="55a7c-144">NOTES</span></span>

## <span data-ttu-id="55a7c-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="55a7c-145">RELATED LINKS</span></span>

## <span data-ttu-id="55a7c-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="55a7c-146">RELATED LINKS</span></span>
