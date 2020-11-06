---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerservicetopology
schema: 2.0.0
ms.openlocfilehash: f5e0b1e0b2e85eb3c17a53b0108e853535712db1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93507135"
---
# Get-AzureRmDeploymentManagerServiceTopology

## Sinossi
Ottiene una topologia di servizio.

## SINTASSI

### Interattivo (impostazione predefinita)
```
Get-AzureRmDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceId
```
Get-AzureRmDeploymentManagerServiceTopology [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InputObject
```
Get-AzureRmDeploymentManagerServiceTopology [-ServiceTopology] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureRmDeploymentManagerServiceTopology** ottiene una topologia di servizio.

Puoi modificare l'oggetto localmente e quindi applicare le modifiche alla topologia usando il cmdlet Set-AzureRmDeploymentManagerServiceTopology.
Specificare la topologia del servizio in base al nome e al nome del gruppo di risorse. In alternativa, puoi specificare l'oggetto ServiceTopology o ResourceId.

## ESEMPI

### Esempio 1
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

Questo comando ottiene una topologia di servizio denominata ContosoServiceTopology in ContosoResourceGroup.

### Esempio 2: ottenere una topologia di servizio usando l'identificatore delle risorse.
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

Questo comando ottiene una topologia di servizio denominata ContosoServiceTopology in ContosoResourceGroup.

### Esempio 3: ottenere una topologia di servizio usando l'oggetto topologia del servizio.
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -ServiceTopology $serviceTopologyObject
```

Questo comando ottiene una topologia di servizio il cui nome e ResourceGroup corrispondono rispettivamente alle proprietà Name e ResourceGroupName della $serviceTopologyObject.

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
Nome della topologia del servizio.

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

### -ServiceTopology
Oggetto Resource della topologia del servizio.

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno

## OUTPUT

### Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceTopologyResource

## Note

## COLLEGAMENTI CORRELATI

[New-AzureRmDeploymentManagerServiceTopology](./New-AzureRmDeploymentManagerServiceTopology.md)

[Remove-AzureRmDeploymentManagerServiceTopology](./Remove-AzureRmDeploymentManagerServiceTopology.md)

[Set-AzureRmDeploymentManagerServiceTopology](./Set-AzureRmDeploymentManagerServiceTopology.md)