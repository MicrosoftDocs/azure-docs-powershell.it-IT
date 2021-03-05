---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: EFDFCE12-F39C-4F52-9962-4601F0C4FD47
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlelasticpoolrecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolRecommendedActionState.md
ms.openlocfilehash: 5ef58938342845b437d714e44a55256892632546
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002957"
---
# <span data-ttu-id="21c2b-101">Set-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="21c2b-101">Set-AzSqlElasticPoolRecommendedActionState</span></span>

## <span data-ttu-id="21c2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21c2b-102">SYNOPSIS</span></span>
<span data-ttu-id="21c2b-103">Aggiorna lo stato di un'azione consigliata SQL pool flessibile di Azure.</span><span class="sxs-lookup"><span data-stu-id="21c2b-103">Updates the state of an Azure SQL Elastic Pool recommended action.</span></span>

## <span data-ttu-id="21c2b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="21c2b-104">SYNTAX</span></span>

```
Set-AzSqlElasticPoolRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -ElasticPoolName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21c2b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="21c2b-105">DESCRIPTION</span></span>
<span data-ttu-id="21c2b-106">Il cmdlet **Set-AzSqlElasticPoolRecommendedActionState** aggiorna lo stato di un'azione consigliata di Azure SQL Pool di elastici.</span><span class="sxs-lookup"><span data-stu-id="21c2b-106">The **Set-AzSqlElasticPoolRecommendedActionState** cmdlet updates state of an Azure SQL Elastic Pool recommended action.</span></span>
<span data-ttu-id="21c2b-107">Questo cmdlet applica un'azione consigliata, annullata o ignorata in base al nuovo stato.</span><span class="sxs-lookup"><span data-stu-id="21c2b-107">This cmdlet applies an recommended action, reverted, or discarded based on the new state.</span></span>

## <span data-ttu-id="21c2b-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="21c2b-108">EXAMPLES</span></span>

### <span data-ttu-id="21c2b-109">Esempio 1: Aggiornare lo stato di un'azione consigliata in In sospeso</span><span class="sxs-lookup"><span data-stu-id="21c2b-109">Example 1: Update the state of a recommended action to Pending</span></span>
```
PS C:\>Set-AzSqlElasticPoolRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
ElasticPoolName            : WIRunnerPool
ResourceGroupName          : WIRunnersProd
ServerName                 : wi-runner-australia-east
AdvisorName                : CreateIndex
RecommendedActionName      : IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893
Details                    : {[indexName, nci_wi_test_table_0.0361551_6C7AE8CC9C87E7FD5893], [indexType, 
                             NONCLUSTERED], [schema, [test_schema]], [table, [test_table_0.0361551]]...} 
ErrorDetails               : Microsoft.Azure.Management.Sql.Models.RecommendedActionErrorInfo
EstimatedImpact            : {ActionDuration, SpaceChange}
ExecuteActionDuration      : PT1M
ExecuteActionInitiatedBy   : User
ExecuteActionInitiatedTime : 4/21/2016 3:24:47 PM
ExecuteActionStartTime     : 4/21/2016 3:24:47 PM
ImplementationDetails      : Microsoft.Azure.Management.Sql.Models.RecommendedActionImplementationInfo
IsArchivedAction           : False
IsExecutableAction         : True
IsRevertableAction         : True
LastRefresh                : 4/21/2016 3:24:47 PM
LinkedObjects              : {}
ObservedImpact             : {CpuUtilization, LogicalReads, LogicalWrites, QueriesWithImprovedPerformance...} 
RecommendationReason       : 
RevertActionDuration       : 
RevertActionInitiatedBy    : 
RevertActionInitiatedTime  : 
RevertActionStartTime      : 
Score                      : 2
State                      : Microsoft.Azure.Management.Sql.Models.RecommendedActionStateInfo
TimeSeries                 : {}
ValidSince                 : 4/21/2016 3:24:47 PM
```

<span data-ttu-id="21c2b-110">Questo comando aggiorna lo stato dell'azione consigliata del pool flessibile IR_ \[ test_schema \] _ \[ test_table_0.0361551 \] _6C7AE8CC9C87E7FD5893 in sospeso.</span><span class="sxs-lookup"><span data-stu-id="21c2b-110">This command updates the state of elastic pool recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 to Pending.</span></span>

## <span data-ttu-id="21c2b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21c2b-111">PARAMETERS</span></span>

### <span data-ttu-id="21c2b-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="21c2b-112">-AdvisorName</span></span>
<span data-ttu-id="21c2b-113">Specifica il nome dell'consulente a cui appartiene l'azione consigliata.</span><span class="sxs-lookup"><span data-stu-id="21c2b-113">Specifies the name of the advisor for which this recommended action belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21c2b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21c2b-114">-DefaultProfile</span></span>
<span data-ttu-id="21c2b-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="21c2b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="21c2b-116">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="21c2b-116">-ElasticPoolName</span></span>
<span data-ttu-id="21c2b-117">Specifica il nome del pool elastico.</span><span class="sxs-lookup"><span data-stu-id="21c2b-117">Specifies name of the elastic pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21c2b-118">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="21c2b-118">-RecommendedActionName</span></span>
<span data-ttu-id="21c2b-119">Specifica il nome dell'azione consigliata per cui questo cmdlet aggiorna lo stato.</span><span class="sxs-lookup"><span data-stu-id="21c2b-119">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21c2b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21c2b-120">-ResourceGroupName</span></span>
<span data-ttu-id="21c2b-121">Specifica il nome del gruppo di risorse del server che contiene questo pool flessibile.</span><span class="sxs-lookup"><span data-stu-id="21c2b-121">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21c2b-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="21c2b-122">-ServerName</span></span>
<span data-ttu-id="21c2b-123">Specifica il nome del server in cui si trova il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="21c2b-123">Specifies the name of the server the elastic pool is in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21c2b-124">-State</span><span class="sxs-lookup"><span data-stu-id="21c2b-124">-State</span></span>
<span data-ttu-id="21c2b-125">Specifica il valore a cui questo cmdlet aggiorna lo stato dell'azione consigliata.</span><span class="sxs-lookup"><span data-stu-id="21c2b-125">Specifies the value to which this cmdlet updates the recommended action state.</span></span>
<span data-ttu-id="21c2b-126">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="21c2b-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="21c2b-127">Attivo</span><span class="sxs-lookup"><span data-stu-id="21c2b-127">Active</span></span>
- <span data-ttu-id="21c2b-128">In sospeso</span><span class="sxs-lookup"><span data-stu-id="21c2b-128">Pending</span></span>
- <span data-ttu-id="21c2b-129">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="21c2b-129">PendingRevert</span></span>
- <span data-ttu-id="21c2b-130">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="21c2b-130">RevertCancelled</span></span>
- <span data-ttu-id="21c2b-131">Ignorato</span><span class="sxs-lookup"><span data-stu-id="21c2b-131">Ignored</span></span>
- <span data-ttu-id="21c2b-132">Risolto</span><span class="sxs-lookup"><span data-stu-id="21c2b-132">Resolved</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState
Parameter Sets: (All)
Aliases:
Accepted values: Active, Pending, PendingRevert, RevertCancelled, Ignored, Resolved

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21c2b-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="21c2b-133">-Confirm</span></span>
<span data-ttu-id="21c2b-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21c2b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21c2b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21c2b-135">-WhatIf</span></span>
<span data-ttu-id="21c2b-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="21c2b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21c2b-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="21c2b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21c2b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21c2b-138">CommonParameters</span></span>
<span data-ttu-id="21c2b-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21c2b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21c2b-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="21c2b-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21c2b-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="21c2b-141">INPUTS</span></span>

### <span data-ttu-id="21c2b-142">System.String</span><span class="sxs-lookup"><span data-stu-id="21c2b-142">System.String</span></span>

### <span data-ttu-id="21c2b-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="21c2b-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span></span>

## <span data-ttu-id="21c2b-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="21c2b-144">OUTPUTS</span></span>

### <span data-ttu-id="21c2b-145">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlElasticPoolRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="21c2b-145">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlElasticPoolRecommendedActionModel</span></span>

## <span data-ttu-id="21c2b-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="21c2b-146">NOTES</span></span>
* <span data-ttu-id="21c2b-147">Parole chiave: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="21c2b-147">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="21c2b-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="21c2b-148">RELATED LINKS</span></span>

[<span data-ttu-id="21c2b-149">Get-AzSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="21c2b-149">Get-AzSqlElasticPoolRecommendedAction</span></span>](./Get-AzSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="21c2b-150">Set-AzSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="21c2b-150">Set-AzSqlDatabaseRecommendedActionState</span></span>](./Set-AzSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="21c2b-151">Set-AzSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="21c2b-151">Set-AzSqlServerRecommendedActionState</span></span>](./Set-AzSqlServerRecommendedActionState.md)

[<span data-ttu-id="21c2b-152">documentazione SQL database</span><span class="sxs-lookup"><span data-stu-id="21c2b-152">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
