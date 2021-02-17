---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: cbe1160c691fe128f5f2950d728501b815294c05
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191343"
---
# Restore-AzRecoveryServicesBackupItem

## SYNOPSIS

Ripristina i dati e la configurazione per un elemento di backup nel punto di ripristino specificato. I parametri obbligatori variano in base al tipo di elemento di backup.
Lo stesso comando viene usato per ripristinare macchine virtuali di Azure, database in esecuzione in macchine virtuali di Azure e condivisioni file di Azure.

## SINTASSI

### AzureVMParameterSet (impostazione predefinita)
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-DiskEncryptionSetId <string>] [-RestoreToSecondaryRegion] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### AzureVMManagedDiskParameterSet
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-TargetResourceGroupName] <String>
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-DiskEncryptionSetId <string>] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AzureVMRestoreManagedAsUnmanaged
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-RestoreAsUnmanagedDisks] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AzureVMUnManagedDiskParameterSet
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-UseOriginalStorageAccount]
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AzureFileShareParameterSet
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-MultipleSourceFilePath <String[]>] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AzureWorkloadParameterSet
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase> [-RestoreToSecondaryRegion]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIZIONE

Il cmdlet **Restore-AzRecoveryServicesBackupItem** ripristina i dati e la configurazione per un elemento di Backup di Azure a un punto di ripristino specificato.

**Per il backup della macchina virtuale di Azure**

Con questo comando è possibile eseguire il backup delle macchine virtuali di Azure e ripristinare i dischi (gestiti e non gestiti). Con l'operazione di ripristino non viene ripristinata la macchina virtuale completa.
Se si tratta di una MACCHINA virtuale su disco gestita, è necessario specificato un gruppo di risorse di destinazione nella posizione in cui vengono mantenuti i dischi ripristinati. Quando si specifica il gruppo di risorse di destinazione, se gli snapshot sono presenti nel gruppo di risorse specificato nei criteri di backup, l'operazione di ripristino sarà immediata e i dischi verranno creati dagli snapshot locali e mantenuti nel gruppo di risorse di destinazione. È anche disponibile un'opzione per ripristinarli come dischi non gestiti, ma si sfruttano i dati presenti nel vault dei servizi di ripristino di Azure e quindi saranno molto più lenti. La configurazione della macchina virtuale e il modello di distribuzione che può essere usato per creare la macchina virtuale dai dischi ripristinati verranno scaricati nell'account di archiviazione specificato.
Se si tratta di una MACCHINA virtuale disco non gestita, gli snapshot sono presenti nell'account di archiviazione originale del disco e/o nel vault dei servizi di ripristino. Se l'utente offre la possibilità di usare l'account di archiviazione originale per il ripristino, è possibile usare il ripristino immediato. In caso contrario, i dati vengono recuperati dall'vault dei servizi di ripristino di Azure e i dischi vengono creati nell'account di archiviazione specificato insieme alla configurazione della macchina virtuale e al modello di distribuzione.

> [!IMPORTANT]
> Per impostazione predefinita, il backup della macchina virtuale di Azure backup tutti i dischi. È possibile eseguire il backup selettivo dei dischi rilevanti usando i parametri exclusionList o InclusionList durante Enable-Backup. L'opzione per ripristinare i dischi in modo selettivo è disponibile solo se ne è stato eseguito il backup in modo selettivo.

Per altre informazioni, vedere i diversi set di parametri possibili e il testo dei parametri.

> [!NOTE]
> Se si usa il parametro -VaultId, deve essere usato anche il parametro -VaultLocation.

**Per il backup della condivisione file di Azure**

È possibile ripristinare un'intera condivisione file o specifici/più file/cartelle nella condivisione. È possibile ripristinare il percorso originale o in un percorso alternativo.

**Per i carichi di lavoro di Azure**

È possibile ripristinare le SQL all'interno delle macchine virtuali di Azure


## ESEMPI

### Esempio 1: Ripristinare i dischi di un disco gestito di cui è stato eseguito il backup da un determinato punto di ripristino

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType "AzureVM" -WorkloadType "AzureVM" -Name "V2VM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetResourceGroupName "Target_RG" -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

Il primo comando recupera il vault dei servizi di ripristino e lo archivia in $vault variabile.
Il secondo comando recupera l'elemento di backup del tipo AzureVM, il nome "V2VM" e lo archivia nella variabile $BackupItem variabile.
Il terzo comando ottiene la data di sette giorni prima e quindi la archivia nella $StartDate variabile.
Il quarto comando ottiene la data corrente e la archivia nella $EndDate variabile.
Il quinto comando ottiene un elenco di punti di ripristino per l'elemento di backup specifico filtrato per $StartDate e $EndDate.
L'ultimo comando ripristina tutti i dischi nel gruppo di risorse di destinazione Target_RG e quindi fornisce le informazioni di configurazione della macchina virtuale e il modello di distribuzione nell'account di archiviazione DestAccount nel gruppo di risorse DestRG.

### Esempio 2: Ripristinare i dischi specificati di un backup della MACCHINA virtuale di Azure su disco gestito da un determinato punto di ripristino

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType "AzureVM" -WorkloadType "AzureVM" -Name "V2VM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $restoreDiskLUNs = ("0", "1")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetResourceGroupName "Target_RG" -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -RestoreDiskList $restoreDiskLUNs -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

Il primo comando recupera il vault dei servizi di ripristino e lo archivia in $vault variabile.
Il secondo comando recupera l'elemento di backup del tipo AzureVM, il nome "V2VM" e lo archivia nella variabile $BackupItem variabile.
Il terzo comando ottiene la data di sette giorni prima e quindi la archivia nella $StartDate variabile.
Il quarto comando ottiene la data corrente e la archivia nella $EndDate variabile.
Il quinto comando ottiene un elenco di punti di ripristino per l'elemento di backup specifico filtrato per $StartDate e $EndDate.
Il sesto comando archivia l'elenco dei dischi da ripristinare nella variabile restoreDiskLUN.
L'ultimo comando ripristina i dischi specificati, dei LUN specificati, nel Target_RG di risorse di destinazione e quindi fornisce le informazioni di configurazione della macchina virtuale e il modello di distribuzione nell'account di archiviazione DestAccount nel gruppo di risorse DestRG.

### Esempio 3: Ripristinare i dischi di una macchina virtuale gestita come dischi non gestiti

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType "AzureVM" -WorkloadType "AzureVM" -Name "V2VM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -RestoreAsUnmanagedDisks -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

Il primo comando recupera il vault RecoveryServices e lo archivia in $vault variabile.
Il secondo comando recupera l'elemento di backup e quindi lo archivia nella $BackupItem variabile.
Il terzo comando ottiene la data di sette giorni prima e quindi la archivia nella $StartDate variabile.
Il quarto comando ottiene la data corrente e la archivia nella $EndDate variabile.
Il quinto comando ottiene un elenco di punti di ripristino per l'elemento di backup specifico filtrato per $StartDate e $EndDate.
Il sesto comando ripristina i dischi come dischi non gestiti.

### Esempio 4: Ripristinare una macchina virtuale non gestita come dischi non gestiti usando l'account di archiviazione originale

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -Name "UnManagedVM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -UseOriginalStorageAccount -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

Il primo comando recupera il vault RecoveryServices e lo archivia in $vault variabile.
Il secondo comando recupera l'elemento di backup e quindi lo archivia nella $BackupItem variabile.
Il terzo comando ottiene la data di sette giorni prima e quindi la archivia nella $StartDate variabile.
Il quarto comando ottiene la data corrente e la archivia nella $EndDate variabile.
Il quinto comando ottiene un elenco di punti di ripristino per l'elemento di backup specifico filtrato per $StartDate e $EndDate.
Il sesto comando ripristina i dischi come dischi non gestiti nei propri account di archiviazione originali

### Esempio 5: Ripristinare più file di un elemento AzureFileShare

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureStorage -WorkloadType AzureVM -VaultId $vault.ID -Name "fileshareitem"
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -VaultId $vault.ID
PS C:\> $files = ("file1.txt", "file2.txt")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -MultipleSourceFilePath $files -SourceFileType File -ResolveConflict Overwrite -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    fileshareitem   Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

Il primo comando recupera il vault dei servizi di ripristino e lo archivia in $vault variabile.
Il secondo comando recupera l'elemento di backup denominato fileshareitem e quindi lo archivia nella $BackupItem variabile.
Il terzo comando ottiene un elenco di punti di ripristino per l'elemento di backup specifico.
Il quarto comando specifica quali file ripristinare e archiviare in $files variabile.
L'ultimo comando ripristina i file specificati nella posizione originale.

### Esempio 6: Ripristinare un db SQL'interno di una macchina virtuale di Azure in un'altra macchina virtuale di destinazione per un punto di ripristino completo distinto

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureWorkload -WorkloadType MSSQL -VaultId $vault.ID -Name "MSSQLSERVER;model"
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $FullRP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $TargetInstance = Get-AzRecoveryServicesBackupProtectableItem -WorkloadType MSSQL -ItemType SQLInstance -Name "<SQLInstance Name>" -ServerName "<SQL VM name>" -VaultId $vault.ID
PS C:\> $AnotherInstanceWithFullConfig = Get-AzRecoveryServicesBackupWorkloadRecoveryConfig -RecoveryPoint $FullRP -TargetItem $TargetInstance -AlternateWorkloadRestore -VaultId $vault.ID
PS C:\> Restore-AzRecoveryServicesBackupItem -WLRecoveryConfig $AnotherInstanceWithLogConfig -VaultId $vault.ID
    WorkloadName       Operation        Status            StartTime                 EndTime          JobID
    ------------       ---------        ------            ---------                 -------          -----
    MSSQLSERVER/m...   Restore          InProgress        3/17/2019 10:02:45 AM                      3274xg2b-e4fg-5952-89b4-8cb566gc1748

```

### Esempio 7: Ripristinare un db SQL'interno di una macchina virtuale di Azure in un'altra macchina virtuale di destinazione per un punto di ripristino del log

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureWorkload -WorkloadType MSSQL -VaultId $vault.ID -Name "MSSQLSERVER;model"
PS C:\> $PointInTime = Get-Date -Date "2019-03-20 01:00:00Z"
PS C:\> $TargetInstance = Get-AzRecoveryServicesBackupProtectableItem -WorkloadType MSSQL -ItemType SQLInstance -Name "<SQLInstance Name>" -ServerName "<SQL VM name>" -VaultId $vault.ID
PS C:\> $AnotherInstanceWithLogConfig = Get-AzRecoveryServicesBackupWorkloadRecoveryConfig -PointInTime $PointInTime -Item $BackupItem -AlternateWorkloadRestore -VaultId $vault.ID
PS C:\> Restore-AzRecoveryServicesBackupItem -WLRecoveryConfig $AnotherInstanceWithLogConfig -VaultId $vault.ID
    WorkloadName     Operation      Status           StartTime                 EndTime           JobID
    ------------     ---------      ------           ---------                 -------           -----
    MSSQLSERVER/m... Restore        InProgress       3/17/2019 10:02:45 AM                       3274xg2b-e4fg-5952-89b4-8cb566gc1748

```

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

### -MultipleSourceFilePath
Usato per il ripristino di più file da una condivisione file. Percorsi degli elementi da ripristinare nella condivisione file.

```yaml
Type: System.String[]
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryPoint

Specifica il punto di ripristino in cui ripristinare l'elemento di backup.
Per ottenere un **oggetto AzureRmRecoveryServicesBackupRecoveryPoint,** usare il cmdlet **Get-AzRecoveryServicesBackupRecoveryPoint.**

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: AzureVMParameterSet, AzureFileParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResolveConflict

Se l'elemento ripristinato è presente anche nella destinazione, usare questa opzione per indicare se sovrascriverlo o meno.
I valori accettabili per questo parametro sono:

- Sovrascrivi
- Ignora

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RestoreFSResolveConflictOption
Parameter Sets: AzureFileParameterSet
Aliases:
Accepted values: Overwrite, Skip

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestoreAsUnmanagedDisks
Usare questa opzione per specificare di ripristinare come dischi non gestiti

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMRestoreAsUnmanaged
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestoreDiskList
Specificare i dischi da ripristinare della macchina virtuale di cui è stato eseguito il backup

```yaml
Type: System.String[]
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestoreOnlyOSDisk
Usare questo parametro per ripristinare solo i dischi del sistema operativo di una macchina virtuale di cui è stato eseguito il backup

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceFilePath

Usato per il ripristino di un elemento specifico da una condivisione file. Percorso dell'elemento da ripristinare nella condivisione file.

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceFileType

Usato per il ripristino di un elemento specifico da una condivisione file. Il tipo di elemento da ripristinare nella condivisione file.
I valori accettabili per questo parametro sono:

- File
- Directory

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SourceFileType]
Parameter Sets: AzureFileParameterSet
Aliases:
Accepted values: File, Directory

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountName

Specifica il nome dell'account di archiviazione di destinazione nell'abbonamento.
Durante il processo di ripristino, questo cmdlet archivia i dischi e le informazioni di configurazione in questo account di archiviazione.

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountResourceGroupName

Specifica il nome del gruppo di risorse che contiene l'account di archiviazione di destinazione nella sottoscrizione.
Durante il processo di ripristino, questo cmdlet archivia i dischi e le informazioni di configurazione in questo account di archiviazione.

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetFileShareName

Condivisione file in cui è necessario ripristinare la condivisione file.

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetFolder

La cartella in cui è necessario ripristinare la condivisione file all'interno di TargetFileShareName. Se il backup del contenuto deve essere ripristinato in una cartella radice, assegnare i valori della cartella di destinazione come stringa vuota.

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetResourceGroupName

Gruppo di risorse in cui vengono ripristinati i dischi gestiti. Applicabile al backup della macchina virtuale con dischi gestiti

```yaml
Type: System.String
Parameter Sets: AzureVMTargetRGParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetStorageAccountName

Account di archiviazione in cui è necessario ripristinare la condivisione file.

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseOriginalStorageAccount

Usare questa opzione se i dischi del punto di ripristino devono essere ripristinati nell'account di archiviazione originale.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskEncryptionSetId 

ID DES per crittografare i dischi ripristinati.

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet, AzureVMManagedDiskParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestoreToSecondaryRegion

Usare questo parametro per attivare il ripristino dell'area incrociata nell'area secondaria.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureIaasVM
Aliases:

Required: False
Position: Named
Default value: False
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

### -VaultLocation

Posizione del Vault dei servizi di ripristino.

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

### -WLRecoveryConfig

Configurazione di ripristino

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase
Parameter Sets: AzureWorkloadParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Confirm

Chiede conferma prima di eseguire il cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

Mostra cosa accadrebbe se il cmdlet viene eseguito. 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### System.String

### Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase

## OUTPUT

### Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase

## NOTE

## COLLEGAMENTI CORRELATI

[Backup-AzRecoveryServicesBackupItem](./Backup-AzRecoveryServicesBackupItem.md)

[Get-AzRecoveryServicesBackupItem](./Get-AzRecoveryServicesBackupItem.md)

[Get-AzRecoveryServicesBackupRecoveryPoint](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
