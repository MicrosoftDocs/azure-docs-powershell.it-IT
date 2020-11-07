---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 2a6d73e14367d2ed8cf0782337a225f3c5dea4ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678838"
---
# Get-AzEventGridSubscription

## Sinossi
Ottiene i dettagli di un abbonamento a un evento o ottiene un elenco di tutti gli abbonamenti agli eventi nell'abbonamento Azure corrente.

## SINTASSI

### EventSubscriptionTopicNameParameterSet (impostazione predefinita)
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [[-ResourceGroupName] <String>]
 [[-TopicName] <String>] [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceIdEventSubscriptionParameterSet
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [-ResourceId] <String>
 [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionTopicTypeNameParameterSet
```
Get-AzEventGridSubscription [[-ResourceGroupName] <String>] [[-TopicTypeName] <String>] [[-Location] <String>]
 [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionCustomTopicInputObjectParameterSet
```
Get-AzEventGridSubscription [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet Get-AzEventGridSubscription ottiene i dettagli di un abbonamento alla griglia di eventi specificato o un elenco di tutti gli abbonamenti alla griglia degli eventi nel gruppo di risorse o dell'abbonamento Azure corrente.
Se viene fornito il nome della sottoscrizione dell'evento, vengono restituiti i dettagli di un singolo abbonamento alla griglia di eventi.
Se il nome dell'abbonamento all'evento non è disponibile, viene restituito un elenco di tutte le sottoscrizioni di eventi.

## ESEMPI

### Esempio 1
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

Ottiene i dettagli della sottoscrizione dell'evento \` EventSubscription1 \` creata per l'argomento \` Topic1 \` nel gruppo di risorse \` MyResourceGroupName \` .

### Esempio 2
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

Ottiene i dettagli dell'abbonamento \` a EventSubscription1 \` creato per l'argomento \` Topic1 \` nel gruppo di risorse \` MyResourceGroupName \` , incluso l'URL completo dell'endpoint se si tratta di un abbonamento a un evento basato su webhook.

### Esempio 3
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

Ottenere un elenco di tutti gli abbonamenti agli eventi creati per l'argomento \` Topic1 \` nel gruppo di risorse \` MyResourceGroupName \` .

### Esempio 4
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

Ottiene i dettagli dell'abbonamento \` a EventSubscription1 \` creato per il gruppo di risorse \` MyResourceGroupName \` .

### Esempio 5
```
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

Ottiene i dettagli della sottoscrizione dell'evento \` EventSubscription1 \` creata per l'abbonamento Azure attualmente selezionato.

### Esempio 6
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

Ottiene l'elenco di tutte le sottoscrizioni di eventi globali create nel gruppo di risorse \` MyResourceGroupName \` .

### Esempio 7
```
PS C:\> Get-AzEventGridSubscription
```

Ottiene l'elenco di tutte le sottoscrizioni di eventi globali create sotto l'abbonamento Azure attualmente selezionato.

### Esempio 8
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

Ottiene l'elenco di tutte le sottoscrizioni di eventi internazionali create in gruppo risorse \` MyResourceGroupName \` nella posizione specificata \` westus2 \` .

### Esempio 9
```
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

Ottiene l'elenco di tutte le sottoscrizioni di eventi create per lo spazio dei nomi EventHub specificato.

### Esempio 10
```
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

Ottiene l'elenco di tutte le sottoscrizioni di eventi create per il tipo di argomento specificato (spazi dei nomi EventHub) nella posizione specificata.

### Esempio 11
```
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

Ottiene l'elenco di tutte le sottoscrizioni di eventi create per il gruppo di risorse specifico.

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

### -EventSubscriptionName
Nome dell'abbonamento a un evento

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IncludeFullEndpointUrl
Includere l'URL completo dell'endpoint della destinazione dell'abbonamento agli eventi.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Oggetto argomento EventGrid.

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Posizione
Posizione

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nome del gruppo di risorse.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Identificatore della risorsa a cui sono stati creati gli abbonamenti agli eventi.

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TopicName
Nome argomento EventGrid.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TopicTypeName
Nome TopicType

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### System. String

### Microsoft. Azure. Commands. EventGrid. Models. PSTopic

## OUTPUT

### Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription

## Note

## COLLEGAMENTI CORRELATI
