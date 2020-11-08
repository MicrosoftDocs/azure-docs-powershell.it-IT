---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
ms.openlocfilehash: 2679a3f63be3b7332020354e325e33573911334b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031802"
---
# Remove-AzDataShare

## Sinossi
Rimuove una condivisione dati.

## SINTASSI

### ByFieldsParameterSet (impostazione predefinita)
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

## Descrizione
Il cmdlet **Remove-AzDataShare** rimuove una condivisione dati.

## ESEMPI

### Esempio 1
```
PS C:\> Remove-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShare"
Are you sure you want to remove data share "AdsShare"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

Questo comando rimuove la condivisione dati denominata AdsShare dall'account di condivisione dati di Azure WikiAds. 

## PARAMETRI

### -AccountName
Nome dell'account di condivisione dati di Azure

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

### -InputObject
Oggetto di condivisione dati di Azure ''' tipo YAML: set di parametri PSDataShare: alias ByObjectParameterSet: 

Obbligatorio: posizione vera: valore predefinito denominato: nessuno accetta l'input della pipeline: true (ByValue) accetta caratteri jolly: false

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

### -Nome
Nome condivisione dati di Azure

Tipo YAML: set di parametri stringa: alias ByFieldsParameterSet: 

Obbligatorio: posizione vera: valore predefinito denominato: nessuno accetta l'input della pipeline: false accetta caratteri jolly: false

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
Oggetto return (se specificato).

Tipo YAML: set di parametri SwitchParameter: (tutti) alias: 

Obbligatorio: posizione falsa: valore predefinito denominato: nessuno accetta l'input della pipeline: false accetta caratteri jolly: false

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
Nome del gruppo di risorse dell'account di condivisione dati di Azure

Tipo YAML: set di parametri stringa: alias ByFieldsParameterSet: 

Obbligatorio: posizione vera: valore predefinito denominato: nessuno accetta l'input della pipeline: false accetta caratteri jolly: false

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
ID risorsa della condivisione dati di Azure

Tipo YAML: set di parametri stringa: alias ByResourceIdParameterSet: 

Obbligatorio: posizione vera: valore predefinito denominato: nessuno accetta l'input della pipeline: true (ByPropertyName) accetta caratteri jolly: false

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

### -Confermare
Richiede la conferma prima di eseguire il cmdlet.

Tipo YAML: set di parametri SwitchParameter: (tutti) alias: CF

Obbligatorio: posizione falsa: valore predefinito denominato: nessuno accetta l'input della pipeline: false accetta caratteri jolly: false

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
Mostra cosa succede se il cmdlet viene eseguito.
Il cmdlet non viene eseguito.

Tipo YAML: set di parametri SwitchParameter: (tutti) alias: Wi

Obbligatorio: posizione falsa: valore predefinito denominato: nessuno accetta l'input della pipeline: false accetta caratteri jolly: false




Tipo YAML: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDset di parametri ataShare: alias ByObjectParameterSet:

Obbligatorio: posizione vera: valore predefinito denominato: nessuno accetta l'input della pipeline: true (ByValue) accetta caratteri jolly: false

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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### System. String

### Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare

## OUTPUT

### System. Boolean

## Note

## COLLEGAMENTI CORRELATI
