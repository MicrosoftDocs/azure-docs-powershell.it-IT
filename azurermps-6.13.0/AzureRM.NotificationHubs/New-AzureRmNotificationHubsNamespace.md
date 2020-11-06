---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 3BA94976-DE88-4F07-9C06-41FEEDE1B829
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/new-azurermnotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: d4bba9d54dac21a8eb19a4b161bb2fdef29d4bb7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521315"
---
# New-AzureRmNotificationHubsNamespace

## Sinossi
Crea uno spazio dei nomi Hub di notifica.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
New-AzureRmNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzureRmNotificationHubsNamespace** crea uno spazio dei nomi dell'hub di notifica.
Gli spazi dei nomi sono contenitori logici che consentono di organizzare e gestire gli hub di notifica.
È necessario avere almeno uno spazio dei nomi dell'hub di notifica.
Un singolo spazio dei nomi può ospitare più hub.
Puoi disporre di più spazi dei nomi per organizzare i tuoi Hub o per dare agli utenti specifici l'autorizzazione per gestire un subset selezionato degli hub.
Per creare uno spazio dei nomi, assicurati di specificare un nome univoco per lo spazio dei nomi; specificare il Data Center in cui verrà posizionato lo spazio dei nomi; e specifica il gruppo di risorse a cui verrà assegnato lo spazio dei nomi.
Dopo aver creato lo spazio dei nomi, puoi usare il cmdlet New-AzureRmNotificationHubsNamespaceAuthorizationRules per assegnare le regole di autorizzazione a tale spazio dei nomi.
Le regole di autorizzazione vengono usate per gestire le autorizzazioni per lo spazio dei nomi.

## ESEMPI

### Esempio 1: creare un hub di notifica
```
PS C:\>New-AzureRmNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners"
```

Questo comando crea un hub di notifica denominato ContosoPartners.
Lo spazio dei nomi sarà disponibile nel Data Center ovest degli Stati Uniti e verrà assegnato al gruppo di risorse ContosoNotificationsGroup.

### Esempio 2: creare un hub di notifica con tag
```
PS C:\>New-AzureRmNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners" -Tags @{Name="Audience";Value="PartnerOrganizations"}
```

Questo comando crea un hub di notifica denominato ContosoPartners.
Lo spazio dei nomi sarà disponibile nel Data Center ovest degli Stati Uniti e verrà assegnato al gruppo di risorse ContosoNotificationsGroup.
Questo comando crea inoltre un tag con il nome audience e il valore PartnerOrganizations e viene assegnato allo spazio dei nomi.
In questo modo, lo spazio dei nomi verrà visualizzato ogni volta che filtri per gli elementi in cui il tag audience è impostato su PartnerOrganizations.

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

### -Posizione
Specifica il nome visualizzato del centro dati che ospiterà lo spazio dei nomi.
Anche se è possibile impostare questo parametro su qualsiasi posizione valida, per ottenere prestazioni ottimali, è consigliabile usare un data center situato in prossimità della maggior parte degli utenti.

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
I gruppi di risorse organizzano elementi come spazi dei nomi, hub di notifica e regole di autorizzazione in modi che semplificano la gestione e l'amministrazione dell'inventario.

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
Specifica le coppie nome/valore che possono essere usate per categorizzare e organizzare gli elementi Azure.
I tag funzionano in modo simile alle parole chiave e funzionano in una distribuzione.
Ad esempio, se si cercano tutti gli elementi con il reparto Tag: la ricerca restituirà tutti gli elementi di Azure che hanno il tag, indipendentemente da oggetti come il tipo di elemento, la posizione o il gruppo di risorse.
Un singolo tag è costituito da due parti: il *nome* e, facoltativamente, il *valore*.
Ad esempio, nel reparto: il nome del tag è reparto e il valore di tag è.
Per aggiungere un tag, usa la sintassi della tabella hash simile alla seguente, che crea il tag CalendarYear: 2016:

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

### -Confermare
Richiede la conferma prima di eseguire il cmdlet.

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
Mostra cosa succede se il cmdlet viene eseguito. Il cmdlet non viene eseguito.

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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### System. String

### System. Collections. Hashtable

## OUTPUT

### Microsoft. Azure. Commands. NotificationHubs. Models. NamespaceAttributes

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureRmNotificationHubsNamespace](./Get-AzureRmNotificationHubsNamespace.md)

[Remove-AzureRmNotificationHubsNamespace](./Remove-AzureRmNotificationHubsNamespace.md)

[Set-AzureRmNotificationHubsNamespace](./Set-AzureRmNotificationHubsNamespace.md)


