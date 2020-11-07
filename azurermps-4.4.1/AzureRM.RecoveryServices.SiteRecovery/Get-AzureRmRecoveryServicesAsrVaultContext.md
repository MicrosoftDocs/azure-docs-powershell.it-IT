---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 0a809f9ef3d3c89edc7571b9bb7b7cc2f03e043b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688253"
---
# Get-AzureRmRecoveryServicesAsrVaultContext

## Sinossi
Ottiene le informazioni sulle impostazioni del Vault ASR per il Vault di servizi di ripristino.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Get-AzureRmRecoveryServicesAsrVaultContext [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureRmRecoveryServicesAsrVaultContext** ottiene le informazioni sulle impostazioni del Vault ASR correlate al Vault di servizi di ripristino.

## ESEMPI

### Esempio 1
```
PS C:\> $VaultSettings = Get-AzureRmRecoveryServicesAsrVaultContext
```

Ottiene le impostazioni del Vault ASR per il Vault dei servizi di ripristino attualmente attivo (nella sessione di PowerShell).

## PARAMETRI

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno

## OUTPUT

### Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings

## Note

## COLLEGAMENTI CORRELATI

