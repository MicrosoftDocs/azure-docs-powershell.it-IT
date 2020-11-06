---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/set-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Set-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Set-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 5a60320736e65fae83547bbf9b2825979f73601e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509715"
---
# <span data-ttu-id="ae9fb-101">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ae9fb-101">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="ae9fb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ae9fb-102">SYNOPSIS</span></span>
<span data-ttu-id="ae9fb-103">Modifica i criteri di protezione del backup.</span><span class="sxs-lookup"><span data-stu-id="ae9fb-103">Modifies a Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae9fb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ae9fb-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase>
 [[-RetentionPolicy] <RetentionPolicyBase>] [[-SchedulePolicy] <SchedulePolicyBase>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae9fb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ae9fb-105">DESCRIPTION</span></span>
<span data-ttu-id="ae9fb-106">Il cmdlet **set-AzureRmBackupProtectionPolicy** modifica un criterio di protezione di Azure backup esistente.</span><span class="sxs-lookup"><span data-stu-id="ae9fb-106">The **Set-AzureRmBackupProtectionPolicy** cmdlet modifies an existing Azure Backup protection policy.</span></span>
<span data-ttu-id="ae9fb-107">È possibile modificare i componenti dei criteri di conservazione e pianificazione del backup.</span><span class="sxs-lookup"><span data-stu-id="ae9fb-107">You can modify the Backup schedule and retention policy components.</span></span>

<span data-ttu-id="ae9fb-108">Le modifiche apportate riguardano il backup e la conservazione degli elementi associati al criterio.</span><span class="sxs-lookup"><span data-stu-id="ae9fb-108">Any changes you make affect the backup and retention of the items associated with the policy.</span></span>

<span data-ttu-id="ae9fb-109">Impostare il contesto del Vault usando il cmdlet Set-AzureRmRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="ae9fb-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="ae9fb-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ae9fb-110">EXAMPLES</span></span>

### <span data-ttu-id="ae9fb-111">Esempio 1: modificare i criteri di protezione del backup</span><span class="sxs-lookup"><span data-stu-id="ae9fb-111">Example 1: Modify a Backup protection policy</span></span>
```
PS C:\>$SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> $RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $Pol = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Set-AzureRmRecoveryServicesBackupProtectionPolicy -Policy $Pol -SchedulePolicy $SchPol -RetentionPolicy $RetPol
```

<span data-ttu-id="ae9fb-112">Il primo comando ottiene un oggetto SchedulePolicy di base e lo archivia nella variabile $SchPol.</span><span class="sxs-lookup"><span data-stu-id="ae9fb-112">The first command gets a base SchedulePolicy object, and then stores it in the $SchPol variable.</span></span>

<span data-ttu-id="ae9fb-113">Il secondo comando rimuove tutti i tempi di esecuzione pianificati dai criteri di pianificazione in $SchPol.</span><span class="sxs-lookup"><span data-stu-id="ae9fb-113">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>

<span data-ttu-id="ae9fb-114">Il terzo comando usa il cmdlet Get-Date per ottenere la data e l'ora correnti e lo archivia nella variabile $DT.</span><span class="sxs-lookup"><span data-stu-id="ae9fb-114">The third command uses the Get-Date cmdlet to get the current date and time, and then stores it in the $DT variable.</span></span>

<span data-ttu-id="ae9fb-115">Il quarto comando aggiunge la data e l'ora in $DT al periodo di esecuzione della pianificazione per i criteri di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="ae9fb-115">The fourth command adds the date and time in $DT to the schedule run time for the schedule policy.</span></span>

<span data-ttu-id="ae9fb-116">Il quinto comando ottiene un oggetto Criteri di conservazione di base e lo archivia nella variabile $RetPol.</span><span class="sxs-lookup"><span data-stu-id="ae9fb-116">The fifth command gets a base retention policy object, and then stores it in the $RetPol variable.</span></span>

<span data-ttu-id="ae9fb-117">Il sesto comando imposta la durata di conservazione su 365 giorni.</span><span class="sxs-lookup"><span data-stu-id="ae9fb-117">The sixth command sets the retention duration to 365 days.</span></span>

<span data-ttu-id="ae9fb-118">Il settimo comando consente di ottenere i criteri di protezione del backup denominati NewPolicy e di archiviarli nella variabile $Pol.</span><span class="sxs-lookup"><span data-stu-id="ae9fb-118">The seventh command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>

<span data-ttu-id="ae9fb-119">Il comando finale modifica i criteri di protezione del backup in $Pol usando i criteri di pianificazione in $SchPol e i criteri di conservazione in $RetPol.</span><span class="sxs-lookup"><span data-stu-id="ae9fb-119">The final command modifies the Backup protection policy in $Pol using schedule policy in $SchPol and the retention policy in $RetPol.</span></span>

## <span data-ttu-id="ae9fb-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ae9fb-120">PARAMETERS</span></span>

### <span data-ttu-id="ae9fb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae9fb-121">-DefaultProfile</span></span>
<span data-ttu-id="ae9fb-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ae9fb-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae9fb-123">-Policy</span><span class="sxs-lookup"><span data-stu-id="ae9fb-123">-Policy</span></span>
<span data-ttu-id="ae9fb-124">Specifica i criteri di protezione del backup modificati da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae9fb-124">Specifies the Backup protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="ae9fb-125">Per ottenere un oggetto **BackupProtectionPolicy** , usa il cmdlet Get-AzureRmRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="ae9fb-125">To obtain a **BackupProtectionPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: PolicyBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae9fb-126">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ae9fb-126">-RetentionPolicy</span></span>
<span data-ttu-id="ae9fb-127">Specifica i criteri di conservazione di base.</span><span class="sxs-lookup"><span data-stu-id="ae9fb-127">Specifies the base retention policy.</span></span>
<span data-ttu-id="ae9fb-128">Per ottenere un oggetto **RetentionPolicy** , usa il cmdlet Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.</span><span class="sxs-lookup"><span data-stu-id="ae9fb-128">To obtain a **RetentionPolicy** object, use the Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: RetentionPolicyBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae9fb-129">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="ae9fb-129">-SchedulePolicy</span></span>
<span data-ttu-id="ae9fb-130">Specifica l'oggetto criterio pianificazione di base.</span><span class="sxs-lookup"><span data-stu-id="ae9fb-130">Specifies the base schedule policy object.</span></span>
<span data-ttu-id="ae9fb-131">Per ottenere un oggetto **SchedulePolicy** , usa l'oggetto Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.</span><span class="sxs-lookup"><span data-stu-id="ae9fb-131">To obtain a **SchedulePolicy** object, use the Get-AzureRmRecoveryServicesBackupSchedulePolicyObject object.</span></span>

```yaml
Type: SchedulePolicyBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae9fb-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ae9fb-132">-Confirm</span></span>
<span data-ttu-id="ae9fb-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae9fb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae9fb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae9fb-134">-WhatIf</span></span>
<span data-ttu-id="ae9fb-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ae9fb-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ae9fb-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ae9fb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae9fb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae9fb-137">CommonParameters</span></span>
<span data-ttu-id="ae9fb-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae9fb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae9fb-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae9fb-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae9fb-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ae9fb-140">INPUTS</span></span>

### <span data-ttu-id="ae9fb-141">PolicyBase</span><span class="sxs-lookup"><span data-stu-id="ae9fb-141">PolicyBase</span></span>
<span data-ttu-id="ae9fb-142">Il parametro ' Policy ' accetta il valore di tipo ' PolicyBase ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="ae9fb-142">Parameter 'Policy' accepts value of type 'PolicyBase' from the pipeline</span></span>

## <span data-ttu-id="ae9fb-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ae9fb-143">OUTPUTS</span></span>

### <span data-ttu-id="ae9fb-144">System. Collections. Generic. list ' 1 [Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. JobBase]</span><span class="sxs-lookup"><span data-stu-id="ae9fb-144">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase]</span></span>

## <span data-ttu-id="ae9fb-145">Note</span><span class="sxs-lookup"><span data-stu-id="ae9fb-145">NOTES</span></span>

## <span data-ttu-id="ae9fb-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ae9fb-146">RELATED LINKS</span></span>

[<span data-ttu-id="ae9fb-147">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ae9fb-147">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="ae9fb-148">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="ae9fb-148">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="ae9fb-149">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ae9fb-149">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="ae9fb-150">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ae9fb-150">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)


