---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: e6145ee1773a0ecee3ebb1f8c9b5b9e2386cf229
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507356"
---
# <span data-ttu-id="5cd04-101">New-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="5cd04-101">New-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="5cd04-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5cd04-102">SYNOPSIS</span></span>
<span data-ttu-id="5cd04-103">Crea un criterio di replica del ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="5cd04-103">Creates an Azure Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5cd04-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5cd04-104">SYNTAX</span></span>

### <span data-ttu-id="5cd04-105">HyperVToAzure (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5cd04-105">HyperVToAzure (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy [-HyperVToAzure] -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cd04-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="5cd04-106">VMwareToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy [-VMwareToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5cd04-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="5cd04-107">AzureToVMware</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy [-AzureToVMware] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5cd04-108">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="5cd04-108">AzureToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy [-AzureToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cd04-109">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="5cd04-109">EnterpriseToEnterprise</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy [-VmmToVmm] -Name <String> -ReplicationProvider <String>
 [-ReplicationMethod <String>] -ReplicationFrequencyInSeconds <String>
 [-NumberOfRecoveryPointsToRetain <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-Compression <String>] -ReplicationPort <UInt16> [-Authentication <String>]
 [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cd04-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5cd04-110">DESCRIPTION</span></span>
<span data-ttu-id="5cd04-111">Il cmdlet **New-AzureRmRecoveryServicesAsrPolicy** crea un criterio di replica del ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="5cd04-111">The **New-AzureRmRecoveryServicesAsrPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="5cd04-112">Il criterio di replica viene usato per specificare le impostazioni di replica, ad esempio la frequenza di replica e il numero di punti di ripristino.</span><span class="sxs-lookup"><span data-stu-id="5cd04-112">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="5cd04-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5cd04-113">EXAMPLES</span></span>

### <span data-ttu-id="5cd04-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5cd04-114">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrPolicy -Name "abc" -ReplicationProvider HyperVReplicaAzure -ReplicationFrequencyInSeconds 30 -NumberOfRecoveryPointsToRetain 10
```

<span data-ttu-id="5cd04-115">Avvia l'operazione di creazione dei criteri di replica usando i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="5cd04-115">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="5cd04-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="5cd04-116">Example 2</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrPolicy -Name "abc122" -ReplicationProvider HyperVReplica2012R2 -ReplicationFrequencyInSeconds 300 -ReplicationPort 211

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

<span data-ttu-id="5cd04-117">Avvia l'operazione di creazione dei criteri di replica usando i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="5cd04-117">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="5cd04-118">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="5cd04-118">Example 3</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrPolicy -Name $policyName1 -ReplicationProvider InMageAzureV2 -RecoveryPoints 40  -RPOWarningThresholdInMinutes 5 -ApplicationConsistentSnapshotFrequencyInMinutes 15
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

### <span data-ttu-id="5cd04-119">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="5cd04-119">Example 4</span></span>
```
PS C:\>  $Job = New-AzureRmRecoveryServicesAsrPolicy -Name $TestPolicy1 -AzureToAzure -RecoveryPointRetentionInHours 10  -ApplicationConsistentSnapshotFrequencyInHours 5 
PS C:\>  Get-AsrJob -name $Job.id
```

<span data-ttu-id="5cd04-120">Avvia l'operazione di creazione dei criteri di replica usando i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="5cd04-120">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="5cd04-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5cd04-121">PARAMETERS</span></span>

### <span data-ttu-id="5cd04-122">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="5cd04-122">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="5cd04-123">Specifica la frequenza (in ore) in cui creare punti di ripristino coerenti dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5cd04-123">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="5cd04-124">-Autenticazione</span><span class="sxs-lookup"><span data-stu-id="5cd04-124">-Authentication</span></span>
<span data-ttu-id="5cd04-125">Specifica il tipo di autenticazione usato.</span><span class="sxs-lookup"><span data-stu-id="5cd04-125">Specifies the type of authentication used.</span></span>
<span data-ttu-id="5cd04-126">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="5cd04-126">Valid values are:</span></span>

- <span data-ttu-id="5cd04-127">Certificato</span><span class="sxs-lookup"><span data-stu-id="5cd04-127">Certificate</span></span>
-  <span data-ttu-id="5cd04-128">Kerberos</span><span class="sxs-lookup"><span data-stu-id="5cd04-128">Kerberos</span></span>

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

### <span data-ttu-id="5cd04-129">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="5cd04-129">-AzureToAzure</span></span>
<span data-ttu-id="5cd04-130">Parametro switch che specifica che i criteri di replica da creare verranno usati per la replica delle macchine virtuali di Azure tra due aree di Azure.</span><span class="sxs-lookup"><span data-stu-id="5cd04-130">Switch parameter specifying that the replication policy being created will be used to replicated Azure virtual machines between two Azure regions.</span></span>

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

### <span data-ttu-id="5cd04-131">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="5cd04-131">-AzureToVMware</span></span>
<span data-ttu-id="5cd04-132">Parametro switch che specifica che i criteri di replica da creare verranno usati per invertire la replica non riuscita sulle macchine virtuali VMware e sui server fisici in cui è in uso Azure di nuovo in un sito VMware locale.</span><span class="sxs-lookup"><span data-stu-id="5cd04-132">Switch parameter specifying that the replication policy being created will be used to reverse replicate failed over VMware virtual machines and Physical servers running in Azure back to an on-premises VMware site.</span></span>

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

### <span data-ttu-id="5cd04-133">-Compressione</span><span class="sxs-lookup"><span data-stu-id="5cd04-133">-Compression</span></span>
<span data-ttu-id="5cd04-134">Specifica se la compressione deve essere abilitata.</span><span class="sxs-lookup"><span data-stu-id="5cd04-134">Specifies if compression should be enabled.</span></span>

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

### <span data-ttu-id="5cd04-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cd04-135">-DefaultProfile</span></span>
<span data-ttu-id="5cd04-136">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5cd04-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cd04-137">-Crittografia</span><span class="sxs-lookup"><span data-stu-id="5cd04-137">-Encryption</span></span>
<span data-ttu-id="5cd04-138">{{Fill Encryption Description}}</span><span class="sxs-lookup"><span data-stu-id="5cd04-138">{{Fill Encryption Description}}</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVToAzure
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cd04-139">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="5cd04-139">-HyperVToAzure</span></span>
<span data-ttu-id="5cd04-140">Il parametro switch per specificare i criteri deve essere usato per replicare le macchine virtuali Hyper-V in Azure</span><span class="sxs-lookup"><span data-stu-id="5cd04-140">Switch parameter to specify policy is to be used to replicate Hyper-V virtual machines to Azure</span></span>

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

### <span data-ttu-id="5cd04-141">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="5cd04-141">-MultiVmSyncStatus</span></span>
<span data-ttu-id="5cd04-142">Specifica lo stato di sincronizzazione di multiVm per il criterio.</span><span class="sxs-lookup"><span data-stu-id="5cd04-142">Specifies multiVm sync status for the policy.</span></span>

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

### <span data-ttu-id="5cd04-143">-Nome</span><span class="sxs-lookup"><span data-stu-id="5cd04-143">-Name</span></span>
<span data-ttu-id="5cd04-144">Specifica il nome del criterio di replica ASR.</span><span class="sxs-lookup"><span data-stu-id="5cd04-144">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="5cd04-145">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="5cd04-145">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="5cd04-146">Specifica i punti di ripristino dei numeri da mantenere.</span><span class="sxs-lookup"><span data-stu-id="5cd04-146">Specifies the number recovery points to retain.</span></span>

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

### <span data-ttu-id="5cd04-147">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="5cd04-147">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="5cd04-148">Specifica l'ID dell'account di archiviazione di Azure a cui eseguire la replica.</span><span class="sxs-lookup"><span data-stu-id="5cd04-148">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="5cd04-149">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="5cd04-149">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="5cd04-150">Mantenere i punti di ripristino per un periodo di tempo specifico in ore.</span><span class="sxs-lookup"><span data-stu-id="5cd04-150">Retain the recovery points for given time in hours.</span></span>

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

### <span data-ttu-id="5cd04-151">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="5cd04-151">-ReplicaDeletion</span></span>
<span data-ttu-id="5cd04-152">Specifica se la macchina virtuale della replica deve essere eliminata per disabilitare la replica da un sito gestito da VMM a un altro.</span><span class="sxs-lookup"><span data-stu-id="5cd04-152">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

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

### <span data-ttu-id="5cd04-153">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="5cd04-153">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="5cd04-154">Specifica l'intervallo di frequenza della replica in secondi.</span><span class="sxs-lookup"><span data-stu-id="5cd04-154">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="5cd04-155">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="5cd04-155">Valid values are:</span></span>

- <span data-ttu-id="5cd04-156">30</span><span class="sxs-lookup"><span data-stu-id="5cd04-156">30</span></span>
- <span data-ttu-id="5cd04-157">300</span><span class="sxs-lookup"><span data-stu-id="5cd04-157">300</span></span>
- <span data-ttu-id="5cd04-158">900</span><span class="sxs-lookup"><span data-stu-id="5cd04-158">900</span></span>

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

### <span data-ttu-id="5cd04-159">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="5cd04-159">-ReplicationMethod</span></span>
<span data-ttu-id="5cd04-160">Specifica il metodo di replica.</span><span class="sxs-lookup"><span data-stu-id="5cd04-160">Specifies the replication method.</span></span>
<span data-ttu-id="5cd04-161">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="5cd04-161">Valid values are:</span></span>

- <span data-ttu-id="5cd04-162">Online</span><span class="sxs-lookup"><span data-stu-id="5cd04-162">Online</span></span>
- <span data-ttu-id="5cd04-163">Offline</span><span class="sxs-lookup"><span data-stu-id="5cd04-163">Offline</span></span>

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

### <span data-ttu-id="5cd04-164">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="5cd04-164">-ReplicationPort</span></span>
<span data-ttu-id="5cd04-165">Specifica la porta usata per la replica.</span><span class="sxs-lookup"><span data-stu-id="5cd04-165">Specifies the port used for replication.</span></span>

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

### <span data-ttu-id="5cd04-166">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="5cd04-166">-ReplicationProvider</span></span>
<span data-ttu-id="5cd04-167">Specifica il provider di replica per il criterio.</span><span class="sxs-lookup"><span data-stu-id="5cd04-167">Specifies the replication provider for the policy.</span></span>

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

### <span data-ttu-id="5cd04-168">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="5cd04-168">-ReplicationStartTime</span></span>
<span data-ttu-id="5cd04-169">Specifica l'ora di inizio della replica.</span><span class="sxs-lookup"><span data-stu-id="5cd04-169">Specifies the replication start time.</span></span>
<span data-ttu-id="5cd04-170">Non deve essere più tardi di 24 ore dall'inizio del processo.</span><span class="sxs-lookup"><span data-stu-id="5cd04-170">It must be no later than 24-hours from the start of the job.</span></span>

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

### <span data-ttu-id="5cd04-171">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="5cd04-171">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="5cd04-172">Il valore di soglia RPO in minuti per mettere in guardia.</span><span class="sxs-lookup"><span data-stu-id="5cd04-172">The RPO threshold value in minutes to warn on.</span></span>

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

### <span data-ttu-id="5cd04-173">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="5cd04-173">-VmmToVmm</span></span>
<span data-ttu-id="5cd04-174">Il parametro switch per specificare i criteri deve essere usato per la replica tra i siti Hyper-V gestiti da un server VMM.</span><span class="sxs-lookup"><span data-stu-id="5cd04-174">Switch parameter to specify policy is to be used to replicate between Hyper-V sites managed by a VMM server.</span></span>

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

### <span data-ttu-id="5cd04-175">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="5cd04-175">-VMwareToAzure</span></span>
<span data-ttu-id="5cd04-176">Parametro switch che specifica che i criteri di replica da creare verranno usati per replicare le macchine virtuali VMware e/o i server fisici in Azure.</span><span class="sxs-lookup"><span data-stu-id="5cd04-176">Switch parameter specifying that the replication policy being created will be used to replicate VMware virtual machines and/or Physical servers to Azure.</span></span>

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

### <span data-ttu-id="5cd04-177">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5cd04-177">-Confirm</span></span>
<span data-ttu-id="5cd04-178">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5cd04-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cd04-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cd04-179">-WhatIf</span></span>
<span data-ttu-id="5cd04-180">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5cd04-180">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5cd04-181">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5cd04-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cd04-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cd04-182">CommonParameters</span></span>
<span data-ttu-id="5cd04-183">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cd04-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cd04-184">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cd04-184">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cd04-185">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5cd04-185">INPUTS</span></span>

### <span data-ttu-id="5cd04-186">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5cd04-186">None</span></span>

## <span data-ttu-id="5cd04-187">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5cd04-187">OUTPUTS</span></span>

### <span data-ttu-id="5cd04-188">System. Object</span><span class="sxs-lookup"><span data-stu-id="5cd04-188">System.Object</span></span>

## <span data-ttu-id="5cd04-189">Note</span><span class="sxs-lookup"><span data-stu-id="5cd04-189">NOTES</span></span>

## <span data-ttu-id="5cd04-190">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5cd04-190">RELATED LINKS</span></span>

[<span data-ttu-id="5cd04-191">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="5cd04-191">Get-AzureRmRecoveryServicesAsrPolicy</span></span>](./Get-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="5cd04-192">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="5cd04-192">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>](./Remove-AzureRmRecoveryServicesAsrPolicy.md)
