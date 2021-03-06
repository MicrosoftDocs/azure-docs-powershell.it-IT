---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/powershell/module/az.network/new-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 9c247784a9f890d97aee301383656f97ef9c7dd4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995356"
---
# New-AzExpressRouteCircuitAuthorization

## SYNOPSIS
Crea un'autorizzazione del circuito ExpressRoute.

## SINTASSI

```
New-AzExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **New-AzExpressRouteCircuitAuthorization** crea un'autorizzazione del circuito che può essere aggiunta a un circuito ExpressRoute. I circuiti ExpressRoute connettono la rete locale al cloud Microsoft usando un provider di connettività anziché Internet pubblico. Il proprietario di un circuito ExpressRoute può creare fino a 10 autorizzazioni per ogni circuito; Queste autorizzazioni generano una chiave di autorizzazione che può essere usata dal proprietario di una rete virtuale per connettere una rete al circuito. Per ogni rete virtuale può essere disponibile una sola autorizzazione.
Dopo aver creato un circuito ExpressRoute, è possibile **usare Add-AzExpressRouteCircuitAuthorization** per aggiungere un'autorizzazione a tale circuito.
In alternativa, è possibile usare **New-AzExpressRouteCircuitAuthorization** per creare un'autorizzazione che può essere aggiunta a un nuovo circuito nello stesso momento in cui viene creato il circuito.

## ESEMPI

### Esempio 1: Creare una nuova autorizzazione del circuito
```
$Authorization = New-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

Questo comando crea una nuova autorizzazione di circuito denominata ContosoCircuitAuthorization e quindi archivia l'oggetto in una variabile denominata $Authorization. Salvare l'oggetto in una variabile è importante: anche se **New-AzExpressRouteCircuitAuthorization** può creare un'autorizzazione di circuito, non può aggiungerla a un percorso di circuito. La variabile $Authorization viene usata New-AzExpressRouteCircuit durante la creazione di un nuovo circuito ExpressRoute.
Per altre informazioni, vedere la documentazione per il cmdlet New-AzExpressRouteCircuit.

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
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### Nessuno

## OUTPUT

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization

## NOTE

## COLLEGAMENTI CORRELATI

[Add-AzExpressRouteCircuitAuthorization](./Add-AzExpressRouteCircuitAuthorization.md)

[Get-AzExpressRouteCircuitAuthorization](./Get-AzExpressRouteCircuitAuthorization.md)

[Remove-AzExpressRouteCircuitAuthorization](./Remove-AzExpressRouteCircuitAuthorization.md)

