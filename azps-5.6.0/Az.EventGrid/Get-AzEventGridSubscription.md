---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 665f090f8de059afa4a7f1bd95685e3364a21611
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991365"
---
# Get-AzEventGridSubscription

## SYNOPSIS
Recupera i dettagli di una sottoscrizione di evento o ottiene un elenco di tutte le sottoscrizioni di eventi nella sottoscrizione di Azure corrente.

## SINTASSI

### EventSubscriptionTopicNameParameterSet (Impostazione predefinita)
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

## DESCRIZIONE
Il cmdlet Get-AzEventGridSubscription cmdlet ottiene i dettagli di una sottoscrizione specificata di Griglia eventi oppure un elenco di tutte le sottoscrizioni della griglia eventi nella sottoscrizione o nel gruppo di risorse corrente di Azure.
Se viene fornito il nome della sottoscrizione dell'evento, vengono restituiti i dettagli di una singola sottoscrizione a Griglia eventi.
Se il nome della sottoscrizione dell'evento non è specificato, viene restituito un elenco di tutte le sottoscrizioni di eventi. Il numero di elementi restituiti in questo elenco è controllato dal parametro Top. Se non si specificato il valore Massimo o $null, l'elenco conterrà tutte le voci di sottoscrizione dell'evento. In caso contrario, Top indicherà il numero massimo di elementi da restituire nell'elenco.
Se sono ancora disponibili più abbonamenti a eventi, il valore in NextLink deve essere usato nella prossima chiamata per ottenere la pagina successiva delle sottoscrizioni degli eventi.
Infine, il parametro ODataQuery viene usato per filtrare i risultati della ricerca. La query di filtro segue la sintassi OData usando solo la proprietà Name. Le operazioni supportate includono: CONTAINS, eq (per uguale), ne (per diverso da) E, OR e NOT.

## ESEMPI

### Esempio 1
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

Recupera i dettagli della sottoscrizione evento EventSubscription1 creata per l'argomento 1 nel gruppo \` \` di risorse \` \` \` MyResourceGroupName. \`

### Esempio 2
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

Recupera i dettagli della sottoscrizione dell'evento EventSubscription1 creata per argomento1 nel gruppo di risorse \` \` \` \` MyResourceGroupName, incluso l'URL completo dell'endpoint se si tratta di una sottoscrizione a un evento basata \` \` su Webhook.

### Esempio 3
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

Ottenere un elenco di tutte le sottoscrizioni di eventi create per argomento1 nel gruppo \` \` di risorse \` MyResourceGroupName \` senza impaginazione.

### Esempio 4
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Elencare le prime 10 sottoscrizioni degli eventi , se presenti, create per argomento1 nel gruppo di risorse \` \` MyResourceGroupName che soddisfa la \` \` query $odataFilter risorsa. Se sono disponibili altri risultati, la $result. NextLink non verrà $null. Per ottenere le pagine o le pagine successiva delle sottoscrizioni degli eventi, è previsto che l'utente chiami di nuovo Get-AzEventGridSubscription e usi il risultato. NextLink ottenuto dalla chiamata precedente. Il chiamante deve arrestarsi quando il risultato è stato restituito. NextLink diventa $null.

### Esempio 5
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

Recupera i dettagli della sottoscrizione evento \` EventSubscription1 \` creata per il gruppo di risorse \` MyResourceGroupName. \`

### Esempio 6
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

Recupera i dettagli della sottoscrizione evento \` EventSubscription1 \` creata per la sottoscrizione di Azure attualmente selezionata.

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

Elencare i primi cinque abbonamenti a eventi (se presenti) creati nel gruppo di risorse MyResourceGroupName che soddisfa la \` \` query $odataFilter risorsa. Se sono disponibili altri risultati, la $result. NextLink non verrà $null. Per ottenere le pagine o le pagine successiva delle sottoscrizioni degli eventi, è previsto che l'utente chiami di nuovo il Get-AzEventGridSubscription e usi il risultato. NextLink ottenuto dalla chiamata precedente. Il chiamante deve arrestarsi quando il risultato è stato restituito. NextLink diventa $null.

### Esempio 9
```powershell
PS C:\> Get-AzEventGridSubscription
```

Ottiene l'elenco di tutte le sottoscrizioni di eventi globali create nella sottoscrizione di Azure attualmente selezionata senza impaginazione.

### Esempio 10
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Elencare le prime 15 sottoscrizioni di eventi globali (se presenti) create nella sottoscrizione di Azure attualmente selezionata che soddisfa la query $odataFilter globale. Se sono disponibili altri risultati, la $result. NextLink non verrà $null. Per ottenere le pagine o le pagine successiva delle sottoscrizioni degli eventi, è previsto che l'utente chiami di nuovo Get-AzEventGridSubscription e usi il risultato. NextLink ottenuto dalla chiamata precedente. Il chiamante deve arrestarsi quando il risultato è stato restituito. NextLink diventa $null.

### Esempio 11
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

Ottiene l'elenco di tutte le sottoscrizioni di eventi locali create nel gruppo di risorse MyResourceGroupName nella posizione specificata \` \` \` westus2 \` senza impaginazione.

### Esempio 12
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2 -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Elencare le prime 15 sottoscrizioni di eventi locali (se presenti) create nel gruppo di risorse MyResourceGroupName nel percorso specificato westus2 che soddisfa la \` \` query $odataFilter \` \` risorsa. Se sono disponibili altri risultati, la $result. NextLink non verrà $null. Per ottenere le pagine o le pagine successiva delle sottoscrizioni degli eventi, è previsto che l'utente chiami di nuovo Get-AzEventGridSubscription e usi il risultato. NextLink ottenuto dalla chiamata precedente. Il chiamante deve arrestarsi quando il risultato è stato restituito. NextLink diventa $null.

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

Elencare i primi 25 abbonamenti a eventi , se presenti, creati per lo spazio dei nomi EventHub specificato che soddisfa la query $odataFilter. Se sono disponibili altri risultati, la $result. NextLink non verrà $null. Per ottenere le pagine o le pagine successiva delle sottoscrizioni degli eventi, è previsto che l'utente chiami di nuovo Get-AzEventGridSubscription e usi il risultato. NextLink ottenuto dalla chiamata precedente. Il chiamante deve arrestarsi quando il risultato è stato restituito. NextLink diventa $null.

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

Elencare i primi 15 abbonamenti a eventi, se presenti, creati per il tipo di argomento specificato (spazi dei nomi EventHub) nella posizione specificata che soddisfa la query $odataFilter specificata. Se sono disponibili altri risultati, la $result. NextLink non verrà $null. Per ottenere le pagine o le pagine successiva delle sottoscrizioni degli eventi, è previsto che l'utente chiami di nuovo Get-AzEventGridSubscription e usi il risultato. NextLink ottenuto dalla chiamata precedente. Il chiamante deve arrestarsi quando il risultato è stato restituito. NextLink diventa $null.

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

Elencare i primi 100 abbonamenti a eventi, se presenti, creati per il gruppo di risorse specifico che soddisfa la query $odataFilter risorsa. Se sono disponibili altri risultati, la $result. NextLink non verrà $null. Per ottenere le pagine o le pagine successiva delle sottoscrizioni degli eventi, è previsto che l'utente chiami di nuovo Get-AzEventGridSubscription e usi il risultato. NextLink ottenuto dalla chiamata precedente. Il chiamante deve arrestarsi quando il risultato è stato restituito. NextLink diventa $null.

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

### -DomainInputObject
Oggetto Domain EventGrid.

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
Oggetto Domain Topic di EventGrid.

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
Nome della sottoscrizione dell'evento

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
Includere l'URL completo dell'endpoint della destinazione della sottoscrizione dell'evento.

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
Oggetto EventGrid Topic.

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

### -Location
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
Collegamento alla pagina successiva delle risorse da ottenere. Questo valore viene ottenuto con la prima chiamata Get-AzEventGrid cmdlet quando sono ancora disponibili altre risorse per la query.

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
Query OData usata per filtrare i risultati dell'elenco. L'applicazione di filtri è attualmente consentita solo per la proprietà Nome. Le operazioni supportate includono: CONTAINS, eq (per uguale), ne (per diverso da) E, OR e NOT.

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
Nome gruppo di risorse.

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
Identificatore della risorsa per cui sono state create le sottoscrizioni degli eventi.

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

### -In alto
Query OData usata per filtrare i risultati dell'elenco. L'applicazione di filtri è attualmente consentita solo per la proprietà Name. Le operazioni supportate includono: CONTAINS, eq (per uguale), ne (per diverso da) E, OR e NOT.

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
Nome dell'argomento EventGrid.

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
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### System.String

### Microsoft.Azure.Commands.EventGrid.Models.PSTopic

### Microsoft.Azure.Commands.EventGrid.Models.PSDomain

### Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic

### System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]

## OUTPUT

### Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription

## NOTE

## COLLEGAMENTI CORRELATI
