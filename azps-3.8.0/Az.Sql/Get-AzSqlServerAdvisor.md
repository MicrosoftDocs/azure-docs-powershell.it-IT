---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: DAEF11C1-281B-4BED-9283-2296E0B57018
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveradvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvisor.md
ms.openlocfilehash: 1d487c4397d1a7c29f0b415ee973d01e4dc6f1a1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022213"
---
# <span data-ttu-id="62cf9-101">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="62cf9-101">Get-AzSqlServerAdvisor</span></span>

## <span data-ttu-id="62cf9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="62cf9-102">SYNOPSIS</span></span>
<span data-ttu-id="62cf9-103">Ottiene uno o più consulenti per un server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="62cf9-103">Gets one or more Advisors for an Azure SQL Server.</span></span>

## <span data-ttu-id="62cf9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="62cf9-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62cf9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="62cf9-105">DESCRIPTION</span></span>
<span data-ttu-id="62cf9-106">Il cmdlet **Get-AzSqlServerAdvisor** ottiene uno o più consulenti di SQL Server di Azure per un server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="62cf9-106">The **Get-AzSqlServerAdvisor** cmdlet gets one or more Azure SQL Server Advisors for an Azure SQL Server.</span></span>

## <span data-ttu-id="62cf9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="62cf9-107">EXAMPLES</span></span>

### <span data-ttu-id="62cf9-108">Esempio 1: elencare tutti i consulenti per il server</span><span class="sxs-lookup"><span data-stu-id="62cf9-108">Example 1: List all the advisors for the server</span></span>
```
PS C:\> Get-AzSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east"
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}

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

<span data-ttu-id="62cf9-109">Questo comando consente di ottenere un elenco di tutti gli Advisor per il server denominato Wi-Runner-Australia-Est appartenente al gruppo di risorse denominato WIRunnersProd.</span><span class="sxs-lookup"><span data-stu-id="62cf9-109">This command gets a list of all the advisors for the server named wi-runner-australia-east that belongs to the resource group named WIRunnersProd.</span></span>

### <span data-ttu-id="62cf9-110">Esempio 2: ottenere un singolo consulente per il server</span><span class="sxs-lookup"><span data-stu-id="62cf9-110">Example 2: Get a single advisor for the server</span></span>
```
PS C:\> Get-AzSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex"
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

<span data-ttu-id="62cf9-111">Questo comando ottiene il consulente denominato CreateIndex per il server denominato Wi-Runner-Australia-Est.</span><span class="sxs-lookup"><span data-stu-id="62cf9-111">This command gets the advisor named CreateIndex for the server named wi-runner-australia-east.</span></span>

### <span data-ttu-id="62cf9-112">Esempio 3: elencare tutti i consulenti con le azioni consigliate incluse nella risposta</span><span class="sxs-lookup"><span data-stu-id="62cf9-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
```
PS C:\>Get-AzSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ExpandRecommendedActions
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

ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}
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

<span data-ttu-id="62cf9-113">Questo comando consente di ottenere tutti gli Advisor per il server denominato Wi-Runner-Australia-Est.</span><span class="sxs-lookup"><span data-stu-id="62cf9-113">This command gets all the advisors for the server named wi-runner-australia-east.</span></span>
<span data-ttu-id="62cf9-114">Poiché il comando usa il parametro *ExpandRecommendedActions* , il cmdlet ottiene le azioni consigliate per i consulenti inclusi nella risposta.</span><span class="sxs-lookup"><span data-stu-id="62cf9-114">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the advisors recommended actions included in the response.</span></span>

### <span data-ttu-id="62cf9-115">Esempio 4: ottenere un singolo consulente con le azioni consigliate incluse nella risposta</span><span class="sxs-lookup"><span data-stu-id="62cf9-115">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
```
PS C:\> Get-AzSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -ExpandRecommendedActions
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

<span data-ttu-id="62cf9-116">Questo comando ottiene Advisor denominato CreateIndex dal server denominato Wi-Runner-Australia-East con le azioni consigliate incluse nella risposta.</span><span class="sxs-lookup"><span data-stu-id="62cf9-116">This command gets advisor named CreateIndex from the server named wi-runner-australia-east with its recommended actions included in the response.</span></span>

### <span data-ttu-id="62cf9-117">Esempio 5: elencare tutti i consulenti per il server tramite filtro</span><span class="sxs-lookup"><span data-stu-id="62cf9-117">Example 5: List all the advisors for the server using filtering</span></span>
```
PS C:\> Get-AzSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName d*
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

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

<span data-ttu-id="62cf9-118">Questo comando consente di ottenere un elenco di tutti gli Advisor per il server denominato Wi-Runner-Australia-Est che appartiene al gruppo di risorse denominato WIRunnersProd che inizia con la lettera "d".</span><span class="sxs-lookup"><span data-stu-id="62cf9-118">This command gets a list of all the advisors for the server named wi-runner-australia-east that belongs to the resource group named WIRunnersProd that start with the letter "d".</span></span>

## <span data-ttu-id="62cf9-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="62cf9-119">PARAMETERS</span></span>

### <span data-ttu-id="62cf9-120">-Advisorname</span><span class="sxs-lookup"><span data-stu-id="62cf9-120">-AdvisorName</span></span>
<span data-ttu-id="62cf9-121">Specifica il nome del consulente ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62cf9-121">Specifies the name of the advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="62cf9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62cf9-122">-DefaultProfile</span></span>
<span data-ttu-id="62cf9-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="62cf9-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62cf9-124">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="62cf9-124">-ExpandRecommendedActions</span></span>
<span data-ttu-id="62cf9-125">Indica che il cmdlet include le azioni consigliate dei consulenti inclusi nella risposta.</span><span class="sxs-lookup"><span data-stu-id="62cf9-125">Indicates that the cmdlet includes the recommended actions of the advisors that are included in the response.</span></span>

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

### <span data-ttu-id="62cf9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62cf9-126">-ResourceGroupName</span></span>
<span data-ttu-id="62cf9-127">Specifica il nome del gruppo di risorse del server.</span><span class="sxs-lookup"><span data-stu-id="62cf9-127">Specifies name of the resource group of the server.</span></span>

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

### <span data-ttu-id="62cf9-128">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="62cf9-128">-ServerName</span></span>
<span data-ttu-id="62cf9-129">Specifica il nome del server per il consulente richiesto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62cf9-129">Specifies the name of the server for the advisor that this cmdlet requests.</span></span>

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

### <span data-ttu-id="62cf9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62cf9-130">CommonParameters</span></span>
<span data-ttu-id="62cf9-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62cf9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62cf9-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="62cf9-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62cf9-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="62cf9-133">INPUTS</span></span>

### <span data-ttu-id="62cf9-134">System. String</span><span class="sxs-lookup"><span data-stu-id="62cf9-134">System.String</span></span>

### <span data-ttu-id="62cf9-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="62cf9-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="62cf9-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="62cf9-136">OUTPUTS</span></span>

### <span data-ttu-id="62cf9-137">Microsoft. Azure. Commands. SQL. Advisor. Model. AzureSqlServerAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="62cf9-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span></span>

## <span data-ttu-id="62cf9-138">Note</span><span class="sxs-lookup"><span data-stu-id="62cf9-138">NOTES</span></span>
* <span data-ttu-id="62cf9-139">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, server, MSSQL, Advisor</span><span class="sxs-lookup"><span data-stu-id="62cf9-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span></span>

## <span data-ttu-id="62cf9-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="62cf9-140">RELATED LINKS</span></span>

[<span data-ttu-id="62cf9-141">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="62cf9-141">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="62cf9-142">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="62cf9-142">Get-AzSqlDatabaseAdvisor</span></span>](./Get-AzSqlDatabaseAdvisor.md)

[<span data-ttu-id="62cf9-143">Get-AzSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="62cf9-143">Get-AzSqlServerRecommendedAction</span></span>](./Get-AzSqlServerRecommendedAction.md)

[<span data-ttu-id="62cf9-144">Set-AzSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="62cf9-144">Set-AzSqlServerAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlServerAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="62cf9-145">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="62cf9-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

