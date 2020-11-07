---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: e5bb8a19cb616c9696ec224d8f1d9d25678d9e47
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855757"
---
# Get-AzRecoveryServicesAsrVaultContext

## Sinossi
Ottiene le informazioni sulle impostazioni del Vault ASR per il Vault di servizi di ripristino.

## SINTASSI

```
Get-AzRecoveryServicesAsrVaultContext [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzRecoveryServicesAsrVaultContext** ottiene le informazioni sulle impostazioni del Vault ASR correlate al Vault di servizi di ripristino.

## ESEMPI

### Esempio 1
```
PS C:\> $VaultSettings = Get-AzRecoveryServicesAsrVaultContext
```

Ottiene le impostazioni del Vault ASR per il Vault dei servizi di ripristino attualmente attivo (nella sessione di PowerShell).

## PARAMETRI

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno

## OUTPUT

### Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings

## Note

## COLLEGAMENTI CORRELATI
