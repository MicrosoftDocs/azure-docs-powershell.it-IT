---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
ms.openlocfilehash: 92a0aac5043be520f6a7ed7afc2066e0532b79ec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960125"
---
# Get-AzDeployment

## SYNOPSIS
Ottenere la distribuzione

## SINTASSI

### GetByDeploymentName (impostazione predefinita)
```
Get-AzDeployment [[-Name] <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByDeploymentId
```
Get-AzDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Get-AzDeployment** ottiene le distribuzioni nell'ambito di sottoscrizione corrente.
Specificare il *parametro Name* o *Id* per filtrare i risultati.
Per impostazione predefinita, **Get-AzDeployment** ottiene tutte le distribuzioni nell'ambito di sottoscrizione corrente.

## ESEMPI

### Esempio 1: Ottenere tutte le distribuzioni nell'ambito di sottoscrizione
```
PS C:\>Get-AzDeployment
```

Questo comando recupera tutte le distribuzioni con l'ambito di sottoscrizione corrente.

### Esempio 2: Ottenere una distribuzione in base al nome
```
PS C:\>Get-AzDeployment -Name "DeployRoles01"
```

Questo comando ottiene la distribuzione DeployRoles01 nell'ambito della sottoscrizione corrente.
È possibile assegnare un nome a una distribuzione quando viene creata usando i cmdlet **New-AzDeployment.**
Se non si assegna un nome, i cmdlet forniscono un nome predefinito basato sul modello usato per creare la distribuzione.

## PARAMETERS

### -DefaultProfile
Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.

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

### -Id
ID di risorsa completo della distribuzione.
Esempio: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}

```yaml
Type: System.String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Nome della distribuzione.

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Pre
Se impostato, indica che il cmdlet deve usare versioni delle API non definitiva per determinare automaticamente la versione da usare.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Nessuno

## OUTPUT

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment

## NOTE

## COLLEGAMENTI CORRELATI
