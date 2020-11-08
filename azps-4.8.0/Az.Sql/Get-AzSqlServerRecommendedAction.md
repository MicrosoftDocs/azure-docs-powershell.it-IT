---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BB513A53-48A0-4F8F-93F0-D3DFA2C3D523
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverrecommendedaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerRecommendedAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerRecommendedAction.md
ms.openlocfilehash: b27ded3d1ec4dbf011ca819ab55ddef0fb0df9c6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190074"
---
# <span data-ttu-id="43573-101">Get-AzSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="43573-101">Get-AzSqlServerRecommendedAction</span></span>

## <span data-ttu-id="43573-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="43573-102">SYNOPSIS</span></span>
<span data-ttu-id="43573-103">Ottiene una o più azioni consigliate per un consulente di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="43573-103">Gets one or more recommended actions for an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="43573-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="43573-104">SYNTAX</span></span>

```
Get-AzSqlServerRecommendedAction [-RecommendedActionName <String>] -ServerName <String> -AdvisorName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43573-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43573-105">DESCRIPTION</span></span>
<span data-ttu-id="43573-106">Il cmdlet **Get-AzSqlServerRecommendedAction** consente di ottenere una o più azioni consigliate per un programma di gestione di SQL Server di Azure.</span><span class="sxs-lookup"><span data-stu-id="43573-106">The **Get-AzSqlServerRecommendedAction** cmdlet gets one or more recommended actions for an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="43573-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="43573-107">EXAMPLES</span></span>

### <span data-ttu-id="43573-108">Esempio 1: ottenere un elenco di tutte le azioni consigliate per un consulente specifico</span><span class="sxs-lookup"><span data-stu-id="43573-108">Example 1: Get a list of  all recommended actions for a specific Advisor</span></span>
```
PS C:\>Get-AzSqlServerRecommendedAction -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex"
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

<span data-ttu-id="43573-109">Questo comando consente di ottenere un elenco di tutte le azioni consigliate per SQL Server Advisor denominato CreateIndex disponibile per il server denominato Wi-Runner-Australia-Est.</span><span class="sxs-lookup"><span data-stu-id="43573-109">This command gets a list of all recommended actions of for the SQL Server Advisor named CreateIndex available for the server named wi-runner-australia-east.</span></span>

### <span data-ttu-id="43573-110">Esempio 2: ottenere una singola azione consigliata per un consulente</span><span class="sxs-lookup"><span data-stu-id="43573-110">Example 2: Get a single recommended action for an Advisor</span></span>
```
PS C:\>Get-AzSqlServerRecommendedAction -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -RecommendedActionName 
IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893
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

<span data-ttu-id="43573-111">Questo comando ottiene un'azione consigliata denominata IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893 dal consulente denominato CreateIndex.</span><span class="sxs-lookup"><span data-stu-id="43573-111">This command gets a recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 from the Advisor named CreateIndex.</span></span>

## <span data-ttu-id="43573-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="43573-112">PARAMETERS</span></span>

### <span data-ttu-id="43573-113">-Advisorname</span><span class="sxs-lookup"><span data-stu-id="43573-113">-AdvisorName</span></span>
<span data-ttu-id="43573-114">Specifica il nome del consulente per il quale questo cmdlet richiede le azioni.</span><span class="sxs-lookup"><span data-stu-id="43573-114">Specifies the name of the advisor for which this cmdlet requests actions.</span></span>

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

### <span data-ttu-id="43573-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43573-115">-DefaultProfile</span></span>
<span data-ttu-id="43573-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="43573-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43573-117">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="43573-117">-RecommendedActionName</span></span>
<span data-ttu-id="43573-118">Specifica il nome dell'azione consigliata ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43573-118">Specifies the name of the recommended action that this cmdlet gets.</span></span>

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

### <span data-ttu-id="43573-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43573-119">-ResourceGroupName</span></span>
<span data-ttu-id="43573-120">Specifica il nome del gruppo di risorse del server che contiene il server.</span><span class="sxs-lookup"><span data-stu-id="43573-120">Specifies the name of the resource group of the server that contains this server.</span></span>

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

### <span data-ttu-id="43573-121">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="43573-121">-ServerName</span></span>
<span data-ttu-id="43573-122">Specifica il nome del server a cui appartiene Advisor.</span><span class="sxs-lookup"><span data-stu-id="43573-122">Specifies the name of the server the Advisor belongs to.</span></span>

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

### <span data-ttu-id="43573-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43573-123">CommonParameters</span></span>
<span data-ttu-id="43573-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43573-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43573-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43573-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43573-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="43573-126">INPUTS</span></span>

### <span data-ttu-id="43573-127">System. String</span><span class="sxs-lookup"><span data-stu-id="43573-127">System.String</span></span>

## <span data-ttu-id="43573-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="43573-128">OUTPUTS</span></span>

### <span data-ttu-id="43573-129">Microsoft. Azure. Commands. SQL. RecommendedAction. Model. AzureSqlServerRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="43573-129">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlServerRecommendedActionModel</span></span>

## <span data-ttu-id="43573-130">Note</span><span class="sxs-lookup"><span data-stu-id="43573-130">NOTES</span></span>
* <span data-ttu-id="43573-131">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, server, MSSQL, Advisor, RecommendedAction</span><span class="sxs-lookup"><span data-stu-id="43573-131">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="43573-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="43573-132">RELATED LINKS</span></span>

[<span data-ttu-id="43573-133">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="43573-133">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="43573-134">Set-AzSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="43573-134">Set-AzSqlServerRecommendedActionState</span></span>](./Set-AzSqlServerRecommendedActionState.md)

[<span data-ttu-id="43573-135">Get-AzSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="43573-135">Get-AzSqlElasticPoolRecommendedAction</span></span>](./Get-AzSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="43573-136">Get-AzSqlDatabaseRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="43573-136">Get-AzSqlDatabaseRecommendedAction</span></span>](./Get-AzSqlDatabaseRecommendedAction.md)

[<span data-ttu-id="43573-137">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="43573-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
