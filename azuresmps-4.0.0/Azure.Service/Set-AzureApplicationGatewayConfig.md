---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D7D99AFA-A85E-43DA-9F2F-8FFD34048E00
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7ede675ab58905f102fb9d0029669115acdb9e85
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029891"
---
# Set-AzureApplicationGatewayConfig

## Sinossi
Configura un gateway dell'applicazione.

## SINTASSI

### configFile
```
Set-AzureApplicationGatewayConfig -Name <String> -ConfigFile <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### configObject
```
Set-AzureApplicationGatewayConfig -Name <String> -Config <ApplicationGatewayConfiguration>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **set-AzureApplicationGatewayConfig** configura un gateway dell'applicazione.

## ESEMPI

### Esempio 1: configurare un gateway dell'applicazione usando un oggetto Configuration
```
PS C:\> $ConfigReturnObject = Get-AzureApplicationGatewayConfig -Name "ApplicationGateway02"
PS C:\> Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -Config $ConfigReturnObject
```

Il primo comando ottiene l'oggetto Configuration per il gateway dell'applicazione denominato ApplicationGateway02 usando il cmdlet **Get-AzureApplicationGatewayConfig** .
Il comando lo archivia nella variabile $ConfigReturnObject.

Il secondo comando imposta la configurazione per l'applicazione denominata ApplicationGateway06 tramite un oggetto di configurazione gateway applicazione archiviato nella variabile $ConfigReturnObject.

### Esempio 2: configurare un gateway dell'applicazione usando un file di configurazione
```
PS C:\> Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -ConfigFile "D:\config.xml"
```

Questo comando imposta la configurazione per l'applicazione denominata ApplicationGateway06 usando un file di configurazione del gateway applicazione nella posizione specificata.

### Esempio 3: modificare una configurazione usando un oggetto Configuration
```
PS C:\> $ConfigReturnObject = Get-AzureApplicationGatewayConfig -Name "ApplicationGateway06"
PS C:\> $ConfigReturnObject.Config.FrontendPorts[0].Port = 443
PS C:\> $ConfigReturnObject | Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06"
```

Il primo comando ottiene l'oggetto Configuration per il gateway dell'applicazione denominato ApplicationGateway06 usando il cmdlet **Get-AzureApplicationGatewayConfig** .
Il comando lo archivia nella variabile $ConfigReturnObject.

Il secondo comando assegna un valore di porta a una proprietà della **porta** nell'oggetto archiviato in $ConfigReturnObject.

Il comando finale passa la $ConfigReturnObject aggiornata al cmdlet corrente.

## PARAMETRI

### -Config
Specifica un oggetto di configurazione gateway applicazione.
Questo cmdlet assegna la configurazione specificata da questo parametro a un gateway dell'applicazione.

```yaml
Type: ApplicationGatewayConfiguration
Parameter Sets: configObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigFile
Specifica il percorso di un file di configurazione, in formato XML, per un gateway dell'applicazione.
Questo cmdlet assegna la configurazione specificata da questo parametro a un gateway dell'applicazione.

```yaml
Type: String
Parameter Sets: configFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Specifica il nome del gateway dell'applicazione configurato da questo cmdlet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
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

### System. String, Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayConfiguration

## OUTPUT

### Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureApplicationGatewayConfig](./Get-AzureApplicationGatewayConfig.md)


