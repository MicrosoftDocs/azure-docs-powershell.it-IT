---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: B07FE1A2-732D-4CCF-A0DF-3CF6B91FB3F3
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
ms.openlocfilehash: 24c9f9631f1a37e218ff8ddf27ad0de54f2d9dbb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975422"
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

Questo comando recupera informazioni sull'hub denominato MyDataHub nel gruppo di risorse di Azure denominato ADFResourceGroup e sul data factory denominato ADFDataWith.

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
Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure

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
Specifica il nome di un gruppo di risorse azure.
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

[New-AzDataHubHub](./New-AzDataFactoryHub.md)

[Remove-AzDataHub](./Remove-AzDataFactoryHub.md)


