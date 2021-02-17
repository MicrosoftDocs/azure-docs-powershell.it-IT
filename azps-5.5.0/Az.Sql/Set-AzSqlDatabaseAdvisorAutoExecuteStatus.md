---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 50E09DF7-F5B5-4668-9520-73D562E91800
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaseadvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 1d6348c5ede63dee1f76059277c8f7d142a2c327
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190999"
---
# <span data-ttu-id="a46bf-101">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="a46bf-101">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="a46bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a46bf-102">SYNOPSIS</span></span>
<span data-ttu-id="a46bf-103">Modifica lo stato di esecuzione automatica di un avviso di SQL database di Azure.</span><span class="sxs-lookup"><span data-stu-id="a46bf-103">Modifies auto execute status of an Azure SQL Database Advisor.</span></span>

## <span data-ttu-id="a46bf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a46bf-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseAdvisorAutoExecuteStatus -AdvisorName <String> -AutoExecuteStatus <AdvisorAutoExecuteStatus>
 -ServerName <String> -DatabaseName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a46bf-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a46bf-105">DESCRIPTION</span></span>
<span data-ttu-id="a46bf-106">Il cmdlet **Set-AzSqlDatabaseAdvisorAutoExecuteStatus** modifica la proprietà di esecuzione automatica per un componente aggiuntivo Azure SQL Database Advisor.</span><span class="sxs-lookup"><span data-stu-id="a46bf-106">The **Set-AzSqlDatabaseAdvisorAutoExecuteStatus** cmdlet modifies the auto execute property for an Azure SQL Database Advisor.</span></span>
<span data-ttu-id="a46bf-107">Attualmente, questo cmdlet supporta i valori Abilitata, Disabilitata e Predefinita.</span><span class="sxs-lookup"><span data-stu-id="a46bf-107">Currently, this cmdlet supports the values Enabled, Disabled, and Default.</span></span>

## <span data-ttu-id="a46bf-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a46bf-108">EXAMPLES</span></span>

### <span data-ttu-id="a46bf-109">Esempio 1: Abilitare l'esecuzione automatica per un consulente</span><span class="sxs-lookup"><span data-stu-id="a46bf-109">Example 1: Enable auto execute for an advisor</span></span>
```
PS C:\>Set-AzSqlDatabaseAdvisorAutoExecuteStatus -ResourceGroupName "ContosoRunnersProd" -ServerName "runner-australia-east" -DatabaseName "ContosoRunner" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
DatabaseName                   : ContosoRunner
ResourceGroupName              : ContosoRunnersProd
ServerName                     : runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Enabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="a46bf-110">Questo comando modifica lo stato di esecuzione automatica di un consulente denominato CreateIndex in Abilitato.</span><span class="sxs-lookup"><span data-stu-id="a46bf-110">This command changes the auto execute status of an advisor named CreateIndex to Enabled.</span></span>

## <span data-ttu-id="a46bf-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a46bf-111">PARAMETERS</span></span>

### <span data-ttu-id="a46bf-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="a46bf-112">-AdvisorName</span></span>
<span data-ttu-id="a46bf-113">Specifica il nome dell'consulente per cui questo cmdlet modifica lo stato.</span><span class="sxs-lookup"><span data-stu-id="a46bf-113">Specifies the name of the advisor for which this cmdlet modifies the status.</span></span>

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

### <span data-ttu-id="a46bf-114">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="a46bf-114">-AutoExecuteStatus</span></span>
<span data-ttu-id="a46bf-115">Specifica il valore per lo stato.</span><span class="sxs-lookup"><span data-stu-id="a46bf-115">Specifies the value for the status.</span></span>
<span data-ttu-id="a46bf-116">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="a46bf-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a46bf-117">Abilitato</span><span class="sxs-lookup"><span data-stu-id="a46bf-117">Enabled</span></span> 
- <span data-ttu-id="a46bf-118">Disabilitato</span><span class="sxs-lookup"><span data-stu-id="a46bf-118">Disabled</span></span> 
- <span data-ttu-id="a46bf-119">Impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="a46bf-119">Default</span></span>

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

### <span data-ttu-id="a46bf-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a46bf-120">-DatabaseName</span></span>
<span data-ttu-id="a46bf-121">Specifica il nome del database per cui il cmdlet modifica lo stato.</span><span class="sxs-lookup"><span data-stu-id="a46bf-121">Specifies the name of the database for which this cmdlet modifies status.</span></span>

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

### <span data-ttu-id="a46bf-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a46bf-122">-DefaultProfile</span></span>
<span data-ttu-id="a46bf-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="a46bf-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a46bf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a46bf-124">-ResourceGroupName</span></span>
<span data-ttu-id="a46bf-125">Specifica il nome del gruppo di risorse del server che contiene il database.</span><span class="sxs-lookup"><span data-stu-id="a46bf-125">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="a46bf-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a46bf-126">-ServerName</span></span>
<span data-ttu-id="a46bf-127">Specifica il nome del server per il database.</span><span class="sxs-lookup"><span data-stu-id="a46bf-127">Specifies the name of the server for the database.</span></span>

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

### <span data-ttu-id="a46bf-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a46bf-128">-Confirm</span></span>
<span data-ttu-id="a46bf-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a46bf-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a46bf-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a46bf-130">-WhatIf</span></span>
<span data-ttu-id="a46bf-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a46bf-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a46bf-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a46bf-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a46bf-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a46bf-133">CommonParameters</span></span>
<span data-ttu-id="a46bf-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a46bf-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a46bf-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a46bf-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a46bf-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="a46bf-136">INPUTS</span></span>

### <span data-ttu-id="a46bf-137">System.String</span><span class="sxs-lookup"><span data-stu-id="a46bf-137">System.String</span></span>

### <span data-ttu-id="a46bf-138">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="a46bf-138">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="a46bf-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a46bf-139">OUTPUTS</span></span>

### <span data-ttu-id="a46bf-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="a46bf-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>

## <span data-ttu-id="a46bf-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="a46bf-141">NOTES</span></span>

## <span data-ttu-id="a46bf-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a46bf-142">RELATED LINKS</span></span>

[<span data-ttu-id="a46bf-143">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="a46bf-143">Get-AzSqlDatabaseAdvisor</span></span>](./Get-AzSqlDatabaseAdvisor.md)

[<span data-ttu-id="a46bf-144">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="a46bf-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

