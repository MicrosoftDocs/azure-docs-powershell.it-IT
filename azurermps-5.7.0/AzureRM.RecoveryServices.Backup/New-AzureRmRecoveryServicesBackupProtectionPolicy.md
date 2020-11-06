---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/new-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/New-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/New-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: e9834236a72a68f64cc9b19d6576e56102f96b13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509719"
---
# <span data-ttu-id="74450-101">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="74450-101">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="74450-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="74450-102">SYNOPSIS</span></span>
<span data-ttu-id="74450-103">Crea un criterio di protezione del backup.</span><span class="sxs-lookup"><span data-stu-id="74450-103">Creates a Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74450-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="74450-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="74450-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74450-105">DESCRIPTION</span></span>
<span data-ttu-id="74450-106">Il cmdlet **New-AzureRmRecoveryServicesBackupProtectionPolicy** crea un criterio di protezione del backup in un Vault.</span><span class="sxs-lookup"><span data-stu-id="74450-106">The **New-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet creates a Backup protection policy in a vault.</span></span>
<span data-ttu-id="74450-107">Un criterio di protezione è associato ad almeno un criterio di conservazione.</span><span class="sxs-lookup"><span data-stu-id="74450-107">A protection policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="74450-108">I criteri di conservazione definiscono la durata di un punto di ripristino con Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="74450-108">The retention policy defines how long a recovery point is kept with Azure Backup.</span></span>

<span data-ttu-id="74450-109">Puoi usare il cmdlet Get-AzureRmRecoveryServicesBackupRetentionPolicyObject per ottenere i criteri di conservazione predefiniti.</span><span class="sxs-lookup"><span data-stu-id="74450-109">You can use the Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet to get the default retention policy.</span></span>
<span data-ttu-id="74450-110">Puoi usare il cmdlet Get-AzureRmRecoveryServicesBackupSchedulePolicyObject per ottenere i criteri di pianificazione predefiniti.</span><span class="sxs-lookup"><span data-stu-id="74450-110">And you can use the Get-AzureRmRecoveryServicesBackupSchedulePolicyObject cmdlet to get the default schedule policy.</span></span>
<span data-ttu-id="74450-111">Gli oggetti **SchedulePolicy** e **RetentionPolicy** vengono usati come input per il cmdlet **New-AzureRmRecoveryServicesBackupProtectionPolicy** .</span><span class="sxs-lookup"><span data-stu-id="74450-111">The **SchedulePolicy** and **RetentionPolicy** objects are used as inputs to the **New-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet.</span></span>

<span data-ttu-id="74450-112">Impostare il contesto del Vault usando il cmdlet Set-AzureRmRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="74450-112">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="74450-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="74450-113">EXAMPLES</span></span>

### <span data-ttu-id="74450-114">Esempio 1: creare un criterio di protezione del backup</span><span class="sxs-lookup"><span data-stu-id="74450-114">Example 1: Create a Backup protection policy</span></span>
```
PS C:\> $SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Dt = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($Dt.ToUniversalTime())
PS C:\> $RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="74450-115">Il primo comando ottiene un **SchedulePolicyObject** di base e lo archivia nella variabile $SchPol.</span><span class="sxs-lookup"><span data-stu-id="74450-115">The first command gets a base **SchedulePolicyObject** , and then stores it in the $SchPol variable.</span></span>

<span data-ttu-id="74450-116">Il secondo comando rimuove tutti i tempi di esecuzione pianificati dai criteri di pianificazione in $SchPol.</span><span class="sxs-lookup"><span data-stu-id="74450-116">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>

<span data-ttu-id="74450-117">Il terzo comando usa il cmdlet Get-Date per ottenere la data e l'ora correnti.</span><span class="sxs-lookup"><span data-stu-id="74450-117">The third command uses the Get-Date cmdlet to get the current date and time.</span></span>

<span data-ttu-id="74450-118">Il quarto comando aggiunge la data e l'ora correnti in $Dt come periodo di esecuzione programmato per i criteri di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="74450-118">The fourth command adds the current date and time in $Dt as the scheduled run time to the schedule policy.</span></span>

<span data-ttu-id="74450-119">Il quinto comando ottiene un oggetto **RetentionPolicy** di base e lo archivia nella variabile $RetPol.</span><span class="sxs-lookup"><span data-stu-id="74450-119">The fifth command gets a base **RetentionPolicy** object, and then stores it in the $RetPol variable.</span></span>

<span data-ttu-id="74450-120">Il sesto comando imposta i criteri durata di conservazione su 365 giorni.</span><span class="sxs-lookup"><span data-stu-id="74450-120">The sixth command sets the retention duration policy to 365 days.</span></span>

<span data-ttu-id="74450-121">Il comando finale crea un oggetto **BackupProtectionPolicy** basato sui criteri di pianificazione e conservazione creati dai comandi precedenti.</span><span class="sxs-lookup"><span data-stu-id="74450-121">The final command creates a **BackupProtectionPolicy** object based on the schedule and retention policies created by the previous commands.</span></span>

## <span data-ttu-id="74450-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="74450-122">PARAMETERS</span></span>

### <span data-ttu-id="74450-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="74450-123">-BackupManagementType</span></span>
<span data-ttu-id="74450-124">Specifica il tipo di gestione del backup.</span><span class="sxs-lookup"><span data-stu-id="74450-124">Specifies the Backup management type.</span></span>
<span data-ttu-id="74450-125">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="74450-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="74450-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="74450-126">AzureVM</span></span> 
- <span data-ttu-id="74450-127">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="74450-127">AzureSQLDatabase</span></span>

```yaml
Type: BackupManagementType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74450-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74450-128">-DefaultProfile</span></span>
<span data-ttu-id="74450-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="74450-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74450-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="74450-130">-Name</span></span>
<span data-ttu-id="74450-131">Specifica il nome del criterio.</span><span class="sxs-lookup"><span data-stu-id="74450-131">Specifies the name of the policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74450-132">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="74450-132">-RetentionPolicy</span></span>
<span data-ttu-id="74450-133">Specifica l'oggetto **RetentionPolicy** di base.</span><span class="sxs-lookup"><span data-stu-id="74450-133">Specifies the base **RetentionPolicy** object.</span></span>
<span data-ttu-id="74450-134">Puoi usare il cmdlet Get-AzureRmRecoveryServicesBackupRetentionPolicyObject per ottenere un oggetto **RetentionPolicy** .</span><span class="sxs-lookup"><span data-stu-id="74450-134">You can use the Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet to get a **RetentionPolicy** object.</span></span>

```yaml
Type: RetentionPolicyBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74450-135">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="74450-135">-SchedulePolicy</span></span>
<span data-ttu-id="74450-136">Specifica l'oggetto **SchedulePolicy** di base.</span><span class="sxs-lookup"><span data-stu-id="74450-136">Specifies the base **SchedulePolicy** object.</span></span>
<span data-ttu-id="74450-137">Puoi usare il cmdlet Get-AzureRmRecoveryServicesBackupSchedulePolicyObject per ottenere un oggetto **SchedulePolicy** .</span><span class="sxs-lookup"><span data-stu-id="74450-137">You can use the Get-AzureRmRecoveryServicesBackupSchedulePolicyObject cmdlet to get a **SchedulePolicy** object.</span></span>

```yaml
Type: SchedulePolicyBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74450-138">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="74450-138">-WorkloadType</span></span>
<span data-ttu-id="74450-139">Specifica il tipo di carico di lavoro.</span><span class="sxs-lookup"><span data-stu-id="74450-139">Specifies the workload type.</span></span>
<span data-ttu-id="74450-140">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="74450-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="74450-141">AzureVM</span><span class="sxs-lookup"><span data-stu-id="74450-141">AzureVM</span></span> 
- <span data-ttu-id="74450-142">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="74450-142">AzureSQLDatabase</span></span>

```yaml
Type: WorkloadType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74450-143">-Confermare</span><span class="sxs-lookup"><span data-stu-id="74450-143">-Confirm</span></span>
<span data-ttu-id="74450-144">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74450-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74450-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74450-145">-WhatIf</span></span>
<span data-ttu-id="74450-146">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="74450-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="74450-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="74450-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74450-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74450-148">CommonParameters</span></span>
<span data-ttu-id="74450-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74450-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74450-150">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74450-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74450-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="74450-151">INPUTS</span></span>

### <span data-ttu-id="74450-152">Nessuno</span><span class="sxs-lookup"><span data-stu-id="74450-152">None</span></span>
<span data-ttu-id="74450-153">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="74450-153">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="74450-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="74450-154">OUTPUTS</span></span>

### <span data-ttu-id="74450-155">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="74450-155">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="74450-156">Note</span><span class="sxs-lookup"><span data-stu-id="74450-156">NOTES</span></span>

## <span data-ttu-id="74450-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="74450-157">RELATED LINKS</span></span>

[<span data-ttu-id="74450-158">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="74450-158">Enable-AzureRmRecoveryServicesBackupProtection</span></span>](./Enable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="74450-159">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="74450-159">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="74450-160">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="74450-160">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="74450-161">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="74450-161">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="74450-162">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="74450-162">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="74450-163">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="74450-163">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


