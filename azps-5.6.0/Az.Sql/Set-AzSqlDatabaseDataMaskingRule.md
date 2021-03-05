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
# Set-AzSqlDatabaseDataMaskingRule

## SYNOPSIS
Imposta le proprietà di una regola di maschera dati per un database.

## SINTASSI

```
Set-AzSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Set-AzSqlDatabaseDataMaskingRule** imposta una regola di maschera dati per un database SQL Azure.
Per usare il cmdlet, specificare i parametri *ResourceGroupName,* *ServerName,* *DatabaseName* e *RuleId* per identificare la regola.
È possibile specificare uno qualsiasi dei parametri di *SchemaName,* *TableName* e *ColumnName* per ridefinire la regola.
Specificare il *parametro MaskingFunction* per modificare la modalità di maschera dei dati.
Se si specifica un valore number o text per *MaskingFunction,* è possibile specificare i parametri *NumberFrom* e *NumberTo* per la maschera numeri oppure i parametri *PrefixSize,* *ReplacementString* e *SuffixSize* per la maschera di testo.
Se il comando ha esito positivo e si specifica il parametro *PassThru,* il cmdlet restituisce un oggetto che descrive le proprietà della regola di maschera dati e gli identificatori delle regole.
Gli identificatori delle regole includono, ma non limitati a, **ResourceGroupName,** **ServerName,** **DatabaseName** e **RuleId.**
Questo cmdlet è supportato anche dal servizio SQL Server stretch database in Azure.

## ESEMPI

### Esempio 1: Modificare l'intervallo di una regola di maschera dati in un database
```powershell
PS C:\>Set-AzSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

Questo comando modifica una regola di maschera dati che contiene l'ID Regola17.
Questa regola viene applicata al database denominato Database01 nel server Server01.
Questo comando modifica i limiti dell'intervallo in cui viene generato un numero casuale come valore mascherato.
Il nuovo intervallo è compreso tra 23 e 42.

### Esempio 2

Imposta le proprietà di una regola di maschera dati per un database. (autogenerati)

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlDatabaseDataMaskingRule -ColumnName 'column1' -DatabaseName $params.databaseName -MaskingFunction NoMasking -NumberFrom 5 -NumberTo 14 -PrefixSize <UInt32> -ReplacementString <String> -ResourceGroupName $params.rgname -SchemaName 'dbo' -ServerName $params.serverName -SuffixSize <UInt32> -TableName 'table1'
```

## PARAMETERS

### -ColumnName
Specifica il nome della colonna di destinazione della regola di maschera.

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

### -DatabaseName
Specifica il nome del database.

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

### -DefaultProfile
Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure

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

### -MaskingFunction
Specifica la funzione maschera utilizzata dalla regola.
I valori accettabili per questo parametro sono:
- Impostazione predefinita
- NoMasking
- Testo
- Numero
- SocialSecurityNumber
- CreditCardNumber
- Email Il valore predefinito è Default.

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

### -NumberFrom
Specifica il numero limite inferiore dell'intervallo da cui viene selezionato un valore casuale.
Specificare questo parametro solo se si specifica un valore Numerico per il *parametro MaskingFunction.*
Il valore predefinito è 0.

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

### -NumberTo
Specifica il numero associato superiore dell'intervallo da cui viene selezionato un valore casuale.
Specificare questo parametro solo se si specifica un valore Numerico per il *parametro MaskingFunction.*
Il valore predefinito è 0.

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

### -PassThru
Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.
Per impostazione predefinita, questo cmdlet non genera alcun output.

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

### -PrefixSize
Specifica il numero di caratteri all'inizio del testo non mascherati.
Specificare questo parametro solo se si specifica un valore Di testo per il *parametro MaskingFunction.*
Il valore predefinito è 0.

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

### -ReplacementString
Specifica il numero di caratteri alla fine del testo non mascherati.
Specificare questo parametro solo se si specifica un valore Di testo per il *parametro MaskingFunction.*
Il valore predefinito è 0.

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

### -ResourceGroupName
Specifica il nome del gruppo di risorse a cui è assegnato il database.

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

### -SchemaName
Specifica il nome di uno schema.

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

### -ServerName
Specifica il nome del server che ospita il database.

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

### -SuffixSize
Specifica il numero di caratteri alla fine del testo non mascherati.
Specificare questo parametro solo se si specifica un valore Di testo per il *parametro MaskingFunction.*
Il valore predefinito è 0.

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

### -TableName
Specifica il nome della tabella di database che contiene la colonna mascherata.

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

### -Confirm
Chiede conferma prima di eseguire il cmdlet.

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

### -WhatIf
Mostra cosa accadrebbe se il cmdlet viene eseguito.
Il cmdlet non viene eseguito.

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

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### System.String

### System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.Nullable'1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## OUTPUT

### Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel

## NOTE

## COLLEGAMENTI CORRELATI

[Get-AzSqlDatabaseDataMaskingRule](./Get-AzSqlDatabaseDataMaskingRule.md)

[New-AzSqlDatabaseDataMaskingRule](./New-AzSqlDatabaseDataMaskingRule.md)

[Remove-AzSqlDatabaseDataMaskingRule](./Remove-AzSqlDatabaseDataMaskingRule.md)

[documentazione SQL database](https://docs.microsoft.com/azure/sql-database/)


