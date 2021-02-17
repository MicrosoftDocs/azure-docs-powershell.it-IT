---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
ms.openlocfilehash: 2679a3f63be3b7332020354e325e33573911334b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177062"
---
# Remove-AzDataShare

## SYNOPSIS
Rimuove una condivisione dati.

## SINTASSI

### ByFieldsParameterSet (Impostazione predefinita)
```
Remove-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByResourceIdParameterSet
```
Remove-AzDataShare -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByObjectParameterSet
```
Remove-AzDataShare -InputObject <PSDataShare> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Remove-AzDataShare** rimuove una condivisione dati.

## ESEMPI

### Esempio 1
```
PS C:\> Remove-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShare"
Are you sure you want to remove data share "AdsShare"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

Questo comando rimuove la condivisione dati denominata AdsShare dall'account di condivisione dati Di Azure WikiAds. 

## PARAMETERS

### -AccountName
Nome account di condivisione dati di Azure

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJob
{{Fill AsJob Description}}

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

### -InputObject
Oggetto di condivisione dati di Azure ' 'Tipo yaml: Set di parametri PSDataShare: Alias ByObjectParameterSet: 

Obbligatorio: Posizione True: Valore predefinito denominato: Nessuna accetta input pipeline: True (ByValue) Accetta caratteri jolly: False

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Nome condivisione dati di Azure

Tipo yaml: Set di parametri stringa: Alias byFieldsParameterSet: 

Obbligatorio: Posizione True: Valore predefinito denominato: Input pipeline None Accept: False Accept wildcard characters: False

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Oggetto restituito (se specificato).

Tipo yaml: Set di parametri SwitchParameter: (Tutti) Alias: 

Obbligatorio: Posizione Falso: valore predefinito denominato: Nessuna accetta input pipeline: Accetta caratteri jolly False: False

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

### -ResourceGroupName
Nome del gruppo di risorse dell'account di condivisione dei dati di Azure

Tipo yaml: Set di parametri stringa: Alias byFieldsParameterSet: 

Obbligatorio: Posizione True: Valore predefinito denominato: Input pipeline None Accept: False Accept wildcard characters: False

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
ID risorsa della condivisione dei dati di Azure

Tipo yaml: Set di parametri stringa: Alias byResourceIdParameterSet: 

Obbligatorio: Posizione True: Valore predefinito denominato: Nessuna accetta input pipeline: True (ByPropertyName) Accetta caratteri jolly: False

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Chiede conferma prima di eseguire il cmdlet.

Tipo yaml: Set di parametri SwitchParameter: (All) Alias: cf

Obbligatorio: Posizione Falso: valore predefinito denominato: Nessuna accetta input pipeline: Accetta caratteri jolly False: False

```yaml
Type: System.Management.Automation.SwitchParameter
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

Tipo yaml: Set di parametri SwitchParameter: (All) Alias: wi

Obbligatorio: Posizione Falso: valore predefinito denominato: Nessuna accetta input pipeline: Accetta caratteri jolly False: False




Tipo yaml: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDset di parametri ataShare: Alias byObjectParameterSet:

Obbligatorio: Posizione True: Valore predefinito denominato: Nessuna accetta input pipeline: True (ByValue) Accetta caratteri jolly: False

```yaml
Type: System.Management.Automation.SwitchParameter
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

### Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare

## OUTPUT

### System.Boolean

## NOTE

## COLLEGAMENTI CORRELATI
