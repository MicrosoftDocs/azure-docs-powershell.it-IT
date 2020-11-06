---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerstep
schema: 2.0.0
ms.openlocfilehash: bd17ee5dd653ee66daf014c57661b3787c04b06f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490950"
---
# Get-AzureRmDeploymentManagerStep

## Sinossi
Ottiene il passaggio di distribuzione.

## SINTASSI

### Interattivo (impostazione predefinita)
```
Get-AzureRmDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceId
```
Get-AzureRmDeploymentManagerStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InputObject
```
Get-AzureRmDeploymentManagerStep [-Step] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureRmDeploymentManagerStep** ottiene un passaggio e restituisce un oggetto che rappresenta questo passaggio.
Specificare il passaggio in base al nome e al nome del gruppo di risorse. In alternativa, puoi specificare l'oggetto step o ResourceId.

Puoi modificare l'oggetto localmente e quindi applicare le modifiche apportate all'origine dell'elemento usando il cmdlet Set-AzureRmDeploymentManagerStep.

## ESEMPI

### Esempio 1: ottenere un passaggio
```powershell
PS C:\> New-AzureRmDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

Questo comando ottiene un passaggio denominato ContosoService1WaitStep in ContosoResourceGroup.

### Esempio 2: ottenere un passaggio usando l'identificatore delle risorse
```powershell
PS C:\> Get-AzureRmDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

Questo comando ottiene un passaggio denominato ContosoService1WaitStep in ContosoResourceGroup.

### Esempio 3: ottenere un passaggio usando un oggetto restituito da New-AzureRmDeploymentManagerStep
```powershell
PS C:\> Get-AzureRmDeploymentManagerStep -Step $stepObject
```

 Questo comando ottiene un passaggio il cui nome e ResourceGroup corrispondono rispettivamente alle proprietà Name e ResourceGroupName della $stepObject.


## PARAMETRI

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

### -Nome
Nome del passaggio.

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gruppo risorse.

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Identificatore della risorsa.

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Step
Oggetto risorsa passaggio.

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.
Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### System. String

### Microsoft. Azure. Commands. DeploymentManager. Models. PSStepResource

## OUTPUT

### Microsoft. Azure. Commands. DeploymentManager. Models. PSStepResource

## Note

## COLLEGAMENTI CORRELATI
