---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitauthorization
schema: 2.0.0
ms.openlocfilehash: ec11ab37bc3fcb787de2b97f46941f23ede1b45a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866089"
---
# Get-AzureRmExpressRouteCircuitAuthorization

## Sinossi
Ottiene informazioni sulle autorizzazioni del circuito ExpressRoute.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Get-AzureRmExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureRmExpressRouteCircuitAuthorization** ottiene informazioni sulle autorizzazioni assegnate a un circuito di ExpressRoute. Circuiti ExpressRoute connettere la rete locale al cloud Microsoft usando un provider di connettività anziché Internet pubblico. Il proprietario di un circuito ExpressRoute può creare fino a 10 autorizzazioni per ogni circuito; Queste autorizzazioni generano una chiave di autorizzazione che può essere usata da un proprietario di rete virtuale per connettere la propria rete al circuito (un'autorizzazione per rete virtuale). Le chiavi di autorizzazione, oltre ad altre informazioni sull'autorizzazione, possono essere visualizzate in qualsiasi momento eseguendo **Get-AzureRmExpressRouteCircuitAuthorization**.

## ESEMPI

### Esempio 1: ottenere tutte le autorizzazioni di ExpressRoute
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzureRmExpressRouteCircuitAuthorization -Circuit $Circuit
```

Questi comandi restituiscono informazioni su tutte le autorizzazioni di ExpressRoute associate a un circuito di ExpressRoute. Il primo comando usa il cmdlet **Get-AzureRmExpressRouteCircuit** per creare un riferimento a un oggetto Circuit denominato ContosoCircuit; il riferimento all'oggetto è archiviato nella variabile $Circuit. Il secondo comando usa quindi il riferimento oggetto e il cmdlet **Get-AzureRmExpressRouteCircuitAuthorization** per restituire informazioni sulle autorizzazioni associate a ContosoCircuit.

### Esempio 2: ottenere tutte le autorizzazioni di ExpressRoute usando il cmdlet Where-Object
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzureRmExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

Questi comandi rappresentano una variante dei comandi usati nell'esempio 1. In questo caso, tuttavia, le informazioni vengono restituite solo per le autorizzazioni disponibili per l'uso, ovvero per le autorizzazioni che non sono state assegnate a una rete virtuale. A questo scopo, le informazioni sull'autorizzazione Circuit vengono restituite nel comando 2 e vengono inviate tramite pipe al cmdlet **Where-Object** .
**Where-Object** seleziona solo le autorizzazioni in cui la proprietà *AuthorizationUseStatus* è impostata su available. Per elencare solo le autorizzazioni non disponibili, usare questa sintassi per la clausola WHERE:

`{$_.AuthorizationUseStatus -ne "Available"}`

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
Specifica l'autorizzazione del circuito ExpressRoute.

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
Specifica il nome dell'autorizzazione del circuito ExpressRoute che viene ottenuto da questo cmdlet.

-Nome "ContosoCircuitAuthorization"

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
**Get-AzureRmExpressRouteCircuitAuthorization** accetta le istanze pipeline dell'oggetto **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit** .

## OUTPUT

### PSExpressRouteCircuitAuthorization
**Get-AzureRmExpressRouteCircuitAuthorization** restituisce le istanze dell'oggetto **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitAuthorization** .

## Note

## COLLEGAMENTI CORRELATI

[Add-AzureRmExpressRouteCircuitAuthorization](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[Get-AzureRmExpressRouteCircuit](./Get-AzureRmExpressRouteCircuit.md)

[New-AzureRmExpressRouteCircuitAuthorization](./New-AzureRmExpressRouteCircuitAuthorization.md)

[Remove-AzureRmExpressRouteCircuitAuthorization](./Remove-AzureRmExpressRouteCircuitAuthorization.md)
