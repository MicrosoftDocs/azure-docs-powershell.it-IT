---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/start-azpolicycompliancescan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
ms.openlocfilehash: db51cfdf499fcf3d6c81f47d977978a6ff4bf8cf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989070"
---
# Start-AzPolicyComplianceScan

## SYNOPSIS
Attiva una valutazione di conformità dei criteri per tutte le risorse in una sottoscrizione o un gruppo di risorse.

## SINTASSI

```
Start-AzPolicyComplianceScan [-ResourceGroupName <String>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Start-AzPolicyComplianceScan avvia** una valutazione di conformità dei criteri per una sottoscrizione o un gruppo di risorse. Lo stato di conformità di tutte le risorse all'interno di tale ambito verrà valutato rispetto a tutti i criteri assegnati.

## ESEMPI

### Esempio 1: Avviare un'analisi di conformità nell'ambito della sottoscrizione
```
PS C:\> Start-AzPolicyComplianceScan
```

Questo comando avvia una valutazione di conformità dei criteri per la sottoscrizione attiva.

### Esempio 2: Avviare un'analisi di conformità nell'ambito del gruppo di risorse
```
PS C:\> Start-AzPolicyComplianceScan -ResourceGroupName "myRG"
```

Questo comando avvia una valutazione di conformità dei criteri per il gruppo di risorse "myRG" nella sottoscrizione attiva.

### Esempio 3: Avviare un'analisi di conformità e attendere il completamento in background
```
PS C:\> $job = Start-AzPolicyComplianceScan -AsJob
PS C:\> $job | Wait-Job
```

Questo comando avvia una valutazione di conformità dei criteri per la sottoscrizione attiva. Attenderà il completamento dell'analisi.

## PARAMETERS

### -AsJob
Eseguire il cmdlet in background.

```yaml
Type: SwitchParameter
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Restituisce True se il comando viene completato correttamente.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nome del gruppo di risorse.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Chiede conferma prima di eseguire il cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa accadrebbe se il cmdlet viene eseguito.
Il cmdlet non viene eseguito.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

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

### System.Boolean

## NOTE

## COLLEGAMENTI CORRELATI
