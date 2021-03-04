---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 65bda3a4829971ce3d073c672b578099130fae6e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953310"
---
# <span data-ttu-id="68eef-101">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="68eef-101">New-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="68eef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68eef-102">SYNOPSIS</span></span>
<span data-ttu-id="68eef-103">Crea criteri di protezione per il backup.</span><span class="sxs-lookup"><span data-stu-id="68eef-103">Creates a Backup protection policy.</span></span>

## <span data-ttu-id="68eef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="68eef-104">SYNTAX</span></span>

```
New-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68eef-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="68eef-105">DESCRIPTION</span></span>
<span data-ttu-id="68eef-106">Il cmdlet **New-AzRecoveryServicesBackupProtectionPolicy** crea un criterio di protezione del backup in un vault.</span><span class="sxs-lookup"><span data-stu-id="68eef-106">The **New-AzRecoveryServicesBackupProtectionPolicy** cmdlet creates a Backup protection policy in a vault.</span></span>
<span data-ttu-id="68eef-107">I criteri di protezione sono associati ad almeno un criterio di conservazione.</span><span class="sxs-lookup"><span data-stu-id="68eef-107">A protection policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="68eef-108">I criteri di conservazione definiscono per quanto tempo viene mantenuto un punto di ripristino con Backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="68eef-108">The retention policy defines how long a recovery point is kept with Azure Backup.</span></span>
<span data-ttu-id="68eef-109">È possibile usare il cmdlet Get-AzRecoveryServicesBackupRetentionPolicyObject per ottenere i criteri di conservazione predefiniti.</span><span class="sxs-lookup"><span data-stu-id="68eef-109">You can use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet to get the default retention policy.</span></span>
<span data-ttu-id="68eef-110">È anche possibile usare il cmdlet Get-AzRecoveryServicesBackupSchedulePolicyObject per ottenere i criteri di pianificazione predefiniti.</span><span class="sxs-lookup"><span data-stu-id="68eef-110">And you can use the Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet to get the default schedule policy.</span></span>
<span data-ttu-id="68eef-111">Gli **oggetti SchedulePolicy** **e RetentionPolicy** vengono usati come input del cmdlet **New-AzRecoveryServicesBackupProtectionPolicy.**</span><span class="sxs-lookup"><span data-stu-id="68eef-111">The **SchedulePolicy** and **RetentionPolicy** objects are used as inputs to the **New-AzRecoveryServicesBackupProtectionPolicy** cmdlet.</span></span>
<span data-ttu-id="68eef-112">Impostare il contesto del vault usando il cmdlet Set-AzRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="68eef-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="68eef-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="68eef-113">EXAMPLES</span></span>

### <span data-ttu-id="68eef-114">Esempio 1: Creare criteri di protezione per il backup</span><span class="sxs-lookup"><span data-stu-id="68eef-114">Example 1: Create a Backup protection policy</span></span>
```powershell
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Dt = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($Dt.ToUniversalTime())
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="68eef-115">Il primo comando ottiene un oggetto **SchedulePolicyObject** di base, quindi lo archivia nella $SchPol variabile.</span><span class="sxs-lookup"><span data-stu-id="68eef-115">The first command gets a base **SchedulePolicyObject**, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="68eef-116">Il secondo comando rimuove tutti gli orari di esecuzione pianificati dai criteri di pianificazione $SchPol.</span><span class="sxs-lookup"><span data-stu-id="68eef-116">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>
<span data-ttu-id="68eef-117">Il terzo comando usa il cmdlet Get-Date per ottenere la data e l'ora correnti.</span><span class="sxs-lookup"><span data-stu-id="68eef-117">The third command uses the Get-Date cmdlet to get the current date and time.</span></span>
<span data-ttu-id="68eef-118">Il quarto comando aggiunge la data e l'ora correnti in $Dt tempo di esecuzione pianificato ai criteri di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="68eef-118">The fourth command adds the current date and time in $Dt as the scheduled run time to the schedule policy.</span></span>
<span data-ttu-id="68eef-119">Il quinto comando ottiene un **oggetto RetentionPolicy** di base e quindi lo archivia nella $RetPol variabile.</span><span class="sxs-lookup"><span data-stu-id="68eef-119">The fifth command gets a base **RetentionPolicy** object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="68eef-120">Il sesto comando imposta i criteri di durata della conservazione su 365 giorni.</span><span class="sxs-lookup"><span data-stu-id="68eef-120">The sixth command sets the retention duration policy to 365 days.</span></span>
<span data-ttu-id="68eef-121">Il comando finale crea un **oggetto BackupProtectionPolicy** in base ai criteri di pianificazione e conservazione creati dai comandi precedenti.</span><span class="sxs-lookup"><span data-stu-id="68eef-121">The final command creates a **BackupProtectionPolicy** object based on the schedule and retention policies created by the previous commands.</span></span>

### <span data-ttu-id="68eef-122">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="68eef-122">Example 2</span></span>

<span data-ttu-id="68eef-123">Crea criteri di protezione per il backup.</span><span class="sxs-lookup"><span data-stu-id="68eef-123">Creates a Backup protection policy.</span></span> <span data-ttu-id="68eef-124">(autogenerati)</span><span class="sxs-lookup"><span data-stu-id="68eef-124">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzRecoveryServicesBackupProtectionPolicy -Name 'NewPolicy' -RetentionPolicy $RetPol -SchedulePolicy $SchPol -VaultId $vault.ID -WorkloadType AzureVM
```

## <span data-ttu-id="68eef-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="68eef-125">PARAMETERS</span></span>

### <span data-ttu-id="68eef-126">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="68eef-126">-BackupManagementType</span></span>
<span data-ttu-id="68eef-127">Classe di risorse protetta.</span><span class="sxs-lookup"><span data-stu-id="68eef-127">The class of resources being protected.</span></span> <span data-ttu-id="68eef-128">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="68eef-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="68eef-129">AzureVM</span><span class="sxs-lookup"><span data-stu-id="68eef-129">AzureVM</span></span> 
- <span data-ttu-id="68eef-130">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="68eef-130">AzureStorage</span></span>
- <span data-ttu-id="68eef-131">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="68eef-131">AzureWorkload</span></span>

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

### <span data-ttu-id="68eef-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68eef-132">-DefaultProfile</span></span>
<span data-ttu-id="68eef-133">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="68eef-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68eef-134">-Name</span><span class="sxs-lookup"><span data-stu-id="68eef-134">-Name</span></span>
<span data-ttu-id="68eef-135">Specifica il nome del criterio.</span><span class="sxs-lookup"><span data-stu-id="68eef-135">Specifies the name of the policy.</span></span>

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

### <span data-ttu-id="68eef-136">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="68eef-136">-RetentionPolicy</span></span>
<span data-ttu-id="68eef-137">Specifica l'oggetto **RetentionPolicy di** base.</span><span class="sxs-lookup"><span data-stu-id="68eef-137">Specifies the base **RetentionPolicy** object.</span></span>
<span data-ttu-id="68eef-138">È possibile usare il cmdlet Get-AzRecoveryServicesBackupRetentionPolicyObject per ottenere un **oggetto RetentionPolicy.**</span><span class="sxs-lookup"><span data-stu-id="68eef-138">You can use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet to get a **RetentionPolicy** object.</span></span>

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

### <span data-ttu-id="68eef-139">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="68eef-139">-SchedulePolicy</span></span>
<span data-ttu-id="68eef-140">Specifica **l'oggetto SchedulePolicy di** base.</span><span class="sxs-lookup"><span data-stu-id="68eef-140">Specifies the base **SchedulePolicy** object.</span></span>
<span data-ttu-id="68eef-141">È possibile usare il cmdlet Get-AzRecoveryServicesBackupSchedulePolicyObject per ottenere un **oggetto SchedulePolicy.**</span><span class="sxs-lookup"><span data-stu-id="68eef-141">You can use the Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet to get a **SchedulePolicy** object.</span></span>

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

### <span data-ttu-id="68eef-142">-VaultId</span><span class="sxs-lookup"><span data-stu-id="68eef-142">-VaultId</span></span>
<span data-ttu-id="68eef-143">ARM ID del Vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="68eef-143">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="68eef-144">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="68eef-144">-WorkloadType</span></span>
<span data-ttu-id="68eef-145">Tipo di carico di lavoro della risorsa.</span><span class="sxs-lookup"><span data-stu-id="68eef-145">Workload type of the resource.</span></span> <span data-ttu-id="68eef-146">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="68eef-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="68eef-147">AzureVM</span><span class="sxs-lookup"><span data-stu-id="68eef-147">AzureVM</span></span> 
- <span data-ttu-id="68eef-148">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="68eef-148">AzureFiles</span></span>
- <span data-ttu-id="68eef-149">MSSQL</span><span class="sxs-lookup"><span data-stu-id="68eef-149">MSSQL</span></span>

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

### <span data-ttu-id="68eef-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="68eef-150">-Confirm</span></span>
<span data-ttu-id="68eef-151">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68eef-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68eef-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68eef-152">-WhatIf</span></span>
<span data-ttu-id="68eef-153">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="68eef-153">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="68eef-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68eef-154">CommonParameters</span></span>
<span data-ttu-id="68eef-155">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68eef-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68eef-156">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="68eef-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68eef-157">INPUT</span><span class="sxs-lookup"><span data-stu-id="68eef-157">INPUTS</span></span>

### <span data-ttu-id="68eef-158">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType</span><span class="sxs-lookup"><span data-stu-id="68eef-158">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType</span></span>

### <span data-ttu-id="68eef-159">System.Nullable'1[[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType, Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.Models, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="68eef-159">System.Nullable\`1[[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType, Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.Models, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="68eef-160">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="68eef-160">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

### <span data-ttu-id="68eef-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="68eef-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

### <span data-ttu-id="68eef-162">System.String</span><span class="sxs-lookup"><span data-stu-id="68eef-162">System.String</span></span>

## <span data-ttu-id="68eef-163">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="68eef-163">OUTPUTS</span></span>

### <span data-ttu-id="68eef-164">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span><span class="sxs-lookup"><span data-stu-id="68eef-164">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="68eef-165">NOTE</span><span class="sxs-lookup"><span data-stu-id="68eef-165">NOTES</span></span>

## <span data-ttu-id="68eef-166">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="68eef-166">RELATED LINKS</span></span>

[<span data-ttu-id="68eef-167">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="68eef-167">Enable-AzRecoveryServicesBackupProtection</span></span>](./Enable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="68eef-168">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="68eef-168">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="68eef-169">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="68eef-169">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="68eef-170">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="68eef-170">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="68eef-171">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="68eef-171">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="68eef-172">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="68eef-172">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


