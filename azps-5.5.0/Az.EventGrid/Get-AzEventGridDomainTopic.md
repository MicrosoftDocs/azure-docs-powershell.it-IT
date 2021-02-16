---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
ms.openlocfilehash: 0303ea7841a187002e4848c74ca656eeea970dbc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209594"
---
# Get-AzEventGridDomainTopic

## SYNOPSIS
Recupera i dettagli di un argomento relativo al dominio della griglia eventi o ottiene un elenco di tutti gli argomenti di dominio della griglia eventi nello specifico dominio griglia eventi nella sottoscrizione di Azure corrente.

## SINTASSI

### DomainTopicNameParameterSet (impostazione predefinita)
```
Get-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name <String>]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdDomainTopicParameterSet
```
Get-AzEventGridDomainTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### NextLinkParameterSet
```
Get-AzEventGridDomainTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet Get-AzEventGridDomainTopic ottiene i dettagli di un argomento di dominio della griglia eventi specificato oppure un elenco di tutti gli argomenti di dominio della griglia eventi per un dominio specifico nella sottoscrizione corrente di Azure.
Se si fornisce il nome dell'argomento dominio, vengono restituiti i dettagli di un singolo argomento Dominio griglia eventi.
Se il nome dell'argomento di dominio non è fornito, viene restituito un elenco di argomenti di dominio sotto il nome di dominio specificato. Il numero di elementi restituiti in questo elenco è controllato dal parametro Top. Se non si specificato il valore Massimo o $null, l'elenco conterrà tutti gli elementi degli argomenti di dominio. In caso contrario, Top indicherà il numero massimo di elementi da restituire nell'elenco.
Se sono ancora disponibili altri argomenti sul dominio, il valore in NextLink deve essere usato nella prossima chiamata per ottenere la pagina successiva di argomenti sul dominio.
Infine, il parametro ODataQuery viene usato per filtrare i risultati della ricerca. La query di filtro segue la sintassi OData usando solo la proprietà Name. Le operazioni supportate includono: CONTAINS, eq (per uguale), ne (per diverso da) E, OR e NOT.

## ESEMPI

### Esempio 1

Recupera i dettagli dell'argomento dominio Griglia eventi DomainTopic1 in Domain1 della griglia eventi nel gruppo di \` \` risorse \` \` \` MyResourceGroupName. \`

```powershell
PS C:\> Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1 -DomainTopicName DomainTopic1

ResourceGroupName : MyResourceGroupName
DomainName        : DomainTopic1
DomainTopicName   : Topic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### Esempio 2

Recupera i dettagli dell'argomento dominio Griglia eventi DomainTopic1 in Domain1 della griglia eventi nel gruppo di risorse \` \` \` MyResourceGroupName usando \` \` l'opzione \` ResourceId.

```powershell
PS C:\> Get-AzEventGridDomainTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1"

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### Esempio 3

Elencare tutti gli argomenti di dominio della griglia eventi in Domain1 della griglia eventi nel gruppo di risorse MyResourceGroupName senza impaginazione (tutti i risultati vengono restituiti \` \` in \` \` un'unica schermata).

```powershell
PS C:\> $result=Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1
PS C:\> echo $result.PsDomainTopicsList


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic2
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic2
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic3
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic3
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### Esempio 4

Elencare tutti gli argomenti sui domini della griglia eventi in Dominio griglia eventi1 nel gruppo di risorse \` \` MyResourceGroupName senza impaginazione (tutti i risultati vengono restituiti in un'unica schermata) usando l'opzione \` \` ResourceId

```powershell
PS C:\> $result=Get-AzEventGridDomainTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1"
PS C:\> echo $result.PsDomainTopicsList


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic2
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic2
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic3
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic3
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### Esempio 5

Elencare gli eventuali argomenti sui domini della griglia eventi in Dominio1 nel gruppo di risorse MyResourceGroupName che soddisfano gli argomenti di dominio \` \` della query $odataFilter \` \` 10 per volta. Se sono disponibili altri risultati, la $result. NextLink non verrà $null. Per ottenere le pagine seguenti di argomenti sul dominio, è previsto che l'utente chiami di nuovo il Get-AzEventGridDomainTopic e usi il risultato. NextLink ottenuto dalla chiamata precedente. Il chiamante deve arrestarsi quando il risultato è stato restituito. NextLink diventa $null.

```powershell
PS C:\> $total = 0
PS C:\> $odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1 -Top 10 -ODataQuery $odataFilter
PS C:\> $total += $result.Count
PS C:\> while ($result.NextLink -ne $Null)
    {
        $result = Get-AzEventGridDomainTopic -NextLink $result.NextLink
        $total += $result.Count
    }

PS C:\> echo "Total number of domain topics is $Total"
```

## PARAMETERS

### -DefaultProfile
Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.

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

### -DomainName
Nome di dominio EventGrid.

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: Domain

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Nome dell'argomento di dominio EventGrid.

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: DomainTopicName

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
Parameter Sets: DomainTopicNameParameterSet, ResourceIdDomainTopicParameterSet
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
Parameter Sets: DomainTopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Identificatore di risorsa che rappresenta l'argomento Dominio griglia eventi o Dominio griglia.

```yaml
Type: System.String
Parameter Sets: ResourceIdDomainTopicParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -In alto
Query OData usata per filtrare i risultati dell'elenco. L'applicazione di filtri è attualmente consentita solo per la proprietà Nome. Le operazioni supportate includono: CONTAINS, eq (per uguale), ne (per diverso da) E, OR e NOT.

```yaml
Type: System.Int32
Parameter Sets: DomainTopicNameParameterSet, ResourceIdDomainTopicParameterSet
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

### System.Int32

## OUTPUT

### Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic

### Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopicListInstance

## NOTE

## COLLEGAMENTI CORRELATI
