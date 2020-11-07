---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 2fec428adb2ba8621d09a1f0ae5e762cdbe4b913
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687505"
---
# New-AzureRmExpressRouteCircuitAuthorization

## Sinossi
Crea un'autorizzazione per il circuito ExpressRoute.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
New-AzureRmExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzureRmExpressRouteCircuitAuthorization** crea un'autorizzazione Circuit che può essere aggiunta a un circuito di ExpressRoute. Circuiti ExpressRoute connettere la rete locale al cloud Microsoft usando un provider di connettività anziché Internet pubblico. Il proprietario di un circuito ExpressRoute può creare fino a 10 autorizzazioni per ogni circuito; Queste autorizzazioni generano una chiave di autorizzazione che può essere usata da un proprietario di rete virtuale per connettere una rete al circuito. Può essere disponibile una sola autorizzazione per ogni rete virtuale.

Dopo aver creato un circuito ExpressRoute, è possibile usare **Add-AzureRmExpressRouteCircuitAuthorization** per aggiungere un'autorizzazione al circuito.
In alternativa, puoi usare **New-AzureRmExpressRouteCircuitAuthorization** per creare un'autorizzazione che può essere aggiunta a un nuovo circuito contemporaneamente alla creazione del circuito.

## ESEMPI

### Esempio 1: creare una nuova autorizzazione Circuit
```
$Authorization = New-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

Questo comando crea una nuova autorizzazione Circuit denominata ContosoCircuitAuthorization e quindi archivia tale oggetto in una variabile denominata $Authorization. Il salvataggio dell'oggetto in una variabile è importante: anche se **New-AzureRmExpressRouteCircuitAuthorization** può creare un'autorizzazione Circuit, non può aggiungere l'autorizzazione a una route Circuit. La variabile $Authorization viene invece usata New-AzureRmExpressRouteCircuit quando si crea un nuovo circuito di ExpressRoute.

Per altre informazioni, vedere la documentazione relativa al cmdlet New-AzureRmExpressRouteCircuit.

## PARAMETRI

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

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno
Questo cmdlet non accetta l'input da pipeline.

## OUTPUT

### PSExpressRouteCircuitAuthorization
Questo cmdlet crea istanze dell'oggetto **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitAuthorization** .

## Note

## COLLEGAMENTI CORRELATI

[Add-AzureRmExpressRouteCircuitAuthorization](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[Get-AzureRmExpressRouteCircuitAuthorization](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[Remove-AzureRmExpressRouteCircuitAuthorization](./Remove-AzureRmExpressRouteCircuitAuthorization.md)

