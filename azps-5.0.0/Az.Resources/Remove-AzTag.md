---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
ms.openlocfilehash: 22a43739ec63f8287ce51c4c4f4a125b4e5b1c65
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203284"
---
# Remove-AzTag

## Sinossi
Elimina i tag o i valori di Azure predefiniti | Elimina l'intero set di tag in una risorsa o un abbonamento.

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

## Descrizione

**RemovePredefinedTagSet** : il cmdlet **Remove-AzTag** Elimina i tag e i valori di Azure predefiniti dall'abbonamento.
Per eliminare valori particolari da un tag predefinito, usare il parametro *value* .
Per impostazione predefinita, **Remove-AzTag** Elimina il tag specificato e tutti i relativi valori. Non è possibile eliminare un tag o un valore attualmente applicato a una risorsa o a un gruppo di risorse.
Prima di usare **Remove-AzTag** , usa il parametro *tag* del cmdlet Set-AzResourceGroup per eliminare il tag o i valori dal gruppo Resource o Resource.
Il modulo tag di Azure che **rimuove-AzTag** fa parte di può aiutare a gestire i tag di Azure predefiniti.
Un tag Azure è una coppia nome-valore che puoi usare per categorizzare le risorse e i gruppi di risorse di Azure, ad esempio per reparto o centro costo, oppure per tenere traccia di note o commenti relativi a risorse e gruppi.
È possibile definire e applicare i tag in un singolo passaggio, ma i tag predefiniti consentono di stabilire nomi e valori standard, coerenti e prevedibili per i tag nell'abbonamento.

**RemoveByResourceIdParameterSet** : il cmdlet **Remove-AzTag** con un **resourceId** Elimina l'intero set di tag in una risorsa o un abbonamento.

## ESEMPI

### Esempio 1: eliminare un tag predefinito
```powershell
PS C:\>Remove-AzTag -Name "Department"
```

Questo comando Elimina il nome del tag predefinito Department e tutti i relativi valori.
Se il tag è stato applicato a qualsiasi risorsa o gruppo di risorse, il comando non riesce.

### Esempio 2: eliminare un valore da un tag predefinito
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

Questo comando Elimina il valore HumanResources dal tag Department predefinito.
Il tag non viene eliminato.
Se il valore è stato applicato a tutte le risorse o ai gruppi di risorse, il comando non riesce.

### Esempio 3: Elimina l'intero set di tag in una sottoscrizione

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}
```

Questo comando Elimina l'intero set di tag nell'abbonamento con {subId}. Non restituirà l'oggetto eliminato se non viene passato "-PassThru".

### Esempio 4: Elimina l'intero set di tag in una risorsa

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

Questo comando Elimina l'intero set di tag nella risorsa con {resourceId}. Restituisce il oject eliminato quando passa "-PassThru".

## PARAMETRI

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

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

### -Nome
Specifica il nome del tag predefinito da rimuovere.
Per impostazione predefinita, **Remove-AzTag** rimuove il tag specificato e tutti i relativi valori.
Per eliminare i valori selezionati, ma non eliminare il tag, usa il parametro *value* .

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

### -Valore
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
Identificatore delle risorse per l'entità Tagged. Una risorsa, un gruppo di risorse o un abbonamento possono essere contrassegnati.

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
Restituisce un oggetto che rappresenta il tag eliminato o il tag risultante con il valore deleted.

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

### -Confermare
Richiede la conferma prima di eseguire il cmdlet.

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
Mostra cosa succede se il cmdlet viene eseguito.
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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### System. String

### System. String []

### System. Management. Automation. SwitchParameter

## OUTPUT

### Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag | Microsoft. Azure. Commands. Tags. Model. PSTagResource

## Note

## COLLEGAMENTI CORRELATI

[Get-AzTag](./Get-AzTag.md)

[New-AzTag](./New-AzTag.md)

[Update-AzTag](./Update-AzTag.md)