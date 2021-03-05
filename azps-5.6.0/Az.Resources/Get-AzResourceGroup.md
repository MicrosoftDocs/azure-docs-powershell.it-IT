---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
ms.openlocfilehash: e431e1e9186cdaf0ec722b5a609a3f0a9f186bd7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973534"
---
# Get-AzResourceGroup

## SYNOPSIS
Ottiene gruppi di risorse.

## SINTASSI

### GetByResourceGroupName (impostazione predefinita)
```
Get-AzResourceGroup [[-Name] <String>] [[-Location] <String>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceGroupId
```
Get-AzResourceGroup [[-Location] <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Get-AzResourceGroup** ottiene i gruppi di risorse di Azure nella sottoscrizione corrente.
È possibile ottenere tutti i gruppi di risorse oppure specificare un gruppo di risorse in base al nome o ad altre proprietà.
Per impostazione predefinita, questo cmdlet recupera tutti i gruppi di risorse nella sottoscrizione corrente.
Per altre informazioni sulle risorse di Azure e sui gruppi di risorse di Azure, vedere il cmdlet New-AzResourceGroup Azure.

## ESEMPI

### Esempio 1: Ottenere un gruppo di risorse per nome
```
PS C:\> Get-AzResourceGroup -Name "EngineerBlog"
```

Questo comando recupera il gruppo di risorse di Azure nell'abbonamento denominato EngineerBlog.

### Esempio 2: Ottenere tutti i tag di un gruppo di risorse
```
PS C:\> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

Questo comando recupera il gruppo di risorse denominato ContosoRG e visualizza i tag associati al gruppo.

### Esempio 3: Ottenere gruppi di risorse in base al tag
```
PS C:\> Get-AzResourceGroup -Tag @{'environment'='prod'}
```

### Esempio 4: Visualizzare i gruppi di risorse per posizione
```
PS C:\> Get-AzResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### Esempio 5: Visualizzare i nomi di tutti i gruppi di risorse in una posizione specifica
```
PS C:\> Get-AzResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### Esempio 6: Visualizzare i gruppi di risorse i cui nomi iniziano con WebServer
```
PS C:\> Get-AzResourceGroup -Name WebServer*
```

## PARAMETERS

### -ApiVersion
Specifica la versione dell'API supportata dal provider di risorse.
È possibile specificare una versione diversa da quella predefinita.

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

### -Id
Specifica l'ID del gruppo di risorse da ottenere.
Non sono consentiti caratteri jolly.

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Location
Specifica la posizione del gruppo di risorse da ottenere.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Specifica il nome del gruppo di risorse da ottenere. Questo parametro supporta i caratteri jolly all'inizio e/o alla fine della stringa.

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupName
Aliases: ResourceGroupName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
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

### -Tag
Tabella hash del tag in base a cui filtrare i gruppi di risorse.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: GetByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### System.String

### System.Collections.Hashtable

## OUTPUT

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup

## NOTE

## COLLEGAMENTI CORRELATI

[New-AzResourceGroup](./New-AzResourceGroup.md)

[Remove-AzResourceGroup](./Remove-AzResourceGroup.md)

[Set-AzResourceGroup](./Set-AzResourceGroup.md)

