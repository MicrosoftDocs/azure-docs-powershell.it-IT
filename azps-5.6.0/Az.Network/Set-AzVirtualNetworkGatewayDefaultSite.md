---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/powershell/module/az.network/set-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 8e35347813849badfa50100cc4cac418e2d66332
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979438"
---
# Set-AzVirtualNetworkGatewayDefaultSite

## SYNOPSIS
Imposta il sito predefinito per un gateway di rete virtuale.

## SINTASSI

```
Set-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Set-AzVirtualNetworkGatewayDefaultSite** assegna un sito predefinito di tunneling forzato a un gateway di rete virtuale.
Il tunneling forzato consente di reindirizzare il traffico associato a Internet dalle macchine virtuali di Azure alla rete locale; in questo modo è possibile controllare e controllare il traffico prima di rilasciarlo.
Il tunneling forzato viene eseguito usando un tunnel VPN; questo tunnel richiede un sito predefinito, un gateway locale in cui viene reindirizzato tutto il traffico associato a Internet di Azure.
**Set-AzVirtualNetworkGatewayDefaultSite** consente di cambiare il sito predefinito assegnato a un gateway.

## ESEMPI

### Esempio 1: Assegnare un sito predefinito a un gateway di rete virtuale
```
PS C:\>$LocalGateway = Get-AzLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

Questo esempio assegna un sito predefinito a un gateway di rete virtuale denominato ContosoVirtualGateway.
Il primo comando crea un riferimento a un oggetto a un gateway locale denominato ContosoLocalGateway.
Questo riferimento all'oggetto archiviato nella variabile $LocalGateway rappresenta il gateway da configurare come sito predefinito.
Il secondo comando crea quindi un riferimento a un oggetto al gateway di rete virtuale e archivia il risultato nella variabile $VirtualGateway.
Il terzo comando usa il cmdlet **Set-AzVirtualNetworkGatewayDefaultSite** per assegnare il sito predefinito a ContosoVirtualGateway.

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

### -GatewayDefaultSite
Specifica un riferimento a un oggetto al gateway di rete locale da assegnare come sito predefinito per la rete virtuale specificata.
È possibile usare il cmdlet Get-AzLocalNetworkGateway per creare un riferimento a un oggetto a un gateway locale.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGateway
Specifica un riferimento a un oggetto al gateway di rete virtuale a cui verrà assegnato il sito predefinito.
È possibile creare un riferimento a un oggetto a un gateway di rete virtuale usando **Get-AzVirtualNetworkGateway** e specificando il nome del gateway.
La variabile $VirtualGateway può essere usata come valore del parametro *VirtualNetworkGateway:*

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

### Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway

## OUTPUT

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway

## NOTE

## COLLEGAMENTI CORRELATI

[Get-AzLocalNetworkGateway](./Get-AzLocalNetworkGateway.md)

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[Remove-AzVirtualNetworkGatewayDefaultSite](./Remove-AzVirtualNetworkGatewayDefaultSite.md)


