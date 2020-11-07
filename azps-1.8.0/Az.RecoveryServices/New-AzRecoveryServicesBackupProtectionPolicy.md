---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 6aaf7fcd32ae7d50f273d69835f9131032b68c21
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677608"
---
# <span data-ttu-id="815cc-101">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="815cc-101">New-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="815cc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="815cc-102">SYNOPSIS</span></span>
<span data-ttu-id="815cc-103">Crea un criterio di protezione del backup.</span><span class="sxs-lookup"><span data-stu-id="815cc-103">Creates a Backup protection policy.</span></span>

## <span data-ttu-id="815cc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="815cc-104">SYNTAX</span></span>

```
New-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="815cc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="815cc-105">DESCRIPTION</span></span>
<span data-ttu-id="815cc-106">Il cmdlet **New-AzRecoveryServicesBackupProtectionPolicy** crea un criterio di protezione del backup in un Vault.</span><span class="sxs-lookup"><span data-stu-id="815cc-106">The **New-AzRecoveryServicesBackupProtectionPolicy** cmdlet creates a Backup protection policy in a vault.</span></span>
<span data-ttu-id="815cc-107">Un criterio di protezione è associato ad almeno un criterio di conservazione.</span><span class="sxs-lookup"><span data-stu-id="815cc-107">A protection policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="815cc-108">I criteri di conservazione definiscono la durata di un punto di ripristino con Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="815cc-108">The retention policy defines how long a recovery point is kept with Azure Backup.</span></span>
<span data-ttu-id="815cc-109">Puoi usare il cmdlet Get-AzRecoveryServicesBackupRetentionPolicyObject per ottenere i criteri di conservazione predefiniti.</span><span class="sxs-lookup"><span data-stu-id="815cc-109">You can use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet to get the default retention policy.</span></span>
<span data-ttu-id="815cc-110">Puoi usare il cmdlet Get-AzRecoveryServicesBackupSchedulePolicyObject per ottenere i criteri di pianificazione predefiniti.</span><span class="sxs-lookup"><span data-stu-id="815cc-110">And you can use the Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet to get the default schedule policy.</span></span>
<span data-ttu-id="815cc-111">Gli oggetti **SchedulePolicy** e **RetentionPolicy** vengono usati come input per il cmdlet **New-AzRecoveryServicesBackupProtectionPolicy** .</span><span class="sxs-lookup"><span data-stu-id="815cc-111">The **SchedulePolicy** and **RetentionPolicy** objects are used as inputs to the **New-AzRecoveryServicesBackupProtectionPolicy** cmdlet.</span></span>
<span data-ttu-id="815cc-112">Impostare il contesto del Vault usando il cmdlet Set-AzRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="815cc-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="815cc-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="815cc-113">EXAMPLES</span></span>

### <span data-ttu-id="815cc-114">Esempio 1: creare un criterio di protezione del backup</span><span class="sxs-lookup"><span data-stu-id="815cc-114">Example 1: Create a Backup protection policy</span></span>
```
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Dt = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($Dt.ToUniversalTime())
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="815cc-115">Il primo comando ottiene un **SchedulePolicyObject** di base e lo archivia nella variabile $SchPol.</span><span class="sxs-lookup"><span data-stu-id="815cc-115">The first command gets a base **SchedulePolicyObject** , and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="815cc-116">Il secondo comando rimuove tutti i tempi di esecuzione pianificati dai criteri di pianificazione in $SchPol.</span><span class="sxs-lookup"><span data-stu-id="815cc-116">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>
<span data-ttu-id="815cc-117">Il terzo comando usa il cmdlet Get-Date per ottenere la data e l'ora correnti.</span><span class="sxs-lookup"><span data-stu-id="815cc-117">The third command uses the Get-Date cmdlet to get the current date and time.</span></span>
<span data-ttu-id="815cc-118">Il quarto comando aggiunge la data e l'ora correnti in $Dt come periodo di esecuzione programmato per i criteri di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="815cc-118">The fourth command adds the current date and time in $Dt as the scheduled run time to the schedule policy.</span></span>
<span data-ttu-id="815cc-119">Il quinto comando ottiene un oggetto **RetentionPolicy** di base e lo archivia nella variabile $RetPol.</span><span class="sxs-lookup"><span data-stu-id="815cc-119">The fifth command gets a base **RetentionPolicy** object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="815cc-120">Il sesto comando imposta i criteri durata di conservazione su 365 giorni.</span><span class="sxs-lookup"><span data-stu-id="815cc-120">The sixth command sets the retention duration policy to 365 days.</span></span>
<span data-ttu-id="815cc-121">Il comando finale crea un oggetto **BackupProtectionPolicy** basato sui criteri di pianificazione e conservazione creati dai comandi precedenti.</span><span class="sxs-lookup"><span data-stu-id="815cc-121">The final command creates a **BackupProtectionPolicy** object based on the schedule and retention policies created by the previous commands.</span></span>

## <span data-ttu-id="815cc-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="815cc-122">PARAMETERS</span></span>

### <span data-ttu-id="815cc-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="815cc-123">-BackupManagementType</span></span>
<span data-ttu-id="815cc-124">Specifica il tipo di gestione del backup.</span><span class="sxs-lookup"><span data-stu-id="815cc-124">Specifies the Backup management type.</span></span>
<span data-ttu-id="815cc-125">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="815cc-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="815cc-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="815cc-126">AzureVM</span></span> 
- <span data-ttu-id="815cc-127">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="815cc-127">AzureSQLDatabase</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="815cc-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="815cc-128">-DefaultProfile</span></span>
<span data-ttu-id="815cc-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="815cc-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="815cc-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="815cc-130">-Name</span></span>
<span data-ttu-id="815cc-131">Specifica il nome del criterio.</span><span class="sxs-lookup"><span data-stu-id="815cc-131">Specifies the name of the policy.</span></span>

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

### <span data-ttu-id="815cc-132">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="815cc-132">-RetentionPolicy</span></span>
<span data-ttu-id="815cc-133">Specifica l'oggetto **RetentionPolicy** di base.</span><span class="sxs-lookup"><span data-stu-id="815cc-133">Specifies the base **RetentionPolicy** object.</span></span>
<span data-ttu-id="815cc-134">Puoi usare il cmdlet Get-AzRecoveryServicesBackupRetentionPolicyObject per ottenere un oggetto **RetentionPolicy** .</span><span class="sxs-lookup"><span data-stu-id="815cc-134">You can use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet to get a **RetentionPolicy** object.</span></span>

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

### <span data-ttu-id="815cc-135">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="815cc-135">-SchedulePolicy</span></span>
<span data-ttu-id="815cc-136">Specifica l'oggetto **SchedulePolicy** di base.</span><span class="sxs-lookup"><span data-stu-id="815cc-136">Specifies the base **SchedulePolicy** object.</span></span>
<span data-ttu-id="815cc-137">Puoi usare il cmdlet Get-AzRecoveryServicesBackupSchedulePolicyObject per ottenere un oggetto **SchedulePolicy** .</span><span class="sxs-lookup"><span data-stu-id="815cc-137">You can use the Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet to get a **SchedulePolicy** object.</span></span>

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

### <span data-ttu-id="815cc-138">-VaultId</span><span class="sxs-lookup"><span data-stu-id="815cc-138">-VaultId</span></span>
<span data-ttu-id="815cc-139">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="815cc-139">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="815cc-140">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="815cc-140">-WorkloadType</span></span>
<span data-ttu-id="815cc-141">Specifica il tipo di carico di lavoro.</span><span class="sxs-lookup"><span data-stu-id="815cc-141">Specifies the workload type.</span></span>
<span data-ttu-id="815cc-142">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="815cc-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="815cc-143">AzureVM</span><span class="sxs-lookup"><span data-stu-id="815cc-143">AzureVM</span></span> 
- <span data-ttu-id="815cc-144">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="815cc-144">AzureSQLDatabase</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="815cc-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="815cc-145">-Confirm</span></span>
<span data-ttu-id="815cc-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="815cc-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="815cc-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="815cc-147">-WhatIf</span></span>
<span data-ttu-id="815cc-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="815cc-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="815cc-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="815cc-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="815cc-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="815cc-150">CommonParameters</span></span>
<span data-ttu-id="815cc-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="815cc-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="815cc-152">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="815cc-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="815cc-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="815cc-153">INPUTS</span></span>

### <span data-ttu-id="815cc-154">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. WorkloadType</span><span class="sxs-lookup"><span data-stu-id="815cc-154">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType</span></span>

### <span data-ttu-id="815cc-155">System. Nullable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. BackupManagementType, Microsoft. Azure. PowerShell. Cmdlets. RecoveryServices. backup. Models, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="815cc-155">System.Nullable\`1[[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType, Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.Models, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="815cc-156">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="815cc-156">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

### <span data-ttu-id="815cc-157">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="815cc-157">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

### <span data-ttu-id="815cc-158">System. String</span><span class="sxs-lookup"><span data-stu-id="815cc-158">System.String</span></span>

## <span data-ttu-id="815cc-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="815cc-159">OUTPUTS</span></span>

### <span data-ttu-id="815cc-160">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="815cc-160">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="815cc-161">Note</span><span class="sxs-lookup"><span data-stu-id="815cc-161">NOTES</span></span>

## <span data-ttu-id="815cc-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="815cc-162">RELATED LINKS</span></span>

[<span data-ttu-id="815cc-163">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="815cc-163">Enable-AzRecoveryServicesBackupProtection</span></span>](./Enable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="815cc-164">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="815cc-164">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="815cc-165">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="815cc-165">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="815cc-166">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="815cc-166">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="815cc-167">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="815cc-167">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="815cc-168">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="815cc-168">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


