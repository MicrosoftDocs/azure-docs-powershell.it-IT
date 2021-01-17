---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicystatesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
ms.openlocfilehash: ad622662615e74908c3d34c513e8570286b76297
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372508"
---
# Get-AzPolicyStateSummary

## Sinossi
Ottiene il riepilogo degli Stati di conformità dei criteri più recenti per le risorse.

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

## Descrizione
Ottiene una visualizzazione di riepilogo degli ultimi numeri di stato di conformità dei criteri in diversi ambiti, suddivisi in assegnazioni di criteri e definizioni di criteri. Include solo gli Stati dei criteri non conformi.

## ESEMPI

### Esempio 1: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi nell'ambito corrente della sottoscrizione
```powershell
PS C:\> Get-AzPolicyStateSummary
```

Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente.

### Esempio 2: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi nell'ambito di sottoscrizione specificato
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione specificata.

### Esempio 3: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi nell'ambito del gruppo di gestione
```powershell
PS C:\> Get-AzPolicyStateSummary -ManagementGroupName "myManagementGroup"
```

Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'ultimo giorno per tutte le risorse all'interno del gruppo di gestione specificato.

### Esempio 4: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi nell'ambito di un gruppo di risorse nell'abbonamento corrente
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup"
```

Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'ultimo giorno per tutte le risorse all'interno del gruppo di risorse specificato (nell'abbonamento nel contesto della sessione corrente).

### Esempio 5: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi nell'ambito di un gruppo di risorse nell'abbonamento specificato
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'ultimo giorno per tutte le risorse all'interno del gruppo di risorse specificato (nell'abbonamento specificato).

### Esempio 6: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi per una risorsa
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'ultimo giorno per la risorsa specificata.

### Esempio 7: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi per una definizione di set di criteri nell'abbonamento corrente
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) effettuate dalla definizione del set di criteri specificata (presente nell'abbonamento nel contesto della sessione corrente).

### Esempio 8: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi per una definizione di set di criteri nella sottoscrizione specificata
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) effettuate dalla definizione del set di criteri specificata (presente nell'abbonamento specificato).

### Esempio 9: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi per una definizione di criteri nell'abbonamento corrente
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) effettuate dalla definizione di criteri specificata (presente nell'abbonamento nel contesto della sessione corrente).

### Esempio 10: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi per una definizione di criterio nella sottoscrizione specificata
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) effettuate dalla definizione di criteri specificata (presente nell'abbonamento specificato).

### Esempio 11: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi per un'assegnazione di criteri nell'abbonamento corrente
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) effettuate dall'assegnazione di criteri specificata (che esiste nell'abbonamento nel contesto della sessione corrente).

### Esempio 12: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi per un'assegnazione di criteri nell'abbonamento specificato
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) effettuate dall'assegnazione di criteri specificata (che esiste nell'abbonamento specificato).

### Esempio 13: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi per un'assegnazione di criteri nel gruppo di risorse specificato nell'abbonamento corrente
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'ultimo giorno per tutte le risorse (all'interno del tenant nel contesto della sessione corrente) effettuate dall'assegnazione di criteri specificata (esistente nel gruppo risorse della sottoscrizione nel contesto della sessione corrente).

### Esempio 14: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi nell'ambito corrente della sottoscrizione, con l'opzione query superiore
```powershell
PS C:\> Get-AzPolicyStateSummary -Top 5
```

Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente. Il comando Ordina i riepiloghi delle assegnazioni dei criteri nei risultati per i conteggi delle risorse non conformi in ordine decrescente e accetta solo i primi 5 riepiloghi delle assegnazioni dei criteri.

### Esempio 15: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi nell'ambito corrente della sottoscrizione, con le opzioni da e a query
```powershell
PS C:\> Get-AzPolicyStateSummary -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'intervallo di date specificato per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente.

### Esempio 16: ottenere l'ultimo riepilogo degli Stati dei criteri non conformi nell'ambito corrente della sottoscrizione, con l'opzione filtro query
```powershell
PS C:\> Get-AzPolicyStateSummary -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

Ottiene la visualizzazione di riepilogo degli ultimi Stati di conformità dei criteri generati nell'ultimo giorno per tutte le risorse all'interno della sottoscrizione nel contesto della sessione corrente.
Il comando limita i risultati restituiti dal filtro in base all'azione di definizione dei criteri (include le azioni Deny o audit) e la posizione delle risorse (esclude la posizione eastus).

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

### Microsoft. Azure. Commands. PolicyInsights. Models. PolicyStateSummary

## Note

## COLLEGAMENTI CORRELATI

[Get-AzPolicyState](./Get-AzPolicyState.md)
