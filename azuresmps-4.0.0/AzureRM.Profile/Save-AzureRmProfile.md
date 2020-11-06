---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06a78584437021df570bc5ff2b6ec19e332bffd8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491321"
---
# Save-AzureRmProfile

## Sinossi
Salva le informazioni di autenticazione correnti da usare in altre sessioni di PowerShell.

## SINTASSI

```
Save-AzureRmProfile [[-Profile] <AzureRMProfile>] [-Path] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet Save-AzureRmProfile Salva le informazioni di autenticazione correnti da usare in altre sessioni di PowerShell.

## ESEMPI

### Esempio 1: salvataggio del profilo della sessione corrente
```
PS C:\> Add-AzureRmAccount
PS C:\> Save-AzureRmProfile -Path C:\test.json
```

Questo esempio salva il profilo Azure della sessione corrente nel file JSON fornito.

### Esempio 2: salvataggio di un profilo specifico
```
PS C:\> Save-AzureRmProfile -Profile (Add-AzureRmAccount) -Path C:\test.json
```

Questo esempio salva il profilo Azure passato al cmdlet nel file JSON fornito.

## PARAMETRI

### -Force
Sovrascrivere il file assegnato se esiste

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Specifica il percorso del file in cui salvare le informazioni di autenticazione.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Specifica il profilo Azure da cui viene letto il cmdlet.
Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.

```yaml
Type: AzureRMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Confermare
Richiede la conferma prima di eseguire il cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa succede se il cmdlet viene eseguito. Il cmdlet non viene eseguito.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

### PSAzureProfile

## Note

## COLLEGAMENTI CORRELATI

[Selezionare-AzureRMProfile]()

