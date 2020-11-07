---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 6006D3AC-48E1-44A0-8BD5-CE996B8957A2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveradvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 02a4348511afabe7f398eafeb6d0849525f0abac
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864965"
---
# <span data-ttu-id="c9153-101">Set-AzSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="c9153-101">Set-AzSqlServerAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="c9153-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c9153-102">SYNOPSIS</span></span>
<span data-ttu-id="c9153-103">Aggiorna lo stato di esecuzione automatica di un consulente di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c9153-103">Updates the auto execute status of an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="c9153-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c9153-104">SYNTAX</span></span>

```
Set-AzSqlServerAdvisorAutoExecuteStatus -AdvisorName <String> -AutoExecuteStatus <AdvisorAutoExecuteStatus>
 -ServerName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9153-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9153-105">DESCRIPTION</span></span>
<span data-ttu-id="c9153-106">Il cmdlet **set-AzSqlServerAdvisorAutoExecuteStatus** imposta la proprietà di esecuzione automatica per un programma di gestione di SQL Server di Azure.</span><span class="sxs-lookup"><span data-stu-id="c9153-106">The **Set-AzSqlServerAdvisorAutoExecuteStatus** cmdlet sets the auto execute property for an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="c9153-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c9153-107">EXAMPLES</span></span>

### <span data-ttu-id="c9153-108">Esempio 1: abilitare l'esecuzione automatica per un consulente</span><span class="sxs-lookup"><span data-stu-id="c9153-108">Example 1: Enable auto execute for an Advisor</span></span>
```
PS C:\>Set-AzSqlServerAdvisorAutoExecuteStatus -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Enabled
AutoExecuteStatusInheritedFrom : Server
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="c9153-109">Questo comando Abilita lo stato di esecuzione automatica di un consulente denominato CreateIndex.</span><span class="sxs-lookup"><span data-stu-id="c9153-109">This command enables the auto execute status of an Advisor named CreateIndex.</span></span>

## <span data-ttu-id="c9153-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c9153-110">PARAMETERS</span></span>

### <span data-ttu-id="c9153-111">-Advisorname</span><span class="sxs-lookup"><span data-stu-id="c9153-111">-AdvisorName</span></span>
<span data-ttu-id="c9153-112">Specifica il nome del consulente per il quale questo cmdlet aggiorna lo stato di esecuzione automatica.</span><span class="sxs-lookup"><span data-stu-id="c9153-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="c9153-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="c9153-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="c9153-114">Specifica il valore a cui questo cmdlet aggiorna lo stato di esecuzione automatica.</span><span class="sxs-lookup"><span data-stu-id="c9153-114">Specifies the value to which this cmdlet updates the auto execute status.</span></span>
<span data-ttu-id="c9153-115">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c9153-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c9153-116">Abilitato</span><span class="sxs-lookup"><span data-stu-id="c9153-116">Enabled</span></span>
- <span data-ttu-id="c9153-117">Disabilitato</span><span class="sxs-lookup"><span data-stu-id="c9153-117">Disabled</span></span>
- <span data-ttu-id="c9153-118">Predefinita</span><span class="sxs-lookup"><span data-stu-id="c9153-118">Default</span></span>

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

### <span data-ttu-id="c9153-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9153-119">-DefaultProfile</span></span>
<span data-ttu-id="c9153-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c9153-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c9153-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9153-121">-ResourceGroupName</span></span>
<span data-ttu-id="c9153-122">Specifica il nome del gruppo di risorse del server.</span><span class="sxs-lookup"><span data-stu-id="c9153-122">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="c9153-123">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="c9153-123">-ServerName</span></span>
<span data-ttu-id="c9153-124">Specifica il nome del server.</span><span class="sxs-lookup"><span data-stu-id="c9153-124">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="c9153-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c9153-125">-Confirm</span></span>
<span data-ttu-id="c9153-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9153-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9153-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9153-127">-WhatIf</span></span>
<span data-ttu-id="c9153-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c9153-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9153-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c9153-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9153-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9153-130">CommonParameters</span></span>
<span data-ttu-id="c9153-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9153-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9153-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c9153-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9153-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c9153-133">INPUTS</span></span>

### <span data-ttu-id="c9153-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c9153-134">System.String</span></span>

### <span data-ttu-id="c9153-135">Microsoft. Azure. Commands. SQL. Advisor. cmdlet. AdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="c9153-135">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="c9153-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c9153-136">OUTPUTS</span></span>

### <span data-ttu-id="c9153-137">Microsoft. Azure. Commands. SQL. Advisor. Model. AzureSqlServerAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="c9153-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span></span>

## <span data-ttu-id="c9153-138">Note</span><span class="sxs-lookup"><span data-stu-id="c9153-138">NOTES</span></span>
* <span data-ttu-id="c9153-139">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, server, MSSQL, Advisor</span><span class="sxs-lookup"><span data-stu-id="c9153-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span></span>

## <span data-ttu-id="c9153-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c9153-140">RELATED LINKS</span></span>

[<span data-ttu-id="c9153-141">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="c9153-141">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="c9153-142">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="c9153-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
