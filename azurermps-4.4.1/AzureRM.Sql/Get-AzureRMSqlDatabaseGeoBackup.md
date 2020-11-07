---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 256AA6F4-D856-4713-A0AC-0DA1A145AA5C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDatabaseGeoBackup.md
ms.openlocfilehash: ad46883722f0c9d4c4d8bf5a5f5f568bb267bba5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688226"
---
# Get-AzureRmSqlDatabaseGeoBackup

## Sinossi
Ottiene un backup Geo-ridondante di un database.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Get-AzureRmSqlDatabaseGeoBackup [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureRMSqlDatabaseGeoBackup** ottiene un backup Geo-ridondante specificato di un database SQL o di tutti i backup Geo-ridondanti disponibili in un server specificato.

Un backup Geo-ridondante è una risorsa ripristinabile che usa file di dati da una posizione geografica distinta.
Puoi usare Geo-Restore per ripristinare un backup Geo-ridondante in caso di interruzioni locali per recuperare il database in una nuova area geografica.

Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.

## ESEMPI

### Esempio 1: ottenere tutti i backup Geo-ridondanti in un server
```
PS C:\>Get-AzureRMSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

Questo comando ottiene tutti i backup Geo-ridondanti disponibili in un server specificato.

### Esempio 2: ottenere un backup Geo-ridondante specificato
```
PS C:\>Get-AzureRMSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

Questo comando consente di ottenere il backup Geo-ridondante del database denominato ContosoDatabase.

## PARAMETRI

### -DatabaseName
Specifica il nome del database da ottenere.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome del gruppo di risorse a cui è assegnato il server di database SQL.

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

### -Nomeserver
Specifica il nome del server che ospita il backup da ripristinare.

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

### -Confermare
Richiede la conferma prima di eseguire il cmdlet.

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
Mostra cosa succede se il cmdlet viene eseguito.
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

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

### Microsoft. Azure. Commands. SQL. backup. Model. AzureSqlDatabaseGeoBackupModel

## Note

## COLLEGAMENTI CORRELATI

[Panoramica: cloud business continuity e ripristino di emergenza del database con database SQL](https://go.microsoft.com/fwlink/?LinkId=746881)

[Recuperare un database SQL di Azure da un'interruzione](https://go.microsoft.com/fwlink/?LinkId=746882)

[Ripristinare-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md)

[Documentazione di database SQL](https://docs.microsoft.com/azure/sql-database/)
