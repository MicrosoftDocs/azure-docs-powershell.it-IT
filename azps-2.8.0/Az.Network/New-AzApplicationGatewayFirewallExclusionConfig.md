---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallexclusionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallExclusionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallExclusionConfig.md
ms.openlocfilehash: 58060c488e778510822d9bc86a21de216447e0f4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93853581"
---
# New-AzApplicationGatewayFirewallExclusionConfig

## Sinossi
Crea un nuovo elenco di regole di esclusione per Application Gateway WAF

## SINTASSI

```
New-AzApplicationGatewayFirewallExclusionConfig -Variable <String> -Operator <String> -Selector <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Cmdlet **New-AzApplicationGatewayFirewallExclusionConfig** un nuovo elenco di regole di esclusione per il gateway applicazione WAF.

## ESEMPI

### Esempio 1
```powershell
PS C:\> $exclusion1 = New-AzApplicationGatewayFirewallExclusionConfig -Variable "RequestHeaderNames" -Operator "StartsWith" -Selector "xyz"
```

Questo comando crea una nuova regola di esclusione elenca la configurazione per la variabile denominata RequestHeaderNames e operator denominata StartsWith e Selector denominata XYZ. La configurazione dell'elenco di esclusione viene salvata in $exclusion 1.

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

### -Operator
Quando la variabile è una raccolta, usare il selettore per specificare gli elementi della raccolta a cui si applica questa esclusione.

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

### -Selector
Quando la variabile è una raccolta, operator usato per specificare gli elementi della raccolta a cui si applica questa esclusione.

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

### -Variabile
Variabile da escludere.

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

### Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallExclusion

## Note

## COLLEGAMENTI CORRELATI
