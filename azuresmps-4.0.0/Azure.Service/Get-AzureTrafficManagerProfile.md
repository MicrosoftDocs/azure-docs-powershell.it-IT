---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 28136DC3-520B-4134-8736-93D86EEABAE1
online version: ''
schema: 2.0.0
ms.openlocfilehash: bf9fd7b67b63ce2bddb762c7006722b6035ffe87
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023494"
---
# Get-AzureTrafficManagerProfile

## Sinossi
Ottiene i dettagli di un profilo di gestione traffico.

## SINTASSI

```
Get-AzureTrafficManagerProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureTrafficManagerProfile** ottiene i dettagli di un profilo di gestione traffico di Microsoft Azure.
Se non specifichi il parametro *Name* , il cmdlet elenca i profili di Traffic Manager nell'abbonamento corrente.

## ESEMPI

### Esempio 1: ottenere l'elenco dei profili di Traffic Manager in un abbonamento
```
PS C:\>Get-AzureTrafficManagerProfile
```

Questo comando consente di ottenere l'elenco dei profili di Traffic Manager nell'abbonamento.

### Esempio 2: ottenere un profilo di Traffic Manager
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile"
```

Questo comando consente di ottenere il profilo Traffic Manager denominato profilo.

### Esempio 3: aggiungere un endpoint a un profilo di gestione traffico
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile" | Add-AzureTrafficManagerEndpoint -DomainName "Myapp2.cloudapp.net" -TrafficManagerProfile $MyTrafficManagerProfile -Type "CloudService" -Status "Enabled" | Set-AzureTrafficManagerProfile
```

Questo comando aggiunge un endpoint a un profilo di Traffic Manager e quindi Salva il profilo.

## PARAMETRI

### -Nome
Specifica il nome del profilo di Traffic Manager da ottenere.

```yaml
Type: String
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

### Microsoft. WindowsAzure. Commands. Utilities. TrafficManager. Models. IProfileWithDefinition
Questo cmdlet genera un oggetto o oggetti del profilo di Traffic Manager.

## Note

## COLLEGAMENTI CORRELATI

[Add-AzureTrafficManagerEndpoint](./Add-AzureTrafficManagerEndpoint.md)

[Disable-AzureTrafficManagerProfile](./Disable-AzureTrafficManagerProfile.md)

[Enable-AzureTrafficManagerProfile](./Enable-AzureTrafficManagerProfile.md)

[New-AzureTrafficManagerProfile](./New-AzureTrafficManagerProfile.md)

[Remove-AzureTrafficManagerProfile](./Remove-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


