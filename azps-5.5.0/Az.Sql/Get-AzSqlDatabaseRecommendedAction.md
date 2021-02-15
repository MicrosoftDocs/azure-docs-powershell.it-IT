---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: EF6C862B-A89C-48AB-A590-92CFA387305F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaserecommendedaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseRecommendedAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseRecommendedAction.md
ms.openlocfilehash: fc54e470ed79593b40d25fdfc4cf655a0a8f44d4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188958"
---
# <span data-ttu-id="08211-101">Get-AzSqlDatabaseRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="08211-101">Get-AzSqlDatabaseRecommendedAction</span></span>

## <span data-ttu-id="08211-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08211-102">SYNOPSIS</span></span>
<span data-ttu-id="08211-103">Recupera una o più azioni consigliate per un amministratore di Azure SQL Database Advisor.</span><span class="sxs-lookup"><span data-stu-id="08211-103">Gets one or more recommended actions for an Azure SQL Database Advisor.</span></span>

## <span data-ttu-id="08211-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="08211-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseRecommendedAction [-RecommendedActionName <String>] -ServerName <String>
 -DatabaseName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08211-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="08211-105">DESCRIPTION</span></span>
<span data-ttu-id="08211-106">Il **cmdlet Get-AzSqlDatabaseRecommendedAction** ottiene una o più azioni consigliate per un'utilità per la SQL database di Azure.</span><span class="sxs-lookup"><span data-stu-id="08211-106">The **Get-AzSqlDatabaseRecommendedAction** cmdlet gets one or more recommended actions for an Azure SQL Database Advisor.</span></span>

## <span data-ttu-id="08211-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="08211-107">EXAMPLES</span></span>

### <span data-ttu-id="08211-108">Esempio 1: Elencare tutte le azioni consigliate per un consulente</span><span class="sxs-lookup"><span data-stu-id="08211-108">Example 1: List all the recommended actions for an Advisor</span></span>
```
PS C:\>Get-AzSqlDatabaseRecommendedAction -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex"
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

DatabaseName               : WIRunner
ResourceGroupName          : WIRunnersProd
ServerName                 : wi-runner-australia-east
AdvisorName                : CreateIndex
RecommendedActionName      : IR_[test_schema]_[test_table_0.236046]_6C7AE8CC9C87E7FD5893
Details                    : {[indexName, nci_wi_test_table_0.236046_6C7AE8CC9C87E7FD5893], [indexType, NONCLUSTERED], 
                             [schema, [test_schema]], [table, [test_table_0.236046]]...} 
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
ObservedImpact             : {SpaceChange}
RecommendationReason       : 
RevertActionDuration       : 
RevertActionInitiatedBy    : 
RevertActionInitiatedTime  : 
RevertActionStartTime      : 
Score                      : 3
State                      : Microsoft.Azure.Management.Sql.Models.RecommendedActionStateInfo
TimeSeries                 : {}
ValidSince                 : 4/21/2016 3:24:47 PM
DatabaseName               : WIRunner
ResourceGroupName          : WIRunnersProd
ServerName                 : wi-runner-australia-east
AdvisorName                : CreateIndex
RecommendedActionName      : IR_[test_schema]_[test_table_0.239359]_6C7AE8CC9C87E7FD5893
Details                    : {[indexName, nci_wi_test_table_0.239359_6C7AE8CC9C87E7FD5893], [indexType, NONCLUSTERED], 
                             [schema, [test_schema]], [table, [test_table_0.239359]]...} 
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
RevertActionDuration       : PT10S
RevertActionInitiatedBy    : System
RevertActionInitiatedTime  : 4/21/2016 3:24:47 PM
RevertActionStartTime      : 4/21/2016 3:24:47 PM
Score                      : 3
State                      : Microsoft.Azure.Management.Sql.Models.RecommendedActionStateInfo
TimeSeries                 : {}
ValidSince                 : 4/21/2016 3:24:47 PM
```

<span data-ttu-id="08211-109">Questo comando ottiene un elenco di tutte le azioni consigliate dell'consulente denominato CreateIndex disponibile per il database denominato wi-runner-australia-east.</span><span class="sxs-lookup"><span data-stu-id="08211-109">This command gets a list of all recommended actions of the Advisor named CreateIndex available for the database named wi-runner-australia-east.</span></span>

### <span data-ttu-id="08211-110">Esempio 2: Ottenere una sola azione consigliata per un consulente</span><span class="sxs-lookup"><span data-stu-id="08211-110">Example 2: Get a single recommended action for an Advisor</span></span>
```
PS C:\>Get-AzSqlDatabaseRecommendedAction -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893"
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

<span data-ttu-id="08211-111">Questo comando recupera l'azione consigliata IR_ \[ test_schema \] _ \[ test_table_0.0361551 _6C7AE8CC9C87E7FD5893 per l'consulente \] denominato CreateIndex.</span><span class="sxs-lookup"><span data-stu-id="08211-111">This command gets the recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 for the Advisor named CreateIndex.</span></span>

## <span data-ttu-id="08211-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="08211-112">PARAMETERS</span></span>

### <span data-ttu-id="08211-113">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="08211-113">-AdvisorName</span></span>
<span data-ttu-id="08211-114">Specifica il nome dell'consulente per cui questo cmdlet richiede le azioni consigliate.</span><span class="sxs-lookup"><span data-stu-id="08211-114">Specifies the name of the Advisor for which this cmdlet requests recommended actions.</span></span>

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

### <span data-ttu-id="08211-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="08211-115">-DatabaseName</span></span>
<span data-ttu-id="08211-116">Specifica il nome del database per cui questo cmdlet richiede le azioni consigliate.</span><span class="sxs-lookup"><span data-stu-id="08211-116">Specifies the name of the database for which this cmdlet requests recommended actions.</span></span>

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

### <span data-ttu-id="08211-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08211-117">-DefaultProfile</span></span>
<span data-ttu-id="08211-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="08211-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="08211-119">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="08211-119">-RecommendedActionName</span></span>
<span data-ttu-id="08211-120">Specifica il nome dell'azione consigliata che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08211-120">Specifies the name of the recommended action that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08211-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08211-121">-ResourceGroupName</span></span>
<span data-ttu-id="08211-122">Specifica il nome del gruppo di risorse del server che contiene il database.</span><span class="sxs-lookup"><span data-stu-id="08211-122">Specifies name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="08211-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="08211-123">-ServerName</span></span>
<span data-ttu-id="08211-124">Specifica il nome del server in cui si trova il database.</span><span class="sxs-lookup"><span data-stu-id="08211-124">Specifies the name of the server the database is in.</span></span>

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

### <span data-ttu-id="08211-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08211-125">CommonParameters</span></span>
<span data-ttu-id="08211-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08211-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08211-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="08211-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08211-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="08211-128">INPUTS</span></span>

### <span data-ttu-id="08211-129">System.String</span><span class="sxs-lookup"><span data-stu-id="08211-129">System.String</span></span>

## <span data-ttu-id="08211-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="08211-130">OUTPUTS</span></span>

### <span data-ttu-id="08211-131">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlDatabaseRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="08211-131">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlDatabaseRecommendedActionModel</span></span>

## <span data-ttu-id="08211-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="08211-132">NOTES</span></span>
* <span data-ttu-id="08211-133">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, sql, database, mssql, advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="08211-133">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="08211-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="08211-134">RELATED LINKS</span></span>

[<span data-ttu-id="08211-135">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="08211-135">Get-AzSqlDatabaseAdvisor</span></span>](./Get-AzSqlDatabaseAdvisor.md)

[<span data-ttu-id="08211-136">Get-AzSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="08211-136">Get-AzSqlServerRecommendedAction</span></span>](./Get-AzSqlServerRecommendedAction.md)

[<span data-ttu-id="08211-137">Set-AzSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="08211-137">Set-AzSqlDatabaseRecommendedActionState</span></span>](./Set-AzSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="08211-138">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="08211-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
