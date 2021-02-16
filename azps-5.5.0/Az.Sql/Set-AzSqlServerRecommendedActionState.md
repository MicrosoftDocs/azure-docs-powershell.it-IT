---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 26EC220C-5123-4CEF-8CC6-5FFD08F33481
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverrecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerRecommendedActionState.md
ms.openlocfilehash: 78366f70db7bd586e1e35566f167c7cae2c2dbf0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197615"
---
# <span data-ttu-id="ffafc-101">Set-AzSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="ffafc-101">Set-AzSqlServerRecommendedActionState</span></span>

## <span data-ttu-id="ffafc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffafc-102">SYNOPSIS</span></span>
<span data-ttu-id="ffafc-103">Aggiorna lo stato di un'azione consigliata SQL Server azure.</span><span class="sxs-lookup"><span data-stu-id="ffafc-103">Updates the state of an Azure SQL Server recommended action.</span></span>

## <span data-ttu-id="ffafc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ffafc-104">SYNTAX</span></span>

```
Set-AzSqlServerRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffafc-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ffafc-105">DESCRIPTION</span></span>
<span data-ttu-id="ffafc-106">Il cmdlet **Set-AzSqlServerRecommendedActionState** aggiorna lo stato di un'azione SQL Server azure consigliata.</span><span class="sxs-lookup"><span data-stu-id="ffafc-106">The **Set-AzSqlServerRecommendedActionState** cmdlet updates state of an Azure SQL Server recommended action.</span></span>
<span data-ttu-id="ffafc-107">Questo cmdlet applica, ripristina o elimina l'azione consigliata in base al nuovo stato.</span><span class="sxs-lookup"><span data-stu-id="ffafc-107">This cmdlet applies, reverts, or discards the recommended action based on the new state.</span></span>

## <span data-ttu-id="ffafc-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ffafc-108">EXAMPLES</span></span>

### <span data-ttu-id="ffafc-109">Esempio1: Aggiornare lo stato dell'azione consigliata specificata in In sospeso</span><span class="sxs-lookup"><span data-stu-id="ffafc-109">Example1: Update the state of the specified recommended action to Pending</span></span>
```
PS C:\>Set-AzSqlServerRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
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

<span data-ttu-id="ffafc-110">Aggiorna lo stato dell'azione consigliata del server denominata "IR_ \[ test_schema \] _ \[ test_table_0.0361551 _6C7AE8CC9C87E7FD5893" in \] "In sospeso"</span><span class="sxs-lookup"><span data-stu-id="ffafc-110">Updates state of server recommended action named "IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893" to "Pending"</span></span>

## <span data-ttu-id="ffafc-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ffafc-111">PARAMETERS</span></span>

### <span data-ttu-id="ffafc-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="ffafc-112">-AdvisorName</span></span>
<span data-ttu-id="ffafc-113">Specifica il nome dell'consulente che contiene l'azione consigliata.</span><span class="sxs-lookup"><span data-stu-id="ffafc-113">Specifies the name of the advisor that contains the recommended action.</span></span>

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

### <span data-ttu-id="ffafc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffafc-114">-DefaultProfile</span></span>
<span data-ttu-id="ffafc-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="ffafc-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ffafc-116">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="ffafc-116">-RecommendedActionName</span></span>
<span data-ttu-id="ffafc-117">Specifica il nome dell'azione consigliata per cui questo cmdlet aggiorna lo stato.</span><span class="sxs-lookup"><span data-stu-id="ffafc-117">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

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

### <span data-ttu-id="ffafc-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffafc-118">-ResourceGroupName</span></span>
<span data-ttu-id="ffafc-119">Specifica il nome del gruppo di risorse del server.</span><span class="sxs-lookup"><span data-stu-id="ffafc-119">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="ffafc-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ffafc-120">-ServerName</span></span>
<span data-ttu-id="ffafc-121">Specifica il nome del server.</span><span class="sxs-lookup"><span data-stu-id="ffafc-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="ffafc-122">-State</span><span class="sxs-lookup"><span data-stu-id="ffafc-122">-State</span></span>
<span data-ttu-id="ffafc-123">Specifica il nuovo valore a cui questo cmdlet aggiorna lo stato dell'azione consigliata.</span><span class="sxs-lookup"><span data-stu-id="ffafc-123">Specifies the new value to which this cmdlet updates the recommended action state.</span></span>
<span data-ttu-id="ffafc-124">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="ffafc-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ffafc-125">Attivo</span><span class="sxs-lookup"><span data-stu-id="ffafc-125">Active</span></span>
- <span data-ttu-id="ffafc-126">In sospeso</span><span class="sxs-lookup"><span data-stu-id="ffafc-126">Pending</span></span>
- <span data-ttu-id="ffafc-127">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="ffafc-127">PendingRevert</span></span>
- <span data-ttu-id="ffafc-128">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="ffafc-128">RevertCancelled</span></span>
- <span data-ttu-id="ffafc-129">Ignorato</span><span class="sxs-lookup"><span data-stu-id="ffafc-129">Ignored</span></span>
- <span data-ttu-id="ffafc-130">Risolto</span><span class="sxs-lookup"><span data-stu-id="ffafc-130">Resolved</span></span>

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

### <span data-ttu-id="ffafc-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ffafc-131">-Confirm</span></span>
<span data-ttu-id="ffafc-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffafc-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffafc-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffafc-133">-WhatIf</span></span>
<span data-ttu-id="ffafc-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ffafc-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffafc-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ffafc-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffafc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffafc-136">CommonParameters</span></span>
<span data-ttu-id="ffafc-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffafc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffafc-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ffafc-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffafc-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="ffafc-139">INPUTS</span></span>

### <span data-ttu-id="ffafc-140">System.String</span><span class="sxs-lookup"><span data-stu-id="ffafc-140">System.String</span></span>

### <span data-ttu-id="ffafc-141">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="ffafc-141">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span></span>

## <span data-ttu-id="ffafc-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ffafc-142">OUTPUTS</span></span>

### <span data-ttu-id="ffafc-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlServerRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="ffafc-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlServerRecommendedActionModel</span></span>

## <span data-ttu-id="ffafc-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="ffafc-144">NOTES</span></span>
* <span data-ttu-id="ffafc-145">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, sql, server, mssql, advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="ffafc-145">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="ffafc-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ffafc-146">RELATED LINKS</span></span>

[<span data-ttu-id="ffafc-147">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="ffafc-147">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="ffafc-148">Get-AzSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="ffafc-148">Get-AzSqlServerRecommendedAction</span></span>](./Get-AzSqlServerRecommendedAction.md)

[<span data-ttu-id="ffafc-149">Set-AzSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="ffafc-149">Set-AzSqlDatabaseRecommendedActionState</span></span>](./Set-AzSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="ffafc-150">Set-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="ffafc-150">Set-AzSqlElasticPoolRecommendedActionState</span></span>](./Set-AzSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="ffafc-151">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="ffafc-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
