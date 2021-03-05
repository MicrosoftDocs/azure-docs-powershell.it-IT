---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/powershell/module/az.resources/get-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
ms.openlocfilehash: b44c861e06c1043fd53e470cfba1e322ce1f1f48
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992444"
---
# Get-AzTag

## SYNOPSIS
Recupera i tag di Azure | Ottiene l'intero set di tag per una risorsa o un abbonamento.

## SINTASSI

### GetPredefinedTagParameterSet
```
Get-AzTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceIdParameterSet
```
Get-AzTag -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE

**GetPredefinedTagSet:** il cmdlet **Get-AzTag** ottiene tag Azure predefiniti nell'abbonamento.
Questo cmdlet restituisce informazioni di base sui tag o informazioni dettagliate sui tag e i relativi valori.
Tutti gli oggetti di output includono una proprietà Count che rappresenta il numero di risorse e gruppi di risorse a cui sono stati applicati i tag e i valori.
Il modulo Tag di Azure di cui fa parte **Get-AzTag** può aiutare a gestire i tag di Azure predefiniti.
Un tag di Azure è una coppia nome-valore che è possibile usare per categorizzare le risorse e i gruppi di risorse di Azure, ad esempio per reparto o centro di costo, oppure per tenere traccia di note o commenti sulle risorse e i gruppi.
È possibile definire e applicare tag in un unico passaggio, ma i tag predefiniti consentono di definire nomi e valori standard, coerenti e prevedibili per i tag nell'abbonamento.
Per creare un tag predefinito, usare il cmdlet New-AzTag tag.
Per applicare un tag predefinito a un gruppo di risorse, usare il *parametro Tag* del cmdlet New-AzTag.
Per cercare un nome tag o un valore o un nome tag specifico nei gruppi di risorse, usare il *parametro Tag* del cmdlet Get-AzResourceGroup.

**GetByResourceIdParameterSet:** il cmdlet **Get-AzTag** con **un valore ResourceId** ottiene l'intero set di tag per una risorsa o una sottoscrizione.

## ESEMPI

### Esempio 1: Ottenere tutti i tag predefiniti
```powershell
PS C:\>Get-AzTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

Questo comando recupera tutti i tag predefiniti nell'abbonamento.
La proprietà Count indica quante volte il tag è stato applicato alle risorse e ai gruppi di risorse nella sottoscrizione.

### Esempio 2: Ottenere un tag in base al nome
```powershell
PS C:\>Get-AzTag -Name "Department"

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3
```

Questo comando ottiene informazioni dettagliate sul tag Department e sui relativi valori.
La proprietà Count indica quante volte il tag e i relativi valori sono stati applicati alle risorse e ai gruppi di risorse nella sottoscrizione.

### Esempio 3: Ottenere i valori di tutti i tag
```powershell
PS C:\>Get-AzTag -Detailed

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3


Name:   FY2015
Count:  2


Name:   CostCenter
Count:  20
Values: 

        Name        Count
        ==========  =====

        0001          5
        0002         10
        0003          5
```

Questo comando usa il *parametro Detailed* per ottenere informazioni dettagliate su tutti i tag predefiniti dell'abbonamento.
*L'uso del parametro Detailed* equivale a usare il *parametro Name* per ogni tag.

### Esempio 4: Ottenere l'intero set di tag in un abbonamento

```powershell
PS C:\>Get-AzTag -ResourceId /subscriptions/{subId}

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             tagKey1  tagValue1
             tagKey2  tagValue2
```

Questo comando recupera l'intero set di tag nell'abbonamento con {subId}.

### Esempio 5: Ottenere l'intero set di tag per una risorsa

```powershell
PS C:\>Get-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

Questo comando ottiene l'intero set di tag per la risorsa con {resourceId}.

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

### -Detailed
Indica che questa operazione aggiunge all'output informazioni sui valori dei tag.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetPredefinedTagParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Nome del tag predefinito.
Per impostazione predefinita, **Get-AzTag** ottiene informazioni di base su tutti i tag predefiniti dell'abbonamento.
Quando si specifica il *parametro Name,* il *parametro Detailed* non ha alcun effetto.

```yaml
Type: System.String
Parameter Sets: GetPredefinedTagParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Identificatore di risorsa per l'entità con tag. Una risorsa, un gruppo di risorse o una sottoscrizione può essere contrassegnata.

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### System.String

### System.Management.Automation.SwitchParameter

## OUTPUT

### Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource

## NOTE

## COLLEGAMENTI CORRELATI

[New-AzTag](./New-AzTag.md)

[Remove-AzTag](./Remove-AzTag.md)

[Update-AzTag](./Update-AzTag.md)
