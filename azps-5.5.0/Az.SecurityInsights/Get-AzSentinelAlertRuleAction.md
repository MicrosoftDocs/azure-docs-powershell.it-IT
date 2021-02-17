---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 6e60f4ed93dd3963fa748db250cacfcf0aeecce3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191215"
---
# Get-AzSentinelAlertRuleAction

## SYNOPSIS
Ottenere una risposta automatica (azione regola di avviso).

## SINTASSI

### AlertRuleId (impostazione predefinita)
```
Get-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ActionId
```
Get-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 -ActionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Get-AzSentinelAlertRuleAction** ottiene una risposta automatica (azione regola di avviso) dall'area di lavoro specificata.
Se si specificano i *parametri ActionId* e *AlertRuleId,* viene restituito un singolo **oggetto AlertRuleAction.**
Se non si specifica il parametro *ActionId,* verrà restituita una matrice contenente tutte le azioni per la regola di avviso specifica nell'area di lavoro specificata.
È possibile usare **l'oggetto Azione** per aggiornare l'azione, ad esempio per modificare l'azione **di** una regola di avviso.

## ESEMPI

### Esempio 1
```powershell
PS C:\> $AlertRuleActions = Get-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
```

Questo esempio recupera  tutte le azioni per la regola di avviso specificata nell'area di lavoro specificata e quindi la archivia nella variabile $AlertRuleActions specificata.

### Esempio 2
```powershell
PS C:\> $AlertRuleAction = Get-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId"
```

Questo esempio ottiene **un'azione AlertRuleAction** per la regola di avviso specificata nell'area di lavoro specificata e la archivia nella variabile $AlertRuleAction specificata.

## PARAMETERS

### -ActionId
ID azione.

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AlertRuleId
ID regola di avviso.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
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

### -ResourceGroupName
Nome del gruppo di risorse.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkspaceName
Nome area di lavoro.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Nessuno
## OUTPUT

### Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse
## NOTE

## COLLEGAMENTI CORRELATI
