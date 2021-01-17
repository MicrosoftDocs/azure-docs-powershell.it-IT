---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 29ABCC1B-8590-4243-A629-709F207927B4
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: a89b4210fcd498aca3a25451e6f691df20d5510e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474460"
---
# Get-AzOperationalInsightsStorageInsight

## Sinossi
Ottiene informazioni su un'analisi dello spazio di archiviazione.

## SINTASSI

### ByWorkspaceName (impostazione predefinita)
```
Get-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByWorkspaceObject
```
Get-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzOperationalInsightsStorageInsight** ottiene informazioni su un'analisi dello spazio di archiviazione esistente.
Se si specifica un nome di Insight di archiviazione, questo cmdlet ottiene le informazioni relative all'analisi dello spazio di archiviazione.
Se non specifichi un nome, questo cmdlet riceverà informazioni su tutti gli approfondimenti di archiviazione in un'area di lavoro.

## ESEMPI

### Esempio 1: ottenere una panoramica dello spazio di archiviazione per nome
```
PS C:\>Get-AzOperationalInsightsStorageInsight -Name "MyStorageInsight" -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

Questo comando consente di ottenere la panoramica dello spazio di archiviazione denominata MyStorageInsight dall'area di lavoro denominata ContosoWorkspace.

### Esempio 2: ottenere una panoramica dello spazio di archiviazione utilizzando un oggetto area di lavoro
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
PS C:\>Get-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight"
```

Il primo comando usa il cmdlet **Get-AzOperationalInsightsWorkspace** per ottenere un'area di lavoro Insights operativa e lo archivia nella variabile $Workspace.
Il secondo comando consente di ottenere l'Insight di archiviazione denominato MyStorageInsight per l'area di lavoro in $Workspace.

## PARAMETRI

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

### -Nome
Specifica il nome della panoramica dello spazio di archiviazione.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome di un gruppo di risorse Azure.

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Area di lavoro
Specifica l'area di lavoro che contiene gli approfondimenti dello spazio di archiviazione.

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WorkspaceName
Specifica il nome dell'area di lavoro che contiene gli approfondimenti dello spazio di archiviazione.

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace

### System. String

## OUTPUT

### Microsoft. Azure. Commands. OperationalInsights. Models. PSStorageInsight

## Note

## COLLEGAMENTI CORRELATI

[Cmdlet di Insight operativi di Azure](./Az.OperationalInsights.md)


