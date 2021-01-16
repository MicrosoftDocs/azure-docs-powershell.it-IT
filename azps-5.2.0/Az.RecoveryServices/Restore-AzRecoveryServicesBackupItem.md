---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 593603e212c2ebfd709e5f4c70797ea369877b76
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360734"
---
# Restore-AzRecoveryServicesBackupItem

## Sinossi

Ripristina i dati e la configurazione per un elemento di backup nel punto di recupero specificato. I parametri obbligatori variano a seconda del tipo di elemento di backup.
Lo stesso comando viene usato per ripristinare le macchine virtuali di Azure, i database in cui sono in uso anche le macchine virtuali Azure e le condivisioni di file Azure.

## SINTASSI

### AzureVMParameterSet (impostazione predefinita)
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### AzureVMManagedDiskParameterSet
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-TargetResourceGroupName] <String>
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AzureVMRestoreManagedAsUnmanaged
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-RestoreAsUnmanagedDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AzureVMUnManagedDiskParameterSet
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-UseOriginalStorageAccount]
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AzureFileShareParameterSet
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-MultipleSourceFilePath <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AzureWorkloadParameterSet
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione

Il cmdlet **Restore-AzRecoveryServicesBackupItem** Ripristina i dati e la configurazione per un elemento di backup di Azure in un punto di recupero specificato.

**Per il backup di Azure VM**

Puoi eseguire il backup di macchine virtuali di Azure e ripristinare dischi (gestiti e non gestiti) usando questo comando. L'operazione di ripristino non ripristina la macchina virtuale completa.
Se si tratta di una VM disco gestito, è necessario specificare un gruppo di risorse di destinazione in cui vengono conservati i dischi ripristinati. Quando viene specificato il gruppo di risorse di destinazione, se gli snapshot sono presenti nel gruppo di risorse specificato in criteri di backup, l'operazione di ripristino sarà immediata e i dischi verranno creati da snapshot locali e conservati in un gruppo di risorse di destinazione. Esiste anche un'opzione per ripristinarli come dischi non gestiti, ma questa operazione sfrutterà i dati presenti in Azure Recovery Services Vault e quindi sarà molto più lenta. La configurazione della VM e del modello di distribuzione, che può essere usata per creare VM fuori dai dischi ripristinati, verrà scaricata nell'account di archiviazione specificato.
Se si tratta di una VM disco non gestita, gli snapshot sono presenti nell'account di archiviazione originale del disco e/o nell'archivio dei servizi di ripristino. Se l'utente concede l'opzione di usare l'account di archiviazione originale per il ripristino, è possibile fornire il ripristino istantaneo. In caso contrario, i dati vengono recuperati dal Vault di servizi di ripristino di Azure e i dischi vengono creati nell'account di archiviazione specificato insieme alla configurazione della VM e del modello di distribuzione.

> [!IMPORTANT]
> Per impostazione predefinita, il backup di Azure VM riporta tutti i dischi. È possibile eseguire il backup in modo selettivo dei dischi rilevanti usando i parametri di esclusione o inclusione durante enable-backup. L'opzione per ripristinare selettivamente i dischi è disponibile solo se è stato eseguito il backup in modo selettivo.

Per altre informazioni, fare riferimento a diversi possibili set di parametri e testo dei parametri.

> [!NOTE]
> Se viene usato il parametro-VaultId, deve essere usato anche il parametro VaultLocation.

**Per il backup di condivisione file Azure**

È possibile ripristinare un'intera condivisione file o file/cartelle specifici/multipli nella condivisione. È possibile ripristinare la posizione originale o in una posizione alternativa.

**Per i carichi di lavoro di Azure**

È possibile ripristinare SQL DBs in Azure VM


## ESEMPI

### Esempio 1: ripristinare i dischi di una VM di Azure disco gestito di cui è stato eseguito il backup da un punto di ripristino specifico

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

Il primo comando ottiene il Vault di servizi di ripristino e lo archivia in $vault variabile.
Il secondo comando ottiene l'elemento di backup di tipo AzureVM, del nome "V2VM" e lo archivia nella variabile $BackupItem.
Il terzo comando ottiene la data da sette giorni prima e lo archivia nella variabile $StartDate.
Il quarto comando ottiene la data corrente e lo archivia nella variabile $EndDate.
Il quinto comando consente di ottenere un elenco di punti di ripristino per l'elemento di backup specifico filtrato da $StartDate e $EndDate.
L'ultimo comando Ripristina tutti i dischi nel gruppo di risorse di destinazione Target_RG e quindi fornisce le informazioni di configurazione VM e il modello di distribuzione nell'account di archiviazione DestAccount nel gruppo di risorse DestRG.

### Esempio 2: ripristinare i dischi specificati di una VM di Azure disk gestita di cui è stato eseguito il backup da un punto di ripristino specificato

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

Il primo comando ottiene il Vault di servizi di ripristino e lo archivia in $vault variabile.
Il secondo comando ottiene l'elemento di backup di tipo AzureVM, del nome "V2VM" e lo archivia nella variabile $BackupItem.
Il terzo comando ottiene la data da sette giorni prima e lo archivia nella variabile $StartDate.
Il quarto comando ottiene la data corrente e lo archivia nella variabile $EndDate.
Il quinto comando consente di ottenere un elenco di punti di ripristino per l'elemento di backup specifico filtrato da $StartDate e $EndDate.
Il sesto comando Archivia l'elenco dei dischi da ripristinare nella variabile restoreDiskLUN.
L'ultimo comando consente di ripristinare i dischi specificati, i LUN specificato, il gruppo di risorse di destinazione Target_RG e quindi fornisce le informazioni di configurazione VM e il modello di distribuzione nell'account di archiviazione DestAccount nel gruppo di risorse DestRG.

### Esempio 3: ripristinare i dischi di una VM gestita come dischi non gestiti

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

Il primo comando ottiene il Vault RecoveryServices e lo archivia in $vault variabile.
Il secondo comando ottiene l'elemento di backup e lo archivia nella variabile $BackupItem.
Il terzo comando ottiene la data da sette giorni prima e lo archivia nella variabile $StartDate.
Il quarto comando ottiene la data corrente e lo archivia nella variabile $EndDate.
Il quinto comando consente di ottenere un elenco di punti di ripristino per l'elemento di backup specifico filtrato da $StartDate e $EndDate.
Il sesto comando Ripristina i dischi come dischi non gestiti.

### Esempio 4: ripristinare una VM non gestita come dischi non gestiti con l'account di archiviazione originale

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

Il primo comando ottiene il Vault RecoveryServices e lo archivia in $vault variabile.
Il secondo comando ottiene l'elemento di backup e lo archivia nella variabile $BackupItem.
Il terzo comando ottiene la data da sette giorni prima e lo archivia nella variabile $StartDate.
Il quarto comando ottiene la data corrente e lo archivia nella variabile $EndDate.
Il quinto comando consente di ottenere un elenco di punti di ripristino per l'elemento di backup specifico filtrato da $StartDate e $EndDate.
Il sesto comando consente di ripristinare i dischi come dischi non gestiti agli account di archiviazione originali

### Esempio 5: ripristinare più file di un elemento AzureFileShare

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

Il primo comando ottiene il Vault di servizi di ripristino e lo archivia in $vault variabile.
Il secondo comando ottiene l'elemento di backup denominato fileshareitem e lo archivia nella variabile $BackupItem.
Il terzo comando ottiene un elenco di punti di ripristino per l'elemento di backup specifico.
Il quarto comando specifica i file da ripristinare e lo archivia in $files variabile.
L'ultimo comando Ripristina i file specificati nella posizione originale.

### Esempio 6: ripristinare un DB SQL all'interno di una VM di Azure a un'altra VM di destinazione per un punto di recupero completo distinto

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

### Esempio 7: ripristinare un DB SQL all'interno di una VM di Azure a un'altra VM di destinazione per un punto di ripristino del log

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

### -MultipleSourceFilePath
Usato per il ripristino di più file da una condivisione file. Percorsi degli elementi da ripristinare all'interno della condivisione file.

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

Specifica il punto di ripristino a cui ripristinare l'elemento di backup.
Per ottenere un oggetto **AzureRmRecoveryServicesBackupRecoveryPoint** , usa il cmdlet **Get-AzRecoveryServicesBackupRecoveryPoint** .

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

Se l'elemento ripristinato esiste anche nella destinazione, usare questa opzione per indicare se sovrascriverlo o meno.
I valori accettabili per questo parametro sono i seguenti:

- Sovrascrivere
- Ignorare

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
Usare questa opzione per specificare il ripristino come dischi non gestiti

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
Specificare i dischi da recuperare della VM di cui è stato eseguito il backup

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
Usare questa opzione per ripristinare solo i dischi del sistema operativo di una VM di cui è stato eseguito il backup

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

Usato per un determinato ripristino degli elementi da una condivisione file. Percorso dell'elemento da ripristinare all'interno della condivisione file.

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

Usato per un determinato ripristino degli elementi da una condivisione file. Tipo dell'elemento da ripristinare all'interno della condivisione file.
I valori accettabili per questo parametro sono i seguenti:

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
Come parte del processo di ripristino, questo cmdlet archivia i dischi e le informazioni di configurazione in questo account di archiviazione.

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

Specifica il nome del gruppo di risorse che contiene l'account di archiviazione di destinazione nell'abbonamento.
Come parte del processo di ripristino, questo cmdlet archivia i dischi e le informazioni di configurazione in questo account di archiviazione.

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

Condivisione file a cui deve essere ripristinata la condivisione file.

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

Cartella in cui deve essere ripristinata la condivisione di file all'interno di TargetFileShareName. Se il contenuto di cui è stato eseguito il backup deve essere ripristinato in una cartella radice, assegnare i valori della cartella di destinazione come stringa vuota.

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

Gruppo di risorse a cui vengono ripristinati i dischi gestiti. Applicabile al backup della VM con dischi gestiti

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

Account di archiviazione a cui deve essere ripristinata la condivisione file.

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

Usare questa opzione se i dischi del punto di ripristino devono essere ripristinati agli account di archiviazione originali.

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

### -VaultLocation

Posizione dell'archivio di servizi di ripristino.

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

### -Confermare

Richiede la conferma prima di eseguire il cmdlet.

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

Mostra cosa succede se il cmdlet viene eseguito. 

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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### System. String

### Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. RecoveryPointBase

## OUTPUT

### Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. JobBase

## Note

## COLLEGAMENTI CORRELATI

[Backup-AzRecoveryServicesBackupItem](./Backup-AzRecoveryServicesBackupItem.md)

[Get-AzRecoveryServicesBackupItem](./Get-AzRecoveryServicesBackupItem.md)

[Get-AzRecoveryServicesBackupRecoveryPoint](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
