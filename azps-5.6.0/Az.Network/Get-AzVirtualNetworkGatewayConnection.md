---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: e4b972944f757c9b0072f091dc820de5fa5d5b1c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964254"
---
# Get-AzVirtualNetworkGatewayConnection

## SYNOPSIS
Ottiene una connessione gateway di rete virtuale

## SINTASSI

```
Get-AzVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
La connessione a Gateway di rete virtuale è l'oggetto che rappresenta il tunnel IPsec (Site-to-Site o Vnet-to-Vnet) connesso al Gateway di rete virtuale in Azure.
Il cmdlet **Get-AzVirtualNetworkGatewayConnection** restituisce l'oggetto della connessione in base al nome e al nome del gruppo di risorse.
Se il cmdlet **Get-AzVirtualNetworkGatewayConnection** viene generato senza specificare il parametro -Name, l'output non mostrerà i dettagli di ConnectionStatus e SharedKey.

## ESEMPI

### 1: Ottenere una connessione a un Gateway di rete virtuale
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

Restituisce l'oggetto della connessione a Gateway di rete virtuale con il nome "myTunnel" all'interno del gruppo di risorse "myRG"

### 2: ottenere tutte le connessioni del Gateway di rete virtuale usando i filtri
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel* -ResourceGroupName myRG
```

Restituisce tutte le connessioni del Gateway di rete virtuale che iniziano con "myTunnel" all'interno del gruppo di risorse "myRG"

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

### -Name
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### -ResourceGroupName
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### System.String

## OUTPUT

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection

## NOTE

## COLLEGAMENTI CORRELATI

[New-AzVirtualNetworkGatewayConnection](./New-AzVirtualNetworkGatewayConnection.md)

[Remove-AzVirtualNetworkGatewayConnection](./Remove-AzVirtualNetworkGatewayConnection.md)

[Set-AzVirtualNetworkGatewayConnection](./Set-AzVirtualNetworkGatewayConnection.md)
