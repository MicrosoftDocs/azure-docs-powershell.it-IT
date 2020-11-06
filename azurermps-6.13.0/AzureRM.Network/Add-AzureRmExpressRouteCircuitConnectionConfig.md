---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7b4a8c9f-874c-4a27-b87e-c8ad7e73188d
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: aab4e78cd01e814ed8eb81b820e20bd3da4c03f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520948"
---
# Add-AzureRmExpressRouteCircuitConnectionConfig

## Sinossi
Aggiunge una configurazione di connessione Circuit a un peering privato di un circuito di route espresso. 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### SetByResource (impostazione predefinita)
```
Add-AzureRmExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SetByResourceId
```
Add-AzureRmExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Add-AzureRmExpressRouteCircuitConnectionConfig** aggiunge una configurazione di connessione Circuit a peering privato per un circuito di ExpressRoute. In questo modo, è possibile peering due circuiti di Route Express tra aree o abbonamenti. Tieni presente che, dopo aver eseguito **Add-AzureRmExpressRouteCircuitPeeringConfig** , devi chiamare il cmdlet Set-AzureRmExpressRouteCircuit per attivare la configurazione.

## ESEMPI

### Esempio 1: aggiungere una risorsa di connessione Circuit a un circuito ExpressRoute esistente
```
$circuit_init = Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzureRmExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Add-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### Esempio 2: aggiungere una configurazione di connessione circuitale tramite piping a un circuito ExpressRoute esistente
```
$circuit_peer = Get-AzureRmExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Add-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzureRmExpressRouteCircuit
```

## PARAMETRI

### -AddressPrefix
Uno spazio di indirizzi minimo/29 per creare tunnel VxLan tra i circuiti di Route Express

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AuthorizationKey
Chiave di autorizzazione per il circuito di routing espresso peer in un altro abbonamento. L'autorizzazione sul circuito peer può essere creata usando i comandi esistenti.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -ExpressRouteCircuit
Il circuito ExpressRoute da modificare. Questo è un oggetto Azure restituito dal cmdlet **Get-AzureRmExpressRouteCircuit** .

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

### -Nome
Nome della risorsa di connessione Circuit da aggiungere.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PeerExpressRouteCircuitPeering
ID risorsa per peering privato del circuito remoto che verrà peered con il circuito corrente.

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confermare
Richiede la conferma prima di eseguire il cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa succede se il cmdlet viene eseguito. Il cmdlet non viene eseguito.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit
Parametri: ExpressRouteCircuit (ByValue)

### System. String

## OUTPUT

### Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureRmExpressRouteCircuit](Get-AzureRmExpressRouteCircuit.md)

[Get-AzureRmExpressRouteCircuitConnectionConfig](Get-AzureRmExpressRouteCircuitConnectionConfig.md)

[Remove-AzureRmExpressRouteCircuitConnectionConfig](Remove-AzureRmExpressRouteCircuitConnectionConfig.md)

[Set-AzureRmExpressRouteCircuitConnectionConfig](Set-AzureRmExpressRouteCircuitConnectionConfig.md)

[New-AzureRmExpressRouteCircuitConnectionConfig](New-AzureRmExpressRouteCircuitConnectionConfig.md)

[Set-AzureRmExpressRouteCircuit](Set-AzureRmExpressRouteCircuit.md)

[Get-AzureRmExpressRouteCircuit](Get-AzureRmExpressRouteCircuit.md)
