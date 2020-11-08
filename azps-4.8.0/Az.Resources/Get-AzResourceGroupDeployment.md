---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
ms.openlocfilehash: 1db46630ea4f864e1658eea8b789a79e6050fbbb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031517"
---
# Get-AzResourceGroupDeployment

## Sinossi
Ottiene le distribuzioni in un gruppo di risorse.

## SINTASSI

### GetByResourceGroupDeploymentName (impostazione predefinita)
```
Get-AzResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceGroupDeploymentId
```
Get-AzResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzResourceGroupDeployment** ottiene le distribuzioni in un gruppo di risorse Azure.
Specificare il *nome* o il parametro *ID* per filtrare i risultati.
Per impostazione predefinita, **Get-AzResourceGroupDeployment** ottiene tutte le distribuzioni per un gruppo di risorse specificato.
Una risorsa Azure è un'entità Azure gestita dall'utente, ad esempio un server di database, un database o un sito Web.
Un gruppo di risorse Azure è una raccolta di risorse Azure distribuite come unità.
Una distribuzione è l'operazione che rende disponibili le risorse del gruppo risorse per l'uso.
Per altre informazioni sulle risorse Azure e sui gruppi di risorse Azure, vedere il cmdlet New-AzResourceGroup.
Puoi usare questo cmdlet per il rilevamento.
Per il debug, usa questo cmdlet con il cmdlet Get-AzLog.

## ESEMPI

### Esempio 1: ottenere tutte le distribuzioni per un gruppo di risorse
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

Questo comando consente di ottenere tutte le distribuzioni per il gruppo di risorse ContosoLabsRG.
L'output Mostra una distribuzione per un Blog di WordPress che ha usato un modello di raccolta.

### Esempio 2: ottenere una distribuzione per nome
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

Questo comando consente di ottenere la distribuzione DeployWebsite01 del gruppo di risorse ContosoLabsRG.
È possibile assegnare un nome a una distribuzione quando la si crea usando i cmdlet **New-AzResourceGroup** o **New-AzResourceGroupDeployment** .
Se non si assegna un nome, i cmdlet prevedono un nome predefinito basato sul modello usato per creare la distribuzione.

### Esempio 3: ottenere le distribuzioni di tutti i gruppi di risorse
```
PS C:\>Get-AzResourceGroup | Get-AzResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

Questo comando consente di ottenere tutti i gruppi di risorse nell'abbonamento usando il cmdlet Get-AzResourceGroup.
Il comando passa i gruppi di risorse al cmdlet corrente usando l'operatore pipeline.
Il cmdlet corrente ottiene tutte le distribuzioni di tutti i gruppi di risorse nell'abbonamento e passa i risultati al cmdlet Format-Table per visualizzare i valori delle proprietà **ResourceGroupName** , **DeploymentName** e **ProvisioningState** .

## PARAMETRI

### -ApiVersion
Specifica la versione dell'API supportata dal provider di risorse.
Puoi specificare una versione diversa rispetto alla versione predefinita.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -ID
Specifica l'ID della distribuzione del gruppo di risorse da ottenere.

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Specifica il nome della distribuzione da ottenere.
I caratteri jolly non sono consentiti.

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre
Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.

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

### -ResourceGroupName
Specifica il nome di un gruppo di risorse.
Il cmdlet ottiene le distribuzioni per il gruppo di risorse specificato da questo parametro.
I caratteri jolly non sono consentiti.
Questo parametro è obbligatorio ed è possibile specificare un solo gruppo di risorse in ogni comando.

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### System. String

## OUTPUT

### Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSResourceGroupDeployment

## Note

## COLLEGAMENTI CORRELATI

[Get-AzResourceGroup](./Get-AzResourceGroup.md)

[New-AzResourceGroup](./New-AzResourceGroup.md)

[New-AzResourceGroupDeployment](./New-AzResourceGroupDeployment.md)

[Remove-AzResourceGroupDeployment](./Remove-AzResourceGroupDeployment.md)

[Stop-AzResourceGroupDeployment](./Stop-AzResourceGroupDeployment.md)

[Test-AzResourceGroupDeployment](./Test-AzResourceGroupDeployment.md)


