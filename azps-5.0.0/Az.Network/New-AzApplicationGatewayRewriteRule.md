---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriterule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
ms.openlocfilehash: 5eaa5cdc8b00fa13d9fc0c06821b664f1afc2a65
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310278"
---
# New-AzApplicationGatewayRewriteRule

## Sinossi
Crea una regola di riscrittura per un gateway dell'applicazione.

## SINTASSI

```
New-AzApplicationGatewayRewriteRule -Name <String> -ActionSet <PSApplicationGatewayRewriteRuleActionSet>
 [-RuleSequence <Int32>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
**Il cmdlet New-AzApplicationGatewayRewriteRule** crea una regola di riscrittura per un gateway dell'applicazione Azure.

## ESEMPI

### Esempio 1: creare una regola di riscrittura per un gateway applicazione
```powershell
PS C:\> $rule = New-AzApplicationGatewayRewriteRule -Name rule1 -ActionSet $action -RuleSequence 101 -Condition $condition
```

Questo comando crea una regola di riscrittura denominata Rule1 e archivia il risultato nella variabile denominata $rule.

## PARAMETRI

### -Actiont
Actiont della regola di riscrittura

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Condition
Condizione per l'esecuzione della regola di riscrittura

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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
Nome del RewriteRule

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

### -RuleSequence
Ordinamento delle regole di questa regola di riscrittura nel set di regole di riscrittura

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno

## OUTPUT

### Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRewriteRule

## Note

## COLLEGAMENTI CORRELATI

[Add-AzApplicationGatewayRewriteRuleSet](./Add-AzApplicationGatewayRewriteRuleSet.md)

[Get-AzApplicationGatewayRewriteRuleSet](./Get-AzApplicationGatewayRewriteRuleSet.md)

[New-AzApplicationGatewayRewriteRuleSet](./New-AzApplicationGatewayRewriteRuleSet.md)

[Remove-AzApplicationGatewayRewriteRuleSet](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[Set-AzApplicationGatewayRewriteRuleSet](./Set-AzApplicationGatewayRewriteRuleSet.md)

[New-AzApplicationGatewayRewriteRuleActionSet](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[New-AzApplicationGatewayRewriteRuleHeaderConfiguration](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
