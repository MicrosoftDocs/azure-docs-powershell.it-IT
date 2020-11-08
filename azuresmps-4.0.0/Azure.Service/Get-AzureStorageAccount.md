---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7D7D1FAE-5360-428B-AAE9-9D1109A7B67F
online version: ''
schema: 2.0.0
ms.openlocfilehash: faccd241929beca1f2423fa9c23f35793233205b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023507"
---
# Get-AzureStorageAccount

## Sinossi
Ottiene gli account di archiviazione per l'abbonamento Azure corrente.

## SINTASSI

```
Get-AzureStorageAccount [[-StorageAccountName] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureStorageAccount** restituisce un oggetto che contiene informazioni sugli account di archiviazione per l'abbonamento corrente.
Se viene specificato il parametro *StorageAccountName* , vengono restituite solo le informazioni sull'account di archiviazione specificato.

## ESEMPI

### Esempio 1: restituire tutti gli account di archiviazione
```
PS C:\> Get-AzureStorageAccount
```

Questo comando restituisce un oggetto con tutti gli account di archiviazione associati alla sottoscrizione corrente.

### Esempio 2: restituire le informazioni sull'account per un account specificato
```
PS C:\> Get-AzureStorageAccount -StorageAccountName "ContosoStore01"
```

Questo comando restituisce un oggetto con solo le informazioni dell'account ContosoStore01.

### Esempio 3: visualizzare una tabella di account di archiviazione
```
PS C:\> Get-AzureStorageAccount | Format-Table -AutoSize -Property @{Label="Name";Expression={$_.StorageAccountName}},"Label","Location"
```

Questo comando restituisce un oggetto con tutti gli account di archiviazione associati alla sottoscrizione corrente e li Visualizza come tabella che mostra il nome dell'account, l'etichetta dell'account e la posizione di archiviazione.

## PARAMETRI

### -InformationAction
Specifica il modo in cui questo cmdlet risponde a un evento informativo.

I valori accettabili per questo parametro sono i seguenti:

- Continuare
- Ignora
- Informarsi
- SilentlyContinue
- Stop
- Sospensione

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Specifica una variabile di informazioni.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
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

### -StorageAccountName
Specifica il nome di un account di archiviazione.
Se specificato, questo cmdlet restituisce solo l'oggetto account di archiviazione specificato.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

### ManagementOperationContext

## Note
* Digitare `help node-dev` per ottenere assistenza per Node.js cmdlet correlati allo sviluppo. Digitare `help php-dev` per ottenere assistenza per i cmdlet correlati allo sviluppo php.

## COLLEGAMENTI CORRELATI

[New-AzureStorageAccount](./New-AzureStorageAccount.md)

[Set-AzureStorageAccount](./Set-AzureStorageAccount.md)


