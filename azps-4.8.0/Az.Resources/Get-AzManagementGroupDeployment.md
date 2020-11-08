---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
ms.openlocfilehash: 79eeb4e1725adf38b2f1dc70fe181280312fa1e8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192185"
---
# Get-AzManagementGroupDeployment

## Sinossi
Ottenere la distribuzione in un gruppo di gestione

## SINTASSI

### GetByDeploymentName (impostazione predefinita)
```
Get-AzManagementGroupDeployment [-ManagementGroupId] <String> [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByDeploymentId
```
Get-AzManagementGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzManagementGroupDeployment** ottiene le distribuzioni in un gruppo di gestione.
Specificare il *nome* o il parametro *ID* per filtrare i risultati.
Per impostazione predefinita, **Get-AzManagementGroupDeployment** ottiene tutte le distribuzioni nel gruppo di gestione.

## ESEMPI

### Esempio 1: ottenere tutte le distribuzioni in un gruppo di gestione
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG"
```

Questo comando consente di ottenere tutte le distribuzioni nel gruppo di gestione "myMG".

### Esempio 2: ottenere una distribuzione per nome
```
PS C:\>Get-AzDeployment -ManagementGroupId "myMG" -Name "Deploy01"
```

Questo comando ottiene la distribuzione "Deploy01" nel gruppo di gestione "myMG".
È possibile assegnare un nome a una distribuzione quando la si crea usando i cmdlet **New-AzManagementGroupDeployment** .
Se non si assegna un nome, i cmdlet prevedono un nome predefinito basato sul modello usato per creare la distribuzione.

### Esempio 3: ottenere una distribuzione in base all'ID
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Management/managementGroups/myMG/providers/Microsoft.Resources/deployments/Deploy01"
```

Questo comando ottiene la distribuzione "Deploy01" nel gruppo di gestione "myMG".

## PARAMETRI

### -ApiVersion
Quando è impostato, indica la versione dell'API del provider di risorse da usare.
Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: IAzureContextContainer
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
esempio:/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}

```yaml
Type: String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagementGroupId
ID gruppo di gestione.

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Nome della distribuzione.

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Pre
Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.

```yaml
Type: SwitchParameter
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
