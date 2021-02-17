---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
ms.openlocfilehash: 9c4bdfe189c16f3e2f6f90d3197149bdc57c78c8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192727"
---
# New-AzResourceGroup

## SYNOPSIS
Crea un gruppo di risorse di Azure.

## SINTASSI

```
New-AzResourceGroup [-Name] <String> [-Location] <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **New-AzResourceGroup** crea un gruppo di risorse di Azure.
È possibile creare un gruppo di risorse usando solo un nome e un percorso e quindi usare il cmdlet New-AzResource per creare risorse da aggiungere al gruppo di risorse.
Per aggiungere una distribuzione a un gruppo di risorse esistente, usare il cmdlet New-AzResourceGroupDeployment distribuzione. Per aggiungere una risorsa a un gruppo di risorse esistente, usare il cmdlet **New-AzResource.** Una risorsa di Azure è un'entità di Azure gestita dall'utente, ad esempio un server di database, un database o un sito Web. Un gruppo di risorse di Azure è una raccolta di risorse di Azure distribuite come unità.

## ESEMPI

### Esempio 1: Creare un gruppo di risorse vuoto
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US"
```

Questo comando crea un gruppo di risorse senza risorse. È possibile usare i cmdlet **New-AzResource** o **New-AzResourceGroupDeployment** per aggiungere risorse e distribuzioni a questo gruppo di risorse.

### Esempio 2: Creare un gruppo di risorse vuoto usando parametri posizionali
```
PS> New-AzResourceGroup RG01 "South Central US"
```

Questo comando crea un gruppo di risorse senza risorse.

### Esempio 3: Creare un gruppo di risorse con contrassegni
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US" -Tag @{Empty=$null; Department="Marketing"}
```

Questo comando crea un gruppo di risorse vuoto. Questo comando è uguale a quello dell'esempio 1, con la differenza che assegna tag al gruppo di risorse. Il primo tag, denominato Vuoto, può essere usato per identificare i gruppi di risorse che non hanno risorse. Il secondo tag si chiama Department e ha valore Marketing. È possibile usare un tag come questo per categorizzare i gruppi di risorse per l'amministrazione o la pianificazione del budget.

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

### -Force
Forza l'esecuzione del comando senza chiedere conferma all'utente.

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

### -Location
Specifica la posizione del gruppo di risorse. Specificare la posizione di un data center di Azure, ad esempio Stati Uniti occidentali o Asia sud-orientale. È possibile inserire un gruppo di risorse in qualsiasi posizione. Il gruppo di risorse non deve essere nella stessa posizione della sottoscrizione di Azure o nella stessa posizione delle relative risorse.
Per determinare la posizione che supporta ogni tipo di risorsa, usare il cmdlet Get-AzResourceProvider con il *parametro ProviderNtassi.*

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Specifica un nome per il gruppo di risorse. Il nome della risorsa deve essere univoco nella sottoscrizione. Se esiste già un gruppo di risorse con questo nome, il comando richiede conferma prima di sostituire il gruppo di risorse esistente.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroupName

Required: True
Position: 0
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

### -Tag
Coppie chiave-valore sotto forma di tabella hash. Ad esempio: @{key0="value0";key1=$null;key2="value2"} Per aggiungere o modificare un tag, è necessario sostituire la raccolta di tag per il gruppo di risorse.
Dopo aver assegnato i tag a risorse e gruppi, è possibile usare il parametro *Tag* di Get-AzResource e Get-AzResourceGroup per cercare risorse e gruppi in base al nome del tag o in base al nome e al valore. È possibile usare i contrassegni per categorizzare le risorse, ad esempio per reparto o centro di costo, oppure per tenere traccia di note o commenti sulle risorse.
Per ottenere i tag predefiniti, usare il cmdlet Get-AzTag predefinito.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Chiede conferma prima di eseguire il cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa accadrebbe se il cmdlet viene eseguito.
Il cmdlet non viene eseguito.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
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

[Get-AzResourceProvider](./Get-AzResourceProvider.md)

[Get-AzResourceGroup](./Get-AzResourceGroup.md)

[New-AzResource](./New-AzResource.md)

[New-AzResourceGroupDeployment](./New-AzResourceGroupDeployment.md)

[Remove-AzResourceGroup](./Remove-AzResourceGroup.md)

[Set-AzResourceGroup](./Set-AzResourceGroup.md)
