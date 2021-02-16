---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F94415DA-1A4A-4D37-A626-1EDF5D1EFE74
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 1a0d36c2e871bd0495216bce18d84dff60e1044d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179223"
---
# Get-AzOperationalInsightsWorkspace

## SYNOPSIS
Ottiene informazioni su un'area di lavoro.

## SINTASSI

```
Get-AzOperationalInsightsWorkspace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Get-AzOperationalInsightsWorkspace** ottiene informazioni su un'area di lavoro esistente.
Se si specifica il nome di un'area di lavoro, questo cmdlet ottiene informazioni sull'area di lavoro.
Se non si specifica un nome, questo cmdlet ottiene informazioni su tutte le aree di lavoro in un gruppo di risorse.
Se non si specifica un nome e un gruppo di risorse, questo cmdlet riceve informazioni su tutte le aree di lavoro di una sottoscrizione.

## ESEMPI

### Esempio 1: Ottenere un'area di lavoro in base al nome
```
PS C:\>Get-AzOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup"
```

Questo comando ottiene un'area di lavoro denominata MyWorkspace nel gruppo di risorse denominato ContosoResourceGroup.

## PARAMETERS

### -DefaultProfile
Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure

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
Specifica il nome dell'area di lavoro.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome di un gruppo di risorse di Azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### System.String

## OUTPUT

### Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace

## NOTE

## COLLEGAMENTI CORRELATI

[Cmdlet di Azure Operational Insights](./Az.OperationalInsights.md)


