---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/test-azurermservicebusname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
ms.openlocfilehash: a35487b2eb1dae8d8af452fba9a47854ecab6efb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512271"
---
# Test-AzureRmServiceBusName

## Sinossi
Controlla la disponibilità del nome o dell'alias dello spazio dei nomi assegnato (nome configurazione DR) 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### AliasCheckNameAvailabilitySet
```
Test-AzureRmServiceBusName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### NamespaceCheckNameAvailabilitySet
```
Test-AzureRmServiceBusName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **test-AzureRmServiceBusName** verifica la disponibilità del nome dello spazio dei nomi o dell'alias (nome configurazione Dr)

## ESEMPI

### Esempio 1
```
PS C:\> Test-AzureRmServiceBusName -Namespace MyNameSapceName
```

Restituisce lo stato della disponibilità del nome dello spazio dei nomi ' MyNameSapceName ' come vero

### Esempio 2
```
PS C:\> Test-AzureRmServiceBusName -Namespace MyNameSapceName
```

Restituisce lo stato della disponibilità del nome dello spazio dei nomi ' MyNameSapceName ' come falso con motivo

### Esempio 3
```
PS C:\> Test-AzureRmServiceBusName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```


## PARAMETRI

### -Aliasname
Nome configurazione DR-nome alias

```yaml
Type: String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases: Alias

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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
Nome dello spazio dei nomi ServiceBus

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nome gruppo risorse

```yaml
Type: String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.
Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### System. String


## OUTPUT

### System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. ServiceBus. Models. PSCheckNameAvailabilityResultAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.5.0.0, Culture = neutral, PublicKeyToken = null]]


## Note

## COLLEGAMENTI CORRELATI
