---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: B07FE1A2-732D-4CCF-A0DF-3CF6B91FB3F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
ms.openlocfilehash: 292a288850371a834f938143cf2ec4380504091b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198887"
---
# Get-AzDataFactoryHub

## SYNOPSIS
Ottiene informazioni sugli hub in Data factory di Azure.

## SINTASSI

### ByFactoryName (Default)
```
Get-AzDataFactoryHub [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzDataFactoryHub [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il **cmdlet Get-AzDataFactoryHub** ottiene informazioni sugli hub in Data factory di Azure.
Se si specifica il nome di un hub, questo cmdlet ottiene informazioni sull'hub.
Se non si specifica un nome, questo cmdlet ottiene informazioni su tutti gli hub in un data factory.

## ESEMPI

### Esempio 1: Ottenere tutti gli hub dati
```
PS C:\>Get-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory"
```

Questo comando recupera tutti gli hub dati nel gruppo di risorse azure denominato ADFResourceGroup e il data factory denominato ADFDataWith.

### Esempio 2: Ottenere un hub dati specifico
```
PS C:\>Get-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "MyDataHub"
```

Questo comando recupera informazioni sull'hub denominato MyDataHub nel gruppo di risorse azure denominato ADFResourceGroup e sul data factory denominato ADFDataWith.

## PARAMETERS

### -DataFactory
Specifica un **oggetto PSDataFactory.**
Questo cmdlet ottiene informazioni sugli hub nel data factory specificato da questo parametro.

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataFactoryName
Specifica il nome di un data factory.
Questo cmdlet ottiene informazioni sugli hub nel data factory specificato da questo parametro.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Name
Specifica il nome dell'hub su cui ottenere informazioni.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome di un gruppo di risorse di Azure.
Questo cmdlet ottiene informazioni sugli hub appartenenti al gruppo specificato da questo parametro.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### System.String

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

## OUTPUT

### Microsoft.Azure.Commands.DataFactories.Models.PSHub

## NOTE
* Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori

## COLLEGAMENTI CORRELATI

[New-AzDataHub](./New-AzDataFactoryHub.md)

[Remove-AzDataHub](./Remove-AzDataFactoryHub.md)


