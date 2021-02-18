---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
ms.openlocfilehash: 4017d9eba94f82b235b5016145ee0692ff56892c
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100410770"
---
# Get-AzExpressRouteServiceProvider

## SYNOPSIS
Ottiene un elenco di provider di servizi ExpressRoute e i relativi attributi.

## SINTASSI

```
Get-AzExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Get-AzExpressRouteServiceProvider** recupera un elenco di provider di servizi ExpressRoute e i relativi attributi. L'attributo include opzioni per la posizione e la larghezza di banda.

## ESEMPI

### Esempio 1: Ottenere un elenco di provider di servizi con posizioni nella "Silicon Valley"
```
Get-AzExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
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

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](https://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Nessuno

## OUTPUT

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider

## NOTE

## COLLEGAMENTI CORRELATI

[Get-AzExpressRouteCircuitARPTable](Get-AzExpressRouteCircuitARPTable.md)

[Get-AzExpressRouteCircuitRouteTable](Get-AzExpressRouteCircuitRouteTable.md)

[Get-AzExpressRouteCircuitRouteTableSummary](Get-AzExpressRouteCircuitRouteTableSummary.md)

[Get-AzExpressRouteCircuitStat](Get-AzExpressRouteCircuitStat.md)
