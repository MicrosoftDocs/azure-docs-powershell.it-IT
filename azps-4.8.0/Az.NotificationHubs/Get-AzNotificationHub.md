---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
ms.openlocfilehash: d270e3020e03a02461d9c54e19458af10401ee79
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192265"
---
# Get-AzNotificationHub

## Sinossi
Ottiene le informazioni sugli hub di notifica.

## SINTASSI

```
Get-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzNotificationHub** ottiene le informazioni sugli hub di notifica in uno spazio dei nomi specificato e assegnato a un gruppo di risorse specificato.
Ad esempio, è possibile ottenere informazioni per tutti gli hub di notifica nello spazio dei nomi ContosoNamespace e assegnati al gruppo di risorse ContosoNotificationsGroup.
In alternativa, puoi usare il parametro *NotificationHub* per limitare i dati restituiti alle informazioni relative a un hub di notifica specifico.
Gli hub di notifica vengono usati per inviare notifiche push a più client, indipendentemente dalla piattaforma, ad esempio iOS, Android, Windows Phone 8 e Windows Store, usati da tali client.
Questi hub equivalgono approssimativamente alle singole app e ognuna delle tue app avrà in genere un hub di notifica personalizzato.
Questo cmdlet ottiene solo le informazioni sull'hub stesso.
Per ottenere informazioni sulle regole di autorizzazione, le stringhe di connessione e le credenziali del servizio di notifica della piattaforma, sono necessari altri cmdlet, ad esempio Get-AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys e Get-AzNotificationHubPNSCredentials.

## ESEMPI

### Esempio 1: ottenere informazioni per tutti gli hub di notifica in uno spazio dei nomi specifico
```
PS C:\>Get-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

Questo comando ottiene le informazioni per tutti gli hub di notifica nello spazio dei nomi denominato ContosoNamespace assegnati al gruppo di risorse ContosoNotificationsGroup.

## PARAMETRI

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
Specifica il nome dell'hub di notifica ottenuto da questo cmdlet.
Gli hub di notifica vengono usati per inviare notifiche push a più client indipendentemente dalla piattaforma utilizzata da tali client.

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

### -ResourceGroup
Specifica il gruppo di risorse a cui è assegnato l'hub di notifica.
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

### Microsoft. Azure. Commands. NotificationHubs. Models. NotificationHubAttributes

## Note

## COLLEGAMENTI CORRELATI

[Get-AzNotificationHubAuthorizationRule](./Get-AzNotificationHubAuthorizationRule.md)

[Get-AzNotificationHubListKey](./Get-AzNotificationHubListKey.md)

[Get-AzNotificationHubPNSCredential](./Get-AzNotificationHubPNSCredential.md)

[New-AzNotificationHub](./New-AzNotificationHub.md)

[Remove-AzNotificationHub](./Remove-AzNotificationHub.md)

[Set-AzNotificationHub](./Set-AzNotificationHub.md)


