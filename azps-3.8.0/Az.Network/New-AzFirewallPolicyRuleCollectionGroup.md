---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 1aeb93085fdf8fa362e38843deacdef6e07929d7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019770"
---
# New-AzFirewallPolicyRuleCollectionGroup

## Sinossi
Creare un nuovo gruppo di raccolta regole criteri di Azure firewall

## SINTASSI

### SetByInputObjectParameterSet
```
New-AzFirewallPolicyRuleCollectionGroup -Name <String> -Priority <UInt32>
 -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]> -ResourceGroupName <String>
 -FirewallPolicyObject <PSAzureFirewallPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetByNameParameterSet
```
New-AzFirewallPolicyRuleCollectionGroup -Name <String> -Priority <UInt32>
 -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]> -ResourceGroupName <String>
 -FirewallPolicyName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzFirewallPolicyRuleCollectionGroup** crea un gruppo di insiemi di regole in un criterio firewall di Azure.

## ESEMPI

### Esempio 1
```powershell
PS C:\> New-AzFirewallPolicyRuleCollectionGroup -Name rg1 -ResourceGroupName TestRg -Location westus -Priority 200 -RuleCollection $filterRule1 -AzureFirewallPolicy $fp
```

Questo esempio crea un gruppo di insiemi di regole nel criterio firewall $fp

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

### -FirewallPolicyName
Nome del criterio firewall

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FirewallPolicyObject
Criteri firewall.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Nome del gruppo di regole

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

### -Priorità
Priorità del gruppo di regole

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nome del gruppo di risorse.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RuleCollection
Elenco di regole

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyBaseRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confermare
Richiede la conferma prima di eseguire il cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa succede se il cmdlet viene eseguito.
Il cmdlet non viene eseguito.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### System. String

### Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicy

## OUTPUT

### Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicyRuleCollectionGroup

## Note

## COLLEGAMENTI CORRELATI
