---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/set-azurermdeploymentmanagerservice
schema: 2.0.0
ms.openlocfilehash: 2f4cab266cf63e1c33c35c051e9cc2b838f5b066
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490809"
---
# Set-AzureRmDeploymentManagerService

## Sinossi
Aggiorna un servizio nella topologia del servizio.

## SINTASSI

```
Set-AzureRmDeploymentManagerService [-Service] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet **set-AzureRmDeploymentManagerService** aggiorna un servizio con l'oggetto servizio specificato.
Il cmdlet restituisce l'oggetto servizio aggiornato.

## ESEMPI

### Esempio 1
```powershell
PS C:\> Set-AzureRmDeploymentManagerService -Service $serviceObject
```

Questo comando aggiorna un servizio il cui nome, nome della topologia del servizio e ResourceGroup corrispondono rispettivamente alle proprietà Name, ServiceTopologyName e ResourceGroupName della $serviceObject.
Il servizio verrà aggiornato alle proprietà impostate nel $serviceObject.

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

### -Servizio
Oggetto servizio.

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Confermare
Richiede la conferma prima di eseguire il cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa succede se il cmdlet viene eseguito. Il cmdlet non viene eseguito.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceResource

## OUTPUT

### Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceResource

## Note

## COLLEGAMENTI CORRELATI

[New-AzureRmDeploymentManagerService](./New-AzureRmDeploymentManagerService.md)

[Get-AzureRmDeploymentManagerService](./Set-AzureRmDeploymentManagerService.md)

[Remove-AzureRmDeploymentManagerService](./Remove-AzureRmDeploymentManagerService.md)