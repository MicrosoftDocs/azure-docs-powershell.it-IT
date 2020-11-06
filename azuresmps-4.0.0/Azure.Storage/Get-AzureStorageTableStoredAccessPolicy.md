---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8c22b3eb95ab940670043f9ae467663c951027d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93507031"
---
# Get-AzureStorageTableStoredAccessPolicy

## Sinossi
Ottiene i criteri di accesso archiviati o i criteri per una tabella di archiviazione di Azure.

## SINTASSI

```
Get-AzureStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureStorageTableStoredAccessPolicy** elenca i criteri di accesso archiviati o i criteri per una tabella di archiviazione di Azure.

## ESEMPI

### Esempio 1: ottenere un criterio di accesso archiviato in una tabella di archiviazione
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

Questo comando consente di ottenere i criteri di accesso denominati Policy50 nella tabella di archiviazione denominata Table02.

### Esempio 2: ottenere tutti i criteri di accesso archiviati in una tabella di archiviazione
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02"
```

Questo comando consente di ottenere tutti i criteri di accesso nella tabella denominata Table02.

## PARAMETRI

### -Contesto
Specifica il contesto di archiviazione di Azure.
Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.

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

### -Policy
Specifica un criterio di accesso archiviato, che include le autorizzazioni per il token SAS (Shared Access Signature).

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tabella
Specifica il nome della tabella di archiviazione di Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

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

[New-AzureStorageTableStoredAccessPolicy](./New-AzureStorageTableStoredAccessPolicy.md)

[Remove-AzureStorageTableStoredAccessPolicy](./Remove-AzureStorageTableStoredAccessPolicy.md)

[Set-AzureStorageTableStoredAccessPolicy](./Set-AzureStorageTableStoredAccessPolicy.md)

[New-AzureStorageContext](./New-AzureStorageContext.md)


