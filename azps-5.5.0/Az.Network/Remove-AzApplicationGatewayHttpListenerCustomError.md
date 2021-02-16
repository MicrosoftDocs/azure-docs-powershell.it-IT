---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 82675befb6a900bacdead036f323959e1e7a72a9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189623"
---
# Remove-AzApplicationGatewayHttpListenerCustomError

## SYNOPSIS
Rimuove un errore personalizzato da un listener http di un gateway applicazioni.

## SINTASSI

```
Remove-AzApplicationGatewayHttpListenerCustomError -StatusCode <String>
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Remove-AzApplicationGatewayCustomError** rimuove un errore personalizzato da un listener http di un gateway di applicazione.

## ESEMPI

### Esempio 1: Rimuove un errore personalizzato da un listener http
```powershell
PS C:\> $updatedlistener = Remove-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

Questo comando rimuove l'errore personalizzato del codice di stato http 502 dal listener http $listener 01 e restituisce il listener aggiornato.

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

### -Http Listener
Listener Http del Gateway applicazione

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -StatusCode
Codice di stato dell'errore del cliente del gateway applicazione.

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

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpHttp Più

## OUTPUT

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError

## NOTE

## COLLEGAMENTI CORRELATI

[Add-AzApplicationGatewayHttpCustomError](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[Get-AzApplicationGatewayHttpCustomError](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[Set-AzApplicationGatewayHttpCustomError](./Set-AzApplicationGatewayHttpListenerCustomError.md)
