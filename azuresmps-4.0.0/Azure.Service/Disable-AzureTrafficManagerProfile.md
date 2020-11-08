---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: ECE9C2A6-7DA2-4477-B877-9970FBE26D7C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8f378cbf8926a650699ec50a2a0a42873dcb7528
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023651"
---
# Disable-AzureTrafficManagerProfile

## Sinossi
Disabilita un profilo di gestione traffico.

## SINTASSI

```
Disable-AzureTrafficManagerProfile -Name <String> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Disable-AzureTrafficManagerProfile Disabilita** un profilo di Microsoft Azure Traffic Manager.
Puoi usare il parametro *PassThru* per visualizzare se l'operazione viene eseguita correttamente.

## ESEMPI

### Esempio 1: disabilitare un profilo di Traffic Manager e visualizzare i risultati
```
PS C:\>Disable-AzureTrafficManagerProfile -Name "MyProfile" -PassThru
True
```

Questo comando Disabilita il profilo di Traffic Manager denominato profilo.
Il comando specifica il parametro *PassThru* per visualizzare se il comando è stato completato.

### Esempio 2: disabilitare un profilo di Traffic Manager e visualizzare nessun risultato
```
PS C:\>Disable-AzureTrafficManagerProfile -Name "MyProfile"
```

Questo comando Disabilita il profilo di gestione traffico denominato profilo, ma non Visualizza se il comando è riuscito.

## PARAMETRI

### -Nome
Specifica il nome del profilo di Traffic Manager da disabilitare.

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
Se l'operazione riesce e se specifichi il parametro *PassThru* , questo cmdlet restituisce un valore di $true.

## Note

## COLLEGAMENTI CORRELATI

[Enable-AzureTrafficManagerProfile](./Enable-AzureTrafficManagerProfile.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[New-AzureTrafficManagerProfile](./New-AzureTrafficManagerProfile.md)

[Remove-AzureTrafficManagerProfile](./Remove-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


