---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/stop-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
ms.openlocfilehash: ec5ab9706bd459a07c91e7060d3bf6da30f76ed5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031006"
---
# <span data-ttu-id="72d19-101">Stop-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="72d19-101">Stop-AzSqlElasticJob</span></span>

## <span data-ttu-id="72d19-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="72d19-102">SYNOPSIS</span></span>
<span data-ttu-id="72d19-103">Arresta un processo in base all'ID esecuzione del processo</span><span class="sxs-lookup"><span data-stu-id="72d19-103">Stops a job given it's job execution id</span></span>

## <span data-ttu-id="72d19-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="72d19-104">SYNTAX</span></span>

### <span data-ttu-id="72d19-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="72d19-105">DefaultSet (Default)</span></span>
```
Stop-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="72d19-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="72d19-106">ObjectSet</span></span>
```
Stop-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobExecutionModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72d19-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="72d19-107">ResourceIdSet</span></span>
```
Stop-AzSqlElasticJob [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72d19-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="72d19-108">DESCRIPTION</span></span>
<span data-ttu-id="72d19-109">Il cmdlet Stop-AzSqlElasticJob arresta un processo con un'esecuzione in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="72d19-109">The Stop-AzSqlElasticJob cmdlet stops a job's with a running execution.</span></span>
<span data-ttu-id="72d19-110">Restituisce lo stato corrente dell'esecuzione del processo</span><span class="sxs-lookup"><span data-stu-id="72d19-110">Returns the current status of the job execution</span></span>

## <span data-ttu-id="72d19-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="72d19-111">EXAMPLES</span></span>

### <span data-ttu-id="72d19-112">Esempio 1: arresta un processo con l'esecuzione di un processo in esecuzione</span><span class="sxs-lookup"><span data-stu-id="72d19-112">Example 1: Stops a job with a running job execution</span></span>
```powershell
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId dab0ebe8-fd52-42e9-bacf-e5f27577039b
$je | Stop-AzSqlElasticJob
JobName JobExecutionId                       Lifecycle                    StartTime            EndTime
------- --------------                       ---------                    ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b WaitingForChildJobExecutions 6/1/2018 10:13:56 PM
```

<span data-ttu-id="72d19-113">Interrompe l'esecuzione di un processo in esecuzione e restituisce lo stato corrente</span><span class="sxs-lookup"><span data-stu-id="72d19-113">Stops a running job execution and returns it's current status</span></span>

### <span data-ttu-id="72d19-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="72d19-114">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Stop-AzSqlElasticJob -AgentName agent -JobExecutionId 00000000-0000-0000-0000-000000000000 -JobName job1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="72d19-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="72d19-115">PARAMETERS</span></span>

### <span data-ttu-id="72d19-116">-AgentName</span><span class="sxs-lookup"><span data-stu-id="72d19-116">-AgentName</span></span>
<span data-ttu-id="72d19-117">Nome dell'agente</span><span class="sxs-lookup"><span data-stu-id="72d19-117">The agent name</span></span>

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

### <span data-ttu-id="72d19-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72d19-118">-DefaultProfile</span></span>
<span data-ttu-id="72d19-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="72d19-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72d19-120">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="72d19-120">-JobExecutionId</span></span>
<span data-ttu-id="72d19-121">ID esecuzione processo.</span><span class="sxs-lookup"><span data-stu-id="72d19-121">The job execution id.</span></span>

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

### <span data-ttu-id="72d19-122">-JobName</span><span class="sxs-lookup"><span data-stu-id="72d19-122">-JobName</span></span>
<span data-ttu-id="72d19-123">Il nome del processo</span><span class="sxs-lookup"><span data-stu-id="72d19-123">The job name</span></span>

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

### <span data-ttu-id="72d19-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="72d19-124">-ParentObject</span></span>
<span data-ttu-id="72d19-125">Oggetto database controllo agente</span><span class="sxs-lookup"><span data-stu-id="72d19-125">The Agent Control Database Object</span></span>

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

### <span data-ttu-id="72d19-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="72d19-126">-ParentResourceId</span></span>
<span data-ttu-id="72d19-127">ID risorsa di esecuzione processo</span><span class="sxs-lookup"><span data-stu-id="72d19-127">The job execution resource id</span></span>

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

### <span data-ttu-id="72d19-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72d19-128">-ResourceGroupName</span></span>
<span data-ttu-id="72d19-129">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="72d19-129">The resource group name</span></span>

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

### <span data-ttu-id="72d19-130">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="72d19-130">-ServerName</span></span>
<span data-ttu-id="72d19-131">Nome del server</span><span class="sxs-lookup"><span data-stu-id="72d19-131">The server name</span></span>

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

### <span data-ttu-id="72d19-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="72d19-132">-Confirm</span></span>
<span data-ttu-id="72d19-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72d19-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72d19-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72d19-134">-WhatIf</span></span>
<span data-ttu-id="72d19-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="72d19-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72d19-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="72d19-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72d19-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72d19-137">CommonParameters</span></span>
<span data-ttu-id="72d19-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72d19-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72d19-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72d19-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72d19-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="72d19-140">INPUTS</span></span>

### <span data-ttu-id="72d19-141">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="72d19-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="72d19-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="72d19-142">OUTPUTS</span></span>

### <span data-ttu-id="72d19-143">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="72d19-143">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="72d19-144">Note</span><span class="sxs-lookup"><span data-stu-id="72d19-144">NOTES</span></span>

## <span data-ttu-id="72d19-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="72d19-145">RELATED LINKS</span></span>
