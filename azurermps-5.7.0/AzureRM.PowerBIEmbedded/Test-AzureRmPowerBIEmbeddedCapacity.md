---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/test-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Test-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Test-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 8f6e161ad9ae2078da15dda659f1aea13929eec9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508083"
---
# Test-AzureRmPowerBIEmbeddedCapacity

## Sinossi
Verifica l'esistenza di un'istanza della capacità incorporata di PowerBI.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Test-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [<CommonParameters>]
```

## Descrizione
Il cmdlet Test-AzureRmPowerBIEmbeddedCapacity verifica l'esistenza di un'istanza della capacità incorporata di PowerBI

## ESEMPI

### Esempio 1
```
PS C:\> Test-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

Questo comando testerà se esiste una capacità denominata testcapacity

## PARAMETRI

### -Nome
Nome della capacità incorporata di PowerBI

```yaml
Type: String
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno
Questo cmdlet non accetta alcun input.

## OUTPUT

### System. Boolean

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureRmPowerBIEmbeddedCapacity](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[Remove-AzureRmPowerBIEmbeddedCapacity](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
