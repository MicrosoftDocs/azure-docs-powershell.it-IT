---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: EFDFCE12-F39C-4F52-9962-4601F0C4FD47
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlelasticpoolrecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPoolRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPoolRecommendedActionState.md
ms.openlocfilehash: 992dc949ec4c17529415beeeb2cf2a831d4d2a68
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512151"
---
# <span data-ttu-id="a4210-101">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="a4210-101">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>

## <span data-ttu-id="a4210-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a4210-102">SYNOPSIS</span></span>
<span data-ttu-id="a4210-103">Aggiorna lo stato di un'azione consigliata di Azure SQL Elastic pool.</span><span class="sxs-lookup"><span data-stu-id="a4210-103">Updates the state of an Azure SQL Elastic Pool recommended action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4210-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a4210-104">SYNTAX</span></span>

```
Set-AzureRmSqlElasticPoolRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -ElasticPoolName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4210-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a4210-105">DESCRIPTION</span></span>
<span data-ttu-id="a4210-106">Il cmdlet **set-AzureRmSqlElasticPoolRecommendedActionState** aggiorna lo stato di un'azione consigliata di Azure SQL Elastic pool.</span><span class="sxs-lookup"><span data-stu-id="a4210-106">The **Set-AzureRmSqlElasticPoolRecommendedActionState** cmdlet updates state of an Azure SQL Elastic Pool recommended action.</span></span>
<span data-ttu-id="a4210-107">Questo cmdlet applica un'azione consigliata, ripristinata o scartata in base al nuovo stato.</span><span class="sxs-lookup"><span data-stu-id="a4210-107">This cmdlet applies an recommended action, reverted, or discarded based on the new state.</span></span>

## <span data-ttu-id="a4210-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a4210-108">EXAMPLES</span></span>

### <span data-ttu-id="a4210-109">Esempio 1: aggiornare lo stato di un'azione consigliata in sospeso</span><span class="sxs-lookup"><span data-stu-id="a4210-109">Example 1: Update the state of a recommended action to Pending</span></span>
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

<span data-ttu-id="a4210-110">Questo comando Aggiorna lo stato dell'azione consigliata del pool elastico denominato IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893 in sospeso.</span><span class="sxs-lookup"><span data-stu-id="a4210-110">This command updates the state of elastic pool recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 to Pending.</span></span>

## <span data-ttu-id="a4210-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a4210-111">PARAMETERS</span></span>

### <span data-ttu-id="a4210-112">-Advisorname</span><span class="sxs-lookup"><span data-stu-id="a4210-112">-AdvisorName</span></span>
<span data-ttu-id="a4210-113">Specifica il nome del consulente per cui appartiene l'azione consigliata.</span><span class="sxs-lookup"><span data-stu-id="a4210-113">Specifies the name of the advisor for which this recommended action belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4210-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4210-114">-DefaultProfile</span></span>
<span data-ttu-id="a4210-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a4210-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4210-116">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="a4210-116">-ElasticPoolName</span></span>
<span data-ttu-id="a4210-117">Specifica il nome del pool elastico.</span><span class="sxs-lookup"><span data-stu-id="a4210-117">Specifies name of the elastic pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4210-118">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="a4210-118">-RecommendedActionName</span></span>
<span data-ttu-id="a4210-119">Specifica il nome dell'azione consigliata per cui questo cmdlet aggiorna lo stato.</span><span class="sxs-lookup"><span data-stu-id="a4210-119">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4210-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4210-120">-ResourceGroupName</span></span>
<span data-ttu-id="a4210-121">Specifica il nome del gruppo di risorse del server che contiene questo pool elastico.</span><span class="sxs-lookup"><span data-stu-id="a4210-121">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4210-122">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="a4210-122">-ServerName</span></span>
<span data-ttu-id="a4210-123">Specifica il nome del server in cui è presente il pool di elastici.</span><span class="sxs-lookup"><span data-stu-id="a4210-123">Specifies the name of the server the elastic pool is in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4210-124">-Stato</span><span class="sxs-lookup"><span data-stu-id="a4210-124">-State</span></span>
<span data-ttu-id="a4210-125">Specifica il valore a cui questo cmdlet aggiorna lo stato di azione consigliato.</span><span class="sxs-lookup"><span data-stu-id="a4210-125">Specifies the value to which this cmdlet updates the recommended action state.</span></span>

<span data-ttu-id="a4210-126">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a4210-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a4210-127">Active</span><span class="sxs-lookup"><span data-stu-id="a4210-127">Active</span></span>
- <span data-ttu-id="a4210-128">In sospeso</span><span class="sxs-lookup"><span data-stu-id="a4210-128">Pending</span></span>
- <span data-ttu-id="a4210-129">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="a4210-129">PendingRevert</span></span>
- <span data-ttu-id="a4210-130">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="a4210-130">RevertCancelled</span></span>
- <span data-ttu-id="a4210-131">Ignorato</span><span class="sxs-lookup"><span data-stu-id="a4210-131">Ignored</span></span>
- <span data-ttu-id="a4210-132">Risolto</span><span class="sxs-lookup"><span data-stu-id="a4210-132">Resolved</span></span>

```yaml
Type: RecommendedActionState
Parameter Sets: (All)
Aliases:
Accepted values: Active, Pending, PendingRevert, RevertCancelled, Ignored, Resolved

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4210-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a4210-133">-Confirm</span></span>
<span data-ttu-id="a4210-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4210-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4210-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4210-135">-WhatIf</span></span>
<span data-ttu-id="a4210-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a4210-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4210-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a4210-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4210-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4210-138">CommonParameters</span></span>
<span data-ttu-id="a4210-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4210-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4210-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4210-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4210-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a4210-141">INPUTS</span></span>

### <span data-ttu-id="a4210-142">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a4210-142">None</span></span>
<span data-ttu-id="a4210-143">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="a4210-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a4210-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a4210-144">OUTPUTS</span></span>

## <span data-ttu-id="a4210-145">Note</span><span class="sxs-lookup"><span data-stu-id="a4210-145">NOTES</span></span>
* <span data-ttu-id="a4210-146">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, elasticpool, MSSQL, Advisor, RecommendedAction</span><span class="sxs-lookup"><span data-stu-id="a4210-146">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="a4210-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a4210-147">RELATED LINKS</span></span>

[<span data-ttu-id="a4210-148">Get-AzureRmSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="a4210-148">Get-AzureRmSqlElasticPoolRecommendedAction</span></span>](./Get-AzureRmSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="a4210-149">Set-AzureRmSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="a4210-149">Set-AzureRmSqlDatabaseRecommendedActionState</span></span>](./Set-AzureRmSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="a4210-150">Set-AzureRmSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="a4210-150">Set-AzureRmSqlServerRecommendedActionState</span></span>](./Set-AzureRmSqlServerRecommendedActionState.md)

[<span data-ttu-id="a4210-151">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="a4210-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)