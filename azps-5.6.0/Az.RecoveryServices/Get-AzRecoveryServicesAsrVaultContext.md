---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 62f27b43158f8b01abc7be48cab93f4bb957258b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958078"
---
# Get-AzRecoveryServicesAsrVaultContext

## SYNOPSIS
Recupera le informazioni delle impostazioni del Vault di Ripristino per il Vault dei servizi di ripristino.

## SINTASSI

```
Get-AzRecoveryServicesAsrVaultContext [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Get-AzRecoveryServicesAsrVaultContext** ottiene le informazioni delle impostazioni del vault ASR relative al vault dei servizi di ripristino.

## ESEMPI

### Esempio 1
```
PS C:\> $VaultSettings = Get-AzRecoveryServicesAsrVaultContext
```

Recupera le impostazioni del vault ASR per il vault dei Servizi di ripristino attualmente attivi (nella sessione di PowerShell).

## PARAMETERS

### -DefaultProfile
Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.

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
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Nessuno

## OUTPUT

### Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings

## NOTE

## COLLEGAMENTI CORRELATI
