---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 31b43930737627a3013f60a82c2ec30626b8518c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018766"
---
# <span data-ttu-id="45f81-101">Update-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="45f81-101">Update-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="45f81-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="45f81-102">SYNOPSIS</span></span>
<span data-ttu-id="45f81-103">Aggiorna un criterio di replica del ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="45f81-103">Updates an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="45f81-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="45f81-104">SYNTAX</span></span>

### <span data-ttu-id="45f81-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="45f81-105">Default (Default)</span></span>
```
Update-AzRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-RecoveryAzureStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="45f81-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="45f81-106">VMwareToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-VMwareToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45f81-107">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="45f81-107">AzureToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-AzureToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="45f81-108">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="45f81-108">AzureToVMware</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-AzureToVMware] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45f81-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="45f81-109">HyperVToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-HyperVToAzure] -InputObject <ASRPolicy>
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="45f81-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="45f81-110">EnterpriseToEnterprise</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-VmmToVmm] -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45f81-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="45f81-111">DESCRIPTION</span></span>
<span data-ttu-id="45f81-112">Il cmdlet **Update-AzRecoveryServicesAsrPolicy** aggiorna i criteri di replica del ripristino del sito di Azure specificati.</span><span class="sxs-lookup"><span data-stu-id="45f81-112">The **Update-AzRecoveryServicesAsrPolicy** cmdlet updates the specified Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="45f81-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="45f81-113">EXAMPLES</span></span>

### <span data-ttu-id="45f81-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="45f81-114">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrPolicy -Policy $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="45f81-115">Avvia l'operazione di aggiornamento dei criteri di replica usando i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="45f81-115">Starts the update replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="45f81-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="45f81-116">Example 2</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="45f81-117">Avvia l'operazione di aggiornamento dei criteri di replica di Azure ad Azure usando i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="45f81-117">Starts the update azure to azure replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="45f81-118">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="45f81-118">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -RecoveryPointRetentionInHours 20
```

<span data-ttu-id="45f81-119">Avvia il criterio di replica di Update Azure to Azure usando i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="45f81-119">Starts the update azure to azure replication policy using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="45f81-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="45f81-120">PARAMETERS</span></span>

### <span data-ttu-id="45f81-121">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="45f81-121">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="45f81-122">Specifica la frequenza (in ore) in cui creare punti di ripristino coerenti dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="45f81-122">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="45f81-123">-Autenticazione</span><span class="sxs-lookup"><span data-stu-id="45f81-123">-Authentication</span></span>
<span data-ttu-id="45f81-124">Specifica il tipo di autenticazione usato.</span><span class="sxs-lookup"><span data-stu-id="45f81-124">Specifies the type of authentication used.</span></span>

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

### <span data-ttu-id="45f81-125">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="45f81-125">-AzureToAzure</span></span>
<span data-ttu-id="45f81-126">Specifica il ripristino di emergenza di Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="45f81-126">Specifies the Azure to Azure disaster recovery.</span></span>

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

### <span data-ttu-id="45f81-127">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="45f81-127">-AzureToVMware</span></span>
<span data-ttu-id="45f81-128">Specifica l'Azure per il ripristino di emergenza vMWare.</span><span class="sxs-lookup"><span data-stu-id="45f81-128">Specifies the Azure to vMWare disaster recovery.</span></span>

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

### <span data-ttu-id="45f81-129">-Compressione</span><span class="sxs-lookup"><span data-stu-id="45f81-129">-Compression</span></span>
<span data-ttu-id="45f81-130">Specifica se la compressione deve essere abilitata.</span><span class="sxs-lookup"><span data-stu-id="45f81-130">Specifies if compression should be enabled.</span></span>

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

### <span data-ttu-id="45f81-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45f81-131">-DefaultProfile</span></span>
<span data-ttu-id="45f81-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="45f81-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="45f81-133">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="45f81-133">-HyperVToAzure</span></span>
<span data-ttu-id="45f81-134">Parametro switch che indica che il criterio specificato viene usato per replicare le macchine virtuali Hyper-V in Azure.</span><span class="sxs-lookup"><span data-stu-id="45f81-134">Switch parameter indicating that the specified policy is used to replicate Hyper-V virtual machines to Azure.</span></span>

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

### <span data-ttu-id="45f81-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45f81-135">-InputObject</span></span>
<span data-ttu-id="45f81-136">Oggetto di input per il cmdlet: specifica l'oggetto Criteri di replica ASR che corrisponde ai criteri di replica da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="45f81-136">Input object for the cmdlet: Specifies the ASR replication policy object corresponding to the replication policy to be updated.</span></span>

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

### <span data-ttu-id="45f81-137">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="45f81-137">-MultiVmSyncStatus</span></span>
<span data-ttu-id="45f81-138">Specifica lo stato di sincronizzazione di multiVm per il criterio.</span><span class="sxs-lookup"><span data-stu-id="45f81-138">Specifies multiVm sync status for the policy.</span></span>

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

### <span data-ttu-id="45f81-139">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="45f81-139">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="45f81-140">Specifica i punti di ripristino dei numeri da mantenere.</span><span class="sxs-lookup"><span data-stu-id="45f81-140">Specifies the number recovery points to retain.</span></span>

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

### <span data-ttu-id="45f81-141">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="45f81-141">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="45f81-142">Specifica l'ID dell'account di archiviazione di Azure della destinazione di replica.</span><span class="sxs-lookup"><span data-stu-id="45f81-142">Specifies the Azure storage account ID of the replication target.</span></span> <span data-ttu-id="45f81-143">Usato come account di archiviazione di destinazione per la replica se non viene fornita un'alternativa durante l'abilitazione della replica tramite il cmdlet New-AzRecoveryServicesASRReplicationProtectedItem.</span><span class="sxs-lookup"><span data-stu-id="45f81-143">Used as the target storage account for replication if an alternate is not provided while enabling replication using the New-AzRecoveryServicesASRReplicationProtectedItem cmdlet.</span></span>


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

### <span data-ttu-id="45f81-144">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="45f81-144">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="45f81-145">Ora in ore per mantenere i punti di ripristino dopo la creazione.</span><span class="sxs-lookup"><span data-stu-id="45f81-145">Time in hours to retain recovery points after creation.</span></span>

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

### <span data-ttu-id="45f81-146">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="45f81-146">-ReplicaDeletion</span></span>
<span data-ttu-id="45f81-147">Specifica se la macchina virtuale della replica deve essere eliminata per disabilitare la replica da un sito gestito da VMM a un altro.</span><span class="sxs-lookup"><span data-stu-id="45f81-147">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

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

### <span data-ttu-id="45f81-148">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="45f81-148">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="45f81-149">Specifica l'intervallo di frequenza della replica in secondi.</span><span class="sxs-lookup"><span data-stu-id="45f81-149">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="45f81-150">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="45f81-150">Valid values are:</span></span>

- <span data-ttu-id="45f81-151">30</span><span class="sxs-lookup"><span data-stu-id="45f81-151">30</span></span>
- <span data-ttu-id="45f81-152">300</span><span class="sxs-lookup"><span data-stu-id="45f81-152">300</span></span>
- <span data-ttu-id="45f81-153">900</span><span class="sxs-lookup"><span data-stu-id="45f81-153">900</span></span>

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

### <span data-ttu-id="45f81-154">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="45f81-154">-ReplicationMethod</span></span>
<span data-ttu-id="45f81-155">Specifica il metodo di replica.</span><span class="sxs-lookup"><span data-stu-id="45f81-155">Specifies the replication method.</span></span>

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

### <span data-ttu-id="45f81-156">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="45f81-156">-ReplicationPort</span></span>
<span data-ttu-id="45f81-157">Specifica la porta usata per la replica.</span><span class="sxs-lookup"><span data-stu-id="45f81-157">Specifies the port used for replication.</span></span>

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

### <span data-ttu-id="45f81-158">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="45f81-158">-ReplicationStartTime</span></span>
<span data-ttu-id="45f81-159">Specifica l'ora di inizio della replica.</span><span class="sxs-lookup"><span data-stu-id="45f81-159">Specifies the replication start time.</span></span>
<span data-ttu-id="45f81-160">Non deve essere più tardi di 24 ore dall'inizio del processo.</span><span class="sxs-lookup"><span data-stu-id="45f81-160">It must be no later than 24-hours from the start of the job.</span></span>

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

### <span data-ttu-id="45f81-161">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="45f81-161">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="45f81-162">Il valore di soglia RPO in minuti per mettere in guardia.</span><span class="sxs-lookup"><span data-stu-id="45f81-162">The RPO threshold value in minutes to warn on.</span></span>

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

### <span data-ttu-id="45f81-163">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="45f81-163">-VmmToVmm</span></span>
<span data-ttu-id="45f81-164">Parametro switch che indica che il criterio specificato viene usato per replicare le macchine virtuali Hyper-V gestite da VMM tra due siti Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="45f81-164">Switch parameter indicating that the specified policy is used to replicate VMM managed Hyper-V virtual machines between two Hyper-V sites.</span></span>

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

### <span data-ttu-id="45f81-165">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="45f81-165">-VMwareToAzure</span></span>
<span data-ttu-id="45f81-166">Parametro switch che indica che il criterio specificato viene usato per replicare le macchine virtuali VMware in Azure.</span><span class="sxs-lookup"><span data-stu-id="45f81-166">Switch parameter indicating that the specified policy is used to replicate VMware virtual machines to Azure.</span></span>

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

### <span data-ttu-id="45f81-167">-Confermare</span><span class="sxs-lookup"><span data-stu-id="45f81-167">-Confirm</span></span>
<span data-ttu-id="45f81-168">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45f81-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45f81-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45f81-169">-WhatIf</span></span>
<span data-ttu-id="45f81-170">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="45f81-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45f81-171">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="45f81-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45f81-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45f81-172">CommonParameters</span></span>
<span data-ttu-id="45f81-173">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45f81-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45f81-174">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45f81-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45f81-175">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="45f81-175">INPUTS</span></span>

### <span data-ttu-id="45f81-176">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="45f81-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="45f81-177">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="45f81-177">OUTPUTS</span></span>

### <span data-ttu-id="45f81-178">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="45f81-178">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="45f81-179">Note</span><span class="sxs-lookup"><span data-stu-id="45f81-179">NOTES</span></span>

## <span data-ttu-id="45f81-180">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="45f81-180">RELATED LINKS</span></span>
