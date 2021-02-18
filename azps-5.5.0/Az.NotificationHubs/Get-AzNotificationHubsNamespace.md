---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
ms.openlocfilehash: 3d0e604d3984a40acde02fb1f977e2922ae2d1d7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206435"
---
# Get-AzNotificationHubsNamespace

## SYNOPSIS
Ottiene informazioni sullo spazio dei nomi di un hub di notifica.

## SINTASSI

```
Get-AzNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Get-AzNotificationHubsHubsBlock ottiene** informazioni sugli spazi dei nomi dell'hub di notifica.
Questo cmdlet consente di ottenere informazioni per tutti gli spazi dei nomi, informazioni sugli spazi dei nomi assegnati a un gruppo di risorse specificato; o per restituire informazioni su uno spazio dei nomi specifico.
Gli spazi dei nomi sono contenitori logici che consentono di organizzare e gestire gli hub di notifica.
È necessario avere almeno uno spazio dei nomi dell'hub di notifica: tutti gli hub di notifica devono essere assegnati a uno spazio dei nomi.
Un singolo spazio dei nomi può ospitare più hub, quindi potrebbe essere necessario un solo spazio dei nomi nell'organizzazione.
Tuttavia, è anche possibile avere più spazi dei nomi per organizzare meglio gli hub o per assegnare a utenti specifici l'autorizzazione per gestire un sottoinsieme selezionato di hub.
Il cmdlet **Get-AzNotificationHubsHub restituisce** informazioni di base sullo spazio dei nomi stesso.
Per ottenere informazioni sulle regole di autorizzazione associate a uno spazio dei nomi, usare Get-AzNotificationHubsAuthorizationRules.

## ESEMPI

### Esempio 1: Ottenere informazioni per tutti gli spazi dei nomi dell'hub di notifica
```
PS C:\>Get-AzNotificationHubsNamespace
```

Questo comando restituisce informazioni per tutti gli spazi dei nomi dell'hub di notifica.

### Esempio 2: Ottenere informazioni per lo spazio dei nomi di un singolo hub di notifica
```
PS C:\>Get-AzNotificationHubsNamespace -Namespace "ContosoNamespace"
```

Questo comando recupera le informazioni per un singolo spazio dei nomi dell'hub di notifica: Contoso Contoso Contoso.

### Esempio 3: Ottenere informazioni per tutti gli hub di notifica assegnati a uno spazio dei nomi specifico
```
PS C:\>Get-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

Questo comando recupera le informazioni per tutti gli spazi dei nomi dell'hub di notifica assegnati al gruppo di risorse ContosoNotificationsGroup.

## PARAMETERS

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
I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che consentono semplicemente la gestione dell'inventario e l'amministrazione di Azure.

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
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### System.String

## OUTPUT

### Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes

## NOTE

## COLLEGAMENTI CORRELATI

[Get-AzNotificationHubsAuthorizationRule](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[New-AzNotificationHubsHubsHubs](./New-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsHubsHubs](./Remove-AzNotificationHubsNamespace.md)

[Set-AzNotificationHubsHubsHubs](./Set-AzNotificationHubsNamespace.md)


