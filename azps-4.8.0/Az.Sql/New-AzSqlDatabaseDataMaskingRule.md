---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A123CB7F-2F95-49EE-9F57-E264EB1F9093
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 35f2bc63366a86501650af1808274a3a0403e77f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188776"
---
# <span data-ttu-id="a7423-101">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="a7423-101">New-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="a7423-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a7423-102">SYNOPSIS</span></span>
<span data-ttu-id="a7423-103">Crea una regola per la mascheratura dei dati per un database.</span><span class="sxs-lookup"><span data-stu-id="a7423-103">Creates a data masking rule for a database.</span></span>

## <span data-ttu-id="a7423-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a7423-104">SYNTAX</span></span>

```
New-AzSqlDatabaseDataMaskingRule -MaskingFunction <String> [-PrefixSize <UInt32>] [-ReplacementString <String>]
 [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru] -SchemaName <String>
 -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a7423-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a7423-105">DESCRIPTION</span></span>
<span data-ttu-id="a7423-106">Il cmdlet **New-AzSqlDatabaseDataMaskingRule** crea una regola per la mascheratura dei dati per un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="a7423-106">The **New-AzSqlDatabaseDataMaskingRule** cmdlet creates a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="a7423-107">Per usare il cmdlet, usare i parametri *ResourceGroupName* , *ServerName* e *DatabaseName* per identificare la regola.</span><span class="sxs-lookup"><span data-stu-id="a7423-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the rule.</span></span>
<span data-ttu-id="a7423-108">Fornisci le proprietà *TableName* e *ColumnName* per specificare la destinazione della regola e il parametro *MaskingFunction* per definire il modo in cui i dati vengono mascherati.</span><span class="sxs-lookup"><span data-stu-id="a7423-108">Provide the *TableName* and *ColumnName* to specify the target of the rule and the *MaskingFunction* parameter to define how the data is masked.</span></span>
<span data-ttu-id="a7423-109">Se *MaskingFunction* ha un valore di Number o text, puoi specificare i parametri *NumberFrom* e *NumberTo* , per la maschera dei numeri, o *PrefixSize* , *ReplacementString* e *SuffixSize* per la mascheratura del testo.</span><span class="sxs-lookup"><span data-stu-id="a7423-109">If *MaskingFunction* has a value of Number or Text, you can specify the *NumberFrom* and *NumberTo* parameters, for number masking, or the *PrefixSize* , *ReplacementString* , and *SuffixSize* for text masking.</span></span>
<span data-ttu-id="a7423-110">Se il comando riesce e viene usato il parametro *PassThru* , il cmdlet restituisce un oggetto che descrive le proprietà della regola di mascheramento dei dati oltre agli identificatori di regola.</span><span class="sxs-lookup"><span data-stu-id="a7423-110">If the command succeeds and the *PassThru* parameter is used, the cmdlet returns an object describing the data masking rule properties in addition to the rule identifiers.</span></span>
<span data-ttu-id="a7423-111">Gli identificatori di regole includono, ma non sono limitati a, *ResourceGroupName* , *nomeserver* , *DatabaseName* e *RuleId*.</span><span class="sxs-lookup"><span data-stu-id="a7423-111">Rule identifiers include, but are not limited to, *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleID*.</span></span>
<span data-ttu-id="a7423-112">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="a7423-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="a7423-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a7423-113">EXAMPLES</span></span>

### <span data-ttu-id="a7423-114">Esempio 1: creare una regola per la mascheratura dei dati per una colonna di numeri in un database</span><span class="sxs-lookup"><span data-stu-id="a7423-114">Example 1: Create a data masking rule for a number column in a database</span></span>
```
PS C:\>New-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"  -SchemaName "Schema01" -TableName "Table01" -ColumnName "Column01" -MaskingFunction "Number" -NumberFrom 5 -NumberTo 14
```

<span data-ttu-id="a7423-115">Questo comando crea una regola di mascheramento dei dati per la colonna denominata Column01 nella tabella denominata Table01 nello schema denominato Schema01.</span><span class="sxs-lookup"><span data-stu-id="a7423-115">This command creates a data masking rule for the column named Column01 in the table named Table01 in the schema named Schema01.</span></span>
<span data-ttu-id="a7423-116">Il database denominato Database01 contiene tutti questi elementi.</span><span class="sxs-lookup"><span data-stu-id="a7423-116">The database named Database01 contains all these items.</span></span>
<span data-ttu-id="a7423-117">La regola è una regola di mascheramento numerico che usa un numero casuale compreso tra 5 e 14 come valore della maschera.</span><span class="sxs-lookup"><span data-stu-id="a7423-117">The rule is a number masking rule that uses a random number between 5 and 14 as the mask value.</span></span>

## <span data-ttu-id="a7423-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a7423-118">PARAMETERS</span></span>

### <span data-ttu-id="a7423-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="a7423-119">-ColumnName</span></span>
<span data-ttu-id="a7423-120">Specifica il nome della colonna di destinazione della regola di mascheramento.</span><span class="sxs-lookup"><span data-stu-id="a7423-120">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="a7423-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a7423-121">-DatabaseName</span></span>
<span data-ttu-id="a7423-122">Specifica il nome del database.</span><span class="sxs-lookup"><span data-stu-id="a7423-122">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="a7423-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7423-123">-DefaultProfile</span></span>
<span data-ttu-id="a7423-124">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a7423-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7423-125">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="a7423-125">-MaskingFunction</span></span>
<span data-ttu-id="a7423-126">Specifica la funzione di mascheramento utilizzata dalla regola.</span><span class="sxs-lookup"><span data-stu-id="a7423-126">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="a7423-127">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a7423-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a7423-128">Predefinita</span><span class="sxs-lookup"><span data-stu-id="a7423-128">Default</span></span>
- <span data-ttu-id="a7423-129">Nomasking</span><span class="sxs-lookup"><span data-stu-id="a7423-129">NoMasking</span></span>
- <span data-ttu-id="a7423-130">Testo</span><span class="sxs-lookup"><span data-stu-id="a7423-130">Text</span></span>
- <span data-ttu-id="a7423-131">Numero</span><span class="sxs-lookup"><span data-stu-id="a7423-131">Number</span></span>
- <span data-ttu-id="a7423-132">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="a7423-132">SocialSecurityNumber</span></span>
- <span data-ttu-id="a7423-133">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="a7423-133">CreditCardNumber</span></span>
- <span data-ttu-id="a7423-134">Messaggio di posta elettronica il valore predefinito è default.</span><span class="sxs-lookup"><span data-stu-id="a7423-134">Email The default value is Default.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NoMasking, Default, Text, Number, SocialSecurityNumber, CreditCardNumber, Email

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7423-135">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="a7423-135">-NumberFrom</span></span>
<span data-ttu-id="a7423-136">Specifica il numero limite inferiore dell'intervallo da cui viene selezionato un valore casuale.</span><span class="sxs-lookup"><span data-stu-id="a7423-136">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="a7423-137">Specifica questo parametro solo se specifichi un valore di Number per il parametro *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="a7423-137">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="a7423-138">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="a7423-138">The default value is 0.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7423-139">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="a7423-139">-NumberTo</span></span>
<span data-ttu-id="a7423-140">Specifica il numero limite superiore dell'intervallo da cui viene selezionato un valore casuale.</span><span class="sxs-lookup"><span data-stu-id="a7423-140">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="a7423-141">Specifica questo parametro solo se specifichi un valore di Number per il parametro *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="a7423-141">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="a7423-142">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="a7423-142">The default value is 0.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7423-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a7423-143">-PassThru</span></span>
<span data-ttu-id="a7423-144">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="a7423-144">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a7423-145">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="a7423-145">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a7423-146">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="a7423-146">-PrefixSize</span></span>
<span data-ttu-id="a7423-147">Specifica il numero di caratteri all'inizio del testo che non sono mascherati.</span><span class="sxs-lookup"><span data-stu-id="a7423-147">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="a7423-148">Specifica questo parametro solo se specifichi un valore di testo per il parametro *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="a7423-148">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="a7423-149">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="a7423-149">The default value is 0.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7423-150">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="a7423-150">-ReplacementString</span></span>
<span data-ttu-id="a7423-151">Specifica il numero di caratteri alla fine del testo che non sono mascherati.</span><span class="sxs-lookup"><span data-stu-id="a7423-151">Specifies the number of characters in the end of the text that are not masked.</span></span>
<span data-ttu-id="a7423-152">Specifica questo parametro solo se specifichi un valore di testo per il parametro *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="a7423-152">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="a7423-153">Il valore predefinito è una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="a7423-153">The default value is an empty string.</span></span>

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

### <span data-ttu-id="a7423-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7423-154">-ResourceGroupName</span></span>
<span data-ttu-id="a7423-155">Specifica il nome del gruppo di risorse a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="a7423-155">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="a7423-156">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="a7423-156">-SchemaName</span></span>
<span data-ttu-id="a7423-157">Specifica il nome di uno schema.</span><span class="sxs-lookup"><span data-stu-id="a7423-157">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="a7423-158">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="a7423-158">-ServerName</span></span>
<span data-ttu-id="a7423-159">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="a7423-159">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="a7423-160">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="a7423-160">-SuffixSize</span></span>
<span data-ttu-id="a7423-161">Specifica il numero di caratteri alla fine del testo che non sono mascherati.</span><span class="sxs-lookup"><span data-stu-id="a7423-161">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="a7423-162">Specifica questo parametro solo se specifichi un valore di testo per il parametro *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="a7423-162">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="a7423-163">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="a7423-163">The default value is 0.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7423-164">-TableName</span><span class="sxs-lookup"><span data-stu-id="a7423-164">-TableName</span></span>
<span data-ttu-id="a7423-165">Specifica il nome della tabella di database che contiene la colonna mascherata.</span><span class="sxs-lookup"><span data-stu-id="a7423-165">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="a7423-166">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a7423-166">-Confirm</span></span>
<span data-ttu-id="a7423-167">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7423-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7423-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7423-168">-WhatIf</span></span>
<span data-ttu-id="a7423-169">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a7423-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7423-170">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a7423-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7423-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7423-171">CommonParameters</span></span>
<span data-ttu-id="a7423-172">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7423-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7423-173">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7423-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7423-174">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a7423-174">INPUTS</span></span>

### <span data-ttu-id="a7423-175">System. String</span><span class="sxs-lookup"><span data-stu-id="a7423-175">System.String</span></span>

### <span data-ttu-id="a7423-176">System. Nullable ' 1 [[System. UInt32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a7423-176">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a7423-177">System. Nullable ' 1 [[System. Double, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a7423-177">System.Nullable\`1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="a7423-178">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a7423-178">OUTPUTS</span></span>

### <span data-ttu-id="a7423-179">Microsoft. Azure. Commands. SQL. datamasking. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="a7423-179">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="a7423-180">Note</span><span class="sxs-lookup"><span data-stu-id="a7423-180">NOTES</span></span>

## <span data-ttu-id="a7423-181">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a7423-181">RELATED LINKS</span></span>

[<span data-ttu-id="a7423-182">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="a7423-182">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="a7423-183">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="a7423-183">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="a7423-184">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="a7423-184">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="a7423-185">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="a7423-185">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


