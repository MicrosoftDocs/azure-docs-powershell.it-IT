---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 26EC220C-5123-4CEF-8CC6-5FFD08F33481
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverrecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerRecommendedActionState.md
ms.openlocfilehash: 5155b2f292b21af9696bee3ca70fca50850a7e73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509575"
---
# <span data-ttu-id="e5178-101">Set-AzureRmSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="e5178-101">Set-AzureRmSqlServerRecommendedActionState</span></span>

## <span data-ttu-id="e5178-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e5178-102">SYNOPSIS</span></span>
<span data-ttu-id="e5178-103">Aggiorna lo stato di un'azione consigliata di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e5178-103">Updates the state of an Azure SQL Server recommended action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5178-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e5178-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5178-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e5178-105">DESCRIPTION</span></span>
<span data-ttu-id="e5178-106">Il cmdlet **set-AzureRmSqlServerRecommendedActionState** aggiorna lo stato di un'azione consigliata di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e5178-106">The **Set-AzureRmSqlServerRecommendedActionState** cmdlet updates state of an Azure SQL Server recommended action.</span></span>
<span data-ttu-id="e5178-107">Questo cmdlet applica, ripristina o Elimina l'azione consigliata in base al nuovo stato.</span><span class="sxs-lookup"><span data-stu-id="e5178-107">This cmdlet applies, reverts, or discards the recommended action based on the new state.</span></span>

## <span data-ttu-id="e5178-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e5178-108">EXAMPLES</span></span>

### <span data-ttu-id="e5178-109">Esempio1: aggiornare lo stato dell'azione consigliata specificata in sospeso</span><span class="sxs-lookup"><span data-stu-id="e5178-109">Example1: Update the state of the specified recommended action to Pending</span></span>
```
PS C:\>Set-AzureRmSqlServerRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
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

<span data-ttu-id="e5178-110">Stato aggiornamenti dell'azione consigliata del server denominata "IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893" a "in sospeso"</span><span class="sxs-lookup"><span data-stu-id="e5178-110">Updates state of server recommended action named "IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893" to "Pending"</span></span>

## <span data-ttu-id="e5178-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e5178-111">PARAMETERS</span></span>

### <span data-ttu-id="e5178-112">-Advisorname</span><span class="sxs-lookup"><span data-stu-id="e5178-112">-AdvisorName</span></span>
<span data-ttu-id="e5178-113">Specifica il nome del consulente che contiene l'azione consigliata.</span><span class="sxs-lookup"><span data-stu-id="e5178-113">Specifies the name of the advisor that contains the recommended action.</span></span>

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

### <span data-ttu-id="e5178-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5178-114">-DefaultProfile</span></span>
<span data-ttu-id="e5178-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e5178-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5178-116">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="e5178-116">-RecommendedActionName</span></span>
<span data-ttu-id="e5178-117">Specifica il nome dell'azione consigliata per cui questo cmdlet aggiorna lo stato.</span><span class="sxs-lookup"><span data-stu-id="e5178-117">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

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

### <span data-ttu-id="e5178-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5178-118">-ResourceGroupName</span></span>
<span data-ttu-id="e5178-119">Specifica il nome del gruppo di risorse del server.</span><span class="sxs-lookup"><span data-stu-id="e5178-119">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="e5178-120">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="e5178-120">-ServerName</span></span>
<span data-ttu-id="e5178-121">Specifica il nome del server.</span><span class="sxs-lookup"><span data-stu-id="e5178-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="e5178-122">-Stato</span><span class="sxs-lookup"><span data-stu-id="e5178-122">-State</span></span>
<span data-ttu-id="e5178-123">Specifica il nuovo valore a cui questo cmdlet aggiorna lo stato di azione consigliato.</span><span class="sxs-lookup"><span data-stu-id="e5178-123">Specifies the new value to which this cmdlet updates the recommended action state.</span></span>

<span data-ttu-id="e5178-124">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="e5178-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e5178-125">Active</span><span class="sxs-lookup"><span data-stu-id="e5178-125">Active</span></span>
- <span data-ttu-id="e5178-126">In sospeso</span><span class="sxs-lookup"><span data-stu-id="e5178-126">Pending</span></span>
- <span data-ttu-id="e5178-127">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="e5178-127">PendingRevert</span></span>
- <span data-ttu-id="e5178-128">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="e5178-128">RevertCancelled</span></span>
- <span data-ttu-id="e5178-129">Ignorato</span><span class="sxs-lookup"><span data-stu-id="e5178-129">Ignored</span></span>
- <span data-ttu-id="e5178-130">Risolto</span><span class="sxs-lookup"><span data-stu-id="e5178-130">Resolved</span></span>

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

### <span data-ttu-id="e5178-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e5178-131">-Confirm</span></span>
<span data-ttu-id="e5178-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5178-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5178-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5178-133">-WhatIf</span></span>
<span data-ttu-id="e5178-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e5178-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5178-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e5178-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5178-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5178-136">CommonParameters</span></span>
<span data-ttu-id="e5178-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5178-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5178-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5178-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5178-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e5178-139">INPUTS</span></span>

### <span data-ttu-id="e5178-140">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e5178-140">None</span></span>
<span data-ttu-id="e5178-141">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="e5178-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e5178-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e5178-142">OUTPUTS</span></span>

### <span data-ttu-id="e5178-143">Microsoft. Azure. Commands. SQL. RecommendedAction. Model. AzureSqlServerRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="e5178-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlServerRecommendedActionModel</span></span>

## <span data-ttu-id="e5178-144">Note</span><span class="sxs-lookup"><span data-stu-id="e5178-144">NOTES</span></span>
* <span data-ttu-id="e5178-145">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, server, MSSQL, Advisor, RecommendedAction</span><span class="sxs-lookup"><span data-stu-id="e5178-145">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="e5178-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e5178-146">RELATED LINKS</span></span>

[<span data-ttu-id="e5178-147">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="e5178-147">Get-AzureRmSqlServerAdvisor</span></span>](./Get-AzureRmSqlServerAdvisor.md)

[<span data-ttu-id="e5178-148">Get-AzureRmSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="e5178-148">Get-AzureRmSqlServerRecommendedAction</span></span>](./Get-AzureRmSqlServerRecommendedAction.md)

[<span data-ttu-id="e5178-149">Set-AzureRmSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="e5178-149">Set-AzureRmSqlDatabaseRecommendedActionState</span></span>](./Set-AzureRmSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="e5178-150">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="e5178-150">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>](./Set-AzureRmSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="e5178-151">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="e5178-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
