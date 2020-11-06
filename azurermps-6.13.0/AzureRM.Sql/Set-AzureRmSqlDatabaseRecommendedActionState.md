---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BDBA3AA3-DCC6-4C83-84C8-EE6D93BFE1D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabaserecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseRecommendedActionState.md
ms.openlocfilehash: c926078b46fbfb27947e53121e159aafe092da3e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520585"
---
# <span data-ttu-id="292a1-101">Set-AzureRmSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="292a1-101">Set-AzureRmSqlDatabaseRecommendedActionState</span></span>

## <span data-ttu-id="292a1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="292a1-102">SYNOPSIS</span></span>
<span data-ttu-id="292a1-103">Aggiorna lo stato di un'azione consigliata per il database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="292a1-103">Updates the state of an Azure SQL Database recommended action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="292a1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="292a1-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -DatabaseName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="292a1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="292a1-105">DESCRIPTION</span></span>
<span data-ttu-id="292a1-106">Il cmdlet **set-AzureRmSqlDatabaseRecommendedActionState** aggiorna lo stato di un'azione consigliata per il database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="292a1-106">The **Set-AzureRmSqlDatabaseRecommendedActionState** cmdlet updates the state of an Azure SQL Database Recommended Action.</span></span>
<span data-ttu-id="292a1-107">In questo modo è possibile applicare un'azione consigliata, ripristinata o scartata in base al nuovo stato.</span><span class="sxs-lookup"><span data-stu-id="292a1-107">This allows a recommended action to be applied, reverted or discarded based on the new state.</span></span>

## <span data-ttu-id="292a1-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="292a1-108">EXAMPLES</span></span>

### <span data-ttu-id="292a1-109">Esempio 1: applicare uno stato di azione consigliato a in sospeso</span><span class="sxs-lookup"><span data-stu-id="292a1-109">Example 1: Apply a recommended action state to pending</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
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

<span data-ttu-id="292a1-110">Questo comando Aggiorna lo stato dell'azione consigliata denominata IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893 che appartiene al database denominato WIRunner in sospeso.</span><span class="sxs-lookup"><span data-stu-id="292a1-110">This command updates the state of the recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 that belongs to the database named WIRunner to Pending.</span></span>

## <span data-ttu-id="292a1-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="292a1-111">PARAMETERS</span></span>

### <span data-ttu-id="292a1-112">-Advisorname</span><span class="sxs-lookup"><span data-stu-id="292a1-112">-AdvisorName</span></span>
<span data-ttu-id="292a1-113">Specifica il nome del consulente per cui appartiene l'azione consigliata.</span><span class="sxs-lookup"><span data-stu-id="292a1-113">Specifies the name of the advisor for which this recommended action belongs to.</span></span>

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

### <span data-ttu-id="292a1-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="292a1-114">-DatabaseName</span></span>
<span data-ttu-id="292a1-115">Specifica il nome del database per il quale questo cmdlet imposta lo stato di azione consigliato.</span><span class="sxs-lookup"><span data-stu-id="292a1-115">Specifies the name of the database for which this cmdlet sets the recommended action state.</span></span>

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

### <span data-ttu-id="292a1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="292a1-116">-DefaultProfile</span></span>
<span data-ttu-id="292a1-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="292a1-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="292a1-118">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="292a1-118">-RecommendedActionName</span></span>
<span data-ttu-id="292a1-119">Specifica il nome dell'azione consigliata per la quale lo stato viene aggiornato.</span><span class="sxs-lookup"><span data-stu-id="292a1-119">Specifies the name of the recommended action for which state is being updated.</span></span>

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

### <span data-ttu-id="292a1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="292a1-120">-ResourceGroupName</span></span>
<span data-ttu-id="292a1-121">Specifica il nome del gruppo di risorse del server che contiene il database.</span><span class="sxs-lookup"><span data-stu-id="292a1-121">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="292a1-122">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="292a1-122">-ServerName</span></span>
<span data-ttu-id="292a1-123">Specifica il nome del server in cui si trova il database.</span><span class="sxs-lookup"><span data-stu-id="292a1-123">Specifies the name of the server the database is in.</span></span>

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

### <span data-ttu-id="292a1-124">-Stato</span><span class="sxs-lookup"><span data-stu-id="292a1-124">-State</span></span>
<span data-ttu-id="292a1-125">Specifica il nuovo valore a cui questo cmdlet aggiorna lo stato di azione consigliato.</span><span class="sxs-lookup"><span data-stu-id="292a1-125">Specifies the new value to which this cmdlet updates the recommended action state.</span></span>
<span data-ttu-id="292a1-126">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="292a1-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="292a1-127">Active</span><span class="sxs-lookup"><span data-stu-id="292a1-127">Active</span></span>
- <span data-ttu-id="292a1-128">In sospeso</span><span class="sxs-lookup"><span data-stu-id="292a1-128">Pending</span></span>
- <span data-ttu-id="292a1-129">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="292a1-129">PendingRevert</span></span>
- <span data-ttu-id="292a1-130">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="292a1-130">RevertCancelled</span></span>
- <span data-ttu-id="292a1-131">Ignorato</span><span class="sxs-lookup"><span data-stu-id="292a1-131">Ignored</span></span>
- <span data-ttu-id="292a1-132">Risolto</span><span class="sxs-lookup"><span data-stu-id="292a1-132">Resolved</span></span>

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

### <span data-ttu-id="292a1-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="292a1-133">-Confirm</span></span>
<span data-ttu-id="292a1-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="292a1-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="292a1-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="292a1-135">-WhatIf</span></span>
<span data-ttu-id="292a1-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="292a1-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="292a1-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="292a1-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="292a1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="292a1-138">CommonParameters</span></span>
<span data-ttu-id="292a1-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="292a1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="292a1-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="292a1-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="292a1-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="292a1-141">INPUTS</span></span>

### <span data-ttu-id="292a1-142">System. String</span><span class="sxs-lookup"><span data-stu-id="292a1-142">System.String</span></span>

### <span data-ttu-id="292a1-143">Microsoft. Azure. Commands. SQL. RecommendedAction. cmdlet. RecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="292a1-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span></span>

## <span data-ttu-id="292a1-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="292a1-144">OUTPUTS</span></span>

### <span data-ttu-id="292a1-145">Microsoft. Azure. Commands. SQL. RecommendedAction. Model. AzureSqlDatabaseRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="292a1-145">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlDatabaseRecommendedActionModel</span></span>

## <span data-ttu-id="292a1-146">Note</span><span class="sxs-lookup"><span data-stu-id="292a1-146">NOTES</span></span>
* <span data-ttu-id="292a1-147">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, database, MSSQL, Advisor, RecommendedAction</span><span class="sxs-lookup"><span data-stu-id="292a1-147">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="292a1-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="292a1-148">RELATED LINKS</span></span>

[<span data-ttu-id="292a1-149">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="292a1-149">Get-AzureRmSqlServerAdvisor</span></span>](./Get-AzureRmSqlServerAdvisor.md)

[<span data-ttu-id="292a1-150">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="292a1-150">Get-AzureRmSqlElasticPoolAdvisor</span></span>](./Get-AzureRmSqlElasticPoolAdvisor.md)

[<span data-ttu-id="292a1-151">Get-AzureRmSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="292a1-151">Get-AzureRmSqlServerRecommendedAction</span></span>](./Get-AzureRmSqlServerRecommendedAction.md)

[<span data-ttu-id="292a1-152">Get-AzureRmSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="292a1-152">Get-AzureRmSqlElasticPoolRecommendedAction</span></span>](./Get-AzureRmSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="292a1-153">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="292a1-153">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>](./Set-AzureRmSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="292a1-154">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="292a1-154">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="292a1-155">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="292a1-155">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>](./Set-AzureRmSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="292a1-156">Set-AzureRmSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="292a1-156">Set-AzureRmSqlServerRecommendedActionState</span></span>](./Set-AzureRmSqlServerRecommendedActionState.md)

[<span data-ttu-id="292a1-157">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="292a1-157">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="292a1-158">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="292a1-158">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span></span>](./Set-AzureRmSqlServerAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="292a1-159">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="292a1-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
