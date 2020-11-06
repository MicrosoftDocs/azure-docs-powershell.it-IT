---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 11a8ffe26a65bf2ecabab7807d8e54bc23b629fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93507060"
---
# Get-AzureStorageQueue

## Sinossi
Elenca le code di archiviazione.

## SINTASSI

### QueueName (impostazione predefinita)
```
Get-AzureStorageQueue [[-Name] <String>] [-Context <IStorageContext>] [<CommonParameters>]
```

### QueuePrefix
```
Get-AzureStorageQueue -Prefix <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureStorageQueue** elenca le code di archiviazione associate a un account di archiviazione di Azure.

## ESEMPI

### Esempio 1: elencare tutte le code di archiviazione di Azure
```
PS C:\>Get-AzureStorageQueue
```

Questo comando consente di ottenere un elenco di tutte le code di archiviazione per l'account di archiviazione corrente.

### Esempio 2: elencare le code di archiviazione di Azure usando un carattere jolly
```
PS C:\>Get-AzureStorageQueue -Name queue*
```

Questo comando usa un carattere jolly per ottenere un elenco delle code di archiviazione il cui nome inizia con Queue.

### Esempio 3: code di archiviazione di elenchi di Azure tramite il prefisso del nome della coda
```
PS C:\>Get-AzureStorageQueue -Prefix "queue"
```

Questo esempio usa il parametro *Prefix* per ottenere un elenco delle code di archiviazione il cui nome inizia con Queue.

## PARAMETRI

### -Contesto
Specifica il contesto di archiviazione di Azure.
Puoi crearlo usando il cmdlet **New-AzureStorageContext** .

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Nome
Specifica un nome.
Se non viene specificato alcun nome, il cmdlet riceve un elenco di tutte le code.
Se viene specificato un nome completo o parziale, il cmdlet ottiene tutte le code che corrispondono al modello di nome.

```yaml
Type: String
Parameter Sets: QueueName
Aliases: N, Queue

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Prefisso
Specifica un prefisso usato nel nome delle code che vuoi ottenere.

```yaml
Type: String
Parameter Sets: QueuePrefix
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

## Note

## COLLEGAMENTI CORRELATI

[New-AzureStorageQueue](./New-AzureStorageQueue.md)

[Remove-AzureStorageQueue](./Remove-AzureStorageQueue.md)


