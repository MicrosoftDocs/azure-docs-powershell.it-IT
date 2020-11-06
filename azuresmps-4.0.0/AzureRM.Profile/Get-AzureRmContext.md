---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 914b75e3952f7841aaf3ff505f51f7b4ebdc6044
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491170"
---
# Get-AzureRmContext

## Sinossi
Ottiene i metadati usati per autenticare le richieste di gestione risorse di Azure.

## SINTASSI

```
Get-AzureRmContext [<CommonParameters>]
```

## Descrizione
Il cmdlet Get-AzureRmContext ottiene i metadati correnti usati per autenticare le richieste di gestione risorse di Azure.

Questo cmdlet consente di ottenere l'account di Active Directory, il tenant di Active Directory, l'abbonamento Azure e l'ambiente Azure di destinazione.
I cmdlet di Azure Resource Manager usano queste impostazioni per impostazione predefinita quando si effettuano richieste di gestione risorse di Azure.

## ESEMPI

### Esempio 1: recupero del contesto corrente
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmContext

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

In questo esempio, stiamo accedendo al nostro account con un abbonamento a Azure usando Add-AzureRmAccount e quindi stiamo ottenendo il contesto della sessione corrente chiamando Get-AzureRmContext.

## PARAMETRI

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

### PSAzureContext
Questo cmdlet restituisce l'account, il tenant e l'abbonamento usati dai cmdlet di Azure Resource Manager.

## Note

## COLLEGAMENTI CORRELATI

[Set-AzureRMContext]()

