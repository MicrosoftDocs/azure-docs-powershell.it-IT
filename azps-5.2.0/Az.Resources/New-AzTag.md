---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
ms.openlocfilehash: 937ac50ac34f8b04912a0d500dedb5b490806b1a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365872"
---
# New-AzTag

## Sinossi
Crea un tag Azure predefinito o aggiunge valori a un tag esistente | Crea o aggiorna l'intero set di tag in una risorsa o un abbonamento.

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

## Descrizione

**CreatePredefinedTagSet**: il cmdlet **New-AzTag** crea un tag Azure predefinito con un valore predefinito facoltativo.
Puoi anche usarla per aggiungere altri valori ai tag predefiniti esistenti.
Per creare un tag predefinito, immetti un nome di tag univoco.
Per aggiungere un valore a un tag predefinito esistente, specificare il nome del tag esistente e il nuovo valore.
Questo cmdlet restituisce un oggetto che rappresenta il tag New o Modified con i relativi valori e il numero di risorse a cui è stato applicato.
Il modulo Tag Azure di cui fa parte **New-AzTag** può aiutarti a gestire i tag di Azure predefiniti.
Un tag Azure è una coppia nome-valore che puoi usare per categorizzare le risorse e i gruppi di risorse di Azure, ad esempio per reparto o centro costo, oppure per tenere traccia di note o commenti relativi a risorse e gruppi.
È possibile definire e applicare i tag in un singolo passaggio, ma i tag predefiniti consentono di stabilire nomi e valori standard, coerenti e prevedibili per i tag nell'abbonamento.
Per applicare un contrassegno predefinito a una risorsa o a un gruppo di risorse, usare il parametro *tag* del cmdlet New-AzTag.
Per cercare gruppi di risorse con un nome di tag o un nome e un valore specificati, usare il parametro *tag* del cmdlet Get-AzResourceGroup.
Ogni tag ha un nome.
I valori sono facoltativi.
Un tag Azure predefinito può avere più valori, ma quando si applica il contrassegno a una risorsa o a un gruppo di risorse, è possibile applicare il nome del tag e solo uno dei relativi valori.
Ad esempio, puoi creare un tag di reparto predefinito con un valore per ogni reparto, come finanza, risorse umane e IT.
Quando si applica il tag Department a una risorsa, si applica un solo valore predefinito, ad esempio Finance.

**CreateByResourceIdParameterSet**: il cmdlet **New-AzTag** con un **resourceId** crea o aggiorna l'intero set di tag in una risorsa o un abbonamento.
Questa operazione consente di aggiungere o sostituire l'intero set di tag nella risorsa o nell'abbonamento specificato. L'entità specificata può avere un massimo di 50 contrassegni.

## ESEMPI

### Esempio 1: creare un tag predefinito
```powershell
PS C:\>New-AzTag -Name "FY2015"
                                
Name   ValuesTable Count Values 
----   ----------- ----- ------
FY2015             0     {}
```

Questo comando crea un tag predefinito denominato FY2015.
Questo tag non contiene valori.
Puoi applicare un contrassegno senza valori a una risorsa o a un gruppo di risorse oppure usare **New-AzTag** per aggiungere valori al tag.
Puoi anche specificare un valore quando applichi il tag al gruppo di risorse o risorse.

### Esempio 2: creare un tag predefinito con un valore
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

Questo comando crea un tag predefinito denominato Department con un valore di Finance.

### Esempio 3: aggiungere un valore a un tag predefinito
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

Questi comandi creano un tag predefinito denominato Department con due valori.
Se il nome del tag esiste, **New-AzTag** aggiunge il valore al tag esistente anziché crearne uno nuovo.

### Esempio 4: usare un tag predefinito
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

I comandi in questo esempio creano e usano un tag predefinito.

### Esempio 5: crea o aggiorna l'intero set di tag in un abbonamento

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

### Esempio 6: crea o aggiorna l'intero set di tag in una risorsa

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

Questo comando crea o aggiorna l'intero set di tag nella risorsa con {resourceId}.

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

### -Valore
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
Identificatore delle risorse per l'entità da contrassegnare. Una risorsa, un gruppo di risorse o un abbonamento possono essere contrassegnati.

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
Tag da inserire nella risorsa.

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

### System. Collections. Hashtable

## OUTPUT

### Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag | Microsoft. Azure. Commands. Tags. Model. PSTagResource

## Note

## COLLEGAMENTI CORRELATI

[Get-AzTag](./Get-AzTag.md)

[Remove-AzTag](./Remove-AzTag.md)

[Update-AzTag](./Update-AzTag.md)