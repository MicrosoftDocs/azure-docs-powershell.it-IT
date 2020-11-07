---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
ms.openlocfilehash: dbb475402ef4068f893cd7d444b5357bf1707578
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855049"
---
# Get-AzNotificationHubsNamespace

## Sinossi
Ottiene informazioni su uno spazio dei nomi dell'hub di notifica.

## SINTASSI

```
Get-AzNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
**Il cmdlet Get-AzNotificationHubsNamespace** ottiene le informazioni sugli spazi dei nomi dell'hub di notifica.
Questo cmdlet offre la possibilità di ottenere informazioni per tutti gli spazi dei nomi, informazioni sugli spazi dei nomi assegnati a un gruppo di risorse specificato. o per restituire informazioni su uno spazio dei nomi specifico.
Gli spazi dei nomi sono contenitori logici che consentono di organizzare e gestire gli hub di notifica.
È necessario avere almeno uno spazio dei nomi dell'hub di notifica: tutti gli hub di notifica devono essere assegnati a uno spazio dei nomi.
Un singolo spazio dei nomi può ospitare più hub, quindi potrebbe essere necessario uno spazio dei nomi nell'organizzazione.
Tuttavia, puoi anche avere più spazi dei nomi per organizzare meglio i tuoi Hub o per dare agli utenti specifici l'autorizzazione per gestire un subset selezionato di hub.
Il cmdlet **Get-AzNotificationHubsNamespace** restituisce le informazioni di base sullo spazio dei nomi stesso.
Per ottenere informazioni sulle regole di autorizzazione associate a uno spazio dei nomi, utilizzare Get-AzNotificationHubsNamespaceAuthorizationRules.

## ESEMPI

### Esempio 1: ottenere informazioni per tutti gli spazi dei nomi dell'hub di notifica
```
PS C:\>Get-AzNotificationHubsNamespace
```

Questo comando restituisce informazioni per tutti gli spazi dei nomi dell'hub di notifica.

### Esempio 2: ottenere informazioni per un singolo spazio dei nomi dell'hub di notifica
```
PS C:\>Get-AzNotificationHubsNamespace -Namespace "ContosoNamespace"
```

Questo comando ottiene le informazioni per un singolo spazio dei nomi dell'hub di notifica: ContosoNamespace.

### Esempio 3: ottenere informazioni per tutti gli hub di notifica assegnati a uno spazio dei nomi specifico
```
PS C:\>Get-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

Questo comando ottiene le informazioni per tutti gli spazi dei nomi dell'hub di notifica assegnati al gruppo di risorse ContosoNotificationsGroup.

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
Specifica un nome univoco per lo spazio dei nomi.
Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroup
Specifica il gruppo di risorse a cui è assegnato lo spazio dei nomi.
I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che semplificano la gestione dell'inventario e l'amministrazione di Azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### System. String

## OUTPUT

### Microsoft. Azure. Commands. NotificationHubs. Models. NamespaceAttributes

## Note

## COLLEGAMENTI CORRELATI

[Get-AzNotificationHubsNamespaceAuthorizationRules](./Get-AzNotificationHubsNamespaceAuthorizationRules.md)

[New-AzNotificationHubsNamespace](./New-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)

[Set-AzNotificationHubsNamespace](./Set-AzNotificationHubsNamespace.md)


