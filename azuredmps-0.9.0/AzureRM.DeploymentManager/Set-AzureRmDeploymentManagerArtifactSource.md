---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/set-azurermdeploymentmanagerartifactsource
schema: 2.0.0
ms.openlocfilehash: 230e443fad4740b6bf9896164f02ae9b382e3ed2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491105"
---
# Set-AzureRmDeploymentManagerArtifactSource

## Sinossi
Aggiorna un'origine dell'elemento.

## SINTASSI

```
Set-AzureRmDeploymentManagerArtifactSource [-ArtifactSource] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet **set-AzureRmDeploymentManagerArtifactSource** aggiorna un'origine dell'elemento con l'oggetto origine dell'elemento specificato.
Il cmdlet restituisce l'oggetto ArtifactSource aggiornato.

## ESEMPI

### Esempio 1
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ArtifactSource $artifactSourceObject
```

Questo comando aggiorna un'origine dell'elemento il cui nome e ResourceGroup corrispondono rispettivamente alle proprietà Name e ResourceGroupName della $artifactSourceObject.
L'origine dell'elemento verrà aggiornata alle proprietà impostate nel $artifactSourceObject.

## PARAMETRI

### -ArtifactSource
Oggetto origine elemento.

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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

### Microsoft. Azure. Commands. DeploymentManager. Models. PSArtifactSource

## OUTPUT

### Microsoft. Azure. Commands. DeploymentManager. Models. PSArtifactSource

## Note

## COLLEGAMENTI CORRELATI

[New-AzureRmDeploymentManagerArtifactSource](./New-AzureRmDeploymentManagerArtifactSource.md)

[Get-AzureRmDeploymentManagerArtifactSource](./Get-AzureRmDeploymentManagerArtifactSource.md)

[Remove-AzureRmDeploymentManagerArtifactSource](./Remove-AzureRmDeploymentManagerArtifactSource.md)