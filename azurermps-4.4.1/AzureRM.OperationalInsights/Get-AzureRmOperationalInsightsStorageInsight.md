---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 29ABCC1B-8590-4243-A629-709F207927B4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: cd7dad03d8542685339778d0b0cdac967f83ea21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687131"
---
# Get-AzureRmOperationalInsightsStorageInsight

## Sinossi
Ottiene informazioni su un'analisi dello spazio di archiviazione.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### ByWorkspaceName (impostazione predefinita)
```
Get-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByWorkspaceObject
```
Get-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureRmOperationalInsightsStorageInsight** ottiene informazioni su un'analisi dello spazio di archiviazione esistente.
Se si specifica un nome di Insight di archiviazione, questo cmdlet ottiene le informazioni relative all'analisi dello spazio di archiviazione.
Se non specifichi un nome, questo cmdlet riceverà informazioni su tutti gli approfondimenti di archiviazione in un'area di lavoro.

## ESEMPI

### Esempio 1: ottenere una panoramica dello spazio di archiviazione per nome
```
PS C:\>Get-AzureRmOperationalInsightsStorageInsight -Name "MyStorageInsight" -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

Questo comando consente di ottenere la panoramica dello spazio di archiviazione denominata MyStorageInsight dall'area di lavoro denominata ContosoWorkspace.

### Esempio 2: ottenere una panoramica dello spazio di archiviazione utilizzando un oggetto area di lavoro
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
PS C:\>Get-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight"
```

Il primo comando usa il cmdlet **Get-AzureRmOperationalInsightsWorkspace** per ottenere un'area di lavoro Insights operativa e lo archivia nella variabile $Workspace.

Il secondo comando consente di ottenere l'Insight di archiviazione denominato MyStorageInsight per l'area di lavoro in $Workspace.

## PARAMETRI

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

### PSWorkspace
Il parametro ' Workspace ' accetta il valore di tipo ' PSWorkspace ' dalla pipeline

## OUTPUT

### System. Collections. Generic. list ' 1 [Microsoft. Azure. Commands. OperationalInsights. Models. PSStorageInsight]

### Microsoft. Azure. Commands. OperationalInsights. Models. PSStorageInsight

## Note

## COLLEGAMENTI CORRELATI

[Cmdlet di Insight operativi di Azure](./AzureRM.OperationalInsights.md)


