---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM.Tags
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/New-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/New-AzureRmTag.md
ms.openlocfilehash: b5b7356a2cda001bb615700b38657cc0d3249ec5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687058"
---
# New-AzureRmTag

## Sinossi
Crea un tag Azure predefinito o aggiunge valori a un tag esistente.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
New-AzureRmTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzureRmTag** crea un tag Azure predefinito con un valore predefinito facoltativo.
Puoi anche usarla per aggiungere altri valori ai tag predefiniti esistenti.
Per creare un tag predefinito, immetti un nome di tag univoco.
Per aggiungere un valore a un tag predefinito esistente, specificare il nome del tag esistente e il nuovo valore.

Questo cmdlet restituisce un oggetto che rappresenta il tag New o Modified con i relativi valori e il numero di risorse a cui è stato applicato.

Il modulo Tag Azure di cui fa parte **New-AzureRmTag** può aiutarti a gestire i tag di Azure predefiniti.
Un tag Azure è una coppia nome-valore che puoi usare per categorizzare le risorse e i gruppi di risorse di Azure, ad esempio per reparto o centro costo, oppure per tenere traccia di note o commenti relativi a risorse e gruppi.

È possibile definire e applicare i tag in un singolo passaggio, ma i tag predefiniti consentono di stabilire nomi e valori standard, coerenti e prevedibili per i tag nell'abbonamento.
Se l'abbonamento include eventuali tag predefiniti, non è possibile applicare tag o valori non definiti a qualsiasi risorsa o gruppo di risorse nell'abbonamento.

Per applicare un contrassegno predefinito a una risorsa o a un gruppo di risorse, usare il parametro *tag* del cmdlet New-AzureRmTag.
Per cercare gruppi di risorse con un nome di tag o un nome e un valore specificati, usare il parametro *tag* del cmdlet Get-AzureRMResourceGroup.

Ogni tag ha un nome.
I valori sono facoltativi.
Un tag Azure predefinito può avere più valori, ma quando si applica il contrassegno a una risorsa o a un gruppo di risorse, è possibile applicare il nome del tag e solo uno dei relativi valori.
Ad esempio, puoi creare un tag di reparto predefinito con un valore per ogni reparto, come finanza, risorse umane e IT.
Quando si applica il tag Department a una risorsa, si applica un solo valore predefinito, ad esempio Finance.

## ESEMPI

### Esempio 1: creare un tag predefinito
```
PS C:\>New-AzureRmTag -Name "FY2015"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====

        Finance     0
```

Questo comando crea un tag predefinito denominato FY2015.
Questo tag non contiene valori.
Puoi applicare un contrassegno senza valori a una risorsa o a un gruppo di risorse oppure usare **New-AzureRmTag** per aggiungere valori al tag.
Puoi anche specificare un valore quando applichi il tag al gruppo di risorse o risorse.

### Esempio 2: creare un tag predefinito con un valore
```
PS C:\>New-AzureRmTag -Name "Department" -Value "Finance"
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
PS C:\>New-AzureRmTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0 PS C:\>New-AzureRmTag -Name "Department" -Value "IT"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0
        IT          0
```

Questi comandi creano un tag predefinito denominato Department con due valori.
Se il nome del tag esiste, **New-AzureRmTag** aggiunge il valore al tag esistente anziché crearne uno nuovo.

### Esempio 4: usare un tag predefinito
```
PS C:\>New-AzureRmTag -Name "CostCenter" -Value "0001"
Name:   CostCenter
Count:  0
Values: 
        Name        Count
        =========   =====
        0001        0 PS C:\>Set-AzureRmResourceGroup -Name "EngineerBlog" -Tag @{Name="CostCenter";Value="0001"}
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
    CostCenter   0001 PS C:\>Get-AzureRmTag -Name "CostCenter"
Name:   CostCenter
Count:  1
Values: 
        Name        Count
        =========   =====
        0001        1 PS C:\>Get-AzureRmResourceGroup -Tag @{Name="CostCenter"}
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

### -Nome
Specifica il nome del tag.
Per creare un nuovo tag predefinito, immettere un nome univoco.

Per aggiungere un valore a un tag esistente, immettere il nome del tag esistente.
Se un tag predefinito esistente ha il nome specificato, **New-AzureRmTag** aggiunge il valore specificato, se presente, al tag con quel nome invece di creare un nuovo tag.

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

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno

## OUTPUT

### Microsoft. Azure. Commands. Tags. Model. PSTag

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureRmTag](./Get-AzureRmTag.md)

[Remove-AzureRmTag](./Remove-AzureRmTag.md)


