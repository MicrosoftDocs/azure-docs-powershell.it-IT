---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
ms.openlocfilehash: 892177efebb3a62e40f79b80b1ac67c488e048d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687687"
---
# Test-AzureRmServiceBusName

## Sinossi
Controlla la disponibilità del nome dello spazio dei nomi assegnato

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Test-AzureRmServiceBusName [-Namespace] <String>
```

## Descrizione
Il cmdlet **test-AzureRmServiceBusName** verifica la disponibilità del nome dello spazio dei nomi

## ESEMPI

### Esempio 1
```
PS C:\> Test-AzureRmServiceBusName -Namespace TestingtheAvailability
```

### Esempio 2
```
PS C:\> Test-AzureRmServiceBusName -Namespace Testi
```

### Esempio 3
```
PS C:\> Test-AzureRmServiceBusName -Namespace Test123
```

Restituisce lo stato della disponibilità del nome dello spazio dei nomi

## PARAMETRI

### -Spazio dei nomi
Nome dello spazio dei nomi ServiceBus.

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

### -Spazio dei nomi
 System. String

## OUTPUT

### [Microsoft. Azure. Commands. ServiceBus. Models. CheckNameAvailabilityResultAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]

### Esempio 1
Messaggio motivo NameAvailable
------------- ------ -------
         True   None

### Esempio 2
Messaggio motivo NameAvailable
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.

### Esempio 3
Messaggio motivo NameAvailable
-------------    ------ -------
        False NameInUse The specified service namespace is not available.

## Note

## COLLEGAMENTI CORRELATI
