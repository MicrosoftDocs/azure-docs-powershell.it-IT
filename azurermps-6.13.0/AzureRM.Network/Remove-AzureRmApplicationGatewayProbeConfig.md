---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 40a7e63150384ac3fa2c330c079d5377c836d52e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513667"
---
# Remove-AzureRmApplicationGatewayProbeConfig

## Sinossi
Rimuove una sonda di integrità da un gateway applicazione esistente.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Remove-AzureRmApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet Remove-AzureRmApplicationGatewayProbeConfig consente di rimuovere una sonda di integrità da un gateway applicazione esistente.

## ESEMPI

### Esempio 1: rimuovere una sonda di integrità da un gateway applicazione esistente
```
PS C:\>$Gateway = Remove-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

Questo comando rimuove la sonda di integrità denominata Probe04 dal gateway dell'applicazione denominata gateway.

## PARAMETRI

### -ApplicationGateway
Specifica il gateway dell'applicazione a cui questo cmdlet rimuove un probe.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Specifica il nome del probe per cui viene rimosso questo cmdlet.

```yaml
Type: System.String
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

### Microsoft. Azure. Commands. Network. Models. PSApplicationGateway
Parametri: ApplicationGateway (ByValue)

## OUTPUT

### Microsoft. Azure. Commands. Network. Models. PSApplicationGateway

## Note

## COLLEGAMENTI CORRELATI

[Rimuovere una sonda da un gateway applicazione esistente](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[Add-AzureRmApplicationGatewayProbeConfig]()

[Get-AzureRmApplicationGatewayProbeConfig]()

[New-AzureRmApplicationGatewayProbeConfig]()

[Set-AzureRmApplicationGatewayProbeConfig]()

