---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Resize-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Resize-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 9f7b85ed3c8f7c1c64ec89f8575975dde81fed7c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688609"
---
# Resize-AzureRmVirtualNetworkGateway

## Sinossi
Ridimensiona un gateway di rete virtuale esistente.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Resize-AzureRmVirtualNetworkGateway** consente di modificare l'unità di stoccaggio (SKU) per un gateway di rete virtuale.
Gli SKU determinano le funzionalità di un gateway, inclusi elementi come la velocità effettiva e il numero massimo di tunnel IP consentiti.
Azure supporta SKU di base, standard, ad alte prestazioni, VpnGw1, VpnGw2 e VpnGw3 (a volte denominate SKU di piccole, medie e grandi dimensioni).
Per informazioni dettagliate sulle funzionalità di ogni tipo di SKU, vedere https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ .

Tieni presente che le SKU si differenziano per i prezzi e le funzionalità.
Per altre informazioni, vedere https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .

## ESEMPI

### Esempio 1: modificare le dimensioni di un gateway di rete virtuale
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

Questo esempio modifica le dimensioni di un gateway di rete virtuale denominato ContosoVirtualGateway.

Il primo comando crea un riferimento all'oggetto a ContosoVirtualGateway; Questo riferimento oggetto è archiviato in una variabile denominata $Gateway.

Il secondo comando usa quindi il cmdlet **Resize-AzureRmVirtualNetworkGateway** per impostare la proprietà *GatewaySku* su Basic.

## PARAMETRI

### -GatewaySku
Specifica il nuovo tipo di SKU gateway.
I valori accettabili per questo parametro sono i seguenti:

- Base
- Standard
- Prestazioni elevate
- VpnGw1
- VpnGw2
- VpnGw3

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGateway
Specifica un riferimento a un oggetto al gateway di rete virtuale da ridimensionare.
Puoi creare questo riferimento di oggetto usando la Get-AzureRmVirtualNetworkGateway e specificando il nome del gateway.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
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

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

###  
Questo cmdlet accetta le istanze pipeline dell'oggetto **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** .

## OUTPUT

###  
Questo cmdlet modifica le istanze esistenti dell'oggetto **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** .

## Note
Non è possibile eseguire il ridimensionamento dagli SKU Basic/standard/HighPerformance alle nuove SKU VpnGw1/VpnGw2/VpnGw3. Vedere https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways per istruzioni.

## COLLEGAMENTI CORRELATI

[Get-AzureRmVpnClientPackage](./Get-AzureRmVpnClientPackage.md)

[Get-AzureRmVirtualNetworkGateway](./Get-AzureRmVirtualNetworkGateway.md)

[Set-AzureRmVirtualNetworkGatewayVpnClientConfig](./Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md)


