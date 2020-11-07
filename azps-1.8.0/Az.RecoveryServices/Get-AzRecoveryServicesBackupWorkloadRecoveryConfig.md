---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupworkloadrecoveryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
ms.openlocfilehash: 6b0f2e2c5b2e9579a92b2cee7387a19fda498fda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677641"
---
# <span data-ttu-id="efe9b-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="efe9b-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span></span>

## <span data-ttu-id="efe9b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="efe9b-102">SYNOPSIS</span></span>
<span data-ttu-id="efe9b-103">Questo comando crea la configurazione di ripristino di un elemento di cui è stato eseguito il backup, ad esempio SQL DB.</span><span class="sxs-lookup"><span data-stu-id="efe9b-103">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="efe9b-104">L'oggetto Configuration archivia tutti i dettagli, ad esempio la modalità di ripristino, le destinazioni di destinazione per il ripristino e i parametri specifici dell'applicazione, come percorsi fisici di destinazione per SQL.</span><span class="sxs-lookup"><span data-stu-id="efe9b-104">The configuration object stores all details such as the recovery mode, target destinations for the restore and application specific parameters like target physical paths for SQL.</span></span>

## <span data-ttu-id="efe9b-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="efe9b-105">SYNTAX</span></span>

### <span data-ttu-id="efe9b-106">RpParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="efe9b-106">RpParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-RecoveryPoint] <RecoveryPointBase>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efe9b-107">LogChainParameterSet</span><span class="sxs-lookup"><span data-stu-id="efe9b-107">LogChainParameterSet</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-PointInTime] <DateTime>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efe9b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="efe9b-108">DESCRIPTION</span></span>
<span data-ttu-id="efe9b-109">Il comando restituisce una configurazione di ripristino per gli elementi AzureWorkload passati al cmdlet Restore.</span><span class="sxs-lookup"><span data-stu-id="efe9b-109">The command returns a recovery config for AzureWorkload items which is passed to the restore cmdlet.</span></span>

## <span data-ttu-id="efe9b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="efe9b-110">EXAMPLES</span></span>

### <span data-ttu-id="efe9b-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="efe9b-111">Example 1</span></span>
```
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -OriginalWorkloadRestore
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -AlternateWorkloadRestore -TargetItem $SQLProtItem
```

<span data-ttu-id="efe9b-112">Il primo cmdlet viene usato per ottenere l'oggetto punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="efe9b-112">The first cmdlet is used to get the Recovery point object.</span></span>
<span data-ttu-id="efe9b-113">Il secondo cmdlet crea un piano di ripristino per un ripristino della posizione originale.</span><span class="sxs-lookup"><span data-stu-id="efe9b-113">The second cmdlet creates a recovery plan for a original location restore.</span></span>
<span data-ttu-id="efe9b-114">Il terzo cmdlet crreats un piano di ripristino per un ripristino di posizione alternativo.</span><span class="sxs-lookup"><span data-stu-id="efe9b-114">THe third cmdlet crreats a recovery plan for a alternate location restore.</span></span>

## <span data-ttu-id="efe9b-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="efe9b-115">PARAMETERS</span></span>

### <span data-ttu-id="efe9b-116">-AlternateWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="efe9b-116">-AlternateWorkloadRestore</span></span>
<span data-ttu-id="efe9b-117">Specifica che il DB di cui è stato eseguito il backup deve essere sovrascritto con le informazioni DB presenti nel punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="efe9b-117">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="efe9b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efe9b-118">-DefaultProfile</span></span>
<span data-ttu-id="efe9b-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="efe9b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efe9b-120">-Elemento</span><span class="sxs-lookup"><span data-stu-id="efe9b-120">-Item</span></span>
<span data-ttu-id="efe9b-121">Specifica l'elemento di backup in cui viene eseguita l'operazione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="efe9b-121">Specifies the backup item on which the restore operation is being performed.</span></span>

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

### <span data-ttu-id="efe9b-122">-OriginalWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="efe9b-122">-OriginalWorkloadRestore</span></span>
<span data-ttu-id="efe9b-123">Specifica che il DB di cui è stato eseguito il backup deve essere sovrascritto con le informazioni DB presenti nel punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="efe9b-123">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="efe9b-124">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="efe9b-124">-PointInTime</span></span>
<span data-ttu-id="efe9b-125">Ora di fine dell'intervallo di tempo per il quale il punto di ripristino deve essere recuperato</span><span class="sxs-lookup"><span data-stu-id="efe9b-125">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="efe9b-126">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="efe9b-126">-RecoveryPoint</span></span>
<span data-ttu-id="efe9b-127">Oggetto punto di ripristino da ripristinare</span><span class="sxs-lookup"><span data-stu-id="efe9b-127">Recovery point object to be restored</span></span>

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

### <span data-ttu-id="efe9b-128">-TargetItem</span><span class="sxs-lookup"><span data-stu-id="efe9b-128">-TargetItem</span></span>
<span data-ttu-id="efe9b-129">Specifica la destinazione in cui deve essere ripristinato il DB.</span><span class="sxs-lookup"><span data-stu-id="efe9b-129">Specifies the target on which the DB needs to be restored.</span></span> <span data-ttu-id="efe9b-130">Per il ripristino di SQL, deve essere solo di tipo elemento protettivo SQLInstance.</span><span class="sxs-lookup"><span data-stu-id="efe9b-130">For SQL restores, it needs to be of protectable item type SQLInstance only.</span></span>

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

### <span data-ttu-id="efe9b-131">-VaultId</span><span class="sxs-lookup"><span data-stu-id="efe9b-131">-VaultId</span></span>
<span data-ttu-id="efe9b-132">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="efe9b-132">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="efe9b-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="efe9b-133">-Confirm</span></span>
<span data-ttu-id="efe9b-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="efe9b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efe9b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efe9b-135">-WhatIf</span></span>
<span data-ttu-id="efe9b-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="efe9b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efe9b-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="efe9b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efe9b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efe9b-138">CommonParameters</span></span>
<span data-ttu-id="efe9b-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efe9b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efe9b-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efe9b-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efe9b-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="efe9b-141">INPUTS</span></span>

### <span data-ttu-id="efe9b-142">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="efe9b-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="efe9b-143">System. String</span><span class="sxs-lookup"><span data-stu-id="efe9b-143">System.String</span></span>

## <span data-ttu-id="efe9b-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="efe9b-144">OUTPUTS</span></span>

### <span data-ttu-id="efe9b-145">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. RecoveryConfigBase</span><span class="sxs-lookup"><span data-stu-id="efe9b-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span></span>

## <span data-ttu-id="efe9b-146">Note</span><span class="sxs-lookup"><span data-stu-id="efe9b-146">NOTES</span></span>

## <span data-ttu-id="efe9b-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="efe9b-147">RELATED LINKS</span></span>