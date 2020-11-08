---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: a4be0aed365517e1ae3ae11155f82ea097db309a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201963"
---
# Set-AzVirtualNetworkGatewayDefaultSite

## Sinossi
Imposta il sito predefinito per un gateway di rete virtuale.

## SINTASSI

```
Set-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **set-AzVirtualNetworkGatewayDefaultSite** assegna un sito predefinito per il tunneling forzato a un gateway di rete virtuale.
Il tunneling forzato consente di reindirizzare il traffico associato a Internet da macchine virtuali di Azure alla rete locale; in questo modo è possibile ispezionare e controllare il traffico prima di rilasciarlo.
Il tunneling forzato viene eseguito usando un tunnel VPN (Virtual Private Network); Questo tunnel richiede un sito predefinito, un gateway locale in cui viene reindirizzato tutto il traffico associato a Internet di Azure.
**Set-AzVirtualNetworkGatewayDefaultSite** offre un modo per cambiare il sito predefinito assegnato a un gateway.

## ESEMPI

### Esempio 1: assegnare un sito predefinito a un gateway di rete virtuale
```
PS C:\>$LocalGateway = Get-AzLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

Questo esempio assegna un sito predefinito a un gateway di rete virtuale denominato ContosoVirtualGateway.
Il primo comando crea un riferimento a un oggetto gateway locale denominato ContosoLocalGateway.
Questo riferimento a un oggetto archiviato nella variabile denominata $LocalGateway rappresenta il gateway da configurare come sito predefinito.
Il secondo comando crea quindi un riferimento a un oggetto al gateway di rete virtuale e archivia il risultato nella variabile denominata $VirtualGateway.
Il terzo comando usa il cmdlet **set-AzVirtualNetworkGatewayDefaultSite** per assegnare il sito predefinito a ContosoVirtualGateway.

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

### -GatewayDefaultSite
Specifica un riferimento a un oggetto al gateway di rete locale da assegnare come sito predefinito per la rete virtuale specificata.
Puoi usare il cmdlet Get-AzLocalNetworkGateway per creare un riferimento a un oggetto in un gateway locale.

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
Specifica un riferimento a un oggetto al gateway di rete virtuale in cui verrà assegnato il sito predefinito.
Puoi creare un riferimento a un oggetto a un gateway di rete virtuale usando il **Get-AzVirtualNetworkGateway** e specificando il nome del gateway.
La variabile $VirtualGateway può quindi essere usata come valore di parametro per il parametro *VirtualNetworkGateway* :

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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway

### Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway

## OUTPUT

### Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway

## Note

## COLLEGAMENTI CORRELATI

[Get-AzLocalNetworkGateway](./Get-AzLocalNetworkGateway.md)

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[Remove-AzVirtualNetworkGatewayDefaultSite](./Remove-AzVirtualNetworkGatewayDefaultSite.md)


