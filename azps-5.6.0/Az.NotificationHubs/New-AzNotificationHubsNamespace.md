---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3BA94976-DE88-4F07-9C06-41FEEDE1B829
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/new-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
ms.openlocfilehash: 20a4da67030962a238838247a7dcf137208e56b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951261"
---
# New-AzNotificationHubsNamespace

## SYNOPSIS
Crea uno spazio dei nomi dell'hub di notifica.

## SINTASSI

```
New-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **New-AzNotificationHubsHubsNotification crea** uno spazio dei nomi dell'hub di notifica.
Gli spazi dei nomi sono contenitori logici che consentono di organizzare e gestire gli hub di notifica.
È necessario avere almeno uno spazio dei nomi dell'hub di notifica.
Un singolo spazio dei nomi può ospitare più hub.
È possibile disporre di più spazi dei nomi per organizzare gli hub o per concedere a singoli utenti specifici l'autorizzazione per gestire un sottoinsieme selezionato degli hub.
Per creare uno spazio dei nomi, assicurarsi di specificare un nome univoco per lo spazio dei nomi; specificare il data center in cui si trova lo spazio dei nomi; e specificare il gruppo di risorse a cui verrà assegnato lo spazio dei nomi.
Dopo aver creato lo spazio dei nomi, è possibile usare il cmdlet New-AzNotificationHubsNamespaceAuthorizationRules per assegnare regole di autorizzazione a tale spazio dei nomi.
Le regole di autorizzazione vengono usate per gestire le autorizzazioni per lo spazio dei nomi.

## ESEMPI

### Esempio 1: Creare un hub di notifica
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners"
```

Questo comando crea un hub di notifica denominato ContosoPartners.
Lo spazio dei nomi si trova nel data center degli Stati Uniti occidentali e verrà assegnato al gruppo di risorse ContosoNotificationsGroup.

### Esempio 2: Creare un hub di notifica con tag
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners" -Tags @{Name="Audience";Value="PartnerOrganizations"}
```

Questo comando crea un hub di notifica denominato ContosoPartners.
Lo spazio dei nomi si trova nel data center degli Stati Uniti occidentali e verrà assegnato al gruppo di risorse ContosoNotificationsGroup.
Inoltre, questo comando crea un tag con il nome Gruppo di destinatari e il valore PartnerOrganizations e viene assegnato allo spazio dei nomi.
In questo modo lo spazio dei nomi verrà visualizzato ogni volta che si filtrano gli elementi in cui il tag Gruppo di destinatari è impostato su PartnerOrganizations.

## PARAMETERS

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

### -Location
Specifica il nome visualizzato del data center che ospiterà lo spazio dei nomi.
Anche se è possibile impostare questo parametro su qualsiasi posizione valida, per ottenere prestazioni ottimali è consigliabile usare un data center situato vicino alla maggior parte degli utenti.

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

### -Spazio dei nomi
Specifica il nome del nuovo spazio dei nomi.
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
Specifica il gruppo di risorse a cui verrà assegnato lo spazio dei nomi.
I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che consentono semplicemente la gestione e l'amministrazione dell'inventario.

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

### -SkuTier
Livello SKU dello spazio dei nomi

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Specifica coppie nome-valore che possono essere usate per categorizzare e organizzare gli elementi di Azure.
I tag funzionano in modo simile alle parole chiave e operano in una distribuzione.
Ad esempio, se si ricercano tutti gli elementi con il tag Department:IT, la ricerca restituirà tutti gli elementi azure che hanno quel tag, indipendentemente dal tipo di elemento, dalla posizione o dal gruppo di risorse.
Un singolo tag è costituito da due parti: *Name e,* facoltativamente, *value.*
Ad esempio, in Department:IT il nome del tag è Department e il valore del tag è IT.
Per aggiungere un tag, usare una sintassi della tabella hash simile alla seguente, che crea il tag CalendarYear:2016:

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Chiede conferma prima di eseguire il cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa accadrebbe se il cmdlet viene eseguito. Il cmdlet non viene eseguito.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### System.String

### System.Collections.Hashtable

## OUTPUT

### Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes

## NOTE

## COLLEGAMENTI CORRELATI

[Get-AzNotificationHubsHubsHubs](./Get-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsHubsHubs](./Remove-AzNotificationHubsNamespace.md)

[Set-AzNotificationHubsHubsHubs](./Set-AzNotificationHubsNamespace.md)


