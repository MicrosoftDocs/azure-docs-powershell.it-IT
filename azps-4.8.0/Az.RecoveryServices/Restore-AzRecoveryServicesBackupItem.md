---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 7dbafdececffe1a5e96c2c39dfb6d63f05961622
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032834"
---
# <span data-ttu-id="3cde6-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="3cde6-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="3cde6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3cde6-102">SYNOPSIS</span></span>

<span data-ttu-id="3cde6-103">Ripristina i dati e la configurazione di un elemento di backup in un punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="3cde6-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

## <span data-ttu-id="3cde6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3cde6-104">SYNTAX</span></span>

### <span data-ttu-id="3cde6-105">AzureVMParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3cde6-105">AzureVMParameterSet (Default)</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 [[-TargetResourceGroupName] <String>] [-UseOriginalStorageAccount] [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-RestoreAsUnmanagedDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cde6-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="3cde6-106">AzureFileParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-MultipleSourceFilePath <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cde6-107">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="3cde6-107">AzureWorkloadParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cde6-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3cde6-108">DESCRIPTION</span></span>

<span data-ttu-id="3cde6-109">Il cmdlet **Restore-AzRecoveryServicesBackupItem** Ripristina i dati e la configurazione per un elemento di backup di Azure in un punto di recupero specificato.</span><span class="sxs-lookup"><span data-stu-id="3cde6-109">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="3cde6-110">Questo cmdlet avvia il ripristino dall'archivio di servizi di ripristino all'account di archiviazione del cliente.</span><span class="sxs-lookup"><span data-stu-id="3cde6-110">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="3cde6-111">L'operazione di ripristino non ripristina la macchina virtuale completa.</span><span class="sxs-lookup"><span data-stu-id="3cde6-111">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="3cde6-112">Ripristina i dischi gestiti in un gruppo di risorse di destinazione e le informazioni di configurazione nell'account di archiviazione del cliente al termine dell'operazione di ripristino, è necessario creare la macchina virtuale e avviarla.</span><span class="sxs-lookup"><span data-stu-id="3cde6-112">It restores the managed disks to a target resource group and configuration information to customer storage account After the restore operation is finished, you must create the virtual machine and start it.</span></span> <span data-ttu-id="3cde6-113">Per altre informazioni, refter è possibile impostare i diversi set di parametri e il testo dei parametri.</span><span class="sxs-lookup"><span data-stu-id="3cde6-113">Please refter to different possible parameter sets and parameter text for more information.</span></span>
<span data-ttu-id="3cde6-114">Imposta il contesto del Vault usando il parametro-VaultId.</span><span class="sxs-lookup"><span data-stu-id="3cde6-114">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="3cde6-115">Nota: per eseguire correttamente questo cmdlet, è anche necessario usare il parametro VaultId-VaultLocation.</span><span class="sxs-lookup"><span data-stu-id="3cde6-115">Note: To successfully execute this cmdlet in addition to -VaultId parameter -VaultLocation parameter should be used as well.</span></span>

## <span data-ttu-id="3cde6-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3cde6-116">EXAMPLES</span></span>

### <span data-ttu-id="3cde6-117">Esempio 1: ripristinare un elemento in un punto di ripristino</span><span class="sxs-lookup"><span data-stu-id="3cde6-117">Example 1: Restore an item to a recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $restoreDiskLUNs = ("0", "1")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetRG $ManagedDiskRG -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -RestoreDiskList $restoreDiskLUNs -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="3cde6-118">Il primo comando ottiene il contenitore di backup di tipo AzureVM e lo archivia nella variabile $Container.</span><span class="sxs-lookup"><span data-stu-id="3cde6-118">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="3cde6-119">Il secondo comando ottiene l'elemento di backup denominato V2VM da $Container e lo archivia nella variabile $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="3cde6-119">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="3cde6-120">Il terzo comando ottiene la data da sette giorni prima e lo archivia nella variabile $StartDate.</span><span class="sxs-lookup"><span data-stu-id="3cde6-120">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="3cde6-121">Il quarto comando ottiene la data corrente e lo archivia nella variabile $EndDate.</span><span class="sxs-lookup"><span data-stu-id="3cde6-121">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="3cde6-122">Il quinto comando consente di ottenere un elenco di punti di ripristino per l'elemento di backup specifico filtrato da $StartDate e $EndDate.</span><span class="sxs-lookup"><span data-stu-id="3cde6-122">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="3cde6-123">L'intervallo di date specificato è gli ultimi 7 giorni.</span><span class="sxs-lookup"><span data-stu-id="3cde6-123">The date range specified is the last 7 days.</span></span>
<span data-ttu-id="3cde6-124">Il settimo comando specifica i dischi da ripristinare dal punto di ripristino e lo archivia in $restoreDiskLUNs variabile.</span><span class="sxs-lookup"><span data-stu-id="3cde6-124">The seventh command specifies which disks to restore from the recovery point and stores it in $restoreDiskLUNs variable.</span></span>
<span data-ttu-id="3cde6-125">L'ultimo comando Ripristina i dischi nell'account di archiviazione di destinazione DestAccount nel gruppo di risorse DestRG.</span><span class="sxs-lookup"><span data-stu-id="3cde6-125">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="3cde6-126">Esempio 2: ripristinare più file di un elemento AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="3cde6-126">Example 2: Restore Multiple files of an AzureFileShare item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureStorage -WorkloadType AzureVM -VaultId $vault.ID -Name "fileshareitem"
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -VaultId $vault.ID
PS C:\> $files = ("file1.txt", "file2.txt")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -MultipleSourceFilePath $files -SourceFileType File -ResolveConflict Overwrite -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    fileshareitem            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="3cde6-127">Il primo comando ottiene il contenitore di backup di tipo AzureVM e lo archivia nella variabile $Container.</span><span class="sxs-lookup"><span data-stu-id="3cde6-127">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="3cde6-128">Il secondo comando ottiene l'elemento di backup denominato fileshareitem e lo archivia nella variabile $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="3cde6-128">The second command gets the Backup item named fileshareitem and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="3cde6-129">Il terzo comando ottiene un elenco di punti di ripristino per l'elemento di backup specifico.</span><span class="sxs-lookup"><span data-stu-id="3cde6-129">The third command gets a list of recovery points for the specific backup item.</span></span>
<span data-ttu-id="3cde6-130">Il quarto comando spceifies i file da ripristinare e lo archivia in $files variabile.</span><span class="sxs-lookup"><span data-stu-id="3cde6-130">The fourth command spceifies which files to restore and stores it in $files variable.</span></span>
<span data-ttu-id="3cde6-131">L'ultimo comando Ripristina i file specificati nella posizione originale.</span><span class="sxs-lookup"><span data-stu-id="3cde6-131">The last command restores the specified files to its original location.</span></span>

### <span data-ttu-id="3cde6-132">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="3cde6-132">Example 3</span></span>

<span data-ttu-id="3cde6-133">Ripristina i dati e la configurazione di un elemento di backup in un punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="3cde6-133">Restores the data and configuration for a Backup item to a recovery point.</span></span> <span data-ttu-id="3cde6-134">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="3cde6-134">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Restore-AzRecoveryServicesBackupItem -VaultId $vault.ID -WLRecoveryConfig <RecoveryConfigBase>
```

## <span data-ttu-id="3cde6-135">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3cde6-135">PARAMETERS</span></span>

### <span data-ttu-id="3cde6-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cde6-136">-DefaultProfile</span></span>

<span data-ttu-id="3cde6-137">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3cde6-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3cde6-138">-MultipleSourceFilePath</span><span class="sxs-lookup"><span data-stu-id="3cde6-138">-MultipleSourceFilePath</span></span>
<span data-ttu-id="3cde6-139">Usato per il ripristino di più file da una condivisione file.</span><span class="sxs-lookup"><span data-stu-id="3cde6-139">Used for Multiple files restore from a file share.</span></span> <span data-ttu-id="3cde6-140">Percorsi degli elementi da ripristinare all'interno della condivisione file.</span><span class="sxs-lookup"><span data-stu-id="3cde6-140">The paths of the items to be restored within the file share.</span></span>

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

### <span data-ttu-id="3cde6-141">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="3cde6-141">-RecoveryPoint</span></span>

<span data-ttu-id="3cde6-142">Specifica il punto di ripristino a cui ripristinare l'elemento di backup.</span><span class="sxs-lookup"><span data-stu-id="3cde6-142">Specifies the recovery point to which to restore the backup item.</span></span>
<span data-ttu-id="3cde6-143">Per ottenere un oggetto **AzureRmRecoveryServicesBackupRecoveryPoint** , usa il cmdlet **Get-AzRecoveryServicesBackupRecoveryPoint** .</span><span class="sxs-lookup"><span data-stu-id="3cde6-143">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: AzureVMParameterSet, AzureFileParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3cde6-144">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="3cde6-144">-ResolveConflict</span></span>

<span data-ttu-id="3cde6-145">Se l'elemento ripristinato esiste anche nella destinazione, usare questa opzione per indicare se sovrascriverlo o meno.</span><span class="sxs-lookup"><span data-stu-id="3cde6-145">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>
<span data-ttu-id="3cde6-146">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="3cde6-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3cde6-147">Sovrascrivere</span><span class="sxs-lookup"><span data-stu-id="3cde6-147">Overwrite</span></span>
- <span data-ttu-id="3cde6-148">Ignorare</span><span class="sxs-lookup"><span data-stu-id="3cde6-148">Skip</span></span>

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

### <span data-ttu-id="3cde6-149">-RestoreAsUnmanagedDisks</span><span class="sxs-lookup"><span data-stu-id="3cde6-149">-RestoreAsUnmanagedDisks</span></span>
<span data-ttu-id="3cde6-150">Usare questa opzione per specificare il ripristino come dischi non gestiti</span><span class="sxs-lookup"><span data-stu-id="3cde6-150">Use this switch to specify to restore as unmanaged disks</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cde6-151">-RestoreDiskList</span><span class="sxs-lookup"><span data-stu-id="3cde6-151">-RestoreDiskList</span></span>
<span data-ttu-id="3cde6-152">Specificare i dischi da recuperare della VM di cui è stato eseguito il backup</span><span class="sxs-lookup"><span data-stu-id="3cde6-152">Specify which disks to recover of the backed up VM</span></span>

```yaml
Type: System.String[]
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cde6-153">-RestoreOnlyOSDisk</span><span class="sxs-lookup"><span data-stu-id="3cde6-153">-RestoreOnlyOSDisk</span></span>
<span data-ttu-id="3cde6-154">Usare questa opzione per ripristinare solo i dischi del sistema operativo di una VM di cui è stato eseguito il backup</span><span class="sxs-lookup"><span data-stu-id="3cde6-154">Use this switch to restore only OS disks of a backed up VM</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cde6-155">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="3cde6-155">-SourceFilePath</span></span>

<span data-ttu-id="3cde6-156">Usato per un determinato ripristino degli elementi da una condivisione file.</span><span class="sxs-lookup"><span data-stu-id="3cde6-156">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="3cde6-157">Percorso dell'elemento da ripristinare all'interno della condivisione file.</span><span class="sxs-lookup"><span data-stu-id="3cde6-157">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="3cde6-158">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="3cde6-158">-SourceFileType</span></span>

<span data-ttu-id="3cde6-159">Usato per un determinato ripristino degli elementi da una condivisione file.</span><span class="sxs-lookup"><span data-stu-id="3cde6-159">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="3cde6-160">Tipo dell'elemento da ripristinare all'interno della condivisione file.</span><span class="sxs-lookup"><span data-stu-id="3cde6-160">The type of the item to be restored within the file share.</span></span>
<span data-ttu-id="3cde6-161">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="3cde6-161">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3cde6-162">File</span><span class="sxs-lookup"><span data-stu-id="3cde6-162">File</span></span>
- <span data-ttu-id="3cde6-163">Directory</span><span class="sxs-lookup"><span data-stu-id="3cde6-163">Directory</span></span>

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

### <span data-ttu-id="3cde6-164">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3cde6-164">-StorageAccountName</span></span>

<span data-ttu-id="3cde6-165">Specifica il nome dell'account di archiviazione di destinazione nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="3cde6-165">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="3cde6-166">Come parte del processo di ripristino, questo cmdlet archivia i dischi e le informazioni di configurazione in questo account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3cde6-166">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cde6-167">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cde6-167">-StorageAccountResourceGroupName</span></span>

<span data-ttu-id="3cde6-168">Specifica il nome del gruppo di risorse che contiene l'account di archiviazione di destinazione nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="3cde6-168">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="3cde6-169">Come parte del processo di ripristino, questo cmdlet archivia i dischi e le informazioni di configurazione in questo account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3cde6-169">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cde6-170">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="3cde6-170">-TargetFileShareName</span></span>

<span data-ttu-id="3cde6-171">Condivisione file a cui deve essere ripristinata la condivisione file.</span><span class="sxs-lookup"><span data-stu-id="3cde6-171">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="3cde6-172">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="3cde6-172">-TargetFolder</span></span>

<span data-ttu-id="3cde6-173">Cartella in cui deve essere ripristinata la condivisione di file all'interno di TargetFileShareName.</span><span class="sxs-lookup"><span data-stu-id="3cde6-173">The folder under which the file share has to be restored to within the TargetFileShareName.</span></span> <span data-ttu-id="3cde6-174">Se il contenuto di cui è stato eseguito il backup deve essere ripristinato in una cartella radice, assegnare i valori della cartella di destinazione come stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="3cde6-174">If the backed-up content is to be restored to a root folder, give the target folder values as an empty string.</span></span>

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

### <span data-ttu-id="3cde6-175">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cde6-175">-TargetResourceGroupName</span></span>

<span data-ttu-id="3cde6-176">Gruppo di risorse a cui vengono ripristinati i dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="3cde6-176">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="3cde6-177">Applicabile al backup della VM con dischi gestiti</span><span class="sxs-lookup"><span data-stu-id="3cde6-177">Applicable to backup of VM with managed disks</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cde6-178">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3cde6-178">-TargetStorageAccountName</span></span>

<span data-ttu-id="3cde6-179">Account di archiviazione a cui deve essere ripristinata la condivisione file.</span><span class="sxs-lookup"><span data-stu-id="3cde6-179">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="3cde6-180">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3cde6-180">-UseOriginalStorageAccount</span></span>

<span data-ttu-id="3cde6-181">Usare questa opzione se i dischi del punto di ripristino devono essere ripristinati agli account di archiviazione originali.</span><span class="sxs-lookup"><span data-stu-id="3cde6-181">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cde6-182">-VaultId</span><span class="sxs-lookup"><span data-stu-id="3cde6-182">-VaultId</span></span>

<span data-ttu-id="3cde6-183">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="3cde6-183">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="3cde6-184">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="3cde6-184">-VaultLocation</span></span>

<span data-ttu-id="3cde6-185">Posizione dell'archivio di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="3cde6-185">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="3cde6-186">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="3cde6-186">-WLRecoveryConfig</span></span>

<span data-ttu-id="3cde6-187">Configurazione di ripristino</span><span class="sxs-lookup"><span data-stu-id="3cde6-187">Recovery config</span></span>

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

### <span data-ttu-id="3cde6-188">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3cde6-188">-Confirm</span></span>

<span data-ttu-id="3cde6-189">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cde6-189">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cde6-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cde6-190">-WhatIf</span></span>

<span data-ttu-id="3cde6-191">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3cde6-191">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="3cde6-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cde6-192">CommonParameters</span></span>
<span data-ttu-id="3cde6-193">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cde6-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cde6-194">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3cde6-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cde6-195">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3cde6-195">INPUTS</span></span>

### <span data-ttu-id="3cde6-196">System. String</span><span class="sxs-lookup"><span data-stu-id="3cde6-196">System.String</span></span>

### <span data-ttu-id="3cde6-197">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="3cde6-197">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="3cde6-198">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3cde6-198">OUTPUTS</span></span>

### <span data-ttu-id="3cde6-199">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="3cde6-199">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="3cde6-200">Note</span><span class="sxs-lookup"><span data-stu-id="3cde6-200">NOTES</span></span>

## <span data-ttu-id="3cde6-201">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3cde6-201">RELATED LINKS</span></span>

[<span data-ttu-id="3cde6-202">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="3cde6-202">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="3cde6-203">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="3cde6-203">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="3cde6-204">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="3cde6-204">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
