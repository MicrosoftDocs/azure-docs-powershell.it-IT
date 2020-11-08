---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 69b115fab623d1a951fa2f77632a33fb437a3555
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021491"
---
# <span data-ttu-id="6b90c-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="6b90c-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="6b90c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6b90c-102">SYNOPSIS</span></span>

<span data-ttu-id="6b90c-103">Ripristina i dati e la configurazione di un elemento di backup in un punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="6b90c-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

## <span data-ttu-id="6b90c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6b90c-104">SYNTAX</span></span>

### <span data-ttu-id="6b90c-105">AzureVMParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6b90c-105">AzureVMParameterSet (Default)</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 [[-TargetResourceGroupName] <String>] [-UseOriginalStorageAccount] [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-RestoreAsUnmanagedDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b90c-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b90c-106">AzureFileParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-MultipleSourceFilePath <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b90c-107">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b90c-107">AzureWorkloadParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b90c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6b90c-108">DESCRIPTION</span></span>

<span data-ttu-id="6b90c-109">Il cmdlet **Restore-AzRecoveryServicesBackupItem** Ripristina i dati e la configurazione per un elemento di backup di Azure in un punto di recupero specificato.</span><span class="sxs-lookup"><span data-stu-id="6b90c-109">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="6b90c-110">Questo cmdlet avvia il ripristino dall'archivio di servizi di ripristino all'account di archiviazione del cliente.</span><span class="sxs-lookup"><span data-stu-id="6b90c-110">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="6b90c-111">L'operazione di ripristino non ripristina la macchina virtuale completa.</span><span class="sxs-lookup"><span data-stu-id="6b90c-111">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="6b90c-112">Ripristina i dischi gestiti in un gruppo di risorse di destinazione e le informazioni di configurazione nell'account di archiviazione del cliente al termine dell'operazione di ripristino, è necessario creare la macchina virtuale e avviarla.</span><span class="sxs-lookup"><span data-stu-id="6b90c-112">It restores the managed disks to a target resource group and configuration information to customer storage account After the restore operation is finished, you must create the virtual machine and start it.</span></span>
<span data-ttu-id="6b90c-113">Imposta il contesto del Vault usando il parametro-VaultId.</span><span class="sxs-lookup"><span data-stu-id="6b90c-113">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="6b90c-114">Nota: per eseguire correttamente questo cmdlet, è anche necessario usare il parametro VaultId-VaultLocation.</span><span class="sxs-lookup"><span data-stu-id="6b90c-114">Note: To successfully execute this cmdlet in addition to -VaultId parameter -VaultLocation parameter should be used as well.</span></span>

## <span data-ttu-id="6b90c-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6b90c-115">EXAMPLES</span></span>

### <span data-ttu-id="6b90c-116">Esempio 1: ripristinare un elemento in un punto di ripristino</span><span class="sxs-lookup"><span data-stu-id="6b90c-116">Example 1: Restore an item to a recovery point</span></span>

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

<span data-ttu-id="6b90c-117">Il primo comando ottiene il contenitore di backup di tipo AzureVM e lo archivia nella variabile $Container.</span><span class="sxs-lookup"><span data-stu-id="6b90c-117">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="6b90c-118">Il secondo comando ottiene l'elemento di backup denominato V2VM da $Container e lo archivia nella variabile $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="6b90c-118">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="6b90c-119">Il terzo comando ottiene la data da sette giorni prima e lo archivia nella variabile $StartDate.</span><span class="sxs-lookup"><span data-stu-id="6b90c-119">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="6b90c-120">Il quarto comando ottiene la data corrente e lo archivia nella variabile $EndDate.</span><span class="sxs-lookup"><span data-stu-id="6b90c-120">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="6b90c-121">Il quinto comando consente di ottenere un elenco di punti di ripristino per l'elemento di backup specifico filtrato da $StartDate e $EndDate.</span><span class="sxs-lookup"><span data-stu-id="6b90c-121">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="6b90c-122">L'intervallo di date specificato è gli ultimi 7 giorni.</span><span class="sxs-lookup"><span data-stu-id="6b90c-122">The date range specified is the last 7 days.</span></span>
<span data-ttu-id="6b90c-123">Il settimo comando specifica i dischi da ripristinare dal punto di ripristino e lo archivia in $restoreDiskLUNs variabile.</span><span class="sxs-lookup"><span data-stu-id="6b90c-123">The seventh command specifies which disks to restore from the recovery point and stores it in $restoreDiskLUNs variable.</span></span>
<span data-ttu-id="6b90c-124">L'ultimo comando Ripristina i dischi nell'account di archiviazione di destinazione DestAccount nel gruppo di risorse DestRG.</span><span class="sxs-lookup"><span data-stu-id="6b90c-124">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="6b90c-125">Esempio 2: ripristinare più file di un elemento AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="6b90c-125">Example 2: Restore Multiple files of an AzureFileShare item</span></span>

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

<span data-ttu-id="6b90c-126">Il primo comando ottiene il contenitore di backup di tipo AzureVM e lo archivia nella variabile $Container.</span><span class="sxs-lookup"><span data-stu-id="6b90c-126">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="6b90c-127">Il secondo comando ottiene l'elemento di backup denominato fileshareitem e lo archivia nella variabile $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="6b90c-127">The second command gets the Backup item named fileshareitem and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="6b90c-128">Il terzo comando ottiene un elenco di punti di ripristino per l'elemento di backup specifico.</span><span class="sxs-lookup"><span data-stu-id="6b90c-128">The third command gets a list of recovery points for the specific backup item.</span></span>
<span data-ttu-id="6b90c-129">Il quarto comando spceifies i file da ripristinare e lo archivia in $files variabile.</span><span class="sxs-lookup"><span data-stu-id="6b90c-129">The fourth command spceifies which files to restore and stores it in $files variable.</span></span>
<span data-ttu-id="6b90c-130">L'ultimo comando Ripristina i file specificati nella posizione originale.</span><span class="sxs-lookup"><span data-stu-id="6b90c-130">The last command restores the specified files to its original location.</span></span>

## <span data-ttu-id="6b90c-131">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6b90c-131">PARAMETERS</span></span>

### <span data-ttu-id="6b90c-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b90c-132">-DefaultProfile</span></span>

<span data-ttu-id="6b90c-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6b90c-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b90c-134">-MultipleSourceFilePath</span><span class="sxs-lookup"><span data-stu-id="6b90c-134">-MultipleSourceFilePath</span></span>
<span data-ttu-id="6b90c-135">Usato per il ripristino di più file da una condivisione file.</span><span class="sxs-lookup"><span data-stu-id="6b90c-135">Used for Multiple files restore from a file share.</span></span> <span data-ttu-id="6b90c-136">Percorsi degli elementi da ripristinare all'interno della condivisione file.</span><span class="sxs-lookup"><span data-stu-id="6b90c-136">The paths of the items to be restored within the file share.</span></span>

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

### <span data-ttu-id="6b90c-137">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="6b90c-137">-RecoveryPoint</span></span>

<span data-ttu-id="6b90c-138">Specifica il punto di ripristino a cui ripristinare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6b90c-138">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="6b90c-139">Per ottenere un oggetto **AzureRmRecoveryServicesBackupRecoveryPoint** , usa il cmdlet **Get-AzRecoveryServicesBackupRecoveryPoint** .</span><span class="sxs-lookup"><span data-stu-id="6b90c-139">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet.</span></span>

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

### <span data-ttu-id="6b90c-140">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="6b90c-140">-ResolveConflict</span></span>

<span data-ttu-id="6b90c-141">Se l'elemento ripristinato esiste anche nella destinazione, usare questa opzione per indicare se sovrascriverlo o meno.</span><span class="sxs-lookup"><span data-stu-id="6b90c-141">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>
<span data-ttu-id="6b90c-142">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="6b90c-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6b90c-143">Sovrascrivere</span><span class="sxs-lookup"><span data-stu-id="6b90c-143">Overwrite</span></span>
- <span data-ttu-id="6b90c-144">Ignorare</span><span class="sxs-lookup"><span data-stu-id="6b90c-144">Skip</span></span>

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

### <span data-ttu-id="6b90c-145">-RestoreAsUnmanagedDisks</span><span class="sxs-lookup"><span data-stu-id="6b90c-145">-RestoreAsUnmanagedDisks</span></span>
<span data-ttu-id="6b90c-146">Usare questa opzione per specificare il ripristino come dischi non gestiti</span><span class="sxs-lookup"><span data-stu-id="6b90c-146">Use this switch to specify to restore as unmanaged disks</span></span>

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

### <span data-ttu-id="6b90c-147">-RestoreDiskList</span><span class="sxs-lookup"><span data-stu-id="6b90c-147">-RestoreDiskList</span></span>
<span data-ttu-id="6b90c-148">Specificare i dischi da recuperare della VM di cui è stato eseguito il backup</span><span class="sxs-lookup"><span data-stu-id="6b90c-148">Specify which disks to recover of the backed up VM</span></span>

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

### <span data-ttu-id="6b90c-149">-RestoreOnlyOSDisk</span><span class="sxs-lookup"><span data-stu-id="6b90c-149">-RestoreOnlyOSDisk</span></span>
<span data-ttu-id="6b90c-150">Usare questa opzione per ripristinare solo i dischi del sistema operativo di una VM di cui è stato eseguito il backup</span><span class="sxs-lookup"><span data-stu-id="6b90c-150">Use this switch to restore only OS disks of a backed up VM</span></span>

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

### <span data-ttu-id="6b90c-151">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="6b90c-151">-SourceFilePath</span></span>

<span data-ttu-id="6b90c-152">Usato per un determinato ripristino degli elementi da una condivisione file.</span><span class="sxs-lookup"><span data-stu-id="6b90c-152">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="6b90c-153">Percorso dell'elemento da ripristinare all'interno della condivisione file.</span><span class="sxs-lookup"><span data-stu-id="6b90c-153">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="6b90c-154">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="6b90c-154">-SourceFileType</span></span>

<span data-ttu-id="6b90c-155">Usato per un determinato ripristino degli elementi da una condivisione file.</span><span class="sxs-lookup"><span data-stu-id="6b90c-155">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="6b90c-156">Tipo dell'elemento da ripristinare all'interno della condivisione file.</span><span class="sxs-lookup"><span data-stu-id="6b90c-156">The type of the item to be restored within the file share.</span></span>
<span data-ttu-id="6b90c-157">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="6b90c-157">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6b90c-158">File</span><span class="sxs-lookup"><span data-stu-id="6b90c-158">File</span></span>
- <span data-ttu-id="6b90c-159">Directory</span><span class="sxs-lookup"><span data-stu-id="6b90c-159">Directory</span></span>

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

### <span data-ttu-id="6b90c-160">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6b90c-160">-StorageAccountName</span></span>

<span data-ttu-id="6b90c-161">Specifica il nome dell'account di archiviazione di destinazione nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="6b90c-161">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="6b90c-162">Come parte del processo di ripristino, questo cmdlet archivia i dischi e le informazioni di configurazione in questo account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="6b90c-162">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="6b90c-163">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b90c-163">-StorageAccountResourceGroupName</span></span>

<span data-ttu-id="6b90c-164">Specifica il nome del gruppo di risorse che contiene l'account di archiviazione di destinazione nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="6b90c-164">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="6b90c-165">Come parte del processo di ripristino, questo cmdlet archivia i dischi e le informazioni di configurazione in questo account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="6b90c-165">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="6b90c-166">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="6b90c-166">-TargetFileShareName</span></span>

<span data-ttu-id="6b90c-167">Condivisione file a cui deve essere ripristinata la condivisione file.</span><span class="sxs-lookup"><span data-stu-id="6b90c-167">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="6b90c-168">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="6b90c-168">-TargetFolder</span></span>

<span data-ttu-id="6b90c-169">Cartella in cui deve essere ripristinata la condivisione di file all'interno di TargetFileShareName.</span><span class="sxs-lookup"><span data-stu-id="6b90c-169">The folder under which the file share has to be restored to within the TargetFileShareName.</span></span> <span data-ttu-id="6b90c-170">Se il contenuto di cui è stato eseguito il backup deve essere ripristinato in una cartella radice, assegnare i valori della cartella di destinazione come stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="6b90c-170">If the backed-up content is to be restored to a root folder, give the target folder values as an empty string.</span></span>

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

### <span data-ttu-id="6b90c-171">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b90c-171">-TargetResourceGroupName</span></span>

<span data-ttu-id="6b90c-172">Gruppo di risorse a cui vengono ripristinati i dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="6b90c-172">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="6b90c-173">Applicabile al backup della VM con dischi gestiti</span><span class="sxs-lookup"><span data-stu-id="6b90c-173">Applicable to backup of VM with managed disks</span></span>

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

### <span data-ttu-id="6b90c-174">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6b90c-174">-TargetStorageAccountName</span></span>

<span data-ttu-id="6b90c-175">Account di archiviazione a cui deve essere ripristinata la condivisione file.</span><span class="sxs-lookup"><span data-stu-id="6b90c-175">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="6b90c-176">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6b90c-176">-UseOriginalStorageAccount</span></span>

<span data-ttu-id="6b90c-177">Usare questa opzione se i dischi del punto di ripristino devono essere ripristinati agli account di archiviazione originali.</span><span class="sxs-lookup"><span data-stu-id="6b90c-177">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

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

### <span data-ttu-id="6b90c-178">-VaultId</span><span class="sxs-lookup"><span data-stu-id="6b90c-178">-VaultId</span></span>

<span data-ttu-id="6b90c-179">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="6b90c-179">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="6b90c-180">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="6b90c-180">-VaultLocation</span></span>

<span data-ttu-id="6b90c-181">Posizione dell'archivio di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="6b90c-181">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="6b90c-182">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="6b90c-182">-WLRecoveryConfig</span></span>

<span data-ttu-id="6b90c-183">Configurazione di ripristino</span><span class="sxs-lookup"><span data-stu-id="6b90c-183">Recovery config</span></span>

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

### <span data-ttu-id="6b90c-184">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6b90c-184">-Confirm</span></span>

<span data-ttu-id="6b90c-185">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b90c-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b90c-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b90c-186">-WhatIf</span></span>

<span data-ttu-id="6b90c-187">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6b90c-187">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6b90c-188">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6b90c-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b90c-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b90c-189">CommonParameters</span></span>
<span data-ttu-id="6b90c-190">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b90c-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b90c-191">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b90c-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b90c-192">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6b90c-192">INPUTS</span></span>

### <span data-ttu-id="6b90c-193">System. String</span><span class="sxs-lookup"><span data-stu-id="6b90c-193">System.String</span></span>

### <span data-ttu-id="6b90c-194">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="6b90c-194">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="6b90c-195">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6b90c-195">OUTPUTS</span></span>

### <span data-ttu-id="6b90c-196">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="6b90c-196">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="6b90c-197">Note</span><span class="sxs-lookup"><span data-stu-id="6b90c-197">NOTES</span></span>

## <span data-ttu-id="6b90c-198">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6b90c-198">RELATED LINKS</span></span>

[<span data-ttu-id="6b90c-199">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="6b90c-199">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="6b90c-200">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="6b90c-200">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="6b90c-201">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="6b90c-201">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
