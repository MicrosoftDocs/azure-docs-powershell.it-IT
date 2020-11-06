---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
ms.openlocfilehash: 4dfa855bba7318e85eb855e35227070a55d4ed73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520050"
---
# Get-AzureRmMlOpClusterKey

## Sinossi
Ottiene i tasti di scelta associati a un cluster di operatività.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### Ottenere le chiavi del cluster di operatività dai parametri di input dei cmdlet.
```
Get-AzureRmMlOpClusterKey -ResourceGroupName <String> -Name <String>
```

### Ottenere le chiavi del cluster di operatività da una definizione di istanza di OperationalizationCluster.
```
Get-AzureRmMlOpClusterKey -Cluster <PSOperationalizationCluster>
```

### Ottenere le chiavi del cluster di operatività da un ID di risorsa Azure.
```
Get-AzureRmMlOpClusterKey -ResourceId <String>
```

## Descrizione
Quando si ottengono le proprietà del cluster, le chiavi per l'account di archiviazione, il registro dei contenitori e altri servizi associati al cluster di operatività non vengono restituiti. Una chiamata specifica per recuperare le chiavi deve essere eseguita perché sono informazioni riservate.

## ESEMPI

### Esempio 1
```
PS C:\> Get-AzureRmMlOpClusterKey -ResourceGroupName my-group -Name my-cluster
```

Restituisce le chiavi segrete per i servizi associati al cluster di operatività.

## PARAMETRI

### -InputObject
Oggetto cluster di operatività.

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Get operationalization cluster's keys from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nome
Nome del cluster di operatività.

```yaml
Type: String
Parameter Sets: Get operationalization cluster's keys from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nome del gruppo di risorse per il cluster di operatività.

```yaml
Type: String
Parameter Sets: Get operationalization cluster's keys from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
ID risorsa Azure per il cluster di operatività.

```yaml
Type: String
Parameter Sets: Get operationalization cluster's keys from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## INGRESSI

### Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster
System. String


## OUTPUT

### Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationClusterCredentials


## Note

## COLLEGAMENTI CORRELATI

