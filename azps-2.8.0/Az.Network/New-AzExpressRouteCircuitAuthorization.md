---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: c6db110c1657eb79deae3adcdfada8a835becdb6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93853002"
---
# New-AzExpressRouteCircuitAuthorization

## Sinossi
Crea un'autorizzazione per il circuito ExpressRoute.

## SINTASSI

```
New-AzExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzExpressRouteCircuitAuthorization** crea un'autorizzazione Circuit che può essere aggiunta a un circuito di ExpressRoute. Circuiti ExpressRoute connettere la rete locale al cloud Microsoft usando un provider di connettività anziché Internet pubblico. Il proprietario di un circuito ExpressRoute può creare fino a 10 autorizzazioni per ogni circuito; Queste autorizzazioni generano una chiave di autorizzazione che può essere usata da un proprietario di rete virtuale per connettere una rete al circuito. Può essere disponibile una sola autorizzazione per ogni rete virtuale.
Dopo aver creato un circuito ExpressRoute, è possibile usare **Add-AzExpressRouteCircuitAuthorization** per aggiungere un'autorizzazione al circuito.
In alternativa, puoi usare **New-AzExpressRouteCircuitAuthorization** per creare un'autorizzazione che può essere aggiunta a un nuovo circuito contemporaneamente alla creazione del circuito.

## ESEMPI

### Esempio 1: creare una nuova autorizzazione Circuit
```
$Authorization = New-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

Questo comando crea una nuova autorizzazione Circuit denominata ContosoCircuitAuthorization e quindi archivia tale oggetto in una variabile denominata $Authorization. Il salvataggio dell'oggetto in una variabile è importante: anche se **New-AzExpressRouteCircuitAuthorization** può creare un'autorizzazione Circuit, non può aggiungere l'autorizzazione a una route Circuit. La variabile $Authorization viene invece usata New-AzExpressRouteCircuit quando si crea un nuovo circuito di ExpressRoute.
Per altre informazioni, vedere la documentazione relativa al cmdlet New-AzExpressRouteCircuit.

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

### -Nome
Specifica un nome univoco per la nuova autorizzazione del circuito ExpressRoute.

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

### Nessuno

## OUTPUT

### Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitAuthorization

## Note

## COLLEGAMENTI CORRELATI

[Add-AzExpressRouteCircuitAuthorization](./Add-AzExpressRouteCircuitAuthorization.md)

[Get-AzExpressRouteCircuitAuthorization](./Get-AzExpressRouteCircuitAuthorization.md)

[Remove-AzExpressRouteCircuitAuthorization](./Remove-AzExpressRouteCircuitAuthorization.md)

