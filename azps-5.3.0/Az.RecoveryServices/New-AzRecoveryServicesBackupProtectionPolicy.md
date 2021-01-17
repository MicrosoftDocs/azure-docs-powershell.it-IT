---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 0a60e3bd7f07f69687766b95eb3d56be3ef1d56f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475746"
---
# <span data-ttu-id="6d277-101">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6d277-101">New-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="6d277-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6d277-102">SYNOPSIS</span></span>
<span data-ttu-id="6d277-103">Crea un criterio di protezione del backup.</span><span class="sxs-lookup"><span data-stu-id="6d277-103">Creates a Backup protection policy.</span></span>

## <span data-ttu-id="6d277-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6d277-104">SYNTAX</span></span>

```
New-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d277-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6d277-105">DESCRIPTION</span></span>
<span data-ttu-id="6d277-106">Il cmdlet **New-AzRecoveryServicesBackupProtectionPolicy** crea un criterio di protezione del backup in un Vault.</span><span class="sxs-lookup"><span data-stu-id="6d277-106">The **New-AzRecoveryServicesBackupProtectionPolicy** cmdlet creates a Backup protection policy in a vault.</span></span>
<span data-ttu-id="6d277-107">Un criterio di protezione è associato ad almeno un criterio di conservazione.</span><span class="sxs-lookup"><span data-stu-id="6d277-107">A protection policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="6d277-108">I criteri di conservazione definiscono la durata di un punto di ripristino con Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="6d277-108">The retention policy defines how long a recovery point is kept with Azure Backup.</span></span>
<span data-ttu-id="6d277-109">Puoi usare il cmdlet Get-AzRecoveryServicesBackupRetentionPolicyObject per ottenere i criteri di conservazione predefiniti.</span><span class="sxs-lookup"><span data-stu-id="6d277-109">You can use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet to get the default retention policy.</span></span>
<span data-ttu-id="6d277-110">Puoi usare il cmdlet Get-AzRecoveryServicesBackupSchedulePolicyObject per ottenere i criteri di pianificazione predefiniti.</span><span class="sxs-lookup"><span data-stu-id="6d277-110">And you can use the Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet to get the default schedule policy.</span></span>
<span data-ttu-id="6d277-111">Gli oggetti **SchedulePolicy** e **RetentionPolicy** vengono usati come input per il cmdlet **New-AzRecoveryServicesBackupProtectionPolicy** .</span><span class="sxs-lookup"><span data-stu-id="6d277-111">The **SchedulePolicy** and **RetentionPolicy** objects are used as inputs to the **New-AzRecoveryServicesBackupProtectionPolicy** cmdlet.</span></span>
<span data-ttu-id="6d277-112">Impostare il contesto del Vault usando il cmdlet Set-AzRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="6d277-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="6d277-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6d277-113">EXAMPLES</span></span>

### <span data-ttu-id="6d277-114">Esempio 1: creare un criterio di protezione del backup</span><span class="sxs-lookup"><span data-stu-id="6d277-114">Example 1: Create a Backup protection policy</span></span>
```powershell
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Dt = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($Dt.ToUniversalTime())
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="6d277-115">Il primo comando ottiene un **SchedulePolicyObject** di base e lo archivia nella variabile $SchPol.</span><span class="sxs-lookup"><span data-stu-id="6d277-115">The first command gets a base **SchedulePolicyObject**, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="6d277-116">Il secondo comando rimuove tutti i tempi di esecuzione pianificati dai criteri di pianificazione in $SchPol.</span><span class="sxs-lookup"><span data-stu-id="6d277-116">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>
<span data-ttu-id="6d277-117">Il terzo comando usa il cmdlet Get-Date per ottenere la data e l'ora correnti.</span><span class="sxs-lookup"><span data-stu-id="6d277-117">The third command uses the Get-Date cmdlet to get the current date and time.</span></span>
<span data-ttu-id="6d277-118">Il quarto comando aggiunge la data e l'ora correnti in $Dt come periodo di esecuzione programmato per i criteri di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="6d277-118">The fourth command adds the current date and time in $Dt as the scheduled run time to the schedule policy.</span></span>
<span data-ttu-id="6d277-119">Il quinto comando ottiene un oggetto **RetentionPolicy** di base e lo archivia nella variabile $RetPol.</span><span class="sxs-lookup"><span data-stu-id="6d277-119">The fifth command gets a base **RetentionPolicy** object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="6d277-120">Il sesto comando imposta i criteri durata di conservazione su 365 giorni.</span><span class="sxs-lookup"><span data-stu-id="6d277-120">The sixth command sets the retention duration policy to 365 days.</span></span>
<span data-ttu-id="6d277-121">Il comando finale crea un oggetto **BackupProtectionPolicy** basato sui criteri di pianificazione e conservazione creati dai comandi precedenti.</span><span class="sxs-lookup"><span data-stu-id="6d277-121">The final command creates a **BackupProtectionPolicy** object based on the schedule and retention policies created by the previous commands.</span></span>

### <span data-ttu-id="6d277-122">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="6d277-122">Example 2</span></span>

<span data-ttu-id="6d277-123">Crea un criterio di protezione del backup.</span><span class="sxs-lookup"><span data-stu-id="6d277-123">Creates a Backup protection policy.</span></span> <span data-ttu-id="6d277-124">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="6d277-124">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzRecoveryServicesBackupProtectionPolicy -Name 'NewPolicy' -RetentionPolicy $RetPol -SchedulePolicy $SchPol -VaultId $vault.ID -WorkloadType AzureVM
```

## <span data-ttu-id="6d277-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6d277-125">PARAMETERS</span></span>

### <span data-ttu-id="6d277-126">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="6d277-126">-BackupManagementType</span></span>
<span data-ttu-id="6d277-127">Classe di risorse protette.</span><span class="sxs-lookup"><span data-stu-id="6d277-127">The class of resources being protected.</span></span> <span data-ttu-id="6d277-128">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="6d277-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6d277-129">AzureVM</span><span class="sxs-lookup"><span data-stu-id="6d277-129">AzureVM</span></span> 
- <span data-ttu-id="6d277-130">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="6d277-130">AzureStorage</span></span>
- <span data-ttu-id="6d277-131">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="6d277-131">AzureWorkload</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureStorage, AzureWorkload

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d277-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d277-132">-DefaultProfile</span></span>
<span data-ttu-id="6d277-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6d277-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d277-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="6d277-134">-Name</span></span>
<span data-ttu-id="6d277-135">Specifica il nome del criterio.</span><span class="sxs-lookup"><span data-stu-id="6d277-135">Specifies the name of the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d277-136">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6d277-136">-RetentionPolicy</span></span>
<span data-ttu-id="6d277-137">Specifica l'oggetto **RetentionPolicy** di base.</span><span class="sxs-lookup"><span data-stu-id="6d277-137">Specifies the base **RetentionPolicy** object.</span></span>
<span data-ttu-id="6d277-138">Puoi usare il cmdlet Get-AzRecoveryServicesBackupRetentionPolicyObject per ottenere un oggetto **RetentionPolicy** .</span><span class="sxs-lookup"><span data-stu-id="6d277-138">You can use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet to get a **RetentionPolicy** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d277-139">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="6d277-139">-SchedulePolicy</span></span>
<span data-ttu-id="6d277-140">Specifica l'oggetto **SchedulePolicy** di base.</span><span class="sxs-lookup"><span data-stu-id="6d277-140">Specifies the base **SchedulePolicy** object.</span></span>
<span data-ttu-id="6d277-141">Puoi usare il cmdlet Get-AzRecoveryServicesBackupSchedulePolicyObject per ottenere un oggetto **SchedulePolicy** .</span><span class="sxs-lookup"><span data-stu-id="6d277-141">You can use the Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet to get a **SchedulePolicy** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d277-142">-VaultId</span><span class="sxs-lookup"><span data-stu-id="6d277-142">-VaultId</span></span>
<span data-ttu-id="6d277-143">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="6d277-143">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="6d277-144">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="6d277-144">-WorkloadType</span></span>
<span data-ttu-id="6d277-145">Tipo di carico di lavoro della risorsa.</span><span class="sxs-lookup"><span data-stu-id="6d277-145">Workload type of the resource.</span></span> <span data-ttu-id="6d277-146">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="6d277-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6d277-147">AzureVM</span><span class="sxs-lookup"><span data-stu-id="6d277-147">AzureVM</span></span> 
- <span data-ttu-id="6d277-148">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="6d277-148">AzureFiles</span></span>
- <span data-ttu-id="6d277-149">MSSQL</span><span class="sxs-lookup"><span data-stu-id="6d277-149">MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d277-150">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6d277-150">-Confirm</span></span>
<span data-ttu-id="6d277-151">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d277-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d277-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d277-152">-WhatIf</span></span>
<span data-ttu-id="6d277-153">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6d277-153">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="6d277-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d277-154">CommonParameters</span></span>
<span data-ttu-id="6d277-155">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d277-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d277-156">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d277-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d277-157">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6d277-157">INPUTS</span></span>

### <span data-ttu-id="6d277-158">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. WorkloadType</span><span class="sxs-lookup"><span data-stu-id="6d277-158">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType</span></span>

### <span data-ttu-id="6d277-159">System. Nullable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. BackupManagementType, Microsoft. Azure. PowerShell. Cmdlets. RecoveryServices. backup. Models, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6d277-159">System.Nullable\`1[[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType, Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.Models, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="6d277-160">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="6d277-160">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

### <span data-ttu-id="6d277-161">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="6d277-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

### <span data-ttu-id="6d277-162">System. String</span><span class="sxs-lookup"><span data-stu-id="6d277-162">System.String</span></span>

## <span data-ttu-id="6d277-163">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6d277-163">OUTPUTS</span></span>

### <span data-ttu-id="6d277-164">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="6d277-164">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="6d277-165">Note</span><span class="sxs-lookup"><span data-stu-id="6d277-165">NOTES</span></span>

## <span data-ttu-id="6d277-166">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6d277-166">RELATED LINKS</span></span>

[<span data-ttu-id="6d277-167">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="6d277-167">Enable-AzRecoveryServicesBackupProtection</span></span>](./Enable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="6d277-168">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6d277-168">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="6d277-169">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="6d277-169">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="6d277-170">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="6d277-170">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="6d277-171">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6d277-171">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="6d277-172">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6d277-172">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


