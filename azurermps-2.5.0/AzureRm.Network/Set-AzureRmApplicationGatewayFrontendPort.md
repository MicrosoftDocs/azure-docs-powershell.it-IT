---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 85C0A1C3-FC6D-496A-B6B5-8DC2A73B8032
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayfrontendport
schema: 2.0.0
ms.openlocfilehash: 83c29e3c059664d7848fe66bd8ad7bcc005a8d47
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866971"
---
# Set-AzureRmApplicationGatewayFrontendPort

## Sinossi
Modifica una porta front-end per un gateway dell'applicazione.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Set-AzureRmApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **set-AzureRmApplicationGatewayFrontendPort** modifica una porta front-end per un gateway dell'applicazione.

## ESEMPI

### Esempio 1: impostare una porta di front-end gateway applicazione in 80
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.

Il secondo comando modifica il gateway in $AppGw per usare la porta 80 per la porta front-end denominata FrontEndPort01.

## PARAMETRI

### -ApplicationGateway
Specifica l'oggetto gateway dell'applicazione con cui questo cmdlet associa la porta front-end.

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Specifica il nome della porta front-end da modificare.

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

### -Porta
Specifica il numero di porta da usare per la porta front-end.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### PSApplicationGateway
Il parametro ' ApplicationGateway ' accetta il valore di tipo ' PSApplicationGateway ' dalla pipeline

## OUTPUT

### Microsoft. Azure. Commands. Network. Models. PSApplicationGateway

## Note

## COLLEGAMENTI CORRELATI

[Add-AzureRmApplicationGatewayFrontendPort](./Add-AzureRmApplicationGatewayFrontendPort.md)

[Get-AzureRmApplicationGatewayFrontendPort](./Get-AzureRmApplicationGatewayFrontendPort.md)

[New-AzureRmApplicationGatewayFrontendPort](./New-AzureRmApplicationGatewayFrontendPort.md)

[Remove-AzureRmApplicationGatewayFrontendPort](./Remove-AzureRmApplicationGatewayFrontendPort.md)
