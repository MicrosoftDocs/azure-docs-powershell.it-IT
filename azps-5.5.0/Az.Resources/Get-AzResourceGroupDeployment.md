---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
ms.openlocfilehash: 82df573a658fda9af97778e59819e45359c226fd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186455"
---
# Get-AzResourceGroupDeployment

## SYNOPSIS
Ottiene le distribuzioni in un gruppo di risorse.

## SINTASSI

### GetByResourceGroupDeploymentName (impostazione predefinita)
```
Get-AzResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceGroupDeploymentId
```
Get-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Get-AzResourceGroupDeployment** ottiene le distribuzioni in un gruppo di risorse di Azure.
Specificare il *parametro Name* o *Id* per filtrare i risultati.
Per impostazione predefinita, **Get-AzResourceGroupDeployment** ottiene tutte le distribuzioni per un gruppo di risorse specificato.
Una risorsa di Azure è un'entità azure gestita dall'utente, ad esempio un server di database, un database o un sito Web.
Un gruppo di risorse di Azure è una raccolta di risorse di Azure distribuite come unità.
Una distribuzione è l'operazione che rende disponibili per l'uso le risorse nel gruppo di risorse.
Per altre informazioni sulle risorse di Azure e sui gruppi di risorse di Azure, vedere il cmdlet New-AzResourceGroup Azure.
È possibile usare questo cmdlet per il monitoraggio.
Per il debug, usare questo cmdlet con Get-AzLog cmdlet.

## ESEMPI

### Esempio 1: Ottenere tutte le distribuzioni per un gruppo di risorse
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

Questo comando recupera tutte le distribuzioni per il gruppo di risorse ContosoLabsRG.
L'output mostra una distribuzione per un blog di WordPress che usava un modello di raccolta.

### Esempio 2: Ottenere una distribuzione in base al nome
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

Questo comando ottiene la distribuzione DeployWebsite01 del gruppo di risorse ContosoLabsRG.
È possibile assegnare un nome a una distribuzione quando viene creata usando i cmdlet **New-AzResourceGroup** **o New-AzResourceGroupDeployment.**
Se non si assegna un nome, i cmdlet forniscono un nome predefinito basato sul modello usato per creare la distribuzione.

### Esempio 3: Ottenere le distribuzioni di tutti i gruppi di risorse
```
PS C:\>Get-AzResourceGroup | Get-AzResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

Questo comando recupera tutti i gruppi di risorse nell'abbonamento usando Get-AzResourceGroup cmdlet.
Il comando passa i gruppi di risorse al cmdlet corrente usando l'operatore pipeline.
Il cmdlet corrente ottiene tutte le distribuzioni di tutti i gruppi di risorse nella sottoscrizione e passa i risultati al cmdlet Format-Table per visualizzare i valori delle proprietà **ResourceGroupName,** **DeploymentName** e **ProvisioningState.**

## PARAMETERS

### -DefaultProfile
Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure

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

### -Name
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
Indica che questo cmdlet considera le versioni delle API non ancora rilasciate quando determina automaticamente la versione da usare.

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
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### System.String

## OUTPUT

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment

## NOTE

## COLLEGAMENTI CORRELATI

[Get-AzResourceGroup](./Get-AzResourceGroup.md)

[New-AzResourceGroup](./New-AzResourceGroup.md)

[New-AzResourceGroupDeployment](./New-AzResourceGroupDeployment.md)

[Remove-AzResourceGroupDeployment](./Remove-AzResourceGroupDeployment.md)

[Stop-AzResourceGroupDeployment](./Stop-AzResourceGroupDeployment.md)

[Test-AzResourceGroupDeployment](./Test-AzResourceGroupDeployment.md)


