---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/add-azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
ms.openlocfilehash: 41314cb2a65912e2973e91b27036fc099d2cbca6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961534"
---
# <span data-ttu-id="fb0b6-101">Add-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="fb0b6-101">Add-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="fb0b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb0b6-102">SYNOPSIS</span></span>
<span data-ttu-id="fb0b6-103">Aggiunge un passaggio di processo a un processo</span><span class="sxs-lookup"><span data-stu-id="fb0b6-103">Adds a job step to a job</span></span>

## <span data-ttu-id="fb0b6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fb0b6-104">SYNTAX</span></span>

### <span data-ttu-id="fb0b6-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fb0b6-105">DefaultSet (Default)</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String> -Name <String>
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb0b6-106">WithOutputDb</span><span class="sxs-lookup"><span data-stu-id="fb0b6-106">WithOutputDb</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String> -OutputTableName <String>
 -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fb0b6-107">WithOutputDbId</span><span class="sxs-lookup"><span data-stu-id="fb0b6-107">WithOutputDbId</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseResourceId <String> -OutputCredentialName <String> -OutputTableName <String> -Name <String>
 [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fb0b6-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="fb0b6-108">ObjectSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fb0b6-109">WithOutputDbUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="fb0b6-109">WithOutputDbUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb0b6-110">WithOutputDbIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="fb0b6-110">WithOutputDbIdUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseResourceId <String>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb0b6-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fb0b6-111">ResourceIdSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fb0b6-112">WithOutputDbUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="fb0b6-112">WithOutputDbUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb0b6-113">WithOutputDbIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="fb0b6-113">WithOutputDbIdUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseResourceId <String> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb0b6-114">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fb0b6-114">DESCRIPTION</span></span>
<span data-ttu-id="fb0b6-115">Il cmdlet Add-AzSqlElasticJobStep aggiunge un passaggio di processo a un processo</span><span class="sxs-lookup"><span data-stu-id="fb0b6-115">The Add-AzSqlElasticJobStep cmdlet adds a job step to a job</span></span>

## <span data-ttu-id="fb0b6-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fb0b6-116">EXAMPLES</span></span>

### <span data-ttu-id="fb0b6-117">Esempio 1: Aggiunge un passaggio a un processo</span><span class="sxs-lookup"><span data-stu-id="fb0b6-117">Example 1: Adds a step to a job</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -Name job1
$job | Add-AzSqlElasticJobStep -Name step1 -TargetGroupName tg1 -CredentialName cred1 -CommandText "SELECT 1"

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="fb0b6-118">Aggiunge un passaggio di processo a un processo</span><span class="sxs-lookup"><span data-stu-id="fb0b6-118">Adds a job step to a job</span></span>

## <span data-ttu-id="fb0b6-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb0b6-119">PARAMETERS</span></span>

### <span data-ttu-id="fb0b6-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="fb0b6-120">-AgentName</span></span>
<span data-ttu-id="fb0b6-121">Il nome dell'agente</span><span class="sxs-lookup"><span data-stu-id="fb0b6-121">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb0b6-122">-CommandText</span><span class="sxs-lookup"><span data-stu-id="fb0b6-122">-CommandText</span></span>
<span data-ttu-id="fb0b6-123">Testo del comando</span><span class="sxs-lookup"><span data-stu-id="fb0b6-123">The command text</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb0b6-124">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="fb0b6-124">-CredentialName</span></span>
<span data-ttu-id="fb0b6-125">Nome delle credenziali</span><span class="sxs-lookup"><span data-stu-id="fb0b6-125">The credential name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb0b6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb0b6-126">-DefaultProfile</span></span>
<span data-ttu-id="fb0b6-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fb0b6-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb0b6-128">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="fb0b6-128">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="fb0b6-129">Secondi per l'intervallo di ripetizione iniziale</span><span class="sxs-lookup"><span data-stu-id="fb0b6-129">The initial retry interval seconds</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb0b6-130">-JobName</span><span class="sxs-lookup"><span data-stu-id="fb0b6-130">-JobName</span></span>
<span data-ttu-id="fb0b6-131">Nome del processo</span><span class="sxs-lookup"><span data-stu-id="fb0b6-131">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb0b6-132">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="fb0b6-132">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="fb0b6-133">Secondi per l'intervallo di ripetizione massimo</span><span class="sxs-lookup"><span data-stu-id="fb0b6-133">The maximum retry interval seconds</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb0b6-134">-Name</span><span class="sxs-lookup"><span data-stu-id="fb0b6-134">-Name</span></span>
<span data-ttu-id="fb0b6-135">Nome della fase del processo</span><span class="sxs-lookup"><span data-stu-id="fb0b6-135">The job step name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb0b6-136">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="fb0b6-136">-OutputCredentialName</span></span>
<span data-ttu-id="fb0b6-137">Nome delle credenziali di output</span><span class="sxs-lookup"><span data-stu-id="fb0b6-137">The output credential name</span></span>

```yaml
Type: System.String
Parameter Sets: WithOutputDb, WithOutputDbId, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject, WithOutputDbUsingParentResourceId, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb0b6-138">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="fb0b6-138">-OutputDatabaseObject</span></span>
<span data-ttu-id="fb0b6-139">Oggetto di database di output</span><span class="sxs-lookup"><span data-stu-id="fb0b6-139">The output database object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: WithOutputDb, WithOutputDbUsingParentObject, WithOutputDbUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb0b6-140">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="fb0b6-140">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="fb0b6-141">ID risorsa database di output</span><span class="sxs-lookup"><span data-stu-id="fb0b6-141">The output database resource id</span></span>

```yaml
Type: System.String
Parameter Sets: WithOutputDbId, WithOutputDbIdUsingParentObject, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb0b6-142">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="fb0b6-142">-OutputSchemaName</span></span>
<span data-ttu-id="fb0b6-143">Nome dello schema di output</span><span class="sxs-lookup"><span data-stu-id="fb0b6-143">The output schema name</span></span>

```yaml
Type: System.String
Parameter Sets: WithOutputDb, WithOutputDbId, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject, WithOutputDbUsingParentResourceId, WithOutputDbIdUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb0b6-144">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="fb0b6-144">-OutputTableName</span></span>
<span data-ttu-id="fb0b6-145">Nome della tabella di output</span><span class="sxs-lookup"><span data-stu-id="fb0b6-145">The output table name</span></span>

```yaml
Type: System.String
Parameter Sets: WithOutputDb, WithOutputDbId, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject, WithOutputDbUsingParentResourceId, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb0b6-146">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="fb0b6-146">-ParentObject</span></span>
<span data-ttu-id="fb0b6-147">Oggetto processo</span><span class="sxs-lookup"><span data-stu-id="fb0b6-147">The job object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb0b6-148">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="fb0b6-148">-ParentResourceId</span></span>
<span data-ttu-id="fb0b6-149">ID risorsa processo</span><span class="sxs-lookup"><span data-stu-id="fb0b6-149">The job resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, WithOutputDbUsingParentResourceId, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb0b6-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb0b6-150">-ResourceGroupName</span></span>
<span data-ttu-id="fb0b6-151">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="fb0b6-151">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb0b6-152">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="fb0b6-152">-RetryAttempts</span></span>
<span data-ttu-id="fb0b6-153">I tentativi riprovati</span><span class="sxs-lookup"><span data-stu-id="fb0b6-153">The retry attempts</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb0b6-154">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="fb0b6-154">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="fb0b6-155">Il moltiplicatore per la ripetizione dell'intervallo di ripetizione</span><span class="sxs-lookup"><span data-stu-id="fb0b6-155">The retry interval back off multiplier</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb0b6-156">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fb0b6-156">-ServerName</span></span>
<span data-ttu-id="fb0b6-157">Il nome del server</span><span class="sxs-lookup"><span data-stu-id="fb0b6-157">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb0b6-158">-StepId</span><span class="sxs-lookup"><span data-stu-id="fb0b6-158">-StepId</span></span>
<span data-ttu-id="fb0b6-159">ID fase</span><span class="sxs-lookup"><span data-stu-id="fb0b6-159">The step id</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb0b6-160">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="fb0b6-160">-TargetGroupName</span></span>
<span data-ttu-id="fb0b6-161">Nome del gruppo di destinazione</span><span class="sxs-lookup"><span data-stu-id="fb0b6-161">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId, ObjectSet, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject, ResourceIdSet, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WithOutputDbUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb0b6-162">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="fb0b6-162">-TimeoutSeconds</span></span>
<span data-ttu-id="fb0b6-163">Secondi di timeout</span><span class="sxs-lookup"><span data-stu-id="fb0b6-163">The time out seconds</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb0b6-164">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fb0b6-164">-Confirm</span></span>
<span data-ttu-id="fb0b6-165">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb0b6-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb0b6-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb0b6-166">-WhatIf</span></span>
<span data-ttu-id="fb0b6-167">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fb0b6-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb0b6-168">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fb0b6-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb0b6-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb0b6-169">CommonParameters</span></span>
<span data-ttu-id="fb0b6-170">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb0b6-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb0b6-171">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fb0b6-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb0b6-172">INPUT</span><span class="sxs-lookup"><span data-stu-id="fb0b6-172">INPUTS</span></span>

### <span data-ttu-id="fb0b6-173">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="fb0b6-173">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="fb0b6-174">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fb0b6-174">OUTPUTS</span></span>

### <span data-ttu-id="fb0b6-175">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="fb0b6-175">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="fb0b6-176">NOTE</span><span class="sxs-lookup"><span data-stu-id="fb0b6-176">NOTES</span></span>

## <span data-ttu-id="fb0b6-177">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fb0b6-177">RELATED LINKS</span></span>
