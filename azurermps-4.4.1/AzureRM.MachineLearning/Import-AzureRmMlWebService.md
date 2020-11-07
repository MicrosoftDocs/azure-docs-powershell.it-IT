---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Import-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Import-AzureRmMlWebService.md
ms.openlocfilehash: d85767623d88c9fd7d0a00ea98e575953132d3f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688282"
---
# Import-AzureRmMlWebService

## Sinossi
Importa un oggetto JSON in una definizione di servizio Web.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### Importare da file JSON.
```
Import-AzureRmMlWebService -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Importare da una stringa JSON.
```
Import-AzureRmMlWebService -JsonString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet Import-AzureRmMlWebService importa, specificato direttamente o in un file a cui si fa riferimento, e crea un oggetto definizione di servizio Web che può essere passato al cmdlet New-AzureRmMlWebService.

## ESEMPI

### --------------------------Esempio 1: importare da una stringa--------------------------
@ {Paragraph = PS C: \\ \> }





```
Import-AzureRmMlWebService -JsonString $jsonDefinition
```

### --------------------------Esempio 2: importare da un percorso di file--------------------------
@ {Paragraph = PS C: \\ \> }





```
Import-AzureRmMlWebService -InputFile "C:\mlservice.json"
```

## PARAMETRI

### -InputFile
Percorso del file che contiene la definizione del servizio Web da importare.

```yaml
Type: System.String
Parameter Sets: Import from JSON file.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JsonString
Stringa formattata JSON contenente la definizione del servizio Web da importare.

```yaml
Type: System.String
Parameter Sets: Import from JSON string.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

## OUTPUT

### Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService

## Note
Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml

## COLLEGAMENTI CORRELATI

