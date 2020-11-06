---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrazuretoazurediskreplicationconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
ms.openlocfilehash: 542e75ed0e6531f5778f9793b678b42f953c15d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508071"
---
# New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig

## Sinossi
Crea un oggetto di mapping del disco per i dischi di una macchina virtuale Azure da replicare.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri <String> -LogStorageAccountId <String>
 -RecoveryAzureStorageAccountId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Descrizione
Crea un oggetto di mapping del disco che esegue il mapping di un disco di una macchina virtuale di Azure all'account di archiviazione della cache e dell'account di archiviazione di destinazione (area di ripristino) da usare per replicare il disco.

## ESEMPI

### Esempio 1
```
PS C:\> New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri  $vhdUri -RecoveryAzureStorageAccountId $recoveryStorageAccountId -LogStorageAccountId $logStorageAccountId
```

Creare un oggetto di mapping del disco per i dischi di una macchina virtuale di Azure da replicare. Usato durante Azure in Azure per abilitare e proteggere l'operazione.

## PARAMETRI

### -Confermare
Richiede la conferma prima di eseguire il cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LogStorageAccountId
Specifica l'ID dell'account di archiviazione del log o della cache da usare per archiviare i registri di replica.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryAzureStorageAccountId
Specifica l'ID dell'account di archiviazione di Azure a cui eseguire la replica.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VhdUri
Specifica l'URI VHD del disco a cui corrisponde il mapping.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa succede se il cmdlet viene eseguito.
Il cmdlet non viene eseguito.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

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

### Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig

## Note

## COLLEGAMENTI CORRELATI
