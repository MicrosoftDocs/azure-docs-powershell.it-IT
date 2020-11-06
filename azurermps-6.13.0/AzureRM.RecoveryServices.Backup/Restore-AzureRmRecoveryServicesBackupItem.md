---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/restore-azurermrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: b454f77bc3ad00ddf604e13672d61a7445c44fed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507367"
---
# <span data-ttu-id="5b84e-101">Restore-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="5b84e-101">Restore-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="5b84e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5b84e-102">SYNOPSIS</span></span>
<span data-ttu-id="5b84e-103">Ripristina i dati e la configurazione di un elemento di backup in un punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="5b84e-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b84e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5b84e-104">SYNTAX</span></span>

### <span data-ttu-id="5b84e-105">AzureVMParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5b84e-105">AzureVMParameterSet (Default)</span></span>
```
Restore-AzureRmRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 [[-TargetResourceGroupName] <String>] [-UseOriginalStorageAccount] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b84e-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b84e-106">AzureFileParameterSet</span></span>
```
Restore-AzureRmRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 -ResolveConflict <RestoreFSResolveConfictOption> [-SourceFilePath <String>] [-SourceFileType <SourceFileType>]
 [-TargetStorageAccountName <String>] [-TargetFileShareName <String>] [-TargetFolder <String>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b84e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5b84e-107">DESCRIPTION</span></span>
<span data-ttu-id="5b84e-108">Il cmdlet **Restore-AzureRmRecoveryServicesBackupItem** Ripristina i dati e la configurazione per un elemento di backup di Azure in un punto di recupero specificato.</span><span class="sxs-lookup"><span data-stu-id="5b84e-108">The **Restore-AzureRmRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="5b84e-109">Questo cmdlet avvia il ripristino dall'archivio di servizi di ripristino all'account di archiviazione del cliente.</span><span class="sxs-lookup"><span data-stu-id="5b84e-109">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="5b84e-110">L'operazione di ripristino non ripristina la macchina virtuale completa.</span><span class="sxs-lookup"><span data-stu-id="5b84e-110">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="5b84e-111">Ripristina i dati del disco e le informazioni di configurazione.</span><span class="sxs-lookup"><span data-stu-id="5b84e-111">It restores the disk data and configuration information.</span></span>
<span data-ttu-id="5b84e-112">Al termine dell'operazione di ripristino, è necessario creare la macchina virtuale e avviarla.</span><span class="sxs-lookup"><span data-stu-id="5b84e-112">After the restore operation is finished, you must create the virtual machine and start it.</span></span>
<span data-ttu-id="5b84e-113">Impostare il contesto del Vault usando il cmdlet Set-AzureRmRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="5b84e-113">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="5b84e-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5b84e-114">EXAMPLES</span></span>

### <span data-ttu-id="5b84e-115">Esempio 1: ripristinare un elemento in un punto di ripristino</span><span class="sxs-lookup"><span data-stu-id="5b84e-115">Example 1: Restore an item to a recovery point</span></span>
```
PS C:\>$Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM 
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzureRmRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() 
PS C:\> $RestoreJob = Restore-AzureRmRecoveryServicesBackupItem -RecoveryPoint $RP[0] -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG"
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="5b84e-116">Il primo comando ottiene il contenitore di backup di tipo AzureVM e lo archivia nella variabile $Container.</span><span class="sxs-lookup"><span data-stu-id="5b84e-116">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="5b84e-117">Il secondo comando ottiene l'elemento di backup denominato V2VM da $Container e lo archivia nella variabile $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="5b84e-117">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="5b84e-118">Il terzo comando ottiene la data da sette giorni prima e lo archivia nella variabile $StartDate.</span><span class="sxs-lookup"><span data-stu-id="5b84e-118">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="5b84e-119">Il quarto comando ottiene la data corrente e lo archivia nella variabile $EndDate.</span><span class="sxs-lookup"><span data-stu-id="5b84e-119">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="5b84e-120">Il quinto comando consente di ottenere un elenco di punti di ripristino per l'elemento di backup specifico filtrato da $StartDate e $EndDate.</span><span class="sxs-lookup"><span data-stu-id="5b84e-120">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="5b84e-121">L'intervallo di date specificato è gli ultimi 7 giorni.</span><span class="sxs-lookup"><span data-stu-id="5b84e-121">The date range specified is the last 7 days.</span></span>
<span data-ttu-id="5b84e-122">L'ultimo comando Ripristina i dischi nell'account di archiviazione di destinazione DestAccount nel gruppo di risorse DestRG.</span><span class="sxs-lookup"><span data-stu-id="5b84e-122">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

## <span data-ttu-id="5b84e-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5b84e-123">PARAMETERS</span></span>

### <span data-ttu-id="5b84e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b84e-124">-DefaultProfile</span></span>
<span data-ttu-id="5b84e-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5b84e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b84e-126">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="5b84e-126">-RecoveryPoint</span></span>
<span data-ttu-id="5b84e-127">Specifica il punto di ripristino a cui ripristinare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5b84e-127">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="5b84e-128">Per ottenere un oggetto **AzureRmRecoveryServicesBackupRecoveryPoint** , usa il cmdlet Get-AzureRmRecoveryServicesBackupRecoveryPoint.</span><span class="sxs-lookup"><span data-stu-id="5b84e-128">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the Get-AzureRmRecoveryServicesBackupRecoveryPoint cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b84e-129">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="5b84e-129">-ResolveConflict</span></span>
<span data-ttu-id="5b84e-130">Se l'elemento ripristinato esiste anche nella destinazione, usare questa opzione per indicare se sovrascriverlo o meno.</span><span class="sxs-lookup"><span data-stu-id="5b84e-130">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RestoreFSResolveConfictOption
Parameter Sets: AzureFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b84e-131">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="5b84e-131">-SourceFilePath</span></span>
<span data-ttu-id="5b84e-132">Usato per un determinato ripristino degli elementi da una condivisione file.</span><span class="sxs-lookup"><span data-stu-id="5b84e-132">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="5b84e-133">Percorso dell'elemento da ripristinare all'interno della condivisione file.</span><span class="sxs-lookup"><span data-stu-id="5b84e-133">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="5b84e-134">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="5b84e-134">-SourceFileType</span></span>
<span data-ttu-id="5b84e-135">Usato per un determinato ripristino degli elementi da una condivisione file.</span><span class="sxs-lookup"><span data-stu-id="5b84e-135">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="5b84e-136">Percorso dell'elemento da ripristinare all'interno della condivisione file.</span><span class="sxs-lookup"><span data-stu-id="5b84e-136">The path of the item to be restored within the file share.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SourceFileType
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b84e-137">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5b84e-137">-StorageAccountName</span></span>
<span data-ttu-id="5b84e-138">Specifica il nome dell'account di archiviazione di destinazione nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="5b84e-138">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="5b84e-139">Come parte del processo di ripristino, questo cmdlet archivia i dischi e le informazioni di configurazione in questo account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="5b84e-139">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b84e-140">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b84e-140">-StorageAccountResourceGroupName</span></span>
<span data-ttu-id="5b84e-141">Specifica il nome del gruppo di risorse che contiene l'account di archiviazione di destinazione nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="5b84e-141">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="5b84e-142">Come parte del processo di ripristino, questo cmdlet archivia i dischi e le informazioni di configurazione in questo account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="5b84e-142">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b84e-143">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="5b84e-143">-TargetFileShareName</span></span>
<span data-ttu-id="5b84e-144">Condivisione file a cui deve essere ripristinata la condivisione file.</span><span class="sxs-lookup"><span data-stu-id="5b84e-144">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="5b84e-145">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="5b84e-145">-TargetFolder</span></span>
<span data-ttu-id="5b84e-146">Cartella in cui deve essere ripristinata la condivisione di file all'interno di targetFileShareName. uscire dalla variabile Empty per ripristinare in root folder.</span><span class="sxs-lookup"><span data-stu-id="5b84e-146">The folder under which the file share has to be restored to within the targetFileShareName.Leave the variable empty to restore under root folder.</span></span>

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

### <span data-ttu-id="5b84e-147">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b84e-147">-TargetResourceGroupName</span></span>
<span data-ttu-id="5b84e-148">Gruppo di risorse a cui vengono ripristinati i dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="5b84e-148">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="5b84e-149">Applicabile al backup della VM con dischi gestiti</span><span class="sxs-lookup"><span data-stu-id="5b84e-149">Applicable to backup of VM with managed disks</span></span>

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

### <span data-ttu-id="5b84e-150">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5b84e-150">-TargetStorageAccountName</span></span>
<span data-ttu-id="5b84e-151">Account di archiviazione a cui deve essere ripristinata la condivisione file.</span><span class="sxs-lookup"><span data-stu-id="5b84e-151">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="5b84e-152">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5b84e-152">-UseOriginalStorageAccount</span></span>
<span data-ttu-id="5b84e-153">Usare questa opzione se i dischi del punto di ripristino devono essere ripristinati agli account di archiviazione originali.</span><span class="sxs-lookup"><span data-stu-id="5b84e-153">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

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

### <span data-ttu-id="5b84e-154">-VaultId</span><span class="sxs-lookup"><span data-stu-id="5b84e-154">-VaultId</span></span>
<span data-ttu-id="5b84e-155">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="5b84e-155">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="5b84e-156">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="5b84e-156">-VaultLocation</span></span>
<span data-ttu-id="5b84e-157">Posizione dell'archivio di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="5b84e-157">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="5b84e-158">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5b84e-158">-Confirm</span></span>
<span data-ttu-id="5b84e-159">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b84e-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b84e-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b84e-160">-WhatIf</span></span>
<span data-ttu-id="5b84e-161">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5b84e-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5b84e-162">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5b84e-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b84e-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b84e-163">CommonParameters</span></span>
<span data-ttu-id="5b84e-164">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b84e-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b84e-165">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b84e-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b84e-166">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5b84e-166">INPUTS</span></span>

### <span data-ttu-id="5b84e-167">System. String</span><span class="sxs-lookup"><span data-stu-id="5b84e-167">System.String</span></span>
<span data-ttu-id="5b84e-168">Parametri: VaultId (ByValue), VaultLocation (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5b84e-168">Parameters: VaultId (ByValue), VaultLocation (ByValue)</span></span>

### <span data-ttu-id="5b84e-169">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="5b84e-169">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="5b84e-170">Parametri: RecoveryPoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5b84e-170">Parameters: RecoveryPoint (ByValue)</span></span>

## <span data-ttu-id="5b84e-171">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5b84e-171">OUTPUTS</span></span>

### <span data-ttu-id="5b84e-172">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="5b84e-172">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="5b84e-173">Note</span><span class="sxs-lookup"><span data-stu-id="5b84e-173">NOTES</span></span>

## <span data-ttu-id="5b84e-174">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5b84e-174">RELATED LINKS</span></span>

[<span data-ttu-id="5b84e-175">Backup-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="5b84e-175">Backup-AzureRmRecoveryServicesBackupItem</span></span>](./Backup-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="5b84e-176">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="5b84e-176">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="5b84e-177">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="5b84e-177">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)


