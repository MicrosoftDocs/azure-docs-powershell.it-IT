---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 6A834F26-C3D1-46DA-A4A6-1BB5B69291D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
ms.openlocfilehash: 12c3e54725abfd5addf33a3d31edcb8f8016e9dd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179231"
---
# Get-AzOperationalInsightsSchema

## SYNOPSIS
Restituisce lo schema associato a un'area di lavoro.

## SINTASSI

```
Get-AzOperationalInsightsSchema [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Get-AzOperationalInsightsSchema restituisce** lo schema associato all'area di lavoro specificata all'interno del gruppo di risorse.

## ESEMPI

### Esempio 1: Ottenere gli schemi per un'area di lavoro
```
PS C:\>Get-AzOperationalInsightsSchema -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

Questo comando recupera gli schemi associati a un'area di lavoro.

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

### -ResourceGroupName
Specifica il nome di un gruppo di risorse di Azure che contiene un'area di lavoro.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WorkspaceName
Specifica il nome di un'area di lavoro.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### System.String

## OUTPUT

### Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSchemaResponse

## NOTE

## COLLEGAMENTI CORRELATI

[Cmdlet di Azure Operational Insights](./Az.OperationalInsights.md)


