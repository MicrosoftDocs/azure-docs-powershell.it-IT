---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 76876cb76e65c913401d62fc7f08b3cb8b5626c0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491434"
---
# New-AzureStorageQueue

## Sinossi
Crea una coda di archiviazione.

## SINTASSI

```
New-AzureStorageQueue [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzureStorageQueue** crea una coda di archiviazione in Azure.

## ESEMPI

### Esempio 1: creare una coda di archiviazione di Azure
```
PS C:\>New-AzureStorageQueue -Name "queueabc"
```

Questo esempio crea una coda di archiviazione denominata queueabc.

### Esempio 2: creare più code di archiviazione di Azure
```
PS C:\>"queue1 queue2 queue3".split() | New-AzureStorageQueue
```

Questo esempio crea più code di archiviazione.
Usa il metodo Split della classe String .NET e quindi passa i nomi sulla pipeline.

## PARAMETRI

### -Contesto
Specifica il contesto di archiviazione di Azure.
Puoi crearlo usando il cmdlet New-AzureStorageContext.

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
Specifica un nome per la coda.

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureStorageQueue](./Get-AzureStorageQueue.md)

[Remove-AzureStorageQueue](./Remove-AzureStorageQueue.md)


