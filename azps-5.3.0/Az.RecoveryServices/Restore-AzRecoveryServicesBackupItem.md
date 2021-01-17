---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 32ecad0d89725d4fa01d76ebfe9a319dfece6b80
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474404"
---
# <span data-ttu-id="ab316-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="ab316-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="ab316-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ab316-102">SYNOPSIS</span></span>

<span data-ttu-id="ab316-103">Ripristina i dati e la configurazione per un elemento di backup nel punto di recupero specificato.</span><span class="sxs-lookup"><span data-stu-id="ab316-103">Restores the data and configuration for a Backup item to the specified recovery point.</span></span> <span data-ttu-id="ab316-104">I parametri obbligatori variano a seconda del tipo di elemento di backup.</span><span class="sxs-lookup"><span data-stu-id="ab316-104">The required parameters vary with the backup item type.</span></span>
<span data-ttu-id="ab316-105">Lo stesso comando viene usato per ripristinare le macchine virtuali di Azure, i database in cui sono in uso anche le macchine virtuali Azure e le condivisioni di file Azure.</span><span class="sxs-lookup"><span data-stu-id="ab316-105">The same command is used to restore Azure Virtual machines, databases running within Azure Virtual machines and Azure file shares as well.</span></span>

## <span data-ttu-id="ab316-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ab316-106">SYNTAX</span></span>

### <span data-ttu-id="ab316-107">AzureVMParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ab316-107">AzureVMParameterSet (Default)</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-DiskEncryptionSetId <string>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab316-108">AzureVMManagedDiskParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab316-108">AzureVMManagedDiskParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-TargetResourceGroupName] <String>
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-DiskEncryptionSetId <string>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab316-109">AzureVMRestoreManagedAsUnmanaged</span><span class="sxs-lookup"><span data-stu-id="ab316-109">AzureVMRestoreManagedAsUnmanaged</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-RestoreAsUnmanagedDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab316-110">AzureVMUnManagedDiskParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab316-110">AzureVMUnManagedDiskParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-UseOriginalStorageAccount]
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab316-111">AzureFileShareParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab316-111">AzureFileShareParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-MultipleSourceFilePath <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab316-112">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab316-112">AzureWorkloadParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab316-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab316-113">DESCRIPTION</span></span>

<span data-ttu-id="ab316-114">Il cmdlet **Restore-AzRecoveryServicesBackupItem** Ripristina i dati e la configurazione per un elemento di backup di Azure in un punto di recupero specificato.</span><span class="sxs-lookup"><span data-stu-id="ab316-114">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>

<span data-ttu-id="ab316-115">**Per il backup di Azure VM**</span><span class="sxs-lookup"><span data-stu-id="ab316-115">**For Azure VM  backup**</span></span>

<span data-ttu-id="ab316-116">Puoi eseguire il backup di macchine virtuali di Azure e ripristinare dischi (gestiti e non gestiti) usando questo comando.</span><span class="sxs-lookup"><span data-stu-id="ab316-116">You can backup Azure virtual machines and restore disks (both managed and un-managed) using this command.</span></span> <span data-ttu-id="ab316-117">L'operazione di ripristino non ripristina la macchina virtuale completa.</span><span class="sxs-lookup"><span data-stu-id="ab316-117">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="ab316-118">Se si tratta di una VM disco gestito, è necessario specificare un gruppo di risorse di destinazione in cui vengono conservati i dischi ripristinati.</span><span class="sxs-lookup"><span data-stu-id="ab316-118">If this is a managed disk VM, a target Resource group should be specified where the restored disks are kept.</span></span> <span data-ttu-id="ab316-119">Quando viene specificato il gruppo di risorse di destinazione, se gli snapshot sono presenti nel gruppo di risorse specificato in criteri di backup, l'operazione di ripristino sarà immediata e i dischi verranno creati da snapshot locali e conservati in un gruppo di risorse di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ab316-119">When target resource group is specified, if the snapshots are present in the resource group that was specified in backup policy, the restore operation will be instant and the disks are created from local snapshots and kept in target-resource group.</span></span> <span data-ttu-id="ab316-120">Esiste anche un'opzione per ripristinarli come dischi non gestiti, ma questa operazione sfrutterà i dati presenti in Azure Recovery Services Vault e quindi sarà molto più lenta.</span><span class="sxs-lookup"><span data-stu-id="ab316-120">There is also an option to restore them as un-managed disks but this will leverage the data present in Azure recovery services vault and hence will be lot slower.</span></span> <span data-ttu-id="ab316-121">La configurazione della VM e del modello di distribuzione, che può essere usata per creare VM fuori dai dischi ripristinati, verrà scaricata nell'account di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="ab316-121">The configuration of the VM and the deployment template which can be used to create VM out of the restored disks will be downloaded to the specified storage account.</span></span>
<span data-ttu-id="ab316-122">Se si tratta di una VM disco non gestita, gli snapshot sono presenti nell'account di archiviazione originale del disco e/o nell'archivio dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="ab316-122">If this is an un-managed disk VM, then the snapshots are present in disk's original storage account and/or in the recovery services vault.</span></span> <span data-ttu-id="ab316-123">Se l'utente concede l'opzione di usare l'account di archiviazione originale per il ripristino, è possibile fornire il ripristino istantaneo.</span><span class="sxs-lookup"><span data-stu-id="ab316-123">If user gives an option to use Original storage account to restore, then instant restore can be provided.</span></span> <span data-ttu-id="ab316-124">In caso contrario, i dati vengono recuperati dal Vault di servizi di ripristino di Azure e i dischi vengono creati nell'account di archiviazione specificato insieme alla configurazione della VM e del modello di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="ab316-124">Otherwise, data is fetched from Azure Recovery services vault and disks are created in specified storage account along with the configuration of the VM and the deployment template.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ab316-125">Per impostazione predefinita, il backup di Azure VM riporta tutti i dischi.</span><span class="sxs-lookup"><span data-stu-id="ab316-125">By default, Azure VM backup backs up all disks.</span></span> <span data-ttu-id="ab316-126">È possibile eseguire il backup in modo selettivo dei dischi rilevanti usando i parametri di esclusione o inclusione durante enable-backup.</span><span class="sxs-lookup"><span data-stu-id="ab316-126">You can selectively backup relevant disks using the exclusionList or InclusionList parameters during Enable-Backup.</span></span> <span data-ttu-id="ab316-127">L'opzione per ripristinare selettivamente i dischi è disponibile solo se è stato eseguito il backup in modo selettivo.</span><span class="sxs-lookup"><span data-stu-id="ab316-127">The option to selectively restore disks is available only if one has selectively backed them up.</span></span>

<span data-ttu-id="ab316-128">Per altre informazioni, fare riferimento a diversi possibili set di parametri e testo dei parametri.</span><span class="sxs-lookup"><span data-stu-id="ab316-128">Please refer to different possible parameter sets and parameter text for more information.</span></span>

> [!NOTE]
> <span data-ttu-id="ab316-129">Se viene usato il parametro-VaultId, deve essere usato anche il parametro VaultLocation.</span><span class="sxs-lookup"><span data-stu-id="ab316-129">If -VaultId parameter is used then -VaultLocation parameter should be used as well.</span></span>

<span data-ttu-id="ab316-130">**Per il backup di condivisione file Azure**</span><span class="sxs-lookup"><span data-stu-id="ab316-130">**For Azure File share backup**</span></span>

<span data-ttu-id="ab316-131">È possibile ripristinare un'intera condivisione file o file/cartelle specifici/multipli nella condivisione.</span><span class="sxs-lookup"><span data-stu-id="ab316-131">You can restore an entire file share or specific/multiple files/folders on the share.</span></span> <span data-ttu-id="ab316-132">È possibile ripristinare la posizione originale o in una posizione alternativa.</span><span class="sxs-lookup"><span data-stu-id="ab316-132">You can restore to the original location or to an alternate location.</span></span>

<span data-ttu-id="ab316-133">**Per i carichi di lavoro di Azure**</span><span class="sxs-lookup"><span data-stu-id="ab316-133">**For Azure Workloads**</span></span>

<span data-ttu-id="ab316-134">È possibile ripristinare SQL DBs in Azure VM</span><span class="sxs-lookup"><span data-stu-id="ab316-134">You can restore SQL DBs within Azure VMs</span></span>


## <span data-ttu-id="ab316-135">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ab316-135">EXAMPLES</span></span>

### <span data-ttu-id="ab316-136">Esempio 1: ripristinare i dischi di una VM di Azure disco gestito di cui è stato eseguito il backup da un punto di ripristino specifico</span><span class="sxs-lookup"><span data-stu-id="ab316-136">Example 1: Restore the disks of a backed up Managed disk Azure VM from a given recovery point</span></span>

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

<span data-ttu-id="ab316-137">Il primo comando ottiene il Vault di servizi di ripristino e lo archivia in $vault variabile.</span><span class="sxs-lookup"><span data-stu-id="ab316-137">The first command gets the Recovery Services vault and stores it in $vault variable.</span></span>
<span data-ttu-id="ab316-138">Il secondo comando ottiene l'elemento di backup di tipo AzureVM, del nome "V2VM" e lo archivia nella variabile $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="ab316-138">The second command gets the Backup item of type AzureVM, of the name "V2VM", and stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="ab316-139">Il terzo comando ottiene la data da sette giorni prima e lo archivia nella variabile $StartDate.</span><span class="sxs-lookup"><span data-stu-id="ab316-139">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="ab316-140">Il quarto comando ottiene la data corrente e lo archivia nella variabile $EndDate.</span><span class="sxs-lookup"><span data-stu-id="ab316-140">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="ab316-141">Il quinto comando consente di ottenere un elenco di punti di ripristino per l'elemento di backup specifico filtrato da $StartDate e $EndDate.</span><span class="sxs-lookup"><span data-stu-id="ab316-141">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="ab316-142">L'ultimo comando Ripristina tutti i dischi nel gruppo di risorse di destinazione Target_RG e quindi fornisce le informazioni di configurazione VM e il modello di distribuzione nell'account di archiviazione DestAccount nel gruppo di risorse DestRG.</span><span class="sxs-lookup"><span data-stu-id="ab316-142">The last command restores all the disks to the target Resource group Target_RG, and then provides the VM configuration information and the deployment template in the storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="ab316-143">Esempio 2: ripristinare i dischi specificati di una VM di Azure disk gestita di cui è stato eseguito il backup da un punto di ripristino specificato</span><span class="sxs-lookup"><span data-stu-id="ab316-143">Example 2: Restore specified disks of a backed up Managed disk Azure VM from a given recovery point</span></span>

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

<span data-ttu-id="ab316-144">Il primo comando ottiene il Vault di servizi di ripristino e lo archivia in $vault variabile.</span><span class="sxs-lookup"><span data-stu-id="ab316-144">The first command gets the Recovery Services vault and stores it in $vault variable.</span></span>
<span data-ttu-id="ab316-145">Il secondo comando ottiene l'elemento di backup di tipo AzureVM, del nome "V2VM" e lo archivia nella variabile $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="ab316-145">The second command gets the Backup item of type AzureVM, of the name "V2VM", and stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="ab316-146">Il terzo comando ottiene la data da sette giorni prima e lo archivia nella variabile $StartDate.</span><span class="sxs-lookup"><span data-stu-id="ab316-146">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="ab316-147">Il quarto comando ottiene la data corrente e lo archivia nella variabile $EndDate.</span><span class="sxs-lookup"><span data-stu-id="ab316-147">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="ab316-148">Il quinto comando consente di ottenere un elenco di punti di ripristino per l'elemento di backup specifico filtrato da $StartDate e $EndDate.</span><span class="sxs-lookup"><span data-stu-id="ab316-148">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="ab316-149">Il sesto comando Archivia l'elenco dei dischi da ripristinare nella variabile restoreDiskLUN.</span><span class="sxs-lookup"><span data-stu-id="ab316-149">The sixth command stores the list of disks to be restored in the restoreDiskLUN variable.</span></span>
<span data-ttu-id="ab316-150">L'ultimo comando consente di ripristinare i dischi specificati, i LUN specificato, il gruppo di risorse di destinazione Target_RG e quindi fornisce le informazioni di configurazione VM e il modello di distribuzione nell'account di archiviazione DestAccount nel gruppo di risorse DestRG.</span><span class="sxs-lookup"><span data-stu-id="ab316-150">The last command restores the given disks, of the specified LUNs, to the target Resource group Target_RG, and then provides the VM configuration information and the deployment template in the storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="ab316-151">Esempio 3: ripristinare i dischi di una VM gestita come dischi non gestiti</span><span class="sxs-lookup"><span data-stu-id="ab316-151">Example 3: Restore disks of a managed VM as unmanaged Disks</span></span>

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

<span data-ttu-id="ab316-152">Il primo comando ottiene il Vault RecoveryServices e lo archivia in $vault variabile.</span><span class="sxs-lookup"><span data-stu-id="ab316-152">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="ab316-153">Il secondo comando ottiene l'elemento di backup e lo archivia nella variabile $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="ab316-153">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="ab316-154">Il terzo comando ottiene la data da sette giorni prima e lo archivia nella variabile $StartDate.</span><span class="sxs-lookup"><span data-stu-id="ab316-154">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="ab316-155">Il quarto comando ottiene la data corrente e lo archivia nella variabile $EndDate.</span><span class="sxs-lookup"><span data-stu-id="ab316-155">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="ab316-156">Il quinto comando consente di ottenere un elenco di punti di ripristino per l'elemento di backup specifico filtrato da $StartDate e $EndDate.</span><span class="sxs-lookup"><span data-stu-id="ab316-156">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="ab316-157">Il sesto comando Ripristina i dischi come dischi non gestiti.</span><span class="sxs-lookup"><span data-stu-id="ab316-157">The sixth command restores the disks as unmanaged disks.</span></span>

### <span data-ttu-id="ab316-158">Esempio 4: ripristinare una VM non gestita come dischi non gestiti con l'account di archiviazione originale</span><span class="sxs-lookup"><span data-stu-id="ab316-158">Example 4: Restore an unmanaged VM as unmanaged Disks using original storage account</span></span>

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

<span data-ttu-id="ab316-159">Il primo comando ottiene il Vault RecoveryServices e lo archivia in $vault variabile.</span><span class="sxs-lookup"><span data-stu-id="ab316-159">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="ab316-160">Il secondo comando ottiene l'elemento di backup e lo archivia nella variabile $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="ab316-160">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="ab316-161">Il terzo comando ottiene la data da sette giorni prima e lo archivia nella variabile $StartDate.</span><span class="sxs-lookup"><span data-stu-id="ab316-161">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="ab316-162">Il quarto comando ottiene la data corrente e lo archivia nella variabile $EndDate.</span><span class="sxs-lookup"><span data-stu-id="ab316-162">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="ab316-163">Il quinto comando consente di ottenere un elenco di punti di ripristino per l'elemento di backup specifico filtrato da $StartDate e $EndDate.</span><span class="sxs-lookup"><span data-stu-id="ab316-163">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="ab316-164">Il sesto comando consente di ripristinare i dischi come dischi non gestiti agli account di archiviazione originali</span><span class="sxs-lookup"><span data-stu-id="ab316-164">The sixth command restores the disks as unmanaged disks to their original storage accounts</span></span>

### <span data-ttu-id="ab316-165">Esempio 5: ripristinare più file di un elemento AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="ab316-165">Example 5: Restore Multiple files of an AzureFileShare item</span></span>

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

<span data-ttu-id="ab316-166">Il primo comando ottiene il Vault di servizi di ripristino e lo archivia in $vault variabile.</span><span class="sxs-lookup"><span data-stu-id="ab316-166">The first command gets the Recovery Services vault and stores it in $vault variable.</span></span>
<span data-ttu-id="ab316-167">Il secondo comando ottiene l'elemento di backup denominato fileshareitem e lo archivia nella variabile $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="ab316-167">The second command gets the Backup item named fileshareitem and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="ab316-168">Il terzo comando ottiene un elenco di punti di ripristino per l'elemento di backup specifico.</span><span class="sxs-lookup"><span data-stu-id="ab316-168">The third command gets a list of recovery points for the specific backup item.</span></span>
<span data-ttu-id="ab316-169">Il quarto comando specifica i file da ripristinare e lo archivia in $files variabile.</span><span class="sxs-lookup"><span data-stu-id="ab316-169">The fourth command specifies which files to restore and stores it in $files variable.</span></span>
<span data-ttu-id="ab316-170">L'ultimo comando Ripristina i file specificati nella posizione originale.</span><span class="sxs-lookup"><span data-stu-id="ab316-170">The last command restores the specified files to its original location.</span></span>

### <span data-ttu-id="ab316-171">Esempio 6: ripristinare un DB SQL all'interno di una VM di Azure a un'altra VM di destinazione per un punto di recupero completo distinto</span><span class="sxs-lookup"><span data-stu-id="ab316-171">Example 6: Restore a SQL DB within an Azure VM to another target VM for a distinct full recovery point</span></span>

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

### <span data-ttu-id="ab316-172">Esempio 7: ripristinare un DB SQL all'interno di una VM di Azure a un'altra VM di destinazione per un punto di ripristino del log</span><span class="sxs-lookup"><span data-stu-id="ab316-172">Example 7: Restore a SQL DB within an Azure VM to another target VM for a log recovery point</span></span>

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

## <span data-ttu-id="ab316-173">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ab316-173">PARAMETERS</span></span>

### <span data-ttu-id="ab316-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab316-174">-DefaultProfile</span></span>

<span data-ttu-id="ab316-175">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ab316-175">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab316-176">-MultipleSourceFilePath</span><span class="sxs-lookup"><span data-stu-id="ab316-176">-MultipleSourceFilePath</span></span>
<span data-ttu-id="ab316-177">Usato per il ripristino di più file da una condivisione file.</span><span class="sxs-lookup"><span data-stu-id="ab316-177">Used for Multiple files restore from a file share.</span></span> <span data-ttu-id="ab316-178">Percorsi degli elementi da ripristinare all'interno della condivisione file.</span><span class="sxs-lookup"><span data-stu-id="ab316-178">The paths of the items to be restored within the file share.</span></span>

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

### <span data-ttu-id="ab316-179">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="ab316-179">-RecoveryPoint</span></span>

<span data-ttu-id="ab316-180">Specifica il punto di ripristino a cui ripristinare l'elemento di backup.</span><span class="sxs-lookup"><span data-stu-id="ab316-180">Specifies the recovery point to which to restore the backup item.</span></span>
<span data-ttu-id="ab316-181">Per ottenere un oggetto **AzureRmRecoveryServicesBackupRecoveryPoint** , usa il cmdlet **Get-AzRecoveryServicesBackupRecoveryPoint** .</span><span class="sxs-lookup"><span data-stu-id="ab316-181">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet.</span></span>

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

### <span data-ttu-id="ab316-182">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="ab316-182">-ResolveConflict</span></span>

<span data-ttu-id="ab316-183">Se l'elemento ripristinato esiste anche nella destinazione, usare questa opzione per indicare se sovrascriverlo o meno.</span><span class="sxs-lookup"><span data-stu-id="ab316-183">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>
<span data-ttu-id="ab316-184">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ab316-184">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ab316-185">Sovrascrivere</span><span class="sxs-lookup"><span data-stu-id="ab316-185">Overwrite</span></span>
- <span data-ttu-id="ab316-186">Ignorare</span><span class="sxs-lookup"><span data-stu-id="ab316-186">Skip</span></span>

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

### <span data-ttu-id="ab316-187">-RestoreAsUnmanagedDisks</span><span class="sxs-lookup"><span data-stu-id="ab316-187">-RestoreAsUnmanagedDisks</span></span>
<span data-ttu-id="ab316-188">Usare questa opzione per specificare il ripristino come dischi non gestiti</span><span class="sxs-lookup"><span data-stu-id="ab316-188">Use this switch to specify to restore as unmanaged disks</span></span>

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

### <span data-ttu-id="ab316-189">-RestoreDiskList</span><span class="sxs-lookup"><span data-stu-id="ab316-189">-RestoreDiskList</span></span>
<span data-ttu-id="ab316-190">Specificare i dischi da recuperare della VM di cui è stato eseguito il backup</span><span class="sxs-lookup"><span data-stu-id="ab316-190">Specify which disks to recover of the backed up VM</span></span>

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

### <span data-ttu-id="ab316-191">-RestoreOnlyOSDisk</span><span class="sxs-lookup"><span data-stu-id="ab316-191">-RestoreOnlyOSDisk</span></span>
<span data-ttu-id="ab316-192">Usare questa opzione per ripristinare solo i dischi del sistema operativo di una VM di cui è stato eseguito il backup</span><span class="sxs-lookup"><span data-stu-id="ab316-192">Use this switch to restore only OS disks of a backed up VM</span></span>

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

### <span data-ttu-id="ab316-193">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="ab316-193">-SourceFilePath</span></span>

<span data-ttu-id="ab316-194">Usato per un determinato ripristino degli elementi da una condivisione file.</span><span class="sxs-lookup"><span data-stu-id="ab316-194">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="ab316-195">Percorso dell'elemento da ripristinare all'interno della condivisione file.</span><span class="sxs-lookup"><span data-stu-id="ab316-195">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="ab316-196">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="ab316-196">-SourceFileType</span></span>

<span data-ttu-id="ab316-197">Usato per un determinato ripristino degli elementi da una condivisione file.</span><span class="sxs-lookup"><span data-stu-id="ab316-197">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="ab316-198">Tipo dell'elemento da ripristinare all'interno della condivisione file.</span><span class="sxs-lookup"><span data-stu-id="ab316-198">The type of the item to be restored within the file share.</span></span>
<span data-ttu-id="ab316-199">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ab316-199">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ab316-200">File</span><span class="sxs-lookup"><span data-stu-id="ab316-200">File</span></span>
- <span data-ttu-id="ab316-201">Directory</span><span class="sxs-lookup"><span data-stu-id="ab316-201">Directory</span></span>

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

### <span data-ttu-id="ab316-202">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ab316-202">-StorageAccountName</span></span>

<span data-ttu-id="ab316-203">Specifica il nome dell'account di archiviazione di destinazione nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="ab316-203">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="ab316-204">Come parte del processo di ripristino, questo cmdlet archivia i dischi e le informazioni di configurazione in questo account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ab316-204">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="ab316-205">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab316-205">-StorageAccountResourceGroupName</span></span>

<span data-ttu-id="ab316-206">Specifica il nome del gruppo di risorse che contiene l'account di archiviazione di destinazione nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="ab316-206">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="ab316-207">Come parte del processo di ripristino, questo cmdlet archivia i dischi e le informazioni di configurazione in questo account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ab316-207">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="ab316-208">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="ab316-208">-TargetFileShareName</span></span>

<span data-ttu-id="ab316-209">Condivisione file a cui deve essere ripristinata la condivisione file.</span><span class="sxs-lookup"><span data-stu-id="ab316-209">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="ab316-210">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="ab316-210">-TargetFolder</span></span>

<span data-ttu-id="ab316-211">Cartella in cui deve essere ripristinata la condivisione di file all'interno di TargetFileShareName.</span><span class="sxs-lookup"><span data-stu-id="ab316-211">The folder under which the file share has to be restored to within the TargetFileShareName.</span></span> <span data-ttu-id="ab316-212">Se il contenuto di cui è stato eseguito il backup deve essere ripristinato in una cartella radice, assegnare i valori della cartella di destinazione come stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="ab316-212">If the backed-up content is to be restored to a root folder, give the target folder values as an empty string.</span></span>

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

### <span data-ttu-id="ab316-213">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab316-213">-TargetResourceGroupName</span></span>

<span data-ttu-id="ab316-214">Gruppo di risorse a cui vengono ripristinati i dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="ab316-214">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="ab316-215">Applicabile al backup della VM con dischi gestiti</span><span class="sxs-lookup"><span data-stu-id="ab316-215">Applicable to backup of VM with managed disks</span></span>

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

### <span data-ttu-id="ab316-216">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ab316-216">-TargetStorageAccountName</span></span>

<span data-ttu-id="ab316-217">Account di archiviazione a cui deve essere ripristinata la condivisione file.</span><span class="sxs-lookup"><span data-stu-id="ab316-217">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="ab316-218">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ab316-218">-UseOriginalStorageAccount</span></span>

<span data-ttu-id="ab316-219">Usare questa opzione se i dischi del punto di ripristino devono essere ripristinati agli account di archiviazione originali.</span><span class="sxs-lookup"><span data-stu-id="ab316-219">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

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

### <span data-ttu-id="ab316-220">-VaultId</span><span class="sxs-lookup"><span data-stu-id="ab316-220">-VaultId</span></span>

<span data-ttu-id="ab316-221">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="ab316-221">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="ab316-222">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="ab316-222">-VaultLocation</span></span>

<span data-ttu-id="ab316-223">Posizione dell'archivio di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="ab316-223">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="ab316-224">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="ab316-224">-WLRecoveryConfig</span></span>

<span data-ttu-id="ab316-225">Configurazione di ripristino</span><span class="sxs-lookup"><span data-stu-id="ab316-225">Recovery config</span></span>

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

### <span data-ttu-id="ab316-226">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ab316-226">-Confirm</span></span>

<span data-ttu-id="ab316-227">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab316-227">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab316-228">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab316-228">-WhatIf</span></span>

<span data-ttu-id="ab316-229">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ab316-229">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="ab316-230">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab316-230">CommonParameters</span></span>
<span data-ttu-id="ab316-231">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab316-231">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab316-232">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab316-232">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab316-233">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ab316-233">INPUTS</span></span>

### <span data-ttu-id="ab316-234">System. String</span><span class="sxs-lookup"><span data-stu-id="ab316-234">System.String</span></span>

### <span data-ttu-id="ab316-235">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="ab316-235">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="ab316-236">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ab316-236">OUTPUTS</span></span>

### <span data-ttu-id="ab316-237">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="ab316-237">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="ab316-238">Note</span><span class="sxs-lookup"><span data-stu-id="ab316-238">NOTES</span></span>

## <span data-ttu-id="ab316-239">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ab316-239">RELATED LINKS</span></span>

[<span data-ttu-id="ab316-240">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="ab316-240">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="ab316-241">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="ab316-241">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="ab316-242">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="ab316-242">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
