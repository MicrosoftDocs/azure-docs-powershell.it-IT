---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/get-azpolicymetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
ms.openlocfilehash: 85a5c38038116d89e7cab1e6efe2718d4c5a697b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989153"
---
# Get-AzPolicyMetadata

## SYNOPSIS
Ottiene risorse metadati dei criteri

## SINTASSI

```
Get-AzPolicyMetadata [-Name <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Get-AzPolicyRemediation** ottiene tutte le risorse dei metadati dei criteri o una particolare risorsa metadati dei criteri.

## ESEMPI

### Esempio 1: Ottenere tutte le risorse sui metadati dei criteri
```powershell
PS C:\> Get-AzPolicyMetadata
```

Questo comando recupera tutte le risorse per i metadati dei criteri

### Esempio 2: Ottenere una raccolta di 10 risorse sui metadati dei criteri
```powershell
PS C:\> Get-AzPolicyMetadata -Top 10
```

Questo comando ottiene una raccolta di 10 risorse sui metadati dei criteri

### Esempio 3: Ottenere una singola risorsa metadati criterio con il nome 'ACF1348'
```powershell
PS C:\> Get-AzPolicyMetadata -Name ACF1348
```

Questo comando ottiene una singola risorsa metadati criterio con il nome 'ACF1348'

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

### -Name
Nome della risorsa.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -In alto
Numero massimo di risorse metadati dei criteri da restituire.

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

### Microsoft.Azure.Commands.PolicyInsights.Models.PSPolicyMetadata

## NOTE

## COLLEGAMENTI CORRELATI
