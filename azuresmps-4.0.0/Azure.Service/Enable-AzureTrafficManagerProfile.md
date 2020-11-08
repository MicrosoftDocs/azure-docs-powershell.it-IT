---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 51A1B699-03F6-4BB9-9186-FDFFB094F16A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 72420272e04519fa888660f8ccb6d432ecb0ee5d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029837"
---
# Enable-AzureTrafficManagerProfile

## Sinossi
Abilita un profilo di Traffic Manager.

## SINTASSI

```
Enable-AzureTrafficManagerProfile -Name <String> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Enable-AzureTrafficManagerProfile** Abilita un profilo di Microsoft Azure Traffic Manager.
Specifica il parametro *PassThru* per visualizzare se l'operazione viene eseguita correttamente.

## ESEMPI

### Esempio 1: abilitare un profilo di Traffic Manager
```
PS C:\>Enable-AzureTrafficManagerProfile -Name "MyProfile"
```

Questo comando consente al profilo di gestione traffico denominato profilo.

### Esempio 2: abilitare un profilo di Traffic Manager e visualizzare i risultati
```
PS C:\>Enable-AzureTrafficManagerProfile -Name "MyProfile" -PassThru
True
```

Questo comando consente al profilo di gestione traffico denominato profilo e indica se il comando è stato completato.

## PARAMETRI

### -Nome
Specifica il nome del profilo di Traffic Manager da abilitare.

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

### -PassThru
Restituisce $True se l'operazione è riuscita; in caso contrario, $False.
Per impostazione predefinita, questo cmdlet non genera alcun output.

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

### -Profile
Specifica il profilo Azure da cui viene letto il cmdlet. Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.

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

### System. Boolean
Questo cmdlet genera $True o $False.
Se l'operazione viene eseguita correttamente e se specifichi il parametro *PassThru* , questo cmdlet restituisce un valore di $true.

## Note

## COLLEGAMENTI CORRELATI

[Disable-AzureTrafficManagerProfile](./Disable-AzureTrafficManagerProfile.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[New-AzureTrafficManagerProfile](./New-AzureTrafficManagerProfile.md)

[Remove-AzureTrafficManagerProfile](./Remove-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


