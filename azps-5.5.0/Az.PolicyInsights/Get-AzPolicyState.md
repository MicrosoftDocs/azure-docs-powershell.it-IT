---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
ms.openlocfilehash: 04600529ded8b95da578d59f0b2f46cd396594ba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206274"
---
# Get-AzPolicyState

## SYNOPSIS
Ottiene gli stati di conformità dei criteri per le risorse.

## SINTASSI

### SubscriptionScope (impostazione predefinita)
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ManagementGroupScope
```
Get-AzPolicyState [-All] -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupScope
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceScope
```
Get-AzPolicyState [-All] -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-Expand <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PolicySetDefinitionScope
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PolicyDefinitionScope
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SubscriptionLevelPolicyAssignmentScope
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupLevelPolicyAssignmentScope
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Ottiene gli stati di conformità dei criteri per le risorse. È possibile eseguire query sui record dello stato dei criteri in vari ambiti. In base all'intervallo di tempo specificato (per impostazione predefinita, ultimo giorno), è possibile eseguire una query su tutti gli stati dei criteri o su tutte le transizioni dello stato dei criteri. È possibile filtrare, raggruppare e calcolare le aggregazioni di gruppi dei risultati.

## ESEMPI

### Esempio 1: Ottenere gli stati dei criteri più recenti nell'ambito della sottoscrizione corrente
```powershell
PS C:\> Get-AzPolicyState
```

Recupera i record di stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse nella sottoscrizione nel contesto della sessione corrente.

### Esempio 2: Ottenere gli stati dei criteri più recenti nell'ambito di sottoscrizione specificato
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

Recupera i record di stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse nella sottoscrizione specificata.

### Esempio 3: Ottenere tutti gli stati dei criteri nell'ambito di sottoscrizione corrente
```powershell
PS C:\> Get-AzPolicyState -All
```

Recupera tutti i record dello stato dei criteri cronologici (incluso l'ultimo) generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente.

### Esempio 4: Ottenere gli stati dei criteri più recenti nell'ambito del gruppo di gestione
```powershell
PS C:\> Get-AzPolicyState -ManagementGroupName "myManagementGroup"
```

Recupera i record di stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse all'interno del gruppo di gestione specificato.

### Esempio 5: Ottenere gli stati dei criteri più recenti nell'ambito del gruppo di risorse nella sottoscrizione corrente
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup"
```

Recupera i record di stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse all'interno del gruppo di risorse specificato (nella sottoscrizione nel contesto della sessione corrente).

### Esempio 6: Ottenere gli stati dei criteri più recenti nell'ambito del gruppo di risorse nella sottoscrizione specificata
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

Recupera i record di stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse all'interno del gruppo di risorse specificato (nella sottoscrizione specificata).

### Esempio 7: Ottenere gli stati dei criteri più recenti per una risorsa
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

Recupera i record di stato dei criteri più recenti generati nell'ultimo giorno per la risorsa specificata.

### Esempio 8: Ottenere gli stati dei criteri più recenti per la definizione di un set di criteri nella sottoscrizione corrente
```powershell
PS C:\> Get-AzPolicyState -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Recupera i record dello stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) eati dalla definizione del set di criteri specificata (presente nella sottoscrizione nel contesto della sessione corrente).

### Esempio 9: Ottenere gli stati dei criteri più recenti per la definizione di un set di criteri nella sottoscrizione specificata
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Recupera i record di stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) a cui è stata attivata la definizione del set di criteri specificata (esistente nella sottoscrizione specificata).

### Esempio 10: Ottenere gli stati dei criteri più recenti per una definizione di criteri nella sottoscrizione corrente
```powershell
PS C:\> Get-AzPolicyState -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Recupera i record di stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) a cui è stata attivata la definizione dei criteri specificata (presente nella sottoscrizione nel contesto della sessione corrente).

### Esempio 11: Ottenere gli stati dei criteri più recenti per una definizione di criteri nella sottoscrizione specificata
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Recupera i record di stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) a cui è stata attivata la definizione dei criteri specificata (esistente nella sottoscrizione specificata).

### Esempio 12: Ottenere gli stati dei criteri più recenti per un'assegnazione di criteri nell'abbonamento corrente
```powershell
PS C:\> Get-AzPolicyState -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Recupera i record dello stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) a cui è stata attivata l'assegnazione di criteri specificata (che esiste nella sottoscrizione nel contesto della sessione corrente).

### Esempio 13: Ottenere gli stati dei criteri più recenti per un'assegnazione di criteri nella sottoscrizione specificata
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Recupera i record di stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) a cui è stata attivata l'assegnazione di criteri specificata (esistente nella sottoscrizione specificata).

### Esempio 14: Ottenere gli stati dei criteri più recenti per un'assegnazione di criteri nel gruppo di risorse specificato nella sottoscrizione corrente
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Recupera i record di stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) esequisiti dall'assegnazione di criteri specificata (che esiste nel gruppo di risorse nella sottoscrizione nel contesto della sessione corrente).

### Esempio 15: Ottenere gli stati dei criteri più recenti nell'ambito della sottoscrizione corrente, con le opzioni di query OrdinaPer, Principali e Seleziona
```powershell
PS C:\> Get-AzPolicyState -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId, IsCompliant"
```

Recupera i record di stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse nella sottoscrizione nel contesto della sessione corrente. Il comando ordina i risultati in base alla data e ora e alle proprietà dei nomi delle assegnazioni dei criteri e accetta solo le prime 5 di quelle elencate in questo ordine.
Seleziona inoltre per elencare solo un sottoinsieme di colonne per ogni record.

### Esempio 16: Ottenere gli stati dei criteri più recenti nell'ambito della sottoscrizione corrente, con le opzioni della query Da e A
```powershell
PS C:\> Get-AzPolicyState -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

Recupera i record di stato dei criteri più recenti generati nell'intervallo di date specificato per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente.

### Esempio 17: Ottenere gli stati dei criteri più recenti nell'ambito della sottoscrizione corrente, con l'opzione della query di filtro
```powershell
PS C:\> Get-AzPolicyState -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ComplianceState eq 'NonCompliant' and ResourceLocation ne 'eastus'"
```

Recupera i record di stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse nella sottoscrizione nel contesto della sessione corrente.
Il comando limita i risultati restituiti filtrando in base all'azione di definizione dei criteri (incluse le azioni di negazione o controllo), lo stato di conformità (include solo lo stato non conforme) e la posizione delle risorse (esclusa la posizione estus).

### Esempio 18: Ottenere gli stati dei criteri più recenti nell'ambito della sottoscrizione corrente, con l'opzione Applica che specifica l'aggregazione del numero di righe
```powershell
PS C:\> Get-AzPolicyState -Apply "aggregate(`$count as NumberOfRecords)"
```

Ottiene il numero di record di stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente.
Il comando restituisce solo il conteggio dei record dello stato dei criteri, che viene restituito all'interno della proprietà AdditionalProperties.

### Esempio 19: Ottenere gli stati dei criteri più recenti nell'ambito della sottoscrizione corrente, con Applica il raggruppamento specificato con aggregazione
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumStates))" -OrderBy "NumStates desc" -Top 5
```

Recupera i record di stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse nella sottoscrizione nel contesto della sessione corrente. Il comando limita i risultati restituiti filtrando in base allo stato di conformità (include solo lo stato non conforme).
Raggruppa i risultati in base all'assegnazione dei criteri, alla definizione del set di criteri e alla definizione dei criteri e calcola il numero di record in ogni gruppo, restituito all'interno della proprietà AdditionalProperties.
Ordina i risultati in base all'aggregazione conteggio in ordine decrescente e accetta solo i primi 5 di quelli elencati in tale ordine.

### Esempio 20: Ottenere gli stati dei criteri più recenti nell'ambito della sottoscrizione corrente, con Applica che specifica il raggruppamento senza aggregazione
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((ResourceId))"
```

Recupera i record di stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse nella sottoscrizione nel contesto della sessione corrente. Il comando limita i risultati restituiti filtrando in base allo stato di conformità (include solo lo stato non conforme).
Raggruppa i risultati in base all'ID risorsa. In questo modo viene generato l'elenco di tutte le risorse all'interno della sottoscrizione non conformi ad almeno un criterio.

### Esempio 21: Ottenere gli stati dei criteri più recenti nell'ambito della sottoscrizione corrente, con Applica che specifica più raggruppamenti
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumNonCompliantResources))" -OrderBy "NumNonCompliantResources desc" -Top 5
```

### Esempio 22: Ottenere gli stati dei criteri più recenti, inclusi i dettagli di valutazione dei criteri per una risorsa
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1" -Expand "PolicyEvaluationDetails"
```

Recupera i record di stato dei criteri più recenti generati nell'ultimo giorno per tutte le risorse nella sottoscrizione nel contesto della sessione corrente. Il comando limita i risultati restituiti filtrando in base allo stato di conformità (include solo lo stato non conforme).
Raggruppa prima i risultati in base all'assegnazione dei criteri, alla definizione del set di criteri, alla definizione del criterio e all'ID risorsa. Quindi, raggruppa ulteriormente i risultati di questo raggruppamento con le stesse proprietà tranne l'ID risorsa e calcola il numero di record in ognuno di questi gruppi, che viene restituito all'interno della proprietà AdditionalProperties.
Ordina i risultati in base all'aggregazione conteggio in ordine decrescente e accetta solo i primi 5 di quelli elencati in tale ordine.
In questo modo i 5 criteri principali vengono generati con il maggior numero di risorse non conformi.

## PARAMETERS

### -All
All'interno dell'intervallo di tempo specificato, ottenere tutti gli stati dei criteri anziché solo l'ultimo.

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

### -Expand
Espandere l'espressione usando la notazione OData.

```yaml
Type: System.String
Parameter Sets: ResourceScope
Aliases:

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

### Microsoft.Azure.Commands.PolicyInsights.Models.PolicyState

## NOTE

## COLLEGAMENTI CORRELATI

[Get-AzPolicyStateSummary](./Get-AzPolicyStateSummary.md)
