---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicyevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
ms.openlocfilehash: 744618bb2cc12b4d57bfb1ed42267fcbbe7a86ab
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347380"
---
# Get-AzPolicyEvent

## Sinossi
Ottiene gli eventi di valutazione dei criteri generati come risorse create o aggiornate.

## SINTASSI

### SubscriptionScope (impostazione predefinita)
```
Get-AzPolicyEvent [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ManagementGroupScope
```
Get-AzPolicyEvent -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupScope
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PolicySetDefinitionScope
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PolicyDefinitionScope
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SubscriptionLevelPolicyAssignmentScope
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupLevelPolicyAssignmentScope
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceScope
```
Get-AzPolicyEvent -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>]
 [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrizione
Ottiene gli eventi di valutazione dei criteri generati come risorse create o aggiornate. I record di eventi dei criteri possono essere interrogati in diversi ambiti in base all'intervallo di tempo specificato (impostazione predefinita per l'ultimo giorno). I risultati possono essere filtrati, raggruppati e le aggregazioni di gruppo possono essere calcolate.

## ESEMPI

### Esempio 1: ottenere gli eventi dei criteri nell'ambito corrente della sottoscrizione
```powershell
PS C:\> Get-AzPolicyEvent
```

Ottiene i record di eventi dei criteri generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente.

### Esempio 2: ottenere gli eventi dei criteri nell'ambito dell'abbonamento specificato
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

Ottiene i record di eventi dei criteri generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione specificata.

### Esempio 3: ottenere gli eventi dei criteri nell'ambito del gruppo di gestione
```powershell
PS C:\> Get-AzPolicyEvent -ManagementGroupName "myManagementGroup"
```

Ottiene i record di eventi dei criteri generati nell'ultimo giorno per tutte le risorse all'interno del gruppo di gestione specificato.

### Esempio 4: ottenere gli eventi dei criteri nell'ambito di un gruppo di risorse nell'abbonamento corrente
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup"
```

Ottiene i record di eventi dei criteri generati nell'ultimo giorno per tutte le risorse all'interno del gruppo di risorse specificato (nell'abbonamento nel contesto della sessione corrente).

### Esempio 5: ottenere gli eventi dei criteri nell'ambito di un gruppo di risorse nell'abbonamento specificato
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

Ottiene i record di eventi dei criteri generati nell'ultimo giorno per tutte le risorse all'interno del gruppo di risorse specificato (nell'abbonamento specificato).

### Esempio 6: ottenere gli eventi dei criteri per una risorsa
```powershell
PS C:\> Get-AzPolicyEvent -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

Ottiene i record di eventi dei criteri generati nell'ultimo giorno per la risorsa specificata.

### Esempio 7: ottenere gli eventi dei criteri per una definizione di set di criteri nell'abbonamento corrente
```powershell
PS C:\> Get-AzPolicyEvent -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ottiene i record di eventi dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) effettuate dalla definizione del set di criteri specificata (che esiste nell'abbonamento nel contesto della sessione corrente).

### Esempio 8: ottenere gli eventi dei criteri per una definizione di set di criteri nell'abbonamento specificato
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ottiene i record di eventi dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) effettuate dalla definizione del set di criteri specificata (che esiste nell'abbonamento specificato).

### Esempio 9: ottenere gli eventi dei criteri per una definizione di criterio nell'abbonamento corrente
```powershell
PS C:\> Get-AzPolicyEvent -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ottiene i record di eventi dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) effettuate dalla definizione di criteri specificata (che esiste nell'abbonamento nel contesto della sessione corrente).

### Esempio 10: ottenere gli eventi dei criteri per una definizione di criterio nell'abbonamento specificato
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ottiene i record di eventi dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) effettuate dalla definizione di criteri specificata (che esiste nell'abbonamento specificato).

### Esempio 11: ottenere gli eventi dei criteri per un'assegnazione di criteri nell'abbonamento corrente
```powershell
PS C:\> Get-AzPolicyEvent -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Ottiene i record di eventi dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) effettuate dall'assegnazione di criteri specificata (che esiste nell'abbonamento nel contesto della sessione corrente).

### Esempio 12: ottenere gli eventi dei criteri per un'assegnazione di criteri nell'abbonamento specificato
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Ottiene i record di eventi dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) effettuate dall'assegnazione di criteri specificata (che esiste nell'abbonamento specificato).

### Esempio 13: ottenere gli eventi dei criteri per un'assegnazione di criteri nel gruppo di risorse specificato nell'abbonamento corrente
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Ottiene i record di eventi dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) effettuate dall'assegnazione di criteri specificata (esistente nel gruppo risorse della sottoscrizione nel contesto della sessione corrente).

### Esempio 14: ottenere gli eventi dei criteri nell'ambito corrente della sottoscrizione, con le opzioni OrderBy, inizio e seleziona query
```powershell
PS C:\> Get-AzPolicyEvent -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId"
```

Ottiene i record di eventi dei criteri generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente. Il comando Ordina i risultati in base al timestamp e alle proprietà dei nomi delle assegnazioni di criteri e accetta solo i primi 5 di quelli elencati in quell'ordine.
Viene inoltre selezionato per elencare solo un sottoinsieme delle colonne per ogni record.

### Esempio 15: ottenere eventi di criteri nell'ambito dell'abbonamento corrente, con le opzioni da e a query
```powershell
PS C:\> Get-AzPolicyEvent -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

Ottiene i record di eventi dei criteri generati nell'intervallo di date specificato per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente.

### Esempio 16: ottenere eventi di criteri nell'ambito dell'abbonamento corrente, con l'opzione di query di filtro
```powershell
PS C:\> Get-AzPolicyEvent -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

Ottiene i record di eventi dei criteri generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente.
Il comando limita i risultati restituiti dal filtro in base all'azione di definizione dei criteri (include le azioni Deny o audit) e la posizione delle risorse (esclude la posizione eastus).

### Esempio 17: ottenere gli eventi dei criteri nell'ambito corrente della sottoscrizione, con l'applicazione specifica dell'aggregazione del conteggio righe
```powershell
PS C:\> Get-AzPolicyEvent -Apply "aggregate(`$count as NumberOfRecords)"
```

Ottiene il numero di record di eventi dei criteri generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente.
Il comando restituisce solo il conteggio dei record di eventi del criterio, che viene restituito all'interno della proprietà AdditionalProperties.

### Esempio 18: ottenere eventi di criteri nell'ambito dell'abbonamento corrente, con applica specificando il raggruppamento con l'aggregazione
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, PolicyDefinitionAction, ResourceId), aggregate(`$count as NumEvents))" -OrderBy "NumEvents desc" -Top 5
```

Ottiene i record di eventi dei criteri generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente. Il comando limita i risultati restituiti dal filtro in base all'azione di definizione dei criteri (include solo gli eventi audit e Deny).
Raggruppa i risultati in base all'assegnazione dei criteri, alla definizione di criteri, all'azione di definizione dei criteri e all'ID delle risorse e calcola il numero di record in ogni gruppo, che viene restituito all'interno della proprietà AdditionalProperties.
Ordina i risultati per l'aggregazione del conteggio in ordine decrescente e accetta solo i primi 5 di quelli elencati in quell'ordine.

### Esempio 19: ottenere eventi di criteri nell'ambito dell'abbonamento corrente, con applica specifica del raggruppamento senza aggregazione
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((ResourceId))"
```

Ottiene i record di eventi dei criteri generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente. Il comando limita i risultati restituiti dal filtro in base all'azione di definizione dei criteri (include solo gli eventi audit e Deny).
Raggruppa i risultati in base all'ID risorsa. In questo modo viene generato l'elenco di tutte le risorse dell'abbonamento che hanno generato un evento Policy per almeno un criterio di controllo o di negazione.

### Esempio 20: ottenere eventi di criteri nell'ambito corrente della sottoscrizione, con applica specificando più raggruppamenti
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicyDefinitionId), aggregate(`$count as NumDeniedResources))" -OrderBy "NumDeniedResources desc" -Top 5
```

Ottiene i record di eventi dei criteri generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente. Il comando limita i risultati restituiti dal filtro in base all'azione di definizione dei criteri (include solo gli eventi Deny).
Raggruppa i risultati per primi in base all'assegnazione dei criteri, alla definizione di criteri e all'ID risorsa. Viene quindi ulteriormente raggruppati i risultati di questo raggruppamento con le stesse proprietà eccetto l'ID risorsa e viene calcolato il numero di record in ognuno di questi gruppi, che viene restituito all'interno della proprietà AdditionalProperties.
Ordina i risultati per l'aggregazione del conteggio in ordine decrescente e accetta solo i primi 5 di quelli elencati in quell'ordine.
In questo articolo vengono generati i primi 5 criteri di negazione con il numero maggiore di risorse negate.

## PARAMETRI

### -Applica
Applicare l'espressione per le aggregazioni usando la notazione OData.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -Filtro
Filtrare l'espressione usando la notazione OData.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Da
Timestamp formattato ISO 8601 che specifica l'ora di inizio dell'intervallo di query.
Se non viene specificato, il valore predefinito è "a" meno 1 giorno.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagementGroupName
Nome del gruppo di gestione.

```yaml
Type: System.String
Parameter Sets: ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OrderBy
Espressione di ordinamento tramite notazione OData.
Uno o più nomi di colonna delimitati da virgole con un "DESC" facoltativo (impostazione predefinita) o "ASC".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PolicyAssignmentName
Nome assegnazione criteri.

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelPolicyAssignmentScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicyDefinitionName
Nome definizione criterio.

```yaml
Type: System.String
Parameter Sets: PolicyDefinitionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicySetDefinitionName
Nome definizione set di criteri.

```yaml
Type: System.String
Parameter Sets: PolicySetDefinitionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nome del gruppo di risorse.

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
ID risorsa.

```yaml
Type: System.String
Parameter Sets: ResourceScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Selezionare
Selezionare espressione usando la notazione OData.
Uno o più nomi di colonna delimitati da virgole.
Limita le colonne di ogni record solo a quelle richieste.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
ID abbonamento.

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, ResourceGroupScope, PolicySetDefinitionScope, PolicyDefinitionScope, SubscriptionLevelPolicyAssignmentScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -To
Timestamp formattato ISO 8601 che specifica l'ora di fine dell'intervallo di query.
Se non viene specificato, il valore predefinito è l'ora della richiesta.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Inizio pagina
Numero massimo di record da restituire.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### System. String

## OUTPUT

### Microsoft. Azure. Commands. PolicyInsights. Models. PolicyEvent

## Note

## COLLEGAMENTI CORRELATI
