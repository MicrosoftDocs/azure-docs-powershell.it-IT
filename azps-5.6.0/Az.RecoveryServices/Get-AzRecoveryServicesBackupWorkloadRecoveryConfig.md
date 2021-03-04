---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupworkloadrecoveryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
ms.openlocfilehash: d608b4265435041a918ba71cdd68ae00892bcc20
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959485"
---
# <span data-ttu-id="44ce4-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="44ce4-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span></span>

## <span data-ttu-id="44ce4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44ce4-102">SYNOPSIS</span></span>
<span data-ttu-id="44ce4-103">Questo comando crea la configurazione di ripristino di un elemento di cui è stato eseguito il backup, ad esempio SQL DB.</span><span class="sxs-lookup"><span data-stu-id="44ce4-103">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="44ce4-104">L'oggetto configurazione archivia tutti i dettagli, ad esempio la modalità di ripristino, le destinazioni di destinazione per il ripristino e parametri specifici dell'applicazione, ad esempio i percorsi fisici di destinazione per SQL.</span><span class="sxs-lookup"><span data-stu-id="44ce4-104">The configuration object stores all details such as the recovery mode, target destinations for the restore and application specific parameters like target physical paths for SQL.</span></span>

## <span data-ttu-id="44ce4-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="44ce4-105">SYNTAX</span></span>

### <span data-ttu-id="44ce4-106">RpParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="44ce4-106">RpParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-RecoveryPoint] <RecoveryPointBase>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44ce4-107">LogChainParameterSet</span><span class="sxs-lookup"><span data-stu-id="44ce4-107">LogChainParameterSet</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-PointInTime] <DateTime>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44ce4-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="44ce4-108">DESCRIPTION</span></span>
<span data-ttu-id="44ce4-109">Il comando restituisce una configurazione di recupero per gli elementi AzureWorkload che viene passata al cmdlet restore.</span><span class="sxs-lookup"><span data-stu-id="44ce4-109">The command returns a recovery config for AzureWorkload items which is passed to the restore cmdlet.</span></span>

## <span data-ttu-id="44ce4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="44ce4-110">EXAMPLES</span></span>

### <span data-ttu-id="44ce4-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="44ce4-111">Example 1</span></span>
```powershell
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -OriginalWorkloadRestore
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -AlternateWorkloadRestore -TargetItem $SQLProtItem
```

<span data-ttu-id="44ce4-112">Il primo cmdlet viene usato per ottenere l'oggetto punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="44ce4-112">The first cmdlet is used to get the Recovery point object.</span></span>
<span data-ttu-id="44ce4-113">Il secondo cmdlet crea un piano di ripristino per un ripristino originale della posizione.</span><span class="sxs-lookup"><span data-stu-id="44ce4-113">The second cmdlet creates a recovery plan for a original location restore.</span></span>
<span data-ttu-id="44ce4-114">Il terzo cmdlet crea un piano di ripristino per un ripristino alternativo della posizione.</span><span class="sxs-lookup"><span data-stu-id="44ce4-114">THe third cmdlet creates a recovery plan for a alternate location restore.</span></span>

### <span data-ttu-id="44ce4-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="44ce4-115">Example 2</span></span>

<span data-ttu-id="44ce4-116">Questo comando crea la configurazione di ripristino di un elemento di cui è stato eseguito il backup, ad esempio SQL DB.</span><span class="sxs-lookup"><span data-stu-id="44ce4-116">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="44ce4-117">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="44ce4-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig -AlternateWorkloadRestore -RecoveryPoint $rp[0] -TargetItem <ProtectableItemBase> -VaultId $vault.ID
```

## <span data-ttu-id="44ce4-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44ce4-118">PARAMETERS</span></span>

### <span data-ttu-id="44ce4-119">-AlternateWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="44ce4-119">-AlternateWorkloadRestore</span></span>
<span data-ttu-id="44ce4-120">Specifica che il database di cui è stato eseguito il backup deve essere ripristinato in un altro server selezionato.</span><span class="sxs-lookup"><span data-stu-id="44ce4-120">Specifies that the backed up DB should be restored onto another selected server.</span></span>

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

### <span data-ttu-id="44ce4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44ce4-121">-DefaultProfile</span></span>
<span data-ttu-id="44ce4-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="44ce4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44ce4-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="44ce4-123">-FilePath</span></span>
<span data-ttu-id="44ce4-124">Specifica il percorso file usato per l'operazione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="44ce4-124">Specifies the filepath which is used for restore operation.</span></span>

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

### <span data-ttu-id="44ce4-125">-FromFull</span><span class="sxs-lookup"><span data-stu-id="44ce4-125">-FromFull</span></span>
<span data-ttu-id="44ce4-126">Specifica il punto di ripristino completo a cui verranno applicati i backup del log.</span><span class="sxs-lookup"><span data-stu-id="44ce4-126">Specifies the Full RecoveryPoint to which Log backups will be applied.</span></span>

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

### <span data-ttu-id="44ce4-127">-Item</span><span class="sxs-lookup"><span data-stu-id="44ce4-127">-Item</span></span>
<span data-ttu-id="44ce4-128">Specifica l'elemento di backup su cui viene eseguita l'operazione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="44ce4-128">Specifies the backup item on which the restore operation is being performed.</span></span>

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

### <span data-ttu-id="44ce4-129">-OriginalWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="44ce4-129">-OriginalWorkloadRestore</span></span>
<span data-ttu-id="44ce4-130">Specifica che il database di cui è stato eseguito il backup deve essere sovrascritto con le informazioni sul database presenti nel punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="44ce4-130">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="44ce4-131">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="44ce4-131">-PointInTime</span></span>
<span data-ttu-id="44ce4-132">Ora di fine dell'intervallo di tempo per cui è necessario recuperare il punto di ripristino</span><span class="sxs-lookup"><span data-stu-id="44ce4-132">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="44ce4-133">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="44ce4-133">-RecoveryPoint</span></span>
<span data-ttu-id="44ce4-134">Oggetto punto di ripristino da ripristinare</span><span class="sxs-lookup"><span data-stu-id="44ce4-134">Recovery point object to be restored</span></span>

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

### <span data-ttu-id="44ce4-135">-RestoreAsFiles</span><span class="sxs-lookup"><span data-stu-id="44ce4-135">-RestoreAsFiles</span></span>
<span data-ttu-id="44ce4-136">Specifica di ripristinare il database come file in un computer.</span><span class="sxs-lookup"><span data-stu-id="44ce4-136">Specifies to restore Database as files in a machine.</span></span>

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

### <span data-ttu-id="44ce4-137">-TargetContainer</span><span class="sxs-lookup"><span data-stu-id="44ce4-137">-TargetContainer</span></span>
<span data-ttu-id="44ce4-138">Specifica il computer di destinazione in cui è necessario ripristinare i file DB.</span><span class="sxs-lookup"><span data-stu-id="44ce4-138">Specifies the target machine on which DB Files need to be restored.</span></span>

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

### <span data-ttu-id="44ce4-139">-TargetItem</span><span class="sxs-lookup"><span data-stu-id="44ce4-139">-TargetItem</span></span>
<span data-ttu-id="44ce4-140">Specifica la destinazione in cui deve essere ripristinato il database di database.</span><span class="sxs-lookup"><span data-stu-id="44ce4-140">Specifies the target on which the DB needs to be restored.</span></span> <span data-ttu-id="44ce4-141">Per SQL, il ripristino deve essere di tipo PROTETTO solo SQLInstance.</span><span class="sxs-lookup"><span data-stu-id="44ce4-141">For SQL restores, it needs to be of protectable item type SQLInstance only.</span></span>

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

### <span data-ttu-id="44ce4-142">-VaultId</span><span class="sxs-lookup"><span data-stu-id="44ce4-142">-VaultId</span></span>
<span data-ttu-id="44ce4-143">ARM ID del Vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="44ce4-143">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="44ce4-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44ce4-144">CommonParameters</span></span>
<span data-ttu-id="44ce4-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44ce4-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44ce4-146">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="44ce4-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44ce4-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="44ce4-147">INPUTS</span></span>

### <span data-ttu-id="44ce4-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="44ce4-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="44ce4-149">System.String</span><span class="sxs-lookup"><span data-stu-id="44ce4-149">System.String</span></span>

## <span data-ttu-id="44ce4-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="44ce4-150">OUTPUTS</span></span>

### <span data-ttu-id="44ce4-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span><span class="sxs-lookup"><span data-stu-id="44ce4-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span></span>

## <span data-ttu-id="44ce4-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="44ce4-152">NOTES</span></span>

## <span data-ttu-id="44ce4-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="44ce4-153">RELATED LINKS</span></span>
