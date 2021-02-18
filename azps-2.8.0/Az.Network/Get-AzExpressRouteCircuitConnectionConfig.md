---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59692f1f-9f1e-4a3c-8200-312c3806a9b7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 0adba1dfe453852b0797f40d6cd4d188db87169f
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100409954"
---
# Get-AzExpressRouteCircuitConnectionConfig

## SYNOPSIS
Ottiene una configurazione della connessione del circuito ExpressRoute associata al peering privato di ExpressRouteCircuit.

## SINTASSI

```
Get-AzExpressRouteCircuitConnectionConfig [[-Name] <String>] [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Get-AzExpressRouteCircuitConnectionConfig** recupera la configurazione di una connessione a un circuito associato al peering privato per un circuito ExpressRoute.

## ESEMPI

### Esempio 1: Visualizzare la configurazione della connessione del circuito per un circuito ExpressRoute
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
```

### Esempio 2: Ottenere la risorsa della connessione del circuito associata a un circuito ExpressRoute usando le piping
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName
```

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

### -ExpressRouteCircuit
Oggetto circuito ExpressRoute contenente la configurazione della connessione del circuito.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Nome della configurazione di connessione al circuito da recuperare.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](https://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit

## OUTPUT

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitConnection

## NOTE

## COLLEGAMENTI CORRELATI

[Get-AzExpressRouteCircuit](Get-AzExpressRouteCircuit.md)

[Add-AzExpressRouteCircuitConnectionConfig](Add-AzExpressRouteCircuitConnectionConfig.md)

[Remove-AzExpressRouteCircuitConnectionConfig](Remove-AzExpressRouteCircuitConnectionConfig.md)




