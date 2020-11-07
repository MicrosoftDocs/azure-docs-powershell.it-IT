---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3f5fbef7c67676f16793b63a8448517ca24aa7e5
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "93859310"
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

### ESEMPIO 1
```
Get-AzsNetworkAdminOverview
```

Panoramica dell'amministratore di rete.

### ESEMPIO 2
```
(Get-AzsNetworkAdminOverview).PublicIpAddressUsage
```

Ottenere l'utilizzo di indirizzi IP pubblici.

## PARAMETRI

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

### Microsoft. AzureStack. Management. Network. admin. Models. AdminOverview

## Note

## COLLEGAMENTI CORRELATI
