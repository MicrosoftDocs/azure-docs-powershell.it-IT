---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 819cdc45e75c15c38c9ae28c583ac3c73e54f4ac
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859945"
---
# Get-AzsComputeQuota

## Sinossi
Restituisce le quote che specificano i limiti di quota per gli oggetti COMPUTE.

## SINTASSI

### Elenco (impostazione predefinita)
```
Get-AzsComputeQuota [-Location <String>] [<CommonParameters>]
```

### Ottieni
```
Get-AzsComputeQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### ResourceId
```
Get-AzsComputeQuota -ResourceId <String> [<CommonParameters>]
```

## Descrizione
Ottenere un elenco di quote esistenti.

## ESEMPI

### --------------------------ESEMPIO 1--------------------------
```
Get-AzsComputeQuota -Location 'local'
```

Ottenere tutte le quote di calcolo nella posizione specificata.

### --------------------------ESEMPIO 2--------------------------
```
Get-AzsComputeQuota 'Default Quota'
```

Ottenere una quota di calcolo specifica.

## PARAMETRI

### -Posizione
{{Fill Location Description}}

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

### -Nome
Nome della quota.

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
ID risorsa.

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

### ComputeQuotaObject

## Note

## COLLEGAMENTI CORRELATI

