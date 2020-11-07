---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 48CF206C-AF63-4013-834E-8EC3646D180B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 9038fae93cf8f79962a19960da8c103820335961
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676755"
---
# <span data-ttu-id="cf7cb-101">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="cf7cb-101">Set-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="cf7cb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cf7cb-102">SYNOPSIS</span></span>
<span data-ttu-id="cf7cb-103">Imposta le proprietà di una regola di mascheramento dei dati per un database.</span><span class="sxs-lookup"><span data-stu-id="cf7cb-103">Sets the properties of a data masking rule for a database.</span></span>

## <span data-ttu-id="cf7cb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cf7cb-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cf7cb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cf7cb-105">DESCRIPTION</span></span>
<span data-ttu-id="cf7cb-106">Il cmdlet **set-AzSqlDatabaseDataMaskingRule** imposta una regola per la mascheratura dei dati per un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="cf7cb-106">The **Set-AzSqlDatabaseDataMaskingRule** cmdlet sets a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="cf7cb-107">Per usare il cmdlet, fornisci i parametri *ResourceGroupName* , *ServerName* , *DatabaseName* e *RuleId* per identificare la regola.</span><span class="sxs-lookup"><span data-stu-id="cf7cb-107">To use the cmdlet, provide the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="cf7cb-108">Puoi specificare qualsiasi parametro di *SchemaName* , *TableName* e *ColumnName* per ridefinire la destinazione della regola.</span><span class="sxs-lookup"><span data-stu-id="cf7cb-108">You can provide any of the parameters of *SchemaName* , *TableName* , and *ColumnName* to retarget the rule.</span></span>
<span data-ttu-id="cf7cb-109">Specifica il parametro *MaskingFunction* per modificare il modo in cui i dati vengono mascherati.</span><span class="sxs-lookup"><span data-stu-id="cf7cb-109">Specify the *MaskingFunction* parameter to modify how the data is masked.</span></span>
<span data-ttu-id="cf7cb-110">Se specifichi un valore di Number o text per *MaskingFunction* , puoi specificare i parametri *NumberFrom* e *NumberTo* per la maschera dei numeri o i parametri *PrefixSize* , *ReplacementString* e *SuffixSize* per la mascheratura del testo.</span><span class="sxs-lookup"><span data-stu-id="cf7cb-110">If you specify a value of Number or Text for *MaskingFunction* , you can specify the *NumberFrom* and *NumberTo* parameters for number masking or the *PrefixSize* , *ReplacementString* , and *SuffixSize* parameters for text masking.</span></span>
<span data-ttu-id="cf7cb-111">Se il comando riesce e se specifichi il parametro *PassThru* , il cmdlet restituisce un oggetto che descrive le proprietà della regola per la mascheratura dei dati e gli identificatori di regola.</span><span class="sxs-lookup"><span data-stu-id="cf7cb-111">If the command succeeds, and if you specify the *PassThru* parameter, the cmdlet returns an object that describes the data masking rule properties and the rule identifiers.</span></span>
<span data-ttu-id="cf7cb-112">Gli identificatori di regole includono, ma non sono limitati a, **ResourceGroupName** , **nomeserver** , **DatabaseName** e **RuleId**.</span><span class="sxs-lookup"><span data-stu-id="cf7cb-112">Rule identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , **DatabaseName** , and **RuleId**.</span></span>
<span data-ttu-id="cf7cb-113">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="cf7cb-113">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="cf7cb-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cf7cb-114">EXAMPLES</span></span>

### <span data-ttu-id="cf7cb-115">Esempio 1: modificare l'intervallo di una regola di mascheramento dei dati in un database</span><span class="sxs-lookup"><span data-stu-id="cf7cb-115">Example 1: Change the range of a data masking rule in a database</span></span>
```
PS C:\>Set-AzSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

<span data-ttu-id="cf7cb-116">Questo comando consente di modificare una regola di mascheramento dei dati con ID Rule17.</span><span class="sxs-lookup"><span data-stu-id="cf7cb-116">This command modifies a data masking rule that has the ID Rule17.</span></span>
<span data-ttu-id="cf7cb-117">Questa regola opera nel database denominato Database01 nel server Server01.</span><span class="sxs-lookup"><span data-stu-id="cf7cb-117">That rule operates in the database named Database01 on server Server01.</span></span>
<span data-ttu-id="cf7cb-118">Questo comando modifica i limiti per l'intervallo in cui viene generato un numero casuale come valore mascherato.</span><span class="sxs-lookup"><span data-stu-id="cf7cb-118">This command changes the boundaries for the interval in which a random number is generated as the masked value.</span></span>
<span data-ttu-id="cf7cb-119">Il nuovo intervallo è compreso tra 23 e 42.</span><span class="sxs-lookup"><span data-stu-id="cf7cb-119">The new range is between 23 and 42.</span></span>

## <span data-ttu-id="cf7cb-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cf7cb-120">PARAMETERS</span></span>

### <span data-ttu-id="cf7cb-121">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="cf7cb-121">-ColumnName</span></span>
<span data-ttu-id="cf7cb-122">Specifica il nome della colonna di destinazione della regola di mascheramento.</span><span class="sxs-lookup"><span data-stu-id="cf7cb-122">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="cf7cb-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cf7cb-123">-DatabaseName</span></span>
<span data-ttu-id="cf7cb-124">Specifica il nome del database.</span><span class="sxs-lookup"><span data-stu-id="cf7cb-124">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="cf7cb-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf7cb-125">-DefaultProfile</span></span>
<span data-ttu-id="cf7cb-126">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="cf7cb-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf7cb-127">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="cf7cb-127">-MaskingFunction</span></span>
<span data-ttu-id="cf7cb-128">Specifica la funzione di mascheramento utilizzata dalla regola.</span><span class="sxs-lookup"><span data-stu-id="cf7cb-128">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="cf7cb-129">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="cf7cb-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cf7cb-130">Predefinita</span><span class="sxs-lookup"><span data-stu-id="cf7cb-130">Default</span></span>
- <span data-ttu-id="cf7cb-131">Nomasking</span><span class="sxs-lookup"><span data-stu-id="cf7cb-131">NoMasking</span></span>
- <span data-ttu-id="cf7cb-132">Testo</span><span class="sxs-lookup"><span data-stu-id="cf7cb-132">Text</span></span>
- <span data-ttu-id="cf7cb-133">Numero</span><span class="sxs-lookup"><span data-stu-id="cf7cb-133">Number</span></span>
- <span data-ttu-id="cf7cb-134">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="cf7cb-134">SocialSecurityNumber</span></span>
- <span data-ttu-id="cf7cb-135">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="cf7cb-135">CreditCardNumber</span></span>
- <span data-ttu-id="cf7cb-136">Messaggio di posta elettronica il valore predefinito è default.</span><span class="sxs-lookup"><span data-stu-id="cf7cb-136">Email The default value is Default.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NoMasking, Default, Text, Number, SocialSecurityNumber, CreditCardNumber, Email

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf7cb-137">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="cf7cb-137">-NumberFrom</span></span>
<span data-ttu-id="cf7cb-138">Specifica il numero limite inferiore dell'intervallo da cui viene selezionato un valore casuale.</span><span class="sxs-lookup"><span data-stu-id="cf7cb-138">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="cf7cb-139">Specifica questo parametro solo se specifichi un valore di Number per il parametro *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="cf7cb-139">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="cf7cb-140">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="cf7cb-140">The default value is 0.</span></span>

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

### <span data-ttu-id="cf7cb-141">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="cf7cb-141">-NumberTo</span></span>
<span data-ttu-id="cf7cb-142">Specifica il numero limite superiore dell'intervallo da cui viene selezionato un valore casuale.</span><span class="sxs-lookup"><span data-stu-id="cf7cb-142">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="cf7cb-143">Specifica questo parametro solo se specifichi un valore di Number per il parametro *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="cf7cb-143">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="cf7cb-144">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="cf7cb-144">The default value is 0.</span></span>

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

### <span data-ttu-id="cf7cb-145">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cf7cb-145">-PassThru</span></span>
<span data-ttu-id="cf7cb-146">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="cf7cb-146">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cf7cb-147">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="cf7cb-147">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cf7cb-148">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="cf7cb-148">-PrefixSize</span></span>
<span data-ttu-id="cf7cb-149">Specifica il numero di caratteri all'inizio del testo che non sono mascherati.</span><span class="sxs-lookup"><span data-stu-id="cf7cb-149">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="cf7cb-150">Specifica questo parametro solo se specifichi un valore di testo per il parametro *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="cf7cb-150">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="cf7cb-151">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="cf7cb-151">The default value is 0.</span></span>

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

### <span data-ttu-id="cf7cb-152">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="cf7cb-152">-ReplacementString</span></span>
<span data-ttu-id="cf7cb-153">Specifica il numero di caratteri alla fine del testo che non sono mascherati.</span><span class="sxs-lookup"><span data-stu-id="cf7cb-153">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="cf7cb-154">Specifica questo parametro solo se specifichi un valore di testo per il parametro *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="cf7cb-154">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="cf7cb-155">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="cf7cb-155">The default value is 0.</span></span>

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

### <span data-ttu-id="cf7cb-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf7cb-156">-ResourceGroupName</span></span>
<span data-ttu-id="cf7cb-157">Specifica il nome del gruppo di risorse a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="cf7cb-157">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="cf7cb-158">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="cf7cb-158">-SchemaName</span></span>
<span data-ttu-id="cf7cb-159">Specifica il nome di uno schema.</span><span class="sxs-lookup"><span data-stu-id="cf7cb-159">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="cf7cb-160">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="cf7cb-160">-ServerName</span></span>
<span data-ttu-id="cf7cb-161">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="cf7cb-161">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="cf7cb-162">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="cf7cb-162">-SuffixSize</span></span>
<span data-ttu-id="cf7cb-163">Specifica il numero di caratteri alla fine del testo che non sono mascherati.</span><span class="sxs-lookup"><span data-stu-id="cf7cb-163">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="cf7cb-164">Specifica questo parametro solo se specifichi un valore di testo per il parametro *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="cf7cb-164">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="cf7cb-165">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="cf7cb-165">The default value is 0.</span></span>

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

### <span data-ttu-id="cf7cb-166">-TableName</span><span class="sxs-lookup"><span data-stu-id="cf7cb-166">-TableName</span></span>
<span data-ttu-id="cf7cb-167">Specifica il nome della tabella di database che contiene la colonna mascherata.</span><span class="sxs-lookup"><span data-stu-id="cf7cb-167">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="cf7cb-168">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cf7cb-168">-Confirm</span></span>
<span data-ttu-id="cf7cb-169">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf7cb-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf7cb-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf7cb-170">-WhatIf</span></span>
<span data-ttu-id="cf7cb-171">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cf7cb-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf7cb-172">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cf7cb-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf7cb-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf7cb-173">CommonParameters</span></span>
<span data-ttu-id="cf7cb-174">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf7cb-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf7cb-175">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf7cb-175">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf7cb-176">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cf7cb-176">INPUTS</span></span>

### <span data-ttu-id="cf7cb-177">System. String</span><span class="sxs-lookup"><span data-stu-id="cf7cb-177">System.String</span></span>

### <span data-ttu-id="cf7cb-178">System. Nullable ' 1 [[System. UInt32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="cf7cb-178">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="cf7cb-179">System. Nullable ' 1 [[System. Double, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="cf7cb-179">System.Nullable\`1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="cf7cb-180">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cf7cb-180">OUTPUTS</span></span>

### <span data-ttu-id="cf7cb-181">Microsoft. Azure. Commands. SQL. datamasking. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="cf7cb-181">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="cf7cb-182">Note</span><span class="sxs-lookup"><span data-stu-id="cf7cb-182">NOTES</span></span>

## <span data-ttu-id="cf7cb-183">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cf7cb-183">RELATED LINKS</span></span>

[<span data-ttu-id="cf7cb-184">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="cf7cb-184">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="cf7cb-185">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="cf7cb-185">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="cf7cb-186">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="cf7cb-186">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="cf7cb-187">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="cf7cb-187">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

