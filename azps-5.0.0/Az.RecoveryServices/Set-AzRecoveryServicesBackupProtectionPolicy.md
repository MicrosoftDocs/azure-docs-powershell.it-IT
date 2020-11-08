---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: f9cd7064c1949639526f2e7b84f01fb6355b584f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193660"
---
# <span data-ttu-id="8ac32-101">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8ac32-101">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="8ac32-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8ac32-102">SYNOPSIS</span></span>
<span data-ttu-id="8ac32-103">Modifica i criteri di protezione del backup.</span><span class="sxs-lookup"><span data-stu-id="8ac32-103">Modifies a Backup protection policy.</span></span>

## <span data-ttu-id="8ac32-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8ac32-104">SYNTAX</span></span>

### <span data-ttu-id="8ac32-105">ModifyPolicyParamSet</span><span class="sxs-lookup"><span data-stu-id="8ac32-105">ModifyPolicyParamSet</span></span>
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ac32-106">FixPolicyParamSet</span><span class="sxs-lookup"><span data-stu-id="8ac32-106">FixPolicyParamSet</span></span>
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-FixForInconsistentItems]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ac32-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8ac32-107">DESCRIPTION</span></span>
<span data-ttu-id="8ac32-108">Il cmdlet **set-AzRecoveryServicesBackupProtectionPolicy** modifica un criterio di protezione di Azure backup esistente.</span><span class="sxs-lookup"><span data-stu-id="8ac32-108">The **Set-AzRecoveryServicesBackupProtectionPolicy** cmdlet modifies an existing Azure Backup protection policy.</span></span>
<span data-ttu-id="8ac32-109">È possibile modificare i componenti dei criteri di conservazione e pianificazione del backup.</span><span class="sxs-lookup"><span data-stu-id="8ac32-109">You can modify the Backup schedule and retention policy components.</span></span>
<span data-ttu-id="8ac32-110">Le modifiche apportate riguardano il backup e la conservazione degli elementi associati al criterio.</span><span class="sxs-lookup"><span data-stu-id="8ac32-110">Any changes you make affect the backup and retention of the items associated with the policy.</span></span>
<span data-ttu-id="8ac32-111">Impostare il contesto del Vault usando il cmdlet Set-AzRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="8ac32-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="8ac32-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8ac32-112">EXAMPLES</span></span>

### <span data-ttu-id="8ac32-113">Esempio 1: modificare i criteri di protezione del backup</span><span class="sxs-lookup"><span data-stu-id="8ac32-113">Example 1: Modify a Backup protection policy</span></span>
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> $Pol.AzureBackupRGName = "RG_prefix"
PS C:\> $Pol.AzureBackupRGNameSuffix = "RG_suffix"
PS C:\> Set-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol -SchedulePolicy $SchPol -RetentionPolicy $RetPol
```

<span data-ttu-id="8ac32-114">Il primo comando ottiene un oggetto SchedulePolicy di base e lo archivia nella variabile $SchPol.</span><span class="sxs-lookup"><span data-stu-id="8ac32-114">The first command gets a base SchedulePolicy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="8ac32-115">Il secondo comando rimuove tutti i tempi di esecuzione pianificati dai criteri di pianificazione in $SchPol.</span><span class="sxs-lookup"><span data-stu-id="8ac32-115">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>
<span data-ttu-id="8ac32-116">Il terzo comando usa il cmdlet Get-Date per ottenere la data e l'ora correnti e lo archivia nella variabile $DT.</span><span class="sxs-lookup"><span data-stu-id="8ac32-116">The third command uses the Get-Date cmdlet to get the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="8ac32-117">Il quarto comando aggiunge la data e l'ora in $DT al periodo di esecuzione della pianificazione per i criteri di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="8ac32-117">The fourth command adds the date and time in $DT to the schedule run time for the schedule policy.</span></span>
<span data-ttu-id="8ac32-118">Il quinto comando ottiene un oggetto Criteri di conservazione di base e lo archivia nella variabile $RetPol.</span><span class="sxs-lookup"><span data-stu-id="8ac32-118">The fifth command gets a base retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="8ac32-119">Il sesto comando imposta la durata di conservazione su 365 giorni.</span><span class="sxs-lookup"><span data-stu-id="8ac32-119">The sixth command sets the retention duration to 365 days.</span></span>
<span data-ttu-id="8ac32-120">Il settimo comando consente di ottenere i criteri di protezione del backup denominati NewPolicy e di archiviarli nella variabile $Pol.</span><span class="sxs-lookup"><span data-stu-id="8ac32-120">The seventh command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="8ac32-121">L'ottavo e il nono set imposta i parametri del gruppo di risorse associati ai criteri che memorizzano i punti di ripristino.</span><span class="sxs-lookup"><span data-stu-id="8ac32-121">The eighth and ninth sets the resource group parameters associated with policy which stores the restore points.</span></span>
<span data-ttu-id="8ac32-122">Il comando finale modifica i criteri di protezione del backup in $Pol usando i criteri di pianificazione in $SchPol e i criteri di conservazione in $RetPol.</span><span class="sxs-lookup"><span data-stu-id="8ac32-122">The final command modifies the Backup protection policy in $Pol using schedule policy in $SchPol and the retention policy in $RetPol.</span></span>

## <span data-ttu-id="8ac32-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8ac32-123">PARAMETERS</span></span>

### <span data-ttu-id="8ac32-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ac32-124">-DefaultProfile</span></span>
<span data-ttu-id="8ac32-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8ac32-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ac32-126">-FixForInconsistentItems</span><span class="sxs-lookup"><span data-stu-id="8ac32-126">-FixForInconsistentItems</span></span>
<span data-ttu-id="8ac32-127">Parametro switch che indica se riprovare o meno l'aggiornamento dei criteri per gli elementi non riusciti.</span><span class="sxs-lookup"><span data-stu-id="8ac32-127">Switch Parameter indicating whether or not to retry Policy Update for failed items.</span></span>

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

### <span data-ttu-id="8ac32-128">-Policy</span><span class="sxs-lookup"><span data-stu-id="8ac32-128">-Policy</span></span>
<span data-ttu-id="8ac32-129">Specifica i criteri di protezione del backup modificati da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ac32-129">Specifies the Backup protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="8ac32-130">Per ottenere un oggetto **BackupProtectionPolicy** , usa il cmdlet Get-AzRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="8ac32-130">To obtain a **BackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="8ac32-131">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8ac32-131">-RetentionPolicy</span></span>
<span data-ttu-id="8ac32-132">Specifica i criteri di conservazione di base.</span><span class="sxs-lookup"><span data-stu-id="8ac32-132">Specifies the base retention policy.</span></span>
<span data-ttu-id="8ac32-133">Per ottenere un oggetto **RetentionPolicy** , usa il cmdlet Get-AzRecoveryServicesBackupRetentionPolicyObject.</span><span class="sxs-lookup"><span data-stu-id="8ac32-133">To obtain a **RetentionPolicy** object, use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet.</span></span>

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

### <span data-ttu-id="8ac32-134">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="8ac32-134">-SchedulePolicy</span></span>
<span data-ttu-id="8ac32-135">Specifica l'oggetto criterio pianificazione di base.</span><span class="sxs-lookup"><span data-stu-id="8ac32-135">Specifies the base schedule policy object.</span></span>
<span data-ttu-id="8ac32-136">Per ottenere un oggetto **SchedulePolicy** , usa l'oggetto Get-AzRecoveryServicesBackupSchedulePolicyObject.</span><span class="sxs-lookup"><span data-stu-id="8ac32-136">To obtain a **SchedulePolicy** object, use the Get-AzRecoveryServicesBackupSchedulePolicyObject object.</span></span>

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

### <span data-ttu-id="8ac32-137">-VaultId</span><span class="sxs-lookup"><span data-stu-id="8ac32-137">-VaultId</span></span>
<span data-ttu-id="8ac32-138">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="8ac32-138">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="8ac32-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8ac32-139">-Confirm</span></span>
<span data-ttu-id="8ac32-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ac32-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ac32-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ac32-141">-WhatIf</span></span>
<span data-ttu-id="8ac32-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8ac32-142">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="8ac32-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ac32-143">CommonParameters</span></span>
<span data-ttu-id="8ac32-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ac32-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ac32-145">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ac32-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ac32-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8ac32-146">INPUTS</span></span>

### <span data-ttu-id="8ac32-147">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="8ac32-147">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="8ac32-148">System. String</span><span class="sxs-lookup"><span data-stu-id="8ac32-148">System.String</span></span>

## <span data-ttu-id="8ac32-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8ac32-149">OUTPUTS</span></span>

### <span data-ttu-id="8ac32-150">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="8ac32-150">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="8ac32-151">Note</span><span class="sxs-lookup"><span data-stu-id="8ac32-151">NOTES</span></span>

## <span data-ttu-id="8ac32-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8ac32-152">RELATED LINKS</span></span>

[<span data-ttu-id="8ac32-153">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8ac32-153">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="8ac32-154">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="8ac32-154">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="8ac32-155">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8ac32-155">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="8ac32-156">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8ac32-156">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)


