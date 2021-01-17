---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: b8683d461fe442ec0ad20098766d975b4cd6ae73
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380096"
---
# Get-AzLoadBalancerOutboundRuleConfig

## Sinossi
Ottiene una configurazione della regola in uscita in un programma di bilanciamento del carico.

## SINTASSI

```
Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzLoadBalancerOutboundRuleConfig** ottiene una configurazione della regola in uscita o un elenco di configurazioni di regole in uscita in un programma di bilanciamento del carico.

## ESEMPI

### Esempio 1: ottenere una configurazione della regola in uscita in un programma di bilanciamento del carico
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer $slb -Name "MyRule"
```

Il primo comando ottiene il bilanciamento del carico denominato MyLoadBalancer e lo archivia nella variabile $slb.
Il secondo comando ottiene la configurazione della regola in uscita denominata regola associata al bilanciamento del carico.

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

### -LoadBalancer
Riferimento della risorsa di bilanciamento del carico.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Nome
Nome della regola in uscita.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### Microsoft. Azure. Commands. Network. Models. PSLoadBalancer

## OUTPUT

### Microsoft. Azure. Commands. Network. Models. PSOutboundRule

## Note

## COLLEGAMENTI CORRELATI

[Add-AzLoadBalancerOutboundRuleConfig](./Add-AzLoadBalancerOutboundRuleConfig.md)

[New-AzLoadBalancerOutboundRuleConfig](./New-AzLoadBalancerOutboundRuleConfig.md)

[Remove-AzLoadBalancerOutboundRuleConfig](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[Set-AzLoadBalancerOutboundRuleConfig](./Set-AzLoadBalancerOutboundRuleConfig.md)
