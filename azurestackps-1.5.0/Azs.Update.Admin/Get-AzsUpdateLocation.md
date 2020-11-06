---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a9234cb73b1f9c3652827293ae2813f78d7ce336
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491553"
---
# Get-AzsUpdateLocation

## Sinossi
Ottenere l'elenco delle posizioni di aggiornamento.

## SINTASSI

### Elenco (impostazione predefinita)
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [<CommonParameters>]
```

### Ottieni
```
Get-AzsUpdateLocation [-Name <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### ResourceId
```
Get-AzsUpdateLocation -ResourceId <String> [<CommonParameters>]
```

## Descrizione
Ottenere l'elenco delle posizioni di aggiornamento. I percorsi restituiti possono essere usati per ottenere gli aggiornamenti disponibili in una determinata posizione usando Get-AzsUpdate.

## ESEMPI

### --------------------------ESEMPIO 1--------------------------
```
Get-AzsUpdateLocation
```

Ottenere l'elenco delle posizioni di aggiornamento.

## PARAMETRI

### -Nome
Il nome del percorso di aggiornamento.

```yaml
Type: String
Parameter Sets: Get
Aliases: Location

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Gruppo risorse in cui si trova la risorsa.

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
ID risorsa.

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

### Microsoft. AzureStack. Management. Update. admin. Models. UpdateLocation

## Note

## COLLEGAMENTI CORRELATI

