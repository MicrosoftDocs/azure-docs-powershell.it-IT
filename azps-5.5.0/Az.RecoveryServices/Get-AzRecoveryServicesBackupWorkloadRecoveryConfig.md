---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupworkloadrecoveryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
ms.openlocfilehash: 4209755de3475b21405fafd7f1e769bbbe3f7718
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192943"
---
# <span data-ttu-id="5ace3-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="5ace3-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span></span>

## <span data-ttu-id="5ace3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ace3-102">SYNOPSIS</span></span>
<span data-ttu-id="5ace3-103">Questo comando crea la configurazione di ripristino di un elemento di cui è stato eseguito il backup, ad esempio SQL DB.</span><span class="sxs-lookup"><span data-stu-id="5ace3-103">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="5ace3-104">L'oggetto configurazione archivia tutti i dettagli, ad esempio la modalità di ripristino, le destinazioni di destinazione per il ripristino e parametri specifici dell'applicazione, ad esempio i percorsi fisici di destinazione per SQL.</span><span class="sxs-lookup"><span data-stu-id="5ace3-104">The configuration object stores all details such as the recovery mode, target destinations for the restore and application specific parameters like target physical paths for SQL.</span></span>

## <span data-ttu-id="5ace3-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5ace3-105">SYNTAX</span></span>

### <span data-ttu-id="5ace3-106">RpParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5ace3-106">RpParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-RecoveryPoint] <RecoveryPointBase>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ace3-107">LogChainParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ace3-107">LogChainParameterSet</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-PointInTime] <DateTime>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ace3-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5ace3-108">DESCRIPTION</span></span>
<span data-ttu-id="5ace3-109">Il comando restituisce una configurazione di recupero per gli elementi AzureWorkload che viene passata al cmdlet restore.</span><span class="sxs-lookup"><span data-stu-id="5ace3-109">The command returns a recovery config for AzureWorkload items which is passed to the restore cmdlet.</span></span>

## <span data-ttu-id="5ace3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5ace3-110">EXAMPLES</span></span>

### <span data-ttu-id="5ace3-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5ace3-111">Example 1</span></span>
```powershell
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -OriginalWorkloadRestore
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -AlternateWorkloadRestore -TargetItem $SQLProtItem
```

<span data-ttu-id="5ace3-112">Il primo cmdlet viene usato per ottenere l'oggetto punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="5ace3-112">The first cmdlet is used to get the Recovery point object.</span></span>
<span data-ttu-id="5ace3-113">Il secondo cmdlet crea un piano di ripristino per un ripristino originale della posizione.</span><span class="sxs-lookup"><span data-stu-id="5ace3-113">The second cmdlet creates a recovery plan for a original location restore.</span></span>
<span data-ttu-id="5ace3-114">Il terzo cmdlet crea un piano di ripristino per un ripristino alternativo della posizione.</span><span class="sxs-lookup"><span data-stu-id="5ace3-114">THe third cmdlet creates a recovery plan for a alternate location restore.</span></span>

### <span data-ttu-id="5ace3-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="5ace3-115">Example 2</span></span>

<span data-ttu-id="5ace3-116">Questo comando crea la configurazione di ripristino di un elemento di cui è stato eseguito il backup, ad esempio SQL DB.</span><span class="sxs-lookup"><span data-stu-id="5ace3-116">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="5ace3-117">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="5ace3-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig -AlternateWorkloadRestore -RecoveryPoint $rp[0] -TargetItem <ProtectableItemBase> -VaultId $vault.ID
```

## <span data-ttu-id="5ace3-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ace3-118">PARAMETERS</span></span>

### <span data-ttu-id="5ace3-119">-AlternateWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="5ace3-119">-AlternateWorkloadRestore</span></span>
<span data-ttu-id="5ace3-120">Specifica che il database di cui è stato eseguito il backup deve essere ripristinato in un altro server selezionato.</span><span class="sxs-lookup"><span data-stu-id="5ace3-120">Specifies that the backed up DB should be restored onto another selected server.</span></span>

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

### <span data-ttu-id="5ace3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ace3-121">-DefaultProfile</span></span>
<span data-ttu-id="5ace3-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5ace3-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ace3-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="5ace3-123">-FilePath</span></span>
<span data-ttu-id="5ace3-124">Specifica il percorso file usato per l'operazione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="5ace3-124">Specifies the filepath which is used for restore operation.</span></span>

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

### <span data-ttu-id="5ace3-125">-FromFull</span><span class="sxs-lookup"><span data-stu-id="5ace3-125">-FromFull</span></span>
<span data-ttu-id="5ace3-126">Specifica il punto di ripristino completo a cui verranno applicati i backup del log.</span><span class="sxs-lookup"><span data-stu-id="5ace3-126">Specifies the Full RecoveryPoint to which Log backups will be applied.</span></span>

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

### <span data-ttu-id="5ace3-127">-Item</span><span class="sxs-lookup"><span data-stu-id="5ace3-127">-Item</span></span>
<span data-ttu-id="5ace3-128">Specifica l'elemento di backup su cui viene eseguita l'operazione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="5ace3-128">Specifies the backup item on which the restore operation is being performed.</span></span>

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

### <span data-ttu-id="5ace3-129">-OriginalWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="5ace3-129">-OriginalWorkloadRestore</span></span>
<span data-ttu-id="5ace3-130">Specifica che il database di cui è stato eseguito il backup deve essere sovrascritto con le informazioni sul database presenti nel punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="5ace3-130">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="5ace3-131">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="5ace3-131">-PointInTime</span></span>
<span data-ttu-id="5ace3-132">Ora di fine dell'intervallo di tempo per cui è necessario recuperare il punto di ripristino</span><span class="sxs-lookup"><span data-stu-id="5ace3-132">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="5ace3-133">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="5ace3-133">-RecoveryPoint</span></span>
<span data-ttu-id="5ace3-134">Oggetto punto di ripristino da ripristinare</span><span class="sxs-lookup"><span data-stu-id="5ace3-134">Recovery point object to be restored</span></span>

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

### <span data-ttu-id="5ace3-135">-RestoreAsFiles</span><span class="sxs-lookup"><span data-stu-id="5ace3-135">-RestoreAsFiles</span></span>
<span data-ttu-id="5ace3-136">Specifica di ripristinare il database come file in un computer.</span><span class="sxs-lookup"><span data-stu-id="5ace3-136">Specifies to restore Database as files in a machine.</span></span>

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

### <span data-ttu-id="5ace3-137">-TargetContainer</span><span class="sxs-lookup"><span data-stu-id="5ace3-137">-TargetContainer</span></span>
<span data-ttu-id="5ace3-138">Specifica il computer di destinazione in cui è necessario ripristinare i file DB.</span><span class="sxs-lookup"><span data-stu-id="5ace3-138">Specifies the target machine on which DB Files need to be restored.</span></span>

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

### <span data-ttu-id="5ace3-139">-TargetItem</span><span class="sxs-lookup"><span data-stu-id="5ace3-139">-TargetItem</span></span>
<span data-ttu-id="5ace3-140">Specifica la destinazione in cui deve essere ripristinato il database di database.</span><span class="sxs-lookup"><span data-stu-id="5ace3-140">Specifies the target on which the DB needs to be restored.</span></span> <span data-ttu-id="5ace3-141">Per SQL, il ripristino deve essere di tipo PROTETTO solo SQLInstance.</span><span class="sxs-lookup"><span data-stu-id="5ace3-141">For SQL restores, it needs to be of protectable item type SQLInstance only.</span></span>

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

### <span data-ttu-id="5ace3-142">-VaultId</span><span class="sxs-lookup"><span data-stu-id="5ace3-142">-VaultId</span></span>
<span data-ttu-id="5ace3-143">ARM ID del Vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="5ace3-143">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="5ace3-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ace3-144">CommonParameters</span></span>
<span data-ttu-id="5ace3-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ace3-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ace3-146">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5ace3-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ace3-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="5ace3-147">INPUTS</span></span>

### <span data-ttu-id="5ace3-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="5ace3-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="5ace3-149">System.String</span><span class="sxs-lookup"><span data-stu-id="5ace3-149">System.String</span></span>

## <span data-ttu-id="5ace3-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5ace3-150">OUTPUTS</span></span>

### <span data-ttu-id="5ace3-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span><span class="sxs-lookup"><span data-stu-id="5ace3-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span></span>

## <span data-ttu-id="5ace3-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="5ace3-152">NOTES</span></span>

## <span data-ttu-id="5ace3-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5ace3-153">RELATED LINKS</span></span>
