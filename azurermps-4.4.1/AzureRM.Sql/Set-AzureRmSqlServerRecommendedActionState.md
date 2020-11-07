---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 26EC220C-5123-4CEF-8CC6-5FFD08F33481
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerRecommendedActionState.md
ms.openlocfilehash: 4b000ef101b07bf882accb10b0256e0dbea513b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688495"
---
# <span data-ttu-id="cae23-101">Set-AzureRmSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="cae23-101">Set-AzureRmSqlServerRecommendedActionState</span></span>

## <span data-ttu-id="cae23-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cae23-102">SYNOPSIS</span></span>
<span data-ttu-id="cae23-103">Aggiorna lo stato di un'azione consigliata di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="cae23-103">Updates the state of an Azure SQL Server recommended action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cae23-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cae23-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cae23-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cae23-105">DESCRIPTION</span></span>
<span data-ttu-id="cae23-106">Il cmdlet **set-AzureRmSqlServerRecommendedActionState** aggiorna lo stato di un'azione consigliata di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="cae23-106">The **Set-AzureRmSqlServerRecommendedActionState** cmdlet updates state of an Azure SQL Server recommended action.</span></span>
<span data-ttu-id="cae23-107">Questo cmdlet applica, ripristina o Elimina l'azione consigliata in base al nuovo stato.</span><span class="sxs-lookup"><span data-stu-id="cae23-107">This cmdlet applies, reverts, or discards the recommended action based on the new state.</span></span>

## <span data-ttu-id="cae23-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cae23-108">EXAMPLES</span></span>

### <span data-ttu-id="cae23-109">Esempio1: aggiornare lo stato dell'azione consigliata specificata in sospeso</span><span class="sxs-lookup"><span data-stu-id="cae23-109">Example1: Update the state of the specified recommended action to Pending</span></span>
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

<span data-ttu-id="cae23-110">Stato aggiornamenti dell'azione consigliata del server denominata "IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893" a "in sospeso"</span><span class="sxs-lookup"><span data-stu-id="cae23-110">Updates state of server recommended action named "IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893" to "Pending"</span></span>

## <span data-ttu-id="cae23-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cae23-111">PARAMETERS</span></span>

### <span data-ttu-id="cae23-112">-Advisorname</span><span class="sxs-lookup"><span data-stu-id="cae23-112">-AdvisorName</span></span>
<span data-ttu-id="cae23-113">Specifica il nome del consulente che contiene l'azione consigliata.</span><span class="sxs-lookup"><span data-stu-id="cae23-113">Specifies the name of the advisor that contains the recommended action.</span></span>

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

### <span data-ttu-id="cae23-114">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="cae23-114">-RecommendedActionName</span></span>
<span data-ttu-id="cae23-115">Specifica il nome dell'azione consigliata per cui questo cmdlet aggiorna lo stato.</span><span class="sxs-lookup"><span data-stu-id="cae23-115">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

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

### <span data-ttu-id="cae23-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cae23-116">-ResourceGroupName</span></span>
<span data-ttu-id="cae23-117">Specifica il nome del gruppo di risorse del server.</span><span class="sxs-lookup"><span data-stu-id="cae23-117">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="cae23-118">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="cae23-118">-ServerName</span></span>
<span data-ttu-id="cae23-119">Specifica il nome del server.</span><span class="sxs-lookup"><span data-stu-id="cae23-119">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="cae23-120">-Stato</span><span class="sxs-lookup"><span data-stu-id="cae23-120">-State</span></span>
<span data-ttu-id="cae23-121">Specifica il nuovo valore a cui questo cmdlet aggiorna lo stato di azione consigliato.</span><span class="sxs-lookup"><span data-stu-id="cae23-121">Specifies the new value to which this cmdlet updates the recommended action state.</span></span>

<span data-ttu-id="cae23-122">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="cae23-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cae23-123">Active</span><span class="sxs-lookup"><span data-stu-id="cae23-123">Active</span></span>
- <span data-ttu-id="cae23-124">In sospeso</span><span class="sxs-lookup"><span data-stu-id="cae23-124">Pending</span></span>
- <span data-ttu-id="cae23-125">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="cae23-125">PendingRevert</span></span>
- <span data-ttu-id="cae23-126">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="cae23-126">RevertCancelled</span></span>
- <span data-ttu-id="cae23-127">Ignorato</span><span class="sxs-lookup"><span data-stu-id="cae23-127">Ignored</span></span>
- <span data-ttu-id="cae23-128">Risolto</span><span class="sxs-lookup"><span data-stu-id="cae23-128">Resolved</span></span>

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

### <span data-ttu-id="cae23-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cae23-129">-Confirm</span></span>
<span data-ttu-id="cae23-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cae23-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cae23-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cae23-131">-WhatIf</span></span>
<span data-ttu-id="cae23-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cae23-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cae23-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cae23-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cae23-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cae23-134">-DefaultProfile</span></span>
<span data-ttu-id="cae23-135">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cae23-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cae23-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cae23-136">CommonParameters</span></span>
<span data-ttu-id="cae23-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cae23-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cae23-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cae23-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cae23-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cae23-139">INPUTS</span></span>

## <span data-ttu-id="cae23-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cae23-140">OUTPUTS</span></span>

### <span data-ttu-id="cae23-141">Microsoft. Azure. Commands. SQL. RecommendedAction. Model. AzureSqlServerRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="cae23-141">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlServerRecommendedActionModel</span></span>

## <span data-ttu-id="cae23-142">Note</span><span class="sxs-lookup"><span data-stu-id="cae23-142">NOTES</span></span>
* <span data-ttu-id="cae23-143">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, server, MSSQL, Advisor, RecommendedAction</span><span class="sxs-lookup"><span data-stu-id="cae23-143">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="cae23-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cae23-144">RELATED LINKS</span></span>

[<span data-ttu-id="cae23-145">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="cae23-145">Get-AzureRmSqlServerAdvisor</span></span>](./Get-AzureRmSqlServerAdvisor.md)

[<span data-ttu-id="cae23-146">Get-AzureRmSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="cae23-146">Get-AzureRmSqlServerRecommendedAction</span></span>](./Get-AzureRmSqlServerRecommendedAction.md)

[<span data-ttu-id="cae23-147">Set-AzureRmSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="cae23-147">Set-AzureRmSqlDatabaseRecommendedActionState</span></span>](./Set-AzureRmSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="cae23-148">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="cae23-148">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>](./Set-AzureRmSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="cae23-149">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="cae23-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
