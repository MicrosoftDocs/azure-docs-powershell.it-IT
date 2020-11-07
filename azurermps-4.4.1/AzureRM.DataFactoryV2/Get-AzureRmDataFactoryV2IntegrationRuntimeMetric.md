---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 8912717f718bff7c669752e5e49c2796ee94b05b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688656"
---
# Get-AzureRmDataFactoryV2IntegrationRuntimeMetric

## Sinossi
Ottiene i dati metrici per un runtime di integrazione. 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### ByIntegrationRuntimeName (impostazione predefinita)
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String>
```

### ByResourceId
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-ResourceId] <String>
```

### ByIntegrationRuntimeObject
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-InputObject] <PSIntegrationRuntime>
```

## Descrizione
Il cmdlet Get-AzureRmDataFactoryV2IntegrationRuntimeMetric ottiene i dati metrici relativi a Integration Runtime in una data factory.

## ESEMPI

### Esempio 1: ottenere la metrica di Integration Runtime
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeMetric -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

IntegrationRuntimeName ResourceGroupName DataFactoryName   Nodes   
---------------------- ----------------- ---------------   -----   
test-selfhost-ir       rg-test-dfv2      test-df-eu2       {Node_1}
```

Questo comando Visualizza i dati metrici relativi al runtime di integrazione denominato "test-SelfHost-IR" nell'abbonamento per il gruppo di risorse denominato "RG-test-dfv2" e data factory denominato "test-DF-EU2".

## PARAMETRI

### -Datafactoryname
Nome della factory di dati.

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InputObject
Oggetto runtime di Integration.

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nome
Nome del runtime di integrazione.

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nome del gruppo di risorse.

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
ID risorsa di Azure.

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## INGRESSI

### System. String
Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime


## OUTPUT

### Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntimeMetrics


## Note

## COLLEGAMENTI CORRELATI
[Get-AzureRmDataFactoryV2IntegrationRuntime]()

