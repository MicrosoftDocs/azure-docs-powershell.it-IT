---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 2CCDF339-9D6E-4B0C-9201-BE641C8827F6
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubpnscredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubPNSCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubPNSCredential.md
ms.openlocfilehash: 282e8092050b5859809c8dad71c4da1ee86c779d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192720"
---
# Get-AzNotificationHubPNSCredential

## Sinossi
Ottiene le credenziali PNS per un hub di notifica.

## SINTASSI

```
Get-AzNotificationHubPNSCredential [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzNotificationHubPNSCredential** ottiene le credenziali del servizio di notifica della piattaforma (PNS) per un hub di notifica.
Ogni hub di notifica ha un singolo set di credenziali PNS.
Queste credenziali vengono applicate ai singoli servizi di notifica push, ad esempio, ma non limitati a; il servizio di notifica push di iOS, il servizio di notifica push Android e Windows Phone 8.

## ESEMPI

### Esempio 1: ottenere le credenziali PNS per un hub di notifica specifico
```
PS C:\>Get-AzNotificationHubPNSCredential -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

Questo comando ottiene le credenziali PNS per l'hub di notifica denominato ContosoInternalHub che appartiene al gruppo di risorse denominato ContosoNotificationsGroup.

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
Specifica l'hub di notifica a cui sono assegnate le credenziali PNS.
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

[Get-AzNotificationHub](./Get-AzNotificationHub.md)


