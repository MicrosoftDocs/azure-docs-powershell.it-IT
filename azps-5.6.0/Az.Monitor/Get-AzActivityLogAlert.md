---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
ms.openlocfilehash: 526b03fb1d73ab88b43929df143e9825f42c7fdf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980206"
---
# Get-AzActivityLogAlert

## SYNOPSIS
Ottiene una o più risorse di avviso del log attività.

## SINTASSI

### GetByNameAndResourceGroup
```
Get-AzActivityLogAlert [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceGroup
```
Get-AzActivityLogAlert [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Get-AzActivityLogAlert** ottiene una o più risorse di avviso del log attività.

## ESEMPI

### Esempio 1: Ottenere avvisi di un log attività in base all'ID sottoscrizione
```
PS C:\>Get-AzActivityLogAlert
```

Questo comando elenca tutti gli avvisi del log attività per la sottoscrizione corrente.

### Esempio 2: Ottenere avvisi del log attività per il gruppo di risorse specificato
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

Questo comando elenca gli avvisi del log attività per il gruppo di risorse specificato.

### Esempio 3: ricevere un avviso del log attività.
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

Questo comando elenca un avviso del log attività (un elenco con un singolo elemento).

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

### -Name
Nome dell'avviso del log attività.

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nome del gruppo di risorse in cui si trova la risorsa di avviso.
Se Name non è Null o vuoto, questo parametro deve contenere e una stringa non vuota.

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### System.String

## OUTPUT

### Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource

## NOTE

## COLLEGAMENTI CORRELATI

[Set-AzActivityLogAlert](./Set-AzActivityLogAlert.md)

[Update-AzActivityLogAlert](./Update-AzActivityLogAlert.md)

[Remove-AzActivityLogAlert](./Remove-AzActivityLogAlert.md)

[New-AzActionGroup](./New-AzActionGroup.md)

[New-AzActivityLogAlertCondition](./New-AzActivityLogAlertCondition.md)
