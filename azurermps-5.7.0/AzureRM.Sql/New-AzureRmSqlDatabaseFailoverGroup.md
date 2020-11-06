---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 71f4796e33ec512f9d0aa2eb27f78ba615eefef1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507851"
---
# New-AzureRmSqlDatabaseFailoverGroup

## Sinossi
Questo comando crea un nuovo gruppo di failover di database SQL di Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
New-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> -FailoverGroupName <String>
 [-PartnerResourceGroupName <String>] -PartnerServerName <String> [-FailoverPolicy <FailoverPolicy>]
 [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Crea un nuovo gruppo di failover di database SQL di Azure per i server specificati.

Due endpoint TDS di database SQL di Azure vengono creati in FailoverGroupName. SqlDatabaseDnsSuffix (ad esempio, FailoverGroupName.database.windows.net) e FailoverGroupName. Secondary. SqlDatabaseDnsSuffix. Questi endpoint possono essere usati per connettersi rispettivamente ai server primari e secondari nel gruppo di failover. Se il server primario è influenzato da un'interruzione, il failover automatico degli endpoint e dei database viene attivato come dettato dai criteri di failover e dal periodo di tolleranza del gruppo di failover.

I gruppi di failover appena creati non contengono database. Per controllare il set di database in un gruppo di failover, usare i cmdlet "Add-AzureRmSqlDatabaseToFailoverGroup" e "Remove-AzureRmSqlDatabaseFromFailoverGroup".

Durante l'anteprima della caratteristica gruppi di failover, per il parametro '-GracePeriodWithDataLossHours ' sono supportati solo i valori maggiori o uguali a 1 ora.

## ESEMPI

### Esempio 1
```
C:\> $failoverGroup = New-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -PartnerServerName secondaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

Questo comando crea un nuovo gruppo di failover con il criterio di failover "automatico" per due server nello stesso gruppo di risorse.

### Esempio 2
```
C:\> $failoverGroup = New-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg1 -ServerName primaryserver -PartnerResourceGroupName rg2 -PartnerServerName secondaryserver1 -FailoverGroupName fg -FailoverPolicy Manual
```

Questo comando crea un nuovo gruppo di failover con i criteri di failover "manuale" per due server in gruppi di risorse diversi.

## PARAMETRI

### -AllowReadOnlyFailoverToPrimary
Se un'interruzione nel server secondario deve attivare il failover automatico dell'endpoint di sola lettura. Questa caratteristica non è ancora supportata.

```yaml
Type: AllowReadOnlyFailoverToPrimary
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
Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure

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

### -FailoverGroupName
Il nome del gruppo di failover di database SQL di Azure da creare.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FailoverPolicy
Criteri di failover del gruppo di failover di database SQL di Azure.

```yaml
Type: FailoverPolicy
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
Intervallo prima che venga avviato il failover automatico se si verifica un'interruzione nel server primario e non è possibile completare il failover senza perdita di dati.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerResourceGroupName
Il nome del gruppo di risorse secondarie del gruppo di failover di database SQL di Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerServerName
Nome del server secondario del gruppo di failover di database SQL di Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nome del gruppo di risorse.

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

### -Nomeserver
Nome del server di database SQL di Azure principale del gruppo di failover.

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

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### System. String

## OUTPUT

### System. Object

## Note

## COLLEGAMENTI CORRELATI

[Set-AzureRmSqlDatabaseFailoverGroup](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[Get-AzureRmSqlDatabaseFailoverGroup](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[Add-AzureRmSqlDatabaseToFailoverGroup](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[Remove-AzureRmSqlDatabaseFromFailoverGroup](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[Switch-AzureRmSqlDatabaseFailoverGroup](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[Remove-AzureRmSqlDatabaseFailoverGroup](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[Documentazione di database SQL](https://docs.microsoft.com/azure/sql-database/)
