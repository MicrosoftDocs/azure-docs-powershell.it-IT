---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 1f7dcd013bb91b8ba209cf3f7b031a90f7bb49cc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93856618"
---
# <span data-ttu-id="60a5a-101">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="60a5a-101">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="60a5a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="60a5a-102">SYNOPSIS</span></span>
<span data-ttu-id="60a5a-103">Modifica i criteri di protezione del backup.</span><span class="sxs-lookup"><span data-stu-id="60a5a-103">Modifies a Backup protection policy.</span></span>

## <span data-ttu-id="60a5a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="60a5a-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60a5a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60a5a-105">DESCRIPTION</span></span>
<span data-ttu-id="60a5a-106">Il cmdlet **set-AzBackupProtectionPolicy** modifica un criterio di protezione di Azure backup esistente.</span><span class="sxs-lookup"><span data-stu-id="60a5a-106">The **Set-AzBackupProtectionPolicy** cmdlet modifies an existing Azure Backup protection policy.</span></span>
<span data-ttu-id="60a5a-107">È possibile modificare i componenti dei criteri di conservazione e pianificazione del backup.</span><span class="sxs-lookup"><span data-stu-id="60a5a-107">You can modify the Backup schedule and retention policy components.</span></span>
<span data-ttu-id="60a5a-108">Le modifiche apportate riguardano il backup e la conservazione degli elementi associati al criterio.</span><span class="sxs-lookup"><span data-stu-id="60a5a-108">Any changes you make affect the backup and retention of the items associated with the policy.</span></span>
<span data-ttu-id="60a5a-109">Impostare il contesto del Vault usando il cmdlet Set-AzRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="60a5a-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="60a5a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="60a5a-110">EXAMPLES</span></span>

### <span data-ttu-id="60a5a-111">Esempio 1: modificare i criteri di protezione del backup</span><span class="sxs-lookup"><span data-stu-id="60a5a-111">Example 1: Modify a Backup protection policy</span></span>
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Set-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol -SchedulePolicy $SchPol -RetentionPolicy $RetPol
```

<span data-ttu-id="60a5a-112">Il primo comando ottiene un oggetto SchedulePolicy di base e lo archivia nella variabile $SchPol.</span><span class="sxs-lookup"><span data-stu-id="60a5a-112">The first command gets a base SchedulePolicy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="60a5a-113">Il secondo comando rimuove tutti i tempi di esecuzione pianificati dai criteri di pianificazione in $SchPol.</span><span class="sxs-lookup"><span data-stu-id="60a5a-113">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>
<span data-ttu-id="60a5a-114">Il terzo comando usa il cmdlet Get-Date per ottenere la data e l'ora correnti e lo archivia nella variabile $DT.</span><span class="sxs-lookup"><span data-stu-id="60a5a-114">The third command uses the Get-Date cmdlet to get the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="60a5a-115">Il quarto comando aggiunge la data e l'ora in $DT al periodo di esecuzione della pianificazione per i criteri di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="60a5a-115">The fourth command adds the date and time in $DT to the schedule run time for the schedule policy.</span></span>
<span data-ttu-id="60a5a-116">Il quinto comando ottiene un oggetto Criteri di conservazione di base e lo archivia nella variabile $RetPol.</span><span class="sxs-lookup"><span data-stu-id="60a5a-116">The fifth command gets a base retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="60a5a-117">Il sesto comando imposta la durata di conservazione su 365 giorni.</span><span class="sxs-lookup"><span data-stu-id="60a5a-117">The sixth command sets the retention duration to 365 days.</span></span>
<span data-ttu-id="60a5a-118">Il settimo comando consente di ottenere i criteri di protezione del backup denominati NewPolicy e di archiviarli nella variabile $Pol.</span><span class="sxs-lookup"><span data-stu-id="60a5a-118">The seventh command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="60a5a-119">Il comando finale modifica i criteri di protezione del backup in $Pol usando i criteri di pianificazione in $SchPol e i criteri di conservazione in $RetPol.</span><span class="sxs-lookup"><span data-stu-id="60a5a-119">The final command modifies the Backup protection policy in $Pol using schedule policy in $SchPol and the retention policy in $RetPol.</span></span>

## <span data-ttu-id="60a5a-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="60a5a-120">PARAMETERS</span></span>

### <span data-ttu-id="60a5a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60a5a-121">-DefaultProfile</span></span>
<span data-ttu-id="60a5a-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="60a5a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60a5a-123">-Policy</span><span class="sxs-lookup"><span data-stu-id="60a5a-123">-Policy</span></span>
<span data-ttu-id="60a5a-124">Specifica i criteri di protezione del backup modificati da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60a5a-124">Specifies the Backup protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="60a5a-125">Per ottenere un oggetto **BackupProtectionPolicy** , usa il cmdlet Get-AzRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="60a5a-125">To obtain a **BackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="60a5a-126">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="60a5a-126">-RetentionPolicy</span></span>
<span data-ttu-id="60a5a-127">Specifica i criteri di conservazione di base.</span><span class="sxs-lookup"><span data-stu-id="60a5a-127">Specifies the base retention policy.</span></span>
<span data-ttu-id="60a5a-128">Per ottenere un oggetto **RetentionPolicy** , usa il cmdlet Get-AzRecoveryServicesBackupRetentionPolicyObject.</span><span class="sxs-lookup"><span data-stu-id="60a5a-128">To obtain a **RetentionPolicy** object, use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60a5a-129">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="60a5a-129">-SchedulePolicy</span></span>
<span data-ttu-id="60a5a-130">Specifica l'oggetto criterio pianificazione di base.</span><span class="sxs-lookup"><span data-stu-id="60a5a-130">Specifies the base schedule policy object.</span></span>
<span data-ttu-id="60a5a-131">Per ottenere un oggetto **SchedulePolicy** , usa l'oggetto Get-AzRecoveryServicesBackupSchedulePolicyObject.</span><span class="sxs-lookup"><span data-stu-id="60a5a-131">To obtain a **SchedulePolicy** object, use the Get-AzRecoveryServicesBackupSchedulePolicyObject object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60a5a-132">-VaultId</span><span class="sxs-lookup"><span data-stu-id="60a5a-132">-VaultId</span></span>
<span data-ttu-id="60a5a-133">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="60a5a-133">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="60a5a-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="60a5a-134">-Confirm</span></span>
<span data-ttu-id="60a5a-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60a5a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60a5a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60a5a-136">-WhatIf</span></span>
<span data-ttu-id="60a5a-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60a5a-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="60a5a-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60a5a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60a5a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60a5a-139">CommonParameters</span></span>
<span data-ttu-id="60a5a-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60a5a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60a5a-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60a5a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60a5a-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="60a5a-142">INPUTS</span></span>

### <span data-ttu-id="60a5a-143">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="60a5a-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="60a5a-144">System. String</span><span class="sxs-lookup"><span data-stu-id="60a5a-144">System.String</span></span>

## <span data-ttu-id="60a5a-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="60a5a-145">OUTPUTS</span></span>

### <span data-ttu-id="60a5a-146">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="60a5a-146">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="60a5a-147">Note</span><span class="sxs-lookup"><span data-stu-id="60a5a-147">NOTES</span></span>

## <span data-ttu-id="60a5a-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="60a5a-148">RELATED LINKS</span></span>

[<span data-ttu-id="60a5a-149">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="60a5a-149">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="60a5a-150">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="60a5a-150">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="60a5a-151">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="60a5a-151">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="60a5a-152">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="60a5a-152">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)


