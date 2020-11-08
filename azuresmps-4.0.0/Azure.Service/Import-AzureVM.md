---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7180CAC6-BFC1-4A18-A754-83D5F05C5BEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: c62c30558147bccd9cdecc73925b7e1a379d1c5b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029717"
---
# Import-AzureVM

## Sinossi
Importa uno stato di una macchina virtuale Azure da un file.

## SINTASSI

```
Import-AzureVM [-Path] <String> [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **Import-AzureVM** importa lo stato salvato in precedenza di una macchina virtuale da un file XML.
Questo cmdlet è utile quando si vuole creare una macchina virtuale dai dati importati in un momento successivo.

L'esecuzione di **Export-AzureVM** , seguita da **Remove-AzureVM** e quindi **Import-AzureVM** per ricreare una macchina virtuale può far sì che la macchina virtuale risultante abbia un indirizzo IP diverso rispetto all'originale.

## ESEMPI

### Esempio 1: importare uno stato macchina virtuale
```
PS C:\> Import-AzureVM -Path "C:\VMstate.xml" | New-AzureVM -ServiceName "ContosoService02"
```

Questo comando importa lo stato di una macchina virtuale dal file VMstate.xml e quindi crea una macchina virtuale nel servizio cloud specificato.

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

### -Path
Specifica il percorso del file con lo stato della macchina virtuale salvato in precedenza.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
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

[Export-AzureVM](./Export-AzureVM.md)

[New-AzureVM](./New-AzureVM.md)


