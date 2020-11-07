---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuitauthorization
schema: 2.0.0
ms.openlocfilehash: 144d70318463b7c5ffebfa6b7d942ec2a351fc24
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866050"
---
# Remove-AzureRmExpressRouteCircuitAuthorization

## Sinossi
Rimuove un'autorizzazione di configurazione di ExpressRoute esistente.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Remove-AzureRmExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Remove-AzureRmExpressRouteCircuitAuthorization** rimuove un'autorizzazione assegnata a un circuito di ExpressRoute. Circuiti ExpressRoute connettere la rete locale a Azure usando un provider di connettività anziché Internet pubblico. Il proprietario di un circuito ExpressRoute può creare fino a 10 autorizzazioni per ogni circuito; Queste autorizzazioni generano una chiave di autorizzazione che può essere usata da un proprietario di rete virtuale per connettere la propria rete al circuito. Può essere disponibile una sola autorizzazione per ogni rete virtuale. In qualsiasi momento, tuttavia, il proprietario del circuito può usare **Remove-AzureRmExpressRouteCircuitAuthorization** per rimuovere l'autorizzazione assegnata a una rete virtuale. Quando ciò accade, la rete virtuale corrispondente non è più in grado di usare il circuito ExpressRoute per connettersi ad Azure.

## ESEMPI

### Esempio 1: rimuovere l'autorizzazione di un circuito da un circuito di ExpressRoute
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

In questo esempio viene rimossa un'autorizzazione Circuit da un circuito ExpressRoute. Il primo comando usa il cmdlet **Get-AzureRmExpressRouteCircuit** per creare un riferimento a un oggetto in un circuito ExpressRoute denominato ContosoCircuit e archivia il risultato nella variabile denominata $Circuit.

Il secondo comando contrassegna l'autorizzazione Circuit ContosoCircuitAuthorization per la rimozione.

Il terzo comando usa il cmdlet Set-AzureRmExpressRouteCircuit per confermare la rimozione del circuito ExpressRoute archiviato nella variabile $Circuit.

## PARAMETRI

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpressRouteCircuit
Specifica l'oggetto ExpressRouteCircuit rimosso da questo cmdlet.

```yaml
Type: PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nome
Specifica il nome dell'autorizzazione Circuit che viene rimossa da questo cmdlet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### PSExpressRouteCircuit
Questo cmdlet accetta le istanze pipeline dell'oggetto **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit** .

## OUTPUT

### PSExpressRouteCircuit
Questo cmdlet modifica le istanze esistenti dell'oggetto **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit** .

## Note

## COLLEGAMENTI CORRELATI

[Add-AzureRmExpressRouteCircuitAuthorization](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[Get-AzureRmExpressRouteCircuit](./Get-AzureRmExpressRouteCircuit.md)

[Get-AzureRmExpressRouteCircuitAuthorization](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[New-AzureRmExpressRouteCircuitAuthorization](./New-AzureRmExpressRouteCircuitAuthorization.md)

[Set-AzureRmExpressRouteCircuit](./Set-AzureRmExpressRouteCircuit.md)
