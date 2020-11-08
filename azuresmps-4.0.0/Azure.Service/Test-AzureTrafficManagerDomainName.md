---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 92E2409B-14BC-428F-8BAF-60D8DAFA5F57
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1adaafdfdd4331bbba86530eb532964430ed7c69
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023893"
---
# Test-AzureTrafficManagerDomainName

## Sinossi
Controlla se un nome di dominio è disponibile come profilo di gestione traffico.

## SINTASSI

```
Test-AzureTrafficManagerDomainName -DomainName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **test-AzureTrafficManagerDomainName** controlla se un nome di dominio è disponibile come profilo di Microsoft Azure Traffic Manager.
Se il nome di dominio è disponibile, questo cmdlet restituisce un valore di $True.

## ESEMPI

### Esempio 1: verificare se è disponibile un nome di dominio
```
PS C:\>Test-AzureTrafficManagerDomainName -DomainName "ContosoApp.trafficmanager.net"
$True
```

Questo comando controlla se il nome di dominio ContosoApp.trafficmanager.net è disponibile come profilo di gestione traffico.

## PARAMETRI

### -DomainName
Specifica il nome di dominio da testare.
È necessario includere la stringa seguente: 

. trafficmanager.net

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Specifica il profilo Azure da cui viene letto il cmdlet. Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

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

### System. Boolean
Questo cmdlet genera $True o $False.
Se il nome di dominio è disponibile, questo cmdlet restituisce un valore di $True.

## Note

## COLLEGAMENTI CORRELATI

