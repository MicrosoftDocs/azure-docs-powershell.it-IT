---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BDBA3AA3-DCC6-4C83-84C8-EE6D93BFE1D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaserecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseRecommendedActionState.md
ms.openlocfilehash: 6d634760080e3fb26153b747e733369b20bc8336
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344035"
---
# <span data-ttu-id="30de7-101">Set-AzSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="30de7-101">Set-AzSqlDatabaseRecommendedActionState</span></span>

## <span data-ttu-id="30de7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="30de7-102">SYNOPSIS</span></span>
<span data-ttu-id="30de7-103">Aggiorna lo stato di un'azione consigliata per il database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="30de7-103">Updates the state of an Azure SQL Database recommended action.</span></span>

## <span data-ttu-id="30de7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="30de7-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -DatabaseName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30de7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="30de7-105">DESCRIPTION</span></span>
<span data-ttu-id="30de7-106">Il cmdlet **set-AzSqlDatabaseRecommendedActionState** aggiorna lo stato di un'azione consigliata per il database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="30de7-106">The **Set-AzSqlDatabaseRecommendedActionState** cmdlet updates the state of an Azure SQL Database Recommended Action.</span></span>
<span data-ttu-id="30de7-107">In questo modo è possibile applicare un'azione consigliata, ripristinata o scartata in base al nuovo stato.</span><span class="sxs-lookup"><span data-stu-id="30de7-107">This allows a recommended action to be applied, reverted or discarded based on the new state.</span></span>

## <span data-ttu-id="30de7-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="30de7-108">EXAMPLES</span></span>

### <span data-ttu-id="30de7-109">Esempio 1: applicare uno stato di azione consigliato a in sospeso</span><span class="sxs-lookup"><span data-stu-id="30de7-109">Example 1: Apply a recommended action state to pending</span></span>
```
PS C:\>Set-AzSqlDatabaseRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
DatabaseName               : WIRunner

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

<span data-ttu-id="30de7-110">Questo comando Aggiorna lo stato dell'azione consigliata denominata IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893 che appartiene al database denominato WIRunner in sospeso.</span><span class="sxs-lookup"><span data-stu-id="30de7-110">This command updates the state of the recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 that belongs to the database named WIRunner to Pending.</span></span>

## <span data-ttu-id="30de7-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="30de7-111">PARAMETERS</span></span>

### <span data-ttu-id="30de7-112">-Advisorname</span><span class="sxs-lookup"><span data-stu-id="30de7-112">-AdvisorName</span></span>
<span data-ttu-id="30de7-113">Specifica il nome del consulente per cui appartiene l'azione consigliata.</span><span class="sxs-lookup"><span data-stu-id="30de7-113">Specifies the name of the advisor for which this recommended action belongs to.</span></span>

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

### <span data-ttu-id="30de7-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="30de7-114">-DatabaseName</span></span>
<span data-ttu-id="30de7-115">Specifica il nome del database per il quale questo cmdlet imposta lo stato di azione consigliato.</span><span class="sxs-lookup"><span data-stu-id="30de7-115">Specifies the name of the database for which this cmdlet sets the recommended action state.</span></span>

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

### <span data-ttu-id="30de7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30de7-116">-DefaultProfile</span></span>
<span data-ttu-id="30de7-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="30de7-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="30de7-118">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="30de7-118">-RecommendedActionName</span></span>
<span data-ttu-id="30de7-119">Specifica il nome dell'azione consigliata per la quale lo stato viene aggiornato.</span><span class="sxs-lookup"><span data-stu-id="30de7-119">Specifies the name of the recommended action for which state is being updated.</span></span>

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

### <span data-ttu-id="30de7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30de7-120">-ResourceGroupName</span></span>
<span data-ttu-id="30de7-121">Specifica il nome del gruppo di risorse del server che contiene il database.</span><span class="sxs-lookup"><span data-stu-id="30de7-121">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="30de7-122">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="30de7-122">-ServerName</span></span>
<span data-ttu-id="30de7-123">Specifica il nome del server in cui si trova il database.</span><span class="sxs-lookup"><span data-stu-id="30de7-123">Specifies the name of the server the database is in.</span></span>

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

### <span data-ttu-id="30de7-124">-Stato</span><span class="sxs-lookup"><span data-stu-id="30de7-124">-State</span></span>
<span data-ttu-id="30de7-125">Specifica il nuovo valore a cui questo cmdlet aggiorna lo stato di azione consigliato.</span><span class="sxs-lookup"><span data-stu-id="30de7-125">Specifies the new value to which this cmdlet updates the recommended action state.</span></span>
<span data-ttu-id="30de7-126">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="30de7-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="30de7-127">Active</span><span class="sxs-lookup"><span data-stu-id="30de7-127">Active</span></span>
- <span data-ttu-id="30de7-128">In sospeso</span><span class="sxs-lookup"><span data-stu-id="30de7-128">Pending</span></span>
- <span data-ttu-id="30de7-129">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="30de7-129">PendingRevert</span></span>
- <span data-ttu-id="30de7-130">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="30de7-130">RevertCancelled</span></span>
- <span data-ttu-id="30de7-131">Ignorato</span><span class="sxs-lookup"><span data-stu-id="30de7-131">Ignored</span></span>
- <span data-ttu-id="30de7-132">Risolto</span><span class="sxs-lookup"><span data-stu-id="30de7-132">Resolved</span></span>

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

### <span data-ttu-id="30de7-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="30de7-133">-Confirm</span></span>
<span data-ttu-id="30de7-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30de7-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30de7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30de7-135">-WhatIf</span></span>
<span data-ttu-id="30de7-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="30de7-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30de7-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="30de7-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30de7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30de7-138">CommonParameters</span></span>
<span data-ttu-id="30de7-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30de7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30de7-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="30de7-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30de7-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="30de7-141">INPUTS</span></span>

### <span data-ttu-id="30de7-142">System. String</span><span class="sxs-lookup"><span data-stu-id="30de7-142">System.String</span></span>

### <span data-ttu-id="30de7-143">Microsoft. Azure. Commands. SQL. RecommendedAction. cmdlet. RecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="30de7-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span></span>

## <span data-ttu-id="30de7-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="30de7-144">OUTPUTS</span></span>

### <span data-ttu-id="30de7-145">Microsoft. Azure. Commands. SQL. RecommendedAction. Model. AzureSqlDatabaseRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="30de7-145">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlDatabaseRecommendedActionModel</span></span>

## <span data-ttu-id="30de7-146">Note</span><span class="sxs-lookup"><span data-stu-id="30de7-146">NOTES</span></span>
* <span data-ttu-id="30de7-147">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, database, MSSQL, Advisor, RecommendedAction</span><span class="sxs-lookup"><span data-stu-id="30de7-147">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="30de7-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="30de7-148">RELATED LINKS</span></span>

[<span data-ttu-id="30de7-149">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="30de7-149">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="30de7-150">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="30de7-150">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="30de7-151">Get-AzSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="30de7-151">Get-AzSqlServerRecommendedAction</span></span>](./Get-AzSqlServerRecommendedAction.md)

[<span data-ttu-id="30de7-152">Get-AzSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="30de7-152">Get-AzSqlElasticPoolRecommendedAction</span></span>](./Get-AzSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="30de7-153">Set-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="30de7-153">Set-AzSqlElasticPoolRecommendedActionState</span></span>](./Set-AzSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="30de7-154">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="30de7-154">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="30de7-155">Set-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="30de7-155">Set-AzSqlElasticPoolRecommendedActionState</span></span>](./Set-AzSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="30de7-156">Set-AzSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="30de7-156">Set-AzSqlServerRecommendedActionState</span></span>](./Set-AzSqlServerRecommendedActionState.md)

[<span data-ttu-id="30de7-157">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="30de7-157">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="30de7-158">Set-AzSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="30de7-158">Set-AzSqlServerAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlServerAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="30de7-159">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="30de7-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
