---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
ms.openlocfilehash: 79b26156ae99bfcdd94671649b403b495377af30
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93856049"
---
# <span data-ttu-id="68d36-101">Add-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="68d36-101">Add-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="68d36-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="68d36-102">SYNOPSIS</span></span>
<span data-ttu-id="68d36-103">Aggiunge un passaggio di processo a un processo</span><span class="sxs-lookup"><span data-stu-id="68d36-103">Adds a job step to a job</span></span>

## <span data-ttu-id="68d36-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="68d36-104">SYNTAX</span></span>

### <span data-ttu-id="68d36-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="68d36-105">DefaultSet (Default)</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String> -Name <String>
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68d36-106">WithOutputDb</span><span class="sxs-lookup"><span data-stu-id="68d36-106">WithOutputDb</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String> -OutputTableName <String>
 -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="68d36-107">WithOutputDbId</span><span class="sxs-lookup"><span data-stu-id="68d36-107">WithOutputDbId</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseResourceId <String> -OutputCredentialName <String> -OutputTableName <String> -Name <String>
 [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="68d36-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="68d36-108">ObjectSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="68d36-109">WithOutputDbUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="68d36-109">WithOutputDbUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68d36-110">WithOutputDbIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="68d36-110">WithOutputDbIdUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseResourceId <String>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68d36-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="68d36-111">ResourceIdSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="68d36-112">WithOutputDbUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="68d36-112">WithOutputDbUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68d36-113">WithOutputDbIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="68d36-113">WithOutputDbIdUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseResourceId <String> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68d36-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="68d36-114">DESCRIPTION</span></span>
<span data-ttu-id="68d36-115">Il cmdlet Add-AzSqlElasticJobStep aggiunge un passaggio di processo a un processo</span><span class="sxs-lookup"><span data-stu-id="68d36-115">The Add-AzSqlElasticJobStep cmdlet adds a job step to a job</span></span>

## <span data-ttu-id="68d36-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="68d36-116">EXAMPLES</span></span>

### <span data-ttu-id="68d36-117">Esempio 1: aggiunge un passaggio a un processo</span><span class="sxs-lookup"><span data-stu-id="68d36-117">Example 1 - Adds a step to a job</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -Name job1
$job | Add-AzSqlElasticJobStep -Name step1 -TargetGroupName tg1 -CredentialName cred1 -CommandText "SELECT 1"

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="68d36-118">Aggiunge un passaggio di processo a un processo</span><span class="sxs-lookup"><span data-stu-id="68d36-118">Adds a job step to a job</span></span>

## <span data-ttu-id="68d36-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="68d36-119">PARAMETERS</span></span>

### <span data-ttu-id="68d36-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="68d36-120">-AgentName</span></span>
<span data-ttu-id="68d36-121">Nome dell'agente</span><span class="sxs-lookup"><span data-stu-id="68d36-121">The agent name</span></span>

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

### <span data-ttu-id="68d36-122">-CommandText</span><span class="sxs-lookup"><span data-stu-id="68d36-122">-CommandText</span></span>
<span data-ttu-id="68d36-123">Testo del comando</span><span class="sxs-lookup"><span data-stu-id="68d36-123">The command text</span></span>

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

### <span data-ttu-id="68d36-124">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="68d36-124">-CredentialName</span></span>
<span data-ttu-id="68d36-125">Nome della credenziale</span><span class="sxs-lookup"><span data-stu-id="68d36-125">The credential name</span></span>

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

### <span data-ttu-id="68d36-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68d36-126">-DefaultProfile</span></span>
<span data-ttu-id="68d36-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="68d36-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68d36-128">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="68d36-128">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="68d36-129">Intervallo di tentativi iniziale secondi</span><span class="sxs-lookup"><span data-stu-id="68d36-129">The initial retry interval seconds</span></span>

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

### <span data-ttu-id="68d36-130">-JobName</span><span class="sxs-lookup"><span data-stu-id="68d36-130">-JobName</span></span>
<span data-ttu-id="68d36-131">Il nome del processo</span><span class="sxs-lookup"><span data-stu-id="68d36-131">The job name</span></span>

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

### <span data-ttu-id="68d36-132">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="68d36-132">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="68d36-133">Intervallo massimo di secondi per il tentativo</span><span class="sxs-lookup"><span data-stu-id="68d36-133">The maximum retry interval seconds</span></span>

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

### <span data-ttu-id="68d36-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="68d36-134">-Name</span></span>
<span data-ttu-id="68d36-135">Nome del passaggio del processo</span><span class="sxs-lookup"><span data-stu-id="68d36-135">The job step name</span></span>

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

### <span data-ttu-id="68d36-136">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="68d36-136">-OutputCredentialName</span></span>
<span data-ttu-id="68d36-137">Nome della credenziale di output</span><span class="sxs-lookup"><span data-stu-id="68d36-137">The output credential name</span></span>

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

### <span data-ttu-id="68d36-138">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="68d36-138">-OutputDatabaseObject</span></span>
<span data-ttu-id="68d36-139">Oggetto di database di output</span><span class="sxs-lookup"><span data-stu-id="68d36-139">The output database object</span></span>

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

### <span data-ttu-id="68d36-140">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="68d36-140">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="68d36-141">ID risorsa del database di output</span><span class="sxs-lookup"><span data-stu-id="68d36-141">The output database resource id</span></span>

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

### <span data-ttu-id="68d36-142">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="68d36-142">-OutputSchemaName</span></span>
<span data-ttu-id="68d36-143">Nome dello schema di output</span><span class="sxs-lookup"><span data-stu-id="68d36-143">The output schema name</span></span>

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

### <span data-ttu-id="68d36-144">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="68d36-144">-OutputTableName</span></span>
<span data-ttu-id="68d36-145">Nome della tabella di output</span><span class="sxs-lookup"><span data-stu-id="68d36-145">The output table name</span></span>

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

### <span data-ttu-id="68d36-146">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="68d36-146">-ParentObject</span></span>
<span data-ttu-id="68d36-147">Oggetto processo</span><span class="sxs-lookup"><span data-stu-id="68d36-147">The job object</span></span>

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

### <span data-ttu-id="68d36-148">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="68d36-148">-ParentResourceId</span></span>
<span data-ttu-id="68d36-149">ID risorsa processo</span><span class="sxs-lookup"><span data-stu-id="68d36-149">The job resource id</span></span>

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

### <span data-ttu-id="68d36-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68d36-150">-ResourceGroupName</span></span>
<span data-ttu-id="68d36-151">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="68d36-151">The resource group name</span></span>

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

### <span data-ttu-id="68d36-152">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="68d36-152">-RetryAttempts</span></span>
<span data-ttu-id="68d36-153">Tentativi di tentativo</span><span class="sxs-lookup"><span data-stu-id="68d36-153">The retry attempts</span></span>

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

### <span data-ttu-id="68d36-154">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="68d36-154">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="68d36-155">Intervallo di tentativi di back off moltiplicatore</span><span class="sxs-lookup"><span data-stu-id="68d36-155">The retry interval back off multiplier</span></span>

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

### <span data-ttu-id="68d36-156">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="68d36-156">-ServerName</span></span>
<span data-ttu-id="68d36-157">Nome del server</span><span class="sxs-lookup"><span data-stu-id="68d36-157">The server name</span></span>

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

### <span data-ttu-id="68d36-158">-StepId</span><span class="sxs-lookup"><span data-stu-id="68d36-158">-StepId</span></span>
<span data-ttu-id="68d36-159">ID passaggio</span><span class="sxs-lookup"><span data-stu-id="68d36-159">The step id</span></span>

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

### <span data-ttu-id="68d36-160">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="68d36-160">-TargetGroupName</span></span>
<span data-ttu-id="68d36-161">Nome del gruppo di destinazione</span><span class="sxs-lookup"><span data-stu-id="68d36-161">The target group name</span></span>

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

### <span data-ttu-id="68d36-162">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="68d36-162">-TimeoutSeconds</span></span>
<span data-ttu-id="68d36-163">I secondi di timeout</span><span class="sxs-lookup"><span data-stu-id="68d36-163">The time out seconds</span></span>

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

### <span data-ttu-id="68d36-164">-Confermare</span><span class="sxs-lookup"><span data-stu-id="68d36-164">-Confirm</span></span>
<span data-ttu-id="68d36-165">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68d36-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68d36-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68d36-166">-WhatIf</span></span>
<span data-ttu-id="68d36-167">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="68d36-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68d36-168">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="68d36-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68d36-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68d36-169">CommonParameters</span></span>
<span data-ttu-id="68d36-170">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68d36-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68d36-171">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68d36-171">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68d36-172">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="68d36-172">INPUTS</span></span>

### <span data-ttu-id="68d36-173">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="68d36-173">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="68d36-174">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="68d36-174">OUTPUTS</span></span>

### <span data-ttu-id="68d36-175">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="68d36-175">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="68d36-176">Note</span><span class="sxs-lookup"><span data-stu-id="68d36-176">NOTES</span></span>

## <span data-ttu-id="68d36-177">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="68d36-177">RELATED LINKS</span></span>
