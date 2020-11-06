---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 691c1d822df332bb9a3e89b218ed2c7ba1166f38
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509692"
---
# <span data-ttu-id="b6cb5-101">New-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="b6cb5-101">New-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="b6cb5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b6cb5-102">SYNOPSIS</span></span>
<span data-ttu-id="b6cb5-103">Crea un criterio di replica del ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="b6cb5-103">Creates an Azure Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6cb5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b6cb5-104">SYNTAX</span></span>

### <span data-ttu-id="b6cb5-105">HyperVToAzure (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b6cb5-105">HyperVToAzure (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy [-HyperVToAzure] -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6cb5-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="b6cb5-106">VMwareToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy [-VMwareToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b6cb5-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="b6cb5-107">AzureToVMware</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy [-AzureToVMware] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b6cb5-108">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="b6cb5-108">AzureToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy [-AzureToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6cb5-109">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="b6cb5-109">EnterpriseToEnterprise</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy [-VmmToVmm] -Name <String> -ReplicationProvider <String>
 [-ReplicationMethod <String>] -ReplicationFrequencyInSeconds <String>
 [-NumberOfRecoveryPointsToRetain <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-Compression <String>] -ReplicationPort <UInt16> [-Authentication <String>]
 [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6cb5-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b6cb5-110">DESCRIPTION</span></span>
<span data-ttu-id="b6cb5-111">Il cmdlet **New-AzureRmRecoveryServicesAsrPolicy** crea un criterio di replica del ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="b6cb5-111">The **New-AzureRmRecoveryServicesAsrPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="b6cb5-112">Il criterio di replica viene usato per specificare le impostazioni di replica, ad esempio la frequenza di replica e il numero di punti di ripristino.</span><span class="sxs-lookup"><span data-stu-id="b6cb5-112">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="b6cb5-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b6cb5-113">EXAMPLES</span></span>

### <span data-ttu-id="b6cb5-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b6cb5-114">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrPolicy -Name "abc" -ReplicationProvider HyperVReplicaAzure -ReplicationFrequencyInSeconds 30 -NumberOfRecoveryPointsToRetain 10
```

<span data-ttu-id="b6cb5-115">Avvia l'operazione di creazione dei criteri di replica usando i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="b6cb5-115">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="b6cb5-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b6cb5-116">Example 2</span></span>
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

<span data-ttu-id="b6cb5-117">Avvia l'operazione di creazione dei criteri di replica usando i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="b6cb5-117">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="b6cb5-118">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="b6cb5-118">Example 3</span></span>
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

### <span data-ttu-id="b6cb5-119">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="b6cb5-119">Example 4</span></span>
```
PS C:\>  $Job = New-AzureRmRecoveryServicesAsrPolicy -Name $TestPolicy1 -AzureToAzure -RecoveryPointRetentionInHours 10  -ApplicationConsistentSnapshotFrequencyInHours 5 
PS C:\>  Get-AsrJob -name $Job.id
```

<span data-ttu-id="b6cb5-120">Avvia l'operazione di creazione dei criteri di replica usando i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="b6cb5-120">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="b6cb5-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b6cb5-121">PARAMETERS</span></span>

### <span data-ttu-id="b6cb5-122">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="b6cb5-122">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="b6cb5-123">Specifica la frequenza (in ore) in cui creare punti di ripristino coerenti dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b6cb5-123">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6cb5-124">-Autenticazione</span><span class="sxs-lookup"><span data-stu-id="b6cb5-124">-Authentication</span></span>
<span data-ttu-id="b6cb5-125">Specifica il tipo di autenticazione usato.</span><span class="sxs-lookup"><span data-stu-id="b6cb5-125">Specifies the type of authentication used.</span></span>
<span data-ttu-id="b6cb5-126">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="b6cb5-126">Valid values are:</span></span>

- <span data-ttu-id="b6cb5-127">Certificato</span><span class="sxs-lookup"><span data-stu-id="b6cb5-127">Certificate</span></span>
-  <span data-ttu-id="b6cb5-128">Kerberos</span><span class="sxs-lookup"><span data-stu-id="b6cb5-128">Kerberos</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6cb5-129">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="b6cb5-129">-AzureToAzure</span></span>
<span data-ttu-id="b6cb5-130">Parametro switch che specifica che i criteri di replica da creare verranno usati per la replica delle macchine virtuali di Azure tra due aree di Azure.</span><span class="sxs-lookup"><span data-stu-id="b6cb5-130">Switch parameter specifying that the replication policy being created will be used to replicated Azure virtual machines between two Azure regions.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6cb5-131">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="b6cb5-131">-AzureToVMware</span></span>
<span data-ttu-id="b6cb5-132">Parametro switch che specifica che i criteri di replica da creare verranno usati per invertire la replica non riuscita sulle macchine virtuali VMware e sui server fisici in cui è in uso Azure di nuovo in un sito VMware locale.</span><span class="sxs-lookup"><span data-stu-id="b6cb5-132">Switch parameter specifying that the replication policy being created will be used to reverse replicate failed over VMware virtual machines and Physical servers running in Azure back to an on-premises VMware site.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6cb5-133">-Compressione</span><span class="sxs-lookup"><span data-stu-id="b6cb5-133">-Compression</span></span>
<span data-ttu-id="b6cb5-134">Specifica se la compressione deve essere abilitata.</span><span class="sxs-lookup"><span data-stu-id="b6cb5-134">Specifies if compression should be enabled.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6cb5-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b6cb5-135">-Confirm</span></span>
<span data-ttu-id="b6cb5-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6cb5-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6cb5-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6cb5-137">-DefaultProfile</span></span>
<span data-ttu-id="b6cb5-138">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b6cb5-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="b6cb5-139">-Crittografia</span><span class="sxs-lookup"><span data-stu-id="b6cb5-139">-Encryption</span></span>
<span data-ttu-id="b6cb5-140">Specifica se la crittografia deve essere abilitata o disabilitata.</span><span class="sxs-lookup"><span data-stu-id="b6cb5-140">Specifies if encryption should be enabled or disabled.</span></span>

```yaml
Type: String
Parameter Sets: HyperVToAzure
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6cb5-141">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="b6cb5-141">-HyperVToAzure</span></span>
<span data-ttu-id="b6cb5-142">Il parametro switch per specificare i criteri deve essere usato per replicare le macchine virtuali Hyper-V in Azure</span><span class="sxs-lookup"><span data-stu-id="b6cb5-142">Switch parameter to specify policy is to be used to replicate Hyper-V virtual machines to Azure</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: HyperVToAzure
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6cb5-143">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="b6cb5-143">-MultiVmSyncStatus</span></span>
<span data-ttu-id="b6cb5-144">Specifica lo stato di sincronizzazione di multiVm per il criterio.</span><span class="sxs-lookup"><span data-stu-id="b6cb5-144">Specifies multiVm sync status for the policy.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, AzureToVMware, AzureToAzure
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6cb5-145">-Nome</span><span class="sxs-lookup"><span data-stu-id="b6cb5-145">-Name</span></span>
<span data-ttu-id="b6cb5-146">Specifica il nome del criterio di replica ASR.</span><span class="sxs-lookup"><span data-stu-id="b6cb5-146">Specifies the name of the ASR replication policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6cb5-147">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="b6cb5-147">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="b6cb5-148">Specifica i punti di ripristino dei numeri da mantenere.</span><span class="sxs-lookup"><span data-stu-id="b6cb5-148">Specifies the number recovery points to retain.</span></span>

```yaml
Type: Int32
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases: RecoveryPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6cb5-149">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="b6cb5-149">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="b6cb5-150">Il valore di soglia RPO in minuti per mettere in guardia.</span><span class="sxs-lookup"><span data-stu-id="b6cb5-150">The RPO threshold value in minutes to warn on.</span></span>

```yaml
Type: Int32
Parameter Sets: VMwareToAzure, AzureToVMware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6cb5-151">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="b6cb5-151">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="b6cb5-152">Specifica l'ID dell'account di archiviazione di Azure a cui eseguire la replica.</span><span class="sxs-lookup"><span data-stu-id="b6cb5-152">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: String
Parameter Sets: HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6cb5-153">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="b6cb5-153">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="b6cb5-154">Mantenere i punti di ripristino per un periodo di tempo specifico in ore.</span><span class="sxs-lookup"><span data-stu-id="b6cb5-154">Retain the recovery points for given time in hours.</span></span>

```yaml
Type: Int32
Parameter Sets: VMwareToAzure, AzureToVMware, AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6cb5-155">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="b6cb5-155">-ReplicaDeletion</span></span>
<span data-ttu-id="b6cb5-156">Specifica se la macchina virtuale della replica deve essere eliminata per disabilitare la replica da un sito gestito da VMM a un altro.</span><span class="sxs-lookup"><span data-stu-id="b6cb5-156">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6cb5-157">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="b6cb5-157">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="b6cb5-158">Specifica l'intervallo di frequenza della replica in secondi.</span><span class="sxs-lookup"><span data-stu-id="b6cb5-158">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="b6cb5-159">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="b6cb5-159">Valid values are:</span></span>

- <span data-ttu-id="b6cb5-160">30</span><span class="sxs-lookup"><span data-stu-id="b6cb5-160">30</span></span>
- <span data-ttu-id="b6cb5-161">300</span><span class="sxs-lookup"><span data-stu-id="b6cb5-161">300</span></span>
- <span data-ttu-id="b6cb5-162">900</span><span class="sxs-lookup"><span data-stu-id="b6cb5-162">900</span></span>

```yaml
Type: String
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases:
Accepted values: 30, 300, 900

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6cb5-163">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="b6cb5-163">-ReplicationMethod</span></span>
<span data-ttu-id="b6cb5-164">Specifica il metodo di replica.</span><span class="sxs-lookup"><span data-stu-id="b6cb5-164">Specifies the replication method.</span></span>
<span data-ttu-id="b6cb5-165">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="b6cb5-165">Valid values are:</span></span>

- <span data-ttu-id="b6cb5-166">Online</span><span class="sxs-lookup"><span data-stu-id="b6cb5-166">Online</span></span>
- <span data-ttu-id="b6cb5-167">Offline</span><span class="sxs-lookup"><span data-stu-id="b6cb5-167">Offline</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6cb5-168">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="b6cb5-168">-ReplicationPort</span></span>
<span data-ttu-id="b6cb5-169">Specifica la porta usata per la replica.</span><span class="sxs-lookup"><span data-stu-id="b6cb5-169">Specifies the port used for replication.</span></span>

```yaml
Type: UInt16
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6cb5-170">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="b6cb5-170">-ReplicationProvider</span></span>
<span data-ttu-id="b6cb5-171">Specifica il provider di replica per il criterio.</span><span class="sxs-lookup"><span data-stu-id="b6cb5-171">Specifies the replication provider for the policy.</span></span>

```yaml
Type: String
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases:
Accepted values: HyperVReplica2012R2, HyperVReplica2012, HyperVReplicaAzure

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6cb5-172">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="b6cb5-172">-ReplicationStartTime</span></span>
<span data-ttu-id="b6cb5-173">Specifica l'ora di inizio della replica.</span><span class="sxs-lookup"><span data-stu-id="b6cb5-173">Specifies the replication start time.</span></span>
<span data-ttu-id="b6cb5-174">Non deve essere più tardi di 24 ore dall'inizio del processo.</span><span class="sxs-lookup"><span data-stu-id="b6cb5-174">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6cb5-175">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="b6cb5-175">-VMwareToAzure</span></span>
<span data-ttu-id="b6cb5-176">Parametro switch che specifica che i criteri di replica da creare verranno usati per replicare le macchine virtuali VMware e/o i server fisici in Azure.</span><span class="sxs-lookup"><span data-stu-id="b6cb5-176">Switch parameter specifying that the replication policy being created will be used to replicate VMware virtual machines and/or Physical servers to Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6cb5-177">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="b6cb5-177">-VmmToVmm</span></span>
<span data-ttu-id="b6cb5-178">Il parametro switch per specificare i criteri deve essere usato per la replica tra i siti Hyper-V gestiti da un server VMM.</span><span class="sxs-lookup"><span data-stu-id="b6cb5-178">Switch parameter to specify policy is to be used to replicate between Hyper-V sites managed by a VMM server.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6cb5-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6cb5-179">-WhatIf</span></span>
<span data-ttu-id="b6cb5-180">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b6cb5-180">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b6cb5-181">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b6cb5-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6cb5-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6cb5-182">CommonParameters</span></span>
<span data-ttu-id="b6cb5-183">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6cb5-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6cb5-184">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6cb5-184">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6cb5-185">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b6cb5-185">INPUTS</span></span>

### <span data-ttu-id="b6cb5-186">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b6cb5-186">None</span></span>

## <span data-ttu-id="b6cb5-187">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b6cb5-187">OUTPUTS</span></span>

### <span data-ttu-id="b6cb5-188">System. Object</span><span class="sxs-lookup"><span data-stu-id="b6cb5-188">System.Object</span></span>

## <span data-ttu-id="b6cb5-189">Note</span><span class="sxs-lookup"><span data-stu-id="b6cb5-189">NOTES</span></span>

## <span data-ttu-id="b6cb5-190">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b6cb5-190">RELATED LINKS</span></span>

[<span data-ttu-id="b6cb5-191">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="b6cb5-191">Get-AzureRmRecoveryServicesAsrPolicy</span></span>](./Get-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="b6cb5-192">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="b6cb5-192">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>](./Remove-AzureRmRecoveryServicesAsrPolicy.md)
