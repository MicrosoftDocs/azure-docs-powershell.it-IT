---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: f3ba8428a6f6a9e618872e1292234751979b3c4b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488842"
---
# Get-AzNotificationHubsNamespaceAuthorizationRule

## Sinossi
Ottiene informazioni sulle regole di autorizzazione associate a uno spazio dei nomi dell'hub di notifica.

## SINTASSI

```
Get-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzNotificationHubsNamespaceAuthorizationRule** restituisce informazioni sulle regole di autorizzazione della firma di accesso condiviso (SAS) associate a uno spazio dei nomi dell'hub di notifica.
Puoi restituire informazioni su tutte le regole associate allo spazio dei nomi.
In alternativa, e includendo il parametro *AuthorizationRule* , puoi restituire informazioni per una regola specifica.
Le regole di autorizzazione gestiscono l'accesso agli spazi dei nomi.
Questa operazione viene eseguita tramite la creazione di collegamenti, come URI, in base a livelli di autorizzazione diversi.
I livelli della piattaforma possono essere uno dei seguenti: 
- Ascoltare
- Invia
- I client di gestione vengono indirizzati a uno di questi URI in base al livello di autorizzazione appropriato.
Ad esempio, un client assegnato l'autorizzazione Listen verrà indirizzato all'URI per l'autorizzazione.
Questo cmdlet ottiene solo le regole di autorizzazione associate a uno spazio dei nomi.
Per ottenere informazioni sullo spazio dei nomi stesso, USA Get-AzNotificationHubsNamespace.

## ESEMPI

### Esempio 1: ottenere informazioni su tutte le regole di autorizzazione assegnate agli spazi dei nomi
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

Questo comando consente di ottenere informazioni su tutte le regole di autorizzazione assegnate sia allo spazio dei nomi ContosoNamespace che al gruppo di risorse ContosoNotificationsGroup.

### Esempio 2: ottenere informazioni su una regola di autorizzazione
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

Questo comando consente di ottenere informazioni su una singola regola di autorizzazione dello spazio dei nomi denominata ListenRule.
È necessario includere lo spazio dei nomi e il gruppo di risorse quando si ottengono informazioni per una specifica regola di autorizzazione.

## PARAMETRI

### -AuthorizationRule
Specifica il nome di una regola di autenticazione SAS.
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
Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure

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
I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che semplificano la gestione dell'inventario e l'amministrazione di Azure.

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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### System. String

## OUTPUT

### Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes

## Note

## COLLEGAMENTI CORRELATI

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)

[New-AzNotificationHubsNamespace](./New-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)

[Set-AzNotificationHubsNamespace](./Set-AzNotificationHubsNamespace.md)


