---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4695AFEA-D244-4FCB-AF36-D8CDEBFB392C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 02a6090a98a80300f886e8bbbd8e2622aa7981d4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196062"
---
# <span data-ttu-id="25b36-101">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="25b36-101">Remove-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="25b36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25b36-102">SYNOPSIS</span></span>
<span data-ttu-id="25b36-103">Rimuove una regola di maschera dati da un database.</span><span class="sxs-lookup"><span data-stu-id="25b36-103">Removes a data masking rule from a database.</span></span>

## <span data-ttu-id="25b36-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="25b36-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseDataMaskingRule [-PassThru] [-Force] -SchemaName <String> -TableName <String>
 -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25b36-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="25b36-105">DESCRIPTION</span></span>
<span data-ttu-id="25b36-106">Il cmdlet **Remove-AzSqlDatabaseDataMaskingRule** rimuove una specifica regola di maschera dati da un database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="25b36-106">The **Remove-AzSqlDatabaseDataMaskingRule** cmdlet removes a specific data masking rule from an Azure SQL database.</span></span>
<span data-ttu-id="25b36-107">È possibile rimuovere una regola di maschera dati usando i parametri *ResourceGroupName,* *ServerName,* *DatabaseName* e *RuleId* per identificare la regola rimossa dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25b36-107">You can remove a data masking rule by using the *ResourceGroupName*, *ServerName*, *DatabaseName*, and *RuleId* parameters to identify the rule that this cmdlet removes.</span></span>
<span data-ttu-id="25b36-108">Questo cmdlet è supportato anche dal servizio SQL Server di estensione del database in Azure.</span><span class="sxs-lookup"><span data-stu-id="25b36-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="25b36-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="25b36-109">EXAMPLES</span></span>

### <span data-ttu-id="25b36-110">Esempio 1: Rimuovere una regola di maschera dati di database</span><span class="sxs-lookup"><span data-stu-id="25b36-110">Example 1: Remove a database data masking rule</span></span>
```
PS C:\>Remove-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SchemaName "dbo" -TableName  "table1" -ColumnName "column1"
```

<span data-ttu-id="25b36-111">Questo comando rimuove il nome della regola Rule01 definita per il database Database01.</span><span class="sxs-lookup"><span data-stu-id="25b36-111">This command removes rule name Rule01 defined for the database Database01.</span></span>
<span data-ttu-id="25b36-112">Il database si trova su Server01 e viene assegnato al gruppo di risorse ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="25b36-112">The database is located on Server01 and assigned to resource group ResourceGroup01.</span></span>

## <span data-ttu-id="25b36-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25b36-113">PARAMETERS</span></span>

### <span data-ttu-id="25b36-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="25b36-114">-ColumnName</span></span>
<span data-ttu-id="25b36-115">Specifica il nome della colonna di destinazione della regola di maschera.</span><span class="sxs-lookup"><span data-stu-id="25b36-115">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="25b36-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="25b36-116">-DatabaseName</span></span>
<span data-ttu-id="25b36-117">Specifica il nome del database.</span><span class="sxs-lookup"><span data-stu-id="25b36-117">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25b36-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25b36-118">-DefaultProfile</span></span>
<span data-ttu-id="25b36-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="25b36-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="25b36-120">-Force</span><span class="sxs-lookup"><span data-stu-id="25b36-120">-Force</span></span>
<span data-ttu-id="25b36-121">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="25b36-121">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25b36-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25b36-122">-PassThru</span></span>
<span data-ttu-id="25b36-123">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="25b36-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="25b36-124">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="25b36-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25b36-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25b36-125">-ResourceGroupName</span></span>
<span data-ttu-id="25b36-126">Specifica il nome del gruppo di risorse a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="25b36-126">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="25b36-127">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="25b36-127">-SchemaName</span></span>
<span data-ttu-id="25b36-128">Specifica il nome di uno schema.</span><span class="sxs-lookup"><span data-stu-id="25b36-128">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="25b36-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="25b36-129">-ServerName</span></span>
<span data-ttu-id="25b36-130">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="25b36-130">Specifies the name of the server that hosts the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25b36-131">-TableName</span><span class="sxs-lookup"><span data-stu-id="25b36-131">-TableName</span></span>
<span data-ttu-id="25b36-132">Specifica il nome di una tabella SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="25b36-132">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="25b36-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25b36-133">-Confirm</span></span>
<span data-ttu-id="25b36-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25b36-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25b36-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25b36-135">-WhatIf</span></span>
<span data-ttu-id="25b36-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="25b36-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25b36-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="25b36-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25b36-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25b36-138">CommonParameters</span></span>
<span data-ttu-id="25b36-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25b36-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25b36-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="25b36-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25b36-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="25b36-141">INPUTS</span></span>

### <span data-ttu-id="25b36-142">System.String</span><span class="sxs-lookup"><span data-stu-id="25b36-142">System.String</span></span>

## <span data-ttu-id="25b36-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="25b36-143">OUTPUTS</span></span>

### <span data-ttu-id="25b36-144">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="25b36-144">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="25b36-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="25b36-145">NOTES</span></span>

## <span data-ttu-id="25b36-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="25b36-146">RELATED LINKS</span></span>

[<span data-ttu-id="25b36-147">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="25b36-147">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="25b36-148">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="25b36-148">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="25b36-149">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="25b36-149">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="25b36-150">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="25b36-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


