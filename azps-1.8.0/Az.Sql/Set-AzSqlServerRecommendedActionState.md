---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 26EC220C-5123-4CEF-8CC6-5FFD08F33481
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverrecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerRecommendedActionState.md
ms.openlocfilehash: b8be70708ddb504825f151eedbf7b3d0502d2781
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676709"
---
# <span data-ttu-id="0b08a-101">Set-AzSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="0b08a-101">Set-AzSqlServerRecommendedActionState</span></span>

## <span data-ttu-id="0b08a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0b08a-102">SYNOPSIS</span></span>
<span data-ttu-id="0b08a-103">Aggiorna lo stato di un'azione consigliata di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0b08a-103">Updates the state of an Azure SQL Server recommended action.</span></span>

## <span data-ttu-id="0b08a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0b08a-104">SYNTAX</span></span>

```
Set-AzSqlServerRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b08a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b08a-105">DESCRIPTION</span></span>
<span data-ttu-id="0b08a-106">Il cmdlet **set-AzSqlServerRecommendedActionState** aggiorna lo stato di un'azione consigliata di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0b08a-106">The **Set-AzSqlServerRecommendedActionState** cmdlet updates state of an Azure SQL Server recommended action.</span></span>
<span data-ttu-id="0b08a-107">Questo cmdlet applica, ripristina o Elimina l'azione consigliata in base al nuovo stato.</span><span class="sxs-lookup"><span data-stu-id="0b08a-107">This cmdlet applies, reverts, or discards the recommended action based on the new state.</span></span>

## <span data-ttu-id="0b08a-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0b08a-108">EXAMPLES</span></span>

### <span data-ttu-id="0b08a-109">Esempio1: aggiornare lo stato dell'azione consigliata specificata in sospeso</span><span class="sxs-lookup"><span data-stu-id="0b08a-109">Example1: Update the state of the specified recommended action to Pending</span></span>
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

<span data-ttu-id="0b08a-110">Stato aggiornamenti dell'azione consigliata del server denominata "IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893" a "in sospeso"</span><span class="sxs-lookup"><span data-stu-id="0b08a-110">Updates state of server recommended action named "IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893" to "Pending"</span></span>

## <span data-ttu-id="0b08a-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0b08a-111">PARAMETERS</span></span>

### <span data-ttu-id="0b08a-112">-Advisorname</span><span class="sxs-lookup"><span data-stu-id="0b08a-112">-AdvisorName</span></span>
<span data-ttu-id="0b08a-113">Specifica il nome del consulente che contiene l'azione consigliata.</span><span class="sxs-lookup"><span data-stu-id="0b08a-113">Specifies the name of the advisor that contains the recommended action.</span></span>

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

### <span data-ttu-id="0b08a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b08a-114">-DefaultProfile</span></span>
<span data-ttu-id="0b08a-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0b08a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b08a-116">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="0b08a-116">-RecommendedActionName</span></span>
<span data-ttu-id="0b08a-117">Specifica il nome dell'azione consigliata per cui questo cmdlet aggiorna lo stato.</span><span class="sxs-lookup"><span data-stu-id="0b08a-117">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

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

### <span data-ttu-id="0b08a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b08a-118">-ResourceGroupName</span></span>
<span data-ttu-id="0b08a-119">Specifica il nome del gruppo di risorse del server.</span><span class="sxs-lookup"><span data-stu-id="0b08a-119">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="0b08a-120">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="0b08a-120">-ServerName</span></span>
<span data-ttu-id="0b08a-121">Specifica il nome del server.</span><span class="sxs-lookup"><span data-stu-id="0b08a-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="0b08a-122">-Stato</span><span class="sxs-lookup"><span data-stu-id="0b08a-122">-State</span></span>
<span data-ttu-id="0b08a-123">Specifica il nuovo valore a cui questo cmdlet aggiorna lo stato di azione consigliato.</span><span class="sxs-lookup"><span data-stu-id="0b08a-123">Specifies the new value to which this cmdlet updates the recommended action state.</span></span>
<span data-ttu-id="0b08a-124">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="0b08a-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0b08a-125">Active</span><span class="sxs-lookup"><span data-stu-id="0b08a-125">Active</span></span>
- <span data-ttu-id="0b08a-126">In sospeso</span><span class="sxs-lookup"><span data-stu-id="0b08a-126">Pending</span></span>
- <span data-ttu-id="0b08a-127">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="0b08a-127">PendingRevert</span></span>
- <span data-ttu-id="0b08a-128">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="0b08a-128">RevertCancelled</span></span>
- <span data-ttu-id="0b08a-129">Ignorato</span><span class="sxs-lookup"><span data-stu-id="0b08a-129">Ignored</span></span>
- <span data-ttu-id="0b08a-130">Risolto</span><span class="sxs-lookup"><span data-stu-id="0b08a-130">Resolved</span></span>

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

### <span data-ttu-id="0b08a-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0b08a-131">-Confirm</span></span>
<span data-ttu-id="0b08a-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b08a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b08a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b08a-133">-WhatIf</span></span>
<span data-ttu-id="0b08a-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0b08a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b08a-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0b08a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b08a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b08a-136">CommonParameters</span></span>
<span data-ttu-id="0b08a-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b08a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b08a-138">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b08a-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b08a-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0b08a-139">INPUTS</span></span>

### <span data-ttu-id="0b08a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="0b08a-140">System.String</span></span>

### <span data-ttu-id="0b08a-141">Microsoft. Azure. Commands. SQL. RecommendedAction. cmdlet. RecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="0b08a-141">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span></span>

## <span data-ttu-id="0b08a-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0b08a-142">OUTPUTS</span></span>

### <span data-ttu-id="0b08a-143">Microsoft. Azure. Commands. SQL. RecommendedAction. Model. AzureSqlServerRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="0b08a-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlServerRecommendedActionModel</span></span>

## <span data-ttu-id="0b08a-144">Note</span><span class="sxs-lookup"><span data-stu-id="0b08a-144">NOTES</span></span>
* <span data-ttu-id="0b08a-145">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, server, MSSQL, Advisor, RecommendedAction</span><span class="sxs-lookup"><span data-stu-id="0b08a-145">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="0b08a-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0b08a-146">RELATED LINKS</span></span>

[<span data-ttu-id="0b08a-147">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="0b08a-147">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="0b08a-148">Get-AzSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="0b08a-148">Get-AzSqlServerRecommendedAction</span></span>](./Get-AzSqlServerRecommendedAction.md)

[<span data-ttu-id="0b08a-149">Set-AzSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="0b08a-149">Set-AzSqlDatabaseRecommendedActionState</span></span>](./Set-AzSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="0b08a-150">Set-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="0b08a-150">Set-AzSqlElasticPoolRecommendedActionState</span></span>](./Set-AzSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="0b08a-151">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="0b08a-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)