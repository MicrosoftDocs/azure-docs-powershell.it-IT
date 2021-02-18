---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F769A8AB-E025-49EE-AEA4-0D27EAEE341F
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespacelistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
ms.openlocfilehash: 88e43b182694b50169738e0b775d9202aac15ffa
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100410464"
---
# Get-AzNotificationHubsNamespaceListKey

## SYNOPSIS
Ottiene le stringhe di connessione primaria e secondaria associate a una regola di autorizzazione dello spazio dei nomi dell'hub di notifica.

## SINTASSI

```
Get-AzNotificationHubsNamespaceListKey [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Get-AzNotificationHubsNotificationListKey** restituisce le stringhe di connessione primaria e secondaria per una regola di autorizzazione della firma di accesso condiviso assegnata a uno spazio dei nomi dell'hub di notifica.
Le regole di autorizzazione gestiscono i diritti utente per uno spazio dei nomi dell'hub di notifica.
Ogni regola include una stringa di connessione principale e una secondaria.

## ESEMPI

### Esempio 1: Ottenere le stringhe di connessione primaria e secondaria per una regola di autorizzazione
```
PS C:\>Get-AzNotificationHubsNamespaceListKey -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

Questo comando restituisce le stringhe di connessione primaria e secondaria per la regola di autorizzazione denominata ListenRule assegnata allo spazio dei nomi Contoso Contoso Contoso.
Quando si esegue questo comando è necessario includere il nome del gruppo di risorse a cui è assegnato lo spazio dei nomi.

## PARAMETERS

### -AuthorizationRule
Specifica il nome di una regola di autenticazione della firma di accesso condiviso.
Queste regole determinano il tipo di accesso all'hub di notifica a cui gli utenti hanno accesso.

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
Specifica lo spazio dei nomi contenente le stringhe di connessione recuperate dal cmdlet.

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
Specifica il gruppo di risorse a cui è assegnato lo spazio dei nomi.
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
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### System.String

## OUTPUT

### Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys

## NOTE

## COLLEGAMENTI CORRELATI

[Get-AzNotificationHubsHubsHubs](./Get-AzNotificationHubsNamespace.md)



