---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 56026A74-A6DC-47A5-9643-5828C3D0E83B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 32219154f2036ee028b05a369c46be1d8e1def87
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029755"
---
# Get-AzureSqlDatabaseOperation

## Sinossi
Ottiene lo stato delle operazioni di database in un server Azure.

## SINTASSI

### ByConnectionContext (impostazione predefinita)
```
Get-AzureSqlDatabaseOperation -ConnectionContext <IServerDataServiceContext> [-Database <Database>]
 [-DatabaseName <String>] [-OperationGuid <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByServerName
```
Get-AzureSqlDatabaseOperation -ServerName <String> [-Database <Database>] [-DatabaseName <String>]
 [-OperationGuid <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureSqlDatabaseOperation** ottiene lo stato delle operazioni di database nel server Azure specificato.
Se specifichi solo il parametro *ServerName* o *ConnectionContext* , il cmdlet ottiene tutte le operazioni di database per il server.
Se si specifica anche un database tramite il parametro *database* o *DatabaseName* , questo cmdlet ottiene tutte le operazioni per il database specificato.
Se si specifica un GUID dell'operazione e *ServerName* o *ConnectionContext* , il cmdlet ottiene una singola operazione di database.

## ESEMPI

### Esempio 1: ottenere lo stato di tutte le operazioni di database per un database
```
PS C:\> $Operations = Get-AzureSqlDatabaseOperation -ConnectionContext $Context -DatabaseName "Database17"
```

Questo comando consente di ottenere lo stato di tutte le operazioni di database nel database denominato Database17 nel server specificato dal contesto di connessione $Context.

### Esempio 2: ottenere lo stato di tutte le operazioni di database per un server
```
PS C:\> $Operations = Get-AzureSqlDatabaseOperation -ConnectionContext $Context
```

Questo comando consente di ottenere lo stato di tutte le operazioni di database nel server che il contesto di connessione $Context specifica.

## PARAMETRI

### -ConnectionContext
Specifica il contesto di connessione di un server.

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Database
Specifica un oggetto che rappresenta un database SQL di Azure.
Se specifichi questo parametro, devi specificare il parametro *ServerName* o il parametro *ConnectionContext* .

```yaml
Type: Database
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
Specifica il nome di un database.
Se specifichi questo parametro, devi specificare il parametro *ServerName* o il parametro *ConnectionContext* .

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

### -OperationGuid
Specifica l'ID operazione che rappresenta un'operazione specifica del database per cui questo cmdlet ottiene lo stato.
Puoi ottenere gli ID operazione richiedendo tutte le operazioni di database per un server o un database SQL di Azure.
Se specifichi questo parametro, devi specificare il parametro *ServerName* o il parametro *ConnectionContext* .

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Profile
Specifica il profilo Azure da cui viene letto il cmdlet.
Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nomeserver
Specifica il nome di un server.

```yaml
Type: String
Parameter Sets: ByServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. database

### Microsoft. WindowsAzure. Commands. SqlDatabase. Model. SqlDatabaseServerContext

### System. Guid

## OUTPUT

### Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. database. DatabaseOperationResponseList []
Questo cmdlet restituisce una matrice di oggetti **DatabaseOperationResponseList** se si ottengono più operazioni.

### Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. database. DatabaseOperationResponse

## Note

## COLLEGAMENTI CORRELATI

[Database SQL di Azure](https://msdn.microsoft.com/library/ee336279.aspx)

[Stato operazione database](https://msdn.microsoft.com/en-us/library/azure/dn720371.aspx)

[Operazioni per i database SQL di Azure](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)

[New-AzureSqlDatabaseServerContext](./New-AzureSqlDatabaseServerContext.md)


