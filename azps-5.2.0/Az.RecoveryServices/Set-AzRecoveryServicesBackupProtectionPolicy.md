---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: e9f89a39b283f073c0fe826f22157570be29e74b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357402"
---
# <span data-ttu-id="a7421-101">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a7421-101">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="a7421-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a7421-102">SYNOPSIS</span></span>
<span data-ttu-id="a7421-103">Modifica i criteri di protezione del backup.</span><span class="sxs-lookup"><span data-stu-id="a7421-103">Modifies a Backup protection policy.</span></span>

## <span data-ttu-id="a7421-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a7421-104">SYNTAX</span></span>

### <span data-ttu-id="a7421-105">ModifyPolicyParamSet</span><span class="sxs-lookup"><span data-stu-id="a7421-105">ModifyPolicyParamSet</span></span>
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7421-106">FixPolicyParamSet</span><span class="sxs-lookup"><span data-stu-id="a7421-106">FixPolicyParamSet</span></span>
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-FixForInconsistentItems]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7421-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a7421-107">DESCRIPTION</span></span>
<span data-ttu-id="a7421-108">Il cmdlet **set-AzRecoveryServicesBackupProtectionPolicy** modifica un criterio di protezione di Azure backup esistente.</span><span class="sxs-lookup"><span data-stu-id="a7421-108">The **Set-AzRecoveryServicesBackupProtectionPolicy** cmdlet modifies an existing Azure Backup protection policy.</span></span>
<span data-ttu-id="a7421-109">È possibile modificare i componenti dei criteri di conservazione e pianificazione del backup.</span><span class="sxs-lookup"><span data-stu-id="a7421-109">You can modify the Backup schedule and retention policy components.</span></span>
<span data-ttu-id="a7421-110">Le modifiche apportate riguardano il backup e la conservazione degli elementi associati al criterio.</span><span class="sxs-lookup"><span data-stu-id="a7421-110">Any changes you make affect the backup and retention of the items associated with the policy.</span></span>
<span data-ttu-id="a7421-111">Impostare il contesto del Vault usando il cmdlet Set-AzRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="a7421-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="a7421-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a7421-112">EXAMPLES</span></span>

### <span data-ttu-id="a7421-113">Esempio 1: modificare i criteri di protezione del backup</span><span class="sxs-lookup"><span data-stu-id="a7421-113">Example 1: Modify a Backup protection policy</span></span>
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

<span data-ttu-id="a7421-114">Ecco la descrizione di alto livello dei passaggi da seguire per la modifica di un criterio di protezione:</span><span class="sxs-lookup"><span data-stu-id="a7421-114">Here is the high-level description of the steps to be followed for modifying a protection policy:</span></span> 
1.  <span data-ttu-id="a7421-115">Ottenere una base SchedulePolicyObject e una base RetentionPolicyObject.</span><span class="sxs-lookup"><span data-stu-id="a7421-115">Get a base SchedulePolicyObject and base RetentionPolicyObject.</span></span> <span data-ttu-id="a7421-116">Archiviarli in una variabile.</span><span class="sxs-lookup"><span data-stu-id="a7421-116">Store them in some variable.</span></span>
2.  <span data-ttu-id="a7421-117">Imposta i diversi parametri degli oggetti Criteri di pianificazione e conservazione secondo il tuo requisito.</span><span class="sxs-lookup"><span data-stu-id="a7421-117">Set the different parameters of schedule and retention policy object as per your requirement.</span></span> <span data-ttu-id="a7421-118">Ad esempio, nello script di esempio precedente, stiamo provando a impostare criteri di protezione settimanali.</span><span class="sxs-lookup"><span data-stu-id="a7421-118">For example- In the above sample script, we are trying to set a weekly protection policy.</span></span> <span data-ttu-id="a7421-119">Abbiamo quindi modificato la frequenza di programmazione in "Weekly" e abbiamo aggiornato anche il periodo di esecuzione della programmazione.</span><span class="sxs-lookup"><span data-stu-id="a7421-119">Hence, we changed the schedule frequency to "Weekly" and also updated the schedule run time.</span></span> <span data-ttu-id="a7421-120">Nell'oggetto Criteri di conservazione è stata aggiornata la durata settimanale del periodo di conservazione e impostato il contrassegno corretto "programma settimanale abilitato".</span><span class="sxs-lookup"><span data-stu-id="a7421-120">In the retention policy object, we updated the weekly retention duration and set the correct "weekly schedule enabled" flag.</span></span> <span data-ttu-id="a7421-121">Nel caso in cui si voglia impostare un criterio giornaliero, impostare il contrassegno "pianificazione giornaliera attivata" su true e assegnare i valori appropriati per gli altri parametri degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="a7421-121">In case you want to set a Daily policy, set the "daily schedule enabled" flag to true and assign appropriate values for other object parameters.</span></span>
3.  <span data-ttu-id="a7421-122">Ottenere i criteri di protezione del backup che si desidera modificare e archiviarli in una variabile.</span><span class="sxs-lookup"><span data-stu-id="a7421-122">Get the backup protection policy that you want to modify and store it in a variable.</span></span> <span data-ttu-id="a7421-123">Nell'esempio precedente sono stati recuperati i criteri di backup con il nome "TestPolicy" che si voleva modificare.</span><span class="sxs-lookup"><span data-stu-id="a7421-123">In the above example, we retrieved the backup policy with the name "TestPolicy" that we wanted to modify.</span></span>
4.  <span data-ttu-id="a7421-124">Modificare i criteri di protezione del backup recuperati nel passaggio 3 usando l'oggetto Criteri di pianificazione e il criterio di conservazione modificati.</span><span class="sxs-lookup"><span data-stu-id="a7421-124">Modify the backup protection policy retrieved in step 3 using the modified schedule policy object and retention policy object.</span></span>

## <span data-ttu-id="a7421-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a7421-125">PARAMETERS</span></span>

### <span data-ttu-id="a7421-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7421-126">-DefaultProfile</span></span>
<span data-ttu-id="a7421-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a7421-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7421-128">-FixForInconsistentItems</span><span class="sxs-lookup"><span data-stu-id="a7421-128">-FixForInconsistentItems</span></span>
<span data-ttu-id="a7421-129">Parametro switch che indica se riprovare o meno l'aggiornamento dei criteri per gli elementi non riusciti.</span><span class="sxs-lookup"><span data-stu-id="a7421-129">Switch Parameter indicating whether or not to retry Policy Update for failed items.</span></span>

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

### <span data-ttu-id="a7421-130">-Policy</span><span class="sxs-lookup"><span data-stu-id="a7421-130">-Policy</span></span>
<span data-ttu-id="a7421-131">Specifica i criteri di protezione del backup modificati da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7421-131">Specifies the Backup protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="a7421-132">Per ottenere un oggetto **BackupProtectionPolicy** , usa il cmdlet Get-AzRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="a7421-132">To obtain a **BackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="a7421-133">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a7421-133">-RetentionPolicy</span></span>
<span data-ttu-id="a7421-134">Specifica i criteri di conservazione di base.</span><span class="sxs-lookup"><span data-stu-id="a7421-134">Specifies the base retention policy.</span></span>
<span data-ttu-id="a7421-135">Per ottenere un oggetto **RetentionPolicy** , usa il cmdlet Get-AzRecoveryServicesBackupRetentionPolicyObject.</span><span class="sxs-lookup"><span data-stu-id="a7421-135">To obtain a **RetentionPolicy** object, use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet.</span></span>

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

### <span data-ttu-id="a7421-136">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="a7421-136">-SchedulePolicy</span></span>
<span data-ttu-id="a7421-137">Specifica l'oggetto criterio pianificazione di base.</span><span class="sxs-lookup"><span data-stu-id="a7421-137">Specifies the base schedule policy object.</span></span>
<span data-ttu-id="a7421-138">Per ottenere un oggetto **SchedulePolicy** , usa l'oggetto Get-AzRecoveryServicesBackupSchedulePolicyObject.</span><span class="sxs-lookup"><span data-stu-id="a7421-138">To obtain a **SchedulePolicy** object, use the Get-AzRecoveryServicesBackupSchedulePolicyObject object.</span></span>

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

### <span data-ttu-id="a7421-139">-VaultId</span><span class="sxs-lookup"><span data-stu-id="a7421-139">-VaultId</span></span>
<span data-ttu-id="a7421-140">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="a7421-140">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="a7421-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a7421-141">-Confirm</span></span>
<span data-ttu-id="a7421-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7421-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7421-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7421-143">-WhatIf</span></span>
<span data-ttu-id="a7421-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a7421-144">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="a7421-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7421-145">CommonParameters</span></span>
<span data-ttu-id="a7421-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7421-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7421-147">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7421-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7421-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a7421-148">INPUTS</span></span>

### <span data-ttu-id="a7421-149">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="a7421-149">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="a7421-150">System. String</span><span class="sxs-lookup"><span data-stu-id="a7421-150">System.String</span></span>

## <span data-ttu-id="a7421-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a7421-151">OUTPUTS</span></span>

### <span data-ttu-id="a7421-152">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="a7421-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="a7421-153">Note</span><span class="sxs-lookup"><span data-stu-id="a7421-153">NOTES</span></span>

## <span data-ttu-id="a7421-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a7421-154">RELATED LINKS</span></span>

[<span data-ttu-id="a7421-155">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a7421-155">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="a7421-156">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="a7421-156">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="a7421-157">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a7421-157">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="a7421-158">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a7421-158">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)


