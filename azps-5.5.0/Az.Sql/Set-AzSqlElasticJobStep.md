---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
ms.openlocfilehash: 4f6f0471224799e818f9db29e5be5a4c49f9c45e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176759"
---
# <span data-ttu-id="60f9b-101">Set-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="60f9b-101">Set-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="60f9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60f9b-102">SYNOPSIS</span></span>
<span data-ttu-id="60f9b-103">Aggiorna un passaggio di processo</span><span class="sxs-lookup"><span data-stu-id="60f9b-103">Updates a job step</span></span>

## <span data-ttu-id="60f9b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="60f9b-104">SYNTAX</span></span>

### <span data-ttu-id="60f9b-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="60f9b-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60f9b-106">WithRemoveOutput</span><span class="sxs-lookup"><span data-stu-id="60f9b-106">WithRemoveOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-RemoveOutput] [-TargetGroupName <String>] [-CredentialName <String>]
 [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="60f9b-107">WithAddOutput</span><span class="sxs-lookup"><span data-stu-id="60f9b-107">WithAddOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -OutputDatabaseResourceId <String> [-OutputCredentialName <String>]
 [-OutputTableName <String>] [-OutputSchemaName <String>] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="60f9b-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="60f9b-108">ObjectSet</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-OutputDatabaseObject <AzureSqlDatabaseModel>] [-OutputCredentialName <String>] [-OutputTableName <String>]
 [-OutputSchemaName <String>] [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60f9b-109">WithRemoveOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="60f9b-109">WithRemoveOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> [-RemoveOutput]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60f9b-110">WithAddOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="60f9b-110">WithAddOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60f9b-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="60f9b-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60f9b-112">WithRemoveOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="60f9b-112">WithRemoveOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-RemoveOutput] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="60f9b-113">WithAddOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="60f9b-113">WithAddOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60f9b-114">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="60f9b-114">DESCRIPTION</span></span>
<span data-ttu-id="60f9b-115">Il cmdlet Set-AzSqlElasticJobStep aggiorna un passaggio di processo</span><span class="sxs-lookup"><span data-stu-id="60f9b-115">The Set-AzSqlElasticJobStep cmdlet updates a job step</span></span>

## <span data-ttu-id="60f9b-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="60f9b-116">EXAMPLES</span></span>

### <span data-ttu-id="60f9b-117">Esempio 1: Aggiorna il gruppo di destinazione di un passaggio di processo per un processo</span><span class="sxs-lookup"><span data-stu-id="60f9b-117">Example 1: Updates a job step's target group for a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -TargetGroupName tg2

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg2             cred1                 (43200,10,1,120,2) SELECT 1
```

### <span data-ttu-id="60f9b-118">Esempio 2: Aggiorna lo script T-SQL di un passaggio di processo per un processo</span><span class="sxs-lookup"><span data-stu-id="60f9b-118">Example 2: Updates a job step's T-SQL script for a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -CommandText "SELECT 2"

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 2
```

<span data-ttu-id="60f9b-119">Aggiorna un passaggio di processo da un processo</span><span class="sxs-lookup"><span data-stu-id="60f9b-119">Updates a job step from a job</span></span>

### <span data-ttu-id="60f9b-120">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="60f9b-120">Example 3</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticJobStep -AgentName agent -CommandText 'SELECT 2' -JobName job1 -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="60f9b-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60f9b-121">PARAMETERS</span></span>

### <span data-ttu-id="60f9b-122">-AgentName</span><span class="sxs-lookup"><span data-stu-id="60f9b-122">-AgentName</span></span>
<span data-ttu-id="60f9b-123">Il nome dell'agente</span><span class="sxs-lookup"><span data-stu-id="60f9b-123">The agent name</span></span>

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

### <span data-ttu-id="60f9b-124">-CommandText</span><span class="sxs-lookup"><span data-stu-id="60f9b-124">-CommandText</span></span>
<span data-ttu-id="60f9b-125">Testo del comando</span><span class="sxs-lookup"><span data-stu-id="60f9b-125">The command text</span></span>

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

### <span data-ttu-id="60f9b-126">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="60f9b-126">-CredentialName</span></span>
<span data-ttu-id="60f9b-127">Nome delle credenziali</span><span class="sxs-lookup"><span data-stu-id="60f9b-127">The credential name</span></span>

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

### <span data-ttu-id="60f9b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60f9b-128">-DefaultProfile</span></span>
<span data-ttu-id="60f9b-129">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="60f9b-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60f9b-130">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="60f9b-130">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="60f9b-131">Secondi per l'intervallo di ripetizione iniziale</span><span class="sxs-lookup"><span data-stu-id="60f9b-131">The initial retry interval seconds</span></span>

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

### <span data-ttu-id="60f9b-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60f9b-132">-InputObject</span></span>
<span data-ttu-id="60f9b-133">Oggetto fase processo</span><span class="sxs-lookup"><span data-stu-id="60f9b-133">The job step object</span></span>

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

### <span data-ttu-id="60f9b-134">-JobName</span><span class="sxs-lookup"><span data-stu-id="60f9b-134">-JobName</span></span>
<span data-ttu-id="60f9b-135">Nome del processo</span><span class="sxs-lookup"><span data-stu-id="60f9b-135">The job name</span></span>

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

### <span data-ttu-id="60f9b-136">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="60f9b-136">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="60f9b-137">Secondi per l'intervallo di ripetizione massimo</span><span class="sxs-lookup"><span data-stu-id="60f9b-137">The maximum retry interval seconds</span></span>

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

### <span data-ttu-id="60f9b-138">-Name</span><span class="sxs-lookup"><span data-stu-id="60f9b-138">-Name</span></span>
<span data-ttu-id="60f9b-139">Nome del passaggio</span><span class="sxs-lookup"><span data-stu-id="60f9b-139">The step name</span></span>

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

### <span data-ttu-id="60f9b-140">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="60f9b-140">-OutputCredentialName</span></span>
<span data-ttu-id="60f9b-141">Nome delle credenziali di output</span><span class="sxs-lookup"><span data-stu-id="60f9b-141">The output credential name</span></span>

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

### <span data-ttu-id="60f9b-142">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="60f9b-142">-OutputDatabaseObject</span></span>
<span data-ttu-id="60f9b-143">Oggetto di database di output</span><span class="sxs-lookup"><span data-stu-id="60f9b-143">The output database object</span></span>

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

### <span data-ttu-id="60f9b-144">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="60f9b-144">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="60f9b-145">ID risorsa database di output</span><span class="sxs-lookup"><span data-stu-id="60f9b-145">The output database resource id</span></span>

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

### <span data-ttu-id="60f9b-146">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="60f9b-146">-OutputSchemaName</span></span>
<span data-ttu-id="60f9b-147">Nome dello schema di output</span><span class="sxs-lookup"><span data-stu-id="60f9b-147">The output schema name</span></span>

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

### <span data-ttu-id="60f9b-148">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="60f9b-148">-OutputTableName</span></span>
<span data-ttu-id="60f9b-149">Nome della tabella di output</span><span class="sxs-lookup"><span data-stu-id="60f9b-149">The output table name</span></span>

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

### <span data-ttu-id="60f9b-150">-RemoveOutput</span><span class="sxs-lookup"><span data-stu-id="60f9b-150">-RemoveOutput</span></span>
<span data-ttu-id="60f9b-151">Il contrassegno per indicare se rimuovere l'output</span><span class="sxs-lookup"><span data-stu-id="60f9b-151">The flag to indicate whether to remove output</span></span>

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

### <span data-ttu-id="60f9b-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60f9b-152">-ResourceGroupName</span></span>
<span data-ttu-id="60f9b-153">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="60f9b-153">The resource group name</span></span>

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

### <span data-ttu-id="60f9b-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="60f9b-154">-ResourceId</span></span>
<span data-ttu-id="60f9b-155">ID risorsa fase processo</span><span class="sxs-lookup"><span data-stu-id="60f9b-155">The job step resource id</span></span>

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

### <span data-ttu-id="60f9b-156">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="60f9b-156">-RetryAttempts</span></span>
<span data-ttu-id="60f9b-157">Il tentativo di continuare</span><span class="sxs-lookup"><span data-stu-id="60f9b-157">The retry attemps</span></span>

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

### <span data-ttu-id="60f9b-158">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="60f9b-158">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="60f9b-159">Moltiplicatore backoff per l'intervallo di ripetizione dei tentativi</span><span class="sxs-lookup"><span data-stu-id="60f9b-159">The retry interval backoff multiplier</span></span>

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

### <span data-ttu-id="60f9b-160">-ServerName</span><span class="sxs-lookup"><span data-stu-id="60f9b-160">-ServerName</span></span>
<span data-ttu-id="60f9b-161">Il nome del server</span><span class="sxs-lookup"><span data-stu-id="60f9b-161">The server name</span></span>

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

### <span data-ttu-id="60f9b-162">-StepId</span><span class="sxs-lookup"><span data-stu-id="60f9b-162">-StepId</span></span>
<span data-ttu-id="60f9b-163">Testo ID passaggio</span><span class="sxs-lookup"><span data-stu-id="60f9b-163">The step id text</span></span>

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

### <span data-ttu-id="60f9b-164">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="60f9b-164">-TargetGroupName</span></span>
<span data-ttu-id="60f9b-165">Nome del gruppo di destinazione</span><span class="sxs-lookup"><span data-stu-id="60f9b-165">The target group name</span></span>

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

### <span data-ttu-id="60f9b-166">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="60f9b-166">-TimeoutSeconds</span></span>
<span data-ttu-id="60f9b-167">I secondi di timeout</span><span class="sxs-lookup"><span data-stu-id="60f9b-167">The timeout seconds</span></span>

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

### <span data-ttu-id="60f9b-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="60f9b-168">-Confirm</span></span>
<span data-ttu-id="60f9b-169">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60f9b-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60f9b-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60f9b-170">-WhatIf</span></span>
<span data-ttu-id="60f9b-171">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60f9b-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60f9b-172">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60f9b-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60f9b-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60f9b-173">CommonParameters</span></span>
<span data-ttu-id="60f9b-174">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60f9b-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60f9b-175">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="60f9b-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60f9b-176">INPUT</span><span class="sxs-lookup"><span data-stu-id="60f9b-176">INPUTS</span></span>

### <span data-ttu-id="60f9b-177">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="60f9b-177">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="60f9b-178">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="60f9b-178">OUTPUTS</span></span>

### <span data-ttu-id="60f9b-179">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="60f9b-179">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="60f9b-180">NOTE</span><span class="sxs-lookup"><span data-stu-id="60f9b-180">NOTES</span></span>

## <span data-ttu-id="60f9b-181">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="60f9b-181">RELATED LINKS</span></span>
