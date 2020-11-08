---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
ms.openlocfilehash: 4f6f0471224799e818f9db29e5be5a4c49f9c45e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191836"
---
# <span data-ttu-id="f9c2f-101">Set-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="f9c2f-101">Set-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="f9c2f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f9c2f-102">SYNOPSIS</span></span>
<span data-ttu-id="f9c2f-103">Aggiorna un passaggio di processo</span><span class="sxs-lookup"><span data-stu-id="f9c2f-103">Updates a job step</span></span>

## <span data-ttu-id="f9c2f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f9c2f-104">SYNTAX</span></span>

### <span data-ttu-id="f9c2f-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f9c2f-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9c2f-106">WithRemoveOutput</span><span class="sxs-lookup"><span data-stu-id="f9c2f-106">WithRemoveOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-RemoveOutput] [-TargetGroupName <String>] [-CredentialName <String>]
 [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f9c2f-107">WithAddOutput</span><span class="sxs-lookup"><span data-stu-id="f9c2f-107">WithAddOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -OutputDatabaseResourceId <String> [-OutputCredentialName <String>]
 [-OutputTableName <String>] [-OutputSchemaName <String>] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f9c2f-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="f9c2f-108">ObjectSet</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-OutputDatabaseObject <AzureSqlDatabaseModel>] [-OutputCredentialName <String>] [-OutputTableName <String>]
 [-OutputSchemaName <String>] [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9c2f-109">WithRemoveOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="f9c2f-109">WithRemoveOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> [-RemoveOutput]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9c2f-110">WithAddOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="f9c2f-110">WithAddOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9c2f-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f9c2f-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9c2f-112">WithRemoveOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f9c2f-112">WithRemoveOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-RemoveOutput] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f9c2f-113">WithAddOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f9c2f-113">WithAddOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9c2f-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f9c2f-114">DESCRIPTION</span></span>
<span data-ttu-id="f9c2f-115">Il cmdlet Set-AzSqlElasticJobStep aggiorna un passaggio di processo</span><span class="sxs-lookup"><span data-stu-id="f9c2f-115">The Set-AzSqlElasticJobStep cmdlet updates a job step</span></span>

## <span data-ttu-id="f9c2f-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f9c2f-116">EXAMPLES</span></span>

### <span data-ttu-id="f9c2f-117">Esempio 1: aggiorna il gruppo di destinazione di un passaggio di processo per un processo</span><span class="sxs-lookup"><span data-stu-id="f9c2f-117">Example 1: Updates a job step's target group for a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -TargetGroupName tg2

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg2             cred1                 (43200,10,1,120,2) SELECT 1
```

### <span data-ttu-id="f9c2f-118">Esempio 2: aggiorna lo script T-SQL di un passaggio di processo per un processo</span><span class="sxs-lookup"><span data-stu-id="f9c2f-118">Example 2: Updates a job step's T-SQL script for a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -CommandText "SELECT 2"

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 2
```

<span data-ttu-id="f9c2f-119">Aggiorna un passaggio di processo da un processo</span><span class="sxs-lookup"><span data-stu-id="f9c2f-119">Updates a job step from a job</span></span>

### <span data-ttu-id="f9c2f-120">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="f9c2f-120">Example 3</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticJobStep -AgentName agent -CommandText 'SELECT 2' -JobName job1 -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="f9c2f-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f9c2f-121">PARAMETERS</span></span>

### <span data-ttu-id="f9c2f-122">-AgentName</span><span class="sxs-lookup"><span data-stu-id="f9c2f-122">-AgentName</span></span>
<span data-ttu-id="f9c2f-123">Nome dell'agente</span><span class="sxs-lookup"><span data-stu-id="f9c2f-123">The agent name</span></span>

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

### <span data-ttu-id="f9c2f-124">-CommandText</span><span class="sxs-lookup"><span data-stu-id="f9c2f-124">-CommandText</span></span>
<span data-ttu-id="f9c2f-125">Testo del comando</span><span class="sxs-lookup"><span data-stu-id="f9c2f-125">The command text</span></span>

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

### <span data-ttu-id="f9c2f-126">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="f9c2f-126">-CredentialName</span></span>
<span data-ttu-id="f9c2f-127">Nome della credenziale</span><span class="sxs-lookup"><span data-stu-id="f9c2f-127">The credential name</span></span>

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

### <span data-ttu-id="f9c2f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9c2f-128">-DefaultProfile</span></span>
<span data-ttu-id="f9c2f-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f9c2f-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9c2f-130">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="f9c2f-130">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="f9c2f-131">Intervallo di tentativi iniziale secondi</span><span class="sxs-lookup"><span data-stu-id="f9c2f-131">The initial retry interval seconds</span></span>

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

### <span data-ttu-id="f9c2f-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f9c2f-132">-InputObject</span></span>
<span data-ttu-id="f9c2f-133">Oggetto passaggio processo</span><span class="sxs-lookup"><span data-stu-id="f9c2f-133">The job step object</span></span>

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

### <span data-ttu-id="f9c2f-134">-JobName</span><span class="sxs-lookup"><span data-stu-id="f9c2f-134">-JobName</span></span>
<span data-ttu-id="f9c2f-135">Il nome del processo</span><span class="sxs-lookup"><span data-stu-id="f9c2f-135">The job name</span></span>

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

### <span data-ttu-id="f9c2f-136">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="f9c2f-136">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="f9c2f-137">Intervallo massimo di secondi per il tentativo</span><span class="sxs-lookup"><span data-stu-id="f9c2f-137">The maximum retry interval seconds</span></span>

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

### <span data-ttu-id="f9c2f-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="f9c2f-138">-Name</span></span>
<span data-ttu-id="f9c2f-139">Il nome del passaggio</span><span class="sxs-lookup"><span data-stu-id="f9c2f-139">The step name</span></span>

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

### <span data-ttu-id="f9c2f-140">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="f9c2f-140">-OutputCredentialName</span></span>
<span data-ttu-id="f9c2f-141">Nome della credenziale di output</span><span class="sxs-lookup"><span data-stu-id="f9c2f-141">The output credential name</span></span>

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

### <span data-ttu-id="f9c2f-142">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="f9c2f-142">-OutputDatabaseObject</span></span>
<span data-ttu-id="f9c2f-143">Oggetto di database di output</span><span class="sxs-lookup"><span data-stu-id="f9c2f-143">The output database object</span></span>

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

### <span data-ttu-id="f9c2f-144">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="f9c2f-144">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="f9c2f-145">ID risorsa del database di output</span><span class="sxs-lookup"><span data-stu-id="f9c2f-145">The output database resource id</span></span>

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

### <span data-ttu-id="f9c2f-146">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="f9c2f-146">-OutputSchemaName</span></span>
<span data-ttu-id="f9c2f-147">Nome dello schema di output</span><span class="sxs-lookup"><span data-stu-id="f9c2f-147">The output schema name</span></span>

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

### <span data-ttu-id="f9c2f-148">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="f9c2f-148">-OutputTableName</span></span>
<span data-ttu-id="f9c2f-149">Nome della tabella di output</span><span class="sxs-lookup"><span data-stu-id="f9c2f-149">The output table name</span></span>

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

### <span data-ttu-id="f9c2f-150">-RemoveOutput</span><span class="sxs-lookup"><span data-stu-id="f9c2f-150">-RemoveOutput</span></span>
<span data-ttu-id="f9c2f-151">Il contrassegno per indicare se rimuovere l'output</span><span class="sxs-lookup"><span data-stu-id="f9c2f-151">The flag to indicate whether to remove output</span></span>

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

### <span data-ttu-id="f9c2f-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9c2f-152">-ResourceGroupName</span></span>
<span data-ttu-id="f9c2f-153">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="f9c2f-153">The resource group name</span></span>

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

### <span data-ttu-id="f9c2f-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9c2f-154">-ResourceId</span></span>
<span data-ttu-id="f9c2f-155">ID risorsa passaggio processo</span><span class="sxs-lookup"><span data-stu-id="f9c2f-155">The job step resource id</span></span>

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

### <span data-ttu-id="f9c2f-156">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="f9c2f-156">-RetryAttempts</span></span>
<span data-ttu-id="f9c2f-157">Tentativo di tenta</span><span class="sxs-lookup"><span data-stu-id="f9c2f-157">The retry attemps</span></span>

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

### <span data-ttu-id="f9c2f-158">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="f9c2f-158">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="f9c2f-159">Moltiplicatore backoff intervallo tentativi</span><span class="sxs-lookup"><span data-stu-id="f9c2f-159">The retry interval backoff multiplier</span></span>

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

### <span data-ttu-id="f9c2f-160">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="f9c2f-160">-ServerName</span></span>
<span data-ttu-id="f9c2f-161">Nome del server</span><span class="sxs-lookup"><span data-stu-id="f9c2f-161">The server name</span></span>

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

### <span data-ttu-id="f9c2f-162">-StepId</span><span class="sxs-lookup"><span data-stu-id="f9c2f-162">-StepId</span></span>
<span data-ttu-id="f9c2f-163">Testo ID passaggio</span><span class="sxs-lookup"><span data-stu-id="f9c2f-163">The step id text</span></span>

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

### <span data-ttu-id="f9c2f-164">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="f9c2f-164">-TargetGroupName</span></span>
<span data-ttu-id="f9c2f-165">Nome del gruppo di destinazione</span><span class="sxs-lookup"><span data-stu-id="f9c2f-165">The target group name</span></span>

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

### <span data-ttu-id="f9c2f-166">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="f9c2f-166">-TimeoutSeconds</span></span>
<span data-ttu-id="f9c2f-167">Secondi di timeout</span><span class="sxs-lookup"><span data-stu-id="f9c2f-167">The timeout seconds</span></span>

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

### <span data-ttu-id="f9c2f-168">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f9c2f-168">-Confirm</span></span>
<span data-ttu-id="f9c2f-169">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9c2f-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9c2f-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9c2f-170">-WhatIf</span></span>
<span data-ttu-id="f9c2f-171">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f9c2f-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9c2f-172">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f9c2f-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9c2f-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9c2f-173">CommonParameters</span></span>
<span data-ttu-id="f9c2f-174">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9c2f-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9c2f-175">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f9c2f-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9c2f-176">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f9c2f-176">INPUTS</span></span>

### <span data-ttu-id="f9c2f-177">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="f9c2f-177">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="f9c2f-178">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f9c2f-178">OUTPUTS</span></span>

### <span data-ttu-id="f9c2f-179">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="f9c2f-179">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="f9c2f-180">Note</span><span class="sxs-lookup"><span data-stu-id="f9c2f-180">NOTES</span></span>

## <span data-ttu-id="f9c2f-181">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f9c2f-181">RELATED LINKS</span></span>
