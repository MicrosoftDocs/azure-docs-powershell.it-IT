---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicymetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
ms.openlocfilehash: cfd32e7ee70ffb387bd1d2a52fdbf5eb60f2e148
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022430"
---
# Get-AzPolicyMetadata

## Sinossi
Ottiene risorse per i metadati dei criteri

## SINTASSI

```
Get-AzPolicyMetadata [-Name <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzPolicyRemediation** consente di ottenere tutte le risorse di metadati dei criteri o una particolare risorsa di metadati dei criteri.

## ESEMPI

### Esempio 1: ottenere tutte le risorse per i metadati dei criteri
```powershell
PS C:\> Get-AzPolicyMetadata
```

Questo comando consente di ottenere tutte le risorse dei criteri

### Esempio 2: ottenere una raccolta di 10 risorse per i metadati dei criteri
```powershell
PS C:\> Get-AzPolicyMetadata -Top 10
```

Questo comando ottiene una raccolta di 10 risorse per i metadati dei criteri

### Esempio 3: ottenere una singola risorsa di metadati dei criteri con il nome "ACF1348"
```powershell
PS C:\> Get-AzPolicyMetadata -Name ACF1348
```

Questo comando consente di ottenere una singola risorsa di metadati dei criteri con il nome "ACF1348"

## PARAMETRI

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

### -Nome
Nome risorsa.

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

### -Inizio pagina
Numero massimo di risorse di metadati dei criteri da restituire.

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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### System. String

## OUTPUT

### Microsoft. Azure. Commands. PolicyInsights. Models. PSPolicyMetadata

## Note

## COLLEGAMENTI CORRELATI
