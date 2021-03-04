---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/remove-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
ms.openlocfilehash: 788817dd9ca344501dc25bad48b71b7e24b653d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955182"
---
# <span data-ttu-id="fec72-101">Remove-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="fec72-101">Remove-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="fec72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fec72-102">SYNOPSIS</span></span>
<span data-ttu-id="fec72-103">Rimuove la fase del processo</span><span class="sxs-lookup"><span data-stu-id="fec72-103">Removes the job step</span></span>

## <span data-ttu-id="fec72-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fec72-104">SYNTAX</span></span>

### <span data-ttu-id="fec72-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fec72-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fec72-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="fec72-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fec72-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fec72-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fec72-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fec72-108">DESCRIPTION</span></span>
<span data-ttu-id="fec72-109">Il cmdlet Remove-AzSqlElasticJobStep rimuove un passaggio di processo da un processo</span><span class="sxs-lookup"><span data-stu-id="fec72-109">The Remove-AzSqlElasticJobStep cmdlet removes a job step from a job</span></span>

## <span data-ttu-id="fec72-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fec72-110">EXAMPLES</span></span>

### <span data-ttu-id="fec72-111">Esempio 1: Rimuove un passaggio di processo da un processo</span><span class="sxs-lookup"><span data-stu-id="fec72-111">Example 1: Removes a job step from a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -Name step1
$jobStep | Remove-AzSqlElasticJobStep

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="fec72-112">Rimuove un passaggio di processo da un processo</span><span class="sxs-lookup"><span data-stu-id="fec72-112">Removes a job step from a job</span></span>

### <span data-ttu-id="fec72-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="fec72-113">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Remove-AzSqlElasticJobStep -AgentName agent -JobName job1 -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="fec72-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fec72-114">PARAMETERS</span></span>

### <span data-ttu-id="fec72-115">-AgentName</span><span class="sxs-lookup"><span data-stu-id="fec72-115">-AgentName</span></span>
<span data-ttu-id="fec72-116">Il nome dell'agente</span><span class="sxs-lookup"><span data-stu-id="fec72-116">The agent name</span></span>

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

### <span data-ttu-id="fec72-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fec72-117">-DefaultProfile</span></span>
<span data-ttu-id="fec72-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fec72-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fec72-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fec72-119">-InputObject</span></span>
<span data-ttu-id="fec72-120">Oggetto di input per la fase del processo</span><span class="sxs-lookup"><span data-stu-id="fec72-120">The job step input object</span></span>

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

### <span data-ttu-id="fec72-121">-JobName</span><span class="sxs-lookup"><span data-stu-id="fec72-121">-JobName</span></span>
<span data-ttu-id="fec72-122">Nome del processo</span><span class="sxs-lookup"><span data-stu-id="fec72-122">The job name</span></span>

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

### <span data-ttu-id="fec72-123">-Name</span><span class="sxs-lookup"><span data-stu-id="fec72-123">-Name</span></span>
<span data-ttu-id="fec72-124">Nome della fase del processo</span><span class="sxs-lookup"><span data-stu-id="fec72-124">The job step name</span></span>

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

### <span data-ttu-id="fec72-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fec72-125">-ResourceGroupName</span></span>
<span data-ttu-id="fec72-126">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="fec72-126">The resource group name</span></span>

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

### <span data-ttu-id="fec72-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fec72-127">-ResourceId</span></span>
<span data-ttu-id="fec72-128">ID risorsa fase processo</span><span class="sxs-lookup"><span data-stu-id="fec72-128">The job step resource id</span></span>

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

### <span data-ttu-id="fec72-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fec72-129">-ServerName</span></span>
<span data-ttu-id="fec72-130">Il nome del server</span><span class="sxs-lookup"><span data-stu-id="fec72-130">The server name</span></span>

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

### <span data-ttu-id="fec72-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fec72-131">-Confirm</span></span>
<span data-ttu-id="fec72-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fec72-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fec72-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fec72-133">-WhatIf</span></span>
<span data-ttu-id="fec72-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fec72-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fec72-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fec72-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fec72-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fec72-136">CommonParameters</span></span>
<span data-ttu-id="fec72-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fec72-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fec72-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fec72-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fec72-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="fec72-139">INPUTS</span></span>

### <span data-ttu-id="fec72-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="fec72-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="fec72-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fec72-141">OUTPUTS</span></span>

### <span data-ttu-id="fec72-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="fec72-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="fec72-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="fec72-143">NOTES</span></span>

## <span data-ttu-id="fec72-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fec72-144">RELATED LINKS</span></span>
