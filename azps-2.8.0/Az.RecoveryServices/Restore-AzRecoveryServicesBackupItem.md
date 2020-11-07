---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 87051d6e8c5dabe5a5e5c5138e06eda0de961219
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855637"
---
# <span data-ttu-id="35f30-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="35f30-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="35f30-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="35f30-102">SYNOPSIS</span></span>

<span data-ttu-id="35f30-103">Ripristina i dati e la configurazione di un elemento di backup in un punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="35f30-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

## <span data-ttu-id="35f30-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="35f30-104">SYNTAX</span></span>

### <span data-ttu-id="35f30-105">AzureVMParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="35f30-105">AzureVMParameterSet (Default)</span></span>

```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 [[-TargetResourceGroupName] <String>] [-UseOriginalStorageAccount] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35f30-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="35f30-106">AzureFileParameterSet</span></span>

```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="35f30-107">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="35f30-107">AzureWorkloadParameterSet</span></span>

```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35f30-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="35f30-108">DESCRIPTION</span></span>

<span data-ttu-id="35f30-109">Il cmdlet **Restore-AzRecoveryServicesBackupItem** Ripristina i dati e la configurazione per un elemento di backup di Azure in un punto di recupero specificato.</span><span class="sxs-lookup"><span data-stu-id="35f30-109">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="35f30-110">Questo cmdlet avvia il ripristino dall'archivio di servizi di ripristino all'account di archiviazione del cliente.</span><span class="sxs-lookup"><span data-stu-id="35f30-110">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="35f30-111">L'operazione di ripristino non ripristina la macchina virtuale completa.</span><span class="sxs-lookup"><span data-stu-id="35f30-111">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="35f30-112">Ripristina i dati del disco e le informazioni di configurazione.</span><span class="sxs-lookup"><span data-stu-id="35f30-112">It restores the disk data and configuration information.</span></span>
<span data-ttu-id="35f30-113">Al termine dell'operazione di ripristino, è necessario creare la macchina virtuale e avviarla.</span><span class="sxs-lookup"><span data-stu-id="35f30-113">After the restore operation is finished, you must create the virtual machine and start it.</span></span>
<span data-ttu-id="35f30-114">Imposta il contesto del Vault usando il parametro-VaultId.</span><span class="sxs-lookup"><span data-stu-id="35f30-114">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="35f30-115">Nota: per eseguire correttamente questo cmdlet, è anche necessario usare il parametro VaultId-VaultLocation.</span><span class="sxs-lookup"><span data-stu-id="35f30-115">Note: To successfully execute this cmdlet in addition to -VaultId parameter -VaultLocation parameter should be used as well.</span></span>

## <span data-ttu-id="35f30-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="35f30-116">EXAMPLES</span></span>

### <span data-ttu-id="35f30-117">Esempio 1: ripristinare un elemento in un punto di ripristino</span><span class="sxs-lookup"><span data-stu-id="35f30-117">Example 1: Restore an item to a recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\>$Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="35f30-118">Il primo comando ottiene il contenitore di backup di tipo AzureVM e lo archivia nella variabile $Container.</span><span class="sxs-lookup"><span data-stu-id="35f30-118">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="35f30-119">Il secondo comando ottiene l'elemento di backup denominato V2VM da $Container e lo archivia nella variabile $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="35f30-119">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="35f30-120">Il terzo comando ottiene la data da sette giorni prima e lo archivia nella variabile $StartDate.</span><span class="sxs-lookup"><span data-stu-id="35f30-120">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="35f30-121">Il quarto comando ottiene la data corrente e lo archivia nella variabile $EndDate.</span><span class="sxs-lookup"><span data-stu-id="35f30-121">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="35f30-122">Il quinto comando consente di ottenere un elenco di punti di ripristino per l'elemento di backup specifico filtrato da $StartDate e $EndDate.</span><span class="sxs-lookup"><span data-stu-id="35f30-122">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="35f30-123">L'intervallo di date specificato è gli ultimi 7 giorni.</span><span class="sxs-lookup"><span data-stu-id="35f30-123">The date range specified is the last 7 days.</span></span>
<span data-ttu-id="35f30-124">L'ultimo comando Ripristina i dischi nell'account di archiviazione di destinazione DestAccount nel gruppo di risorse DestRG.</span><span class="sxs-lookup"><span data-stu-id="35f30-124">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

## <span data-ttu-id="35f30-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="35f30-125">PARAMETERS</span></span>

### <span data-ttu-id="35f30-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35f30-126">-DefaultProfile</span></span>

<span data-ttu-id="35f30-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="35f30-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35f30-128">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="35f30-128">-RecoveryPoint</span></span>

<span data-ttu-id="35f30-129">Specifica il punto di ripristino a cui ripristinare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="35f30-129">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="35f30-130">Per ottenere un oggetto **AzureRmRecoveryServicesBackupRecoveryPoint** , usa il cmdlet **Get-AzRecoveryServicesBackupRecoveryPoint** .</span><span class="sxs-lookup"><span data-stu-id="35f30-130">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet.</span></span>

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

### <span data-ttu-id="35f30-131">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="35f30-131">-ResolveConflict</span></span>

<span data-ttu-id="35f30-132">Se l'elemento ripristinato esiste anche nella destinazione, usare questa opzione per indicare se sovrascriverlo o meno.</span><span class="sxs-lookup"><span data-stu-id="35f30-132">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>
<span data-ttu-id="35f30-133">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="35f30-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="35f30-134">Sovrascrivere</span><span class="sxs-lookup"><span data-stu-id="35f30-134">Overwrite</span></span>
- <span data-ttu-id="35f30-135">Ignorare</span><span class="sxs-lookup"><span data-stu-id="35f30-135">Skip</span></span>

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

### <span data-ttu-id="35f30-136">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="35f30-136">-SourceFilePath</span></span>

<span data-ttu-id="35f30-137">Usato per un determinato ripristino degli elementi da una condivisione file.</span><span class="sxs-lookup"><span data-stu-id="35f30-137">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="35f30-138">Percorso dell'elemento da ripristinare all'interno della condivisione file.</span><span class="sxs-lookup"><span data-stu-id="35f30-138">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="35f30-139">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="35f30-139">-SourceFileType</span></span>

<span data-ttu-id="35f30-140">Usato per un determinato ripristino degli elementi da una condivisione file.</span><span class="sxs-lookup"><span data-stu-id="35f30-140">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="35f30-141">Tipo dell'elemento da ripristinare all'interno della condivisione file.</span><span class="sxs-lookup"><span data-stu-id="35f30-141">The type of the item to be restored within the file share.</span></span>
<span data-ttu-id="35f30-142">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="35f30-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="35f30-143">File</span><span class="sxs-lookup"><span data-stu-id="35f30-143">File</span></span>
- <span data-ttu-id="35f30-144">Directory</span><span class="sxs-lookup"><span data-stu-id="35f30-144">Directory</span></span>

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

### <span data-ttu-id="35f30-145">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="35f30-145">-StorageAccountName</span></span>

<span data-ttu-id="35f30-146">Specifica il nome dell'account di archiviazione di destinazione nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="35f30-146">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="35f30-147">Come parte del processo di ripristino, questo cmdlet archivia i dischi e le informazioni di configurazione in questo account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="35f30-147">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="35f30-148">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35f30-148">-StorageAccountResourceGroupName</span></span>

<span data-ttu-id="35f30-149">Specifica il nome del gruppo di risorse che contiene l'account di archiviazione di destinazione nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="35f30-149">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="35f30-150">Come parte del processo di ripristino, questo cmdlet archivia i dischi e le informazioni di configurazione in questo account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="35f30-150">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="35f30-151">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="35f30-151">-TargetFileShareName</span></span>

<span data-ttu-id="35f30-152">Condivisione file a cui deve essere ripristinata la condivisione file.</span><span class="sxs-lookup"><span data-stu-id="35f30-152">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="35f30-153">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="35f30-153">-TargetFolder</span></span>

<span data-ttu-id="35f30-154">Cartella in cui deve essere ripristinata la condivisione di file all'interno di TargetFileShareName.</span><span class="sxs-lookup"><span data-stu-id="35f30-154">The folder under which the file share has to be restored to within the TargetFileShareName.</span></span> <span data-ttu-id="35f30-155">Se il contenuto di cui è stato eseguito il backup deve essere ripristinato in una cartella radice, assegnare i valori della cartella di destinazione come stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="35f30-155">If the backed-up content is to be restored to a root folder, give the target folder values as an empty string.</span></span>

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

### <span data-ttu-id="35f30-156">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35f30-156">-TargetResourceGroupName</span></span>

<span data-ttu-id="35f30-157">Gruppo di risorse a cui vengono ripristinati i dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="35f30-157">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="35f30-158">Applicabile al backup della VM con dischi gestiti</span><span class="sxs-lookup"><span data-stu-id="35f30-158">Applicable to backup of VM with managed disks</span></span>

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

### <span data-ttu-id="35f30-159">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="35f30-159">-TargetStorageAccountName</span></span>

<span data-ttu-id="35f30-160">Account di archiviazione a cui deve essere ripristinata la condivisione file.</span><span class="sxs-lookup"><span data-stu-id="35f30-160">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="35f30-161">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="35f30-161">-UseOriginalStorageAccount</span></span>

<span data-ttu-id="35f30-162">Usare questa opzione se i dischi del punto di ripristino devono essere ripristinati agli account di archiviazione originali.</span><span class="sxs-lookup"><span data-stu-id="35f30-162">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

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

### <span data-ttu-id="35f30-163">-VaultId</span><span class="sxs-lookup"><span data-stu-id="35f30-163">-VaultId</span></span>

<span data-ttu-id="35f30-164">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="35f30-164">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="35f30-165">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="35f30-165">-VaultLocation</span></span>

<span data-ttu-id="35f30-166">Posizione dell'archivio di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="35f30-166">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="35f30-167">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="35f30-167">-WLRecoveryConfig</span></span>

<span data-ttu-id="35f30-168">Configurazione di ripristino</span><span class="sxs-lookup"><span data-stu-id="35f30-168">Recovery config</span></span>

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

### <span data-ttu-id="35f30-169">-Confermare</span><span class="sxs-lookup"><span data-stu-id="35f30-169">-Confirm</span></span>

<span data-ttu-id="35f30-170">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35f30-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35f30-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35f30-171">-WhatIf</span></span>

<span data-ttu-id="35f30-172">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35f30-172">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="35f30-173">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35f30-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35f30-174">-CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35f30-174">-CommonParameters</span></span>

<span data-ttu-id="35f30-175">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35f30-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35f30-176">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35f30-176">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35f30-177">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="35f30-177">INPUTS</span></span>

### <span data-ttu-id="35f30-178">System. String</span><span class="sxs-lookup"><span data-stu-id="35f30-178">System.String</span></span>

### <span data-ttu-id="35f30-179">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="35f30-179">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="35f30-180">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="35f30-180">OUTPUTS</span></span>

### <span data-ttu-id="35f30-181">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="35f30-181">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="35f30-182">Note</span><span class="sxs-lookup"><span data-stu-id="35f30-182">NOTES</span></span>

## <span data-ttu-id="35f30-183">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="35f30-183">RELATED LINKS</span></span>

[<span data-ttu-id="35f30-184">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="35f30-184">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="35f30-185">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="35f30-185">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="35f30-186">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="35f30-186">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
