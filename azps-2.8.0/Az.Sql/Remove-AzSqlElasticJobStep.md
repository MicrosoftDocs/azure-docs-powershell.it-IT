---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
ms.openlocfilehash: 83d5733144c07c229cf8b5321ee9d3417ab112ad
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857334"
---
# <span data-ttu-id="a9ecf-101">Remove-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="a9ecf-101">Remove-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="a9ecf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a9ecf-102">SYNOPSIS</span></span>
<span data-ttu-id="a9ecf-103">Rimuove il passaggio del processo</span><span class="sxs-lookup"><span data-stu-id="a9ecf-103">Removes the job step</span></span>

## <span data-ttu-id="a9ecf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a9ecf-104">SYNTAX</span></span>

### <span data-ttu-id="a9ecf-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a9ecf-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a9ecf-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="a9ecf-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9ecf-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a9ecf-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9ecf-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9ecf-108">DESCRIPTION</span></span>
<span data-ttu-id="a9ecf-109">Il cmdlet Remove-AzSqlElasticJobStep rimuove un passaggio di processo da un processo</span><span class="sxs-lookup"><span data-stu-id="a9ecf-109">The Remove-AzSqlElasticJobStep cmdlet removes a job step from a job</span></span>

## <span data-ttu-id="a9ecf-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a9ecf-110">EXAMPLES</span></span>

### <span data-ttu-id="a9ecf-111">Esempio 1-rimuove un passaggio di processo da un processo</span><span class="sxs-lookup"><span data-stu-id="a9ecf-111">Example 1 - Removes a job step from a job</span></span>
```
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -Name step1
$jobStep | Remove-AzSqlElasticJobStep

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="a9ecf-112">Rimuove un passaggio di processo da un processo</span><span class="sxs-lookup"><span data-stu-id="a9ecf-112">Removes a job step from a job</span></span>

## <span data-ttu-id="a9ecf-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a9ecf-113">PARAMETERS</span></span>

### <span data-ttu-id="a9ecf-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="a9ecf-114">-AgentName</span></span>
<span data-ttu-id="a9ecf-115">Nome dell'agente</span><span class="sxs-lookup"><span data-stu-id="a9ecf-115">The agent name</span></span>

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

### <span data-ttu-id="a9ecf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9ecf-116">-DefaultProfile</span></span>
<span data-ttu-id="a9ecf-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a9ecf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9ecf-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9ecf-118">-InputObject</span></span>
<span data-ttu-id="a9ecf-119">Oggetto di input del passaggio del processo</span><span class="sxs-lookup"><span data-stu-id="a9ecf-119">The job step input object</span></span>

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

### <span data-ttu-id="a9ecf-120">-JobName</span><span class="sxs-lookup"><span data-stu-id="a9ecf-120">-JobName</span></span>
<span data-ttu-id="a9ecf-121">Il nome del processo</span><span class="sxs-lookup"><span data-stu-id="a9ecf-121">The job name</span></span>

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

### <span data-ttu-id="a9ecf-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="a9ecf-122">-Name</span></span>
<span data-ttu-id="a9ecf-123">Nome del passaggio del processo</span><span class="sxs-lookup"><span data-stu-id="a9ecf-123">The job step name</span></span>

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

### <span data-ttu-id="a9ecf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9ecf-124">-ResourceGroupName</span></span>
<span data-ttu-id="a9ecf-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="a9ecf-125">The resource group name</span></span>

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

### <span data-ttu-id="a9ecf-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9ecf-126">-ResourceId</span></span>
<span data-ttu-id="a9ecf-127">ID risorsa passaggio processo</span><span class="sxs-lookup"><span data-stu-id="a9ecf-127">The job step resource id</span></span>

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

### <span data-ttu-id="a9ecf-128">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="a9ecf-128">-ServerName</span></span>
<span data-ttu-id="a9ecf-129">Nome del server</span><span class="sxs-lookup"><span data-stu-id="a9ecf-129">The server name</span></span>

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

### <span data-ttu-id="a9ecf-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a9ecf-130">-Confirm</span></span>
<span data-ttu-id="a9ecf-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9ecf-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9ecf-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9ecf-132">-WhatIf</span></span>
<span data-ttu-id="a9ecf-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a9ecf-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9ecf-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a9ecf-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9ecf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9ecf-135">CommonParameters</span></span>
<span data-ttu-id="a9ecf-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9ecf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9ecf-137">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9ecf-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9ecf-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a9ecf-138">INPUTS</span></span>

### <span data-ttu-id="a9ecf-139">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="a9ecf-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="a9ecf-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a9ecf-140">OUTPUTS</span></span>

### <span data-ttu-id="a9ecf-141">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="a9ecf-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="a9ecf-142">Note</span><span class="sxs-lookup"><span data-stu-id="a9ecf-142">NOTES</span></span>

## <span data-ttu-id="a9ecf-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a9ecf-143">RELATED LINKS</span></span>
