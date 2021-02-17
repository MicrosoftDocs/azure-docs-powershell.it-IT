---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: e9f89a39b283f073c0fe826f22157570be29e74b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191295"
---
# <span data-ttu-id="461a4-101">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="461a4-101">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="461a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="461a4-102">SYNOPSIS</span></span>
<span data-ttu-id="461a4-103">Modifica i criteri di protezione per il backup.</span><span class="sxs-lookup"><span data-stu-id="461a4-103">Modifies a Backup protection policy.</span></span>

## <span data-ttu-id="461a4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="461a4-104">SYNTAX</span></span>

### <span data-ttu-id="461a4-105">ModifyPolicyParamSet</span><span class="sxs-lookup"><span data-stu-id="461a4-105">ModifyPolicyParamSet</span></span>
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="461a4-106">FixPolicyParamSet</span><span class="sxs-lookup"><span data-stu-id="461a4-106">FixPolicyParamSet</span></span>
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-FixForInconsistentItems]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="461a4-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="461a4-107">DESCRIPTION</span></span>
<span data-ttu-id="461a4-108">Il cmdlet **Set-AzRecoveryServicesBackupProtectionPolicy** modifica un criterio di protezione backup di Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="461a4-108">The **Set-AzRecoveryServicesBackupProtectionPolicy** cmdlet modifies an existing Azure Backup protection policy.</span></span>
<span data-ttu-id="461a4-109">È possibile modificare i componenti della pianificazione di backup e dei criteri di conservazione.</span><span class="sxs-lookup"><span data-stu-id="461a4-109">You can modify the Backup schedule and retention policy components.</span></span>
<span data-ttu-id="461a4-110">Qualsiasi modifica apportata influisce sul backup e sulla conservazione degli elementi associati al criterio.</span><span class="sxs-lookup"><span data-stu-id="461a4-110">Any changes you make affect the backup and retention of the items associated with the policy.</span></span>
<span data-ttu-id="461a4-111">Impostare il contesto del vault usando il cmdlet Set-AzRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="461a4-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="461a4-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="461a4-112">EXAMPLES</span></span>

### <span data-ttu-id="461a4-113">Esempio 1: Modificare un criterio di protezione per il backup</span><span class="sxs-lookup"><span data-stu-id="461a4-113">Example 1: Modify a Backup protection policy</span></span>
```
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Time = Get-Date
PS C:\> $Time1 = Get-Date -Year $Time.Year -Month $Time.Month -Day $Time.Day -Hour $Time.Hour -Minute 0 -Second 0 -Millisecond 0
PS C:\> $Time1 = $Time1.ToUniversalTime()
PS C:\> $SchPol.ScheduleRunTimes.Add($Time1)
PS C:\> $SchPol.ScheduleRunFrequency.Clear
PS C:\> $SchPol.ScheduleRunDays.Add("Monday")
PS C:\> $SchPol.ScheduleRunFrequency="Weekly"
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.IsDailyScheduleEnabled=$false
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 0
PS C:\> $RetPol.IsWeeklyScheduleEnabled=$true 
PS C:\> $RetPol.WeeklySchedule.DaysOfTheWeek.Add("Monday")
PS C:\> $RetPol.WeeklySchedule.DurationCountInWeeks = 365
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "azurefiles" -Name "azurefilesvault"
PS C:\> $Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "TestPolicy" -VaultId $vault.ID
PS C:\> $Pol.SnapshotRetentionInDays=5
PS C:\> Set-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol -SchedulePolicy $SchPol -RetentionPolicy $RetPol
```

<span data-ttu-id="461a4-114">Ecco la descrizione dettagliata dei passaggi da seguire per modificare i criteri di protezione:</span><span class="sxs-lookup"><span data-stu-id="461a4-114">Here is the high-level description of the steps to be followed for modifying a protection policy:</span></span> 
1.  <span data-ttu-id="461a4-115">Ottenere un oggetto SchedulePolicyObject di base e un oggetto RetentionPolicyObject di base.</span><span class="sxs-lookup"><span data-stu-id="461a4-115">Get a base SchedulePolicyObject and base RetentionPolicyObject.</span></span> <span data-ttu-id="461a4-116">Archiviarli in una variabile.</span><span class="sxs-lookup"><span data-stu-id="461a4-116">Store them in some variable.</span></span>
2.  <span data-ttu-id="461a4-117">Impostare i diversi parametri dell'oggetto pianificazione e dei criteri di conservazione in base ai propri requisiti.</span><span class="sxs-lookup"><span data-stu-id="461a4-117">Set the different parameters of schedule and retention policy object as per your requirement.</span></span> <span data-ttu-id="461a4-118">Ad esempio, nello script di esempio precedente si sta cercando di impostare criteri di protezione settimanali.</span><span class="sxs-lookup"><span data-stu-id="461a4-118">For example- In the above sample script, we are trying to set a weekly protection policy.</span></span> <span data-ttu-id="461a4-119">Di conseguenza, è stata modificata la frequenza della pianificazione in "Settimanale" e aggiornata anche la data di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="461a4-119">Hence, we changed the schedule frequency to "Weekly" and also updated the schedule run time.</span></span> <span data-ttu-id="461a4-120">Nell'oggetto criterio di conservazione è stata aggiornata la durata di conservazione settimanale e impostato il contrassegno corretto "pianificazione settimanale abilitata".</span><span class="sxs-lookup"><span data-stu-id="461a4-120">In the retention policy object, we updated the weekly retention duration and set the correct "weekly schedule enabled" flag.</span></span> <span data-ttu-id="461a4-121">Nel caso in cui si voglia impostare un criterio Giornaliero, impostare il contrassegno "pianificazione giornaliera abilitata" su true e assegnare i valori appropriati per altri parametri dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="461a4-121">In case you want to set a Daily policy, set the "daily schedule enabled" flag to true and assign appropriate values for other object parameters.</span></span>
3.  <span data-ttu-id="461a4-122">Ottenere i criteri di protezione del backup da modificare e archiviare in una variabile.</span><span class="sxs-lookup"><span data-stu-id="461a4-122">Get the backup protection policy that you want to modify and store it in a variable.</span></span> <span data-ttu-id="461a4-123">Nell'esempio precedente è stato recuperato il criterio di backup con il nome "TestPolicy" che si vuole modificare.</span><span class="sxs-lookup"><span data-stu-id="461a4-123">In the above example, we retrieved the backup policy with the name "TestPolicy" that we wanted to modify.</span></span>
4.  <span data-ttu-id="461a4-124">Modificare i criteri di protezione del backup recuperati nel passaggio 3 usando l'oggetto criterio di pianificazione modificato e l'oggetto criterio di conservazione modificato.</span><span class="sxs-lookup"><span data-stu-id="461a4-124">Modify the backup protection policy retrieved in step 3 using the modified schedule policy object and retention policy object.</span></span>

## <span data-ttu-id="461a4-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="461a4-125">PARAMETERS</span></span>

### <span data-ttu-id="461a4-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="461a4-126">-DefaultProfile</span></span>
<span data-ttu-id="461a4-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="461a4-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="461a4-128">-FixForInconsistentItems</span><span class="sxs-lookup"><span data-stu-id="461a4-128">-FixForInconsistentItems</span></span>
<span data-ttu-id="461a4-129">Parametro switch che indica se riprovare o meno l'aggiornamento dei criteri per gli elementi non riusciti.</span><span class="sxs-lookup"><span data-stu-id="461a4-129">Switch Parameter indicating whether or not to retry Policy Update for failed items.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FixPolicyParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="461a4-130">-Policy</span><span class="sxs-lookup"><span data-stu-id="461a4-130">-Policy</span></span>
<span data-ttu-id="461a4-131">Specifica i criteri di protezione del backup che il cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="461a4-131">Specifies the Backup protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="461a4-132">Per ottenere un **oggetto BackupProtectionPolicy,** usare il cmdlet Get-AzRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="461a4-132">To obtain a **BackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="461a4-133">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="461a4-133">-RetentionPolicy</span></span>
<span data-ttu-id="461a4-134">Specifica i criteri di conservazione di base.</span><span class="sxs-lookup"><span data-stu-id="461a4-134">Specifies the base retention policy.</span></span>
<span data-ttu-id="461a4-135">Per ottenere un **oggetto RetentionPolicy,** usare il cmdlet Get-AzRecoveryServicesBackupRetentionPolicyObject conservazione.</span><span class="sxs-lookup"><span data-stu-id="461a4-135">To obtain a **RetentionPolicy** object, use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase
Parameter Sets: ModifyPolicyParamSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="461a4-136">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="461a4-136">-SchedulePolicy</span></span>
<span data-ttu-id="461a4-137">Specifica l'oggetto criterio di pianificazione di base.</span><span class="sxs-lookup"><span data-stu-id="461a4-137">Specifies the base schedule policy object.</span></span>
<span data-ttu-id="461a4-138">Per ottenere un **oggetto SchedulePolicy,** usare l'oggetto Get-AzRecoveryServicesBackupSchedulePolicyObject programmazione.</span><span class="sxs-lookup"><span data-stu-id="461a4-138">To obtain a **SchedulePolicy** object, use the Get-AzRecoveryServicesBackupSchedulePolicyObject object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase
Parameter Sets: ModifyPolicyParamSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="461a4-139">-VaultId</span><span class="sxs-lookup"><span data-stu-id="461a4-139">-VaultId</span></span>
<span data-ttu-id="461a4-140">ARM ID del Vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="461a4-140">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="461a4-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="461a4-141">-Confirm</span></span>
<span data-ttu-id="461a4-142">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="461a4-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="461a4-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="461a4-143">-WhatIf</span></span>
<span data-ttu-id="461a4-144">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="461a4-144">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="461a4-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="461a4-145">CommonParameters</span></span>
<span data-ttu-id="461a4-146">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="461a4-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="461a4-147">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="461a4-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="461a4-148">INPUT</span><span class="sxs-lookup"><span data-stu-id="461a4-148">INPUTS</span></span>

### <span data-ttu-id="461a4-149">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span><span class="sxs-lookup"><span data-stu-id="461a4-149">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="461a4-150">System.String</span><span class="sxs-lookup"><span data-stu-id="461a4-150">System.String</span></span>

## <span data-ttu-id="461a4-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="461a4-151">OUTPUTS</span></span>

### <span data-ttu-id="461a4-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="461a4-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="461a4-153">NOTE</span><span class="sxs-lookup"><span data-stu-id="461a4-153">NOTES</span></span>

## <span data-ttu-id="461a4-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="461a4-154">RELATED LINKS</span></span>

[<span data-ttu-id="461a4-155">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="461a4-155">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="461a4-156">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="461a4-156">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="461a4-157">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="461a4-157">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="461a4-158">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="461a4-158">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)


