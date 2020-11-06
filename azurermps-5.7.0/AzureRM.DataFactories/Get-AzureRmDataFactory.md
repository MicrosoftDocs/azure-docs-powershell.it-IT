---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: ECE1F469-E3C3-4294-A288-8BAE851E8599
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactory.md
ms.openlocfilehash: 2f0f4ea68de5071a860b55a464d339d65ff2882c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508255"
---
# Get-AzureRmDataFactory

## Sinossi
Ottiene informazioni sulle Factory di dati.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Get-AzureRmDataFactory [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureRmDataFactory** ottiene informazioni sulle Factory di dati in un gruppo di risorse di Azure.
Se specifichi il nome di una data factory, questo cmdlet ottiene informazioni su tale data factory.
Se non specifichi un nome, questo cmdlet recupera informazioni su tutti i factory di dati in un gruppo di risorse di Azure.

## ESEMPI

### Esempio 1: ottenere tutte le factory di dati
```
PS C:\>Get-AzureRmDataFactory -ResourceGroupName "ADF"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : WestUS
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration

DataFactoryName   : WikiADF2
ResourceGroupName : ADF
Location          : westus
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

Questo comando Visualizza informazioni su tutti i factory di dati nell'abbonamento a Azure.

### Esempio 2: ottenere una factory di dati specifica
```
PS C:\>$DataFactory = Get-AzureRmDataFactory -ResourceGroupName "ADF" -Name "WikiADF"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : westus
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

Questo comando Visualizza le informazioni sulla factory di dati denominate WikiADF nell'abbonamento per il gruppo di risorse denominato ADF e lo archivia nella variabile $DataFactory.
Specifica il parametro *DataFactory* nei cmdlet successivi per usare la factory di dati archiviata in $DataFactory.

## PARAMETRI

### -DefaultProfile
Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Specifica il nome della factory di dati per cui ottenere informazioni.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome di un gruppo di risorse Azure.
Questo cmdlet ottiene informazioni sulle Factory di dati che appartengono al gruppo specificato da questo parametro.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno
Questo cmdlet non accetta alcun input.

## OUTPUT

### System. Collections. Generic. list ' 1 [[Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory, Microsoft. WindowsAzure. Commands. Utilities, Version = 0.8.2.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]] Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory

## Note
* Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory

## COLLEGAMENTI CORRELATI

[New-AzureRmDataFactory](./New-AzureRmDataFactory.md)

[Remove-AzureRmDataFactory](./Remove-AzureRmDataFactory.md)


