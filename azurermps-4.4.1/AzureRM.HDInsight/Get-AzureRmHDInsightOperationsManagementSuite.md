---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightOperationsManagementSuite.md
ms.openlocfilehash: 0f3e9e542ff1d05a9872096a784c8dabfed1910b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688312"
---
# Get-AzureRmHDInsightOperationsManagementSuite

## Sinossi
Ottiene lo stato dell'installazione di Operations Management Suite (OMS) nel cluster.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Get-AzureRmHDInsightOperationsManagementSuite [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureRmHDInsightOperationsManagementSuite** ottiene lo stato dell'installazione OMS in un cluster HDInsight di Azure. Se OMS è abilitato, restituirà anche l'ID area di lavoro OMS.

## ESEMPI

### Esempio 1
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

L'OMS (Operations Management Suite) è abilitato nel cluster perché la proprietà ClusterMonitoringEnabled è true. L'ID area di lavoro OMS in cui scorrono i registri è 1d364e89-BB71-4503-aa3d-a23535aea7bd

### Esempio 2
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

L'OMS (Operations Management Suite) è abilitato nel cluster perché la proprietà ClusterMonitoringEnabled è true. L'ID area di lavoro OMS in cui scorrono i registri è 1d364e89-BB71-4503-aa3d-a23535aea7bd

### Esempio 3
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

L'OMS (Operations Management Suite) è disabilitata nel cluster perché la proprietà ClusterMonitoringEnabled è false.

### Esempio 4
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

L'OMS (Operations Management Suite) è disabilitata nel cluster perché la proprietà ClusterMonitoringEnabled è false.

## PARAMETRI

### -Nome
Nome del cluster per ottenere lo stato di Operations Management Suite (OMS).

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
Gruppo di risorse del cluster.

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

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### System. String

## OUTPUT

### Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightOMS

## Note

## COLLEGAMENTI CORRELATI

