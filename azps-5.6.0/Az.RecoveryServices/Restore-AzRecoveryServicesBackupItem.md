---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 3d3cbb196a287e24837c0e7b0e61b16eaa06ce95
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997511"
---
# <span data-ttu-id="1f6a2-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="1f6a2-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="1f6a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f6a2-102">SYNOPSIS</span></span>

<span data-ttu-id="1f6a2-103">Ripristina i dati e la configurazione di un elemento di backup nel punto di ripristino specificato.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-103">Restores the data and configuration for a Backup item to the specified recovery point.</span></span> <span data-ttu-id="1f6a2-104">I parametri obbligatori variano in base al tipo di elemento di backup.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-104">The required parameters vary with the backup item type.</span></span>
<span data-ttu-id="1f6a2-105">Lo stesso comando viene usato anche per ripristinare macchine virtuali di Azure, database in esecuzione all'interno di Macchine virtuali di Azure e condivisioni file di Azure.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-105">The same command is used to restore Azure Virtual machines, databases running within Azure Virtual machines and Azure file shares as well.</span></span>

## <span data-ttu-id="1f6a2-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1f6a2-106">SYNTAX</span></span>

### <span data-ttu-id="1f6a2-107">AzureVMParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1f6a2-107">AzureVMParameterSet (Default)</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-DiskEncryptionSetId <string>] [-RestoreToSecondaryRegion] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f6a2-108">AzureVMManagedDiskParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f6a2-108">AzureVMManagedDiskParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-TargetResourceGroupName] <String>
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-DiskEncryptionSetId <string>] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f6a2-109">AzureVMRestoreManagedAsUnmanaged</span><span class="sxs-lookup"><span data-stu-id="1f6a2-109">AzureVMRestoreManagedAsUnmanaged</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-RestoreAsUnmanagedDisks] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f6a2-110">AzureVMUnManagedDiskParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f6a2-110">AzureVMUnManagedDiskParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-UseOriginalStorageAccount]
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f6a2-111">AzureFileShareParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f6a2-111">AzureFileShareParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-MultipleSourceFilePath <String[]>] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f6a2-112">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f6a2-112">AzureWorkloadParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase> [-RestoreToSecondaryRegion]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f6a2-113">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1f6a2-113">DESCRIPTION</span></span>

<span data-ttu-id="1f6a2-114">Il cmdlet **Restore-AzRecoveryServicesBackupItem** ripristina i dati e la configurazione per un elemento di Backup di Azure a un punto di ripristino specificato.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-114">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>

<span data-ttu-id="1f6a2-115">**Per il backup della macchina virtuale di Azure**</span><span class="sxs-lookup"><span data-stu-id="1f6a2-115">**For Azure VM  backup**</span></span>

<span data-ttu-id="1f6a2-116">Con questo comando è possibile eseguire il backup delle macchine virtuali di Azure e ripristinare i dischi (gestiti e non gestiti).</span><span class="sxs-lookup"><span data-stu-id="1f6a2-116">You can backup Azure virtual machines and restore disks (both managed and un-managed) using this command.</span></span> <span data-ttu-id="1f6a2-117">Con l'operazione di ripristino non viene ripristinata la macchina virtuale completa.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-117">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="1f6a2-118">Se si tratta di una macchina virtuale su disco gestita, è necessario specificare la posizione in cui vengono mantenuti i dischi ripristinati.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-118">If this is a managed disk VM, a target Resource group should be specified where the restored disks are kept.</span></span> <span data-ttu-id="1f6a2-119">Quando si specifica il gruppo di risorse di destinazione, se gli snapshot sono presenti nel gruppo di risorse specificato nei criteri di backup, l'operazione di ripristino sarà immediata e i dischi verranno creati dagli snapshot locali e mantenuti nel gruppo di risorse di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-119">When target resource group is specified, if the snapshots are present in the resource group that was specified in backup policy, the restore operation will be instant and the disks are created from local snapshots and kept in target-resource group.</span></span> <span data-ttu-id="1f6a2-120">È anche disponibile un'opzione per ripristinarli come dischi non gestiti, ma i dati presenti nel vault dei servizi di ripristino di Azure verranno sfruttati, quindi saranno molto più lenti.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-120">There is also an option to restore them as un-managed disks but this will leverage the data present in Azure recovery services vault and hence will be lot slower.</span></span> <span data-ttu-id="1f6a2-121">La configurazione della macchina virtuale e il modello di distribuzione che può essere usato per creare la macchina virtuale dai dischi ripristinati verranno scaricati nell'account di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-121">The configuration of the VM and the deployment template which can be used to create VM out of the restored disks will be downloaded to the specified storage account.</span></span>
<span data-ttu-id="1f6a2-122">Se si tratta di una macchina virtuale disco non gestita, gli snapshot sono presenti nell'account di archiviazione originale del disco e/o nel vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-122">If this is an un-managed disk VM, then the snapshots are present in disk's original storage account and/or in the recovery services vault.</span></span> <span data-ttu-id="1f6a2-123">Se l'utente offre la possibilità di usare l'account di archiviazione originale per il ripristino, è possibile usare il ripristino immediato.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-123">If user gives an option to use Original storage account to restore, then instant restore can be provided.</span></span> <span data-ttu-id="1f6a2-124">In caso contrario, i dati vengono recuperati dall'vault dei servizi di ripristino di Azure e i dischi vengono creati nell'account di archiviazione specificato insieme alla configurazione della macchina virtuale e al modello di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-124">Otherwise, data is fetched from Azure Recovery services vault and disks are created in specified storage account along with the configuration of the VM and the deployment template.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1f6a2-125">Per impostazione predefinita, il backup della macchina virtuale di Azure backup tutti i dischi.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-125">By default, Azure VM backup backs up all disks.</span></span> <span data-ttu-id="1f6a2-126">È possibile eseguire il backup selettivo dei dischi rilevanti usando i parametri exclusionList o InclusionList durante Enable-Backup.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-126">You can selectively backup relevant disks using the exclusionList or InclusionList parameters during Enable-Backup.</span></span> <span data-ttu-id="1f6a2-127">L'opzione per ripristinare i dischi in modo selettivo è disponibile solo se ne è stato eseguito il backup in modo selettivo.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-127">The option to selectively restore disks is available only if one has selectively backed them up.</span></span>

<span data-ttu-id="1f6a2-128">Per altre informazioni, vedere i diversi set di parametri possibili e il testo dei parametri.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-128">Please refer to different possible parameter sets and parameter text for more information.</span></span>

> [!NOTE]
> <span data-ttu-id="1f6a2-129">Se si usa il parametro -VaultId, deve essere usato anche il parametro -VaultLocation.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-129">If -VaultId parameter is used then -VaultLocation parameter should be used as well.</span></span>

<span data-ttu-id="1f6a2-130">**Per il backup della condivisione file di Azure**</span><span class="sxs-lookup"><span data-stu-id="1f6a2-130">**For Azure File share backup**</span></span>

<span data-ttu-id="1f6a2-131">È possibile ripristinare un'intera condivisione file o specifici/più file/cartelle nella condivisione.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-131">You can restore an entire file share or specific/multiple files/folders on the share.</span></span> <span data-ttu-id="1f6a2-132">È possibile ripristinare il percorso originale o in un percorso alternativo.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-132">You can restore to the original location or to an alternate location.</span></span>

<span data-ttu-id="1f6a2-133">**Per i carichi di lavoro di Azure**</span><span class="sxs-lookup"><span data-stu-id="1f6a2-133">**For Azure Workloads**</span></span>

<span data-ttu-id="1f6a2-134">È possibile ripristinare le SQL all'interno delle macchine virtuali di Azure</span><span class="sxs-lookup"><span data-stu-id="1f6a2-134">You can restore SQL DBs within Azure VMs</span></span>


## <span data-ttu-id="1f6a2-135">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1f6a2-135">EXAMPLES</span></span>

### <span data-ttu-id="1f6a2-136">Esempio 1: Ripristinare i dischi di un disco gestito di cui è stato eseguito il backup da un determinato punto di ripristino</span><span class="sxs-lookup"><span data-stu-id="1f6a2-136">Example 1: Restore the disks of a backed up Managed disk Azure VM from a given recovery point</span></span>

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

<span data-ttu-id="1f6a2-137">Il primo comando recupera il vault dei servizi di ripristino e lo archivia in $vault variabile.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-137">The first command gets the Recovery Services vault and stores it in $vault variable.</span></span>
<span data-ttu-id="1f6a2-138">Il secondo comando recupera l'elemento di backup del tipo AzureVM, il nome "V2VM" e lo archivia nella variabile $BackupItem variabile.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-138">The second command gets the Backup item of type AzureVM, of the name "V2VM", and stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="1f6a2-139">Il terzo comando ottiene la data di sette giorni prima e quindi la archivia nella $StartDate variabile.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-139">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="1f6a2-140">Il quarto comando ottiene la data corrente e la archivia nella $EndDate variabile.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-140">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="1f6a2-141">Il quinto comando ottiene un elenco di punti di ripristino per l'elemento di backup specifico filtrato per $StartDate e $EndDate.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-141">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="1f6a2-142">L'ultimo comando ripristina tutti i dischi nel gruppo di risorse di destinazione Target_RG e quindi fornisce le informazioni di configurazione della macchina virtuale e il modello di distribuzione nell'account di archiviazione DestAccount nel gruppo di risorse DestRG.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-142">The last command restores all the disks to the target Resource group Target_RG, and then provides the VM configuration information and the deployment template in the storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="1f6a2-143">Esempio 2: Ripristinare i dischi specificati di un disco gestito di cui è stato eseguito il backup da un determinato punto di ripristino</span><span class="sxs-lookup"><span data-stu-id="1f6a2-143">Example 2: Restore specified disks of a backed up Managed disk Azure VM from a given recovery point</span></span>

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

<span data-ttu-id="1f6a2-144">Il primo comando recupera il vault dei servizi di ripristino e lo archivia in $vault variabile.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-144">The first command gets the Recovery Services vault and stores it in $vault variable.</span></span>
<span data-ttu-id="1f6a2-145">Il secondo comando recupera l'elemento di backup del tipo AzureVM, il nome "V2VM" e lo archivia nella variabile $BackupItem variabile.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-145">The second command gets the Backup item of type AzureVM, of the name "V2VM", and stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="1f6a2-146">Il terzo comando ottiene la data di sette giorni prima e quindi la archivia nella $StartDate variabile.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-146">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="1f6a2-147">Il quarto comando ottiene la data corrente e la archivia nella $EndDate variabile.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-147">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="1f6a2-148">Il quinto comando ottiene un elenco di punti di ripristino per l'elemento di backup specifico filtrato per $StartDate e $EndDate.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-148">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="1f6a2-149">Il sesto comando archivia l'elenco dei dischi da ripristinare nella variabile restoreDiskLUN.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-149">The sixth command stores the list of disks to be restored in the restoreDiskLUN variable.</span></span>
<span data-ttu-id="1f6a2-150">L'ultimo comando ripristina i dischi specificati, dei LUN specificati, nel Target_RG di risorse di destinazione e quindi fornisce le informazioni di configurazione della macchina virtuale e il modello di distribuzione nell'account di archiviazione DestAccount nel gruppo di risorse DestRG.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-150">The last command restores the given disks, of the specified LUNs, to the target Resource group Target_RG, and then provides the VM configuration information and the deployment template in the storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="1f6a2-151">Esempio 3: Ripristinare i dischi di una macchina virtuale gestita come dischi non gestiti</span><span class="sxs-lookup"><span data-stu-id="1f6a2-151">Example 3: Restore disks of a managed VM as unmanaged Disks</span></span>

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

<span data-ttu-id="1f6a2-152">Il primo comando recupera il vault RecoveryServices e lo archivia in $vault variabile.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-152">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="1f6a2-153">Il secondo comando recupera l'elemento di backup e quindi lo archivia nella $BackupItem variabile.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-153">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="1f6a2-154">Il terzo comando ottiene la data di sette giorni prima e quindi la archivia nella $StartDate variabile.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-154">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="1f6a2-155">Il quarto comando ottiene la data corrente e la archivia nella $EndDate variabile.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-155">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="1f6a2-156">Il quinto comando ottiene un elenco di punti di ripristino per l'elemento di backup specifico filtrato per $StartDate e $EndDate.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-156">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="1f6a2-157">Il sesto comando ripristina i dischi come dischi non gestiti.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-157">The sixth command restores the disks as unmanaged disks.</span></span>

### <span data-ttu-id="1f6a2-158">Esempio 4: Ripristinare una macchina virtuale non gestita come dischi non gestiti usando l'account di archiviazione originale</span><span class="sxs-lookup"><span data-stu-id="1f6a2-158">Example 4: Restore an unmanaged VM as unmanaged Disks using original storage account</span></span>

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

<span data-ttu-id="1f6a2-159">Il primo comando recupera il vault RecoveryServices e lo archivia in $vault variabile.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-159">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="1f6a2-160">Il secondo comando recupera l'elemento di backup e quindi lo archivia nella $BackupItem variabile.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-160">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="1f6a2-161">Il terzo comando ottiene la data di sette giorni prima e quindi la archivia nella $StartDate variabile.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-161">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="1f6a2-162">Il quarto comando ottiene la data corrente e la archivia nella $EndDate variabile.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-162">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="1f6a2-163">Il quinto comando ottiene un elenco di punti di ripristino per l'elemento di backup specifico filtrato per $StartDate e $EndDate.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-163">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="1f6a2-164">Il sesto comando ripristina i dischi come dischi non gestiti nei propri account di archiviazione originali</span><span class="sxs-lookup"><span data-stu-id="1f6a2-164">The sixth command restores the disks as unmanaged disks to their original storage accounts</span></span>

### <span data-ttu-id="1f6a2-165">Esempio 5: Ripristinare più file di un elemento AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="1f6a2-165">Example 5: Restore Multiple files of an AzureFileShare item</span></span>

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

<span data-ttu-id="1f6a2-166">Il primo comando recupera il vault dei servizi di ripristino e lo archivia in $vault variabile.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-166">The first command gets the Recovery Services vault and stores it in $vault variable.</span></span>
<span data-ttu-id="1f6a2-167">Il secondo comando recupera l'elemento di backup denominato fileshareitem e quindi lo archivia nella $BackupItem variabile.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-167">The second command gets the Backup item named fileshareitem and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="1f6a2-168">Il terzo comando ottiene un elenco di punti di ripristino per l'elemento di backup specifico.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-168">The third command gets a list of recovery points for the specific backup item.</span></span>
<span data-ttu-id="1f6a2-169">Il quarto comando specifica quali file ripristinare e archiviare in $files variabile.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-169">The fourth command specifies which files to restore and stores it in $files variable.</span></span>
<span data-ttu-id="1f6a2-170">L'ultimo comando ripristina i file specificati nella posizione originale.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-170">The last command restores the specified files to its original location.</span></span>

### <span data-ttu-id="1f6a2-171">Esempio 6: Ripristinare un db SQL'interno di una macchina virtuale di Azure in un'altra macchina virtuale di destinazione per un punto di ripristino completo distinto</span><span class="sxs-lookup"><span data-stu-id="1f6a2-171">Example 6: Restore a SQL DB within an Azure VM to another target VM for a distinct full recovery point</span></span>

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

### <span data-ttu-id="1f6a2-172">Esempio 7: Ripristinare un db SQL'interno di una macchina virtuale di Azure in un'altra macchina virtuale di destinazione per un punto di ripristino del log</span><span class="sxs-lookup"><span data-stu-id="1f6a2-172">Example 7: Restore a SQL DB within an Azure VM to another target VM for a log recovery point</span></span>

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

## <span data-ttu-id="1f6a2-173">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f6a2-173">PARAMETERS</span></span>

### <span data-ttu-id="1f6a2-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f6a2-174">-DefaultProfile</span></span>

<span data-ttu-id="1f6a2-175">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-175">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f6a2-176">-MultipleSourceFilePath</span><span class="sxs-lookup"><span data-stu-id="1f6a2-176">-MultipleSourceFilePath</span></span>
<span data-ttu-id="1f6a2-177">Usato per il ripristino di più file da una condivisione file.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-177">Used for Multiple files restore from a file share.</span></span> <span data-ttu-id="1f6a2-178">Percorsi degli elementi da ripristinare nella condivisione file.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-178">The paths of the items to be restored within the file share.</span></span>

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

### <span data-ttu-id="1f6a2-179">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="1f6a2-179">-RecoveryPoint</span></span>

<span data-ttu-id="1f6a2-180">Specifica il punto di ripristino in cui ripristinare l'elemento di backup.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-180">Specifies the recovery point to which to restore the backup item.</span></span>
<span data-ttu-id="1f6a2-181">Per ottenere un **oggetto AzureRmRecoveryServicesBackupRecoveryPoint,** usare il cmdlet **Get-AzRecoveryServicesBackupRecoveryPoint.**</span><span class="sxs-lookup"><span data-stu-id="1f6a2-181">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet.</span></span>

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

### <span data-ttu-id="1f6a2-182">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="1f6a2-182">-ResolveConflict</span></span>

<span data-ttu-id="1f6a2-183">Se l'elemento ripristinato è presente anche nella destinazione, usare questa opzione per indicare se sovrascriverlo o meno.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-183">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>
<span data-ttu-id="1f6a2-184">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="1f6a2-184">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1f6a2-185">Sovrascrivi</span><span class="sxs-lookup"><span data-stu-id="1f6a2-185">Overwrite</span></span>
- <span data-ttu-id="1f6a2-186">Ignora</span><span class="sxs-lookup"><span data-stu-id="1f6a2-186">Skip</span></span>

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

### <span data-ttu-id="1f6a2-187">-RestoreAsUnmanagedDisks</span><span class="sxs-lookup"><span data-stu-id="1f6a2-187">-RestoreAsUnmanagedDisks</span></span>
<span data-ttu-id="1f6a2-188">Usare questa opzione per specificare di ripristinare come dischi non gestiti</span><span class="sxs-lookup"><span data-stu-id="1f6a2-188">Use this switch to specify to restore as unmanaged disks</span></span>

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

### <span data-ttu-id="1f6a2-189">-RestoreDiskList</span><span class="sxs-lookup"><span data-stu-id="1f6a2-189">-RestoreDiskList</span></span>
<span data-ttu-id="1f6a2-190">Specificare i dischi da ripristinare della macchina virtuale di cui è stato eseguito il backup</span><span class="sxs-lookup"><span data-stu-id="1f6a2-190">Specify which disks to recover of the backed up VM</span></span>

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

### <span data-ttu-id="1f6a2-191">-RestoreOnlyOSDisk</span><span class="sxs-lookup"><span data-stu-id="1f6a2-191">-RestoreOnlyOSDisk</span></span>
<span data-ttu-id="1f6a2-192">Usare questo parametro per ripristinare solo i dischi del sistema operativo di una macchina virtuale di cui è stato eseguito il backup</span><span class="sxs-lookup"><span data-stu-id="1f6a2-192">Use this switch to restore only OS disks of a backed up VM</span></span>

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

### <span data-ttu-id="1f6a2-193">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="1f6a2-193">-SourceFilePath</span></span>

<span data-ttu-id="1f6a2-194">Usato per il ripristino di un elemento specifico da una condivisione file.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-194">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="1f6a2-195">Percorso dell'elemento da ripristinare nella condivisione file.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-195">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="1f6a2-196">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="1f6a2-196">-SourceFileType</span></span>

<span data-ttu-id="1f6a2-197">Usato per il ripristino di un elemento specifico da una condivisione file.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-197">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="1f6a2-198">Il tipo di elemento da ripristinare nella condivisione file.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-198">The type of the item to be restored within the file share.</span></span>
<span data-ttu-id="1f6a2-199">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="1f6a2-199">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1f6a2-200">File</span><span class="sxs-lookup"><span data-stu-id="1f6a2-200">File</span></span>
- <span data-ttu-id="1f6a2-201">Directory</span><span class="sxs-lookup"><span data-stu-id="1f6a2-201">Directory</span></span>

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

### <span data-ttu-id="1f6a2-202">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1f6a2-202">-StorageAccountName</span></span>

<span data-ttu-id="1f6a2-203">Specifica il nome dell'account di archiviazione di destinazione nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-203">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="1f6a2-204">Durante il processo di ripristino, questo cmdlet archivia i dischi e le informazioni di configurazione in questo account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-204">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="1f6a2-205">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f6a2-205">-StorageAccountResourceGroupName</span></span>

<span data-ttu-id="1f6a2-206">Specifica il nome del gruppo di risorse che contiene l'account di archiviazione di destinazione nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-206">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="1f6a2-207">Durante il processo di ripristino, questo cmdlet archivia i dischi e le informazioni di configurazione in questo account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-207">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="1f6a2-208">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="1f6a2-208">-TargetFileShareName</span></span>

<span data-ttu-id="1f6a2-209">Condivisione file in cui è necessario ripristinare la condivisione file.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-209">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="1f6a2-210">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="1f6a2-210">-TargetFolder</span></span>

<span data-ttu-id="1f6a2-211">La cartella in cui è necessario ripristinare la condivisione file all'interno di TargetFileShareName.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-211">The folder under which the file share has to be restored to within the TargetFileShareName.</span></span> <span data-ttu-id="1f6a2-212">Se il backup del contenuto deve essere ripristinato in una cartella radice, assegnare i valori della cartella di destinazione come stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-212">If the backed-up content is to be restored to a root folder, give the target folder values as an empty string.</span></span>

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

### <span data-ttu-id="1f6a2-213">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f6a2-213">-TargetResourceGroupName</span></span>

<span data-ttu-id="1f6a2-214">Gruppo di risorse in cui vengono ripristinati i dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-214">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="1f6a2-215">Applicabile al backup della macchina virtuale con dischi gestiti</span><span class="sxs-lookup"><span data-stu-id="1f6a2-215">Applicable to backup of VM with managed disks</span></span>

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

### <span data-ttu-id="1f6a2-216">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1f6a2-216">-TargetStorageAccountName</span></span>

<span data-ttu-id="1f6a2-217">Account di archiviazione in cui è necessario ripristinare la condivisione file.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-217">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="1f6a2-218">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1f6a2-218">-UseOriginalStorageAccount</span></span>

<span data-ttu-id="1f6a2-219">Usare questa opzione se i dischi del punto di ripristino devono essere ripristinati nei relativi account di archiviazione originali.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-219">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

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

### <span data-ttu-id="1f6a2-220">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="1f6a2-220">-DiskEncryptionSetId</span></span> 

<span data-ttu-id="1f6a2-221">ID DES per crittografare i dischi ripristinati.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-221">The DES ID to encrypt the restored disks.</span></span>

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

### <span data-ttu-id="1f6a2-222">-RestoreToSecondaryRegion</span><span class="sxs-lookup"><span data-stu-id="1f6a2-222">-RestoreToSecondaryRegion</span></span>

<span data-ttu-id="1f6a2-223">Usare questo parametro per attivare il ripristino dell'area incrociata nell'area secondaria.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-223">Use this switch to trigger the Cross region restore to secondary region.</span></span>

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

### <span data-ttu-id="1f6a2-224">-VaultId</span><span class="sxs-lookup"><span data-stu-id="1f6a2-224">-VaultId</span></span>

<span data-ttu-id="1f6a2-225">ARM ID del Vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-225">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="1f6a2-226">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="1f6a2-226">-VaultLocation</span></span>

<span data-ttu-id="1f6a2-227">Posizione del Vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-227">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="1f6a2-228">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="1f6a2-228">-WLRecoveryConfig</span></span>

<span data-ttu-id="1f6a2-229">Configurazione di ripristino</span><span class="sxs-lookup"><span data-stu-id="1f6a2-229">Recovery config</span></span>

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

### <span data-ttu-id="1f6a2-230">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f6a2-230">-Confirm</span></span>

<span data-ttu-id="1f6a2-231">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-231">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f6a2-232">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f6a2-232">-WhatIf</span></span>

<span data-ttu-id="1f6a2-233">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-233">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="1f6a2-234">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f6a2-234">CommonParameters</span></span>
<span data-ttu-id="1f6a2-235">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-235">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f6a2-236">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1f6a2-236">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f6a2-237">INPUT</span><span class="sxs-lookup"><span data-stu-id="1f6a2-237">INPUTS</span></span>

### <span data-ttu-id="1f6a2-238">System.String</span><span class="sxs-lookup"><span data-stu-id="1f6a2-238">System.String</span></span>

### <span data-ttu-id="1f6a2-239">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="1f6a2-239">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="1f6a2-240">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1f6a2-240">OUTPUTS</span></span>

### <span data-ttu-id="1f6a2-241">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="1f6a2-241">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="1f6a2-242">NOTE</span><span class="sxs-lookup"><span data-stu-id="1f6a2-242">NOTES</span></span>

## <span data-ttu-id="1f6a2-243">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1f6a2-243">RELATED LINKS</span></span>

[<span data-ttu-id="1f6a2-244">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="1f6a2-244">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="1f6a2-245">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="1f6a2-245">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="1f6a2-246">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="1f6a2-246">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
