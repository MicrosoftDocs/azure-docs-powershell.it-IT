---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 1B2AA717-ECD6-4CC0-AB6D-A199AF21A4A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
ms.openlocfilehash: c367c4b4f7ebe7c9d6d51b832eed22249f262864
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191487"
---
# Set-AzNotificationHubsNamespace

## SYNOPSIS
Imposta i valori delle proprietà per uno spazio dei nomi dell'hub di notifica.

## SINTASSI

```
Set-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-State] <NamespaceState>] [[-Critical] <Boolean>] [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Set-AzNotificationHubs Consente di impostare** i valori delle proprietà di uno spazio dei nomi dell'hub di notifica esistente.
Gli spazi dei nomi sono contenitori logici che consentono di organizzare e gestire gli hub di notifica.
È necessario avere almeno uno spazio dei nomi dell'hub di notifica.
Inoltre, tutti gli hub di notifica devono avere uno spazio dei nomi assegnato.
Questo cmdlet viene usato principalmente per abilitare e disabilitare uno spazio dei nomi.
Quando uno spazio dei nomi è disabilitato, gli utenti non possono connettersi a nessuno degli hub di notifica nello spazio dei nomi, né gli amministratori possono usare questi hub per inviare notifiche push.
Per abilitare nuovamente uno spazio dei nomi disabilitato, usare questo cmdlet per impostare la **proprietà Stato** dello spazio dei nomi su Attivo.
È anche possibile usare questo cmdlet per contrassegnare uno spazio dei nomi come critico.
In questo modo si impedisce l'eliminazione dello spazio dei nomi.
Per rimuovere uno spazio dei nomi critico, è necessario rimuovere prima il tag critico.

## ESEMPI

### Esempio 1: Disabilitare uno spazio dei nomi
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Disabled"
```

Questo comando disabilita lo spazio dei nomi denominato ContosoPartners, situato nel data center degli Stati Uniti occidentali, e assegnato al gruppo di risorse ContosoNotificationsGroup.

### Esempio 2: Abilitare uno spazio dei nomi
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Active"
```

Questo comando abilita lo spazio dei nomi denominato ContosoPartners che si trova nel data center Degli Stati Uniti occidentale e assegnato al gruppo di risorse ContosoNotificationsGroup.

## PARAMETERS

### -Critico
Indica se lo spazio dei nomi è uno spazio dei nomi critico.
Gli spazi dei nomi critici non possono essere eliminati.
Per eliminare uno spazio dei nomi critico, è necessario impostare il valore di questa proprietà su False per contrassegnare lo spazio dei nomi come non critico.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
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

### -Force
Non chiedere conferma.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location
Specifica il nome visualizzato del data center che ospita lo spazio dei nomi.
Anche se è possibile impostare questo parametro su qualsiasi posizione di Azure valida, per ottenere prestazioni ottimali è consigliabile usare un data center situato vicino alla maggior parte degli utenti.
Per ottenere un elenco aggiornato delle posizioni di Azure, eseguire il comando seguente: `Get-AzLocation | Select-Object DisplayName`

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
Specifica lo spazio dei nomi modificato da questo cmdlet.
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

### -State
Specifica lo stato corrente dello spazio dei nomi.
I valori accettabili per questo parametro sono: Attivo e Disabilitato.

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState
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
Specifica coppie nome-valore che possono essere usate per categorizzare e organizzare gli elementi di Azure.
I tag funzionano in modo simile alle parole chiave e operano in una distribuzione.
Ad esempio, se si ricercano tutti gli elementi con il tag Department:IT, la ricerca restituirà tutti gli elementi azure che hanno quel tag, indipendentemente dal tipo di elemento, dalla posizione o dal gruppo di risorse.
Un singolo tag è costituito da due parti: *Name e,* facoltativamente, *value.*
Ad esempio, in Department:IT il nome del tag è Department e il valore del tag è IT.
Per aggiungere un tag, usare una sintassi della tabella hash simile alla seguente, che crea il tag CalendarYear:2016: -Tag @{Name="CalendarYear"; Value="2016"} Per aggiungere più tag nello stesso comando, separare i singoli tag con una virgola: -Tag @{Name="CalendarYear"; Value="2016"}, @{Name="FiscalYear"; Value="2017"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
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

### Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState

### System.Boolean

### System.Collections.Hashtable

## OUTPUT

### Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes

## NOTE

## COLLEGAMENTI CORRELATI

[Get-AzNotificationHubsHubsHubs](./Get-AzNotificationHubsNamespace.md)

[New-AzNotificationHubsHubsHubs](./New-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsHubsHubs](./Remove-AzNotificationHubsNamespace.md)


