---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 1B2AA717-ECD6-4CC0-AB6D-A199AF21A4A5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/set-azurermnotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: b1fe6ae9085dcfc1d74eaf86af831a1e984a9143
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688436"
---
# Set-AzureRmNotificationHubsNamespace

## Sinossi
Imposta i valori delle proprietà per uno spazio dei nomi Hub di notifica.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Set-AzureRmNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-State] <NamespaceState>] [[-Critical] <Boolean>] [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet **set-AzureRmNotificationHubsNamespace** imposta i valori delle proprietà di uno spazio dei nomi esistente dell'hub di notifica.

Gli spazi dei nomi sono contenitori logici che consentono di organizzare e gestire gli hub di notifica.
È necessario avere almeno uno spazio dei nomi dell'hub di notifica.
Inoltre, tutti gli hub di notifica devono avere uno spazio dei nomi assegnato.

Questo cmdlet viene usato principalmente per abilitare e disabilitare uno spazio dei nomi.
Quando uno spazio dei nomi è disabilitato, gli utenti non possono connettersi agli hub di notifica nello spazio dei nomi, né possono usare questi hub per inviare notifiche push.
Per riabilitare uno spazio dei nomi disabilitato, usa questo cmdlet per impostare la proprietà **state** dello spazio dei nomi su Active.

Puoi anche usare questo cmdlet per contrassegnare uno spazio dei nomi come critico.
In questo modo viene impedito l'eliminazione dello spazio dei nomi.
Per rimuovere uno spazio dei nomi critico, devi prima rimuovere il tag critical.

## ESEMPI

### Esempio 1: disabilitare uno spazio dei nomi
```
PS C:\>Set-AzureRmNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Disabled"
```

Questo comando Disabilita lo spazio dei nomi denominato ContosoPartners situato nel Data Center ovest degli Stati Uniti e assegnato al gruppo di risorse ContosoNotificationsGroup.

### Esempio 2: abilitare uno spazio dei nomi
```
PS C:\>Set-AzureRmNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Active"
```

Questo comando consente allo spazio dei nomi denominato ContosoPartners situato nel Data Center ovest degli Stati Uniti e assegnato al gruppo di risorse ContosoNotificationsGroup.

## PARAMETRI

### -Critical
Indica se lo spazio dei nomi è uno spazio dei nomi critico.
Gli spazi dei nomi critici non possono essere eliminati.
Per eliminare uno spazio dei nomi critico, è necessario impostare il valore di questa proprietà su false per contrassegnare lo spazio dei nomi come non critico.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Non chiedere conferma.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Posizione
Specifica il nome visualizzato del centro dati che ospita lo spazio dei nomi.
Anche se è possibile impostare questo parametro su qualsiasi posizione di Azure valida, per ottenere prestazioni ottimali, è consigliabile usare un data center situato vicino alla maggior parte degli utenti.

Per ottenere un elenco aggiornato delle posizioni di Azure, eseguire il comando seguente:

`Get-AzureLocation | Select-Object DisplayName`

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Spazio dei nomi
Specifica lo spazio dei nomi modificato da questo cmdlet.

Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.

```yaml
Type: String
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

I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che semplificano la gestione dell'inventario e l'amministrazione di Azure.

```yaml
Type: String
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
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Stato
Specifica lo stato corrente dello spazio dei nomi.
I valori accettabili per questo parametro sono: Active e disabled.

```yaml
Type: NamespaceState
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Specifica le coppie nome/valore che possono essere usate per categorizzare e organizzare gli elementi Azure.
I tag funzionano in modo simile alle parole chiave e funzionano in una distribuzione.
Ad esempio, se si cercano tutti gli elementi con il reparto Tag: la ricerca restituirà tutti gli elementi di Azure che hanno il tag, indipendentemente da oggetti come il tipo di elemento, la posizione o il gruppo di risorse.

Un singolo tag è costituito da due parti: il *nome* e (facoltativamente) il *valore*.
Ad esempio, nel reparto: il nome del tag è reparto e il valore di tag è.
Per aggiungere un tag, usa la sintassi della tabella hash simile alla seguente, che crea il tag CalendarYear: 2016:

-Tags @ {Name = "CalendarYear"; Value = "2016"}

Per aggiungere più tag nello stesso comando, separare i singoli tag usando le virgole:

-Tag @ {Name = "CalendarYear"; Value = "2016"}, @ {Name = "anno fiscale"; Value = "2017"}

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confermare
Richiede la conferma prima di eseguire il cmdlet.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
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

### Nessuno
Questo cmdlet non accetta alcun input.

## OUTPUT

### Microsoft. Azure. Commands. NotificationHubs. Models. NamespaceAttributes

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureRmNotificationHubsNamespace](./Get-AzureRmNotificationHubsNamespace.md)

[New-AzureRmNotificationHubsNamespace](./New-AzureRmNotificationHubsNamespace.md)

[Remove-AzureRmNotificationHubsNamespace](./Remove-AzureRmNotificationHubsNamespace.md)


