---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: EFDFCE12-F39C-4F52-9962-4601F0C4FD47
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpoolrecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolRecommendedActionState.md
ms.openlocfilehash: 64a8884075bcc849deffd4083c95ec1849859a68
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176750"
---
# <span data-ttu-id="05995-101">Set-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="05995-101">Set-AzSqlElasticPoolRecommendedActionState</span></span>

## <span data-ttu-id="05995-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05995-102">SYNOPSIS</span></span>
<span data-ttu-id="05995-103">Aggiorna lo stato di un'azione consigliata SQL pool flessibile di Azure.</span><span class="sxs-lookup"><span data-stu-id="05995-103">Updates the state of an Azure SQL Elastic Pool recommended action.</span></span>

## <span data-ttu-id="05995-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="05995-104">SYNTAX</span></span>

```
Set-AzSqlElasticPoolRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -ElasticPoolName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05995-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="05995-105">DESCRIPTION</span></span>
<span data-ttu-id="05995-106">Il cmdlet **Set-AzSqlElasticPoolRecommendedActionState** aggiorna lo stato di un'azione consigliata di Azure SQL Pool di elastici.</span><span class="sxs-lookup"><span data-stu-id="05995-106">The **Set-AzSqlElasticPoolRecommendedActionState** cmdlet updates state of an Azure SQL Elastic Pool recommended action.</span></span>
<span data-ttu-id="05995-107">Questo cmdlet applica un'azione consigliata, annullata o rimossa in base al nuovo stato.</span><span class="sxs-lookup"><span data-stu-id="05995-107">This cmdlet applies an recommended action, reverted, or discarded based on the new state.</span></span>

## <span data-ttu-id="05995-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="05995-108">EXAMPLES</span></span>

### <span data-ttu-id="05995-109">Esempio 1: Aggiornare lo stato di un'azione consigliata in In sospeso</span><span class="sxs-lookup"><span data-stu-id="05995-109">Example 1: Update the state of a recommended action to Pending</span></span>
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

<span data-ttu-id="05995-110">Questo comando aggiorna lo stato dell'azione consigliata del pool flessibile IR_ \[ test_schema \] _ \[ test_table_0.0361551 \] _6C7AE8CC9C87E7FD5893 in sospeso.</span><span class="sxs-lookup"><span data-stu-id="05995-110">This command updates the state of elastic pool recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 to Pending.</span></span>

## <span data-ttu-id="05995-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05995-111">PARAMETERS</span></span>

### <span data-ttu-id="05995-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="05995-112">-AdvisorName</span></span>
<span data-ttu-id="05995-113">Specifica il nome dell'consulente a cui appartiene l'azione consigliata.</span><span class="sxs-lookup"><span data-stu-id="05995-113">Specifies the name of the advisor for which this recommended action belongs to.</span></span>

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

### <span data-ttu-id="05995-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05995-114">-DefaultProfile</span></span>
<span data-ttu-id="05995-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="05995-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="05995-116">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="05995-116">-ElasticPoolName</span></span>
<span data-ttu-id="05995-117">Specifica il nome del pool elastico.</span><span class="sxs-lookup"><span data-stu-id="05995-117">Specifies name of the elastic pool.</span></span>

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

### <span data-ttu-id="05995-118">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="05995-118">-RecommendedActionName</span></span>
<span data-ttu-id="05995-119">Specifica il nome dell'azione consigliata per cui questo cmdlet aggiorna lo stato.</span><span class="sxs-lookup"><span data-stu-id="05995-119">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

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

### <span data-ttu-id="05995-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05995-120">-ResourceGroupName</span></span>
<span data-ttu-id="05995-121">Specifica il nome del gruppo di risorse del server che contiene questo pool flessibile.</span><span class="sxs-lookup"><span data-stu-id="05995-121">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="05995-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="05995-122">-ServerName</span></span>
<span data-ttu-id="05995-123">Specifica il nome del server in cui si trova il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="05995-123">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="05995-124">-State</span><span class="sxs-lookup"><span data-stu-id="05995-124">-State</span></span>
<span data-ttu-id="05995-125">Specifica il valore a cui questo cmdlet aggiorna lo stato dell'azione consigliata.</span><span class="sxs-lookup"><span data-stu-id="05995-125">Specifies the value to which this cmdlet updates the recommended action state.</span></span>
<span data-ttu-id="05995-126">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="05995-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="05995-127">Attivo</span><span class="sxs-lookup"><span data-stu-id="05995-127">Active</span></span>
- <span data-ttu-id="05995-128">In sospeso</span><span class="sxs-lookup"><span data-stu-id="05995-128">Pending</span></span>
- <span data-ttu-id="05995-129">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="05995-129">PendingRevert</span></span>
- <span data-ttu-id="05995-130">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="05995-130">RevertCancelled</span></span>
- <span data-ttu-id="05995-131">Ignorato</span><span class="sxs-lookup"><span data-stu-id="05995-131">Ignored</span></span>
- <span data-ttu-id="05995-132">Risolto</span><span class="sxs-lookup"><span data-stu-id="05995-132">Resolved</span></span>

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

### <span data-ttu-id="05995-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="05995-133">-Confirm</span></span>
<span data-ttu-id="05995-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05995-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05995-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05995-135">-WhatIf</span></span>
<span data-ttu-id="05995-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="05995-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05995-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="05995-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05995-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05995-138">CommonParameters</span></span>
<span data-ttu-id="05995-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05995-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05995-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="05995-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05995-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="05995-141">INPUTS</span></span>

### <span data-ttu-id="05995-142">System.String</span><span class="sxs-lookup"><span data-stu-id="05995-142">System.String</span></span>

### <span data-ttu-id="05995-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="05995-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span></span>

## <span data-ttu-id="05995-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="05995-144">OUTPUTS</span></span>

### <span data-ttu-id="05995-145">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlElasticPoolRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="05995-145">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlElasticPoolRecommendedActionModel</span></span>

## <span data-ttu-id="05995-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="05995-146">NOTES</span></span>
* <span data-ttu-id="05995-147">Parole chiave: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="05995-147">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="05995-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="05995-148">RELATED LINKS</span></span>

[<span data-ttu-id="05995-149">Get-AzSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="05995-149">Get-AzSqlElasticPoolRecommendedAction</span></span>](./Get-AzSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="05995-150">Set-AzSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="05995-150">Set-AzSqlDatabaseRecommendedActionState</span></span>](./Set-AzSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="05995-151">Set-AzSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="05995-151">Set-AzSqlServerRecommendedActionState</span></span>](./Set-AzSqlServerRecommendedActionState.md)

[<span data-ttu-id="05995-152">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="05995-152">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
