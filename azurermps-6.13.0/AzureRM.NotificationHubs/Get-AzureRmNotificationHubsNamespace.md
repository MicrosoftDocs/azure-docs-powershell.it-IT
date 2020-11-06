---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: b4603566b793cbded7e593c9e4a23c3788c140de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521319"
---
# Get-AzureRmNotificationHubsNamespace

## Sinossi
Ottiene informazioni su uno spazio dei nomi dell'hub di notifica.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Get-AzureRmNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
**Il cmdlet Get-AzureRmNotificationHubsNamespace** ottiene le informazioni sugli spazi dei nomi dell'hub di notifica.
Questo cmdlet offre la possibilità di ottenere informazioni per tutti gli spazi dei nomi, informazioni sugli spazi dei nomi assegnati a un gruppo di risorse specificato. o per restituire informazioni su uno spazio dei nomi specifico.
Gli spazi dei nomi sono contenitori logici che consentono di organizzare e gestire gli hub di notifica.
È necessario avere almeno uno spazio dei nomi dell'hub di notifica: tutti gli hub di notifica devono essere assegnati a uno spazio dei nomi.
Un singolo spazio dei nomi può ospitare più hub, quindi potrebbe essere necessario uno spazio dei nomi nell'organizzazione.
Tuttavia, puoi anche avere più spazi dei nomi per organizzare meglio i tuoi Hub o per dare agli utenti specifici l'autorizzazione per gestire un subset selezionato di hub.
Il cmdlet **Get-AzureRmNotificationHubsNamespace** restituisce le informazioni di base sullo spazio dei nomi stesso.
Per ottenere informazioni sulle regole di autorizzazione associate a uno spazio dei nomi, utilizzare Get-AzureRmNotificationHubsNamespaceAuthorizationRules.

## ESEMPI

### Esempio 1: ottenere informazioni per tutti gli spazi dei nomi dell'hub di notifica
```
PS C:\>Get-AzureRmNotificationHubsNamespace
```

Questo comando restituisce informazioni per tutti gli spazi dei nomi dell'hub di notifica.

### Esempio 2: ottenere informazioni per un singolo spazio dei nomi dell'hub di notifica
```
PS C:\>Get-AzureRmNotificationHubsNamespace -Namespace "ContosoNamespace"
```

Questo comando ottiene le informazioni per un singolo spazio dei nomi dell'hub di notifica: ContosoNamespace.

### Esempio 3: ottenere informazioni per tutti gli hub di notifica assegnati a uno spazio dei nomi specifico
```
PS C:\>Get-AzureRmNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

Questo comando ottiene le informazioni per tutti gli spazi dei nomi dell'hub di notifica assegnati al gruppo di risorse ContosoNotificationsGroup.

## PARAMETRI

### -DefaultProfile
Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure

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

[Get-AzureRmNotificationHubsNamespaceAuthorizationRules](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[New-AzureRmNotificationHubsNamespace](./New-AzureRmNotificationHubsNamespace.md)

[Remove-AzureRmNotificationHubsNamespace](./Remove-AzureRmNotificationHubsNamespace.md)

[Set-AzureRmNotificationHubsNamespace](./Set-AzureRmNotificationHubsNamespace.md)


