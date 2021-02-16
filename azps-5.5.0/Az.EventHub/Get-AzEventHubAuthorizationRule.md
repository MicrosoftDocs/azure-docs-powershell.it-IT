---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 6940e12f813cbc4292f02ab98f0b35774da67025
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204131"
---
# Get-AzEventHubAuthorizationRule

## SYNOPSIS
Recupera i dettagli di una regola di autorizzazione o ottiene un elenco di regole di autorizzazione.

## SINTASSI

### NamespaceAuthorizationRuleSet (impostazione predefinita)
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventhubAuthorizationRuleSet
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Eventhub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AliasAuthoRuleSet
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il Get-AzEventHubAuthorizationRule cmdlet di autorizzazione ottiene i dettagli di una regola di autorizzazione oppure un elenco di tutte le regole di autorizzazione per un hub eventi specificato.
Se viene fornito il nome di una regola di autorizzazione, vengono restituiti i dettagli di quella singola regola di autorizzazione.
Se non viene fornito il nome di una regola di autorizzazione, viene restituito un elenco di tutte le regole di autorizzazione per l'hub eventi specificato.
Se è specificato il nome dell'alias di ripristino di emergenza, vengono restituiti i dettagli della regola di autorizzazione dello spazio dei nomi per l'alias configurato.

## ESEMPI

### Esempio 1: AuthorizationRule per lo spazio dei nomi
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyAuthRuleName
```

Ottiene la regola di autorizzazione \` MyAuthRuleName \` nello spazio dei nomi \` MyHostName. \`

### Esempio 2: AuthorizationRules per lo spazio dei nomi
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

Ottiene un elenco di tutte le regole di autorizzazione nello spazio \` dei nomi MyHostName. \`

### Esempio 3: AuthorizationRule per EventHub
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -Name MyAuthRuleName
```

Ottiene la regola di autorizzazione \` MyAuthRuleName \` nell'hub eventi MyEventHubName, il cui ambito è indicato dallo spazio dei nomi \` \` \` MyHubName. \`

### Esempio 4: AuthorizationRules per EventHub
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

Ottiene le regole di autorizzazione dell'elenco nell'hub eventi MyEventHubName, il cui ambito è indicato dallo spazio dei nomi \` \` \` MyHubName. \`

### Esempio 5: AuthorizationRule per l'alias (Configurazione georecovery)
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName -Name MyAuthRuleName
```

Ottiene la regola di autorizzazione \` MyAuthRuleName \` nello spazio dei nomi \` MyHostName. \`

### Esempio 6: AuthorizationRules per l'alias (Configurazione georecovery)
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName
```

Ottiene un elenco di tutte le regole di autorizzazione \` MyAuthRuleName \` nello spazio dei nomi \` MyHostName. \`

## PARAMETERS

### -AliasName
Nome alias

```yaml
Type: System.String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -Eventhub
Nome Eventhub

```yaml
Type: System.String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
AuthorizationRule Name

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Spazio dei nomi
Nome spazio dei nomi

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nome gruppo di risorse

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### System.String

## OUTPUT

### Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes

## NOTE

## COLLEGAMENTI CORRELATI
