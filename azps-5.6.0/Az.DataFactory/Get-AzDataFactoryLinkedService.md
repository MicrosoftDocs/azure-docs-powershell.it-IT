---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: DFA41A2B-7C8A-42CB-B0B6-5E6FF853EFEE
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryLinkedService.md
ms.openlocfilehash: 9f52e2a709e2518dbc749b20afc97125e9b3ae64
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975421"
---
# Get-AzDataFactoryLinkedService

## SYNOPSIS
Ottiene informazioni sui servizi collegati in Data factory di Azure.

## SINTASSI

### ByFactoryName (Default)
```
Get-AzDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Get-AzDataFactoryLinkedService** ottiene informazioni sui servizi collegati in Data factory di Azure.
Se si specifica il nome di un servizio collegato, questo cmdlet ottiene informazioni sul servizio collegato.
Se non si specifica un nome, questo cmdlet ottiene informazioni su tutti i servizi collegati nel data factory.

## ESEMPI

### Esempio 1: Ottenere informazioni su tutti i servizi collegati
```
PS C:\>Get-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List
```

Questo comando recupera informazioni su tutti i servizi collegati nel data factory denominato WikiADF e quindi passa i servizi collegati al cmdlet Format-List usando l'operatore della pipeline.
Questo cmdlet formatta i risultati.
Per altre informazioni, digitare `Get-Help Format-List` .

### Esempio 2: Ottenere informazioni su uno specifico servizio collegato
```
PS C:\>Get-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "HDILinkedService"
LinkedServiceName   ResourceGroupName     DataFactoryName              Properties
-----------------   -----------------     ---------------              ----------
HDILinkedService    ADF                   WikiADF                      Microsoft.DataFactories.HDInsightBYOCAsset
```

Questo comando recupera informazioni sul servizio collegato denominato HDILinkedService nel data factory denominato WikiADF.

### Esempio 3: Ottenere informazioni su uno specifico servizio collegato specificando il parametro DataFactory
```
PS C:\>$DataFactory = Get-AzDataFactory -ResourceGroupName "ADF" -Name "ContosoFactory"
PS C:\> Get-AzDataFactoryLinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

Il primo comando usa il cmdlet Get-AzDataFactory per ottenere il data factory denominato ContosoFactory e quindi lo archivia nella $DataFactory variabile.
Il secondo comando riceve informazioni sul servizio collegato per il data factory archiviato in $DataFactory e quindi le passa al cmdlet Format-Table usando l'operatore della pipeline.
**Format-Table formatta** l'output come set di dati con le proprietà specificate come colonne del set di dati.

## PARAMETERS

### -DataFactory
Specifica un **oggetto PSDataFactory.**
Questo cmdlet ottiene servizi collegati che appartengono al data factory specificato da questo parametro.

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
Questo cmdlet ottiene servizi collegati che appartengono al data factory specificato da questo parametro.

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
Specifica il nome del servizio collegato su cui ottenere informazioni.

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
Questo cmdlet ottiene servizi collegati che appartengono al gruppo specificato da questo parametro.

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

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System.String

## OUTPUT

### Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService

## NOTE
* Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori

## COLLEGAMENTI CORRELATI

[New-AzDataFactoryLinkedService](./New-AzDataFactoryLinkedService.md)

[Remove-AzDataFactoryLinkedService](./Remove-AzDataFactoryLinkedService.md)


