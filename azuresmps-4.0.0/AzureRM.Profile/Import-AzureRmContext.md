---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 46efba5e2ab9a5c51172264b343b0f4f2b508065
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/23/2019
ms.locfileid: "93490450"
---
# Import-AzureRmContext

## Sinossi
Carica le informazioni di autenticazione di Azure da un file.

## SINTASSI

### InMemoryProfile
```
Import-AzureRmContext [-AzureContext] <AzureRmProfile> [-WhatIf] [-Confirm]
```

### ProfileFromDisk
```
Import-AzureRmContext [-Path] <String> [-WhatIf] [-Confirm]
```

## Descrizione
Il cmdlet Import-AzureRmContext carica le informazioni di autenticazione da un file per impostare l'ambiente e il contesto di Azure.
I cmdlet eseguiti nella sessione corrente usano queste informazioni per autenticare le richieste in Azure Resource Manager.

## ESEMPI

### Esempio 1: importazione di un contesto da un AzureRmProfile
```
PS C:\> Import-AzureRmContext -AzureContext (Add-AzureRmAccount)

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

Questo esempio importa un contesto da un PSAzureProfile passato al cmdlet.

### Esempio 2: importazione di un contesto da un file JSON
```
PS C:\> Import-AzureRmContext -Path C:\test.json

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

Questo esempio seleziona un contesto da un file JSON passato al cmdlet.
Questo file JSON può essere creato da Import-AzureRmContext.

## PARAMETRI

### -AzureContext
Specifica il contesto Azure da cui viene letto il cmdlet.
Se non specifichi un contesto, questo cmdlet viene letto dal contesto predefinito locale.

```yaml
Type: AzureRmProfile
Parameter Sets: InMemoryProfile
Aliases: Profile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path
Specifica il percorso delle informazioni sul contesto salvate tramite Save-AzureRMContext.

```yaml
Type: String
Parameter Sets: ProfileFromDisk
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confermare
Richiede la conferma prima di eseguire il cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa succede se il cmdlet viene eseguito.
Il cmdlet non viene eseguito.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

## INGRESSI

### Microsoft. Azure. Commands. Common. Authentication. Models. AzureRMProfile
System. String

## OUTPUT

### Microsoft. Azure. Commands. profile. Models. PSAzureProfile

## Note

## COLLEGAMENTI CORRELATI

