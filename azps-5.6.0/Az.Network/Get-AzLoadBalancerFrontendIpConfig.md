---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6BEED413-E2E4-4557-BD31-2A655E790C1D
online version: https://docs.microsoft.com/powershell/module/az.network/get-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 2cafba2d579a37db45f12c5e3dd1746f799bfe21
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956798"
---
# Get-AzLoadBalancerFrontendIpConfig

## SYNOPSIS
Ottiene una configurazione IP front-end in un servizio di bilanciamento del carico.

## SINTASSI

```
Get-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Get-AzLoadBalancerFrontendIpConfig** ottiene una configurazione IP front-end o un elenco di configurazioni IP front-end in una soluzione di bilanciamento del carico.

## ESEMPI

### Esempio 1: Ottenere una configurazione IP front-end in un servizio di bilanciamento del carico
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -LoadBalancer $slb
```

Il primo comando ottiene la bilanciamento del carico denominata MyLoadBalancer e quindi la archivia nella variabile $slb.
Il secondo comando ottiene la configurazione IP front-end associata a questa bilanciamento del carico.

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

### -LoadBalancer
Specifica la bilanciamento del carico associata alla configurazione IP front-end da ottenere.

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

### -Name
Specifica il nome della bilanciamento del carico che contiene la configurazione IP front-end da ottenere.

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
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Microsoft.Azure.Commands.Network.Models.PSLoadBalancer

## OUTPUT

### Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration

## NOTE

## COLLEGAMENTI CORRELATI

[Add-AzLoadBalancerFrontendIpConfig](./Add-AzLoadBalancerFrontendIpConfig.md)

[Get-AzLoadBalancer](./Get-AzLoadBalancer.md)

[New-AzLoadBalancerFrontendIpConfig](./New-AzLoadBalancerFrontendIpConfig.md)

[Remove-AzLoadBalancerFrontendIpConfig](./Remove-AzLoadBalancerFrontendIpConfig.md)

[Set-AzLoadBalancerFrontendIpConfig](./Set-AzLoadBalancerFrontendIpConfig.md)


