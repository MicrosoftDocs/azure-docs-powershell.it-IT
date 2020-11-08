---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceLoggingProperty.md
ms.openlocfilehash: 21c182dff12f8dd373000a295f964bd59484e337
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191135"
---
# Set-AzStorageServiceLoggingProperty

## Sinossi
Modifica la registrazione per i servizi di archiviazione di Azure.

## SINTASSI

```
Set-AzStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **set-AzStorageServiceLoggingProperty** modifica la registrazione per i servizi di archiviazione di Azure.

## ESEMPI

### Esempio 1: modificare le proprietà di registrazione per il servizio BLOB
```
C:\PS>Set-AzStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

Questo comando modifica la registrazione della versione 1,0 per l'archiviazione BLOB per includere le operazioni di lettura e scrittura.
La registrazione del servizio di archiviazione di Azure mantiene le voci per 10 giorni.
Poiché questo comando specifica il parametro *PassThru* , il comando Visualizza le proprietà di registrazione modificate.

## PARAMETRI

### -Contesto
Specifica un contesto di archiviazione di Azure.
Per ottenere un contesto di archiviazione, usare il cmdlet New-AzStorageContext.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LoggingOperations
Specifica una matrice di operazioni del servizio di archiviazione di Azure.
Azure Storage Services registra le operazioni specificate da questo parametro.
I valori accettabili per questo parametro sono i seguenti:
- Nessuno
- Leggere
- Scrivere
- Eliminare
- Tutti

```yaml
Type: Microsoft.Azure.Storage.Shared.Protocol.LoggingOperations[]
Parameter Sets: (All)
Aliases:
Accepted values: None, Read, Write, Delete, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Indica che questo cmdlet restituisce le proprietà di registrazione aggiornate.
Se non specifichi questo parametro, questo cmdlet non restituisce un valore.

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

### -RetentionDays
Specifica il numero di giorni in cui il servizio di archiviazione di Azure mantiene le informazioni registrate.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceType
Specifica il tipo di servizio di archiviazione.
Questo cmdlet modifica le proprietà di registrazione per il tipo di servizio specificato da questo parametro.
I valori accettabili per questo parametro sono i seguenti:
- BLOB 
- tavolo
- Coda
- File il valore di file non è attualmente supportato.

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
Parameter Sets: (All)
Aliases:
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Versione
Specifica la versione della registrazione del servizio di archiviazione di Azure.
Il valore predefinito è 1,0.

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext

## OUTPUT

### Microsoft. Azure. storage. Shared. Protocol. LoggingProperties

## Note

## COLLEGAMENTI CORRELATI

[Get-AzStorageServiceLoggingProperty](./Get-AzStorageServiceLoggingProperty.md)

[New-AzStorageContext](./New-AzStorageContext.md)


