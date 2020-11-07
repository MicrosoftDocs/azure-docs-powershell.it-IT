---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
ms.openlocfilehash: ee880422e01b68bb595c709c1642038f75003c49
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93856370"
---
# New-AzTag

## Sinossi
Crea un tag Azure predefinito o aggiunge valori a un tag esistente.

## SINTASSI

```
New-AzTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzTag** crea un tag Azure predefinito con un valore predefinito facoltativo.
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

## ESEMPI

### Esempio 1: creare un tag predefinito
```
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
```
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
```
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
```
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
Specifica il nome del tag.
Per creare un nuovo tag predefinito, immettere un nome univoco.
Per aggiungere un valore a un tag esistente, immettere il nome del tag esistente.
Se un tag predefinito esistente ha il nome specificato, **New-AzTag** aggiunge il valore specificato, se presente, al tag con quel nome invece di creare un nuovo tag.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Valore
Specifica un valore di tag.
I tag predefiniti possono avere più valori, ma è possibile immettere un solo valore in ogni comando.
Questo parametro è facoltativo, perché i tag possono avere nomi senza valori.

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

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### System. String

## OUTPUT

### Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag

## Note

## COLLEGAMENTI CORRELATI

[Get-AzTag](./Get-AzTag.md)

[Remove-AzTag](./Remove-AzTag.md)


