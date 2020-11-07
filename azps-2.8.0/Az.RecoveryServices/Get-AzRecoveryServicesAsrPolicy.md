---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 87d89766468008548db70c757ee173cd141dc946
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855797"
---
# Get-AzRecoveryServicesAsrPolicy

## Sinossi
Ottiene i criteri di replica ASR.

## SINTASSI

### Predefinito (impostazione predefinita)
```
Get-AzRecoveryServicesAsrPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByName
```
Get-AzRecoveryServicesAsrPolicy -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFriendlyName
```
Get-AzRecoveryServicesAsrPolicy -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzRecoveryServicesAsrPolicy** Ottiene l'elenco dei criteri di replica del ripristino del sito Azure configurati o di un criterio di replica specifico per nome.

## ESEMPI

### Esempio 1
```
PS C:\> $Policy = Get-AzRecoveryServicesAsrPolicy
```

Restituisce l'elenco dei criteri di replica

### Esempio 2
```
PS C:\>  Get-AzRecoveryServicesAsrPolicy -Name abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

Restituisce i criteri di replica con nome.

### Esempio 3
```
PS C:\> Get-AzRecoveryServicesAsrPolicy -FriendlyName abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

Restituisce i criteri di replica con il nome descrittivo specificato.

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

### -FriendlyName
Specifica il nome descrittivo dei criteri di replica ASR.

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Specifica il nome del criterio di replica ASR.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
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

### Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy

## Note

## COLLEGAMENTI CORRELATI

[New-AzRecoveryServicesAsrPolicy](./New-AzRecoveryServicesAsrPolicy.md)

[Remove-AzRecoveryServicesAsrPolicy](./Remove-AzRecoveryServicesAsrPolicy.md)
