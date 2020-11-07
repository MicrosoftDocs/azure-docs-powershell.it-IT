---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 848A6972-AB29-46FB-8E03-FF2ADB113A0E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 5c43820c57531ca5a844e1ab429c26d85fecceee
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676995"
---
# <span data-ttu-id="33dfc-101">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="33dfc-101">Get-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="33dfc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="33dfc-102">SYNOPSIS</span></span>
<span data-ttu-id="33dfc-103">Ottiene le regole di mascheramento dei dati da un database.</span><span class="sxs-lookup"><span data-stu-id="33dfc-103">Gets the data masking rules from a database.</span></span>

## <span data-ttu-id="33dfc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="33dfc-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseDataMaskingRule [-SchemaName <String>] [-TableName <String>] [-ColumnName <String>]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33dfc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="33dfc-105">DESCRIPTION</span></span>
<span data-ttu-id="33dfc-106">Il cmdlet **Get-AzSqlDatabaseDataMaskingRule** ottiene una regola di mascheramento dei dati specifica o tutte le regole per la mascheratura dei dati per un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="33dfc-106">The **Get-AzSqlDatabaseDataMaskingRule** cmdlet gets either a specific data masking rule or all of the data masking rules for an Azure SQL database.</span></span>
<span data-ttu-id="33dfc-107">Per usare il cmdlet, USA i parametri *ResourceGroupName* , *ServerName* e *DatabaseName* per identificare il database e il parametro *RuleId* per specificare la regola restituita da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33dfc-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database, and the *RuleId* parameter to specify which rule this cmdlet returns.</span></span>
<span data-ttu-id="33dfc-108">Se non fornisci *RuleId* , vengono restituite tutte le regole per la mascheratura dei dati per il database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="33dfc-108">If you do not provide *RuleId* , all the data masking rules for that Azure SQL database are returned.</span></span>
<span data-ttu-id="33dfc-109">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="33dfc-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="33dfc-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="33dfc-110">EXAMPLES</span></span>

### <span data-ttu-id="33dfc-111">Esempio 1: ottenere tutte le regole per la mascheratura dei dati da un database</span><span class="sxs-lookup"><span data-stu-id="33dfc-111">Example 1: Get all data masking rules from a database</span></span>
```
PS C:\>Get-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName      : database01
ResourceGroupName : resourcegroup01
ServerName        : server01
SchemaName        : dbo
TableName         : table1
ColumnName        : column1
MaskingFunction   : Default
PrefixSize        :
SuffixSize        :
ReplacementString :
NumberFrom        :
NumberTo          :

DatabaseName      : database01
ResourceGroupName : resourcegroup01
ServerName        : server01
SchemaName        : dbo
TableName         : table2
ColumnName        : column2
MaskingFunction   : Default
PrefixSize        :
SuffixSize        :
ReplacementString :
NumberFrom        :
NumberTo          :
```

### <span data-ttu-id="33dfc-112">Esempio 2: ottenere la regola di mascheramento dei dati definita nello schema "dbo", tabella "Tabella1" e colonna "Column1".</span><span class="sxs-lookup"><span data-stu-id="33dfc-112">Example 2: Get the data masking rule defined on schema "dbo", table "table1" and column "column1".</span></span>
```
PS C:\>Get-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SchemaName "dbo" -TableName  "table1" -ColumnName "column1"
DatabaseName      : database01
ResourceGroupName : resourcegroup01
ServerName        : server01
SchemaName        : dbo
TableName         : table1
ColumnName        : column1
MaskingFunction   : Default
PrefixSize        :
SuffixSize        :
ReplacementString :
NumberFrom        :
NumberTo          :
```

## <span data-ttu-id="33dfc-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="33dfc-113">PARAMETERS</span></span>

### <span data-ttu-id="33dfc-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="33dfc-114">-ColumnName</span></span>
<span data-ttu-id="33dfc-115">Specifica il nome della colonna di destinazione della regola di mascheramento.</span><span class="sxs-lookup"><span data-stu-id="33dfc-115">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="33dfc-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="33dfc-116">-DatabaseName</span></span>
<span data-ttu-id="33dfc-117">Specifica il nome del database.</span><span class="sxs-lookup"><span data-stu-id="33dfc-117">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="33dfc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33dfc-118">-DefaultProfile</span></span>
<span data-ttu-id="33dfc-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="33dfc-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="33dfc-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33dfc-120">-ResourceGroupName</span></span>
<span data-ttu-id="33dfc-121">Specifica il nome del gruppo di risorse a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="33dfc-121">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="33dfc-122">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="33dfc-122">-SchemaName</span></span>
<span data-ttu-id="33dfc-123">Specifica il nome di uno schema.</span><span class="sxs-lookup"><span data-stu-id="33dfc-123">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="33dfc-124">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="33dfc-124">-ServerName</span></span>
<span data-ttu-id="33dfc-125">Specifica il nome del server.</span><span class="sxs-lookup"><span data-stu-id="33dfc-125">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="33dfc-126">-TableName</span><span class="sxs-lookup"><span data-stu-id="33dfc-126">-TableName</span></span>
<span data-ttu-id="33dfc-127">Specifica il nome di una tabella SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="33dfc-127">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="33dfc-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="33dfc-128">-Confirm</span></span>
<span data-ttu-id="33dfc-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33dfc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33dfc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33dfc-130">-WhatIf</span></span>
<span data-ttu-id="33dfc-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="33dfc-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33dfc-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="33dfc-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33dfc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33dfc-133">CommonParameters</span></span>
<span data-ttu-id="33dfc-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33dfc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33dfc-135">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="33dfc-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33dfc-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="33dfc-136">INPUTS</span></span>

### <span data-ttu-id="33dfc-137">System. String</span><span class="sxs-lookup"><span data-stu-id="33dfc-137">System.String</span></span>

## <span data-ttu-id="33dfc-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="33dfc-138">OUTPUTS</span></span>

### <span data-ttu-id="33dfc-139">Microsoft. Azure. Commands. SQL. datamasking. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="33dfc-139">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="33dfc-140">Note</span><span class="sxs-lookup"><span data-stu-id="33dfc-140">NOTES</span></span>

## <span data-ttu-id="33dfc-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="33dfc-141">RELATED LINKS</span></span>

[<span data-ttu-id="33dfc-142">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="33dfc-142">Get-AzSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="33dfc-143">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="33dfc-143">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="33dfc-144">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="33dfc-144">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="33dfc-145">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="33dfc-145">Set-AzSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="33dfc-146">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="33dfc-146">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)


