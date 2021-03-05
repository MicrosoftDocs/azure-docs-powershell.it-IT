---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/update-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 2255a2397c7096ec1a7b5f45dc4fa699649b071a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005821"
---
# <span data-ttu-id="b1b45-101">Update-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="b1b45-101">Update-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="b1b45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1b45-102">SYNOPSIS</span></span>
<span data-ttu-id="b1b45-103">Aggiorna i criteri di replica di Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b1b45-103">Updates an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="b1b45-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b1b45-104">SYNTAX</span></span>

### <span data-ttu-id="b1b45-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b1b45-105">Default (Default)</span></span>
```
Update-AzRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-RecoveryAzureStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b1b45-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="b1b45-106">VMwareToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-VMwareToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1b45-107">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="b1b45-107">AzureToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-AzureToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b1b45-108">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="b1b45-108">AzureToVMware</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-AzureToVMware] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1b45-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="b1b45-109">HyperVToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-HyperVToAzure] -InputObject <ASRPolicy>
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b1b45-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="b1b45-110">EnterpriseToEnterprise</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-VmmToVmm] -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1b45-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b1b45-111">DESCRIPTION</span></span>
<span data-ttu-id="b1b45-112">Il cmdlet **Update-AzRecoveryServicesAsrPolicy** aggiorna i criteri di replica di Azure Site Recovery specificati.</span><span class="sxs-lookup"><span data-stu-id="b1b45-112">The **Update-AzRecoveryServicesAsrPolicy** cmdlet updates the specified Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="b1b45-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b1b45-113">EXAMPLES</span></span>

### <span data-ttu-id="b1b45-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b1b45-114">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrPolicy -Policy $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="b1b45-115">Avvia l'operazione dei criteri di replica degli aggiornamenti usando i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="b1b45-115">Starts the update replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="b1b45-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b1b45-116">Example 2</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="b1b45-117">Avvia l'operazione di aggiornamento da Azure a Criteri di replica di Azure usando i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="b1b45-117">Starts the update azure to azure replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="b1b45-118">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="b1b45-118">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -RecoveryPointRetentionInHours 20
```

<span data-ttu-id="b1b45-119">Avvia l'aggiornamento dei criteri di replica di Azure ad Azure usando i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="b1b45-119">Starts the update azure to azure replication policy using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="b1b45-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1b45-120">PARAMETERS</span></span>

### <span data-ttu-id="b1b45-121">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="b1b45-121">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="b1b45-122">Specifica la frequenza in ore in cui creare punti di ripristino coerenti dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b1b45-122">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1b45-123">-Autenticazione</span><span class="sxs-lookup"><span data-stu-id="b1b45-123">-Authentication</span></span>
<span data-ttu-id="b1b45-124">Specifica il tipo di autenticazione usata.</span><span class="sxs-lookup"><span data-stu-id="b1b45-124">Specifies the type of authentication used.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1b45-125">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="b1b45-125">-AzureToAzure</span></span>
<span data-ttu-id="b1b45-126">Specifica il ripristino di emergenza da Azure ad Azure.</span><span class="sxs-lookup"><span data-stu-id="b1b45-126">Specifies the Azure to Azure disaster recovery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1b45-127">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="b1b45-127">-AzureToVMware</span></span>
<span data-ttu-id="b1b45-128">Specifica il ripristino di emergenza da Azure a vMWare.</span><span class="sxs-lookup"><span data-stu-id="b1b45-128">Specifies the Azure to vMWare disaster recovery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1b45-129">-Compression</span><span class="sxs-lookup"><span data-stu-id="b1b45-129">-Compression</span></span>
<span data-ttu-id="b1b45-130">Specifica se deve essere abilitata la compressione.</span><span class="sxs-lookup"><span data-stu-id="b1b45-130">Specifies if compression should be enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1b45-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1b45-131">-DefaultProfile</span></span>
<span data-ttu-id="b1b45-132">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b1b45-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="b1b45-133">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="b1b45-133">-HyperVToAzure</span></span>
<span data-ttu-id="b1b45-134">Parametro di parametro che indica che il criterio specificato viene usato per replicare le macchine virtuali di Hyper-V in Azure.</span><span class="sxs-lookup"><span data-stu-id="b1b45-134">Switch parameter indicating that the specified policy is used to replicate Hyper-V virtual machines to Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HyperVToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1b45-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1b45-135">-InputObject</span></span>
<span data-ttu-id="b1b45-136">Oggetto di input per il cmdlet: specifica l'oggetto criterio di replica ASR corrispondente ai criteri di replica da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="b1b45-136">Input object for the cmdlet: Specifies the ASR replication policy object corresponding to the replication policy to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1b45-137">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="b1b45-137">-MultiVmSyncStatus</span></span>
<span data-ttu-id="b1b45-138">Specifica lo stato di sincronizzazione multiVm per il criterio.</span><span class="sxs-lookup"><span data-stu-id="b1b45-138">Specifies multiVm sync status for the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, AzureToAzure, AzureToVMware
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1b45-139">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="b1b45-139">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="b1b45-140">Specifica i punti di ripristino del numero da conservare.</span><span class="sxs-lookup"><span data-stu-id="b1b45-140">Specifies the number recovery points to retain.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases: RecoveryPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1b45-141">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="b1b45-141">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="b1b45-142">Specifica l'ID account di archiviazione di Azure della destinazione della replica.</span><span class="sxs-lookup"><span data-stu-id="b1b45-142">Specifies the Azure storage account ID of the replication target.</span></span> <span data-ttu-id="b1b45-143">Usato come account di archiviazione di destinazione per la replica se non viene fornita un'alternativa durante l'abilitazione della replica con il cmdlet New-AzRecoveryServicesASRReplicationProtectedItem destinazione.</span><span class="sxs-lookup"><span data-stu-id="b1b45-143">Used as the target storage account for replication if an alternate is not provided while enabling replication using the New-AzRecoveryServicesASRReplicationProtectedItem cmdlet.</span></span>


```yaml
Type: System.String
Parameter Sets: Default, HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1b45-144">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="b1b45-144">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="b1b45-145">Tempo in ore per conservare i punti di ripristino dopo la creazione.</span><span class="sxs-lookup"><span data-stu-id="b1b45-145">Time in hours to retain recovery points after creation.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VMwareToAzure, AzureToAzure, AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1b45-146">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="b1b45-146">-ReplicaDeletion</span></span>
<span data-ttu-id="b1b45-147">Specifica se la macchina virtuale di replica deve essere eliminata quando si disabilita la replica da un sito gestito DA ANDR A un altro.</span><span class="sxs-lookup"><span data-stu-id="b1b45-147">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1b45-148">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="b1b45-148">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="b1b45-149">Specifica l'intervallo della frequenza di replica in secondi.</span><span class="sxs-lookup"><span data-stu-id="b1b45-149">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="b1b45-150">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="b1b45-150">Valid values are:</span></span>

- <span data-ttu-id="b1b45-151">30</span><span class="sxs-lookup"><span data-stu-id="b1b45-151">30</span></span>
- <span data-ttu-id="b1b45-152">300</span><span class="sxs-lookup"><span data-stu-id="b1b45-152">300</span></span>
- <span data-ttu-id="b1b45-153">900</span><span class="sxs-lookup"><span data-stu-id="b1b45-153">900</span></span>

```yaml
Type: System.String
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases:
Accepted values: 30, 300, 900

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1b45-154">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="b1b45-154">-ReplicationMethod</span></span>
<span data-ttu-id="b1b45-155">Specifica il metodo di replica.</span><span class="sxs-lookup"><span data-stu-id="b1b45-155">Specifies the replication method.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1b45-156">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="b1b45-156">-ReplicationPort</span></span>
<span data-ttu-id="b1b45-157">Specifica la porta usata per la replica.</span><span class="sxs-lookup"><span data-stu-id="b1b45-157">Specifies the port used for replication.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1b45-158">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="b1b45-158">-ReplicationStartTime</span></span>
<span data-ttu-id="b1b45-159">Specifica l'ora di inizio della replica.</span><span class="sxs-lookup"><span data-stu-id="b1b45-159">Specifies the replication start time.</span></span>
<span data-ttu-id="b1b45-160">Non deve essere oltre le 24 ore dall'inizio del processo.</span><span class="sxs-lookup"><span data-stu-id="b1b45-160">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1b45-161">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="b1b45-161">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="b1b45-162">Valore soglia RPO in minuti per l'avviso.</span><span class="sxs-lookup"><span data-stu-id="b1b45-162">The RPO threshold value in minutes to warn on.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VMwareToAzure, AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1b45-163">-PiùVmm</span><span class="sxs-lookup"><span data-stu-id="b1b45-163">-VmmToVmm</span></span>
<span data-ttu-id="b1b45-164">Parametro di parametro che indica che il criterio specificato viene usato per replicare le macchine virtuali Di Hyper-V gestite IN ALTRO MODO tra due siti di Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="b1b45-164">Switch parameter indicating that the specified policy is used to replicate VMM managed Hyper-V virtual machines between two Hyper-V sites.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1b45-165">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="b1b45-165">-VMwareToAzure</span></span>
<span data-ttu-id="b1b45-166">Parametro di parametro che indica che il criterio specificato viene usato per replicare le macchine virtuali VMware in Azure.</span><span class="sxs-lookup"><span data-stu-id="b1b45-166">Switch parameter indicating that the specified policy is used to replicate VMware virtual machines to Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1b45-167">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b1b45-167">-Confirm</span></span>
<span data-ttu-id="b1b45-168">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1b45-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1b45-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1b45-169">-WhatIf</span></span>
<span data-ttu-id="b1b45-170">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b1b45-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b1b45-171">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b1b45-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1b45-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1b45-172">CommonParameters</span></span>
<span data-ttu-id="b1b45-173">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1b45-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1b45-174">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b1b45-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1b45-175">INPUT</span><span class="sxs-lookup"><span data-stu-id="b1b45-175">INPUTS</span></span>

### <span data-ttu-id="b1b45-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="b1b45-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="b1b45-177">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b1b45-177">OUTPUTS</span></span>

### <span data-ttu-id="b1b45-178">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="b1b45-178">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b1b45-179">NOTE</span><span class="sxs-lookup"><span data-stu-id="b1b45-179">NOTES</span></span>

## <span data-ttu-id="b1b45-180">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b1b45-180">RELATED LINKS</span></span>
