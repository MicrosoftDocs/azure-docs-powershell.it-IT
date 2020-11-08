---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 4661C479-6E3B-425D-B9D2-B36D7A83130C
online version: ''
schema: 2.0.0
ms.openlocfilehash: c3c55ebd22337a8078f3ae495b3901317f4201e0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029756"
---
# Get-AzureSqlDatabaseImportExportStatus

## Sinossi
Ottiene lo stato di una richiesta di importazione o esportazione.

## SINTASSI

### ByConnectionInfo
```
Get-AzureSqlDatabaseImportExportStatus -Username <String> -Password <String> -ServerName <String>
 -RequestId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByRequestObject
```
Get-AzureSqlDatabaseImportExportStatus -Request <ImportExportRequest> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureSqlDatabaseImportExportStatus** ottiene lo stato di una richiesta di importazione o esportazione.
Il cmdlet Start-AzureSqlDatabaseImport o Start-AzureSqlDatabaseExport avvia le richieste.
Puoi specificare l'oggetto Request usando il parametro *Request* oppure puoi identificare la richiesta usando il parametro *RequestId* e i parametri *username* , *password* e *ServerName* .

## ESEMPI

### Esempio 1: ottenere lo stato di una richiesta di esportazione
```
PS C:\> $ExportRequest = Start-AzureSqlDatabaseExport -SqlConnectionContext $SqlContext -StorageContainer $Container -DatabaseName $DatabaseName -BlobName $BlobName
PS C:\> Get-AzureSqlDatabaseImportExportStatus -Request $ExportRequest
```

Il primo comando crea una richiesta di esportazione e la archivia nella variabile $ExportRequest.

Il secondo comando ottiene lo stato della richiesta di esportazione archiviata in $ExportRequest.

## PARAMETRI

### -Password
Specifica la password necessaria per connettersi al server di database SQL di Azure.
Devi specificare questo parametro se hai specificato il parametro *RequestId* .

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### -Request
Specifica un oggetto **ImportExportRequest** .
Per ottenere un oggetto di richiesta di importazione o esportazione, usare il cmdlet Start-AzureSqlDatabaseImport o Start-AzureSqlDatabaseExport.

```yaml
Type: ImportExportRequest
Parameter Sets: ByRequestObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequestId
Specifica il GUID dell'operazione di importazione o esportazione per cui questo cmdlet ottiene lo stato.
Se specifichi questo parametro, devi specificare il *nome utente* , la *password* e i parametri *ServerName* .

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nomeserver
Specifica il nome del server di database SQL di Azure.
Devi specificare questo parametro se hai specificato il parametro *RequestId* .

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Username
Specifica il nome utente necessario per connettersi al server di database SQL di Azure.
Devi specificare questo parametro se hai specificato il parametro *RequestId* .

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

### Microsoft. WindowsAzure. Commands. SqlDatabase. Services. ImportExport. StatusInfo

## Note

## COLLEGAMENTI CORRELATI

[Database SQL di Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Ottenere lo stato Import Export database](https://msdn.microsoft.com/en-us/library/azure/dn781289.aspx)

[Operazioni per i database SQL di Azure](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Start-AzureSqlDatabaseExport](./Start-AzureSqlDatabaseExport.md)

[Start-AzureSqlDatabaseImport](./Start-AzureSqlDatabaseImport.md)


