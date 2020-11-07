---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: EFDFCE12-F39C-4F52-9962-4601F0C4FD47
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPoolRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPoolRecommendedActionState.md
ms.openlocfilehash: 1bc5d89a381027bd72697d873308eb85807a6e63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687064"
---
# <span data-ttu-id="9faca-101">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="9faca-101">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>

## <span data-ttu-id="9faca-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9faca-102">SYNOPSIS</span></span>
<span data-ttu-id="9faca-103">Aggiorna lo stato di un'azione consigliata di Azure SQL Elastic pool.</span><span class="sxs-lookup"><span data-stu-id="9faca-103">Updates the state of an Azure SQL Elastic Pool recommended action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9faca-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9faca-104">SYNTAX</span></span>

```
Set-AzureRmSqlElasticPoolRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -ElasticPoolName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9faca-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9faca-105">DESCRIPTION</span></span>
<span data-ttu-id="9faca-106">Il cmdlet **set-AzureRmSqlElasticPoolRecommendedActionState** aggiorna lo stato di un'azione consigliata di Azure SQL Elastic pool.</span><span class="sxs-lookup"><span data-stu-id="9faca-106">The **Set-AzureRmSqlElasticPoolRecommendedActionState** cmdlet updates state of an Azure SQL Elastic Pool recommended action.</span></span>
<span data-ttu-id="9faca-107">Questo cmdlet applica un'azione consigliata, ripristinata o scartata in base al nuovo stato.</span><span class="sxs-lookup"><span data-stu-id="9faca-107">This cmdlet applies an recommended action, reverted, or discarded based on the new state.</span></span>

## <span data-ttu-id="9faca-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9faca-108">EXAMPLES</span></span>

### <span data-ttu-id="9faca-109">Esempio 1: aggiornare lo stato di un'azione consigliata in sospeso</span><span class="sxs-lookup"><span data-stu-id="9faca-109">Example 1: Update the state of a recommended action to Pending</span></span>
```
PS C:\>Set-AzureRmSqlElasticPoolRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
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

<span data-ttu-id="9faca-110">Questo comando Aggiorna lo stato dell'azione consigliata del pool elastico denominato IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893 in sospeso.</span><span class="sxs-lookup"><span data-stu-id="9faca-110">This command updates the state of elastic pool recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 to Pending.</span></span>

## <span data-ttu-id="9faca-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9faca-111">PARAMETERS</span></span>

### <span data-ttu-id="9faca-112">-Advisorname</span><span class="sxs-lookup"><span data-stu-id="9faca-112">-AdvisorName</span></span>
<span data-ttu-id="9faca-113">Specifica il nome del consulente per cui appartiene l'azione consigliata.</span><span class="sxs-lookup"><span data-stu-id="9faca-113">Specifies the name of the advisor for which this recommended action belongs to.</span></span>

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

### <span data-ttu-id="9faca-114">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="9faca-114">-ElasticPoolName</span></span>
<span data-ttu-id="9faca-115">Specifica il nome del pool elastico.</span><span class="sxs-lookup"><span data-stu-id="9faca-115">Specifies name of the elastic pool.</span></span>

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

### <span data-ttu-id="9faca-116">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="9faca-116">-RecommendedActionName</span></span>
<span data-ttu-id="9faca-117">Specifica il nome dell'azione consigliata per cui questo cmdlet aggiorna lo stato.</span><span class="sxs-lookup"><span data-stu-id="9faca-117">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

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

### <span data-ttu-id="9faca-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9faca-118">-ResourceGroupName</span></span>
<span data-ttu-id="9faca-119">Specifica il nome del gruppo di risorse del server che contiene questo pool elastico.</span><span class="sxs-lookup"><span data-stu-id="9faca-119">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="9faca-120">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="9faca-120">-ServerName</span></span>
<span data-ttu-id="9faca-121">Specifica il nome del server in cui è presente il pool di elastici.</span><span class="sxs-lookup"><span data-stu-id="9faca-121">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="9faca-122">-Stato</span><span class="sxs-lookup"><span data-stu-id="9faca-122">-State</span></span>
<span data-ttu-id="9faca-123">Specifica il valore a cui questo cmdlet aggiorna lo stato di azione consigliato.</span><span class="sxs-lookup"><span data-stu-id="9faca-123">Specifies the value to which this cmdlet updates the recommended action state.</span></span>

<span data-ttu-id="9faca-124">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="9faca-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9faca-125">Active</span><span class="sxs-lookup"><span data-stu-id="9faca-125">Active</span></span>
- <span data-ttu-id="9faca-126">In sospeso</span><span class="sxs-lookup"><span data-stu-id="9faca-126">Pending</span></span>
- <span data-ttu-id="9faca-127">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="9faca-127">PendingRevert</span></span>
- <span data-ttu-id="9faca-128">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="9faca-128">RevertCancelled</span></span>
- <span data-ttu-id="9faca-129">Ignorato</span><span class="sxs-lookup"><span data-stu-id="9faca-129">Ignored</span></span>
- <span data-ttu-id="9faca-130">Risolto</span><span class="sxs-lookup"><span data-stu-id="9faca-130">Resolved</span></span>

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

### <span data-ttu-id="9faca-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9faca-131">-Confirm</span></span>
<span data-ttu-id="9faca-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9faca-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9faca-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9faca-133">-WhatIf</span></span>
<span data-ttu-id="9faca-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9faca-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9faca-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9faca-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9faca-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9faca-136">-DefaultProfile</span></span>
<span data-ttu-id="9faca-137">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9faca-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9faca-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9faca-138">CommonParameters</span></span>
<span data-ttu-id="9faca-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9faca-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9faca-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9faca-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9faca-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9faca-141">INPUTS</span></span>

## <span data-ttu-id="9faca-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9faca-142">OUTPUTS</span></span>

## <span data-ttu-id="9faca-143">Note</span><span class="sxs-lookup"><span data-stu-id="9faca-143">NOTES</span></span>
* <span data-ttu-id="9faca-144">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, elasticpool, MSSQL, Advisor, RecommendedAction</span><span class="sxs-lookup"><span data-stu-id="9faca-144">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="9faca-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9faca-145">RELATED LINKS</span></span>

[<span data-ttu-id="9faca-146">Get-AzureRmSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="9faca-146">Get-AzureRmSqlElasticPoolRecommendedAction</span></span>](./Get-AzureRmSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="9faca-147">Set-AzureRmSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="9faca-147">Set-AzureRmSqlDatabaseRecommendedActionState</span></span>](./Set-AzureRmSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="9faca-148">Set-AzureRmSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="9faca-148">Set-AzureRmSqlServerRecommendedActionState</span></span>](./Set-AzureRmSqlServerRecommendedActionState.md)

[<span data-ttu-id="9faca-149">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="9faca-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
