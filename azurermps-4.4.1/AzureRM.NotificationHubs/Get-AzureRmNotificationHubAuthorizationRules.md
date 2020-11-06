---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 7A9D8F5A-6035-411B-8FDB-96ABFEED05A2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: 5d2398e86a5507e5672dba46cafbbb1f27c402a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521570"
---
# Get-AzureRmNotificationHubAuthorizationRules

## Sinossi
Ottiene informazioni sulle regole di autorizzazione associate a un hub di notifica.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Get-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureRmNotificationHubAuthorizationRules** ottiene informazioni sulle regole di autorizzazione della firma di accesso condiviso (SAS) associate a un hub di notifica.
Il cmdlet restituisce informazioni su tutte le regole associate a un hub o, includendo il parametro *AuthorizationRule* , ottiene informazioni su una regola specifica.

Le regole di autorizzazione gestiscono l'accesso agli hub di notifica.
Una regola di autorizzazione creerà collegamenti, come URI, in base a livelli di autorizzazione diversi.
I client vengono indirizzati a uno di questi URI in base al livello di autorizzazione appropriato.
Ad esempio, un client con l'autorizzazione Listen verrà indirizzato all'URI per l'autorizzazione.

Il cmdlet **Get-AzureRmNotificationHubAuthorizationRules** ottiene solo le informazioni sulle regole di autorizzazione associate a un hub di notifica.
Per ottenere informazioni sull'hub stesso, USA Get-AzureRmNotificationHub.

## ESEMPI

### Esempio 1: ottenere informazioni per tutte le regole di autorizzazione assegnate a un hub di notifica
```
PS C:\>Get-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

Questo comando ottiene le informazioni per tutte le regole di autorizzazione assegnate all'hub di notifica denominato ContosoInternalHub nello spazio dei nomi ContosoNamespace.
Devi specificare lo spazio dei nomi in cui si trova l'hub e il gruppo di risorse a cui è stato assegnato l'hub.

### Esempio 2: ottenere informazioni per le regole di autorizzazione assegnate a un hub di notifica
```
PS C:\>Get-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub" -AuthorizationRule "ListenRule"
```

Questo comando ottiene le informazioni per tutte le regole di autorizzazione assegnate all'hub di notifica denominato ContosoInternalHub nello spazio dei nomi ContosoNamespace.
Il comando usa il parametro *AuthorizationRule* per limitare i dati restituiti a una singola regola di autorizzazione denominata ListenRule.

## PARAMETRI

### -AuthorizationRule
Specifica il nome di una regola di autenticazione SAS.
Queste regole determinano il tipo di accesso che gli utenti hanno all'hub di notifica.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Spazio dei nomi
Specifica lo spazio dei nomi a cui è assegnato l'hub di notifica.
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

### -NotificationHub
Specifica l'hub di notifica che questo cmdlet assegna le regole di autorizzazione.
Gli hub di notifica vengono usati per inviare notifiche push a più client indipendentemente dalla piattaforma utilizzata da tali client.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroup
Specifica il gruppo di risorse a cui è assegnato l'hub di notifica.
I gruppi di risorse organizzano elementi come spazi dei nomi, hub di notifica e regole di autorizzazione in modi che semplificano la gestione delle scorte e l'amministrazione di Azure.

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

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

### System. Collections. Generic. list ' 1 [Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes]

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureRmNotificationHubsNamespaceAuthorizationRules](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[New-AzureRmNotificationHubAuthorizationRules](./New-AzureRmNotificationHubAuthorizationRules.md)

[Remove-AzureRmNotificationHubAuthorizationRules](./Remove-AzureRmNotificationHubAuthorizationRules.md)

[Set-AzureRmNotificationHubAuthorizationRules](./Set-AzureRmNotificationHubAuthorizationRules.md)


