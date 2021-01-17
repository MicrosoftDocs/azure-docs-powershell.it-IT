---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
ms.openlocfilehash: 0303ea7841a187002e4848c74ca656eeea970dbc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346771"
---
# Get-AzEventGridDomainTopic

## Sinossi
Ottiene i dettagli di un argomento relativo al dominio della griglia di eventi oppure ottiene un elenco di tutti gli argomenti relativi al dominio della griglia eventi in un dominio specifico della griglia di eventi nell'abbonamento a Azure corrente.

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

## Descrizione
Il cmdlet Get-AzEventGridDomainTopic ottiene i dettagli di un argomento del dominio della griglia di eventi specificato o un elenco di tutti gli argomenti relativi al dominio della griglia di eventi in un dominio specifico dell'abbonamento a Azure corrente.
Se viene fornito il nome dell'argomento di dominio, vengono restituiti i dettagli di un singolo argomento relativo al dominio della griglia eventi.
Se il nome dell'argomento del dominio non è disponibile, viene restituito un elenco di argomenti del dominio con il nome di dominio specificato. Il numero di elementi restituiti in questo elenco è controllato dal parametro top. Se il valore superiore non è specificato o $null, l'elenco conterrà tutti gli elementi del dominio. In caso contrario, l'inizio indicherà il numero massimo di elementi da restituire nell'elenco.
Se sono ancora disponibili altri argomenti di dominio, il valore in NextLink deve essere usato nella chiamata successiva per ottenere la pagina successiva di argomenti di dominio.
Infine, il parametro ODataQuery viene usato per eseguire filtri per i risultati della ricerca. La query di filtro segue la sintassi OData usando solo la proprietà Name. Le operazioni supportate includono: CONTAINs, EQ (per uguale), ne (per non uguale) e, o e non.

## ESEMPI

### Esempio 1

Ottiene i dettagli dell'argomento relativo al dominio della griglia dell'evento \` DomainTopic1 \` in Domain Grid \` dominio1 \` nel gruppo di risorse \` MyResourceGroupName \` .

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

Ottiene i dettagli dell'argomento relativo al dominio della griglia dell'evento \` DomainTopic1 in \` Domain Grid \` dominio1 \` nel gruppo di risorse \` MyResourceGroupName \` usando l'opzione ResourceId.

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

Elenca tutti gli argomenti relativi al dominio della griglia eventi in Domain Grid \` dominio1 \` nel gruppo di risorse \` MyResourceGroupName \` senza paginazione (tutti i risultati vengono restituiti in un solo colpo).

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

Elenca tutti gli argomenti relativi al dominio della griglia eventi in Domain Grid \` dominio1 \` nel gruppo di risorse \` MyResourceGroupName \` senza paginazione (tutti i risultati vengono restituiti in un solo colpo) usando l'opzione ResourceId

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

Elencare gli argomenti relativi al dominio della griglia degli eventi in Domain \` dominio1 \` nel gruppo di risorse \` MyResourceGroupName \` che soddisfano gli argomenti di $odataFilter query 10 Domain alla volta. Se sono disponibili più risultati, la $result. NextLink non sarà $null. Per ottenere la pagina o le pagine successive degli argomenti di dominio, si prevede che l'utente richiami Get-AzEventGridDomainTopic e usi result. NextLink ottenuto dalla chiamata precedente. Il chiamante deve fermarsi quando viene restituito. NextLink diventa $null.

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

## PARAMETRI

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

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

### -Nome
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
Identificatore delle risorse che rappresenta il dominio dell'evento Grid o Domain Grid.

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

### -Inizio pagina
Query OData utilizzata per filtrare i risultati dell'elenco. Il filtro è attualmente consentito solo nella proprietà Name. Le operazioni supportate includono: CONTAINs, EQ (per uguale), ne (per non uguale) e, o e non.

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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### System. String

### System. Int32

## OUTPUT

### Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic

### Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopicListInstance

## Note

## COLLEGAMENTI CORRELATI
