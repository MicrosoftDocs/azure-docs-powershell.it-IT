---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: e91b7edacc575ac98eb78ae44c88be4f6873f34c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521672"
---
# Get-AzureRmEventHubNamespaceKey

## Sinossi
Ottiene i dettagli delle chiavi connectionStrings primarie e secondarie per la regola di autorizzazione della regola di autorizzazione dello spazio dei nomi Hub eventi specificato.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Get-AzureRmEventHubNamespaceKey [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthorizationRuleName] <String>
```

## Descrizione
Il cmdlet Get-AzureRmEventHubNamespaceKey restituisce i dati connectionStrings principali e secondari e i dettagli delle chiavi della regola di autorizzazione specificata nello spazio dei nomi dell'hub eventi specificato.

## ESEMPI

### Esempio 1
```
PS C:\> Get-AzureRmEventHubNamespaceKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

Ottiene i dettagli delle caratteristiche connectionStrings primarie e secondarie e delle chiavi per la regola di autorizzazione \` MyAuthRuleName nello \` spazio dei nomi Hub eventi mynamespacename \` \` nel gruppo di risorse \` MyResourceGroupName \` .

## PARAMETRI

### -AuthorizationRuleName
Nome della regola di autorizzazione nello spazio dei nomi Hub eventi.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
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

### Microsoft. Azure. Commands. EventHub. Models. ListKeysAttributes

## Note

## COLLEGAMENTI CORRELATI

