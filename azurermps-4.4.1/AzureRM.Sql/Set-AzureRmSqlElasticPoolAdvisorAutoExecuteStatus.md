---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BAA0781E-DC02-4AAF-A039-9B71B67E6696
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 5a03216c0a1d507731be75b63277cdd46e3be46d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512804"
---
# <span data-ttu-id="3b4f1-101">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="3b4f1-101">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="3b4f1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3b4f1-102">SYNOPSIS</span></span>
<span data-ttu-id="3b4f1-103">Aggiorna lo stato di esecuzione automatica di un Advisor di Azure SQL Elastic pool.</span><span class="sxs-lookup"><span data-stu-id="3b4f1-103">Updates auto execute status of an Azure SQL Elastic Pool Advisor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b4f1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3b4f1-104">SYNTAX</span></span>

```
Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> -ElasticPoolName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3b4f1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3b4f1-105">DESCRIPTION</span></span>
<span data-ttu-id="3b4f1-106">Il cmdlet **set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus** imposta la proprietà di esecuzione automatica per un consulente di Azure SQL Elastic pool Advisor.</span><span class="sxs-lookup"><span data-stu-id="3b4f1-106">The **Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus** cmdlet sets auto execute property for an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="3b4f1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3b4f1-107">EXAMPLES</span></span>

### <span data-ttu-id="3b4f1-108">Esempio 1: abilitare l'esecuzione automatica per un consulente</span><span class="sxs-lookup"><span data-stu-id="3b4f1-108">Example 1: Enable auto execute for an advisor</span></span>
```
PS C:\>Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
'Enabled'ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Enabled
AutoExecuteStatusInheritedFrom : ElasticPool
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="3b4f1-109">Questo comando imposta lo stato di esecuzione automatica di un consulente denominato CreateIndex su Enabled.</span><span class="sxs-lookup"><span data-stu-id="3b4f1-109">This command sets the auto execute status of an advisor named CreateIndex to enabled.</span></span>

## <span data-ttu-id="3b4f1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3b4f1-110">PARAMETERS</span></span>

### <span data-ttu-id="3b4f1-111">-Advisorname</span><span class="sxs-lookup"><span data-stu-id="3b4f1-111">-AdvisorName</span></span>
<span data-ttu-id="3b4f1-112">Specifica il nome del consulente per il quale questo cmdlet aggiorna lo stato di esecuzione automatica.</span><span class="sxs-lookup"><span data-stu-id="3b4f1-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="3b4f1-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="3b4f1-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="3b4f1-114">Specifica un nuovo valore a cui questo cmdlet aggiorna lo stato di esecuzione automatica.</span><span class="sxs-lookup"><span data-stu-id="3b4f1-114">Specifies a new value to which this cmdlet updates the auto execute status.</span></span>

<span data-ttu-id="3b4f1-115">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="3b4f1-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3b4f1-116">Abilitato</span><span class="sxs-lookup"><span data-stu-id="3b4f1-116">Enabled</span></span>
- <span data-ttu-id="3b4f1-117">Disabilitato</span><span class="sxs-lookup"><span data-stu-id="3b4f1-117">Disabled</span></span>
- <span data-ttu-id="3b4f1-118">Predefinita</span><span class="sxs-lookup"><span data-stu-id="3b4f1-118">Default</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled, Default

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b4f1-119">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="3b4f1-119">-ElasticPoolName</span></span>
<span data-ttu-id="3b4f1-120">Specifica il nome del pool elastico.</span><span class="sxs-lookup"><span data-stu-id="3b4f1-120">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="3b4f1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b4f1-121">-ResourceGroupName</span></span>
<span data-ttu-id="3b4f1-122">Specifica il nome del gruppo di risorse del server che contiene questo pool elastico.</span><span class="sxs-lookup"><span data-stu-id="3b4f1-122">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="3b4f1-123">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="3b4f1-123">-ServerName</span></span>
<span data-ttu-id="3b4f1-124">Specifica il nome del server in cui è presente il pool di elastici.</span><span class="sxs-lookup"><span data-stu-id="3b4f1-124">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="3b4f1-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3b4f1-125">-Confirm</span></span>
<span data-ttu-id="3b4f1-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b4f1-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b4f1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b4f1-127">-WhatIf</span></span>
<span data-ttu-id="3b4f1-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3b4f1-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b4f1-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3b4f1-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b4f1-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b4f1-130">-DefaultProfile</span></span>
<span data-ttu-id="3b4f1-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3b4f1-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b4f1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b4f1-132">CommonParameters</span></span>
<span data-ttu-id="3b4f1-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b4f1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b4f1-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b4f1-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b4f1-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3b4f1-135">INPUTS</span></span>

## <span data-ttu-id="3b4f1-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3b4f1-136">OUTPUTS</span></span>

### <span data-ttu-id="3b4f1-137">Microsoft. Azure. Commands. SQL. Advisor. Model. AzureSqlElasticPoolAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="3b4f1-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span></span>

## <span data-ttu-id="3b4f1-138">Note</span><span class="sxs-lookup"><span data-stu-id="3b4f1-138">NOTES</span></span>
* <span data-ttu-id="3b4f1-139">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Elastic pool, MSSQL, Advisor</span><span class="sxs-lookup"><span data-stu-id="3b4f1-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, elastic pool, mssql, advisor</span></span>

## <span data-ttu-id="3b4f1-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3b4f1-140">RELATED LINKS</span></span>

[<span data-ttu-id="3b4f1-141">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="3b4f1-141">Get-AzureRmSqlElasticPoolAdvisor</span></span>](./Get-AzureRmSqlElasticPoolAdvisor.md)

[<span data-ttu-id="3b4f1-142">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="3b4f1-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
