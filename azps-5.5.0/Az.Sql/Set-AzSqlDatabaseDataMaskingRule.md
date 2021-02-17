---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 48CF206C-AF63-4013-834E-8EC3646D180B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 544db2f0e23cb510c81fb64898b6bcf856e760e5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188007"
---
# <span data-ttu-id="15eb7-101">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="15eb7-101">Set-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="15eb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15eb7-102">SYNOPSIS</span></span>
<span data-ttu-id="15eb7-103">Imposta le proprietà di una regola di maschera dati per un database.</span><span class="sxs-lookup"><span data-stu-id="15eb7-103">Sets the properties of a data masking rule for a database.</span></span>

## <span data-ttu-id="15eb7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="15eb7-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="15eb7-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="15eb7-105">DESCRIPTION</span></span>
<span data-ttu-id="15eb7-106">Il **cmdlet Set-AzSqlDatabaseDataMaskingRule** imposta una regola di maschera dati per un database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="15eb7-106">The **Set-AzSqlDatabaseDataMaskingRule** cmdlet sets a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="15eb7-107">Per usare il cmdlet, specificare i parametri *ResourceGroupName,* *ServerName,* *DatabaseName* e *RuleId* per identificare la regola.</span><span class="sxs-lookup"><span data-stu-id="15eb7-107">To use the cmdlet, provide the *ResourceGroupName*, *ServerName*, *DatabaseName*, and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="15eb7-108">È possibile specificare uno qualsiasi dei parametri di *SchemaName,* *TableName* e *ColumnName* per ridefinire la regola.</span><span class="sxs-lookup"><span data-stu-id="15eb7-108">You can provide any of the parameters of *SchemaName*, *TableName*, and *ColumnName* to retarget the rule.</span></span>
<span data-ttu-id="15eb7-109">Specificare il *parametro MaskingFunction* per modificare la modalità di maschera dei dati.</span><span class="sxs-lookup"><span data-stu-id="15eb7-109">Specify the *MaskingFunction* parameter to modify how the data is masked.</span></span>
<span data-ttu-id="15eb7-110">Se si specifica un valore Number o Text per *MaskingFunction,* è possibile specificare i parametri *NumberFrom* e *NumberTo* per la maschera numeri oppure i parametri *PrefixSize,* *ReplacementString* e *SuffixSize* per la maschera di testo.</span><span class="sxs-lookup"><span data-stu-id="15eb7-110">If you specify a value of Number or Text for *MaskingFunction*, you can specify the *NumberFrom* and *NumberTo* parameters for number masking or the *PrefixSize*, *ReplacementString*, and *SuffixSize* parameters for text masking.</span></span>
<span data-ttu-id="15eb7-111">Se il comando ha esito positivo e si specifica il parametro *PassThru,* il cmdlet restituisce un oggetto che descrive le proprietà della regola di maschera dati e gli identificatori delle regole.</span><span class="sxs-lookup"><span data-stu-id="15eb7-111">If the command succeeds, and if you specify the *PassThru* parameter, the cmdlet returns an object that describes the data masking rule properties and the rule identifiers.</span></span>
<span data-ttu-id="15eb7-112">Gli identificatori delle regole includono, ma non limitati a, **ResourceGroupName,** **ServerName,** **DatabaseName** e **RuleId.**</span><span class="sxs-lookup"><span data-stu-id="15eb7-112">Rule identifiers include, but are not limited to, **ResourceGroupName**, **ServerName**, **DatabaseName**, and **RuleId**.</span></span>
<span data-ttu-id="15eb7-113">Questo cmdlet è supportato anche dal servizio SQL Server di estensione del database in Azure.</span><span class="sxs-lookup"><span data-stu-id="15eb7-113">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="15eb7-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="15eb7-114">EXAMPLES</span></span>

### <span data-ttu-id="15eb7-115">Esempio 1: Modificare l'intervallo di una regola di maschera dati in un database</span><span class="sxs-lookup"><span data-stu-id="15eb7-115">Example 1: Change the range of a data masking rule in a database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

<span data-ttu-id="15eb7-116">Questo comando modifica una regola di maschera dati che contiene l'ID Regola17.</span><span class="sxs-lookup"><span data-stu-id="15eb7-116">This command modifies a data masking rule that has the ID Rule17.</span></span>
<span data-ttu-id="15eb7-117">Questa regola viene applicata al database denominato Database01 nel server Server01.</span><span class="sxs-lookup"><span data-stu-id="15eb7-117">That rule operates in the database named Database01 on server Server01.</span></span>
<span data-ttu-id="15eb7-118">Questo comando modifica i limiti dell'intervallo in cui viene generato un numero casuale come valore mascherato.</span><span class="sxs-lookup"><span data-stu-id="15eb7-118">This command changes the boundaries for the interval in which a random number is generated as the masked value.</span></span>
<span data-ttu-id="15eb7-119">Il nuovo intervallo è compreso tra 23 e 42.</span><span class="sxs-lookup"><span data-stu-id="15eb7-119">The new range is between 23 and 42.</span></span>

### <span data-ttu-id="15eb7-120">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="15eb7-120">Example 2</span></span>

<span data-ttu-id="15eb7-121">Imposta le proprietà di una regola di maschera dati per un database.</span><span class="sxs-lookup"><span data-stu-id="15eb7-121">Sets the properties of a data masking rule for a database.</span></span> <span data-ttu-id="15eb7-122">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="15eb7-122">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlDatabaseDataMaskingRule -ColumnName 'column1' -DatabaseName $params.databaseName -MaskingFunction NoMasking -NumberFrom 5 -NumberTo 14 -PrefixSize <UInt32> -ReplacementString <String> -ResourceGroupName $params.rgname -SchemaName 'dbo' -ServerName $params.serverName -SuffixSize <UInt32> -TableName 'table1'
```

## <span data-ttu-id="15eb7-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="15eb7-123">PARAMETERS</span></span>

### <span data-ttu-id="15eb7-124">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="15eb7-124">-ColumnName</span></span>
<span data-ttu-id="15eb7-125">Specifica il nome della colonna di destinazione della regola di maschera.</span><span class="sxs-lookup"><span data-stu-id="15eb7-125">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="15eb7-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="15eb7-126">-DatabaseName</span></span>
<span data-ttu-id="15eb7-127">Specifica il nome del database.</span><span class="sxs-lookup"><span data-stu-id="15eb7-127">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="15eb7-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15eb7-128">-DefaultProfile</span></span>
<span data-ttu-id="15eb7-129">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="15eb7-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="15eb7-130">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="15eb7-130">-MaskingFunction</span></span>
<span data-ttu-id="15eb7-131">Specifica la funzione maschera utilizzata dalla regola.</span><span class="sxs-lookup"><span data-stu-id="15eb7-131">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="15eb7-132">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="15eb7-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="15eb7-133">Impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="15eb7-133">Default</span></span>
- <span data-ttu-id="15eb7-134">NoMasking</span><span class="sxs-lookup"><span data-stu-id="15eb7-134">NoMasking</span></span>
- <span data-ttu-id="15eb7-135">Testo</span><span class="sxs-lookup"><span data-stu-id="15eb7-135">Text</span></span>
- <span data-ttu-id="15eb7-136">Numero</span><span class="sxs-lookup"><span data-stu-id="15eb7-136">Number</span></span>
- <span data-ttu-id="15eb7-137">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="15eb7-137">SocialSecurityNumber</span></span>
- <span data-ttu-id="15eb7-138">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="15eb7-138">CreditCardNumber</span></span>
- <span data-ttu-id="15eb7-139">Email Il valore predefinito è Default.</span><span class="sxs-lookup"><span data-stu-id="15eb7-139">Email The default value is Default.</span></span>

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

### <span data-ttu-id="15eb7-140">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="15eb7-140">-NumberFrom</span></span>
<span data-ttu-id="15eb7-141">Specifica il numero limite inferiore dell'intervallo da cui viene selezionato un valore casuale.</span><span class="sxs-lookup"><span data-stu-id="15eb7-141">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="15eb7-142">Specificare questo parametro solo se si specifica il valore Number per il *parametro MaskingFunction.*</span><span class="sxs-lookup"><span data-stu-id="15eb7-142">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="15eb7-143">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="15eb7-143">The default value is 0.</span></span>

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

### <span data-ttu-id="15eb7-144">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="15eb7-144">-NumberTo</span></span>
<span data-ttu-id="15eb7-145">Specifica il numero associato superiore dell'intervallo da cui viene selezionato un valore casuale.</span><span class="sxs-lookup"><span data-stu-id="15eb7-145">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="15eb7-146">Specificare questo parametro solo se si specifica il valore Number per il *parametro MaskingFunction.*</span><span class="sxs-lookup"><span data-stu-id="15eb7-146">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="15eb7-147">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="15eb7-147">The default value is 0.</span></span>

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

### <span data-ttu-id="15eb7-148">-PassThru</span><span class="sxs-lookup"><span data-stu-id="15eb7-148">-PassThru</span></span>
<span data-ttu-id="15eb7-149">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="15eb7-149">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="15eb7-150">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="15eb7-150">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="15eb7-151">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="15eb7-151">-PrefixSize</span></span>
<span data-ttu-id="15eb7-152">Specifica il numero di caratteri all'inizio del testo non mascherato.</span><span class="sxs-lookup"><span data-stu-id="15eb7-152">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="15eb7-153">Specificare questo parametro solo se si specifica un valore Di testo per il *parametro MaskingFunction.*</span><span class="sxs-lookup"><span data-stu-id="15eb7-153">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="15eb7-154">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="15eb7-154">The default value is 0.</span></span>

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

### <span data-ttu-id="15eb7-155">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="15eb7-155">-ReplacementString</span></span>
<span data-ttu-id="15eb7-156">Specifica il numero di caratteri alla fine del testo non mascherati.</span><span class="sxs-lookup"><span data-stu-id="15eb7-156">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="15eb7-157">Specificare questo parametro solo se si specifica un valore Di testo per il *parametro MaskingFunction.*</span><span class="sxs-lookup"><span data-stu-id="15eb7-157">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="15eb7-158">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="15eb7-158">The default value is 0.</span></span>

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

### <span data-ttu-id="15eb7-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15eb7-159">-ResourceGroupName</span></span>
<span data-ttu-id="15eb7-160">Specifica il nome del gruppo di risorse a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="15eb7-160">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="15eb7-161">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="15eb7-161">-SchemaName</span></span>
<span data-ttu-id="15eb7-162">Specifica il nome di uno schema.</span><span class="sxs-lookup"><span data-stu-id="15eb7-162">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="15eb7-163">-ServerName</span><span class="sxs-lookup"><span data-stu-id="15eb7-163">-ServerName</span></span>
<span data-ttu-id="15eb7-164">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="15eb7-164">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="15eb7-165">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="15eb7-165">-SuffixSize</span></span>
<span data-ttu-id="15eb7-166">Specifica il numero di caratteri alla fine del testo non mascherati.</span><span class="sxs-lookup"><span data-stu-id="15eb7-166">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="15eb7-167">Specificare questo parametro solo se si specifica un valore Di testo per il *parametro MaskingFunction.*</span><span class="sxs-lookup"><span data-stu-id="15eb7-167">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="15eb7-168">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="15eb7-168">The default value is 0.</span></span>

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

### <span data-ttu-id="15eb7-169">-TableName</span><span class="sxs-lookup"><span data-stu-id="15eb7-169">-TableName</span></span>
<span data-ttu-id="15eb7-170">Specifica il nome della tabella di database che contiene la colonna mascherata.</span><span class="sxs-lookup"><span data-stu-id="15eb7-170">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="15eb7-171">-Confirm</span><span class="sxs-lookup"><span data-stu-id="15eb7-171">-Confirm</span></span>
<span data-ttu-id="15eb7-172">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15eb7-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15eb7-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15eb7-173">-WhatIf</span></span>
<span data-ttu-id="15eb7-174">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="15eb7-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15eb7-175">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="15eb7-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15eb7-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15eb7-176">CommonParameters</span></span>
<span data-ttu-id="15eb7-177">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15eb7-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15eb7-178">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="15eb7-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15eb7-179">INPUT</span><span class="sxs-lookup"><span data-stu-id="15eb7-179">INPUTS</span></span>

### <span data-ttu-id="15eb7-180">System.String</span><span class="sxs-lookup"><span data-stu-id="15eb7-180">System.String</span></span>

### <span data-ttu-id="15eb7-181">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="15eb7-181">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="15eb7-182">System.Nullable'1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="15eb7-182">System.Nullable\`1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="15eb7-183">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="15eb7-183">OUTPUTS</span></span>

### <span data-ttu-id="15eb7-184">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="15eb7-184">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="15eb7-185">NOTE</span><span class="sxs-lookup"><span data-stu-id="15eb7-185">NOTES</span></span>

## <span data-ttu-id="15eb7-186">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="15eb7-186">RELATED LINKS</span></span>

[<span data-ttu-id="15eb7-187">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="15eb7-187">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="15eb7-188">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="15eb7-188">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="15eb7-189">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="15eb7-189">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="15eb7-190">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="15eb7-190">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


