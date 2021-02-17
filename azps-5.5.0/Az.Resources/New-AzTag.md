---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
ms.openlocfilehash: 937ac50ac34f8b04912a0d500dedb5b490806b1a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183654"
---
# New-AzTag

## SYNOPSIS
Crea un tag di Azure predefinito o aggiunge valori a un tag | Crea o aggiorna l'intero set di tag per una risorsa o un abbonamento.

## SINTASSI

### CreatePredefinedTagParameterSet

```powershell
New-AzTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### CreateByResourceIdParameterSet

```powershell
New-AzTag
   -ResourceId <String>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## DESCRIZIONE

**CreatePredefinedTagSet:** il cmdlet **New-AzTag** crea un tag di Azure predefinito con un valore predefinito facoltativo.
È anche possibile usarla per aggiungere altri valori ai tag predefiniti esistenti.
Per creare un tag predefinito, immettere un nome tag univoco.
Per aggiungere un valore a un tag predefinito esistente, specificare il nome del tag esistente e il nuovo valore.
Questo cmdlet restituisce un oggetto che rappresenta il tag nuovo o modificato con i relativi valori e il numero di risorse a cui è stato applicato.
Il modulo Tag di Azure di cui fa parte **il nuovo AzTag** consente di gestire i tag di Azure predefiniti.
Un tag di Azure è una coppia nome-valore che è possibile usare per categorizzare le risorse e i gruppi di risorse di Azure, ad esempio per reparto o centro di costo, oppure per tenere traccia di note o commenti sulle risorse e i gruppi.
È possibile definire e applicare i tag in un unico passaggio, ma i tag predefiniti consentono di definire nomi e valori standard, coerenti e prevedibili per i tag nell'abbonamento.
Per applicare un tag predefinito a una risorsa o a un gruppo di risorse, usare il *parametro Tag* del cmdlet New-AzTag.
Per cercare gruppi di risorse con un nome tag o un nome e un valore specificati, usare il *parametro Tag* del cmdlet Get-AzResourceGroup.
A ogni tag è stato specificato un nome.
I valori sono facoltativi.
Un tag predefinito di Azure può avere più valori, ma quando si applica il tag a una risorsa o a un gruppo di risorse, si applica il nome del tag e solo uno dei relativi valori.
Ad esempio, è possibile creare un tag Reparto predefinito con un valore per ogni reparto, ad esempio Finanze, Risorse umane e IT.
Quando si applica il tag Reparto a una risorsa, si applica un solo valore predefinito, ad esempio Finanze.

**CreateByResourceIdParameterSet:** il cmdlet **New-AzTag** con **un valore ResourceId** crea o aggiorna l'intero set di tag in una risorsa o una sottoscrizione.
Questa operazione consente di aggiungere o sostituire l'intero set di tag nella risorsa o nella sottoscrizione specificata. L'entità specificata può contenere al massimo 50 tag.

## ESEMPI

### Esempio 1: Creare un tag predefinito
```powershell
PS C:\>New-AzTag -Name "FY2015"
                                
Name   ValuesTable Count Values 
----   ----------- ----- ------
FY2015             0     {}
```

Questo comando crea un tag predefinito denominato FY2015.
Questo tag non ha valori.
È possibile applicare un tag senza valori a una risorsa o a un gruppo di risorse oppure usare **New-AzTag** per aggiungere valori al tag.
È anche possibile specificare un valore quando si applica il tag alla risorsa o al gruppo di risorse.

### Esempio 2: Creare un tag predefinito con un valore
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

Questo comando crea un tag predefinito denominato Reparto con il valore Finanze.

### Esempio 3: Aggiungere un valore a un tag predefinito
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0 
PS C:\>New-AzTag -Name "Department" -Value "IT"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0
        IT          0
```

Questi comandi creano un tag predefinito denominato Reparto con due valori.
Se il nome del tag esiste, **New-AzTag** aggiunge il valore al tag esistente invece di crearne uno nuovo.

### Esempio 4: Usare un tag predefinito
```powershell
PS C:\>New-AzTag -Name "CostCenter" -Value "0001"
Name:   CostCenter
Count:  0
Values: 
        Name        Count
        =========   =====
        0001        0 
PS C:\>Set-AzResourceGroup -Name "EngineerBlog" -Tag @{Name="CostCenter";Value="0001"}
Name:      EngineerBlog
Location:  East US
Resources: 
            
  Name             Type                     Location
    ===============  =======================  ========
    EngineerBlog     Microsoft.Web/sites      West US
    EngSvr01         Microsoft.Sql/servers    West US
    EngDB02          Microsoft.Sql/databases  West US
Tags: 
    Name         Value
    ==========   =====
    CostCenter   0001 
PS C:\>Get-AzTag -Name "CostCenter"
Name:   CostCenter
Count:  1
Values: 
        Name        Count
        =========   =====
        0001        1 
PS C:\>Get-AzResourceGroup -Tag @{Name="CostCenter"}
Name:      EngineerBlog
Location:  East US
Resources: 
     Name             Type                     Location
    ===============  =======================  ========
    EngineerBlog     Microsoft.Web/sites      West US

    EngSvr01         Microsoft.Sql/servers    West US
    EngDB02          Microsoft.Sql/databases  West US
Tags: 
    Name         Value
    ==========   =====
    CostCenter   0001
```

I comandi di questo esempio creano e usano un tag predefinito.

### Esempio 5: Creare o aggiornare l'intero set di tag in un abbonamento

```powershell
PS C:\>$Tags = @{"tagKey1"="tagValue1"; "tagKey2"="tagValue2"}
PS C:\>New-AzTag -ResourceId /subscriptions/{subId} -Tag $Tags

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             tagKey1  tagValue1
             tagKey2  tagValue2
```

Questo comando crea o aggiorna l'intero set di tag nell'abbonamento con {subId}.

### Esempio 6: Creare o aggiornare l'intero set di tag in una risorsa

```powershell
PS C:\>$Tags = @{"Dept"="Finance"; "Status"="Normal"}
PS C:\>New-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1 -Tag $Tags

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

Questo comando crea o aggiorna l'intero set di tag della risorsa con {resourceId}.

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
Specifica il nome del tag predefinito.
Per creare un nuovo tag predefinito, immettere un nome univoco.
Per aggiungere un valore a un tag esistente, immettere il nome del tag esistente.
Se un tag predefinito esistente ha il nome specificato, **New-AzTag** aggiunge il valore specificato, se presente, al tag con quel nome invece di creare un nuovo tag.

```yaml
Type: System.String
Parameter Sets: CreatePredefinedTagParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Value
Specifica un valore di tag predefinito.
I tag predefiniti possono avere più valori, ma è possibile immettere un solo valore in ogni comando.
Questo parametro è facoltativo, perché i tag possono avere nomi senza valori.

```yaml
Type: System.String
Parameter Sets: CreatePredefinedTagParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Identificatore di risorsa per l'entità contrassegnata. Una risorsa, un gruppo di risorse o una sottoscrizione può essere contrassegnata.

```yaml
Type: System.String
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
I tag da inserire nella risorsa.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: 1
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

### Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource

## NOTE

## COLLEGAMENTI CORRELATI

[Get-AzTag](./Get-AzTag.md)

[Remove-AzTag](./Remove-AzTag.md)

[Update-AzTag](./Update-AzTag.md)