---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
ms.openlocfilehash: 22a43739ec63f8287ce51c4c4f4a125b4e5b1c65
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189222"
---
# Remove-AzTag

## SYNOPSIS
Elimina i tag o i valori predefiniti di Azure | Elimina l'intero set di tag per una risorsa o un abbonamento.

## SINTASSI

### RemovePredefinedTagParameterSet

```powershell
Remove-AzTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveByResourceIdParameterSet

```powershell
Remove-AzTag
   -ResourceId <String>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## DESCRIZIONE

**RemovePredefinedTagSet:** il cmdlet **Remove-AzTag** elimina i tag e i valori predefiniti di Azure dalla sottoscrizione.
Per eliminare determinati valori da un tag predefinito, usare il *parametro Value.*
Per impostazione predefinita, **Remove-AzTag** elimina il tag specificato e tutti i relativi valori. Non è possibile eliminare un tag o un valore attualmente applicato a una risorsa o a un gruppo di risorse.
Prima di **usare Remove-AzTag,** usare il parametro *Tag* del cmdlet Set-AzResourceGroup per eliminare il tag o i valori dalla risorsa o dal gruppo di risorse.
Il modulo Tag di Azure **di cui remove-AzTag** fa parte consente di gestire i tag di Azure predefiniti.
Un tag di Azure è una coppia nome-valore che è possibile usare per categorizzare le risorse e i gruppi di risorse di Azure, ad esempio per reparto o centro di costo, oppure per tenere traccia di note o commenti sulle risorse e i gruppi.
È possibile definire e applicare tag in un unico passaggio, ma i tag predefiniti consentono di definire nomi e valori standard, coerenti e prevedibili per i tag nell'abbonamento.

**RemoveByResourceIdParameterSet:** il cmdlet **Remove-AzTag** con **un valore ResourceId** elimina l'intero set di tag per una risorsa o una sottoscrizione.

## ESEMPI

### Esempio 1: Eliminare un tag predefinito
```powershell
PS C:\>Remove-AzTag -Name "Department"
```

Questo comando elimina il tag predefinito denominato Reparto e tutti i relativi valori.
Se il tag è stato applicato a qualsiasi risorsa o gruppo di risorse, il comando non riesce.

### Esempio 2: Eliminare un valore da un tag predefinito
```powershell
PS C:\>Remove-AzTag -Name "Department" -Value "HumanResources" -PassThru
Name:   Department
Count:  14
Values: 

        Name        Count
        =========   =====

        Finance        2
        IT            12
```

Questo comando elimina il valore HumanResources dal tag department predefinito.
Il tag non viene eliminato.
Se il valore è stato applicato a qualsiasi risorsa o gruppo di risorse, il comando non riesce.

### Esempio 3: Elimina l'intero set di tag in un abbonamento

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}
```

Questo comando elimina l'intero set di tag nell'abbonamento con {subId}. Non restituirà l'oggetto eliminato se non passa "-PassThru".

### Esempio 4: Eliminare l'intero set di tag in una risorsa

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1 -PassThru

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

Questo comando elimina l'intero set di tag per la risorsa con {resourceId}. Restituisce l'oggetto eliminato quando si passa "-PassThru".

## PARAMETERS

### -DefaultProfile
Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.

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

### -Name
Specifica il nome del tag predefinito da rimuovere.
Per impostazione predefinita, **Remove-AzTag** rimuove il tag specificato e tutti i relativi valori.
Per eliminare i valori selezionati, ma non eliminare il tag, usare il *parametro* Value.

```yaml
Type: System.String
Parameter Sets: RemovePredefinedTagParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Value
Elimina i valori specificati dal tag predefinito, ma non elimina il tag.

```yaml
Type: System.String[]
Parameter Sets: RemovePredefinedTagParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Identificatore di risorsa per l'entità con tag. Una risorsa, un gruppo di risorse o una sottoscrizione può essere contrassegnata.

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Restituisce un oggetto che rappresenta il tag eliminato o il tag risultante con valore eliminato.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

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

### System.String[]

### System.Management.Automation.SwitchParameter

## OUTPUT

### Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource

## NOTE

## COLLEGAMENTI CORRELATI

[Get-AzTag](./Get-AzTag.md)

[New-AzTag](./New-AzTag.md)

[Update-AzTag](./Update-AzTag.md)