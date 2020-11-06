---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 5AAB22C6-8E3C-4BDC-8A54-DA5A9906B762
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseadvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAdvisor.md
ms.openlocfilehash: 853702ab34a6a9dab7e90f2335f99deb7155a837
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518540"
---
# <span data-ttu-id="84d3e-101">Get-AzureRmSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="84d3e-101">Get-AzureRmSqlDatabaseAdvisor</span></span>

## <span data-ttu-id="84d3e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="84d3e-102">SYNOPSIS</span></span>
<span data-ttu-id="84d3e-103">Ottiene uno o più consulenti per un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="84d3e-103">Gets one or more Advisors for an Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84d3e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="84d3e-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 -DatabaseName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="84d3e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84d3e-105">DESCRIPTION</span></span>
<span data-ttu-id="84d3e-106">Il cmdlet **Get-AzureRmSqlDatabaseAdvisor** ottiene uno o più consulenti di database SQL di Azure per un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="84d3e-106">The **Get-AzureRmSqlDatabaseAdvisor** cmdlet gets one or more Azure SQL Database Advisors for an Azure SQL Database.</span></span>

## <span data-ttu-id="84d3e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="84d3e-107">EXAMPLES</span></span>

### <span data-ttu-id="84d3e-108">Esempio 1: elencare tutti gli Advisor per il database specificato</span><span class="sxs-lookup"><span data-stu-id="84d3e-108">Example 1: List all the advisors for the specified database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner"
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

<span data-ttu-id="84d3e-109">Questo comando ottiene elenca tutti gli Advisor per il database denominato WIRunner che appartiene al server denominato Wi-Runner-Australia-Est.</span><span class="sxs-lookup"><span data-stu-id="84d3e-109">This command gets lists all the advisors for the database named WIRunner that belongs to the server named wi-runner-australia-east.</span></span>

### <span data-ttu-id="84d3e-110">Esempio 2: ottenere un singolo consulente per il database specificato</span><span class="sxs-lookup"><span data-stu-id="84d3e-110">Example 2: Get a single advisor for the specified database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex"
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

<span data-ttu-id="84d3e-111">Questo comando consente di ottenere il consulente denominato CreateIndex per il database denominato WIRunner.</span><span class="sxs-lookup"><span data-stu-id="84d3e-111">This command gets the Advisor named CreateIndex for the database named WIRunner.</span></span>

### <span data-ttu-id="84d3e-112">Esempio 3: elencare tutti i consulenti con le azioni consigliate incluse nella risposta</span><span class="sxs-lookup"><span data-stu-id="84d3e-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -ExpandRecommendedActions
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

<span data-ttu-id="84d3e-113">Questo comando consente di ottenere tutti gli Advisor per il database denominato ' WIRunner ' con le azioni consigliate incluse nella risposta.</span><span class="sxs-lookup"><span data-stu-id="84d3e-113">This command gets all the advisors for the database named 'WIRunner' with their recommended actions included in the response.</span></span>
<span data-ttu-id="84d3e-114">Poiché il comando usa il parametro *ExpandRecommendedActions* , il cmdlet ottiene le azioni consigliate con la risposta.</span><span class="sxs-lookup"><span data-stu-id="84d3e-114">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the recommended actions with the response.</span></span>

### <span data-ttu-id="84d3e-115">Esempio 4: ottenere un singolo consulente con le azioni consigliate incluse nella risposta</span><span class="sxs-lookup"><span data-stu-id="84d3e-115">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex" -ExpandRecommendedActions
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

<span data-ttu-id="84d3e-116">Questo comando ottiene il consulente denominato CreateIndex dal database denominato WIRunner con le azioni consigliate incluse nella risposta.</span><span class="sxs-lookup"><span data-stu-id="84d3e-116">This command gets the Advisor named CreateIndex from the database named WIRunner with its recommended actions included in the response.</span></span>
<span data-ttu-id="84d3e-117">Poiché il comando usa il parametro *ExpandRecommendedActions* , il cmdlet ottiene le azioni consigliate con la risposta.</span><span class="sxs-lookup"><span data-stu-id="84d3e-117">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the recommended actions with the response.</span></span>

## <span data-ttu-id="84d3e-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="84d3e-118">PARAMETERS</span></span>

### <span data-ttu-id="84d3e-119">-Advisorname</span><span class="sxs-lookup"><span data-stu-id="84d3e-119">-AdvisorName</span></span>
<span data-ttu-id="84d3e-120">Specifica il nome del consulente ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84d3e-120">Specifies the name of the advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="84d3e-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="84d3e-121">-DatabaseName</span></span>
<span data-ttu-id="84d3e-122">Specifica il nome del database per cui questo cmdlet richiede il consulente.</span><span class="sxs-lookup"><span data-stu-id="84d3e-122">Specifies the name of the database for which this cmdlet requests the Advisor.</span></span>

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

### <span data-ttu-id="84d3e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84d3e-123">-DefaultProfile</span></span>
<span data-ttu-id="84d3e-124">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="84d3e-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="84d3e-125">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="84d3e-125">-ExpandRecommendedActions</span></span>
<span data-ttu-id="84d3e-126">Indica che questo cmdlet ottiene le azioni consigliate con la risposta.</span><span class="sxs-lookup"><span data-stu-id="84d3e-126">Indicates that this cmdlet gets the recommended actions with the response.</span></span>

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

### <span data-ttu-id="84d3e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84d3e-127">-ResourceGroupName</span></span>
<span data-ttu-id="84d3e-128">Specifica il nome del gruppo di risorse del server che contiene il database.</span><span class="sxs-lookup"><span data-stu-id="84d3e-128">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="84d3e-129">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="84d3e-129">-ServerName</span></span>
<span data-ttu-id="84d3e-130">Specifica il nome del server che contiene il database.</span><span class="sxs-lookup"><span data-stu-id="84d3e-130">Specifies the name of the server that contains the database.</span></span>

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

### <span data-ttu-id="84d3e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84d3e-131">CommonParameters</span></span>
<span data-ttu-id="84d3e-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84d3e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84d3e-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84d3e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84d3e-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="84d3e-134">INPUTS</span></span>

### <span data-ttu-id="84d3e-135">System. String</span><span class="sxs-lookup"><span data-stu-id="84d3e-135">System.String</span></span>

### <span data-ttu-id="84d3e-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="84d3e-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="84d3e-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="84d3e-137">OUTPUTS</span></span>

### <span data-ttu-id="84d3e-138">Microsoft. Azure. Commands. SQL. Advisor. Model. AzureSqlDatabaseAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="84d3e-138">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>

## <span data-ttu-id="84d3e-139">Note</span><span class="sxs-lookup"><span data-stu-id="84d3e-139">NOTES</span></span>
* <span data-ttu-id="84d3e-140">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, database, MSSQL, Advisor</span><span class="sxs-lookup"><span data-stu-id="84d3e-140">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor</span></span>

## <span data-ttu-id="84d3e-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="84d3e-141">RELATED LINKS</span></span>

[<span data-ttu-id="84d3e-142">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="84d3e-142">Get-AzureRmSqlServerAdvisor</span></span>](./Get-AzureRmSqlServerAdvisor.md)

[<span data-ttu-id="84d3e-143">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="84d3e-143">Get-AzureRmSqlElasticPoolAdvisor</span></span>](./Get-AzureRmSqlElasticPoolAdvisor.md)

[<span data-ttu-id="84d3e-144">Get-AzureRmSqlDatabaseRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="84d3e-144">Get-AzureRmSqlDatabaseRecommendedAction</span></span>](./Get-AzureRmSqlDatabaseRecommendedAction.md)

[<span data-ttu-id="84d3e-145">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="84d3e-145">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span></span>](./Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="84d3e-146">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="84d3e-146">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
