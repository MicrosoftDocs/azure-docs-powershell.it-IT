---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CC033DA8-FACC-44E2-82F9-E30FADBF8926
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: ac18c96353e247c721f95acf83e174e18a578b2c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990987"
---
# Remove-AzApplicationGatewayRequestRoutingRule

## SYNOPSIS
Rimuove una regola di routing delle richieste da un gateway applicazioni.

## SINTASSI

```
Remove-AzApplicationGatewayRequestRoutingRule -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Remove-AzApplicationGatewayRequestRoutingRule** rimuove una regola di routing delle richieste da un gateway applicazione di Azure.

## ESEMPI

### Esempio 1: Rimuovere una regola di routing delle richieste da un gateway applicazioni
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule02"
```

Il primo comando ottiene un gateway applicazione e lo archivia nella $AppGw variabile.
Il secondo comando rimuove la regola di routing delle richieste denominata Rule02 dal gateway applicazione archiviato in $AppGw.

## PARAMETERS

### -ApplicationGateway
Specifica il gateway applicazione da cui rimuovere una regola di routing delle richieste.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

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
Specifica il nome della regola di routing delle richieste da cui questo cmdlet rimuove.

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

### Microsoft.Azure.Commands.Network.Models.PSApplicationGateway

## OUTPUT

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule

## NOTE

## COLLEGAMENTI CORRELATI

[Add-AzApplicationGatewayRequestRoutingRule](./Add-AzApplicationGatewayRequestRoutingRule.md)

[Get-AzApplicationGatewayRequestRoutingRule](./Get-AzApplicationGatewayRequestRoutingRule.md)

[New-AzApplicationGatewayRequestRoutingRule](./New-AzApplicationGatewayRequestRoutingRule.md)

[Set-AzApplicationGatewayRequestRoutingRule](./Set-AzApplicationGatewayRequestRoutingRule.md)


