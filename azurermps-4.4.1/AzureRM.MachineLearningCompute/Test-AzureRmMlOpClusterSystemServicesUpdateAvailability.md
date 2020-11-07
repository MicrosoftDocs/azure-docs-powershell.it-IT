---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Test-AzureRmMlOpClusterSystemServicesUpdateAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Test-AzureRmMlOpClusterSystemServicesUpdateAvailability.md
ms.openlocfilehash: 067fdf88b7a7b29007f81ab26590ffaa542ac7e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686822"
---
# Test-AzureRmMlOpClusterSystemServicesUpdateAvailability

## Sinossi
Controlla se sono disponibili aggiornamenti per i servizi di sistema associati a un cluster di operatività.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### Verificare la disponibilità degli aggiornamenti dai parametri di input dei cmdlet.
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName <String> -Name <String>
```

### Verificare la disponibilità degli aggiornamenti da una definizione di istanza di OperationalizationCluster.
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -InputObject <PSOperationalizationCluster>
```

### Verificare la disponibilità degli aggiornamenti da un ID di Azure resouce.
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceId <String>
```

## Descrizione
I servizi di sistema ricevono gli aggiornamenti in modo indipendente dal cluster di operatività. L'uso di questo cmdlet consentirà all'utente di sapere se Invoke-AzureRmMlOpClusterSystemServicesUpdate.

## ESEMPI

### Esempio 1
```
PS C:\> Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName my-group -Name my-cluster
```

### Esempio 2
```
PS C:\> Get-AzureRmMlOpCluster | Test-AzureRmMlOpClusterSystemServicesUpdateAvailability
```

### Esempio 3
```
PS C:\> Find-AzureRmResource -ResourceType Microsoft.MachineLearningCompute/operationalizationClusters | Test-AzureRmMlOpClusterSystemServicesUpdateAvailability
```

## PARAMETRI

### -InputObject
Oggetto cluster di operatività.

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Test for update availability from an OperationalizationCluster instance definition.
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
Parameter Sets: Test for update availability from cmdlet input parameters.
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
Parameter Sets: Test for update availability from cmdlet input parameters.
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
Parameter Sets: Test for update availability from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## INGRESSI

### Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster
### System. String


## OUTPUT

### Microsoft. Azure. Commands. MachineLearningCompute. Models. PSCheckSystemServicesUpdatesAvailableResponse


## Note

## COLLEGAMENTI CORRELATI

