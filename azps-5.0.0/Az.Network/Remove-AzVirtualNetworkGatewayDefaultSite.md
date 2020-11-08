---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 288812137887e4fc22308bba56a3fbdbeeb28c85
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201763"
---
# Remove-AzVirtualNetworkGatewayDefaultSite

## Sinossi
Rimuove il sito predefinito da un gateway di rete virtuale.

## SINTASSI

```
Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Remove-AzVirtualNetworkGatewayDefaultSite** rimuove il sito predefinito per il tunneling forzato da un gateway di rete virtuale.
Il tunneling forzato consente di reindirizzare il traffico associato a Internet da macchine virtuali di Azure alla rete locale; in questo modo è possibile ispezionare e controllare il traffico prima di rilasciarlo.
Il tunneling forzato viene eseguito usando un tunnel VPN (Virtual Private Network); Questo tunnel richiede un sito predefinito, un gateway locale in cui viene reindirizzato tutto il traffico associato a Internet di Azure.
**Remove-AzVirtualNetworkGatewayDefaultSite** rimuove il sito predefinito assegnato a un gateway.
Se si esegue questa operazione, sarà necessario usare Set-AzVirtualNetworkGatewayDefaultSite per assegnare un nuovo sito predefinito prima che il gateway possa essere usato per il tunneling forzato.

## ESEMPI

### Esempio 1: rimuovere il sito predefinito assegnato a un gateway di rete virtuale
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway $Gateway
```

In questo esempio viene rimosso il sito predefinito attualmente assegnato a un gateway di rete virtuale denominato ContosoVirtualGateway.
Il primo comando USA **Get-AzVirtualNetworkGateway** per creare un riferimento a un oggetto al gateway; Questo riferimento oggetto è archiviato in una variabile denominata $Gateway.
Il secondo comando usa quindi **Remove-AzVirtualNetworkGatewayDefaultSite** per rimuovere il sito predefinito assegnato a tale gateway.

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

### -VirtualNetworkGateway
Specifica un riferimento a un oggetto al gateway di rete virtuale che contiene il sito predefinito da rimuovere.
Puoi creare un riferimento a un oggetto a un gateway di rete virtuale usando la Get-AzVirtualNetworkGateway e specificando il nome del gateway.

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

## OUTPUT

### Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway

## Note

## COLLEGAMENTI CORRELATI

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[Set-AzVirtualNetworkGatewayDefaultSite](./Set-AzVirtualNetworkGatewayDefaultSite.md)


