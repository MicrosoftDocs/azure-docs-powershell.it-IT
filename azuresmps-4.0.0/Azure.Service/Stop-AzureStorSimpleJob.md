---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A1E143A8-70F2-4158-9A10-F2082AD62A73
online version: ''
schema: 2.0.0
ms.openlocfilehash: 371291f4bd33809bc2f5880e4380c448219ed37a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029474"
---
# Stop-AzureStorSimpleJob

## Sinossi
Interrompe un processo di StorSimple.

## SINTASSI

```
Stop-AzureStorSimpleJob -InstanceId <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Stop-AzureStorSimpleJob** arresta un processo StorSimple in corso.
Puoi specificare i processi fornendo un ID istanza o un nome processo.

## ESEMPI

### Esempio 1: arrestare i processi per un dispositivo
```
PS C:\>Get-AzureStorSimpleJob -DeviceName "Device07" | Stop-AzureStorSimpleJob -Force
```

Questo comando ottiene i processi per il dispositivo denominato Device07, usando il cmdlet **Get-AzureStorSimpleJob** .
Il comando passa i processi al cmdlet corrente usando l'operatore pipeline.
Il cmdlet corrente interrompe i processi passati al comando.
Il comando specifica il parametro *Force* e quindi non chiede conferma prima di arrestare un processo.

### Esempio 2: interrompere un processo specifico
```
PS C:\>Stop-AzureStorSimpleJob -InstanceId "574f47e0-44e9-495c-b8a5-0203c57ebf6d" -Force
```

Questo comando interrompe il processo con l'ID istanza specificato.

## PARAMETRI

### -Force
Impone l'esecuzione del comando senza richiedere la conferma dell'utente.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstanceId
Specifica l'ID del processo del dispositivo da interrompere.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profile
Specifica un profilo Azure.

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

### Nessuno

## OUTPUT

### DeviceJobDetails
Questo cmdlet ottiene i dettagli della **DeviceJob** che questo cmdlet si arresta.

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureStorSimpleJob](./Get-AzureStorSimpleJob.md)


