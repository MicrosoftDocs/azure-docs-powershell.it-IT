---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 6006D3AC-48E1-44A0-8BD5-CE996B8957A2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveradvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 02a4348511afabe7f398eafeb6d0849525f0abac
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195918"
---
# <span data-ttu-id="1cb45-101">Set-AzSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="1cb45-101">Set-AzSqlServerAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="1cb45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cb45-102">SYNOPSIS</span></span>
<span data-ttu-id="1cb45-103">Aggiorna lo stato di esecuzione automatica di un avviso SQL Server azure.</span><span class="sxs-lookup"><span data-stu-id="1cb45-103">Updates the auto execute status of an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="1cb45-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1cb45-104">SYNTAX</span></span>

```
Set-AzSqlServerAdvisorAutoExecuteStatus -AdvisorName <String> -AutoExecuteStatus <AdvisorAutoExecuteStatus>
 -ServerName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cb45-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1cb45-105">DESCRIPTION</span></span>
<span data-ttu-id="1cb45-106">Il cmdlet **Set-AzSqlServerAdvisorAutoExecuteStatus** imposta la proprietà di esecuzione automatica per un operatore SQL Server Azure.</span><span class="sxs-lookup"><span data-stu-id="1cb45-106">The **Set-AzSqlServerAdvisorAutoExecuteStatus** cmdlet sets the auto execute property for an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="1cb45-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1cb45-107">EXAMPLES</span></span>

### <span data-ttu-id="1cb45-108">Esempio 1: Abilitare l'esecuzione automatica per un consulente</span><span class="sxs-lookup"><span data-stu-id="1cb45-108">Example 1: Enable auto execute for an Advisor</span></span>
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

<span data-ttu-id="1cb45-109">Questo comando abilita lo stato di esecuzione automatica di un consulente denominato CreateIndex.</span><span class="sxs-lookup"><span data-stu-id="1cb45-109">This command enables the auto execute status of an Advisor named CreateIndex.</span></span>

## <span data-ttu-id="1cb45-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1cb45-110">PARAMETERS</span></span>

### <span data-ttu-id="1cb45-111">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="1cb45-111">-AdvisorName</span></span>
<span data-ttu-id="1cb45-112">Specifica il nome dell'consulente per cui questo cmdlet aggiorna lo stato di esecuzione automatica.</span><span class="sxs-lookup"><span data-stu-id="1cb45-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="1cb45-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="1cb45-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="1cb45-114">Specifica il valore a cui questo cmdlet aggiorna lo stato di esecuzione automatica.</span><span class="sxs-lookup"><span data-stu-id="1cb45-114">Specifies the value to which this cmdlet updates the auto execute status.</span></span>
<span data-ttu-id="1cb45-115">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="1cb45-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1cb45-116">Abilitato</span><span class="sxs-lookup"><span data-stu-id="1cb45-116">Enabled</span></span>
- <span data-ttu-id="1cb45-117">Disabilitato</span><span class="sxs-lookup"><span data-stu-id="1cb45-117">Disabled</span></span>
- <span data-ttu-id="1cb45-118">Impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="1cb45-118">Default</span></span>

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

### <span data-ttu-id="1cb45-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cb45-119">-DefaultProfile</span></span>
<span data-ttu-id="1cb45-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="1cb45-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1cb45-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cb45-121">-ResourceGroupName</span></span>
<span data-ttu-id="1cb45-122">Specifica il nome del gruppo di risorse del server.</span><span class="sxs-lookup"><span data-stu-id="1cb45-122">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="1cb45-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1cb45-123">-ServerName</span></span>
<span data-ttu-id="1cb45-124">Specifica il nome del server.</span><span class="sxs-lookup"><span data-stu-id="1cb45-124">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="1cb45-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1cb45-125">-Confirm</span></span>
<span data-ttu-id="1cb45-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1cb45-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cb45-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cb45-127">-WhatIf</span></span>
<span data-ttu-id="1cb45-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1cb45-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cb45-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1cb45-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cb45-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cb45-130">CommonParameters</span></span>
<span data-ttu-id="1cb45-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cb45-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cb45-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1cb45-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cb45-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="1cb45-133">INPUTS</span></span>

### <span data-ttu-id="1cb45-134">System.String</span><span class="sxs-lookup"><span data-stu-id="1cb45-134">System.String</span></span>

### <span data-ttu-id="1cb45-135">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="1cb45-135">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="1cb45-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1cb45-136">OUTPUTS</span></span>

### <span data-ttu-id="1cb45-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="1cb45-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span></span>

## <span data-ttu-id="1cb45-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="1cb45-138">NOTES</span></span>
* <span data-ttu-id="1cb45-139">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, sql, server, mssql, advisor</span><span class="sxs-lookup"><span data-stu-id="1cb45-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span></span>

## <span data-ttu-id="1cb45-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1cb45-140">RELATED LINKS</span></span>

[<span data-ttu-id="1cb45-141">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="1cb45-141">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="1cb45-142">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="1cb45-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
