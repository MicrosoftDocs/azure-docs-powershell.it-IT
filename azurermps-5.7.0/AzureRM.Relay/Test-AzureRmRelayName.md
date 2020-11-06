---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/test-azurermrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
ms.openlocfilehash: adf7c4b7f8d80e16b49d9d55b742a55279232a07
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518024"
---
# Test-AzureRmRelayName

## Sinossi
Controlla la disponibilità del nome dello spazio dei nomi assegnato

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Test-AzureRmRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **test-AzureRmRelayName** verifica la disponibilità del nome dello spazio dei nomi

## ESEMPI

### Esempio 1
```
PS C:\> Test-AzureRmRelayName -Namespace TestingtheAvailability
```

### Esempio 2
```
PS C:\> Test-AzureRmRelayName -Namespace Testi
```

### Esempio 3
```
PS C:\> Test-AzureRmRelayName -Namespace Test123
```

Restituisce lo stato della disponibilità del nome dello spazio dei nomi

## PARAMETRI

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

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

### -Spazio dei nomi
Nome dello spazio dei nomi Relay.

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

### [Microsoft. Azure. Commands. Relay. Models. CheckNameAvailabilityResultAttributes, Microsoft. Azure. Commands. Relay, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]

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

