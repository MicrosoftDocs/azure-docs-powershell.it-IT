---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: f3ba8428a6f6a9e618872e1292234751979b3c4b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206426"
---
# Get-AzNotificationHubsNamespaceAuthorizationRule

## SYNOPSIS
Ottiene informazioni sulle regole di autorizzazione associate a uno spazio dei nomi dell'hub di notifica.

## SINTASSI

```
Get-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Get-AzNotificationHubsAuthorizationRule** restituisce informazioni sulle regole di autorizzazione della firma di accesso condiviso associate a uno spazio dei nomi dell'hub di notifica.
È possibile restituire informazioni su tutte le regole associate allo spazio dei nomi.
In alternativa, includendo il *parametro AuthorizationRule,* è possibile restituire informazioni per una regola specifica.
Le regole di autorizzazione gestiscono l'accesso agli spazi dei nomi.
Questa operazione viene eseguita mediante la creazione di collegamenti, come URI, in base a diversi livelli di autorizzazione.
I livelli della piattaforma possono essere uno dei seguenti: 
- Ascoltare
- Invia
- La gestione dei client viene indirizzata a uno di questi URL in base al livello di autorizzazione appropriato.
Ad esempio, un client con l'autorizzazione di ascolto verrà indirizzato all'URI per tale autorizzazione.
Questo cmdlet ottiene solo le regole di autorizzazione associate a uno spazio dei nomi.
Per ottenere informazioni sullo spazio dei nomi stesso, usare Get-AzNotificationHubsHubsHubs.

## ESEMPI

### Esempio 1: Ottenere informazioni su tutte le regole di autorizzazione assegnate agli spazi dei nomi
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

Questo comando ottiene informazioni su tutte le regole di autorizzazione assegnate sia allo spazio dei nomi ContosoCliente che al gruppo di risorse ContosoNotificationsGroup.

### Esempio 2: Ottenere informazioni su una regola di autorizzazione
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

Questo comando ottiene informazioni su una singola regola di autorizzazione dello spazio dei nomi denominata ListenRule.
Quando si ottengono informazioni per una regola di autorizzazione specifica, è necessario includere lo spazio dei nomi e il gruppo di risorse.

## PARAMETERS

### -AuthorizationRule
Specifica il nome di una regola di autenticazione della firma di accesso condiviso.
Queste regole determinano il tipo di accesso che gli utenti hanno allo spazio dei nomi.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure

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

### -Spazio dei nomi
Specifica lo spazio dei nomi a cui vengono assegnate le regole di autorizzazione.
Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroup
Specifica il gruppo di risorse a cui sono assegnate le regole di autorizzazione.
I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che consentono semplicemente la gestione dell'inventario e l'amministrazione di Azure.

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

### Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes

## NOTE

## COLLEGAMENTI CORRELATI

[Get-AzNotificationHubsHubsHubs](./Get-AzNotificationHubsNamespace.md)

[New-AzNotificationHubsHubsHubs](./New-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsHubsHubs](./Remove-AzNotificationHubsNamespace.md)

[Set-AzNotificationHubsHubsHubs](./Set-AzNotificationHubsNamespace.md)


