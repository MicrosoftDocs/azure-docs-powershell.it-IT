---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
ms.openlocfilehash: 058f4a61f1e7ff2fe7f416ea0e4ada098c9efe51
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365273"
---
# Get-AzTag

## Sinossi
Ottiene i tag Azure predefiniti | Ottiene l'intero set di tag in una risorsa o un abbonamento.

## SINTASSI

### GetPredefinedTagParameterSet
```
Get-AzTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceIdParameterSet
```
Get-AzTag -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione

**GetPredefinedTagSet**: il cmdlet **Get-AzTag** ottiene i tag di Azure predefiniti nell'abbonamento.
Questo cmdlet restituisce le informazioni di base sui tag o le informazioni dettagliate sui tag e i relativi valori.
Tutti gli oggetti di output includono una proprietà Count che rappresenta il numero di risorse e gruppi di risorse a cui sono stati applicati i tag e i valori.
Il modulo tag di Azure che **Get-AzTag** fa parte di può aiutare a gestire i tag di Azure predefiniti.
Un tag Azure è una coppia nome-valore che puoi usare per categorizzare le risorse e i gruppi di risorse di Azure, ad esempio per reparto o centro costo, oppure per tenere traccia di note o commenti relativi a risorse e gruppi.
È possibile definire e applicare i tag in un singolo passaggio, ma i tag predefiniti consentono di stabilire nomi e valori standard, coerenti e prevedibili per i tag nell'abbonamento.
Per creare un tag predefinito, usare il cmdlet New-AzTag.
Per applicare un contrassegno predefinito a un gruppo di risorse, usa il parametro *tag* del cmdlet New-AzTag.
Per cercare un nome di tag specifico o un nome e un valore per i gruppi di risorse, usa il parametro *tag* del cmdlet Get-AzResourceGroup.

**GetByResourceIdParameterSet**: il cmdlet **Get-AzTag** con un **resourceId** Ottiene l'intero set di tag in una risorsa o un abbonamento.

## ESEMPI

### Esempio 1: ottenere tutti i tag predefiniti
```powershell
PS C:\>Get-AzTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

Questo comando ottiene tutti i tag predefiniti nell'abbonamento.
La proprietà Count Mostra il numero di volte in cui il tag è stato applicato alle risorse e ai gruppi di risorse nell'abbonamento.

### Esempio 2: ottenere un tag per nome
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

Questo comando consente di ottenere informazioni dettagliate sul tag Department e sui relativi valori.
La proprietà Count Mostra il numero di volte in cui il tag e ognuno dei relativi valori sono stati applicati alle risorse e ai gruppi di risorse nell'abbonamento.

### Esempio 3: ottenere i valori di tutti i tag
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

Questo comando usa il parametro *detailed* per ottenere informazioni dettagliate su tutti i tag predefiniti nell'abbonamento.
L'uso del parametro *detailed* equivale all'uso del parametro *Name* per ogni tag.

### Esempio 4: ottenere l'intero set di tag in una sottoscrizione

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

Questo comando consente di ottenere l'intero set di tag nell'abbonamento con {subId}.

### Esempio 5: ottenere l'intero set di tag in una risorsa

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

Questo comando consente di ottenere l'intero set di tag nella risorsa con {resourceId}.

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

### -Dettagli
Indica che questa operazione aggiunge informazioni sui valori di tag nell'output.

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

### -Nome
Nome del tag predefinito.
Per impostazione predefinita, **Get-AzTag** ottiene le informazioni di base su tutti i tag predefiniti nell'abbonamento.
Quando specifichi il parametro *Name* , il parametro *detailed* non ha alcun effetto.

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
Identificatore delle risorse per l'entità Tagged. Una risorsa, un gruppo di risorse o un abbonamento possono essere contrassegnati.

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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### System. String

### System. Management. Automation. SwitchParameter

## OUTPUT

### Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag | Microsoft. Azure. Commands. Tags. Model. PSTagResource

## Note

## COLLEGAMENTI CORRELATI

[New-AzTag](./New-AzTag.md)

[Remove-AzTag](./Remove-AzTag.md)

[Update-AzTag](./Update-AzTag.md)
