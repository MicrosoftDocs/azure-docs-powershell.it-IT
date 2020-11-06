---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4695AFEA-D244-4FCB-AF36-D8CDEBFB392C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: d20e6f838370e73dc4d6ff849e6088df9b9f28cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519842"
---
# <span data-ttu-id="53eab-101">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="53eab-101">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="53eab-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="53eab-102">SYNOPSIS</span></span>
<span data-ttu-id="53eab-103">Rimuove una regola di mascheramento dei dati da un database.</span><span class="sxs-lookup"><span data-stu-id="53eab-103">Removes a data masking rule from a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53eab-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="53eab-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseDataMaskingRule [-PassThru] [-Force] -SchemaName <String> -TableName <String>
 -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53eab-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="53eab-105">DESCRIPTION</span></span>
<span data-ttu-id="53eab-106">Il cmdlet **Remove-AzureRmSqlDatabaseDataMaskingRule** rimuove una specifica regola di mascheramento dei dati da un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="53eab-106">The **Remove-AzureRmSqlDatabaseDataMaskingRule** cmdlet removes a specific data masking rule from an Azure SQL database.</span></span>
<span data-ttu-id="53eab-107">Puoi rimuovere una regola di mascheramento dei dati usando i parametri *ResourceGroupName* , *nomeserver* , *DatabaseName* e *RuleId* per identificare la regola rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53eab-107">You can remove a data masking rule by using the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule that this cmdlet removes.</span></span>

<span data-ttu-id="53eab-108">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="53eab-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="53eab-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="53eab-109">EXAMPLES</span></span>

### <span data-ttu-id="53eab-110">Esempio 1: rimuovere una regola di mascheramento dei dati del database</span><span class="sxs-lookup"><span data-stu-id="53eab-110">Example 1: Remove a database data masking rule</span></span>
```
PS C:\>Remove-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SchemaName "dbo" -TableName  "table1" -ColumnName "column1"
```

<span data-ttu-id="53eab-111">Questo comando rimuove il nome della regola Rule01 definito per il database Database01.</span><span class="sxs-lookup"><span data-stu-id="53eab-111">This command removes rule name Rule01 defined for the database Database01.</span></span>
<span data-ttu-id="53eab-112">Il database si trova in Server01 e assegnato al gruppo di risorse ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="53eab-112">The database is located on Server01 and assigned to resource group ResourceGroup01.</span></span>

## <span data-ttu-id="53eab-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="53eab-113">PARAMETERS</span></span>

### <span data-ttu-id="53eab-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="53eab-114">-ColumnName</span></span>
<span data-ttu-id="53eab-115">Specifica il nome della colonna di destinazione della regola di mascheramento.</span><span class="sxs-lookup"><span data-stu-id="53eab-115">Specifies the name of the column targeted by the masking rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53eab-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="53eab-116">-DatabaseName</span></span>
<span data-ttu-id="53eab-117">Specifica il nome del database.</span><span class="sxs-lookup"><span data-stu-id="53eab-117">Specifies the name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53eab-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53eab-118">-DefaultProfile</span></span>
<span data-ttu-id="53eab-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="53eab-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53eab-120">-Force</span><span class="sxs-lookup"><span data-stu-id="53eab-120">-Force</span></span>
<span data-ttu-id="53eab-121">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="53eab-121">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53eab-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="53eab-122">-PassThru</span></span>
<span data-ttu-id="53eab-123">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="53eab-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="53eab-124">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="53eab-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53eab-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53eab-125">-ResourceGroupName</span></span>
<span data-ttu-id="53eab-126">Specifica il nome del gruppo di risorse a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="53eab-126">Specifies the name of the resource group to which the database is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53eab-127">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="53eab-127">-SchemaName</span></span>
<span data-ttu-id="53eab-128">Specifica il nome di uno schema.</span><span class="sxs-lookup"><span data-stu-id="53eab-128">Specifies the name of a schema.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53eab-129">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="53eab-129">-ServerName</span></span>
<span data-ttu-id="53eab-130">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="53eab-130">Specifies the name of the server that hosts the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53eab-131">-TableName</span><span class="sxs-lookup"><span data-stu-id="53eab-131">-TableName</span></span>
<span data-ttu-id="53eab-132">Specifica il nome di una tabella SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="53eab-132">Specifies the name of an Azure SQL table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53eab-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="53eab-133">-Confirm</span></span>
<span data-ttu-id="53eab-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53eab-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53eab-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53eab-135">-WhatIf</span></span>
<span data-ttu-id="53eab-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="53eab-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53eab-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="53eab-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53eab-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53eab-138">CommonParameters</span></span>
<span data-ttu-id="53eab-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53eab-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53eab-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53eab-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53eab-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="53eab-141">INPUTS</span></span>

### <span data-ttu-id="53eab-142">Microsoft. Azure. Commands. SQL. Security. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="53eab-142">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="53eab-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="53eab-143">OUTPUTS</span></span>

### <span data-ttu-id="53eab-144">Microsoft. Azure. Commands. SQL. Security. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="53eab-144">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="53eab-145">Note</span><span class="sxs-lookup"><span data-stu-id="53eab-145">NOTES</span></span>

## <span data-ttu-id="53eab-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="53eab-146">RELATED LINKS</span></span>

[<span data-ttu-id="53eab-147">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="53eab-147">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="53eab-148">New-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="53eab-148">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="53eab-149">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="53eab-149">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="53eab-150">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="53eab-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


