---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 623acc7d96fc6c3dc4f1496f42a53bf276f8e778
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032840"
---
# Get-AzRecoveryServicesBackupJob

## Sinossi

Ottiene i processi di backup.

## SINTASSI

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione

Il cmdlet **Get-AzRecoveryServicesBackupJob** ottiene i processi di backup di Azure per un Vault specifico.
Imposta il contesto del Vault usando il parametro-VaultId.

## ESEMPI

### Esempio 1: ottenere tutti i processi in corso

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Joblist = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> $Joblist[0]

WorkloadName     Operation            Status               StartTime                 EndTime
------------     ---------            ------               ---------                 -------
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

Il primo comando ottiene lo stato di un processo in corso come matrice e lo archivia nella variabile $Joblist.
Il secondo comando Visualizza il primo elemento nella matrice $Joblist.

### Esempio 2: ottenere tutti i processi non riusciti negli ultimi 7 giorni

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed -VaultId $vault.ID
```

Questo comando restituisce i processi non riusciti dell'ultima settimana nel Vault.
Il parametro *from* specifica un tempo di sette giorni nel passato specificato in UTC.
Il comando non specifica un valore per il parametro *to* .
Di conseguenza, usa il valore predefinito dell'ora corrente.

### Esempio 3: ottenere un processo in corso e attendere il completamento

```powershell
$vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
$Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
$Job = $Jobs[0]
While ( $Job.Status -ne Completed ) {
    Write-Host -Object "Waiting for completion..."
    Start-Sleep -Seconds 10
    $Job = Get-AzRecoveryServicesBackupJob -Job $Job -VaultId $vault.ID
}
Write-Host -Object "Done!"

Waiting for completion... 
Waiting for completion... 
Waiting for completion... 
Done!
```

Questo script esegue il polling del primo processo che è attualmente in corso fino al completamento del processo.

Nota: è possibile usare il cmdlet **wait-AzRecoveryServicesBackupJob** per attendere il completamento di un processo di backup di Azure invece del ciclo while.

### Esempio 4: ottenere tutti i processi di AzureVM negli ultimi 2 giorni che sono stati completati correttamente

```powershell
$vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
$Jobs = Get-AzRecoveryServicesBackupJob  -VaultId $vault.ID  -Status Completed -From (Get-Date).AddDays(-2).ToUniversalTime() -BackupManagementType AzureVM
```
Il primo cmdlet recupera l'oggetto Vault. Il secondo cmdlet archivia tutti i processi di AzureVM nella volta specificata, che sono stati completati negli ultimi 2 giorni per $jobs. Cambiare il valore del parametro BackupManagementType in MAB per recuperare i processi di agente MAB.

## PARAMETRI

### -BackupManagementType

Classe di risorse protette. Attualmente i valori supportati per questo cmdlet sono AzureVM, AzureStorage, AzureWorkload, MAB.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureStorage, AzureWorkload, MAB

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -Da

Specifica l'inizio, come oggetto **DateTime** , di un intervallo di tempo per i processi ottenuti da questo cmdlet.
Per ottenere un oggetto **DateTime** , usare il cmdlet **get-date** .
Per altre informazioni sugli oggetti **DateTime** , digitare `Get-Help Get-Date` .
Usare il formato UTC per le date.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Job

Specifica il processo da ottenere.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobId

Specifica l'ID di un processo ottenuto da questo cmdlet.
L'ID è la proprietà JobId di un oggetto **Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. JobBase** .

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Operazione

Specifica un'operazione dei processi ottenuti da questo cmdlet.
I valori accettabili per questo parametro sono i seguenti:

- Backup
- ConfigureBackup
- DeleteBackupData
- DisableBackup
- Ripristinare
- BackupDataMove

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobOperation]
Parameter Sets: (All)
Aliases:
Accepted values: Backup, Restore, ConfigureBackup, DisableBackup, DeleteBackupData

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Stato

Specifica lo stato dei processi ottenuti da questo cmdlet.
I valori accettabili per questo parametro sono i seguenti:

- InProgress
- Fallito
- Annullata
- Annullamento
- Completato
- CompletedWithWarnings

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobStatus]
Parameter Sets: (All)
Aliases:
Accepted values: InProgress, Cancelling, Cancelled, Completed, CompletedWithWarnings, Failed

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -To

Specifica la fine, come oggetto **DateTime** , di un intervallo di tempo per i processi ottenuti da questo cmdlet.
Il valore predefinito è l'ora di sistema corrente.
Se specifichi questo parametro, devi anche specificare il parametro **-from** .
Usare il formato UTC per le date.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
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

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### System. String

## OUTPUT

### Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. JobBase

## Note

## COLLEGAMENTI CORRELATI

[Get-AzRecoveryServicesBackupJobDetail](./Get-AzRecoveryServicesBackupJobDetail.md)

[Stop-AzRecoveryServicesBackupJob](./Stop-AzRecoveryServicesBackupJob.md)

[Wait-AzRecoveryServicesBackupJob](./Wait-AzRecoveryServicesBackupJob.md)
