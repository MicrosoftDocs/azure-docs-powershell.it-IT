---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 54DFBB63-AE8C-4918-870F-19FAD6CC5E4A
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/set-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: ecc68d6f87728f3bccb2d7fe1947c293e6b670d3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989630"
---
# Set-AzOperationalInsightsWorkspace

## SYNOPSIS
Aggiorna un'area di lavoro.

## SINTASSI

### ByName (Impostazione predefinita)
```
Set-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [[-Sku] <String>]
 [[-Tag] <Hashtable>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-PublicNetworkAccessForIngestion <String>] [-PublicNetworkAccessForQuery <String>] [<CommonParameters>]
```

### ByObject
```
Set-AzOperationalInsightsWorkspace [-Workspace] <PSWorkspace> [[-Sku] <String>] [[-Tag] <Hashtable>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-PublicNetworkAccessForIngestion <String>] [-PublicNetworkAccessForQuery <String>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Set-AzOperationalInsightsWorkspace** modifica la configurazione di un'area di lavoro.

## ESEMPI

### Esempio 1: Modificare un'area di lavoro in base al nome
```
PS C:\>Set-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku Standard -Tags @{ "Department" = "IT" }
```

Questo comando modifica lo SKU e i tag dell'area di lavoro denominata MyWorkspace nel gruppo di risorse denominato ContosoResourceGroup.

### Esempio 2: Aggiornare un'area di lavoro tramite la pipeline
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Set-AzOperationalInsightsWorkspace -Sku "Premium"
```

Questo comando usa il cmdlet Get-AzOperationalInsightsWorkspace per ottenere l'area di lavoro denominata MyWorkSpace e quindi la passa al cmdlet **Set-AzOperationalInsightsWorkspace usando** l'operatore della pipeline per impostare lo SKU su Premium.

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
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicNetworkAccessForIngestion
Tipo di accesso di rete per l'accesso all'inserimento nell'area di lavoro. Il valore deve essere "Abilitato" o "Disabilitato"

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

### -PublicNetworkAccessForQuery
Tipo di accesso di rete per accedere alla query dell'area di lavoro. Il valore deve essere "Abilitato" o "Disabilitato"

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

### -ResourceGroupName
Specifica il nome del gruppo di risorse azure.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RetentionInDays
Conservazione dei dati dell'area di lavoro in giorni. 730 giorni è il massimo consentito per tutte le altre SKU

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SKU
Specifica il livello di servizio dell'area di lavoro.
I valori validi sono: 
- gratis
- standard
- premium
- pernode
- autonomo
- pergb2018

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: free, standard, premium, pernode, standalone, pergb2018

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Tag di risorse per l'area di lavoro.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Area di lavoro
Specifica l'area di lavoro da aggiornare.

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace

### System.String

### System.Collections.Hashtable

### System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## OUTPUT

### Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace

## NOTE

## COLLEGAMENTI CORRELATI

[Cmdlet di Azure Operational Insights](./Az.OperationalInsights.md)

[Get-AzOperationalInsightsWorkspace](./Get-AzOperationalInsightsWorkspace.md)


