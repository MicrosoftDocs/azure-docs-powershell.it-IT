---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: d97c6825a6681127e2275a7d3d171e6500daba5d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678680"
---
# Add-AzExpressRouteCircuitAuthorization

## Sinossi
Aggiunge un'autorizzazione del circuito ExpressRoute.

## SINTASSI

```
Add-AzExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Add-AzExpressRouteCircuitAuthorization** aggiunge un'autorizzazione a un circuito di ExpressRoute. Circuiti ExpressRoute connettere la rete locale al cloud Microsoft usando un provider di connettività anziché Internet pubblico. Il proprietario di un circuito ExpressRoute può creare fino a 10 autorizzazioni per ogni circuito; Queste autorizzazioni generano una chiave di autorizzazione che può essere usata da un proprietario di rete virtuale per connettere la propria rete al circuito (un'autorizzazione per rete virtuale). **Add-AzExpressRouteCircuitAuthorization** aggiunge una nuova autorizzazione a un circuito e genera contemporaneamente la chiave di autorizzazione corrispondente. Queste chiavi possono essere visualizzate in qualsiasi momento eseguendo il cmdlet Get-AzExpressRouteCircuitAuthorization e, se necessario, possono quindi essere copiate e inoltrate al proprietario di rete appropriato.
Tieni presente che, dopo aver eseguito **Add-AzExpressRouteCircuitAuthorization** , devi chiamare il cmdlet Set-AzExpressRouteCircuit per attivare la chiave. Se non si chiama **set-AzExpressRouteCircuit,** l'autorizzazione verrà aggiunta al circuito, ma non verrà abilitata per l'uso.

## ESEMPI

### Esempio 1: aggiungere un'autorizzazione al circuito ExpressRoute specificato
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

I comandi in questo esempio aggiungono una nuova autorizzazione a un circuito di ExpressRoute esistente. Il primo comando USA **Get-AzExpressRouteCircuit** per creare un riferimento a un oggetto Circuit denominato ContosoCircuit. Il riferimento a un oggetto viene archiviato in una variabile denominata $Circuit.
Nel secondo comando viene usato il cmdlet **Add-AzExpressRouteCircuitAuthorization** per aggiungere una nuova autorizzazione (ContosoCircuitAuthorization) al circuito di ExpressRoute. Questo comando aggiunge l'autorizzazione ma non attiva tale autorizzazione. L'attivazione di un'autorizzazione richiede l'opzione **set-AzExpressRouteCircuit** visualizzata nel comando finale dell'esempio.

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

### -ExpressRouteCircuit
Specifica il circuito di ExpressRoute a cui questo cmdlet aggiunge l'autorizzazione.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nome
Specifica il nome dell'autorizzazione Circuit da aggiungere.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit

## OUTPUT

### Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit

## Note

## COLLEGAMENTI CORRELATI

[Get-AzExpressRouteCircuit](./Get-AzExpressRouteCircuit.md)

[Get-AzExpressRouteCircuitAuthorization](./Get-AzExpressRouteCircuitAuthorization.md)

[New-AzExpressRouteCircuitAuthorization](./New-AzExpressRouteCircuitAuthorization.md)

[Remove-AzExpressRouteCircuitAuthorization](./Remove-AzExpressRouteCircuitAuthorization.md)

[Set-AzExpressRouteCircuit](./Set-AzExpressRouteCircuit.md)
