---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
ms.openlocfilehash: 5507e180d5f56b75006f31f9cc6753f50d821a3b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973613"
---
# Get-AzDeploymentOperation

## SYNOPSIS
Ottenere l'operazione di distribuzione

## SINTASSI

### GetByDeploymentName (impostazione predefinita)
```
Get-AzDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByDeploymentObject
```
Get-AzDeploymentOperation -DeploymentObject <PSDeployment> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Get-AzDeploymentOperation** elenca tutte le operazioni che fanno parte di una distribuzione per consentire di identificare e fornire altre informazioni sulle esatte operazioni non riuscite per una particolare distribuzione.
Può anche mostrare la risposta e il contenuto della richiesta per ogni operazione di distribuzione.
Si tratta delle stesse informazioni fornite nei dettagli della distribuzione nel portale.

Per ottenere la richiesta e il contenuto della risposta, abilitare l'impostazione quando si invia una distribuzione tramite **New-AzDeployment.**
Può potenzialmente registrare ed esporre segreti come le password usate nelle operazioni di proprietà delle risorse o **listKeys** che vengono quindi restituite quando si recuperano le operazioni di distribuzione.
Per altre informazioni su questa impostazione e su come abilitarla, vedere New-AzDeployment distribuzione di modelli ARM debug

## ESEMPI

### Esempio 1: Ottenere le operazioni di distribuzione con un nome di distribuzione
```powershell
PS C:\>Get-AzDeploymentOperation -DeploymentName test
```

Recupera l'operazione di distribuzione con il nome "test" nell'ambito della sottoscrizione corrente.

### Esempio 2: Ottenere una distribuzione e ottenere le operazioni di distribuzione
```powershell
PS C:\>Get-AzDeployment -Name "test" | Get-AzDeploymentOperation
```

Questo comando ottiene il "test" di distribuzione nell'ambito di sottoscrizione corrente e ottiene le operazioni di distribuzione.

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

### -DeploymentName
Nome della distribuzione.

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentObject
Oggetto di distribuzione.

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: GetByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -OperationId
ID dell'operazione di distribuzione.

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Pre
Se impostato, indica che il cmdlet deve usare versioni delle API non beta per determinare automaticamente la versione da usare.

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

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment

## OUTPUT

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation

## NOTE

## COLLEGAMENTI CORRELATI
