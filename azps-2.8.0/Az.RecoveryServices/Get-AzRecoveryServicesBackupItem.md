---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 2dfc4b8fd0491a9f8c2200876609ab0a8cb00cce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855749"
---
# Get-AzRecoveryServicesBackupItem

## Sinossi

Ottiene gli elementi da un contenitore nel backup.

## SINTASSI

### GetItemsForContainer (impostazione predefinita)

```
Get-AzRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetItemsForVault

```
Get-AzRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetItemsForPolicy

```
Get-AzRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>] [[-DeleteState] <ItemDeleteState>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione

Il cmdlet **Get-AzRecoveryServicesBackupItem** ottiene gli elementi in un contenitore o un valore in Azure Backup e lo stato di protezione degli elementi.
Un contenitore registrato in un Vault di servizi di ripristino di Azure può avere uno o più elementi che possono essere protetti.
Per le macchine virtuali di Azure può essere presente un solo elemento di backup nel contenitore della macchina virtuale.
Imposta il contesto del Vault usando il parametro-VaultId.

## ESEMPI

### Esempio 1: ottenere un elemento da un contenitore di backup

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM -VaultId $vault.ID
```

Il primo comando ottiene il contenitore di tipo AzureVM e lo archivia nella variabile $Container.
Il secondo comando ottiene l'elemento di backup denominato V2VM in $Container e lo archivia nella variabile $BackupItem.

## PARAMETRI

### -BackupManagementType

Specifica il tipo di gestione del backup.
I valori accettabili per questo parametro sono i seguenti:

- AzureVM
- Marte
- SCDPM
- AzureBackupServer
- AzureSQL
- AzureStorage
- AzureWorkload

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: GetItemsForVault
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Contenitore

Specifica un oggetto contenitore da cui questo cmdlet ottiene gli elementi di backup.
Per ottenere un **AzureRmRecoveryServicesBackupContainer** , usare il cmdlet **Get-AzRecoveryServicesBackupContainer** .

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: GetItemsForContainer
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -DeleteState
Specifica il DeleteState dell'elemento i valori accettabili per questo parametro sono i seguenti:

- ToBeDeleted
- NotDeleted

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemDeleteState
Parameter Sets: (All)
Aliases:
Accepted values: ToBeDeleted, NotDeleted

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome

Specifica il nome del contenitore.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Policy

Oggetto Criteri di protezione.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: GetItemsForPolicy
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProtectionState

Specifica lo stato di protezione.
I valori accettabili per questo parametro sono i seguenti:

- IRPending.
La sincronizzazione iniziale non è stata avviata e non è ancora disponibile un punto di recupero.
- Protetta.
La protezione è in corso.
- ProtectionError.
Si è verificato un errore di protezione.
- ProtectionStopped.
La protezione è disabilitata.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemProtectionState
Parameter Sets: (All)
Aliases:
Accepted values: IRPending, ProtectionError, Protected, ProtectionStopped

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProtectionStatus

Specifica lo stato di protezione complessivo di un elemento nel contenitore.
I valori accettabili per questo parametro sono i seguenti:

- Sano
- Malsano

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemProtectionStatus
Parameter Sets: (All)
Aliases:
Accepted values: Healthy, Unhealthy

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultId

ID ARM dell'archivio servizi di ripristino.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WorkloadType

Specifica il tipo di carico di lavoro.
I valori accettabili per questo parametro sono i seguenti:

- AzureVM
- AzureSQLDatabase
- AzureFiles
- MSSQL

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: GetItemsForContainer, GetItemsForVault
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CommonParameters

Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. ContainerBase

### System. String

## OUTPUT

### Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. ItemBase

## Note

## COLLEGAMENTI CORRELATI

[Backup-AzRecoveryServicesBackupItem](./Backup-AzRecoveryServicesBackupItem.md)

[Disable-AzRecoveryServicesBackupProtection](./Disable-AzRecoveryServicesBackupProtection.md)

[Get-AzRecoveryServicesBackupRecoveryPoint](./Get-AzRecoveryServicesBackupRecoveryPoint.md)

[Ripristinare-AzRecoveryServicesBackupItem](./Restore-AzRecoveryServicesBackupItem.md)
