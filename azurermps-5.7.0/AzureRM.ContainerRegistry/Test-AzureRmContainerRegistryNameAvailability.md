---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/test-azurermcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryNameAvailability.md
ms.openlocfilehash: da415c21532ea0b2178cc2a75d6a3d09bdc2d50b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516816"
---
# Test-AzureRmContainerRegistryNameAvailability

## Sinossi
Controlla la disponibilità di un nome del registro di sistema contenitore.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Test-AzureRmContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet Test-AzureRmContainerRegistryNameAvailability controlla se un nome del registro di sistema contenitore è valido e disponibile per l'uso.

## ESEMPI

### Esempio 1: verifica la disponibilità di un nome del registro di sistema contenitore
```powershell
PS C:\>Test-AzureRmContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

Questo comando controlla la disponibilità del nome del registro di sistema \` SomeRegistryName \` .

## PARAMETRI

### -Nome
Nome del registro di sistema contenitore.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno
Questo cmdlet non accetta alcun input.

## OUTPUT

### Microsoft. Azure. Management. ContainerRegistry. Models. RegistryNameStatus

## Note

## COLLEGAMENTI CORRELATI

[New-AzureRmContainerRegistry]()

