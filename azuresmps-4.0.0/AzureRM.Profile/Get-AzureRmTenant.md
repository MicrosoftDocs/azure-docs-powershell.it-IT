---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2cabb88c490c7fdea56fd5ffde280cfd55bc8f3d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491165"
---
# Get-AzureRmTenant

## Sinossi
Ottiene i tenant autorizzati per l'utente corrente.

## SINTASSI

```
Get-AzureRmTenant [[-TenantId] <String>] [<CommonParameters>]
```

## Descrizione
Il cmdlet Get-AzureRmTenant ottiene i tenant autorizzati per l'utente corrente.

## ESEMPI

### Esempio 1: recupero di tutti i tenant
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmTenant

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com

TenantId : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Domain   : microsoft.com
```

Questo esempio Mostra come ottenere tutti i tenant autorizzati di un account Azure.

### Esempio 2: ottenere un tenant specifico
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com
```

Questo esempio Mostra come ottenere uno specifico tenant autorizzato di un account Azure.

## PARAMETRI

### -ID tenant
Specifica l'ID del tenant ottenuto da questo cmdlet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Domain, Tenant

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

### PSAzureTenant
Questo cmdlet restituisce l'ID tenant e le informazioni sul dominio associato per i tenant autorizzati per l'account corrente.

## Note

## COLLEGAMENTI CORRELATI

