---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: A123CB7F-2F95-49EE-9F57-E264EB1F9093
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: b53b32b30e1b69da94ac8319ed3a5f4eee7ffc0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507859"
---
# <span data-ttu-id="8116f-101">New-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="8116f-101">New-AzureRmSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="8116f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8116f-102">SYNOPSIS</span></span>
<span data-ttu-id="8116f-103">Crea una regola per la mascheratura dei dati per un database.</span><span class="sxs-lookup"><span data-stu-id="8116f-103">Creates a data masking rule for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8116f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8116f-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseDataMaskingRule -MaskingFunction <String> [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8116f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8116f-105">DESCRIPTION</span></span>
<span data-ttu-id="8116f-106">Il cmdlet **New-AzureRmSqlDatabaseDataMaskingRule** crea una regola per la mascheratura dei dati per un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="8116f-106">The **New-AzureRmSqlDatabaseDataMaskingRule** cmdlet creates a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="8116f-107">Per usare il cmdlet, USA i parametri *ResourceGroupName* , *ServerName* , *DatabaseName* e *RuleId* per identificare la regola.</span><span class="sxs-lookup"><span data-stu-id="8116f-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="8116f-108">Fornisci le proprietà *TableName* e *ColumnName* per specificare la destinazione della regola e il parametro *MaskingFunction* per definire il modo in cui i dati vengono mascherati.</span><span class="sxs-lookup"><span data-stu-id="8116f-108">Provide the *TableName* and *ColumnName* to specify the target of the rule and the *MaskingFunction* parameter to define how the data is masked.</span></span>

<span data-ttu-id="8116f-109">Se *MaskingFunction* ha un valore di Number o text, puoi specificare i parametri *NumberFrom* e *NumberTo* , per la maschera dei numeri, o *PrefixSize* , *ReplacementString* e *SuffixSize* per la mascheratura del testo.</span><span class="sxs-lookup"><span data-stu-id="8116f-109">If *MaskingFunction* has a value of Number or Text, you can specify the *NumberFrom* and *NumberTo* parameters, for number masking, or the *PrefixSize* , *ReplacementString* , and *SuffixSize* for text masking.</span></span>

<span data-ttu-id="8116f-110">Se il comando riesce e viene usato il parametro *PassThru* , il cmdlet restituisce un oggetto che descrive le proprietà della regola di mascheramento dei dati oltre agli identificatori di regola.</span><span class="sxs-lookup"><span data-stu-id="8116f-110">If the command succeeds and the *PassThru* parameter is used, the cmdlet returns an object describing the data masking rule properties in addition to the rule identifiers.</span></span>
<span data-ttu-id="8116f-111">Gli identificatori di regole includono, ma non sono limitati a, *ResourceGroupName* , *nomeserver* , *DatabaseName* e *RuleId*.</span><span class="sxs-lookup"><span data-stu-id="8116f-111">Rule identifiers include, but are not limited to, *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleID*.</span></span>

<span data-ttu-id="8116f-112">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="8116f-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="8116f-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8116f-113">EXAMPLES</span></span>

### <span data-ttu-id="8116f-114">Esempio 1: creare una regola per la mascheratura dei dati per una colonna di numeri in un database</span><span class="sxs-lookup"><span data-stu-id="8116f-114">Example 1: Create a data masking rule for a number column in a database</span></span>
```
PS C:\>New-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RuleId "Rule01" -SchemaName "Schema01" -TableName "Table01" -ColumnName "Column01" -MaskingFunction "Number" -NumberFrom 5 -NumberTo 14
```

<span data-ttu-id="8116f-115">Questo comando crea una regola di mascheramento dei dati per la colonna denominata Column01 nella tabella denominata Table01 nello schema denominato Schema01.</span><span class="sxs-lookup"><span data-stu-id="8116f-115">This command creates a data masking rule for the column named Column01 in the table named Table01 in the schema named Schema01.</span></span>
<span data-ttu-id="8116f-116">Il database denominato Database01 contiene tutti questi elementi.</span><span class="sxs-lookup"><span data-stu-id="8116f-116">The database named Database01 contains all these items.</span></span>
<span data-ttu-id="8116f-117">La regola è una regola di mascheramento numerico che usa un numero casuale compreso tra 5 e 14 come valore della maschera.</span><span class="sxs-lookup"><span data-stu-id="8116f-117">The rule is a number masking rule that uses a random number between 5 and 14 as the mask value.</span></span>
<span data-ttu-id="8116f-118">La regola è denominata Rule01.</span><span class="sxs-lookup"><span data-stu-id="8116f-118">The rule is named Rule01.</span></span>

## <span data-ttu-id="8116f-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8116f-119">PARAMETERS</span></span>

### <span data-ttu-id="8116f-120">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="8116f-120">-ColumnName</span></span>
<span data-ttu-id="8116f-121">Specifica il nome della colonna di destinazione della regola di mascheramento.</span><span class="sxs-lookup"><span data-stu-id="8116f-121">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="8116f-122">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8116f-122">-DatabaseName</span></span>
<span data-ttu-id="8116f-123">Specifica il nome del database.</span><span class="sxs-lookup"><span data-stu-id="8116f-123">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="8116f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8116f-124">-DefaultProfile</span></span>
<span data-ttu-id="8116f-125">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8116f-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8116f-126">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="8116f-126">-MaskingFunction</span></span>
<span data-ttu-id="8116f-127">Specifica la funzione di mascheramento utilizzata dalla regola.</span><span class="sxs-lookup"><span data-stu-id="8116f-127">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="8116f-128">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="8116f-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8116f-129">Predefinita</span><span class="sxs-lookup"><span data-stu-id="8116f-129">Default</span></span>
- <span data-ttu-id="8116f-130">Nomasking</span><span class="sxs-lookup"><span data-stu-id="8116f-130">NoMasking</span></span>
- <span data-ttu-id="8116f-131">Testo</span><span class="sxs-lookup"><span data-stu-id="8116f-131">Text</span></span>
- <span data-ttu-id="8116f-132">Numero</span><span class="sxs-lookup"><span data-stu-id="8116f-132">Number</span></span>
- <span data-ttu-id="8116f-133">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="8116f-133">SocialSecurityNumber</span></span>
- <span data-ttu-id="8116f-134">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="8116f-134">CreditCardNumber</span></span>
- <span data-ttu-id="8116f-135">Posta elettronica</span><span class="sxs-lookup"><span data-stu-id="8116f-135">Email</span></span>

<span data-ttu-id="8116f-136">Il valore predefinito è default.</span><span class="sxs-lookup"><span data-stu-id="8116f-136">The default value is Default.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: NoMasking, Default, Text, Number, SocialSecurityNumber, CreditCardNumber, Email

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8116f-137">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="8116f-137">-NumberFrom</span></span>
<span data-ttu-id="8116f-138">Specifica il numero limite inferiore dell'intervallo da cui viene selezionato un valore casuale.</span><span class="sxs-lookup"><span data-stu-id="8116f-138">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="8116f-139">Specifica questo parametro solo se specifichi un valore di Number per il parametro *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="8116f-139">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="8116f-140">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="8116f-140">The default value is 0.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8116f-141">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="8116f-141">-NumberTo</span></span>
<span data-ttu-id="8116f-142">Specifica il numero limite superiore dell'intervallo da cui viene selezionato un valore casuale.</span><span class="sxs-lookup"><span data-stu-id="8116f-142">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="8116f-143">Specifica questo parametro solo se specifichi un valore di Number per il parametro *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="8116f-143">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="8116f-144">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="8116f-144">The default value is 0.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8116f-145">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8116f-145">-PassThru</span></span>
<span data-ttu-id="8116f-146">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="8116f-146">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8116f-147">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="8116f-147">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8116f-148">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="8116f-148">-PrefixSize</span></span>
<span data-ttu-id="8116f-149">Specifica il numero di caratteri all'inizio del testo che non sono mascherati.</span><span class="sxs-lookup"><span data-stu-id="8116f-149">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="8116f-150">Specifica questo parametro solo se specifichi un valore di testo per il parametro *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="8116f-150">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="8116f-151">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="8116f-151">The default value is 0.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8116f-152">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="8116f-152">-ReplacementString</span></span>
<span data-ttu-id="8116f-153">Specifica il numero di caratteri alla fine del testo che non sono mascherati.</span><span class="sxs-lookup"><span data-stu-id="8116f-153">Specifies the number of characters in the end of the text that are not masked.</span></span>
<span data-ttu-id="8116f-154">Specifica questo parametro solo se specifichi un valore di testo per il parametro *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="8116f-154">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="8116f-155">Il valore predefinito è una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="8116f-155">The default value is an empty string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8116f-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8116f-156">-ResourceGroupName</span></span>
<span data-ttu-id="8116f-157">Specifica il nome del gruppo di risorse a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="8116f-157">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="8116f-158">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="8116f-158">-SchemaName</span></span>
<span data-ttu-id="8116f-159">Specifica il nome di uno schema.</span><span class="sxs-lookup"><span data-stu-id="8116f-159">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="8116f-160">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="8116f-160">-ServerName</span></span>
<span data-ttu-id="8116f-161">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="8116f-161">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="8116f-162">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="8116f-162">-SuffixSize</span></span>
<span data-ttu-id="8116f-163">Specifica il numero di caratteri alla fine del testo che non sono mascherati.</span><span class="sxs-lookup"><span data-stu-id="8116f-163">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="8116f-164">Specifica questo parametro solo se specifichi un valore di testo per il parametro *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="8116f-164">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="8116f-165">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="8116f-165">The default value is 0.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8116f-166">-TableName</span><span class="sxs-lookup"><span data-stu-id="8116f-166">-TableName</span></span>
<span data-ttu-id="8116f-167">Specifica il nome della tabella di database che contiene la colonna mascherata.</span><span class="sxs-lookup"><span data-stu-id="8116f-167">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="8116f-168">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8116f-168">-Confirm</span></span>
<span data-ttu-id="8116f-169">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8116f-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8116f-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8116f-170">-WhatIf</span></span>
<span data-ttu-id="8116f-171">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8116f-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8116f-172">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8116f-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8116f-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8116f-173">CommonParameters</span></span>
<span data-ttu-id="8116f-174">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8116f-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8116f-175">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8116f-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8116f-176">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8116f-176">INPUTS</span></span>

###  
<span data-ttu-id="8116f-177">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="8116f-177">None.</span></span>

## <span data-ttu-id="8116f-178">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8116f-178">OUTPUTS</span></span>

### <span data-ttu-id="8116f-179">Microsoft. Azure. Commands. SQL. Security. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="8116f-179">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="8116f-180">Note</span><span class="sxs-lookup"><span data-stu-id="8116f-180">NOTES</span></span>

## <span data-ttu-id="8116f-181">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8116f-181">RELATED LINKS</span></span>

[<span data-ttu-id="8116f-182">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="8116f-182">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="8116f-183">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="8116f-183">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="8116f-184">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="8116f-184">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="8116f-185">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="8116f-185">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


