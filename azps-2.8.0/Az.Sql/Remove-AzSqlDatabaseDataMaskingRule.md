---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4695AFEA-D244-4FCB-AF36-D8CDEBFB392C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 016b77c7e58a3c95405d6364118a9d0ec7815660
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93856813"
---
# <span data-ttu-id="b243a-101">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="b243a-101">Remove-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="b243a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b243a-102">SYNOPSIS</span></span>
<span data-ttu-id="b243a-103">Rimuove una regola di mascheramento dei dati da un database.</span><span class="sxs-lookup"><span data-stu-id="b243a-103">Removes a data masking rule from a database.</span></span>

## <span data-ttu-id="b243a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b243a-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseDataMaskingRule [-PassThru] [-Force] -SchemaName <String> -TableName <String>
 -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b243a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b243a-105">DESCRIPTION</span></span>
<span data-ttu-id="b243a-106">Il cmdlet **Remove-AzSqlDatabaseDataMaskingRule** rimuove una specifica regola di mascheramento dei dati da un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="b243a-106">The **Remove-AzSqlDatabaseDataMaskingRule** cmdlet removes a specific data masking rule from an Azure SQL database.</span></span>
<span data-ttu-id="b243a-107">Puoi rimuovere una regola di mascheramento dei dati usando i parametri *ResourceGroupName* , *nomeserver* , *DatabaseName* e *RuleId* per identificare la regola rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b243a-107">You can remove a data masking rule by using the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule that this cmdlet removes.</span></span>
<span data-ttu-id="b243a-108">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="b243a-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="b243a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b243a-109">EXAMPLES</span></span>

### <span data-ttu-id="b243a-110">Esempio 1: rimuovere una regola di mascheramento dei dati del database</span><span class="sxs-lookup"><span data-stu-id="b243a-110">Example 1: Remove a database data masking rule</span></span>
```
PS C:\>Remove-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SchemaName "dbo" -TableName  "table1" -ColumnName "column1"
```

<span data-ttu-id="b243a-111">Questo comando rimuove il nome della regola Rule01 definito per il database Database01.</span><span class="sxs-lookup"><span data-stu-id="b243a-111">This command removes rule name Rule01 defined for the database Database01.</span></span>
<span data-ttu-id="b243a-112">Il database si trova in Server01 e assegnato al gruppo di risorse ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="b243a-112">The database is located on Server01 and assigned to resource group ResourceGroup01.</span></span>

## <span data-ttu-id="b243a-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b243a-113">PARAMETERS</span></span>

### <span data-ttu-id="b243a-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="b243a-114">-ColumnName</span></span>
<span data-ttu-id="b243a-115">Specifica il nome della colonna di destinazione della regola di mascheramento.</span><span class="sxs-lookup"><span data-stu-id="b243a-115">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="b243a-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b243a-116">-DatabaseName</span></span>
<span data-ttu-id="b243a-117">Specifica il nome del database.</span><span class="sxs-lookup"><span data-stu-id="b243a-117">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="b243a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b243a-118">-DefaultProfile</span></span>
<span data-ttu-id="b243a-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b243a-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b243a-120">-Force</span><span class="sxs-lookup"><span data-stu-id="b243a-120">-Force</span></span>
<span data-ttu-id="b243a-121">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b243a-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b243a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b243a-122">-PassThru</span></span>
<span data-ttu-id="b243a-123">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="b243a-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b243a-124">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="b243a-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b243a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b243a-125">-ResourceGroupName</span></span>
<span data-ttu-id="b243a-126">Specifica il nome del gruppo di risorse a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="b243a-126">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="b243a-127">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="b243a-127">-SchemaName</span></span>
<span data-ttu-id="b243a-128">Specifica il nome di uno schema.</span><span class="sxs-lookup"><span data-stu-id="b243a-128">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="b243a-129">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="b243a-129">-ServerName</span></span>
<span data-ttu-id="b243a-130">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="b243a-130">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="b243a-131">-TableName</span><span class="sxs-lookup"><span data-stu-id="b243a-131">-TableName</span></span>
<span data-ttu-id="b243a-132">Specifica il nome di una tabella SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="b243a-132">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="b243a-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b243a-133">-Confirm</span></span>
<span data-ttu-id="b243a-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b243a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b243a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b243a-135">-WhatIf</span></span>
<span data-ttu-id="b243a-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b243a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b243a-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b243a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b243a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b243a-138">CommonParameters</span></span>
<span data-ttu-id="b243a-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b243a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b243a-140">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b243a-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b243a-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b243a-141">INPUTS</span></span>

### <span data-ttu-id="b243a-142">System. String</span><span class="sxs-lookup"><span data-stu-id="b243a-142">System.String</span></span>

## <span data-ttu-id="b243a-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b243a-143">OUTPUTS</span></span>

### <span data-ttu-id="b243a-144">Microsoft. Azure. Commands. SQL. datamasking. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="b243a-144">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="b243a-145">Note</span><span class="sxs-lookup"><span data-stu-id="b243a-145">NOTES</span></span>

## <span data-ttu-id="b243a-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b243a-146">RELATED LINKS</span></span>

[<span data-ttu-id="b243a-147">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="b243a-147">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="b243a-148">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="b243a-148">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="b243a-149">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="b243a-149">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="b243a-150">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="b243a-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


