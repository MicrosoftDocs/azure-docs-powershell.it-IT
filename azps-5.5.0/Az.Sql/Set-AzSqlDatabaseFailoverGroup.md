---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 8b78cfc7a2934b4670702562941ea0e00c2a70c8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207875"
---
# Set-AzSqlDatabaseFailoverGroup

## SYNOPSIS
Modifica la configurazione di un gruppo di failover del SQL database di Azure.

## SINTASSI

```
Set-AzSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Questo comando modifica la configurazione di un gruppo di failover del SQL database di Azure.
Il server primario del gruppo di failover deve essere usato per eseguire il comando.
Per controllare il set di database nel gruppo, usare invece "Add-AzSqlDatabaseToFailoverGroup" e "Remove-AzSqlDatabaseFromFailoverGroup".
Durante l'anteprima della funzionalità Gruppi di failover, sono supportati solo i valori maggiori o uguali a 1 ora per il parametro '-GracePeriodWithDataLossHours'.

## ESEMPI

### Esempio 1
```
PS C:\> $failoverGroup = Set-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

Imposta il criterio di failover di un gruppo di failover su "Automatico".

### Esempio 2
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg | Set-AzSqlDatabaseFailoverGroup -FailoverPolicy Manual
```

Imposta il criterio di failover di un gruppo di failover su "Manuale" tramite piping nel gruppo di failover.

## PARAMETERS

### -AllowReadOnlyFailoverToPrimary
Se le interruzioni nel server secondario devono attivare il failover automatico dell'endpoint di sola lettura.

```yaml
Type: Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AllowReadOnlyFailoverToPrimary
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure

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

### -FailoverGroupName
Nome del gruppo di failover del database SQL Azure.

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

### -FailoverPolicy
Criteri di failover del gruppo di failover SQL database di Azure.

```yaml
Type: Microsoft.Azure.Commands.Sql.FailoverGroup.Model.FailoverPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: Automatic
Accept pipeline input: False
Accept wildcard characters: False
```

### -GracePeriodWithDataLossHours
Intervallo prima dell'avvio del failover automatico se si verifica un'interruzione nel server primario. Questo significa che Il database SQL Azure non avvierà il failover automatico prima della scadenza del periodo di tolleranza. Tenere presente che l'operazione di failover con l'opzione AllowDataLoss potrebbe causare la perdita di dati a causa della natura della sincronizzazione asincrona.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nome del gruppo di risorse.

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

### -ServerName
Nome del server di database SQL Azure primario del gruppo di failover.

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

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### System.String

## OUTPUT

### Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel

## NOTE

## COLLEGAMENTI CORRELATI

[New-AzSqlDatabaseFailoverGroup](./New-AzSqlDatabaseFailoverGroup.md)

[Get-AzSqlDatabaseFailoverGroup](./Get-AzSqlDatabaseFailoverGroup.md)

[Add-AzSqlDatabaseToFailoverGroup](./Add-AzSqlDatabaseToFailoverGroup.md)

[Remove-AzSqlDatabaseFromFailoverGroup](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[Switch-AzSqlDatabaseFailoverGroup](./Switch-AzSqlDatabaseFailoverGroup.md)

[Remove-AzSqlDatabaseFailoverGroup](./Remove-AzSqlDatabaseFailoverGroup.md)

[SQL documentazione del database](https://docs.microsoft.com/azure/sql-database/)
