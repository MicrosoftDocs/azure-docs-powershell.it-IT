---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/restore-azurermrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: 6013531367f5996924da1776c0062ebb5ad02b90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509723"
---
# <span data-ttu-id="202c4-101">Restore-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="202c4-101">Restore-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="202c4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="202c4-102">SYNOPSIS</span></span>
<span data-ttu-id="202c4-103">Ripristina i dati e la configurazione di un elemento di backup in un punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="202c4-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="202c4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="202c4-104">SYNTAX</span></span>

```
Restore-AzureRmRecoveryServicesBackupItem [-RecoveryPoint] <RecoveryPointBase> [-StorageAccountName] <String>
 [-StorageAccountResourceGroupName] <String> [-UseOriginalStorageAccount]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="202c4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="202c4-105">DESCRIPTION</span></span>
<span data-ttu-id="202c4-106">Il cmdlet **Restore-AzureRmRecoveryServicesBackupItem** Ripristina i dati e la configurazione per un elemento di backup di Azure in un punto di recupero specificato.</span><span class="sxs-lookup"><span data-stu-id="202c4-106">The **Restore-AzureRmRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="202c4-107">Questo cmdlet avvia il ripristino dall'archivio di servizi di ripristino all'account di archiviazione del cliente.</span><span class="sxs-lookup"><span data-stu-id="202c4-107">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>

<span data-ttu-id="202c4-108">L'operazione di ripristino non ripristina la macchina virtuale completa.</span><span class="sxs-lookup"><span data-stu-id="202c4-108">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="202c4-109">Ripristina i dati del disco e le informazioni di configurazione.</span><span class="sxs-lookup"><span data-stu-id="202c4-109">It restores the disk data and configuration information.</span></span>
<span data-ttu-id="202c4-110">Al termine dell'operazione di ripristino, è necessario creare la macchina virtuale e avviarla.</span><span class="sxs-lookup"><span data-stu-id="202c4-110">After the restore operation is finished, you must create the virtual machine and start it.</span></span>

<span data-ttu-id="202c4-111">Impostare il contesto del Vault usando il cmdlet Set-AzureRmRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="202c4-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="202c4-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="202c4-112">EXAMPLES</span></span>

### <span data-ttu-id="202c4-113">Esempio 1: ripristinare un elemento in un punto di ripristino</span><span class="sxs-lookup"><span data-stu-id="202c4-113">Example 1: Restore an item to a recovery point</span></span>
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

<span data-ttu-id="202c4-114">Il primo comando ottiene il contenitore di backup di tipo AzureVM e lo archivia nella variabile $Container.</span><span class="sxs-lookup"><span data-stu-id="202c4-114">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="202c4-115">Il secondo comando ottiene l'elemento di backup denominato V2VM da $Container e lo archivia nella variabile $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="202c4-115">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>

<span data-ttu-id="202c4-116">Il terzo comando ottiene la data da sette giorni prima e lo archivia nella variabile $StartDate.</span><span class="sxs-lookup"><span data-stu-id="202c4-116">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>

<span data-ttu-id="202c4-117">Il quarto comando ottiene la data corrente e lo archivia nella variabile $EndDate.</span><span class="sxs-lookup"><span data-stu-id="202c4-117">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>

<span data-ttu-id="202c4-118">Il quinto comando consente di ottenere un elenco di punti di ripristino per l'elemento di backup specifico filtrato da $StartDate e $EndDate.</span><span class="sxs-lookup"><span data-stu-id="202c4-118">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="202c4-119">L'intervallo di date specificato è gli ultimi 7 giorni.</span><span class="sxs-lookup"><span data-stu-id="202c4-119">The date range specified is the last 7 days.</span></span>

<span data-ttu-id="202c4-120">L'ultimo comando Ripristina i dischi nell'account di archiviazione di destinazione DestAccount nel gruppo di risorse DestRG.</span><span class="sxs-lookup"><span data-stu-id="202c4-120">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

## <span data-ttu-id="202c4-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="202c4-121">PARAMETERS</span></span>

### <span data-ttu-id="202c4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="202c4-122">-DefaultProfile</span></span>
<span data-ttu-id="202c4-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="202c4-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="202c4-124">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="202c4-124">-RecoveryPoint</span></span>
<span data-ttu-id="202c4-125">Specifica il punto di ripristino a cui ripristinare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="202c4-125">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="202c4-126">Per ottenere un oggetto **AzureRmRecoveryServicesBackupRecoveryPoint** , usa il cmdlet Get-AzureRmRecoveryServicesBackupRecoveryPoint.</span><span class="sxs-lookup"><span data-stu-id="202c4-126">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the Get-AzureRmRecoveryServicesBackupRecoveryPoint cmdlet.</span></span>

```yaml
Type: RecoveryPointBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="202c4-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="202c4-127">-StorageAccountName</span></span>
<span data-ttu-id="202c4-128">Specifica il nome dell'account di archiviazione di destinazione nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="202c4-128">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="202c4-129">Come parte del processo di ripristino, questo cmdlet archivia i dischi e le informazioni di configurazione in questo account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="202c4-129">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="202c4-130">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="202c4-130">-StorageAccountResourceGroupName</span></span>
<span data-ttu-id="202c4-131">Specifica il nome del gruppo di risorse che contiene l'account di archiviazione di destinazione nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="202c4-131">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="202c4-132">Come parte del processo di ripristino, questo cmdlet archivia i dischi e le informazioni di configurazione in questo account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="202c4-132">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="202c4-133">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="202c4-133">-UseOriginalStorageAccount</span></span>
<span data-ttu-id="202c4-134">Usare questa opzione se i dischi del punto di ripristino devono essere ripristinati agli account di archiviazione originali.</span><span class="sxs-lookup"><span data-stu-id="202c4-134">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="202c4-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="202c4-135">-Confirm</span></span>
<span data-ttu-id="202c4-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="202c4-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="202c4-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="202c4-137">-WhatIf</span></span>
<span data-ttu-id="202c4-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="202c4-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="202c4-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="202c4-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="202c4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="202c4-140">CommonParameters</span></span>
<span data-ttu-id="202c4-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="202c4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="202c4-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="202c4-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="202c4-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="202c4-143">INPUTS</span></span>

### <span data-ttu-id="202c4-144">RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="202c4-144">RecoveryPointBase</span></span>
<span data-ttu-id="202c4-145">Il parametro ' RecoveryPoint ' accetta il valore di tipo ' RecoveryPointBase ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="202c4-145">Parameter 'RecoveryPoint' accepts value of type 'RecoveryPointBase' from the pipeline</span></span>

## <span data-ttu-id="202c4-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="202c4-146">OUTPUTS</span></span>

### <span data-ttu-id="202c4-147">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="202c4-147">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="202c4-148">Note</span><span class="sxs-lookup"><span data-stu-id="202c4-148">NOTES</span></span>

## <span data-ttu-id="202c4-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="202c4-149">RELATED LINKS</span></span>

[<span data-ttu-id="202c4-150">Backup-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="202c4-150">Backup-AzureRmRecoveryServicesBackupItem</span></span>](./Backup-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="202c4-151">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="202c4-151">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="202c4-152">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="202c4-152">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)


