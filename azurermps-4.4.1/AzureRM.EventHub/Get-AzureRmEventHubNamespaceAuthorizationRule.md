---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: bad0e86061a5ffaa937209d778d5eaa83e29879d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688318"
---
# Get-AzureRmEventHubNamespaceAuthorizationRule

## Sinossi
Ottiene i dettagli di una regola di autorizzazione dello spazio dei nomi Eventubs o ottiene un elenco di regole di autorizzazione.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Get-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [[-AuthorizationRuleName] <String>]
```

## Descrizione
Il cmdlet Get-AzureRmEventHubNamespaceAuthorizationRule ottiene i dettagli di una regola di autorizzazione dello spazio dei nomi degli hub eventi specificata o un elenco di regole di autorizzazione dello spazio dei nomi.
Se viene specificato il nome della regola di autorizzazione, vengono restituiti i dettagli di una singola regola di autorizzazione.
Se non viene specificato un nome per la regola di autorizzazione, viene restituito un elenco di tutte le regole di autorizzazione nello spazio dei nomi.

## ESEMPI

### Esempio 1
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

Restituisce la regola \` di autorizzazione MyAuthRuleName \` nello spazio dei nomi Hub di eventi NamespaceName \` \` , con il gruppo di risorse \` MyResourceGroupName \` .

### Esempio 2
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName RootManageSharedAccessKey
```

Restituisce la regola di autorizzazione predefinita \` RootManageSharedAccessKey \` nello spazio dei nomi Hub di eventi NamespaceName \` \` , con il gruppo di risorse \` MyResourceGroupName \` .

### Esempio 3
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName
```

Restituisce tutte le regole di autorizzazione nello spazio dei nomi Hub eventi NamespaceName \` \` , con il gruppo di risorse \` MyResourceGroupName \` .

## PARAMETRI

### -AuthorizationRuleName
Nome della regola di autorizzazione dello spazio dei nomi Hub eventi.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NamespaceName
Nome dello spazio dei nomi Hub eventi.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nome del gruppo di risorse.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## INGRESSI

### System. String

## OUTPUT

### System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. EventHub. Models. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. Commands. EventHub, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]

## Note

## COLLEGAMENTI CORRELATI

