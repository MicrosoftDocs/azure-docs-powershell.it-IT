---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/get-azpolicystatesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
ms.openlocfilehash: 09fce075ae0f6d8c55f5ef18d070a72daafa2cac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989084"
---
# Get-AzPolicyStateSummary

## SYNOPSIS
Recupera il riepilogo più recente degli stati di conformità dei criteri per le risorse.

## SINTASSI

### SubscriptionScope (impostazione predefinita)
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ManagementGroupScope
```
Get-AzPolicyStateSummary -ManagementGroupName <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupScope
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### PolicySetDefinitionScope
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### PolicyDefinitionScope
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### SubscriptionLevelPolicyAssignmentScope
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceGroupLevelPolicyAssignmentScope
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceScope
```
Get-AzPolicyStateSummary -ResourceId <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Ottiene una visualizzazione di riepilogo dei numeri più recenti dello stato di conformità dei criteri in vari ambiti, suddivisi in assegnazioni di criteri e definizioni dei criteri. Include solo stati dei criteri non conformi.

## ESEMPI

### Esempio 1: Ottenere un riepilogo degli stati dei criteri non conformi più recenti nell'ambito della sottoscrizione corrente
```powershell
PS C:\> Get-AzPolicyStateSummary
```

Ottiene la visualizzazione di riepilogo degli stati di conformità dei criteri più recenti generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente.

### Esempio 2: Ottenere un riepilogo degli stati dei criteri non conformi più recenti nell'ambito di sottoscrizione specificato
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

Ottiene la visualizzazione di riepilogo degli stati di conformità dei criteri più recenti generati nell'ultimo giorno per tutte le risorse nella sottoscrizione specificata.

### Esempio 3: Ottenere un riepilogo degli stati dei criteri non conformi più recenti nell'ambito del gruppo di gestione
```powershell
PS C:\> Get-AzPolicyStateSummary -ManagementGroupName "myManagementGroup"
```

Ottiene la visualizzazione di riepilogo degli stati di conformità dei criteri più recenti generati nell'ultimo giorno per tutte le risorse all'interno del gruppo di gestione specificato.

### Esempio 4: Ottenere un riepilogo degli stati dei criteri non conformi più recenti nell'ambito del gruppo di risorse nella sottoscrizione corrente
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup"
```

Ottiene la visualizzazione di riepilogo degli stati di conformità dei criteri più recenti generati nell'ultimo giorno per tutte le risorse all'interno del gruppo di risorse specificato (nella sottoscrizione nel contesto della sessione corrente).

### Esempio 5: Ottenere un riepilogo degli stati dei criteri non conformi più recenti nell'ambito del gruppo di risorse nella sottoscrizione specificata
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

Ottiene la visualizzazione di riepilogo degli stati di conformità dei criteri più recenti generati nell'ultimo giorno per tutte le risorse all'interno del gruppo di risorse specificato (nella sottoscrizione specificata).

### Esempio 6: Ottenere il riepilogo più recente degli stati dei criteri non conformi per una risorsa
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

Ottiene la visualizzazione di riepilogo degli stati di conformità dei criteri più recenti generati nell'ultimo giorno per la risorsa specificata.

### Esempio 7: Ottenere il riepilogo più recente degli stati dei criteri non conformi per la definizione di un set di criteri nella sottoscrizione corrente
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ottiene la visualizzazione di riepilogo degli stati di conformità dei criteri più recenti generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) applicate dalla definizione del set di criteri specificata (che esiste nella sottoscrizione nel contesto della sessione corrente).

### Esempio 8: Ottenere il riepilogo più recente degli stati dei criteri non conformi per la definizione di un set di criteri nella sottoscrizione specificata
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ottiene la visualizzazione di riepilogo degli stati di conformità dei criteri più recenti generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) applicate dalla definizione del set di criteri specificata (esistente nella sottoscrizione specificata).

### Esempio 9: Ottenere il riepilogo più recente degli stati dei criteri non conformi per la definizione di un criterio nella sottoscrizione corrente
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ottiene la visualizzazione di riepilogo degli stati di conformità dei criteri più recenti generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) applicate dalla definizione dei criteri specificata (che esiste nella sottoscrizione nel contesto della sessione corrente).

### Esempio 10: Ottenere il riepilogo più recente degli stati dei criteri non conformi per la definizione di un criterio nella sottoscrizione specificata
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ottiene la visualizzazione di riepilogo degli stati di conformità dei criteri più recenti generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) applicate dalla definizione dei criteri specificata (esistente nella sottoscrizione specificata).

### Esempio 11: Ottenere il riepilogo più recente degli stati dei criteri non conformi per un'assegnazione di criteri nella sottoscrizione corrente
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Ottiene la visualizzazione di riepilogo degli stati di conformità dei criteri più recenti generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) applicate dall'assegnazione dei criteri specificata (presente nella sottoscrizione nel contesto della sessione corrente).

### Esempio 12: Ottenere il riepilogo più recente degli stati dei criteri non conformi per un'assegnazione di criteri nella sottoscrizione specificata
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Ottiene la visualizzazione di riepilogo degli stati di conformità dei criteri più recenti generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) applicate dall'assegnazione dei criteri specificata (esistente nella sottoscrizione specificata).

### Esempio 13: Ottenere il riepilogo più recente degli stati dei criteri non conformi per un'assegnazione di criteri nel gruppo di risorse specificato nella sottoscrizione corrente
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Ottiene la visualizzazione di riepilogo degli stati di conformità dei criteri più recenti generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) applicate dall'assegnazione di criteri specificata (presente nel gruppo di risorse nella sottoscrizione nel contesto della sessione corrente).

### Esempio 14: Ottenere il riepilogo più recente degli stati dei criteri non conformi nell'ambito della sottoscrizione corrente, con l'opzione di query Principale
```powershell
PS C:\> Get-AzPolicyStateSummary -Top 5
```

Ottiene la visualizzazione di riepilogo degli stati di conformità dei criteri più recenti generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente. Il comando ordina i riepiloghi delle assegnazioni dei criteri nei risultati in base al numero di risorse non conformi in ordine decrescente e accetta solo i primi 5 riepiloghi delle assegnazioni dei criteri.

### Esempio 15: Ottenere il riepilogo più recente degli stati dei criteri non conformi nell'ambito della sottoscrizione corrente, con le opzioni di query Da e A
```powershell
PS C:\> Get-AzPolicyStateSummary -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

Ottiene la visualizzazione di riepilogo degli stati di conformità dei criteri più recenti generati nell'intervallo di date specificato per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente.

### Esempio 16: Ottenere il riepilogo più recente degli stati dei criteri non conformi nell'ambito della sottoscrizione corrente, con l'opzione della query di filtro
```powershell
PS C:\> Get-AzPolicyStateSummary -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

Ottiene la visualizzazione di riepilogo degli stati di conformità dei criteri più recenti generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente.
Il comando limita i risultati restituiti filtrando in base all'azione di definizione dei criteri (incluse le azioni di negazione o controllo) e alla posizione delle risorse (esclusa la posizione est).

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

### Microsoft.Azure.Commands.PolicyInsights.Models.PolicyStateSummary

## NOTE

## COLLEGAMENTI CORRELATI

[Get-AzPolicyState](./Get-AzPolicyState.md)
