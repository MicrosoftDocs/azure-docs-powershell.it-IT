---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A1815E7F-720E-4526-A779-106C181B840D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22b04496d9ce310b58662c62b70a195e8cfa8878
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029493"
---
# Start-AzureEmulator

## Sinossi
Avvia gli emulatori COMPUTE e storage.

## SINTASSI

```
Start-AzureEmulator [-Launch] [-Mode <ComputeEmulatorMode>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.
Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .

Il cmdlet **Start-AzureEmulator** avvia sia gli emulatori Compute che storage e ospita il servizio corrente nell'emulatore di calcolo.

## ESEMPI

### Esempio 1: avviare l'emulatore e avviare un browser
```
PS C:\> Start-AzureEmulator -L
```

In questo esempio viene eseguito il servizio nell'emulatore di Azure e viene avviata una nuova finestra del browser nel servizio emulato.

## PARAMETRI

### -Avvio
Apre una nuova finestra del browser nel servizio dopo averla ospitata nell'emulatore.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ln

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Modalità
Specifica la modalità di emulazione.
I valori validi sono: Full ed Express.
Il valore predefinito è Express.

```yaml
Type: ComputeEmulatorMode
Parameter Sets: (All)
Aliases: 

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

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

## Note

## COLLEGAMENTI CORRELATI

[New-AzureServiceProject](./New-AzureServiceProject.md)

[Publish-AzureServiceProject](./Publish-AzureServiceProject.md)

[Stop-AzureEmulator](./Stop-AzureEmulator.md)


