---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BC8C0D59-662F-47D2-8619-9F69D78B171D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlelasticpooladvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolAdvisor.md
ms.openlocfilehash: f6b8fba0fd629493fdd848708db009e09c86e417
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519674"
---
# <span data-ttu-id="30e62-101">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="30e62-101">Get-AzureRmSqlElasticPoolAdvisor</span></span>

## <span data-ttu-id="30e62-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="30e62-102">SYNOPSIS</span></span>
<span data-ttu-id="30e62-103">Ottiene uno o più consulenti per un pool elastico di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="30e62-103">Gets one or more Advisors for an Azure SQL Elastic Pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30e62-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="30e62-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 -ElasticPoolName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="30e62-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="30e62-105">DESCRIPTION</span></span>
<span data-ttu-id="30e62-106">Il cmdlet **Get-AzureRmSqlElasticPoolAdvisor** ottiene uno o più consulenti di Azure SQL Elastic pool Advisor per un pool di Azure SQL Elastic.</span><span class="sxs-lookup"><span data-stu-id="30e62-106">The **Get-AzureRmSqlElasticPoolAdvisor** cmdlet gets one or more Azure SQL Elastic Pool Advisors for an Azure SQL Elastic Pool.</span></span>

## <span data-ttu-id="30e62-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="30e62-107">EXAMPLES</span></span>

### <span data-ttu-id="30e62-108">Esempio 1: elencare tutti gli Advisor per il pool elastico specificato</span><span class="sxs-lookup"><span data-stu-id="30e62-108">Example 1: List all the advisors for the specified elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -PoolName "WIRunnerPool"
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

<span data-ttu-id="30e62-109">Il comando ottiene elenca tutti gli Advisor per il pool elastico denominato WIRunnerPool.</span><span class="sxs-lookup"><span data-stu-id="30e62-109">The command gets lists all the advisors for the elastic pool named WIRunnerPool.</span></span>

### <span data-ttu-id="30e62-110">Esempio 2: ottenere un singolo consulente per il pool elastico specificato</span><span class="sxs-lookup"><span data-stu-id="30e62-110">Example 2: Get a single advisor for the specified elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex"
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

<span data-ttu-id="30e62-111">Questo comando consente di ottenere il consulente denominato CreateIndex per il pool elastico denominato WIRunnerPool.</span><span class="sxs-lookup"><span data-stu-id="30e62-111">This command gets the Advisor named CreateIndex for the elastic pool named WIRunnerPool.</span></span>

### <span data-ttu-id="30e62-112">Esempio 3: elencare tutti i consulenti con le azioni consigliate incluse nella risposta</span><span class="sxs-lookup"><span data-stu-id="30e62-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -ExpandRecommendedActions
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

<span data-ttu-id="30e62-113">Questo comando consente di ottenere tutti gli Advisor per il pool elastico con le azioni consigliate incluse nella risposta.</span><span class="sxs-lookup"><span data-stu-id="30e62-113">This command gets all the advisors for the elastic pool with their recommended actions included in the response.</span></span>

### <span data-ttu-id="30e62-114">Esempio 4: ottenere un singolo consulente con le azioni consigliate incluse nella risposta</span><span class="sxs-lookup"><span data-stu-id="30e62-114">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -ExpandRecommendedActions
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

<span data-ttu-id="30e62-115">Questo comando ottiene Advisor denominato CreateIndex dal server denominato Wi-Runner-Australia-East con le azioni consigliate incluse nella risposta.</span><span class="sxs-lookup"><span data-stu-id="30e62-115">This command gets advisor named CreateIndex from the server named wi-runner-australia-east with its recommended actions included in the response.</span></span>

## <span data-ttu-id="30e62-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="30e62-116">PARAMETERS</span></span>

### <span data-ttu-id="30e62-117">-Advisorname</span><span class="sxs-lookup"><span data-stu-id="30e62-117">-AdvisorName</span></span>
<span data-ttu-id="30e62-118">Specifica il nome del consulente ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30e62-118">Specifies the name of the Advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="30e62-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30e62-119">-DefaultProfile</span></span>
<span data-ttu-id="30e62-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="30e62-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="30e62-121">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="30e62-121">-ElasticPoolName</span></span>
<span data-ttu-id="30e62-122">Specifica il nome del pool elastico per il quale questo cmdlet richiede il consulente.</span><span class="sxs-lookup"><span data-stu-id="30e62-122">Specifies the name of the elastic pool for which this cmdlet requests the Advisor.</span></span>

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

### <span data-ttu-id="30e62-123">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="30e62-123">-ExpandRecommendedActions</span></span>
<span data-ttu-id="30e62-124">Indica che il cmdlet include le azioni consigliate del consulente nella risposta.</span><span class="sxs-lookup"><span data-stu-id="30e62-124">Indicates that the cmdlet includes the recommended actions of the Advisor in the response.</span></span>

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

### <span data-ttu-id="30e62-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30e62-125">-ResourceGroupName</span></span>
<span data-ttu-id="30e62-126">Specifica il nome del gruppo di risorse del server che contiene questo pool elastico.</span><span class="sxs-lookup"><span data-stu-id="30e62-126">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="30e62-127">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="30e62-127">-ServerName</span></span>
<span data-ttu-id="30e62-128">Specifica il nome del server in cui è presente il pool di elastici.</span><span class="sxs-lookup"><span data-stu-id="30e62-128">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="30e62-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30e62-129">CommonParameters</span></span>
<span data-ttu-id="30e62-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30e62-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30e62-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30e62-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30e62-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="30e62-132">INPUTS</span></span>

### <span data-ttu-id="30e62-133">System. String</span><span class="sxs-lookup"><span data-stu-id="30e62-133">System.String</span></span>

### <span data-ttu-id="30e62-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="30e62-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="30e62-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="30e62-135">OUTPUTS</span></span>

### <span data-ttu-id="30e62-136">Microsoft. Azure. Commands. SQL. Advisor. Model. AzureSqlElasticPoolAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="30e62-136">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span></span>

## <span data-ttu-id="30e62-137">Note</span><span class="sxs-lookup"><span data-stu-id="30e62-137">NOTES</span></span>
* <span data-ttu-id="30e62-138">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, elasticpool, MSSQL, Advisor</span><span class="sxs-lookup"><span data-stu-id="30e62-138">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor</span></span>

## <span data-ttu-id="30e62-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="30e62-139">RELATED LINKS</span></span>

[<span data-ttu-id="30e62-140">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="30e62-140">Get-AzureRmSqlServerAdvisor</span></span>](./Get-AzureRmSqlServerAdvisor.md)

[<span data-ttu-id="30e62-141">Get-AzureRmSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="30e62-141">Get-AzureRmSqlDatabaseAdvisor</span></span>](./Get-AzureRmSqlDatabaseAdvisor.md)

[<span data-ttu-id="30e62-142">Get-AzureRmSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="30e62-142">Get-AzureRmSqlElasticPoolRecommendedAction</span></span>](./Get-AzureRmSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="30e62-143">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="30e62-143">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="30e62-144">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="30e62-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)