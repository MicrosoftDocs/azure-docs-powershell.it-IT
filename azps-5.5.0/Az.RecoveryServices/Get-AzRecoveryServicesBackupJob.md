---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: cc8b9017180c431caabc31970877d9fe0e4c346a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183919"
---
# Get-AzRecoveryServicesBackupJob

## SYNOPSIS

Recupera i processi di backup.

## SINTASSI

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
  [-UseSecondaryRegion] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE

Il cmdlet **Get-AzRecoveryServicesBackupJob** ottiene i processi di Backup di Azure per un vault specifico.
Impostare il contesto del vault usando il parametro -VaultId.

## ESEMPI

### Esempio 1: Ottenere tutti i processi in corso

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Joblist = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> $Joblist[0]

WorkloadName     Operation            Status               StartTime                 EndTime
------------     ---------            ------               ---------                 -------
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

Il primo comando ottiene lo stato di un processo in corso come matrice e quindi lo archivia nella $Joblist variabile.
Il secondo comando visualizza il primo elemento della $Joblist matrice.

### Esempio 2: Ottenere tutti i processi non riusciti negli ultimi 7 giorni

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed -VaultId $vault.ID
```

Questo comando recupera i processi non riusciti dell'ultima settimana nel Vault.
Il *parametro From* specifica un'ora di sette giorni nel passato specificato in UTC.
Il comando non specifica un valore per il *parametro To.*
Di conseguenza, usa il valore predefinito dell'ora corrente.

### Esempio 3: Ottenere un processo in corso e attendere il completamento

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

Questo script esegue il polling del primo processo attualmente in corso finché non viene completato.

Nota: è possibile usare il cmdlet **Wait-AzRecoveryServicesBackupJob per** attendere il completamento di un processo di backup di Azure invece del ciclo While.

### Esempio 4: Ottenere tutti i processi AzureVM negli ultimi 2 giorni, che sono stati completati correttamente

```powershell
$vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
$Jobs = Get-AzRecoveryServicesBackupJob  -VaultId $vault.ID  -Status Completed -From (Get-Date).AddDays(-2).ToUniversalTime() -BackupManagementType AzureVM
```
Il primo cmdlet recupera l'oggetto vault. Il secondo cmdlet archivia tutti i processi AzureVM nel vault specificato completato negli ultimi 2 giorni per $jobs. Modificare il valore del parametro BackupManagementType in MAB per recuperare i processi dell'agente MAB.

## PARAMETERS

### -BackupManagementType

Classe di risorse protetta. Attualmente i valori supportati per questo cmdlet sono AzureVM, AzureStorage, AzureWorkload, MAB.

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

### -Da

Specifica l'inizio, come oggetto **DateTime,** di un intervallo di tempo per i processi che questo cmdlet ottiene.
Per ottenere un **oggetto DateTime,** usare il cmdlet **Get-Date.**
Per altre informazioni sugli **oggetti DateTime,** digitare `Get-Help Get-Date` .
Utilizzare il formato UTC per le date.

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

Specifica l'ID di un processo che riceve questo cmdlet.
L'ID è la proprietà JobId di un **oggetto Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase.**

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

Specifica un'operazione dei processi che riceve questo cmdlet.
I valori accettabili per questo parametro sono:

- Backup
- ConfigureBackup
- DeleteBackupData
- DisableBackup
- Ripristina
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

Specifica lo stato dei processi che riceve questo cmdlet.
I valori accettabili per questo parametro sono:

- InProgress
- Operazione non riuscita
- Annullato
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

### -A

Specifica la fine, come oggetto **DateTime,** di un intervallo di tempo per i processi che questo cmdlet ottiene.
Il valore predefinito è l'ora di sistema corrente.
Se si specifica questo parametro, è necessario specificare anche **il parametro -From.**
Utilizzare il formato UTC per le date.

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

ARM ID del Vault dei servizi di ripristino.

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
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### System.String

## OUTPUT

### Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase

## NOTE

## COLLEGAMENTI CORRELATI

[Get-AzRecoveryServicesBackupJobDetail](./Get-AzRecoveryServicesBackupJobDetail.md)

[Stop-AzRecoveryServicesBackupJob](./Stop-AzRecoveryServicesBackupJob.md)

[Wait-AzRecoveryServicesBackupJob](./Wait-AzRecoveryServicesBackupJob.md)
