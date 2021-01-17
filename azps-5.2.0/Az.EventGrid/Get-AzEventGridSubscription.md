---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 587e42ac4c9f318ff46381fdef5b09fa7ce55b63
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329611"
---
# Get-AzEventGridSubscription

## Sinossi
Ottiene i dettagli di un abbonamento a un evento o ottiene un elenco di tutti gli abbonamenti agli eventi nell'abbonamento Azure corrente.

## SINTASSI

### EventSubscriptionTopicNameParameterSet (impostazione predefinita)
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-TopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdEventSubscriptionParameterSet
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceId] <String> [-IncludeFullEndpointUrl]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionDomainNameParameterSet
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-DomainName <String>] [-DomainTopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>]
 [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionTopicTypeNameParameterSet
```
Get-AzEventGridSubscription [-ResourceGroupName <String>] [-TopicTypeName <String>] [-Location <String>]
 [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### EventSubscriptionCustomTopicInputObjectParameterSet
```
Get-AzEventGridSubscription [-InputObject] <PSTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionDomainInputObjectParameterSet
```
Get-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionDomainTopicInputObjectParameterSet
```
Get-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### NextLinkParameterSet
```
Get-AzEventGridSubscription [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet Get-AzEventGridSubscription ottiene i dettagli di un abbonamento alla griglia di eventi specificato o un elenco di tutti gli abbonamenti alla griglia degli eventi nel gruppo di risorse o dell'abbonamento Azure corrente.
Se viene fornito il nome della sottoscrizione dell'evento, vengono restituiti i dettagli di un singolo abbonamento alla griglia di eventi.
Se il nome dell'abbonamento all'evento non è disponibile, viene restituito un elenco di tutte le sottoscrizioni di eventi. Il numero di elementi restituiti in questo elenco è controllato dal parametro top. Se il valore superiore non è specificato o $null, l'elenco conterrà tutti gli elementi dell'abbonamento agli eventi. In caso contrario, l'inizio indicherà il numero massimo di elementi da restituire nell'elenco.
Se altre sottoscrizioni di eventi sono ancora disponibili, il valore in NextLink deve essere usato nella chiamata successiva per ottenere la pagina successiva di abbonamenti a eventi.
Infine, il parametro ODataQuery viene usato per eseguire filtri per i risultati della ricerca. La query di filtro segue la sintassi OData usando solo la proprietà Name. Le operazioni supportate includono: CONTAINs, EQ (per uguale), ne (per non uguale) e, o e non.

## ESEMPI

### Esempio 1
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

Ottiene i dettagli della sottoscrizione dell'evento \` EventSubscription1 \` creata per l'argomento \` Topic1 \` nel gruppo di risorse \` MyResourceGroupName \` .

### Esempio 2
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

Ottiene i dettagli dell'abbonamento \` a EventSubscription1 \` creato per l'argomento \` Topic1 \` nel gruppo di risorse \` MyResourceGroupName \` , incluso l'URL completo dell'endpoint se si tratta di un abbonamento a un evento basato su webhook.

### Esempio 3
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

Ottenere un elenco di tutti gli abbonamenti agli eventi creati per l'argomento \` Topic1 \` nel gruppo di risorse \` MyResourceGroupName \` senza paginazione.

### Esempio 4
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Elencare le prime 10 sottoscrizioni di eventi (se presenti) create per l'argomento \` Topic1 \` nel gruppo di risorse \` MyResourceGroupName \` che soddisfa la query $odataFilter. Se sono disponibili più risultati, la $result. NextLink non sarà $null. Per ottenere la pagina o le pagine successive degli abbonamenti agli eventi, si prevede che l'utente richiami Get-AzEventGridSubscription e usi result. NextLink ottenuto dalla chiamata precedente. Il chiamante deve fermarsi quando viene restituito. NextLink diventa $null.

### Esempio 5
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

Ottiene i dettagli dell'abbonamento \` a EventSubscription1 \` creato per il gruppo di risorse \` MyResourceGroupName \` .

### Esempio 6
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

Ottiene i dettagli della sottoscrizione dell'evento \` EventSubscription1 \` creata per l'abbonamento Azure attualmente selezionato.

### Esempio 7
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

Ottiene l'elenco di tutte le sottoscrizioni di eventi globali create nel gruppo di risorse \` MyResourceGroupName \` senza impaginazione.

### Esempio 8
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Top 5 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Elencare le prime 5 sottoscrizioni di eventi (se presenti) create in MyResourceGroupName gruppo risorse \` \` che soddisfano la query $odataFilter. Se sono disponibili più risultati, la $result. NextLink non sarà $null. Per ottenere la pagina o le pagine successive degli abbonamenti agli eventi, si prevede che l'utente richiami Get-AzEventGridSubscription e usi result. NextLink ottenuto dalla chiamata precedente. Il chiamante deve fermarsi quando viene restituito. NextLink diventa $null.

### Esempio 9
```powershell
PS C:\> Get-AzEventGridSubscription
```

Ottiene l'elenco di tutte le sottoscrizioni di eventi globali create nell'ambito dell'abbonamento Azure attualmente selezionato senza impaginazione.

### Esempio 10
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Elencare le prime 15 sottoscrizioni di eventi globali create sotto l'abbonamento Azure attualmente selezionato che soddisfa la query $odataFilter. Se sono disponibili più risultati, la $result. NextLink non sarà $null. Per ottenere la pagina o le pagine successive degli abbonamenti agli eventi, si prevede che l'utente richiami Get-AzEventGridSubscription e usi result. NextLink ottenuto dalla chiamata precedente. Il chiamante deve fermarsi quando viene restituito. NextLink diventa $null.

### Esempio 11
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

Ottiene l'elenco di tutte le sottoscrizioni di eventi internazionali create in gruppo risorse \` MyResourceGroupName \` nella posizione specificata \` westus2 \` senza impaginazione.

### Esempio 12
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2 -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Elencare le prime 15 sottoscrizioni di eventi regionali create in gruppo risorse \` MyResourceGroupName \` nella posizione specificata \` westus2 \` che soddisfa la query $odataFilter. Se sono disponibili più risultati, la $result. NextLink non sarà $null. Per ottenere la pagina o le pagine successive degli abbonamenti agli eventi, si prevede che l'utente richiami Get-AzEventGridSubscription e usi result. NextLink ottenuto dalla chiamata precedente. Il chiamante deve fermarsi quando viene restituito. NextLink diventa $null.

### Esempio 13
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

Ottiene l'elenco di tutte le sottoscrizioni di eventi create per lo spazio dei nomi EventHub specificato senza impaginazione.

### Esempio 14
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" -Top 25 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Elencare le prime 25 sottoscrizioni di eventi create per lo spazio dei nomi EventHub specificato che soddisfa la query $odataFilter. Se sono disponibili più risultati, la $result. NextLink non sarà $null. Per ottenere la pagina o le pagine successive degli abbonamenti agli eventi, si prevede che l'utente richiami Get-AzEventGridSubscription e usi result. NextLink ottenuto dalla chiamata precedente. Il chiamante deve fermarsi quando viene restituito. NextLink diventa $null.

### Esempio 15
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

Ottiene l'elenco di tutte le sottoscrizioni di eventi create per il tipo di argomento specificato (spazi dei nomi EventHub) nella posizione specificata senza impaginazione.

### Esempio 16
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Elencare le prime 15 sottoscrizioni di eventi (se presenti) create per il tipo di argomento specificato (spazi dei nomi EventHub) nella posizione specificata che soddisfa la query $odataFilter. Se sono disponibili più risultati, la $result. NextLink non sarà $null. Per ottenere la pagina o le pagine successive degli abbonamenti agli eventi, si prevede che l'utente richiami Get-AzEventGridSubscription e usi result. NextLink ottenuto dalla chiamata precedente. Il chiamante deve fermarsi quando viene restituito. NextLink diventa $null.

### Esempio 17
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

Ottiene l'elenco di tutte le sottoscrizioni di eventi create per il gruppo di risorse specifico senza impaginazione.

### Esempio 18
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName -Top 100 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Elencare le prime sottoscrizioni di eventi di 100 (se presenti) create per il gruppo di risorse specifico che soddisfa la query $odataFilter. Se sono disponibili più risultati, la $result. NextLink non sarà $null. Per ottenere la pagina o le pagine successive degli abbonamenti agli eventi, si prevede che l'utente richiami Get-AzEventGridSubscription e usi result. NextLink ottenuto dalla chiamata precedente. Il chiamante deve fermarsi quando viene restituito. NextLink diventa $null.

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

### -DomainInputObject
Oggetto di dominio EventGrid.

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: EventSubscriptionDomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DomainName
Nome di dominio EventGrid.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DomainTopicInputObject
Oggetto argomento del dominio EventGrid.

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic
Parameter Sets: EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DomainTopicName
Nome dell'argomento di dominio EventGrid.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EventSubscriptionName
Nome dell'abbonamento a un evento

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IncludeFullEndpointUrl
Includere l'URL completo dell'endpoint della destinazione dell'abbonamento agli eventi.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
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
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NextLink
Il collegamento per la pagina successiva delle risorse da ottenere. Questo valore viene ottenuto con la prima chiamata di cmdlet Get-AzEventGrid quando sono ancora disponibili altre risorse per la query.

```yaml
Type: System.String
Parameter Sets: NextLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ODataQuery
Query OData utilizzata per filtrare i risultati dell'elenco. Il filtro è attualmente consentito solo nella proprietà Name. Le operazioni supportate includono: CONTAINs, EQ (per uguale), ne (per non uguale) e, o e non.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nome del gruppo di risorse.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: ResourceGroup

Required: False
Position: Named
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

### -Inizio pagina
Query OData utilizzata per filtrare i risultati dell'elenco. Il filtro è attualmente consentito solo nella proprietà Name. Le operazioni supportate includono: CONTAINs, EQ (per uguale), ne (per non uguale) e, o e non.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
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
Position: Named
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
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### System. String

### Microsoft. Azure. Commands. EventGrid. Models. PSTopic

### Microsoft.Azure.Commands.EventGrid.Models.PSDomin

### Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic

### System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]

## OUTPUT

### Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription

## Note

## COLLEGAMENTI CORRELATI
