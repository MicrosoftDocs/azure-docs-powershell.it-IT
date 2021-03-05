---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayavailableservervariableandheader
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
ms.openlocfilehash: f4f2e76a9354ee6ed796b64cbdd83f21d70ff954
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978382"
---
# Get-AzApplicationGatewayAvailableServerVariableAndHeader

## SYNOPSIS
Ottenere le variabili del server supportate e le intestazioni di richiesta e risposta disponibili.

## SINTASSI

```
Get-AzApplicationGatewayAvailableServerVariableAndHeader [-DefaultProfile <IAzureContextContainer>]
 [-ServerVariable] [-RequestHeader] [-ResponseHeader] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Get-AzApplicationGatewayAvailableServerVariableAndHeader** ottiene le variabili del server supportate e le intestazioni di richiesta e risposta disponibili. I parametri possono essere usati per ottenere le variabili o gli elenchi di intestazioni.

## ESEMPI

### Esempio 1
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ServerVariable
```

Questo comando restituisce tutte le variabili del server disponibili.

### Esempio 2
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -RequestHeader
```

Questo comando restituisce tutte le intestazioni di richiesta disponibili.

### Esempio 3
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ResponseHeader
```

Questo comando restituisce tutte le intestazioni di risposta disponibili.

### Esempio 4
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader - ServerVariable -RequestHeader -ResponseHeader
```

Questo comando restituisce tutte le variabili del server disponibili, le intestazioni di richiesta e risposta.

### Esempio 5
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader
```

Questo comando restituisce tutte le variabili del server disponibili, le intestazioni di richiesta e risposta.

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

### -RequestHeader
Intestazioni di richiesta disponibili di Gateway applicazione.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResponseHeader
Intestazioni di risposta disponibili di Gateway applicazione.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerVariable
Variabili server disponibili di Gateway applicazione.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Nessuno

## OUTPUT

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult

## NOTE
**List-AzApplicationGatewayAvailableServerVariableAndHeader** è un alias per il cmdlet **Get-AzApplicationGatewayAvailableServerVariableAndHeader.**

## COLLEGAMENTI CORRELATI
