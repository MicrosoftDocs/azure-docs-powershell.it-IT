---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
ms.openlocfilehash: df3f6673729a868e7aeb349a34fba32b2033862e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194430"
---
# Get-AzEventGridTopic

## SYNOPSIS
Recupera i dettagli di un argomento Griglia eventi o ottiene un elenco di tutti gli argomenti della griglia eventi nella sottoscrizione di Azure corrente.

## SINTASSI

### ResourceGroupNameParameterSet (impostazione predefinita)
```
Get-AzEventGridTopic [[-ResourceGroupName] <String>] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### TopicNameParameterSet
```
Get-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdEventSubscriptionParameterSet
```
Get-AzEventGridTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### NextLinkParameterSet
```
Get-AzEventGridTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet Get-AzEventGridTopic cmdlet ottiene i dettagli di un argomento della griglia eventi specificato o un elenco di tutti gli argomenti della griglia eventi nella sottoscrizione di Azure corrente.
Se si fornisce il nome dell'argomento, vengono restituiti i dettagli di un singolo argomento griglia eventi.
Se non viene fornito il nome dell'argomento, viene restituito un elenco di argomenti. Il numero di elementi restituiti in questo elenco è controllato dal parametro Top. Se non si specificato il valore Primo o $null, l'elenco conterrà tutti gli elementi degli argomenti. In caso contrario, Top indicherà il numero massimo di elementi da restituire nell'elenco.
Se sono ancora disponibili altri argomenti, il valore in NextLink deve essere usato nella prossima chiamata per ottenere la pagina successiva di argomenti.
Infine, il parametro ODataQuery viene usato per filtrare i risultati della ricerca. La query di filtro segue la sintassi OData usando solo la proprietà Name. Le operazioni supportate includono: CONTAINS, eq (per uguale), ne (per diverso da) E, OR e NOT.

## ESEMPI

### Esempio 1
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

Recupera i dettagli dell'argomento Griglia eventi \` Argomento1 \` nel gruppo di risorse \` MyResourceGroupName. \`

### Esempio 2
```powershell
PS C:\> Get-AzEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

Recupera i dettagli dell'argomento Griglia eventi \` Argomento1 \` nel gruppo di risorse \` MyResourceGroupName. \`

### Esempio 3
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName
```

Elencare tutti gli argomenti della griglia eventi nel gruppo di risorse \` MyResourceGroupName \` senza impaginazione.

### Esempio 4
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

Elencare i primi 10 argomenti della griglia degli eventi (se presenti) nel gruppo di risorse MyResourceGroupName che soddisfa la \` \` query $odataFilter risorsa. Se sono disponibili altri risultati, la $result. NextLink non verrà $null. Per visualizzare le pagine o le pagine seguenti di argomenti, è previsto che l'utente chiami di nuovo le Get-AzEventGridTopic e usi il risultato. NextLink ottenuto dalla chiamata precedente. Caller should stop when result. NextLink diventa $null.

### Esempio 5
```powershell
PS C:\> Get-AzEventGridTopic
```

Elencare tutti gli argomenti della griglia eventi nella sottoscrizione senza impaginazione.

### Esempio 6
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

Elencare i primi 10 argomenti della griglia degli eventi (se presenti) nell'abbonamento che soddisfa la query $odataFilter eventi. Se sono disponibili altri risultati, la $result. NextLink non verrà $null. Per visualizzare le pagine o le pagine seguenti di argomenti, è previsto che l'utente chiami di nuovo le Get-AzEventGridTopic e usi il risultato. NextLink ottenuto dalla chiamata precedente. Caller should stop when result. NextLink diventa $null.

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

### -Name
Nome dell'argomento EventGrid.

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
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
Parameter Sets: ResourceGroupNameParameterSet, TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
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
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Identificatore di risorsa che rappresenta l'argomento griglia eventi.

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -In alto
Numero massimo di risorse da ottenere. Il valore valido è compreso tra 1 e 100. Se viene specificato il valore superiore e sono ancora disponibili altri risultati, il risultato conterrà un collegamento alla pagina successiva in cui eseguire la query in NextLink. Se non si specificato il valore Massimo, verrà restituito contemporaneamente l'elenco completo delle risorse.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ResourceGroupNameParameterSet, TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
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

### System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]

## OUTPUT

### Microsoft.Azure.Commands.EventGrid.Models.PSTopic

### Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance

## NOTE

## COLLEGAMENTI CORRELATI
