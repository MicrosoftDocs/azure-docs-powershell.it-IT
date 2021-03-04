---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BC8C0D59-662F-47D2-8619-9F69D78B171D
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlelasticpooladvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolAdvisor.md
ms.openlocfilehash: 9c9a6b2b95f5126ecdc214db2227c46b01c5725c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999534"
---
# <span data-ttu-id="5844b-101">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="5844b-101">Get-AzSqlElasticPoolAdvisor</span></span>

## <span data-ttu-id="5844b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5844b-102">SYNOPSIS</span></span>
<span data-ttu-id="5844b-103">Ottiene uno o più consulenti per un pool di SQL azure.</span><span class="sxs-lookup"><span data-stu-id="5844b-103">Gets one or more Advisors for an Azure SQL Elastic Pool.</span></span>

## <span data-ttu-id="5844b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5844b-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 -ElasticPoolName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5844b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5844b-105">DESCRIPTION</span></span>
<span data-ttu-id="5844b-106">Il cmdlet **Get-AzSqlElasticPoolAdvisor** ottiene uno o più consulenti del pool di SQL elastici di Azure per un pool SQL flessibile di Azure.</span><span class="sxs-lookup"><span data-stu-id="5844b-106">The **Get-AzSqlElasticPoolAdvisor** cmdlet gets one or more Azure SQL Elastic Pool Advisors for an Azure SQL Elastic Pool.</span></span>

## <span data-ttu-id="5844b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5844b-107">EXAMPLES</span></span>

### <span data-ttu-id="5844b-108">Esempio 1: Elencare tutti gli consulenti per il pool di elastico specificato</span><span class="sxs-lookup"><span data-stu-id="5844b-108">Example 1: List all the advisors for the specified elastic pool</span></span>
```
PS C:\>Get-AzSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool"
ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}

ElasticPoolName                : WIRunnerPool
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

<span data-ttu-id="5844b-109">Il comando ottiene l'elenco di tutti gli consulenti per il pool elastico denominato WIRunnerPool.</span><span class="sxs-lookup"><span data-stu-id="5844b-109">The command gets lists all the advisors for the elastic pool named WIRunnerPool.</span></span>

### <span data-ttu-id="5844b-110">Esempio 2: Ottenere un singolo consulente per il pool di elastici specificato</span><span class="sxs-lookup"><span data-stu-id="5844b-110">Example 2: Get a single advisor for the specified elastic pool</span></span>
```
PS C:\>Get-AzSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex"
ElasticPoolName                : WIRunnerPool
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

<span data-ttu-id="5844b-111">Questo comando recupera l'advisor denominato CreateIndex per il pool di elastici denominato WIRunnerPool.</span><span class="sxs-lookup"><span data-stu-id="5844b-111">This command gets the Advisor named CreateIndex for the elastic pool named WIRunnerPool.</span></span>

### <span data-ttu-id="5844b-112">Esempio 3: Elencare tutti i consulenti con le azioni consigliate incluse nella risposta</span><span class="sxs-lookup"><span data-stu-id="5844b-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
```
PS C:\>Get-AzSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -ExpandRecommendedActions
ElasticPoolName                : WIRunnerPool
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

ElasticPoolName                : WIRunnerPool
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

ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}

ElasticPoolName                : WIRunnerPool
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

<span data-ttu-id="5844b-113">Questo comando include tutti gli consulenti per il pool elastico con le azioni consigliate incluse nella risposta.</span><span class="sxs-lookup"><span data-stu-id="5844b-113">This command gets all the advisors for the elastic pool with their recommended actions included in the response.</span></span>

### <span data-ttu-id="5844b-114">Esempio 4: Ottenere un singolo consulente con le azioni consigliate incluse nella risposta</span><span class="sxs-lookup"><span data-stu-id="5844b-114">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
```
PS C:\>Get-AzSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -ExpandRecommendedActions
ElasticPoolName                : WIRunnerPool
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

<span data-ttu-id="5844b-115">Questo comando ottiene il comando denominato CreateIndex dal server denominato wi-runner-australia-east con le azioni consigliate incluse nella risposta.</span><span class="sxs-lookup"><span data-stu-id="5844b-115">This command gets advisor named CreateIndex from the server named wi-runner-australia-east with its recommended actions included in the response.</span></span>

### <span data-ttu-id="5844b-116">Esempio 5: Elencare tutti gli consulenti per il pool flessibile specificato usando i filtri</span><span class="sxs-lookup"><span data-stu-id="5844b-116">Example 5: List all the advisors for the specified elastic pool using filtering</span></span>
```
PS C:\>Get-AzSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName d*
ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

ElasticPoolName                : WIRunnerPool
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

<span data-ttu-id="5844b-117">Il comando ottiene l'elenco di tutti gli consulenti per il pool flessibile denominato WIRunnerPool che iniziano con la lettera "d".</span><span class="sxs-lookup"><span data-stu-id="5844b-117">The command gets lists all the advisors for the elastic pool named WIRunnerPool that start with the letter "d".</span></span>

## <span data-ttu-id="5844b-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5844b-118">PARAMETERS</span></span>

### <span data-ttu-id="5844b-119">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="5844b-119">-AdvisorName</span></span>
<span data-ttu-id="5844b-120">Specifica il nome dell'consulente che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5844b-120">Specifies the name of the Advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5844b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5844b-121">-DefaultProfile</span></span>
<span data-ttu-id="5844b-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5844b-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5844b-123">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="5844b-123">-ElasticPoolName</span></span>
<span data-ttu-id="5844b-124">Specifica il nome del pool flessibile per cui questo cmdlet richiede l'advisor.</span><span class="sxs-lookup"><span data-stu-id="5844b-124">Specifies the name of the elastic pool for which this cmdlet requests the Advisor.</span></span>

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

### <span data-ttu-id="5844b-125">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="5844b-125">-ExpandRecommendedActions</span></span>
<span data-ttu-id="5844b-126">Indica che il cmdlet include le azioni consigliate dell'consulente nella risposta.</span><span class="sxs-lookup"><span data-stu-id="5844b-126">Indicates that the cmdlet includes the recommended actions of the Advisor in the response.</span></span>

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

### <span data-ttu-id="5844b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5844b-127">-ResourceGroupName</span></span>
<span data-ttu-id="5844b-128">Specifica il nome del gruppo di risorse del server che contiene questo pool flessibile.</span><span class="sxs-lookup"><span data-stu-id="5844b-128">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="5844b-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5844b-129">-ServerName</span></span>
<span data-ttu-id="5844b-130">Specifica il nome del server in cui si trova il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="5844b-130">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="5844b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5844b-131">CommonParameters</span></span>
<span data-ttu-id="5844b-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5844b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5844b-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5844b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5844b-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="5844b-134">INPUTS</span></span>

### <span data-ttu-id="5844b-135">System.String</span><span class="sxs-lookup"><span data-stu-id="5844b-135">System.String</span></span>

### <span data-ttu-id="5844b-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5844b-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5844b-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5844b-137">OUTPUTS</span></span>

### <span data-ttu-id="5844b-138">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="5844b-138">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span></span>

## <span data-ttu-id="5844b-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="5844b-139">NOTES</span></span>
* <span data-ttu-id="5844b-140">Parole chiave: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor</span><span class="sxs-lookup"><span data-stu-id="5844b-140">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor</span></span>

## <span data-ttu-id="5844b-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5844b-141">RELATED LINKS</span></span>

[<span data-ttu-id="5844b-142">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="5844b-142">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="5844b-143">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="5844b-143">Get-AzSqlDatabaseAdvisor</span></span>](./Get-AzSqlDatabaseAdvisor.md)

[<span data-ttu-id="5844b-144">Get-AzSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="5844b-144">Get-AzSqlElasticPoolRecommendedAction</span></span>](./Get-AzSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="5844b-145">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="5844b-145">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="5844b-146">documentazione SQL database</span><span class="sxs-lookup"><span data-stu-id="5844b-146">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
