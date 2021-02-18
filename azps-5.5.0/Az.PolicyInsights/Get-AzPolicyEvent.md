---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicyevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
ms.openlocfilehash: 744618bb2cc12b4d57bfb1ed42267fcbbe7a86ab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193183"
---
# Get-AzPolicyEvent

## SYNOPSIS
Recupera gli eventi di valutazione dei criteri generati quando le risorse vengono create o aggiornate.

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

## DESCRIZIONE
Recupera gli eventi di valutazione dei criteri generati quando le risorse vengono create o aggiornate. È possibile eseguire query sui record di eventi dei criteri in vari ambiti in base all'intervallo di tempo specificato (l'impostazione predefinita è l'ultimo giorno). È possibile filtrare, raggruppare e calcolare le aggregazioni di gruppi dei risultati.

## ESEMPI

### Esempio 1: Ottenere eventi dei criteri nell'ambito della sottoscrizione corrente
```powershell
PS C:\> Get-AzPolicyEvent
```

Recupera i record dell'evento dei criteri generati nell'ultimo giorno per tutte le risorse nella sottoscrizione nel contesto della sessione corrente.

### Esempio 2: Ottenere eventi dei criteri nell'ambito di sottoscrizione specificato
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

Recupera i record dell'evento dei criteri generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione specificata.

### Esempio 3: Ottenere eventi dei criteri nell'ambito del gruppo di gestione
```powershell
PS C:\> Get-AzPolicyEvent -ManagementGroupName "myManagementGroup"
```

Ottiene i record dell'evento dei criteri generati nell'ultimo giorno per tutte le risorse all'interno del gruppo di gestione specificato.

### Esempio 4: Ottenere eventi dei criteri nell'ambito del gruppo di risorse nella sottoscrizione corrente
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup"
```

Ottiene i record dell'evento dei criteri generati nell'ultimo giorno per tutte le risorse all'interno del gruppo di risorse specificato (nella sottoscrizione nel contesto della sessione corrente).

### Esempio 5: Ottenere eventi dei criteri nell'ambito del gruppo di risorse nella sottoscrizione specificata
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

Ottiene i record dell'evento dei criteri generati nell'ultimo giorno per tutte le risorse all'interno del gruppo di risorse specificato (nella sottoscrizione specificata).

### Esempio 6: Ottenere eventi dei criteri per una risorsa
```powershell
PS C:\> Get-AzPolicyEvent -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

Ottiene i record dell'evento dei criteri generati nell'ultimo giorno per la risorsa specificata.

### Esempio 7: Ottenere eventi dei criteri per la definizione di un set di criteri nella sottoscrizione corrente
```powershell
PS C:\> Get-AzPolicyEvent -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Recupera i record dell'evento dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) a cui è stata attivata la definizione del set di criteri specificata (presente nella sottoscrizione nel contesto della sessione corrente).

### Esempio 8: Ottenere eventi dei criteri per la definizione di un set di criteri nella sottoscrizione specificata
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Recupera i record dell'evento dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) a cui è stata attivata la definizione del set di criteri specificata (esistente nella sottoscrizione specificata).

### Esempio 9: Ottenere eventi dei criteri per una definizione di criteri nella sottoscrizione corrente
```powershell
PS C:\> Get-AzPolicyEvent -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Recupera i record dell'evento dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) a cui è stata attivata la definizione dei criteri specificata (presente nella sottoscrizione nel contesto della sessione corrente).

### Esempio 10: Ottenere eventi dei criteri per una definizione di criteri nella sottoscrizione specificata
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Recupera i record dell'evento dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) a cui è stata attivata la definizione dei criteri specificata (esistente nella sottoscrizione specificata).

### Esempio 11: Ottenere eventi dei criteri per un'assegnazione di criteri nella sottoscrizione corrente
```powershell
PS C:\> Get-AzPolicyEvent -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Recupera i record dell'evento dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) applicate dall'assegnazione di criteri specificata (che esiste nella sottoscrizione nel contesto della sessione corrente).

### Esempio 12: Ottenere eventi dei criteri per un'assegnazione di criteri nella sottoscrizione specificata
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Recupera i record di eventi dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) applicate dall'assegnazione di criteri specificata (esistente nella sottoscrizione specificata).

### Esempio 13: Ottenere eventi dei criteri per un'assegnazione di criteri nel gruppo di risorse specificato nella sottoscrizione corrente
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Recupera i record dell'evento dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) applicate dall'assegnazione di criteri specificata (presente nel gruppo di risorse nella sottoscrizione nel contesto della sessione corrente).

### Esempio 14: Ottenere eventi dei criteri nell'ambito della sottoscrizione corrente, con le opzioni di query OrdinaPer, Principali e Seleziona
```powershell
PS C:\> Get-AzPolicyEvent -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId"
```

Recupera i record dell'evento dei criteri generati nell'ultimo giorno per tutte le risorse nella sottoscrizione nel contesto della sessione corrente. Il comando ordina i risultati in base alla data e ora e alle proprietà dei nomi delle assegnazioni dei criteri e accetta solo le prime 5 di quelle elencate in questo ordine.
Seleziona inoltre per elencare solo un sottoinsieme di colonne per ogni record.

### Esempio 15: Ottenere eventi dei criteri nell'ambito della sottoscrizione corrente, con le opzioni della query Da e A
```powershell
PS C:\> Get-AzPolicyEvent -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

Recupera i record di eventi dei criteri generati nell'intervallo di date specificato per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente.

### Esempio 16: Ottenere eventi dei criteri nell'ambito della sottoscrizione corrente, con l'opzione della query di filtro
```powershell
PS C:\> Get-AzPolicyEvent -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

Recupera i record dell'evento dei criteri generati nell'ultimo giorno per tutte le risorse nella sottoscrizione nel contesto della sessione corrente.
Il comando limita i risultati restituiti filtrando in base all'azione di definizione dei criteri (incluse le azioni di negazione o controllo) e alla posizione delle risorse (esclusa la posizione est).

### Esempio 17: Ottenere eventi dei criteri nell'ambito della sottoscrizione corrente, con l'opzione Applica che specifica l'aggregazione del numero di righe
```powershell
PS C:\> Get-AzPolicyEvent -Apply "aggregate(`$count as NumberOfRecords)"
```

Ottiene il numero di record di eventi dei criteri generati nell'ultimo giorno per tutte le risorse nella sottoscrizione nel contesto della sessione corrente.
Il comando restituisce solo il conteggio dei record dell'evento dei criteri, che viene restituito all'interno della proprietà AdditionalProperties.

### Esempio 18: Ottenere eventi dei criteri nell'ambito della sottoscrizione corrente, con Applica che specifica il raggruppamento con l'aggregazione
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, PolicyDefinitionAction, ResourceId), aggregate(`$count as NumEvents))" -OrderBy "NumEvents desc" -Top 5
```

Recupera i record dell'evento dei criteri generati nell'ultimo giorno per tutte le risorse nella sottoscrizione nel contesto della sessione corrente. Il comando limita i risultati restituiti dal filtro in base all'azione di definizione dei criteri (include solo gli eventi di controllo e di negazione).
Raggruppa i risultati in base all'assegnazione dei criteri, alla definizione dei criteri, all'azione di definizione dei criteri e all'ID risorsa e calcola il numero di record in ogni gruppo, che viene restituito all'interno della proprietà AdditionalProperties.
Ordina i risultati in base all'aggregazione conteggio in ordine decrescente e accetta solo i primi 5 di quelli elencati in tale ordine.

### Esempio 19: Ottenere eventi dei criteri nell'ambito della sottoscrizione corrente, con Applica che specifica il raggruppamento senza aggregazione
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((ResourceId))"
```

Recupera i record dell'evento dei criteri generati nell'ultimo giorno per tutte le risorse nella sottoscrizione nel contesto della sessione corrente. Il comando limita i risultati restituiti dal filtro in base all'azione di definizione dei criteri (include solo gli eventi di controllo e di negazione).
Raggruppa i risultati in base all'ID risorsa. L'elenco di tutte le risorse all'interno della sottoscrizione che ha generato un evento dei criteri per almeno un criterio di controllo o di negazione viene generato.

### Esempio 20: Ottenere eventi dei criteri nell'ambito della sottoscrizione corrente, con Applica che specifica più raggruppamenti
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicyDefinitionId), aggregate(`$count as NumDeniedResources))" -OrderBy "NumDeniedResources desc" -Top 5
```

Recupera i record dell'evento dei criteri generati nell'ultimo giorno per tutte le risorse nella sottoscrizione nel contesto della sessione corrente. Il comando limita i risultati restituiti dal filtro in base all'azione di definizione dei criteri (include solo gli eventi di negazione).
Raggruppa prima di tutto i risultati in base all'assegnazione dei criteri, alla definizione dei criteri e all'ID risorsa. Quindi, raggruppa ulteriormente i risultati di questo raggruppamento con le stesse proprietà tranne l'ID risorsa e calcola il numero di record in ognuno di questi gruppi, che viene restituito all'interno della proprietà AdditionalProperties.
Ordina i risultati in base all'aggregazione conteggio in ordine decrescente e accetta solo i primi 5 di quelli elencati in tale ordine.
In questo modo vengono generati i 5 criteri di negazione principali con il maggior numero di risorse negate.

## PARAMETERS

### -Applica
Applicare un'espressione per le aggregazioni usando la notazione OData.

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

### -Filter
Espressione di filtro con notazione OData.

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
Timestamp formattato ISO 8601 che specifica l'ora di inizio dell'intervallo in cui eseguire la query.
Se non è specificato, per impostazione predefinita viene utilizzato il valore del parametro "A" meno 1 giorno.

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
Espressione di ordinamento con notazione OData.
Uno o più nomi di colonna separati da virgola con un valore facoltativo "desc" (impostazione predefinita) o "asc".

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
Nome dell'assegnazione dei criteri.

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
Nome della definizione dei criteri.

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
Nome della definizione del set di criteri.

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

### -Select
Espressione di selezione con notazione OData.
Uno o più nomi di colonna separati da virgola.
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

### -A
Timestamp formattato ISO 8601 che specifica l'ora di fine dell'intervallo in cui eseguire la query.
Se non è specificato, per impostazione predefinita viene visualizzato il momento della richiesta.

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

### -In alto
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
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### System.String

## OUTPUT

### Microsoft.Azure.Commands.PolicyInsights.Models.PolicyEvent

## NOTE

## COLLEGAMENTI CORRELATI
