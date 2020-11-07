---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailableservervariableandheader
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
ms.openlocfilehash: 8f0fc8caba03251ede507fc383ef99c10a06eeb3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678627"
---
# Get-AzApplicationGatewayAvailableServerVariableAndHeader

## Sinossi
Ottenere le variabili server supportate e le intestazioni di richiesta e risposta disponibili.

## SINTASSI

```
Get-AzApplicationGatewayAvailableServerVariableAndHeader [-DefaultProfile <IAzureContextContainer>]
 [-ServerVariable] [-RequestHeader] [-ResponseHeader] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzApplicationGatewayAvailableServerVariableAndHeader** ottiene le variabili server supportate e le intestazioni di richiesta e risposta disponibili. I parametri possono essere usati per ottenere le variabili o gli elenchi di intestazioni.

## ESEMPI

### Esempio 1
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ServerVariable
```

Questi comandi restituiscono tutte le variabili del server disponibili.

### Esempio 2
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -RequestHeader
```

Questi comandi restituiscono tutte le intestazioni di richiesta disponibili.

### Esempio 3
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ResponseHeader
```

Questi comandi restituiscono tutte le intestazioni di risposta disponibili.

### Esempio 4
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader - ServerVariable -RequestHeader -ResponseHeader
```

Questi comandi restituiscono tutte le variabili server disponibili, le intestazioni di richiesta e risposta.

### Esempio 5
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader
```

Questi comandi restituiscono tutte le variabili server disponibili, le intestazioni di richiesta e risposta.

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

### -RequestHeader
Intestazioni delle richieste disponibili per Application Gateway.

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
Intestazioni di risposta disponibili in Application Gateway.

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
Variabili server disponibili in Application Gateway.

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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### Nessuno

## OUTPUT

### Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult

## Note
**List-AzApplicationGatewayAvailableServerVariableAndHeader** è un alias per il cmdlet **Get-AzApplicationGatewayAvailableServerVariableAndHeader** .

## COLLEGAMENTI CORRELATI
