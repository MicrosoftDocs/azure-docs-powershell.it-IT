---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/set-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
ms.openlocfilehash: ec2f9174cc0ca8781b56784836a4583b0568128e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981565"
---
# <span data-ttu-id="af4be-101">Set-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="af4be-101">Set-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="af4be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af4be-102">SYNOPSIS</span></span>
<span data-ttu-id="af4be-103">Aggiorna una fase di un processo</span><span class="sxs-lookup"><span data-stu-id="af4be-103">Updates a job step</span></span>

## <span data-ttu-id="af4be-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="af4be-104">SYNTAX</span></span>

### <span data-ttu-id="af4be-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="af4be-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af4be-106">WithRemoveOutput</span><span class="sxs-lookup"><span data-stu-id="af4be-106">WithRemoveOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-RemoveOutput] [-TargetGroupName <String>] [-CredentialName <String>]
 [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="af4be-107">WithAddOutput</span><span class="sxs-lookup"><span data-stu-id="af4be-107">WithAddOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -OutputDatabaseResourceId <String> [-OutputCredentialName <String>]
 [-OutputTableName <String>] [-OutputSchemaName <String>] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="af4be-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="af4be-108">ObjectSet</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-OutputDatabaseObject <AzureSqlDatabaseModel>] [-OutputCredentialName <String>] [-OutputTableName <String>]
 [-OutputSchemaName <String>] [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af4be-109">WithRemoveOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="af4be-109">WithRemoveOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> [-RemoveOutput]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af4be-110">WithAddOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="af4be-110">WithAddOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af4be-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="af4be-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af4be-112">WithRemoveOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="af4be-112">WithRemoveOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-RemoveOutput] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="af4be-113">WithAddOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="af4be-113">WithAddOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af4be-114">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="af4be-114">DESCRIPTION</span></span>
<span data-ttu-id="af4be-115">Il cmdlet Set-AzSqlElasticJobStep aggiorna un passaggio di processo</span><span class="sxs-lookup"><span data-stu-id="af4be-115">The Set-AzSqlElasticJobStep cmdlet updates a job step</span></span>

## <span data-ttu-id="af4be-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="af4be-116">EXAMPLES</span></span>

### <span data-ttu-id="af4be-117">Esempio 1: Aggiorna il gruppo di destinazione di un passaggio di processo per un processo</span><span class="sxs-lookup"><span data-stu-id="af4be-117">Example 1: Updates a job step's target group for a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -TargetGroupName tg2

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg2             cred1                 (43200,10,1,120,2) SELECT 1
```

### <span data-ttu-id="af4be-118">Esempio 2: Aggiorna lo script T-SQL di un passaggio di processo per un processo</span><span class="sxs-lookup"><span data-stu-id="af4be-118">Example 2: Updates a job step's T-SQL script for a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -CommandText "SELECT 2"

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 2
```

<span data-ttu-id="af4be-119">Aggiorna un passaggio di processo da un processo</span><span class="sxs-lookup"><span data-stu-id="af4be-119">Updates a job step from a job</span></span>

### <span data-ttu-id="af4be-120">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="af4be-120">Example 3</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticJobStep -AgentName agent -CommandText 'SELECT 2' -JobName job1 -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="af4be-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af4be-121">PARAMETERS</span></span>

### <span data-ttu-id="af4be-122">-AgentName</span><span class="sxs-lookup"><span data-stu-id="af4be-122">-AgentName</span></span>
<span data-ttu-id="af4be-123">Il nome dell'agente</span><span class="sxs-lookup"><span data-stu-id="af4be-123">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af4be-124">-CommandText</span><span class="sxs-lookup"><span data-stu-id="af4be-124">-CommandText</span></span>
<span data-ttu-id="af4be-125">Testo del comando</span><span class="sxs-lookup"><span data-stu-id="af4be-125">The command text</span></span>

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

### <span data-ttu-id="af4be-126">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="af4be-126">-CredentialName</span></span>
<span data-ttu-id="af4be-127">Nome delle credenziali</span><span class="sxs-lookup"><span data-stu-id="af4be-127">The credential name</span></span>

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

### <span data-ttu-id="af4be-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af4be-128">-DefaultProfile</span></span>
<span data-ttu-id="af4be-129">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="af4be-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af4be-130">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="af4be-130">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="af4be-131">Secondi per l'intervallo di ripetizione iniziale</span><span class="sxs-lookup"><span data-stu-id="af4be-131">The initial retry interval seconds</span></span>

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

### <span data-ttu-id="af4be-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af4be-132">-InputObject</span></span>
<span data-ttu-id="af4be-133">Oggetto fase processo</span><span class="sxs-lookup"><span data-stu-id="af4be-133">The job step object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel
Parameter Sets: ObjectSet, WithRemoveOutputUsingParentObject, WithAddOutputUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af4be-134">-JobName</span><span class="sxs-lookup"><span data-stu-id="af4be-134">-JobName</span></span>
<span data-ttu-id="af4be-135">Nome del processo</span><span class="sxs-lookup"><span data-stu-id="af4be-135">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af4be-136">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="af4be-136">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="af4be-137">Secondi per l'intervallo di ripetizione massimo</span><span class="sxs-lookup"><span data-stu-id="af4be-137">The maximum retry interval seconds</span></span>

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

### <span data-ttu-id="af4be-138">-Name</span><span class="sxs-lookup"><span data-stu-id="af4be-138">-Name</span></span>
<span data-ttu-id="af4be-139">Nome del passaggio</span><span class="sxs-lookup"><span data-stu-id="af4be-139">The step name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af4be-140">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="af4be-140">-OutputCredentialName</span></span>
<span data-ttu-id="af4be-141">Nome delle credenziali di output</span><span class="sxs-lookup"><span data-stu-id="af4be-141">The output credential name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithAddOutput, ObjectSet, WithAddOutputUsingParentObject, ResourceIdSet, WithAddOutputUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af4be-142">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="af4be-142">-OutputDatabaseObject</span></span>
<span data-ttu-id="af4be-143">Oggetto di database di output</span><span class="sxs-lookup"><span data-stu-id="af4be-143">The output database object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af4be-144">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="af4be-144">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="af4be-145">ID risorsa database di output</span><span class="sxs-lookup"><span data-stu-id="af4be-145">The output database resource id</span></span>

```yaml
Type: System.String
Parameter Sets: WithAddOutput, WithAddOutputUsingParentObject, WithAddOutputUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af4be-146">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="af4be-146">-OutputSchemaName</span></span>
<span data-ttu-id="af4be-147">Nome dello schema di output</span><span class="sxs-lookup"><span data-stu-id="af4be-147">The output schema name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithAddOutput, ObjectSet, WithAddOutputUsingParentObject, ResourceIdSet, WithAddOutputUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af4be-148">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="af4be-148">-OutputTableName</span></span>
<span data-ttu-id="af4be-149">Nome della tabella di output</span><span class="sxs-lookup"><span data-stu-id="af4be-149">The output table name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithAddOutput, ObjectSet, WithAddOutputUsingParentObject, ResourceIdSet, WithAddOutputUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af4be-150">-RemoveOutput</span><span class="sxs-lookup"><span data-stu-id="af4be-150">-RemoveOutput</span></span>
<span data-ttu-id="af4be-151">Il contrassegno per indicare se rimuovere l'output</span><span class="sxs-lookup"><span data-stu-id="af4be-151">The flag to indicate whether to remove output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WithRemoveOutput, WithRemoveOutputUsingParentObject, WithRemoveOutputUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af4be-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af4be-152">-ResourceGroupName</span></span>
<span data-ttu-id="af4be-153">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="af4be-153">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af4be-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af4be-154">-ResourceId</span></span>
<span data-ttu-id="af4be-155">ID risorsa fase processo</span><span class="sxs-lookup"><span data-stu-id="af4be-155">The job step resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, WithRemoveOutputUsingParentResourceId, WithAddOutputUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af4be-156">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="af4be-156">-RetryAttempts</span></span>
<span data-ttu-id="af4be-157">I tentativi di attemps</span><span class="sxs-lookup"><span data-stu-id="af4be-157">The retry attemps</span></span>

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

### <span data-ttu-id="af4be-158">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="af4be-158">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="af4be-159">Moltiplicatore backoff per l'intervallo di ripetizione dei tentativi</span><span class="sxs-lookup"><span data-stu-id="af4be-159">The retry interval backoff multiplier</span></span>

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

### <span data-ttu-id="af4be-160">-ServerName</span><span class="sxs-lookup"><span data-stu-id="af4be-160">-ServerName</span></span>
<span data-ttu-id="af4be-161">Il nome del server</span><span class="sxs-lookup"><span data-stu-id="af4be-161">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af4be-162">-StepId</span><span class="sxs-lookup"><span data-stu-id="af4be-162">-StepId</span></span>
<span data-ttu-id="af4be-163">Testo ID passaggio</span><span class="sxs-lookup"><span data-stu-id="af4be-163">The step id text</span></span>

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

### <span data-ttu-id="af4be-164">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="af4be-164">-TargetGroupName</span></span>
<span data-ttu-id="af4be-165">Nome del gruppo di destinazione</span><span class="sxs-lookup"><span data-stu-id="af4be-165">The target group name</span></span>

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

### <span data-ttu-id="af4be-166">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="af4be-166">-TimeoutSeconds</span></span>
<span data-ttu-id="af4be-167">I secondi di timeout</span><span class="sxs-lookup"><span data-stu-id="af4be-167">The timeout seconds</span></span>

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

### <span data-ttu-id="af4be-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="af4be-168">-Confirm</span></span>
<span data-ttu-id="af4be-169">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af4be-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af4be-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af4be-170">-WhatIf</span></span>
<span data-ttu-id="af4be-171">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="af4be-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af4be-172">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="af4be-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af4be-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af4be-173">CommonParameters</span></span>
<span data-ttu-id="af4be-174">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af4be-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af4be-175">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="af4be-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af4be-176">INPUT</span><span class="sxs-lookup"><span data-stu-id="af4be-176">INPUTS</span></span>

### <span data-ttu-id="af4be-177">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="af4be-177">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="af4be-178">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="af4be-178">OUTPUTS</span></span>

### <span data-ttu-id="af4be-179">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="af4be-179">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="af4be-180">NOTE</span><span class="sxs-lookup"><span data-stu-id="af4be-180">NOTES</span></span>

## <span data-ttu-id="af4be-181">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="af4be-181">RELATED LINKS</span></span>
