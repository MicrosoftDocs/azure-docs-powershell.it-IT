---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 1F094EBA-E4AE-4B3E-BA20-858818C6FD12
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDataSource.md
ms.openlocfilehash: 4fb6a38ff9c79a16d150402d3a2e2be135e0c004
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179246"
---
# Get-AzOperationalInsightsDataSource

## SYNOPSIS
Recuperare origini dati nell'area di lavoro Analisi log di Azure.

## SINTASSI

### ByWorkspaceNameBy Testo (impostazione predefinita)
```
Get-AzOperationalInsightsDataSource [[-ResourceGroupName] <String>] [[-WorkspaceName] <String>]
 [-Kind] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByWorkspaceObjectByName
```
Get-AzOperationalInsightsDataSource [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByWorkspaceObjectBy Scorte
```
Get-AzOperationalInsightsDataSource [[-Workspace] <PSWorkspace>] [[-Kind] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByWorkspaceNameByName
```
Get-AzOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Get-AzOperationalInsightsDataSource ottiene** le origini dati.
È possibile specificare un'origine dati da ottenere.
È possibile filtrare i risultati in base al tipo di origine dati.

## ESEMPI

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

### -Kind
Specifica il tipo di origini dati da ottenere.
I valori accettabili per questo parametro sono:
- AzureActivityLog 
- CustomLog 
- LinuxPerformanceObject 
- LinuxSyslog 
- WindowsEvent 
- WindowsPerformanceCounter

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter, ApplicationInsights

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByKind
Aliases:
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter, ApplicationInsights

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Specifica il nome di un'origine dati da ottenere.

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByName
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByName
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome di un gruppo di risorse che contiene le origini dati da ottenere.

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Area di lavoro
Specifica un'area di lavoro in cui viene eseguito il cmdlet.

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObjectByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObjectByKind
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WorkspaceName
Specifica il nome di un'area di lavoro in cui viene eseguito il cmdlet.

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace

### System.String

## OUTPUT

### Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource

## NOTE
* Parole chiave: azure, azurerm, arm, risorsa, gestione, responsabile, operativo, approfondimenti

## COLLEGAMENTI CORRELATI

[Remove-AzOperationalInsightsDataSource](./Remove-AzOperationalInsightsDataSource.md)

[Set-AzOperationalInsightsDataSource](./Set-AzOperationalInsightsDataSource.md)


