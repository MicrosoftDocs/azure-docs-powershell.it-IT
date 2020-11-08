---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 52e4a9b76adc8c8980ab20951278435894a303bc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200674"
---
# <span data-ttu-id="8741b-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="8741b-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="8741b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8741b-102">SYNOPSIS</span></span>

<span data-ttu-id="8741b-103">Ripristina i dati e la configurazione di un elemento di backup in un punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="8741b-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

## <span data-ttu-id="8741b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8741b-104">SYNTAX</span></span>

### <span data-ttu-id="8741b-105">AzureVMParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8741b-105">AzureVMParameterSet (Default)</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8741b-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="8741b-106">AzureFileParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-MultipleSourceFilePath <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8741b-107">AzureVMRestoreAsUnmanaged</span><span class="sxs-lookup"><span data-stu-id="8741b-107">AzureVMRestoreAsUnmanaged</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-RestoreAsUnmanagedDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8741b-108">AzureVMTargetRGParameterSet</span><span class="sxs-lookup"><span data-stu-id="8741b-108">AzureVMTargetRGParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-TargetResourceGroupName] <String>
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8741b-109">AzureVMUseOSAParameterSet</span><span class="sxs-lookup"><span data-stu-id="8741b-109">AzureVMUseOSAParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-UseOriginalStorageAccount]
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8741b-110">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="8741b-110">AzureWorkloadParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8741b-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8741b-111">DESCRIPTION</span></span>

<span data-ttu-id="8741b-112">Il cmdlet **Restore-AzRecoveryServicesBackupItem** Ripristina i dati e la configurazione per un elemento di backup di Azure in un punto di recupero specificato.</span><span class="sxs-lookup"><span data-stu-id="8741b-112">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="8741b-113">Questo cmdlet avvia il ripristino dall'archivio di servizi di ripristino all'account di archiviazione del cliente.</span><span class="sxs-lookup"><span data-stu-id="8741b-113">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="8741b-114">L'operazione di ripristino non ripristina la macchina virtuale completa.</span><span class="sxs-lookup"><span data-stu-id="8741b-114">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="8741b-115">Ripristina i dischi gestiti in un gruppo di risorse di destinazione e le informazioni di configurazione nell'account di archiviazione del cliente al termine dell'operazione di ripristino, è necessario creare la macchina virtuale e avviarla.</span><span class="sxs-lookup"><span data-stu-id="8741b-115">It restores the managed disks to a target resource group and configuration information to customer storage account After the restore operation is finished, you must create the virtual machine and start it.</span></span> <span data-ttu-id="8741b-116">Per altre informazioni, refter è possibile impostare i diversi set di parametri e il testo dei parametri.</span><span class="sxs-lookup"><span data-stu-id="8741b-116">Please refter to different possible parameter sets and parameter text for more information.</span></span>
<span data-ttu-id="8741b-117">Imposta il contesto del Vault usando il parametro-VaultId.</span><span class="sxs-lookup"><span data-stu-id="8741b-117">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="8741b-118">Nota: per eseguire correttamente questo cmdlet, è anche necessario usare il parametro VaultId-VaultLocation.</span><span class="sxs-lookup"><span data-stu-id="8741b-118">Note: To successfully execute this cmdlet in addition to -VaultId parameter -VaultLocation parameter should be used as well.</span></span>

## <span data-ttu-id="8741b-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8741b-119">EXAMPLES</span></span>

### <span data-ttu-id="8741b-120">Esempio 1: ripristinare un elemento in un punto di ripristino</span><span class="sxs-lookup"><span data-stu-id="8741b-120">Example 1: Restore an item to a recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $restoreDiskLUNs = ("0", "1")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetResourceGroupName "Target_RG" -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -RestoreDiskList $restoreDiskLUNs -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="8741b-121">Il primo comando ottiene il Vault RecoveryServices e lo archivia in $vault variabile.</span><span class="sxs-lookup"><span data-stu-id="8741b-121">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="8741b-122">Il secondo comando ottiene gli elementi di backup e lo archivia nella variabile $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="8741b-122">The second command gets the Backup items and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="8741b-123">Il terzo comando ottiene la data da sette giorni prima e lo archivia nella variabile $StartDate.</span><span class="sxs-lookup"><span data-stu-id="8741b-123">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="8741b-124">Il quarto comando ottiene la data corrente e lo archivia nella variabile $EndDate.</span><span class="sxs-lookup"><span data-stu-id="8741b-124">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="8741b-125">Il quinto comando consente di ottenere un elenco di punti di ripristino per l'elemento di backup specifico filtrato da $StartDate e $EndDate.</span><span class="sxs-lookup"><span data-stu-id="8741b-125">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="8741b-126">Il sesto comando specifica i dischi da ripristinare dal punto di ripristino e lo archivia in $restoreDiskLUNs variabile.</span><span class="sxs-lookup"><span data-stu-id="8741b-126">The sixth command specifies which disks to restore from the recovery point and stores it in $restoreDiskLUNs variable.</span></span>
<span data-ttu-id="8741b-127">L'ultimo comando Ripristina i dischi nell'account di archiviazione di destinazione DestAccount nel gruppo di risorse DestRG.</span><span class="sxs-lookup"><span data-stu-id="8741b-127">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="8741b-128">Esempio 2: ripristinare più file di un elemento AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="8741b-128">Example 2: Restore Multiple files of an AzureFileShare item</span></span>

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

<span data-ttu-id="8741b-129">Il primo comando ottiene il contenitore di backup di tipo AzureVM e lo archivia nella variabile $Container.</span><span class="sxs-lookup"><span data-stu-id="8741b-129">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="8741b-130">Il secondo comando ottiene l'elemento di backup denominato fileshareitem e lo archivia nella variabile $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="8741b-130">The second command gets the Backup item named fileshareitem and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="8741b-131">Il terzo comando ottiene un elenco di punti di ripristino per l'elemento di backup specifico.</span><span class="sxs-lookup"><span data-stu-id="8741b-131">The third command gets a list of recovery points for the specific backup item.</span></span>
<span data-ttu-id="8741b-132">Il quarto comando spceifies i file da ripristinare e lo archivia in $files variabile.</span><span class="sxs-lookup"><span data-stu-id="8741b-132">The fourth command spceifies which files to restore and stores it in $files variable.</span></span>
<span data-ttu-id="8741b-133">L'ultimo comando Ripristina i file specificati nella posizione originale.</span><span class="sxs-lookup"><span data-stu-id="8741b-133">The last command restores the specified files to its original location.</span></span>

### <span data-ttu-id="8741b-134">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="8741b-134">Example 3</span></span>

<span data-ttu-id="8741b-135">Ripristina i dati e la configurazione di un elemento di backup in un punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="8741b-135">Restores the data and configuration for a Backup item to a recovery point.</span></span> <span data-ttu-id="8741b-136">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="8741b-136">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Restore-AzRecoveryServicesBackupItem -VaultId $vault.ID -WLRecoveryConfig <RecoveryConfigBase>
```
### <span data-ttu-id="8741b-137">Esempio 4: ripristinare una VM gestita come dischi gestiti</span><span class="sxs-lookup"><span data-stu-id="8741b-137">Example 4: Restore a managed VM as managed Disks</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetResourceGroupName "Target_RG" -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="8741b-138">Il primo comando ottiene il Vault RecoveryServices e lo archivia in $vault variabile.</span><span class="sxs-lookup"><span data-stu-id="8741b-138">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="8741b-139">Il secondo comando ottiene l'elemento di backup e lo archivia nella variabile $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="8741b-139">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="8741b-140">Il terzo comando ottiene la data da sette giorni prima e lo archivia nella variabile $StartDate.</span><span class="sxs-lookup"><span data-stu-id="8741b-140">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="8741b-141">Il quarto comando ottiene la data corrente e lo archivia nella variabile $EndDate.</span><span class="sxs-lookup"><span data-stu-id="8741b-141">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="8741b-142">Il quinto comando consente di ottenere un elenco di punti di ripristino per l'elemento di backup specifico filtrato da $StartDate e $EndDate.</span><span class="sxs-lookup"><span data-stu-id="8741b-142">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="8741b-143">Il sesto comando Ripristina i dischi come dischi gestiti con il gruppo di risorse di destinazione indicato.</span><span class="sxs-lookup"><span data-stu-id="8741b-143">The sixth command restores the disks as managed disks with the given target resource group.</span></span>

### <span data-ttu-id="8741b-144">Esempio 5: ripristinare una VM gestita come dischi non gestiti</span><span class="sxs-lookup"><span data-stu-id="8741b-144">Example 5: Restore a managed VM as unmanaged Disks</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -RestoreAsUnmanagedDisks -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="8741b-145">Il primo comando ottiene il Vault RecoveryServices e lo archivia in $vault variabile.</span><span class="sxs-lookup"><span data-stu-id="8741b-145">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="8741b-146">Il secondo comando ottiene l'elemento di backup e lo archivia nella variabile $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="8741b-146">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="8741b-147">Il terzo comando ottiene la data da sette giorni prima e lo archivia nella variabile $StartDate.</span><span class="sxs-lookup"><span data-stu-id="8741b-147">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="8741b-148">Il quarto comando ottiene la data corrente e lo archivia nella variabile $EndDate.</span><span class="sxs-lookup"><span data-stu-id="8741b-148">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="8741b-149">Il quinto comando consente di ottenere un elenco di punti di ripristino per l'elemento di backup specifico filtrato da $StartDate e $EndDate.</span><span class="sxs-lookup"><span data-stu-id="8741b-149">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="8741b-150">Il sesto comando Ripristina i dischi come dischi non gestiti.</span><span class="sxs-lookup"><span data-stu-id="8741b-150">The sixth command restores the disks as unmanaged disks.</span></span>

### <span data-ttu-id="8741b-151">Esempio 6: ripristinare una VM non gestita come dischi non gestiti con l'account di archiviazione originale.</span><span class="sxs-lookup"><span data-stu-id="8741b-151">Example 6: Restore an unmanaged VM as unmanaged Disks using original storage account.</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -UseOriginalStorageAccount -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="8741b-152">Il primo comando ottiene il Vault RecoveryServices e lo archivia in $vault variabile.</span><span class="sxs-lookup"><span data-stu-id="8741b-152">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="8741b-153">Il secondo comando ottiene l'elemento di backup e lo archivia nella variabile $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="8741b-153">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="8741b-154">Il terzo comando ottiene la data da sette giorni prima e lo archivia nella variabile $StartDate.</span><span class="sxs-lookup"><span data-stu-id="8741b-154">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="8741b-155">Il quarto comando ottiene la data corrente e lo archivia nella variabile $EndDate.</span><span class="sxs-lookup"><span data-stu-id="8741b-155">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="8741b-156">Il quinto comando consente di ottenere un elenco di punti di ripristino per l'elemento di backup specifico filtrato da $StartDate e $EndDate.</span><span class="sxs-lookup"><span data-stu-id="8741b-156">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="8741b-157">Il sesto comando Ripristina i dischi come dischi non gestiti usando l'account di archiviazione originale della VM.</span><span class="sxs-lookup"><span data-stu-id="8741b-157">The sixth command restores the disks as unmanaged disks using the original storage account of the VM.</span></span>

## <span data-ttu-id="8741b-158">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8741b-158">PARAMETERS</span></span>

### <span data-ttu-id="8741b-159">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8741b-159">-DefaultProfile</span></span>

<span data-ttu-id="8741b-160">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8741b-160">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8741b-161">-MultipleSourceFilePath</span><span class="sxs-lookup"><span data-stu-id="8741b-161">-MultipleSourceFilePath</span></span>
<span data-ttu-id="8741b-162">Usato per il ripristino di più file da una condivisione file.</span><span class="sxs-lookup"><span data-stu-id="8741b-162">Used for Multiple files restore from a file share.</span></span> <span data-ttu-id="8741b-163">Percorsi degli elementi da ripristinare all'interno della condivisione file.</span><span class="sxs-lookup"><span data-stu-id="8741b-163">The paths of the items to be restored within the file share.</span></span>

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

### <span data-ttu-id="8741b-164">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="8741b-164">-RecoveryPoint</span></span>

<span data-ttu-id="8741b-165">Specifica il punto di ripristino a cui ripristinare l'elemento di backup.</span><span class="sxs-lookup"><span data-stu-id="8741b-165">Specifies the recovery point to which to restore the backup item.</span></span>
<span data-ttu-id="8741b-166">Per ottenere un oggetto **AzureRmRecoveryServicesBackupRecoveryPoint** , usa il cmdlet **Get-AzRecoveryServicesBackupRecoveryPoint** .</span><span class="sxs-lookup"><span data-stu-id="8741b-166">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet.</span></span>

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

### <span data-ttu-id="8741b-167">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="8741b-167">-ResolveConflict</span></span>

<span data-ttu-id="8741b-168">Se l'elemento ripristinato esiste anche nella destinazione, usare questa opzione per indicare se sovrascriverlo o meno.</span><span class="sxs-lookup"><span data-stu-id="8741b-168">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>
<span data-ttu-id="8741b-169">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="8741b-169">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8741b-170">Sovrascrivere</span><span class="sxs-lookup"><span data-stu-id="8741b-170">Overwrite</span></span>
- <span data-ttu-id="8741b-171">Ignorare</span><span class="sxs-lookup"><span data-stu-id="8741b-171">Skip</span></span>

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

### <span data-ttu-id="8741b-172">-RestoreAsUnmanagedDisks</span><span class="sxs-lookup"><span data-stu-id="8741b-172">-RestoreAsUnmanagedDisks</span></span>
<span data-ttu-id="8741b-173">Usare questa opzione per specificare il ripristino come dischi non gestiti</span><span class="sxs-lookup"><span data-stu-id="8741b-173">Use this switch to specify to restore as unmanaged disks</span></span>

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

### <span data-ttu-id="8741b-174">-RestoreDiskList</span><span class="sxs-lookup"><span data-stu-id="8741b-174">-RestoreDiskList</span></span>
<span data-ttu-id="8741b-175">Specificare i dischi da recuperare della VM di cui è stato eseguito il backup</span><span class="sxs-lookup"><span data-stu-id="8741b-175">Specify which disks to recover of the backed up VM</span></span>

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

### <span data-ttu-id="8741b-176">-RestoreOnlyOSDisk</span><span class="sxs-lookup"><span data-stu-id="8741b-176">-RestoreOnlyOSDisk</span></span>
<span data-ttu-id="8741b-177">Usare questa opzione per ripristinare solo i dischi del sistema operativo di una VM di cui è stato eseguito il backup</span><span class="sxs-lookup"><span data-stu-id="8741b-177">Use this switch to restore only OS disks of a backed up VM</span></span>

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

### <span data-ttu-id="8741b-178">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="8741b-178">-SourceFilePath</span></span>

<span data-ttu-id="8741b-179">Usato per un determinato ripristino degli elementi da una condivisione file.</span><span class="sxs-lookup"><span data-stu-id="8741b-179">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="8741b-180">Percorso dell'elemento da ripristinare all'interno della condivisione file.</span><span class="sxs-lookup"><span data-stu-id="8741b-180">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="8741b-181">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="8741b-181">-SourceFileType</span></span>

<span data-ttu-id="8741b-182">Usato per un determinato ripristino degli elementi da una condivisione file.</span><span class="sxs-lookup"><span data-stu-id="8741b-182">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="8741b-183">Tipo dell'elemento da ripristinare all'interno della condivisione file.</span><span class="sxs-lookup"><span data-stu-id="8741b-183">The type of the item to be restored within the file share.</span></span>
<span data-ttu-id="8741b-184">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="8741b-184">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8741b-185">File</span><span class="sxs-lookup"><span data-stu-id="8741b-185">File</span></span>
- <span data-ttu-id="8741b-186">Directory</span><span class="sxs-lookup"><span data-stu-id="8741b-186">Directory</span></span>

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

### <span data-ttu-id="8741b-187">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8741b-187">-StorageAccountName</span></span>

<span data-ttu-id="8741b-188">Specifica il nome dell'account di archiviazione di destinazione nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="8741b-188">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="8741b-189">Come parte del processo di ripristino, questo cmdlet archivia i dischi e le informazioni di configurazione in questo account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="8741b-189">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="8741b-190">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8741b-190">-StorageAccountResourceGroupName</span></span>

<span data-ttu-id="8741b-191">Specifica il nome del gruppo di risorse che contiene l'account di archiviazione di destinazione nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="8741b-191">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="8741b-192">Come parte del processo di ripristino, questo cmdlet archivia i dischi e le informazioni di configurazione in questo account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="8741b-192">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="8741b-193">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="8741b-193">-TargetFileShareName</span></span>

<span data-ttu-id="8741b-194">Condivisione file a cui deve essere ripristinata la condivisione file.</span><span class="sxs-lookup"><span data-stu-id="8741b-194">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="8741b-195">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="8741b-195">-TargetFolder</span></span>

<span data-ttu-id="8741b-196">Cartella in cui deve essere ripristinata la condivisione di file all'interno di TargetFileShareName.</span><span class="sxs-lookup"><span data-stu-id="8741b-196">The folder under which the file share has to be restored to within the TargetFileShareName.</span></span> <span data-ttu-id="8741b-197">Se il contenuto di cui è stato eseguito il backup deve essere ripristinato in una cartella radice, assegnare i valori della cartella di destinazione come stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="8741b-197">If the backed-up content is to be restored to a root folder, give the target folder values as an empty string.</span></span>

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

### <span data-ttu-id="8741b-198">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8741b-198">-TargetResourceGroupName</span></span>

<span data-ttu-id="8741b-199">Gruppo di risorse a cui vengono ripristinati i dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="8741b-199">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="8741b-200">Applicabile al backup della VM con dischi gestiti</span><span class="sxs-lookup"><span data-stu-id="8741b-200">Applicable to backup of VM with managed disks</span></span>

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

### <span data-ttu-id="8741b-201">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8741b-201">-TargetStorageAccountName</span></span>

<span data-ttu-id="8741b-202">Account di archiviazione a cui deve essere ripristinata la condivisione file.</span><span class="sxs-lookup"><span data-stu-id="8741b-202">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="8741b-203">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8741b-203">-UseOriginalStorageAccount</span></span>

<span data-ttu-id="8741b-204">Usare questa opzione se i dischi del punto di ripristino devono essere ripristinati agli account di archiviazione originali.</span><span class="sxs-lookup"><span data-stu-id="8741b-204">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

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

### <span data-ttu-id="8741b-205">-VaultId</span><span class="sxs-lookup"><span data-stu-id="8741b-205">-VaultId</span></span>

<span data-ttu-id="8741b-206">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="8741b-206">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="8741b-207">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="8741b-207">-VaultLocation</span></span>

<span data-ttu-id="8741b-208">Posizione dell'archivio di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="8741b-208">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="8741b-209">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="8741b-209">-WLRecoveryConfig</span></span>

<span data-ttu-id="8741b-210">Configurazione di ripristino</span><span class="sxs-lookup"><span data-stu-id="8741b-210">Recovery config</span></span>

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

### <span data-ttu-id="8741b-211">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8741b-211">-Confirm</span></span>

<span data-ttu-id="8741b-212">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8741b-212">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8741b-213">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8741b-213">-WhatIf</span></span>

<span data-ttu-id="8741b-214">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8741b-214">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="8741b-215">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8741b-215">CommonParameters</span></span>
<span data-ttu-id="8741b-216">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8741b-216">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8741b-217">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8741b-217">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8741b-218">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8741b-218">INPUTS</span></span>

### <span data-ttu-id="8741b-219">System. String</span><span class="sxs-lookup"><span data-stu-id="8741b-219">System.String</span></span>

### <span data-ttu-id="8741b-220">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="8741b-220">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="8741b-221">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8741b-221">OUTPUTS</span></span>

### <span data-ttu-id="8741b-222">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="8741b-222">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="8741b-223">Note</span><span class="sxs-lookup"><span data-stu-id="8741b-223">NOTES</span></span>

## <span data-ttu-id="8741b-224">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8741b-224">RELATED LINKS</span></span>

[<span data-ttu-id="8741b-225">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="8741b-225">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="8741b-226">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="8741b-226">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="8741b-227">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="8741b-227">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
