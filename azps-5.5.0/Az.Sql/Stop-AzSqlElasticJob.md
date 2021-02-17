---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/stop-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
ms.openlocfilehash: ec5ab9706bd459a07c91e7060d3bf6da30f76ed5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207858"
---
# <span data-ttu-id="cdd8b-101">Stop-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="cdd8b-101">Stop-AzSqlElasticJob</span></span>

## <span data-ttu-id="cdd8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cdd8b-102">SYNOPSIS</span></span>
<span data-ttu-id="cdd8b-103">Interrompe un processo dato l'ID di esecuzione del processo</span><span class="sxs-lookup"><span data-stu-id="cdd8b-103">Stops a job given it's job execution id</span></span>

## <span data-ttu-id="cdd8b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cdd8b-104">SYNTAX</span></span>

### <span data-ttu-id="cdd8b-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cdd8b-105">DefaultSet (Default)</span></span>
```
Stop-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cdd8b-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="cdd8b-106">ObjectSet</span></span>
```
Stop-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobExecutionModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdd8b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="cdd8b-107">ResourceIdSet</span></span>
```
Stop-AzSqlElasticJob [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdd8b-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cdd8b-108">DESCRIPTION</span></span>
<span data-ttu-id="cdd8b-109">Il Stop-AzSqlElasticJob cmdlet interrompe un processo con un'esecuzione in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="cdd8b-109">The Stop-AzSqlElasticJob cmdlet stops a job's with a running execution.</span></span>
<span data-ttu-id="cdd8b-110">Restituisce lo stato corrente dell'esecuzione del processo</span><span class="sxs-lookup"><span data-stu-id="cdd8b-110">Returns the current status of the job execution</span></span>

## <span data-ttu-id="cdd8b-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cdd8b-111">EXAMPLES</span></span>

### <span data-ttu-id="cdd8b-112">Esempio 1: Interrompe un processo con l'esecuzione di un processo in esecuzione</span><span class="sxs-lookup"><span data-stu-id="cdd8b-112">Example 1: Stops a job with a running job execution</span></span>
```powershell
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId dab0ebe8-fd52-42e9-bacf-e5f27577039b
$je | Stop-AzSqlElasticJob
JobName JobExecutionId                       Lifecycle                    StartTime            EndTime
------- --------------                       ---------                    ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b WaitingForChildJobExecutions 6/1/2018 10:13:56 PM
```

<span data-ttu-id="cdd8b-113">Interrompe l'esecuzione di un processo in esecuzione e lo restituisce allo stato corrente</span><span class="sxs-lookup"><span data-stu-id="cdd8b-113">Stops a running job execution and returns it's current status</span></span>

### <span data-ttu-id="cdd8b-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="cdd8b-114">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Stop-AzSqlElasticJob -AgentName agent -JobExecutionId 00000000-0000-0000-0000-000000000000 -JobName job1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="cdd8b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cdd8b-115">PARAMETERS</span></span>

### <span data-ttu-id="cdd8b-116">-AgentName</span><span class="sxs-lookup"><span data-stu-id="cdd8b-116">-AgentName</span></span>
<span data-ttu-id="cdd8b-117">Il nome dell'agente</span><span class="sxs-lookup"><span data-stu-id="cdd8b-117">The agent name</span></span>

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

### <span data-ttu-id="cdd8b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdd8b-118">-DefaultProfile</span></span>
<span data-ttu-id="cdd8b-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cdd8b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdd8b-120">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="cdd8b-120">-JobExecutionId</span></span>
<span data-ttu-id="cdd8b-121">ID di esecuzione del processo.</span><span class="sxs-lookup"><span data-stu-id="cdd8b-121">The job execution id.</span></span>

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

### <span data-ttu-id="cdd8b-122">-JobName</span><span class="sxs-lookup"><span data-stu-id="cdd8b-122">-JobName</span></span>
<span data-ttu-id="cdd8b-123">Nome del processo</span><span class="sxs-lookup"><span data-stu-id="cdd8b-123">The job name</span></span>

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

### <span data-ttu-id="cdd8b-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="cdd8b-124">-ParentObject</span></span>
<span data-ttu-id="cdd8b-125">Oggetto di database controllo agente</span><span class="sxs-lookup"><span data-stu-id="cdd8b-125">The Agent Control Database Object</span></span>

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

### <span data-ttu-id="cdd8b-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="cdd8b-126">-ParentResourceId</span></span>
<span data-ttu-id="cdd8b-127">ID risorsa di esecuzione del processo</span><span class="sxs-lookup"><span data-stu-id="cdd8b-127">The job execution resource id</span></span>

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

### <span data-ttu-id="cdd8b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdd8b-128">-ResourceGroupName</span></span>
<span data-ttu-id="cdd8b-129">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="cdd8b-129">The resource group name</span></span>

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

### <span data-ttu-id="cdd8b-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cdd8b-130">-ServerName</span></span>
<span data-ttu-id="cdd8b-131">Il nome del server</span><span class="sxs-lookup"><span data-stu-id="cdd8b-131">The server name</span></span>

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

### <span data-ttu-id="cdd8b-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cdd8b-132">-Confirm</span></span>
<span data-ttu-id="cdd8b-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdd8b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdd8b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdd8b-134">-WhatIf</span></span>
<span data-ttu-id="cdd8b-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cdd8b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdd8b-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cdd8b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdd8b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdd8b-137">CommonParameters</span></span>
<span data-ttu-id="cdd8b-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdd8b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdd8b-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cdd8b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdd8b-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="cdd8b-140">INPUTS</span></span>

### <span data-ttu-id="cdd8b-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="cdd8b-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="cdd8b-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cdd8b-142">OUTPUTS</span></span>

### <span data-ttu-id="cdd8b-143">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="cdd8b-143">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="cdd8b-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="cdd8b-144">NOTES</span></span>

## <span data-ttu-id="cdd8b-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cdd8b-145">RELATED LINKS</span></span>
