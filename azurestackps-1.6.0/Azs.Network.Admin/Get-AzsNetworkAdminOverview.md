---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d3c564a004c006a9fd77c6fb5cef034b402b0b1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93685238"
---
# Get-AzsNetworkAdminOverview

## Sinossi
Ottenere una panoramica dello stato del provider di risorse di rete.

## SINTASSI

```
Get-AzsNetworkAdminOverview [<CommonParameters>]
```

## Descrizione
Ottenere una panoramica dello stato del provider di risorse di rete. Le singole proprietà includono un conteggio dettagliato dell'uso delle risorse e dell'integrità per componente.

## ESEMPI

### --------------------------ESEMPIO 1--------------------------
```
Get-AzsNetworkAdminOverview
```

Panoramica dell'amministratore di rete.

### --------------------------ESEMPIO 2--------------------------
```
(Get-AzsNetworkAdminOverview).PublicIpAddressUsage
```

Ottenere l'utilizzo di indirizzi IP pubblici.

## PARAMETRI

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

### Microsoft. AzureStack. Management. Network. admin. Models. AdminOverview

## Note

## COLLEGAMENTI CORRELATI

