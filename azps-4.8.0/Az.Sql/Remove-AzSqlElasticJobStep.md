---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
ms.openlocfilehash: b097c95f45700afabd3317a1014641da061d410d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189275"
---
# <span data-ttu-id="c6209-101">Remove-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="c6209-101">Remove-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="c6209-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c6209-102">SYNOPSIS</span></span>
<span data-ttu-id="c6209-103">Rimuove il passaggio del processo</span><span class="sxs-lookup"><span data-stu-id="c6209-103">Removes the job step</span></span>

## <span data-ttu-id="c6209-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c6209-104">SYNTAX</span></span>

### <span data-ttu-id="c6209-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c6209-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c6209-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="c6209-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6209-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c6209-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6209-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c6209-108">DESCRIPTION</span></span>
<span data-ttu-id="c6209-109">Il cmdlet Remove-AzSqlElasticJobStep rimuove un passaggio di processo da un processo</span><span class="sxs-lookup"><span data-stu-id="c6209-109">The Remove-AzSqlElasticJobStep cmdlet removes a job step from a job</span></span>

## <span data-ttu-id="c6209-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c6209-110">EXAMPLES</span></span>

### <span data-ttu-id="c6209-111">Esempio 1: rimuove un passaggio di processo da un processo</span><span class="sxs-lookup"><span data-stu-id="c6209-111">Example 1: Removes a job step from a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -Name step1
$jobStep | Remove-AzSqlElasticJobStep

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="c6209-112">Rimuove un passaggio di processo da un processo</span><span class="sxs-lookup"><span data-stu-id="c6209-112">Removes a job step from a job</span></span>

### <span data-ttu-id="c6209-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c6209-113">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Remove-AzSqlElasticJobStep -AgentName agent -JobName job1 -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="c6209-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c6209-114">PARAMETERS</span></span>

### <span data-ttu-id="c6209-115">-AgentName</span><span class="sxs-lookup"><span data-stu-id="c6209-115">-AgentName</span></span>
<span data-ttu-id="c6209-116">Nome dell'agente</span><span class="sxs-lookup"><span data-stu-id="c6209-116">The agent name</span></span>

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

### <span data-ttu-id="c6209-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6209-117">-DefaultProfile</span></span>
<span data-ttu-id="c6209-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c6209-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6209-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6209-119">-InputObject</span></span>
<span data-ttu-id="c6209-120">Oggetto di input del passaggio del processo</span><span class="sxs-lookup"><span data-stu-id="c6209-120">The job step input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6209-121">-JobName</span><span class="sxs-lookup"><span data-stu-id="c6209-121">-JobName</span></span>
<span data-ttu-id="c6209-122">Il nome del processo</span><span class="sxs-lookup"><span data-stu-id="c6209-122">The job name</span></span>

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

### <span data-ttu-id="c6209-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="c6209-123">-Name</span></span>
<span data-ttu-id="c6209-124">Nome del passaggio del processo</span><span class="sxs-lookup"><span data-stu-id="c6209-124">The job step name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6209-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6209-125">-ResourceGroupName</span></span>
<span data-ttu-id="c6209-126">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="c6209-126">The resource group name</span></span>

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

### <span data-ttu-id="c6209-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6209-127">-ResourceId</span></span>
<span data-ttu-id="c6209-128">ID risorsa passaggio processo</span><span class="sxs-lookup"><span data-stu-id="c6209-128">The job step resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6209-129">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="c6209-129">-ServerName</span></span>
<span data-ttu-id="c6209-130">Nome del server</span><span class="sxs-lookup"><span data-stu-id="c6209-130">The server name</span></span>

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

### <span data-ttu-id="c6209-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c6209-131">-Confirm</span></span>
<span data-ttu-id="c6209-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6209-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6209-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6209-133">-WhatIf</span></span>
<span data-ttu-id="c6209-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c6209-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6209-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c6209-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6209-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6209-136">CommonParameters</span></span>
<span data-ttu-id="c6209-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6209-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6209-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c6209-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6209-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c6209-139">INPUTS</span></span>

### <span data-ttu-id="c6209-140">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="c6209-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="c6209-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c6209-141">OUTPUTS</span></span>

### <span data-ttu-id="c6209-142">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="c6209-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="c6209-143">Note</span><span class="sxs-lookup"><span data-stu-id="c6209-143">NOTES</span></span>

## <span data-ttu-id="c6209-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c6209-144">RELATED LINKS</span></span>
