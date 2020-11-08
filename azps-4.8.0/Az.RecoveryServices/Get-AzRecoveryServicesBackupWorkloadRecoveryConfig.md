---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupworkloadrecoveryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
ms.openlocfilehash: 4209755de3475b21405fafd7f1e769bbbe3f7718
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190683"
---
# <span data-ttu-id="48e2c-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="48e2c-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span></span>

## <span data-ttu-id="48e2c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="48e2c-102">SYNOPSIS</span></span>
<span data-ttu-id="48e2c-103">Questo comando crea la configurazione di ripristino di un elemento di cui è stato eseguito il backup, ad esempio SQL DB.</span><span class="sxs-lookup"><span data-stu-id="48e2c-103">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="48e2c-104">L'oggetto Configuration archivia tutti i dettagli, ad esempio la modalità di ripristino, le destinazioni di destinazione per il ripristino e i parametri specifici dell'applicazione, come percorsi fisici di destinazione per SQL.</span><span class="sxs-lookup"><span data-stu-id="48e2c-104">The configuration object stores all details such as the recovery mode, target destinations for the restore and application specific parameters like target physical paths for SQL.</span></span>

## <span data-ttu-id="48e2c-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="48e2c-105">SYNTAX</span></span>

### <span data-ttu-id="48e2c-106">RpParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="48e2c-106">RpParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-RecoveryPoint] <RecoveryPointBase>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48e2c-107">LogChainParameterSet</span><span class="sxs-lookup"><span data-stu-id="48e2c-107">LogChainParameterSet</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-PointInTime] <DateTime>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48e2c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="48e2c-108">DESCRIPTION</span></span>
<span data-ttu-id="48e2c-109">Il comando restituisce una configurazione di ripristino per gli elementi AzureWorkload passati al cmdlet Restore.</span><span class="sxs-lookup"><span data-stu-id="48e2c-109">The command returns a recovery config for AzureWorkload items which is passed to the restore cmdlet.</span></span>

## <span data-ttu-id="48e2c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="48e2c-110">EXAMPLES</span></span>

### <span data-ttu-id="48e2c-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="48e2c-111">Example 1</span></span>
```powershell
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -OriginalWorkloadRestore
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -AlternateWorkloadRestore -TargetItem $SQLProtItem
```

<span data-ttu-id="48e2c-112">Il primo cmdlet viene usato per ottenere l'oggetto punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="48e2c-112">The first cmdlet is used to get the Recovery point object.</span></span>
<span data-ttu-id="48e2c-113">Il secondo cmdlet crea un piano di ripristino per un ripristino della posizione originale.</span><span class="sxs-lookup"><span data-stu-id="48e2c-113">The second cmdlet creates a recovery plan for a original location restore.</span></span>
<span data-ttu-id="48e2c-114">Il terzo cmdlet crea un piano di ripristino per un ripristino di posizione alternativo.</span><span class="sxs-lookup"><span data-stu-id="48e2c-114">THe third cmdlet creates a recovery plan for a alternate location restore.</span></span>

### <span data-ttu-id="48e2c-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="48e2c-115">Example 2</span></span>

<span data-ttu-id="48e2c-116">Questo comando crea la configurazione di ripristino di un elemento di cui è stato eseguito il backup, ad esempio SQL DB.</span><span class="sxs-lookup"><span data-stu-id="48e2c-116">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="48e2c-117">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="48e2c-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig -AlternateWorkloadRestore -RecoveryPoint $rp[0] -TargetItem <ProtectableItemBase> -VaultId $vault.ID
```

## <span data-ttu-id="48e2c-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="48e2c-118">PARAMETERS</span></span>

### <span data-ttu-id="48e2c-119">-AlternateWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="48e2c-119">-AlternateWorkloadRestore</span></span>
<span data-ttu-id="48e2c-120">Specifica che il DB di cui è stato eseguito il backup deve essere ripristinato su un altro server selezionato.</span><span class="sxs-lookup"><span data-stu-id="48e2c-120">Specifies that the backed up DB should be restored onto another selected server.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48e2c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48e2c-121">-DefaultProfile</span></span>
<span data-ttu-id="48e2c-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="48e2c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48e2c-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="48e2c-123">-FilePath</span></span>
<span data-ttu-id="48e2c-124">Specifica il FilePath usato per l'operazione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="48e2c-124">Specifies the filepath which is used for restore operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48e2c-125">-FromFull</span><span class="sxs-lookup"><span data-stu-id="48e2c-125">-FromFull</span></span>
<span data-ttu-id="48e2c-126">Specifica il RecoveryPoint completo a cui verranno applicati i backup del log.</span><span class="sxs-lookup"><span data-stu-id="48e2c-126">Specifies the Full RecoveryPoint to which Log backups will be applied.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48e2c-127">-Elemento</span><span class="sxs-lookup"><span data-stu-id="48e2c-127">-Item</span></span>
<span data-ttu-id="48e2c-128">Specifica l'elemento di backup in cui viene eseguita l'operazione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="48e2c-128">Specifies the backup item on which the restore operation is being performed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48e2c-129">-OriginalWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="48e2c-129">-OriginalWorkloadRestore</span></span>
<span data-ttu-id="48e2c-130">Specifica che il DB di cui è stato eseguito il backup deve essere sovrascritto con le informazioni DB presenti nel punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="48e2c-130">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48e2c-131">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="48e2c-131">-PointInTime</span></span>
<span data-ttu-id="48e2c-132">Ora di fine dell'intervallo di tempo per il quale il punto di ripristino deve essere recuperato</span><span class="sxs-lookup"><span data-stu-id="48e2c-132">End time of Time range for which recovery point need to be fetched</span></span>

```yaml
Type: System.DateTime
Parameter Sets: LogChainParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48e2c-133">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="48e2c-133">-RecoveryPoint</span></span>
<span data-ttu-id="48e2c-134">Oggetto punto di ripristino da ripristinare</span><span class="sxs-lookup"><span data-stu-id="48e2c-134">Recovery point object to be restored</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: RpParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48e2c-135">-RestoreAsFiles</span><span class="sxs-lookup"><span data-stu-id="48e2c-135">-RestoreAsFiles</span></span>
<span data-ttu-id="48e2c-136">Specifica di ripristinare il database come file in un computer.</span><span class="sxs-lookup"><span data-stu-id="48e2c-136">Specifies to restore Database as files in a machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48e2c-137">-TargetContainer</span><span class="sxs-lookup"><span data-stu-id="48e2c-137">-TargetContainer</span></span>
<span data-ttu-id="48e2c-138">Specifica il computer di destinazione in cui devono essere ripristinati i file DB.</span><span class="sxs-lookup"><span data-stu-id="48e2c-138">Specifies the target machine on which DB Files need to be restored.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48e2c-139">-TargetItem</span><span class="sxs-lookup"><span data-stu-id="48e2c-139">-TargetItem</span></span>
<span data-ttu-id="48e2c-140">Specifica la destinazione in cui deve essere ripristinato il DB.</span><span class="sxs-lookup"><span data-stu-id="48e2c-140">Specifies the target on which the DB needs to be restored.</span></span> <span data-ttu-id="48e2c-141">Per il ripristino di SQL, deve essere solo di tipo elemento protettivo SQLInstance.</span><span class="sxs-lookup"><span data-stu-id="48e2c-141">For SQL restores, it needs to be of protectable item type SQLInstance only.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48e2c-142">-VaultId</span><span class="sxs-lookup"><span data-stu-id="48e2c-142">-VaultId</span></span>
<span data-ttu-id="48e2c-143">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="48e2c-143">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="48e2c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48e2c-144">CommonParameters</span></span>
<span data-ttu-id="48e2c-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48e2c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48e2c-146">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="48e2c-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48e2c-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="48e2c-147">INPUTS</span></span>

### <span data-ttu-id="48e2c-148">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="48e2c-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="48e2c-149">System. String</span><span class="sxs-lookup"><span data-stu-id="48e2c-149">System.String</span></span>

## <span data-ttu-id="48e2c-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="48e2c-150">OUTPUTS</span></span>

### <span data-ttu-id="48e2c-151">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. RecoveryConfigBase</span><span class="sxs-lookup"><span data-stu-id="48e2c-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span></span>

## <span data-ttu-id="48e2c-152">Note</span><span class="sxs-lookup"><span data-stu-id="48e2c-152">NOTES</span></span>

## <span data-ttu-id="48e2c-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="48e2c-153">RELATED LINKS</span></span>
