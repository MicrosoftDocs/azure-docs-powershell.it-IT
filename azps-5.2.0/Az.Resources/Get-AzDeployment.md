---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
ms.openlocfilehash: 75ebbe0eedd9aad396500701d5e94efff76069f2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325399"
---
# Get-AzDeployment

## Sinossi
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

## Descrizione
Il cmdlet **Get-AzDeployment** ottiene le distribuzioni in corrispondenza dell'ambito corrente della sottoscrizione.
Specificare il *nome* o il parametro *ID* per filtrare i risultati.
Per impostazione predefinita, **Get-AzDeployment** ottiene tutte le distribuzioni nell'ambito corrente della sottoscrizione.

## ESEMPI

### Esempio 1: ottenere tutte le distribuzioni all'ambito dell'abbonamento
```
PS C:\>Get-AzDeployment
```

Questo comando consente di ottenere tutte le distribuzioni nell'ambito corrente della sottoscrizione.

### Esempio 2: ottenere una distribuzione per nome
```
PS C:\>Get-AzDeployment -Name "DeployRoles01"
```

Questo comando consente di ottenere la distribuzione di DeployRoles01 nell'ambito corrente della sottoscrizione.
È possibile assegnare un nome a una distribuzione quando la si crea usando i cmdlet **New-AzDeployment** .
Se non si assegna un nome, i cmdlet prevedono un nome predefinito basato sul modello usato per creare la distribuzione.

## PARAMETRI

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

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

### -ID
ID risorsa completo della distribuzione.
esempio:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}

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

### -Nome
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
Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.

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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### Nessuno

## OUTPUT

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEPLOYMENT

## Note

## COLLEGAMENTI CORRELATI
