---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheFirewallRule.md
ms.openlocfilehash: 7f2e9a3bb54aab9def9eba7bdc2a84680fe121c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508007"
---
# Remove-AzureRmRedisCacheFirewallRule

## Sinossi
Rimuovere una regola del firewall da una cache di Redis.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### NormalParameterSet (impostazione predefinita)
```
Remove-AzureRmRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### PSRedisFirewallRuleObject
```
Remove-AzureRmRedisCacheFirewallRule -InputObject <PSRedisFirewallRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Rimuovere una regola del firewall da una cache di Redis.

## ESEMPI

### Esempio 1: rimuovere una singola regola del firewall
```
PS C:\>Remove-AzureRmRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -PassThru
True
```

Questo comando rimuove una regola del firewall denominata ruleone dalla cache Redis denominata cache. 

## PARAMETRI

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
oggetto di tipo PSRedisFirewallRule

```yaml
Type: PSRedisFirewallRule
Parameter Sets: PSRedisFirewallRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nome
Nome della cache di Redis.

```yaml
Type: String
Parameter Sets: NormalParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
{{Fill PassThru Description}}

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nome del gruppo di risorse in cui è presente la cache.

```yaml
Type: String
Parameter Sets: NormalParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RuleName
Nome della regola del firewall.

```yaml
Type: String
Parameter Sets: NormalParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confermare
Richiede la conferma prima di eseguire il cmdlet.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### System. String

## OUTPUT

### System. Boolean

## Note

## COLLEGAMENTI CORRELATI

[New-AzureRmRedisCacheFirewallRule](./New-AzureRmRedisCacheFirewallRule.md)

[Get-AzureRmRedisCacheFirewallRule](./Get-AzureRmRedisCacheFirewallRule.md)

[Get-AzureRmRedisCache](./Get-AzureRmRedisCache.md)

[New-AzureRmRedisCache](./New-AzureRmRedisCache.md)

[Remove-AzureRmRedisCache](./Remove-AzureRmRedisCache.md)

[Set-AzureRmRedisCache](./Set-AzureRmRedisCache.md)
