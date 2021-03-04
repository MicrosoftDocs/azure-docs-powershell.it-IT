---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BAA0781E-DC02-4AAF-A039-9B71B67E6696
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlelasticpooladvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md
ms.openlocfilehash: aa181dcb171a1842c2b6158078e60b717b33d579
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952989"
---
# <span data-ttu-id="01b04-101">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="01b04-101">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="01b04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01b04-102">SYNOPSIS</span></span>
<span data-ttu-id="01b04-103">Stato di esecuzione automatica degli aggiornamenti di un consulente SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="01b04-103">Updates auto execute status of an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="01b04-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="01b04-104">SYNTAX</span></span>

```
Set-AzSqlElasticPoolAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> -ElasticPoolName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="01b04-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="01b04-105">DESCRIPTION</span></span>
<span data-ttu-id="01b04-106">Il cmdlet **Set-AzSqlElasticPoolAdvisorAutoExecuteStatus** imposta la proprietà di esecuzione automatica per un consulente SQL pool flessibile di Azure.</span><span class="sxs-lookup"><span data-stu-id="01b04-106">The **Set-AzSqlElasticPoolAdvisorAutoExecuteStatus** cmdlet sets auto execute property for an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="01b04-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="01b04-107">EXAMPLES</span></span>

### <span data-ttu-id="01b04-108">Esempio 1: Abilitare l'esecuzione automatica per un consulente</span><span class="sxs-lookup"><span data-stu-id="01b04-108">Example 1: Enable auto execute for an advisor</span></span>
```
PS C:\>Set-AzSqlElasticPoolAdvisorAutoExecuteStatus -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
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

<span data-ttu-id="01b04-109">Questo comando imposta lo stato di esecuzione automatica di un consulente denominato CreateIndex su abilitato.</span><span class="sxs-lookup"><span data-stu-id="01b04-109">This command sets the auto execute status of an advisor named CreateIndex to enabled.</span></span>

## <span data-ttu-id="01b04-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01b04-110">PARAMETERS</span></span>

### <span data-ttu-id="01b04-111">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="01b04-111">-AdvisorName</span></span>
<span data-ttu-id="01b04-112">Specifica il nome dell'consulente per cui questo cmdlet aggiorna lo stato di esecuzione automatica.</span><span class="sxs-lookup"><span data-stu-id="01b04-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="01b04-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="01b04-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="01b04-114">Specifica un nuovo valore a cui questo cmdlet aggiorna lo stato di esecuzione automatica.</span><span class="sxs-lookup"><span data-stu-id="01b04-114">Specifies a new value to which this cmdlet updates the auto execute status.</span></span>
<span data-ttu-id="01b04-115">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="01b04-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="01b04-116">Abilitato</span><span class="sxs-lookup"><span data-stu-id="01b04-116">Enabled</span></span>
- <span data-ttu-id="01b04-117">Disabilitato</span><span class="sxs-lookup"><span data-stu-id="01b04-117">Disabled</span></span>
- <span data-ttu-id="01b04-118">Impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="01b04-118">Default</span></span>

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

### <span data-ttu-id="01b04-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01b04-119">-DefaultProfile</span></span>
<span data-ttu-id="01b04-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="01b04-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="01b04-121">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="01b04-121">-ElasticPoolName</span></span>
<span data-ttu-id="01b04-122">Specifica il nome del pool elastico.</span><span class="sxs-lookup"><span data-stu-id="01b04-122">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="01b04-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01b04-123">-ResourceGroupName</span></span>
<span data-ttu-id="01b04-124">Specifica il nome del gruppo di risorse del server che contiene questo pool flessibile.</span><span class="sxs-lookup"><span data-stu-id="01b04-124">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="01b04-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="01b04-125">-ServerName</span></span>
<span data-ttu-id="01b04-126">Specifica il nome del server in cui si trova il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="01b04-126">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="01b04-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01b04-127">-Confirm</span></span>
<span data-ttu-id="01b04-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01b04-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01b04-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01b04-129">-WhatIf</span></span>
<span data-ttu-id="01b04-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="01b04-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01b04-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="01b04-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01b04-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01b04-132">CommonParameters</span></span>
<span data-ttu-id="01b04-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01b04-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01b04-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="01b04-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01b04-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="01b04-135">INPUTS</span></span>

### <span data-ttu-id="01b04-136">System.String</span><span class="sxs-lookup"><span data-stu-id="01b04-136">System.String</span></span>

### <span data-ttu-id="01b04-137">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="01b04-137">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="01b04-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="01b04-138">OUTPUTS</span></span>

### <span data-ttu-id="01b04-139">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="01b04-139">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span></span>

## <span data-ttu-id="01b04-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="01b04-140">NOTES</span></span>
* <span data-ttu-id="01b04-141">Parole chiave: azure, azurerm, arm, resource, management, manager, sql, elastic pool, mssql, advisor</span><span class="sxs-lookup"><span data-stu-id="01b04-141">Keywords: azure, azurerm, arm, resource, management, manager, sql, elastic pool, mssql, advisor</span></span>

## <span data-ttu-id="01b04-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="01b04-142">RELATED LINKS</span></span>

[<span data-ttu-id="01b04-143">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="01b04-143">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="01b04-144">documentazione SQL database</span><span class="sxs-lookup"><span data-stu-id="01b04-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
