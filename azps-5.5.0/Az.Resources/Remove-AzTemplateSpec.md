---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTemplateSpec.md
ms.openlocfilehash: 718de3ac2da38b8ed7950e8f8a59b0d8fc2f4db7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189215"
---
# Remove-AzTemplateSpec

## SYNOPSIS
Rimuove una specifica del modello

## SINTASSI

### RemoveByNameParameterSet (impostazione predefinita)
```
Remove-AzTemplateSpec [-Force] [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveByIdParameterSet
```
Remove-AzTemplateSpec [-Force] [[-Version] <String>] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIZIONE
Rimuove una specifica specifica specifica del modello. Se viene fornito **il parametro version -Version,** verrà rimossa solo la versione specificata. Se non viene fornita alcuna versione specifica, le specifiche del modello e tutte le relative versioni verranno rimosse. Se il **contrassegno -Force** è presente, non verrà visualizzata alcuna richiesta di conferma per la rimozione.

## ESEMPI

### Esempio 1: Rimozione di una versione specifica in base al nome
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

Rimuove la versione 'v1.0' della specifica di modello denominata "MyTemplateSpec" all'interno del gruppo di risorse "myRG".

### Esempio 2: Rimozione di una versione specifica in base all'ID risorsa
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

Rimuove la versione 'v1.0' della specifica del modello denominata "MyTemplateSpec" all'interno del gruppo di risorse "myRG" del \{ subId della \} sottoscrizione.

### Esempio 3: Rimozione di una specifica di modello e di tutte le versioni in base al nome
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

Rimuove la specifica del modello denominata "MyTemplateSpec" e tutte le relative versioni all'interno del gruppo di risorse "myRG".

### Esempio 3: Rimozione di una specifica del modello e di tutte le versioni in base all'ID risorsa
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -ResourceGroupName 'myRG'
```

Rimuove la specifica del modello denominata "MyTemplateSpec" e tutte le relative versioni all'interno del gruppo di risorse 'myRG' di \{ subscription \} subId.

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

### -Force
Non chiedere conferma.

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

### -Name
Nome della specifica di modello.

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nome del gruppo di risorse delle specifiche del modello.

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
ID risorsa completo della specifica del modello. Esempio: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}

```yaml
Type: System.String
Parameter Sets: RemoveByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Version
Versione delle specifiche del modello da eliminare.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Chiede conferma prima di eseguire il cmdlet.

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
Mostra cosa accadrebbe se il cmdlet viene eseguito. Il cmdlet non viene eseguito.

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

## OUTPUT

### System.Boolean

## NOTE

## COLLEGAMENTI CORRELATI
