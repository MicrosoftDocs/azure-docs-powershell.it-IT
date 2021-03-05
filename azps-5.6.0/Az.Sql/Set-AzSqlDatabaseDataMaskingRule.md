---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 48CF206C-AF63-4013-834E-8EC3646D180B
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 8ed90e6c3a145298029f1ef4d12b6248ed39526e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994921"
---
# <span data-ttu-id="62978-101">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="62978-101">Set-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="62978-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62978-102">SYNOPSIS</span></span>
<span data-ttu-id="62978-103">Imposta le proprietà di una regola di maschera dati per un database.</span><span class="sxs-lookup"><span data-stu-id="62978-103">Sets the properties of a data masking rule for a database.</span></span>

## <span data-ttu-id="62978-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="62978-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="62978-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="62978-105">DESCRIPTION</span></span>
<span data-ttu-id="62978-106">Il cmdlet **Set-AzSqlDatabaseDataMaskingRule** imposta una regola di maschera dati per un database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="62978-106">The **Set-AzSqlDatabaseDataMaskingRule** cmdlet sets a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="62978-107">Per usare il cmdlet, specificare i parametri *ResourceGroupName,* *ServerName,* *DatabaseName* e *RuleId* per identificare la regola.</span><span class="sxs-lookup"><span data-stu-id="62978-107">To use the cmdlet, provide the *ResourceGroupName*, *ServerName*, *DatabaseName*, and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="62978-108">È possibile specificare uno qualsiasi dei parametri di *SchemaName,* *TableName* e *ColumnName* per ridefinire la regola.</span><span class="sxs-lookup"><span data-stu-id="62978-108">You can provide any of the parameters of *SchemaName*, *TableName*, and *ColumnName* to retarget the rule.</span></span>
<span data-ttu-id="62978-109">Specificare il *parametro MaskingFunction* per modificare la modalità di maschera dei dati.</span><span class="sxs-lookup"><span data-stu-id="62978-109">Specify the *MaskingFunction* parameter to modify how the data is masked.</span></span>
<span data-ttu-id="62978-110">Se si specifica un valore number o text per *MaskingFunction,* è possibile specificare i parametri *NumberFrom* e *NumberTo* per la maschera numeri oppure i parametri *PrefixSize,* *ReplacementString* e *SuffixSize* per la maschera di testo.</span><span class="sxs-lookup"><span data-stu-id="62978-110">If you specify a value of Number or Text for *MaskingFunction*, you can specify the *NumberFrom* and *NumberTo* parameters for number masking or the *PrefixSize*, *ReplacementString*, and *SuffixSize* parameters for text masking.</span></span>
<span data-ttu-id="62978-111">Se il comando ha esito positivo e si specifica il parametro *PassThru,* il cmdlet restituisce un oggetto che descrive le proprietà della regola di maschera dati e gli identificatori delle regole.</span><span class="sxs-lookup"><span data-stu-id="62978-111">If the command succeeds, and if you specify the *PassThru* parameter, the cmdlet returns an object that describes the data masking rule properties and the rule identifiers.</span></span>
<span data-ttu-id="62978-112">Gli identificatori delle regole includono, ma non limitati a, **ResourceGroupName,** **ServerName,** **DatabaseName** e **RuleId.**</span><span class="sxs-lookup"><span data-stu-id="62978-112">Rule identifiers include, but are not limited to, **ResourceGroupName**, **ServerName**, **DatabaseName**, and **RuleId**.</span></span>
<span data-ttu-id="62978-113">Questo cmdlet è supportato anche dal servizio SQL Server stretch database in Azure.</span><span class="sxs-lookup"><span data-stu-id="62978-113">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="62978-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="62978-114">EXAMPLES</span></span>

### <span data-ttu-id="62978-115">Esempio 1: Modificare l'intervallo di una regola di maschera dati in un database</span><span class="sxs-lookup"><span data-stu-id="62978-115">Example 1: Change the range of a data masking rule in a database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

<span data-ttu-id="62978-116">Questo comando modifica una regola di maschera dati che contiene l'ID Regola17.</span><span class="sxs-lookup"><span data-stu-id="62978-116">This command modifies a data masking rule that has the ID Rule17.</span></span>
<span data-ttu-id="62978-117">Questa regola viene applicata al database denominato Database01 nel server Server01.</span><span class="sxs-lookup"><span data-stu-id="62978-117">That rule operates in the database named Database01 on server Server01.</span></span>
<span data-ttu-id="62978-118">Questo comando modifica i limiti dell'intervallo in cui viene generato un numero casuale come valore mascherato.</span><span class="sxs-lookup"><span data-stu-id="62978-118">This command changes the boundaries for the interval in which a random number is generated as the masked value.</span></span>
<span data-ttu-id="62978-119">Il nuovo intervallo è compreso tra 23 e 42.</span><span class="sxs-lookup"><span data-stu-id="62978-119">The new range is between 23 and 42.</span></span>

### <span data-ttu-id="62978-120">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="62978-120">Example 2</span></span>

<span data-ttu-id="62978-121">Imposta le proprietà di una regola di maschera dati per un database.</span><span class="sxs-lookup"><span data-stu-id="62978-121">Sets the properties of a data masking rule for a database.</span></span> <span data-ttu-id="62978-122">(autogenerati)</span><span class="sxs-lookup"><span data-stu-id="62978-122">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlDatabaseDataMaskingRule -ColumnName 'column1' -DatabaseName $params.databaseName -MaskingFunction NoMasking -NumberFrom 5 -NumberTo 14 -PrefixSize <UInt32> -ReplacementString <String> -ResourceGroupName $params.rgname -SchemaName 'dbo' -ServerName $params.serverName -SuffixSize <UInt32> -TableName 'table1'
```

## <span data-ttu-id="62978-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62978-123">PARAMETERS</span></span>

### <span data-ttu-id="62978-124">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="62978-124">-ColumnName</span></span>
<span data-ttu-id="62978-125">Specifica il nome della colonna di destinazione della regola di maschera.</span><span class="sxs-lookup"><span data-stu-id="62978-125">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="62978-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="62978-126">-DatabaseName</span></span>
<span data-ttu-id="62978-127">Specifica il nome del database.</span><span class="sxs-lookup"><span data-stu-id="62978-127">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="62978-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62978-128">-DefaultProfile</span></span>
<span data-ttu-id="62978-129">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="62978-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62978-130">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="62978-130">-MaskingFunction</span></span>
<span data-ttu-id="62978-131">Specifica la funzione maschera utilizzata dalla regola.</span><span class="sxs-lookup"><span data-stu-id="62978-131">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="62978-132">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="62978-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="62978-133">Impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="62978-133">Default</span></span>
- <span data-ttu-id="62978-134">NoMasking</span><span class="sxs-lookup"><span data-stu-id="62978-134">NoMasking</span></span>
- <span data-ttu-id="62978-135">Testo</span><span class="sxs-lookup"><span data-stu-id="62978-135">Text</span></span>
- <span data-ttu-id="62978-136">Numero</span><span class="sxs-lookup"><span data-stu-id="62978-136">Number</span></span>
- <span data-ttu-id="62978-137">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="62978-137">SocialSecurityNumber</span></span>
- <span data-ttu-id="62978-138">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="62978-138">CreditCardNumber</span></span>
- <span data-ttu-id="62978-139">Email Il valore predefinito è Default.</span><span class="sxs-lookup"><span data-stu-id="62978-139">Email The default value is Default.</span></span>

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

### <span data-ttu-id="62978-140">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="62978-140">-NumberFrom</span></span>
<span data-ttu-id="62978-141">Specifica il numero limite inferiore dell'intervallo da cui viene selezionato un valore casuale.</span><span class="sxs-lookup"><span data-stu-id="62978-141">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="62978-142">Specificare questo parametro solo se si specifica un valore Numerico per il *parametro MaskingFunction.*</span><span class="sxs-lookup"><span data-stu-id="62978-142">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="62978-143">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="62978-143">The default value is 0.</span></span>

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

### <span data-ttu-id="62978-144">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="62978-144">-NumberTo</span></span>
<span data-ttu-id="62978-145">Specifica il numero associato superiore dell'intervallo da cui viene selezionato un valore casuale.</span><span class="sxs-lookup"><span data-stu-id="62978-145">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="62978-146">Specificare questo parametro solo se si specifica un valore Numerico per il *parametro MaskingFunction.*</span><span class="sxs-lookup"><span data-stu-id="62978-146">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="62978-147">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="62978-147">The default value is 0.</span></span>

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

### <span data-ttu-id="62978-148">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62978-148">-PassThru</span></span>
<span data-ttu-id="62978-149">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="62978-149">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="62978-150">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="62978-150">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="62978-151">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="62978-151">-PrefixSize</span></span>
<span data-ttu-id="62978-152">Specifica il numero di caratteri all'inizio del testo non mascherati.</span><span class="sxs-lookup"><span data-stu-id="62978-152">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="62978-153">Specificare questo parametro solo se si specifica un valore Di testo per il *parametro MaskingFunction.*</span><span class="sxs-lookup"><span data-stu-id="62978-153">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="62978-154">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="62978-154">The default value is 0.</span></span>

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

### <span data-ttu-id="62978-155">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="62978-155">-ReplacementString</span></span>
<span data-ttu-id="62978-156">Specifica il numero di caratteri alla fine del testo non mascherati.</span><span class="sxs-lookup"><span data-stu-id="62978-156">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="62978-157">Specificare questo parametro solo se si specifica un valore Di testo per il *parametro MaskingFunction.*</span><span class="sxs-lookup"><span data-stu-id="62978-157">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="62978-158">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="62978-158">The default value is 0.</span></span>

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

### <span data-ttu-id="62978-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62978-159">-ResourceGroupName</span></span>
<span data-ttu-id="62978-160">Specifica il nome del gruppo di risorse a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="62978-160">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="62978-161">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="62978-161">-SchemaName</span></span>
<span data-ttu-id="62978-162">Specifica il nome di uno schema.</span><span class="sxs-lookup"><span data-stu-id="62978-162">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="62978-163">-ServerName</span><span class="sxs-lookup"><span data-stu-id="62978-163">-ServerName</span></span>
<span data-ttu-id="62978-164">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="62978-164">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="62978-165">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="62978-165">-SuffixSize</span></span>
<span data-ttu-id="62978-166">Specifica il numero di caratteri alla fine del testo non mascherati.</span><span class="sxs-lookup"><span data-stu-id="62978-166">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="62978-167">Specificare questo parametro solo se si specifica un valore Di testo per il *parametro MaskingFunction.*</span><span class="sxs-lookup"><span data-stu-id="62978-167">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="62978-168">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="62978-168">The default value is 0.</span></span>

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

### <span data-ttu-id="62978-169">-TableName</span><span class="sxs-lookup"><span data-stu-id="62978-169">-TableName</span></span>
<span data-ttu-id="62978-170">Specifica il nome della tabella di database che contiene la colonna mascherata.</span><span class="sxs-lookup"><span data-stu-id="62978-170">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="62978-171">-Confirm</span><span class="sxs-lookup"><span data-stu-id="62978-171">-Confirm</span></span>
<span data-ttu-id="62978-172">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62978-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62978-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62978-173">-WhatIf</span></span>
<span data-ttu-id="62978-174">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="62978-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62978-175">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="62978-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62978-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62978-176">CommonParameters</span></span>
<span data-ttu-id="62978-177">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62978-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62978-178">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="62978-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62978-179">INPUT</span><span class="sxs-lookup"><span data-stu-id="62978-179">INPUTS</span></span>

### <span data-ttu-id="62978-180">System.String</span><span class="sxs-lookup"><span data-stu-id="62978-180">System.String</span></span>

### <span data-ttu-id="62978-181">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="62978-181">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="62978-182">System.Nullable'1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="62978-182">System.Nullable\`1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="62978-183">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="62978-183">OUTPUTS</span></span>

### <span data-ttu-id="62978-184">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="62978-184">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="62978-185">NOTE</span><span class="sxs-lookup"><span data-stu-id="62978-185">NOTES</span></span>

## <span data-ttu-id="62978-186">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="62978-186">RELATED LINKS</span></span>

[<span data-ttu-id="62978-187">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="62978-187">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="62978-188">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="62978-188">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="62978-189">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="62978-189">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="62978-190">documentazione SQL database</span><span class="sxs-lookup"><span data-stu-id="62978-190">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


