---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/resize-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
ms.openlocfilehash: b3a468f06db6d75671049b08efcf7970553c5c79
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852665"
---
# Resize-AzVirtualNetworkGateway

## Sinossi
Ridimensiona un gateway di rete virtuale esistente.

## SINTASSI

```
Resize-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Resize-AzVirtualNetworkGateway** consente di modificare l'unità di stoccaggio (SKU) per un gateway di rete virtuale.
Gli SKU determinano le funzionalità di un gateway, inclusi elementi come la velocità effettiva e il numero massimo di tunnel IP consentiti.
Azure supporta le SKU di base, standard, ad alte prestazioni, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ, in alcuni casi indicati come SKU di piccole, medie e grandi dimensioni.
Per informazioni dettagliate sulle funzionalità di ogni tipo di SKU, vedere https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ .
Tieni presente che le SKU si differenziano per i prezzi e le funzionalità.
Per altre informazioni, vedere https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .

## ESEMPI

### Esempio 1: modificare le dimensioni di un gateway di rete virtuale
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

Questo esempio modifica le dimensioni di un gateway di rete virtuale denominato ContosoVirtualGateway.
Il primo comando crea un riferimento all'oggetto a ContosoVirtualGateway; Questo riferimento oggetto è archiviato in una variabile denominata $Gateway.
Il secondo comando usa quindi il cmdlet **Resize-AzVirtualNetworkGateway** per impostare la proprietà *GatewaySku* su Basic.

## PARAMETRI

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GatewaySku
Specifica il nuovo tipo di SKU gateway.
I valori accettabili per questo parametro sono i seguenti:
- Base
- Standard
- Prestazioni elevate
- VpnGw1
- VpnGw2
- VpnGw3
- VpnGw1AZ 
- VpnGw2AZ 
- VpnGw3AZ 
- ErGw1AZ 
- ErGw2AZ 
- ErGw3AZ 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGateway
Specifica un riferimento a un oggetto al gateway di rete virtuale da ridimensionare.
Puoi creare questo riferimento di oggetto usando la Get-AzVirtualNetworkGateway e specificando il nome del gateway.

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

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway

### System. String

## OUTPUT

### Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway

## Note
Non è possibile eseguire il ridimensionamento dagli SKU Basic/standard/HighPerformance alle nuove SKU VpnGw1/VpnGw2/VpnGw3. Il ridimensionamento ulteriore non è consentito da/a VpnGw1AZ/VpnGw2AZ/VpnGw3AZ o ErGw1AZ/ErGw2AZ/ErGw3AZ. Il ridimensionamento è consentito solo all'interno della serie SKU, ad esempio VpnGw1AZ può essere ridimensionato in/da VpnGw2AZ/VpnGw3AZ e ErGw1AZ può essere ridimensionato in/da ErGw2AZ/ErGw3AZ. Vedere https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways per istruzioni.

## COLLEGAMENTI CORRELATI

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[New-AzVirtualNetworkGateway](./New-AzVirtualNetworkGateway.md)

[Remove-AzVirtualNetworkGateway](./Remove-AzVirtualNetworkGateway.md)

[Reset-AzVirtualNetworkGateway](./Reset-AzVirtualNetworkGateway.md)

[Set-AzVirtualNetworkGateway](./Set-AzVirtualNetworkGateway.md)

[Get-AzVpnClientPackage](./Get-AzVpnClientPackage.md)

[Set-AzVirtualNetworkGatewayVpnClientConfig](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)
