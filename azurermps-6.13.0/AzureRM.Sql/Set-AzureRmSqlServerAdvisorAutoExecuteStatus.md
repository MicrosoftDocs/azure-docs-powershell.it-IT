---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 6006D3AC-48E1-44A0-8BD5-CE996B8957A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserveradvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 47cbdf20afbae41c9dddc76f45d4065b28067f60
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520132"
---
# <span data-ttu-id="ab115-101">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="ab115-101">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="ab115-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ab115-102">SYNOPSIS</span></span>
<span data-ttu-id="ab115-103">Aggiorna lo stato di esecuzione automatica di un consulente di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ab115-103">Updates the auto execute status of an Azure SQL Server Advisor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab115-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ab115-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab115-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab115-105">DESCRIPTION</span></span>
<span data-ttu-id="ab115-106">Il cmdlet **set-AzureRmSqlServerAdvisorAutoExecuteStatus** imposta la proprietà di esecuzione automatica per un programma di gestione di SQL Server di Azure.</span><span class="sxs-lookup"><span data-stu-id="ab115-106">The **Set-AzureRmSqlServerAdvisorAutoExecuteStatus** cmdlet sets the auto execute property for an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="ab115-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ab115-107">EXAMPLES</span></span>

### <span data-ttu-id="ab115-108">Esempio 1: abilitare l'esecuzione automatica per un consulente</span><span class="sxs-lookup"><span data-stu-id="ab115-108">Example 1: Enable auto execute for an Advisor</span></span>
```
PS C:\>Set-AzureRmSqlServerAdvisorAutoExecuteStatus -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
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

<span data-ttu-id="ab115-109">Questo comando Abilita lo stato di esecuzione automatica di un consulente denominato CreateIndex.</span><span class="sxs-lookup"><span data-stu-id="ab115-109">This command enables the auto execute status of an Advisor named CreateIndex.</span></span>

## <span data-ttu-id="ab115-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ab115-110">PARAMETERS</span></span>

### <span data-ttu-id="ab115-111">-Advisorname</span><span class="sxs-lookup"><span data-stu-id="ab115-111">-AdvisorName</span></span>
<span data-ttu-id="ab115-112">Specifica il nome del consulente per il quale questo cmdlet aggiorna lo stato di esecuzione automatica.</span><span class="sxs-lookup"><span data-stu-id="ab115-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="ab115-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="ab115-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="ab115-114">Specifica il valore a cui questo cmdlet aggiorna lo stato di esecuzione automatica.</span><span class="sxs-lookup"><span data-stu-id="ab115-114">Specifies the value to which this cmdlet updates the auto execute status.</span></span>
<span data-ttu-id="ab115-115">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ab115-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ab115-116">Abilitato</span><span class="sxs-lookup"><span data-stu-id="ab115-116">Enabled</span></span>
- <span data-ttu-id="ab115-117">Disabilitato</span><span class="sxs-lookup"><span data-stu-id="ab115-117">Disabled</span></span>
- <span data-ttu-id="ab115-118">Predefinita</span><span class="sxs-lookup"><span data-stu-id="ab115-118">Default</span></span>

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

### <span data-ttu-id="ab115-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab115-119">-DefaultProfile</span></span>
<span data-ttu-id="ab115-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ab115-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab115-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab115-121">-ResourceGroupName</span></span>
<span data-ttu-id="ab115-122">Specifica il nome del gruppo di risorse del server.</span><span class="sxs-lookup"><span data-stu-id="ab115-122">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="ab115-123">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="ab115-123">-ServerName</span></span>
<span data-ttu-id="ab115-124">Specifica il nome del server.</span><span class="sxs-lookup"><span data-stu-id="ab115-124">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="ab115-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ab115-125">-Confirm</span></span>
<span data-ttu-id="ab115-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab115-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab115-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab115-127">-WhatIf</span></span>
<span data-ttu-id="ab115-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ab115-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab115-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ab115-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab115-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab115-130">CommonParameters</span></span>
<span data-ttu-id="ab115-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab115-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab115-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab115-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab115-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ab115-133">INPUTS</span></span>

### <span data-ttu-id="ab115-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ab115-134">System.String</span></span>

### <span data-ttu-id="ab115-135">Microsoft. Azure. Commands. SQL. Advisor. cmdlet. AdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="ab115-135">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="ab115-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ab115-136">OUTPUTS</span></span>

### <span data-ttu-id="ab115-137">Microsoft. Azure. Commands. SQL. Advisor. Model. AzureSqlServerAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="ab115-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span></span>

## <span data-ttu-id="ab115-138">Note</span><span class="sxs-lookup"><span data-stu-id="ab115-138">NOTES</span></span>
* <span data-ttu-id="ab115-139">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, server, MSSQL, Advisor</span><span class="sxs-lookup"><span data-stu-id="ab115-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span></span>

## <span data-ttu-id="ab115-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ab115-140">RELATED LINKS</span></span>

[<span data-ttu-id="ab115-141">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="ab115-141">Get-AzureRmSqlServerAdvisor</span></span>](./Get-AzureRmSqlServerAdvisor.md)

[<span data-ttu-id="ab115-142">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="ab115-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
