---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: d120054a7eef5afd27101d84911a1a57a0b4819a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367233"
---
# <span data-ttu-id="adcc1-101">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="adcc1-101">New-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="adcc1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="adcc1-102">SYNOPSIS</span></span>
<span data-ttu-id="adcc1-103">Crea un criterio di replica del ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="adcc1-103">Creates an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="adcc1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="adcc1-104">SYNTAX</span></span>

### <span data-ttu-id="adcc1-105">HyperVToAzure (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="adcc1-105">HyperVToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrPolicy [-HyperVToAzure] -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="adcc1-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="adcc1-106">VMwareToAzure</span></span>
```
New-AzRecoveryServicesAsrPolicy [-VMwareToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="adcc1-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="adcc1-107">AzureToVMware</span></span>
```
New-AzRecoveryServicesAsrPolicy [-AzureToVMware] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="adcc1-108">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="adcc1-108">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrPolicy [-AzureToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adcc1-109">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="adcc1-109">EnterpriseToEnterprise</span></span>
```
New-AzRecoveryServicesAsrPolicy [-VmmToVmm] -Name <String> -ReplicationProvider <String>
 [-ReplicationMethod <String>] -ReplicationFrequencyInSeconds <String>
 [-NumberOfRecoveryPointsToRetain <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-Compression <String>] -ReplicationPort <UInt16> [-Authentication <String>]
 [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="adcc1-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="adcc1-110">DESCRIPTION</span></span>
<span data-ttu-id="adcc1-111">Il cmdlet **New-AzRecoveryServicesAsrPolicy** crea un criterio di replica del ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="adcc1-111">The **New-AzRecoveryServicesAsrPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="adcc1-112">Il criterio di replica viene usato per specificare le impostazioni di replica, ad esempio la frequenza di replica e il numero di punti di ripristino.</span><span class="sxs-lookup"><span data-stu-id="adcc1-112">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="adcc1-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="adcc1-113">EXAMPLES</span></span>

### <span data-ttu-id="adcc1-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="adcc1-114">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrPolicy -Name "abc" -ReplicationProvider HyperVReplicaAzure -ReplicationFrequencyInSeconds 30 -NumberOfRecoveryPointsToRetain 10
```

<span data-ttu-id="adcc1-115">Avvia l'operazione di creazione dei criteri di replica usando i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="adcc1-115">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="adcc1-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="adcc1-116">Example 2</span></span>
```
PS C:\> New-AzRecoveryServicesAsrPolicy -Name "abc122" -ReplicationProvider HyperVReplica2012R2 -ReplicationFrequencyInSeconds 300 -ReplicationPort 211

Name             : 1c609a5b-324e-461c-866f-ad58f944df25
ID               : /Subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationJobs/1c609a5b-324e-461c-866f-ad58f944df25
Type             :
JobType          : AddProtectionProfile
DisplayName      : Create replication policy
ClientRequestId  : b10c83ee-fee2-42d4-ad1d-dfc3e166faab ActivityId: 67e8453c-fae0-465f-801c-dfa2e6e6ee23
State            : Succeeded
StateDescription : Completed
StartTime        : 8/29/2017 10:18:10 AM
EndTime          : 8/29/2017 10:18:11 AM
TargetObjectId   : bb8e8c57-221d-5668-9d82-b15a3e19a6a3
TargetObjectType : ProtectionProfile
TargetObjectName : abc122
AllowedActions   :
Tasks            : {Prerequisites check for creating the replication policy, Creating the replication policy}
Errors           : {}
```

<span data-ttu-id="adcc1-117">Avvia l'operazione di creazione dei criteri di replica usando i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="adcc1-117">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="adcc1-118">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="adcc1-118">Example 3</span></span>
```
PS C:\> New-AzRecoveryServicesAsrPolicy -Name $policyName1 -ReplicationProvider InMageAzureV2 -RecoveryPoints 40  -RPOWarningThresholdInMinutes 5 -ApplicationConsistentSnapshotFrequencyInMinutes 15
Name             : ed69e451-878b-4f19-9c0f-73184be05eaf
ID               : /Subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationJobs/ed69e451-878b-4f19-9c0f-73184be05eaf
Type             :
JobType          :
DisplayName      :
ClientRequestId  : d8922fa2-303c-4eb4-b556-e07969ea6fba ActivityId: 9e946cdf-2351-44c2-9aef-70ef2eab29b4
State            : NotStarted
StateDescription : NotStarted
StartTime        :
EndTime          :
TargetObjectId   :
TargetObjectType :
TargetObjectName :
AllowedActions   :
Tasks            : {}
Errors           : {}
```

### <span data-ttu-id="adcc1-119">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="adcc1-119">Example 4</span></span>
```
PS C:\>  $Job = New-AzRecoveryServicesAsrPolicy -Name $TestPolicy1 -AzureToAzure -RecoveryPointRetentionInHours 10  -ApplicationConsistentSnapshotFrequencyInHours 5 
PS C:\>  Get-AsrJob -name $Job.id
```

<span data-ttu-id="adcc1-120">Avvia l'operazione di creazione dei criteri di replica usando i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="adcc1-120">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="adcc1-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="adcc1-121">PARAMETERS</span></span>

### <span data-ttu-id="adcc1-122">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="adcc1-122">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="adcc1-123">Specifica la frequenza (in ore) in cui creare punti di ripristino coerenti dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="adcc1-123">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="adcc1-124">-Autenticazione</span><span class="sxs-lookup"><span data-stu-id="adcc1-124">-Authentication</span></span>
<span data-ttu-id="adcc1-125">Specifica il tipo di autenticazione usato.</span><span class="sxs-lookup"><span data-stu-id="adcc1-125">Specifies the type of authentication used.</span></span>
<span data-ttu-id="adcc1-126">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="adcc1-126">Valid values are:</span></span>

- <span data-ttu-id="adcc1-127">Certificato</span><span class="sxs-lookup"><span data-stu-id="adcc1-127">Certificate</span></span>
-  <span data-ttu-id="adcc1-128">Kerberos</span><span class="sxs-lookup"><span data-stu-id="adcc1-128">Kerberos</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adcc1-129">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="adcc1-129">-AzureToAzure</span></span>
<span data-ttu-id="adcc1-130">Parametro switch specifica lo scenario per la creazione di criteri di Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="adcc1-130">Switch parameter specifies the scenario for azure to azure policy creation.</span></span>

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

### <span data-ttu-id="adcc1-131">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="adcc1-131">-AzureToVMware</span></span>
<span data-ttu-id="adcc1-132">Parametro switch specifica lo scenario per la creazione di criteri di Azure per vMWare.</span><span class="sxs-lookup"><span data-stu-id="adcc1-132">Switch parameter specifies the scenario for azure to vMWare policy creation.</span></span>

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

### <span data-ttu-id="adcc1-133">-Compressione</span><span class="sxs-lookup"><span data-stu-id="adcc1-133">-Compression</span></span>
<span data-ttu-id="adcc1-134">Specifica se la compressione deve essere abilitata.</span><span class="sxs-lookup"><span data-stu-id="adcc1-134">Specifies if compression should be enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adcc1-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adcc1-135">-DefaultProfile</span></span>
<span data-ttu-id="adcc1-136">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="adcc1-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="adcc1-137">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="adcc1-137">-HyperVToAzure</span></span>
<span data-ttu-id="adcc1-138">Il parametro switch per specificare i criteri deve essere usato per replicare le macchine virtuali Hyper-V in Azure</span><span class="sxs-lookup"><span data-stu-id="adcc1-138">Switch parameter to specify policy is to be used to replicate Hyper-V virtual machines to Azure</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HyperVToAzure
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adcc1-139">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="adcc1-139">-MultiVmSyncStatus</span></span>
<span data-ttu-id="adcc1-140">Specifica lo stato di sincronizzazione di multiVm per il criterio.</span><span class="sxs-lookup"><span data-stu-id="adcc1-140">Specifies multiVm sync status for the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, AzureToVMware, AzureToAzure
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adcc1-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="adcc1-141">-Name</span></span>
<span data-ttu-id="adcc1-142">Specifica il nome del criterio di replica ASR.</span><span class="sxs-lookup"><span data-stu-id="adcc1-142">Specifies the name of the ASR replication policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adcc1-143">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="adcc1-143">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="adcc1-144">Specifica i punti di ripristino dei numeri da mantenere.</span><span class="sxs-lookup"><span data-stu-id="adcc1-144">Specifies the number recovery points to retain.</span></span>

```yaml
Type: System.Int32
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases: RecoveryPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adcc1-145">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="adcc1-145">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="adcc1-146">Specifica l'ID dell'account di archiviazione di Azure a cui eseguire la replica.</span><span class="sxs-lookup"><span data-stu-id="adcc1-146">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adcc1-147">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="adcc1-147">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="adcc1-148">Mantenere i punti di ripristino per un periodo di tempo specifico in ore.</span><span class="sxs-lookup"><span data-stu-id="adcc1-148">Retain the recovery points for given time in hours.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VMwareToAzure, AzureToVMware, AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adcc1-149">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="adcc1-149">-ReplicaDeletion</span></span>
<span data-ttu-id="adcc1-150">Specifica se la macchina virtuale della replica deve essere eliminata per disabilitare la replica da un sito gestito da VMM a un altro.</span><span class="sxs-lookup"><span data-stu-id="adcc1-150">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adcc1-151">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="adcc1-151">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="adcc1-152">Specifica l'intervallo di frequenza della replica in secondi.</span><span class="sxs-lookup"><span data-stu-id="adcc1-152">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="adcc1-153">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="adcc1-153">Valid values are:</span></span>

- <span data-ttu-id="adcc1-154">30</span><span class="sxs-lookup"><span data-stu-id="adcc1-154">30</span></span>
- <span data-ttu-id="adcc1-155">300</span><span class="sxs-lookup"><span data-stu-id="adcc1-155">300</span></span>
- <span data-ttu-id="adcc1-156">900</span><span class="sxs-lookup"><span data-stu-id="adcc1-156">900</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases:
Accepted values: 30, 300, 900

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adcc1-157">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="adcc1-157">-ReplicationMethod</span></span>
<span data-ttu-id="adcc1-158">Specifica il metodo di replica.</span><span class="sxs-lookup"><span data-stu-id="adcc1-158">Specifies the replication method.</span></span>
<span data-ttu-id="adcc1-159">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="adcc1-159">Valid values are:</span></span>

- <span data-ttu-id="adcc1-160">Online</span><span class="sxs-lookup"><span data-stu-id="adcc1-160">Online</span></span>
- <span data-ttu-id="adcc1-161">Offline</span><span class="sxs-lookup"><span data-stu-id="adcc1-161">Offline</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adcc1-162">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="adcc1-162">-ReplicationPort</span></span>
<span data-ttu-id="adcc1-163">Specifica la porta usata per la replica.</span><span class="sxs-lookup"><span data-stu-id="adcc1-163">Specifies the port used for replication.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adcc1-164">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="adcc1-164">-ReplicationProvider</span></span>
<span data-ttu-id="adcc1-165">Specifica il provider di replica per il criterio.</span><span class="sxs-lookup"><span data-stu-id="adcc1-165">Specifies the replication provider for the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases:
Accepted values: HyperVReplica2012R2, HyperVReplica2012, HyperVReplicaAzure

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adcc1-166">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="adcc1-166">-ReplicationStartTime</span></span>
<span data-ttu-id="adcc1-167">Specifica l'ora di inizio della replica.</span><span class="sxs-lookup"><span data-stu-id="adcc1-167">Specifies the replication start time.</span></span>
<span data-ttu-id="adcc1-168">Non deve essere più tardi di 24 ore dall'inizio del processo.</span><span class="sxs-lookup"><span data-stu-id="adcc1-168">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adcc1-169">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="adcc1-169">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="adcc1-170">Il valore di soglia RPO in minuti per mettere in guardia.</span><span class="sxs-lookup"><span data-stu-id="adcc1-170">The RPO threshold value in minutes to warn on.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VMwareToAzure, AzureToVMware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adcc1-171">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="adcc1-171">-VmmToVmm</span></span>
<span data-ttu-id="adcc1-172">Il parametro switch per specificare i criteri deve essere usato per la replica tra i siti Hyper-V gestiti da un server VMM.</span><span class="sxs-lookup"><span data-stu-id="adcc1-172">Switch parameter to specify policy is to be used to replicate between Hyper-V sites managed by a VMM server.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adcc1-173">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="adcc1-173">-VMwareToAzure</span></span>
<span data-ttu-id="adcc1-174">Parametro switch che specifica che i criteri di replica da creare verranno usati per replicare le macchine virtuali VMware e/o i server fisici in Azure.</span><span class="sxs-lookup"><span data-stu-id="adcc1-174">Switch parameter specifying that the replication policy being created will be used to replicate VMware virtual machines and/or Physical servers to Azure.</span></span>

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

### <span data-ttu-id="adcc1-175">-Confermare</span><span class="sxs-lookup"><span data-stu-id="adcc1-175">-Confirm</span></span>
<span data-ttu-id="adcc1-176">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="adcc1-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adcc1-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adcc1-177">-WhatIf</span></span>
<span data-ttu-id="adcc1-178">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="adcc1-178">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="adcc1-179">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="adcc1-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adcc1-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adcc1-180">CommonParameters</span></span>
<span data-ttu-id="adcc1-181">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adcc1-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adcc1-182">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="adcc1-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adcc1-183">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="adcc1-183">INPUTS</span></span>

### <span data-ttu-id="adcc1-184">Nessuno</span><span class="sxs-lookup"><span data-stu-id="adcc1-184">None</span></span>

## <span data-ttu-id="adcc1-185">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="adcc1-185">OUTPUTS</span></span>

### <span data-ttu-id="adcc1-186">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="adcc1-186">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="adcc1-187">Note</span><span class="sxs-lookup"><span data-stu-id="adcc1-187">NOTES</span></span>

## <span data-ttu-id="adcc1-188">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="adcc1-188">RELATED LINKS</span></span>

[<span data-ttu-id="adcc1-189">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="adcc1-189">Get-AzRecoveryServicesAsrPolicy</span></span>](./Get-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="adcc1-190">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="adcc1-190">Remove-AzRecoveryServicesAsrPolicy</span></span>](./Remove-AzRecoveryServicesAsrPolicy.md)
