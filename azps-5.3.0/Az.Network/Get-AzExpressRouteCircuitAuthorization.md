---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 7c942968439d7d55fe78a3dd95c36501a2eaf10f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473989"
---
# Get-AzExpressRouteCircuitAuthorization

## Sinossi
Ottiene informazioni sulle autorizzazioni del circuito ExpressRoute.

## SINTASSI

```
Get-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzExpressRouteCircuitAuthorization** ottiene informazioni sulle autorizzazioni assegnate a un circuito di ExpressRoute. Circuiti ExpressRoute connettere la rete locale al cloud Microsoft usando un provider di connettività anziché Internet pubblico. Il proprietario di un circuito ExpressRoute può creare fino a 10 autorizzazioni per ogni circuito; Queste autorizzazioni generano una chiave di autorizzazione che può essere usata da un proprietario di rete virtuale per connettere la propria rete al circuito (un'autorizzazione per rete virtuale). Le chiavi di autorizzazione, oltre ad altre informazioni sull'autorizzazione, possono essere visualizzate in qualsiasi momento eseguendo **Get-AzExpressRouteCircuitAuthorization**.

## ESEMPI

### Esempio 1: ottenere tutte le autorizzazioni di ExpressRoute
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit
```

Questi comandi restituiscono informazioni su tutte le autorizzazioni di ExpressRoute associate a un circuito di ExpressRoute. Il primo comando usa il cmdlet **Get-AzExpressRouteCircuit** per creare un riferimento a un oggetto Circuit denominato ContosoCircuit; il riferimento all'oggetto è archiviato nella variabile $Circuit. Il secondo comando usa quindi il riferimento oggetto e il cmdlet **Get-AzExpressRouteCircuitAuthorization** per restituire informazioni sulle autorizzazioni associate a ContosoCircuit.

### Esempio 2: ottenere tutte le autorizzazioni di ExpressRoute usando il cmdlet Where-Object
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

Questi comandi rappresentano una variante dei comandi usati nell'esempio 1. In questo caso, tuttavia, le informazioni vengono restituite solo per le autorizzazioni disponibili per l'uso, ovvero per le autorizzazioni che non sono state assegnate a una rete virtuale. A questo scopo, le informazioni sull'autorizzazione Circuit vengono restituite nel comando 2 e vengono inviate tramite pipe al cmdlet **Where-Object** .
**Where-Object** seleziona solo le autorizzazioni in cui la proprietà *AuthorizationUseStatus* è impostata su available. Per elencare solo le autorizzazioni non disponibili, usare questa sintassi per la clausola WHERE: `{$_.AuthorizationUseStatus -ne "Available"}`

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
Specifica l'autorizzazione del circuito ExpressRoute.

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
Specifica il nome dell'autorizzazione del circuito ExpressRoute che viene ottenuto da questo cmdlet.
-Nome "ContosoCircuitAuthorization"

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

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit

## OUTPUT

### Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitAuthorization

## Note

## COLLEGAMENTI CORRELATI

[Add-AzExpressRouteCircuitAuthorization](./Add-AzExpressRouteCircuitAuthorization.md)

[Get-AzExpressRouteCircuit](./Get-AzExpressRouteCircuit.md)

[New-AzExpressRouteCircuitAuthorization](./New-AzExpressRouteCircuitAuthorization.md)

[Remove-AzExpressRouteCircuitAuthorization](./Remove-AzExpressRouteCircuitAuthorization.md)
