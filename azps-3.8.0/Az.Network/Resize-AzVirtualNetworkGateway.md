---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/resize-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
ms.openlocfilehash: 31ec0453b0ce64c27d1bb37d4bf6c0f100a8c760
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100411756"
---
# Resize-AzVirtualNetworkGateway

## SYNOPSIS
Ridimensiona un gateway di rete virtuale esistente.

## SINTASSI

```
Resize-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Resize-AzVirtualNetworkGateway** consente di modificare l'unità di conservazione delle azioni per un gateway di rete virtuale.
Gli SKU determinano le funzionalità di un gateway, tra cui la velocità effettiva e il numero massimo di tunnel IP consentiti.
Azure supporta SKU di base, standard, ad alte prestazioni, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ (noto anche come SKU piccole, medie e grandi).
Per informazioni dettagliate sulle funzionalità di ogni tipo di SKU, vedere https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ .
Tenere presente che gli SKU variano in base ai prezzi e alle funzionalità.
Per altre informazioni, vedere https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .

## ESEMPI

### Esempio 1: Modificare le dimensioni di un gateway di rete virtuale
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

Questo esempio modifica le dimensioni di un gateway di rete virtuale denominato ContosoVirtualGateway.
Il primo comando crea un riferimento a un oggetto a ContosoVirtualGateway; questo riferimento all'oggetto è archiviato in una variabile denominata $Gateway.
Il secondo comando usa quindi il cmdlet **Resize-AzVirtualNetworkGateway** per impostare la proprietà *GatewaySku* su Basic.

## PARAMETERS

### -DefaultProfile
Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.

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
Specifica il nuovo tipo di SKU del gateway.
I valori accettabili per questo parametro sono:
- Di base
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
È possibile creare questo riferimento all'oggetto usando Get-AzVirtualNetworkGateway e specificando il nome del gateway.

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
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway

### System.String

## OUTPUT

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway

## NOTE
Non è possibile eseguire il ridimensionamento dagli SKU Di base/Standard/HighPerformance alle nuove SKU VpnGw1/VpnGw2/VpnGw3. Ulteriori ridimensionamento non sono consentiti da/a VpnGw1AZ/VpnGw2AZ/VpnGw3AZ o ErGw1AZ/ErGw2AZ/ErGw3AZ. Il ridimensionamento è consentito solo all'interno della "serie" SKU, ad esempio VpnGw1AZ può essere ridimensionato in/da VpnGw2AZ/VpnGw3AZ e ErGw1AZ possono essere ridimensionati in/da ErGw2AZ/ErGw3AZ. Per https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways istruzioni, vedere.

## COLLEGAMENTI CORRELATI

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[New-AzVirtualNetworkGateway](./New-AzVirtualNetworkGateway.md)

[Remove-AzVirtualNetworkGateway](./Remove-AzVirtualNetworkGateway.md)

[Reset-AzVirtualNetworkGateway](./Reset-AzVirtualNetworkGateway.md)

[Set-AzVirtualNetworkGateway](./Set-AzVirtualNetworkGateway.md)

[Get-AzVpnClientPackage](./Get-AzVpnClientPackage.md)

