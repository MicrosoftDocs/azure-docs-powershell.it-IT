---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 288812137887e4fc22308bba56a3fbdbeeb28c85
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179471"
---
# Remove-AzVirtualNetworkGatewayDefaultSite

## SYNOPSIS
Rimuove il sito predefinito da un gateway di rete virtuale.

## SINTASSI

```
Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Remove-AzVirtualNetworkGatewayDefaultSite** rimuove il sito predefinito di tunneling forzato da un gateway di rete virtuale.
Il tunneling forzato consente di reindirizzare il traffico associato a Internet dalle macchine virtuali di Azure alla rete locale; in questo modo è possibile controllare e controllare il traffico prima di rilasciarlo.
Il tunneling forzato viene eseguito usando un tunnel VPN; questo tunnel richiede un sito predefinito, un gateway locale in cui viene reindirizzato tutto il traffico associato a Internet di Azure.
**Remove-AzVirtualNetworkGatewayDefaultSite** rimuove il sito predefinito assegnato a un gateway.
In questo caso, sarà necessario usare Set-AzVirtualNetworkGatewayDefaultSite assegnare un nuovo sito predefinito prima di poter usare il gateway per l'uso dei tunnel forzati.

## ESEMPI

### Esempio 1: Rimuovere il sito predefinito assegnato a un gateway di rete virtuale
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway $Gateway
```

Questo esempio rimuove il sito predefinito attualmente assegnato a un gateway di rete virtuale denominato ContosoVirtualGateway.
Il primo comando usa **Get-AzVirtualNetworkGateway** per creare un riferimento a un oggetto al gateway; questo riferimento all'oggetto è archiviato in una variabile denominata $Gateway.
Il secondo comando usa **quindi Remove-AzVirtualNetworkGatewayDefaultSite** per rimuovere il sito predefinito assegnato al gateway.

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

### -VirtualNetworkGateway
Specifica un riferimento a un oggetto al gateway di rete virtuale contenente il sito predefinito da rimuovere.
È possibile creare un riferimento a un oggetto a un gateway di rete virtuale usando il Get-AzVirtualNetworkGateway e specificando il nome del gateway.

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

## OUTPUT

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway

## NOTE

## COLLEGAMENTI CORRELATI

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[Set-AzVirtualNetworkGatewayDefaultSite](./Set-AzVirtualNetworkGatewayDefaultSite.md)


