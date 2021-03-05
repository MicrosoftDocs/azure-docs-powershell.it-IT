---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 606C5453-F841-4574-95F8-5CC29A4186E1
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsightproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightProperty.md
ms.openlocfilehash: 9f0ff8ea56110da2fcdc34a973fe8968aa7a701f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009086"
---
# Get-AzHDInsightProperty

## SYNOPSIS
Ottiene le proprietà relative al servizio HDInsight, ad esempio le posizioni disponibili e la capacità.

## SINTASSI

```
Get-AzHDInsightProperty [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Get-AzHDInsightProperty** ottiene proprietà specifiche di Azure HDInsight, ad esempio l'elenco delle posizioni disponibili, le versioni del cluster HDInsight e la capacità di calcolo disponibile.

## ESEMPI

### Esempio 1: Ottenere le proprietà di un cluster Azure HDInsight
```
PS C:\>Get-AzHDInsightProperty -Location "East US 2"
```

Questo comando recupera le proprietà da un servizio HDInsight dalla località Stati Uniti orientali 2.

## PARAMETERS

### -DefaultProfile
Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure

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

### -Location
Specifica la posizione per cui recuperare le proprietà HDInsight.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Nessuno
## OUTPUT

### Microsoft.Azure.Management.HDInsight.Models.AzureHDInsightCapabilities
## NOTE

## COLLEGAMENTI CORRELATI
