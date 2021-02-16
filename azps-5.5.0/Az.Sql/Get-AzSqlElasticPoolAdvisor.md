---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BC8C0D59-662F-47D2-8619-9F69D78B171D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpooladvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolAdvisor.md
ms.openlocfilehash: 3032824d51e7892c21830decbdb1c92d03d7a2e1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209219"
---
# <span data-ttu-id="1f6a0-101">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="1f6a0-101">Get-AzSqlElasticPoolAdvisor</span></span>

## <span data-ttu-id="1f6a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f6a0-102">SYNOPSIS</span></span>
<span data-ttu-id="1f6a0-103">Ottiene uno o più consulenti per un pool di SQL azure.</span><span class="sxs-lookup"><span data-stu-id="1f6a0-103">Gets one or more Advisors for an Azure SQL Elastic Pool.</span></span>

## <span data-ttu-id="1f6a0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1f6a0-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 -ElasticPoolName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1f6a0-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1f6a0-105">DESCRIPTION</span></span>
<span data-ttu-id="1f6a0-106">Il cmdlet **Get-AzSqlElasticPoolAdvisor** ottiene uno o più consulenti del pool di SQL elastici di Azure per un pool SQL flessibile di Azure.</span><span class="sxs-lookup"><span data-stu-id="1f6a0-106">The **Get-AzSqlElasticPoolAdvisor** cmdlet gets one or more Azure SQL Elastic Pool Advisors for an Azure SQL Elastic Pool.</span></span>

## <span data-ttu-id="1f6a0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1f6a0-107">EXAMPLES</span></span>

### <span data-ttu-id="1f6a0-108">Esempio 1: Elencare tutti gli consulenti per il pool di elastico specificato</span><span class="sxs-lookup"><span data-stu-id="1f6a0-108">Example 1: List all the advisors for the specified elastic pool</span></span>
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

<span data-ttu-id="1f6a0-109">Il comando ottiene l'elenco di tutti gli consulenti per il pool elastico denominato WIRunnerPool.</span><span class="sxs-lookup"><span data-stu-id="1f6a0-109">The command gets lists all the advisors for the elastic pool named WIRunnerPool.</span></span>

### <span data-ttu-id="1f6a0-110">Esempio 2: Ottenere un singolo consulente per il pool di elastici specificato</span><span class="sxs-lookup"><span data-stu-id="1f6a0-110">Example 2: Get a single advisor for the specified elastic pool</span></span>
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

<span data-ttu-id="1f6a0-111">Questo comando recupera l'advisor denominato CreateIndex per il pool di elastici denominato WIRunnerPool.</span><span class="sxs-lookup"><span data-stu-id="1f6a0-111">This command gets the Advisor named CreateIndex for the elastic pool named WIRunnerPool.</span></span>

### <span data-ttu-id="1f6a0-112">Esempio 3: Elencare tutti gli consulenti con le azioni consigliate incluse nella risposta</span><span class="sxs-lookup"><span data-stu-id="1f6a0-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
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

<span data-ttu-id="1f6a0-113">Questo comando include tutti gli consulenti per il pool elastico con le azioni consigliate incluse nella risposta.</span><span class="sxs-lookup"><span data-stu-id="1f6a0-113">This command gets all the advisors for the elastic pool with their recommended actions included in the response.</span></span>

### <span data-ttu-id="1f6a0-114">Esempio 4: Ottenere un consulente con le azioni consigliate incluse nella risposta</span><span class="sxs-lookup"><span data-stu-id="1f6a0-114">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
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

<span data-ttu-id="1f6a0-115">Questo comando ottiene il comando denominato CreateIndex dal server denominato wi-runner-australia-east con le azioni consigliate incluse nella risposta.</span><span class="sxs-lookup"><span data-stu-id="1f6a0-115">This command gets advisor named CreateIndex from the server named wi-runner-australia-east with its recommended actions included in the response.</span></span>

### <span data-ttu-id="1f6a0-116">Esempio 5: Elencare tutti gli consulenti per il pool flessibile specificato usando i filtri</span><span class="sxs-lookup"><span data-stu-id="1f6a0-116">Example 5: List all the advisors for the specified elastic pool using filtering</span></span>
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

<span data-ttu-id="1f6a0-117">Il comando ottiene l'elenco di tutti gli consulenti per il pool elastico denominato WIRunnerPool che iniziano con la lettera "d".</span><span class="sxs-lookup"><span data-stu-id="1f6a0-117">The command gets lists all the advisors for the elastic pool named WIRunnerPool that start with the letter "d".</span></span>

## <span data-ttu-id="1f6a0-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f6a0-118">PARAMETERS</span></span>

### <span data-ttu-id="1f6a0-119">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="1f6a0-119">-AdvisorName</span></span>
<span data-ttu-id="1f6a0-120">Specifica il nome dell'consulente che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f6a0-120">Specifies the name of the Advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1f6a0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f6a0-121">-DefaultProfile</span></span>
<span data-ttu-id="1f6a0-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="1f6a0-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f6a0-123">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="1f6a0-123">-ElasticPoolName</span></span>
<span data-ttu-id="1f6a0-124">Specifica il nome del pool flessibile per cui questo cmdlet richiede l'advisor.</span><span class="sxs-lookup"><span data-stu-id="1f6a0-124">Specifies the name of the elastic pool for which this cmdlet requests the Advisor.</span></span>

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

### <span data-ttu-id="1f6a0-125">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="1f6a0-125">-ExpandRecommendedActions</span></span>
<span data-ttu-id="1f6a0-126">Indica che il cmdlet include le azioni consigliate dell'consulente nella risposta.</span><span class="sxs-lookup"><span data-stu-id="1f6a0-126">Indicates that the cmdlet includes the recommended actions of the Advisor in the response.</span></span>

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

### <span data-ttu-id="1f6a0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f6a0-127">-ResourceGroupName</span></span>
<span data-ttu-id="1f6a0-128">Specifica il nome del gruppo di risorse del server che contiene questo pool flessibile.</span><span class="sxs-lookup"><span data-stu-id="1f6a0-128">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="1f6a0-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1f6a0-129">-ServerName</span></span>
<span data-ttu-id="1f6a0-130">Specifica il nome del server in cui si trova il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="1f6a0-130">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="1f6a0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f6a0-131">CommonParameters</span></span>
<span data-ttu-id="1f6a0-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f6a0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f6a0-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1f6a0-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f6a0-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="1f6a0-134">INPUTS</span></span>

### <span data-ttu-id="1f6a0-135">System.String</span><span class="sxs-lookup"><span data-stu-id="1f6a0-135">System.String</span></span>

### <span data-ttu-id="1f6a0-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1f6a0-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1f6a0-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1f6a0-137">OUTPUTS</span></span>

### <span data-ttu-id="1f6a0-138">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="1f6a0-138">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span></span>

## <span data-ttu-id="1f6a0-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="1f6a0-139">NOTES</span></span>
* <span data-ttu-id="1f6a0-140">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, sql, elasticpool, mssql, advisor</span><span class="sxs-lookup"><span data-stu-id="1f6a0-140">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor</span></span>

## <span data-ttu-id="1f6a0-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1f6a0-141">RELATED LINKS</span></span>

[<span data-ttu-id="1f6a0-142">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="1f6a0-142">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="1f6a0-143">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="1f6a0-143">Get-AzSqlDatabaseAdvisor</span></span>](./Get-AzSqlDatabaseAdvisor.md)

[<span data-ttu-id="1f6a0-144">Get-AzSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="1f6a0-144">Get-AzSqlElasticPoolRecommendedAction</span></span>](./Get-AzSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="1f6a0-145">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="1f6a0-145">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="1f6a0-146">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="1f6a0-146">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
