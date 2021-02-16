---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/start-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlElasticJob.md
ms.openlocfilehash: 5ab6b7e6e77fcfcf470c67bfdd8e300ddc4343ea
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195911"
---
# <span data-ttu-id="7363d-101">Start-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="7363d-101">Start-AzSqlElasticJob</span></span>

## <span data-ttu-id="7363d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7363d-102">SYNOPSIS</span></span>
<span data-ttu-id="7363d-103">Avvia un processo, restituisce un ID di esecuzione del processo che può essere polled per visualizzarne lo stato</span><span class="sxs-lookup"><span data-stu-id="7363d-103">Starts a job, returning a job execution id that can be polled to view it's status</span></span>

## <span data-ttu-id="7363d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7363d-104">SYNTAX</span></span>

### <span data-ttu-id="7363d-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7363d-105">DefaultSet (Default)</span></span>
```
Start-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> [-Wait] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7363d-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="7363d-106">ObjectSet</span></span>
```
Start-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobModel> [-Wait] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7363d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7363d-107">ResourceIdSet</span></span>
```
Start-AzSqlElasticJob [-ParentResourceId] <String> [-Wait] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7363d-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7363d-108">DESCRIPTION</span></span>
<span data-ttu-id="7363d-109">Il cmdlet Start-AzSqlElasticJob avvia un processo che restituisce l'esecuzione di un nuovo processo</span><span class="sxs-lookup"><span data-stu-id="7363d-109">The Start-AzSqlElasticJob cmdlet starts a job returning a new job execution</span></span>

## <span data-ttu-id="7363d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7363d-110">EXAMPLES</span></span>

### <span data-ttu-id="7363d-111">Esempio 1 - Avvia un processo che restituisce un'esecuzione di un nuovo processo</span><span class="sxs-lookup"><span data-stu-id="7363d-111">Example 1 - Starts a job returning a new job execution</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Start-AzSqlElasticJob

JobName JobExecutionId                       Lifecycle StartTime EndTime
------- --------------                       --------- --------- -------
job1    b93b3a90-987b-4565-b3d3-5fa1751fa9bc Created
```

<span data-ttu-id="7363d-112">Avvia un processo che restituisce l'esecuzione di un nuovo processo</span><span class="sxs-lookup"><span data-stu-id="7363d-112">Starts a job returning a new job execution</span></span>

## <span data-ttu-id="7363d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7363d-113">PARAMETERS</span></span>

### <span data-ttu-id="7363d-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="7363d-114">-AgentName</span></span>
<span data-ttu-id="7363d-115">Il nome dell'agente</span><span class="sxs-lookup"><span data-stu-id="7363d-115">The agent name</span></span>

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

### <span data-ttu-id="7363d-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7363d-116">-AsJob</span></span>
<span data-ttu-id="7363d-117">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7363d-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7363d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7363d-118">-DefaultProfile</span></span>
<span data-ttu-id="7363d-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7363d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7363d-120">-JobName</span><span class="sxs-lookup"><span data-stu-id="7363d-120">-JobName</span></span>
<span data-ttu-id="7363d-121">Nome del processo</span><span class="sxs-lookup"><span data-stu-id="7363d-121">The job name</span></span>

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

### <span data-ttu-id="7363d-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7363d-122">-ParentObject</span></span>
<span data-ttu-id="7363d-123">Oggetto processo</span><span class="sxs-lookup"><span data-stu-id="7363d-123">The job object</span></span>

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

### <span data-ttu-id="7363d-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="7363d-124">-ParentResourceId</span></span>
<span data-ttu-id="7363d-125">ID risorsa processo</span><span class="sxs-lookup"><span data-stu-id="7363d-125">The job resource id</span></span>

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

### <span data-ttu-id="7363d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7363d-126">-ResourceGroupName</span></span>
<span data-ttu-id="7363d-127">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="7363d-127">The resource group name</span></span>

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

### <span data-ttu-id="7363d-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7363d-128">-ServerName</span></span>
<span data-ttu-id="7363d-129">Il nome del server</span><span class="sxs-lookup"><span data-stu-id="7363d-129">The server name</span></span>

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

### <span data-ttu-id="7363d-130">-Wait</span><span class="sxs-lookup"><span data-stu-id="7363d-130">-Wait</span></span>
<span data-ttu-id="7363d-131">Il contrassegno di attesa per indicare di aspettare fino al completamento dell'esecuzione del processo</span><span class="sxs-lookup"><span data-stu-id="7363d-131">The wait flag to indicate to wait until the job's execution is done</span></span>

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

### <span data-ttu-id="7363d-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7363d-132">-Confirm</span></span>
<span data-ttu-id="7363d-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7363d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7363d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7363d-134">-WhatIf</span></span>
<span data-ttu-id="7363d-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7363d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7363d-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7363d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7363d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7363d-137">CommonParameters</span></span>
<span data-ttu-id="7363d-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7363d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7363d-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7363d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7363d-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="7363d-140">INPUTS</span></span>

### <span data-ttu-id="7363d-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="7363d-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="7363d-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7363d-142">OUTPUTS</span></span>

### <span data-ttu-id="7363d-143">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="7363d-143">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="7363d-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="7363d-144">NOTES</span></span>

## <span data-ttu-id="7363d-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7363d-145">RELATED LINKS</span></span>
