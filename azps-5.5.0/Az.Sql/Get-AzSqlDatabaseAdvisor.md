---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5AAB22C6-8E3C-4BDC-8A54-DA5A9906B762
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseadvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvisor.md
ms.openlocfilehash: 05bde2ee8a5bbcae941203115c49ff6b9fbc6bae
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197766"
---
# <span data-ttu-id="249b4-101">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="249b4-101">Get-AzSqlDatabaseAdvisor</span></span>

## <span data-ttu-id="249b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="249b4-102">SYNOPSIS</span></span>
<span data-ttu-id="249b4-103">Ottiene uno o più consulenti per un database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="249b4-103">Gets one or more Advisors for an Azure SQL Database.</span></span>

## <span data-ttu-id="249b4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="249b4-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 -DatabaseName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="249b4-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="249b4-105">DESCRIPTION</span></span>
<span data-ttu-id="249b4-106">Il cmdlet **Get-AzSqlDatabaseAdvisor** ottiene uno o più consulenti database di Azure SQL per un database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="249b4-106">The **Get-AzSqlDatabaseAdvisor** cmdlet gets one or more Azure SQL Database Advisors for an Azure SQL Database.</span></span>

## <span data-ttu-id="249b4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="249b4-107">EXAMPLES</span></span>

### <span data-ttu-id="249b4-108">Esempio 1: Elencare tutti gli consulenti per il database specificato</span><span class="sxs-lookup"><span data-stu-id="249b4-108">Example 1: List all the advisors for the specified database</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner"
DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : SchemaIssue
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 8/1/2016 3:01:41 PM
RecommendationsStatus          : SchemaIsConsistent
RecommendedActions             : {}
```

<span data-ttu-id="249b4-109">Questo comando ottiene l'elenco di tutti gli consulenti per il database denominato WIRunner che appartiene al server denominato wi-run-australia-east.</span><span class="sxs-lookup"><span data-stu-id="249b4-109">This command gets lists all the advisors for the database named WIRunner that belongs to the server named wi-runner-australia-east.</span></span>

### <span data-ttu-id="249b4-110">Esempio 2: Ottenere un unico consulente per il database specificato</span><span class="sxs-lookup"><span data-stu-id="249b4-110">Example 2: Get a single advisor for the specified database</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex"
DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="249b4-111">Questo comando recupera l'advisor denominato CreateIndex per il database denominato WIRunner.</span><span class="sxs-lookup"><span data-stu-id="249b4-111">This command gets the Advisor named CreateIndex for the database named WIRunner.</span></span>

### <span data-ttu-id="249b4-112">Esempio 3: Elencare tutti gli consulenti con le azioni consigliate incluse nella risposta</span><span class="sxs-lookup"><span data-stu-id="249b4-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -ExpandRecommendedActions
DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.236046]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.239359]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.437714]_6C7AE8CC9C87E7FD5893...} 

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {IR_[test_schema]_[test_table_0.0288891]_38724E1DCF2178318957, 
                                 IR_[test_schema]_[test_table_0.140264]_38724E1DCF2178318957, 
                                 IR_[test_schema]_[test_table_0.412191]_38724E1DCF2178318957, 
                                 IR_[test_schema]_[test_table_0.442075]_38724E1DCF2178318957...} 

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : SchemaIssue
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 8/1/2016 3:04:26 PM
RecommendationsStatus          : SchemaIsConsistent
RecommendedActions             : {}
```

<span data-ttu-id="249b4-113">Questo comando recupera tutti gli consulenti per il database denominati "WIRunner" con le azioni consigliate incluse nella risposta.</span><span class="sxs-lookup"><span data-stu-id="249b4-113">This command gets all the advisors for the database named 'WIRunner' with their recommended actions included in the response.</span></span>
<span data-ttu-id="249b4-114">Poiché il comando usa *il parametro ExpandRecommendedActions,* il cmdlet ottiene le azioni consigliate con la risposta.</span><span class="sxs-lookup"><span data-stu-id="249b4-114">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the recommended actions with the response.</span></span>

### <span data-ttu-id="249b4-115">Esempio 4: Ottenere un consulente con le azioni consigliate incluse nella risposta</span><span class="sxs-lookup"><span data-stu-id="249b4-115">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex" -ExpandRecommendedActions
DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.236046]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.239359]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.437714]_6C7AE8CC9C87E7FD5893...}
```

<span data-ttu-id="249b4-116">Questo comando recupera l'consulente denominato CreateIndex dal database denominato WIRunner con le azioni consigliate incluse nella risposta.</span><span class="sxs-lookup"><span data-stu-id="249b4-116">This command gets the Advisor named CreateIndex from the database named WIRunner with its recommended actions included in the response.</span></span>
<span data-ttu-id="249b4-117">Poiché il comando usa *il parametro ExpandRecommendedActions,* il cmdlet ottiene le azioni consigliate con la risposta.</span><span class="sxs-lookup"><span data-stu-id="249b4-117">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the recommended actions with the response.</span></span>

### <span data-ttu-id="249b4-118">Esempio 5: Elencare tutti gli consulenti per il database specificato usando i filtri</span><span class="sxs-lookup"><span data-stu-id="249b4-118">Example 5: List all the advisors for the specified database using filtering</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName d*
DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}
```

<span data-ttu-id="249b4-119">Questo comando ottiene l'elenco di tutti gli consulenti per il database denominato WIRunner che appartiene al server denominato wi-run-australia-east e inizia con la lettera "d".</span><span class="sxs-lookup"><span data-stu-id="249b4-119">This command gets lists all the advisors for the database named WIRunner that belongs to the server named wi-runner-australia-east and start with the letter "d".</span></span>

## <span data-ttu-id="249b4-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="249b4-120">PARAMETERS</span></span>

### <span data-ttu-id="249b4-121">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="249b4-121">-AdvisorName</span></span>
<span data-ttu-id="249b4-122">Specifica il nome dell'consulente che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="249b4-122">Specifies the name of the advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="249b4-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="249b4-123">-DatabaseName</span></span>
<span data-ttu-id="249b4-124">Specifica il nome del database per cui questo cmdlet richiede l'advisor.</span><span class="sxs-lookup"><span data-stu-id="249b4-124">Specifies the name of the database for which this cmdlet requests the Advisor.</span></span>

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

### <span data-ttu-id="249b4-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="249b4-125">-DefaultProfile</span></span>
<span data-ttu-id="249b4-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="249b4-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="249b4-127">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="249b4-127">-ExpandRecommendedActions</span></span>
<span data-ttu-id="249b4-128">Indica che questo cmdlet ottiene le azioni consigliate con la risposta.</span><span class="sxs-lookup"><span data-stu-id="249b4-128">Indicates that this cmdlet gets the recommended actions with the response.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="249b4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="249b4-129">-ResourceGroupName</span></span>
<span data-ttu-id="249b4-130">Specifica il nome del gruppo di risorse del server che contiene il database.</span><span class="sxs-lookup"><span data-stu-id="249b4-130">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="249b4-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="249b4-131">-ServerName</span></span>
<span data-ttu-id="249b4-132">Specifica il nome del server che contiene il database.</span><span class="sxs-lookup"><span data-stu-id="249b4-132">Specifies the name of the server that contains the database.</span></span>

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

### <span data-ttu-id="249b4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="249b4-133">CommonParameters</span></span>
<span data-ttu-id="249b4-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="249b4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="249b4-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="249b4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="249b4-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="249b4-136">INPUTS</span></span>

### <span data-ttu-id="249b4-137">System.String</span><span class="sxs-lookup"><span data-stu-id="249b4-137">System.String</span></span>

### <span data-ttu-id="249b4-138">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="249b4-138">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="249b4-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="249b4-139">OUTPUTS</span></span>

### <span data-ttu-id="249b4-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="249b4-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>

## <span data-ttu-id="249b4-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="249b4-141">NOTES</span></span>
* <span data-ttu-id="249b4-142">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, sql, database, mssql, advisor</span><span class="sxs-lookup"><span data-stu-id="249b4-142">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor</span></span>

## <span data-ttu-id="249b4-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="249b4-143">RELATED LINKS</span></span>

[<span data-ttu-id="249b4-144">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="249b4-144">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="249b4-145">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="249b4-145">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="249b4-146">Get-AzSqlDatabaseRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="249b4-146">Get-AzSqlDatabaseRecommendedAction</span></span>](./Get-AzSqlDatabaseRecommendedAction.md)

[<span data-ttu-id="249b4-147">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="249b4-147">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlDatabaseAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="249b4-148">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="249b4-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
