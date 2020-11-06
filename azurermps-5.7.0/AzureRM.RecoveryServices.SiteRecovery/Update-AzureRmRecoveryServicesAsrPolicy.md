---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: bf049e18d75867f7dd9904e8d2ab2223dffdb0bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508027"
---
# <span data-ttu-id="97106-101">Update-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="97106-101">Update-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="97106-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="97106-102">SYNOPSIS</span></span>
<span data-ttu-id="97106-103">Aggiorna un criterio di replica del ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="97106-103">Updates an Azure Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97106-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="97106-104">SYNTAX</span></span>

### <span data-ttu-id="97106-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="97106-105">Default (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97106-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="97106-106">VMwareToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-VMwareToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97106-107">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="97106-107">AzureToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-AzureToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="97106-108">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="97106-108">AzureToVMware</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-AzureToVMware] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97106-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="97106-109">HyperVToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-HyperVToAzure] -InputObject <ASRPolicy>
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97106-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="97106-110">EnterpriseToEnterprise</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-VmmToVmm] -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97106-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="97106-111">DESCRIPTION</span></span>
<span data-ttu-id="97106-112">Il cmdlet **Update-AzureRmRecoveryServicesAsrPolicy** aggiorna i criteri di replica del ripristino del sito di Azure specificati.</span><span class="sxs-lookup"><span data-stu-id="97106-112">The **Update-AzureRmRecoveryServicesAsrPolicy** cmdlet updates the specified Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="97106-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="97106-113">EXAMPLES</span></span>

### <span data-ttu-id="97106-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="97106-114">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrPolicy -Policy $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="97106-115">Avvia l'operazione di aggiornamento dei criteri di replica usando i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="97106-115">Starts the update replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="97106-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="97106-116">Example 2</span></span>
```
PS C:\> Update-AzureRmRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="97106-117">Avvia l'operazione di aggiornamento dei criteri di replica di Azure ad Azure usando i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="97106-117">Starts the update azure to azure replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="97106-118">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="97106-118">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -RecoveryPointRetentionInHours 20
```

<span data-ttu-id="97106-119">Avvia il criterio di replica di Update Azure to Azure usando i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="97106-119">Starts the update azure to azure replication policy using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="97106-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="97106-120">PARAMETERS</span></span>

### <span data-ttu-id="97106-121">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="97106-121">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="97106-122">Specifica la frequenza (in ore) in cui creare punti di ripristino coerenti dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="97106-122">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="97106-123">-Autenticazione</span><span class="sxs-lookup"><span data-stu-id="97106-123">-Authentication</span></span>
<span data-ttu-id="97106-124">Specifica il tipo di autenticazione usato.</span><span class="sxs-lookup"><span data-stu-id="97106-124">Specifies the type of authentication used.</span></span>

```yaml
Type: String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97106-125">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="97106-125">-AzureToAzure</span></span>
<span data-ttu-id="97106-126">Parametro switch che specifica che i criteri di replica usati per replicare le macchine virtuali di Azure tra due aree di Azure verranno aggiornati.</span><span class="sxs-lookup"><span data-stu-id="97106-126">Switch parameter specifying that the replication policy used to replicate Azure virtual machines between two Azure regions will be updated.</span></span>

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

### <span data-ttu-id="97106-127">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="97106-127">-AzureToVMware</span></span>
<span data-ttu-id="97106-128">Parametro switch che indica che il criterio specfied viene usato per replicare il failover sulle macchine virtuali in uso in Azure di nuovo in un sito VMware locale.</span><span class="sxs-lookup"><span data-stu-id="97106-128">Switch parameter indicating that the specfied policy is used to replicate failed over virtual machines running in Azure back to an on-premises VMware site.</span></span>

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

### <span data-ttu-id="97106-129">-Compressione</span><span class="sxs-lookup"><span data-stu-id="97106-129">-Compression</span></span>
<span data-ttu-id="97106-130">Specifica se la compressione deve essere abilitata.</span><span class="sxs-lookup"><span data-stu-id="97106-130">Specifies if compression should be enabled.</span></span>

```yaml
Type: String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97106-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="97106-131">-Confirm</span></span>
<span data-ttu-id="97106-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97106-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97106-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97106-133">-DefaultProfile</span></span>
<span data-ttu-id="97106-134">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="97106-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="97106-135">-Crittografia</span><span class="sxs-lookup"><span data-stu-id="97106-135">-Encryption</span></span>
<span data-ttu-id="97106-136">Specifica se la crittografia deve essere abilitata o disabilitata.</span><span class="sxs-lookup"><span data-stu-id="97106-136">Specifies if encryption should be enabled or disabled.</span></span>

```yaml
Type: String
Parameter Sets: Default, HyperVToAzure
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97106-137">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="97106-137">-HyperVToAzure</span></span>
<span data-ttu-id="97106-138">Parametro switch che indica che il criterio specfied viene usato per replicare le macchine virtuali Hyper-V in Azure.</span><span class="sxs-lookup"><span data-stu-id="97106-138">Switch parameter indicating that the specfied policy is used to replicate Hyper-V virtual machines to Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: HyperVToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97106-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97106-139">-InputObject</span></span>
<span data-ttu-id="97106-140">Oggetto di input per il cmdlet: specifica l'oggetto Criteri di replica ASR che corrisponde ai criteri di replica da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="97106-140">Input object for the cmdlet: Specifies the ASR replication policy object corresponding to the replication policy to be updated.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97106-141">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="97106-141">-MultiVmSyncStatus</span></span>
<span data-ttu-id="97106-142">Specifica lo stato di sincronizzazione di multiVm per il criterio.</span><span class="sxs-lookup"><span data-stu-id="97106-142">Specifies multiVm sync status for the policy.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, AzureToAzure, AzureToVMware
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97106-143">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="97106-143">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="97106-144">Specifica i punti di ripristino dei numeri da mantenere.</span><span class="sxs-lookup"><span data-stu-id="97106-144">Specifies the number recovery points to retain.</span></span>

```yaml
Type: Int32
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases: RecoveryPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97106-145">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="97106-145">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="97106-146">Il valore di soglia RPO in minuti per mettere in guardia.</span><span class="sxs-lookup"><span data-stu-id="97106-146">The RPO threshold value in minutes to warn on.</span></span>

```yaml
Type: Int32
Parameter Sets: VMwareToAzure, AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97106-147">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="97106-147">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="97106-148">Specifica l'ID dell'account di archiviazione di Azure della destinazione di replica.</span><span class="sxs-lookup"><span data-stu-id="97106-148">Specifies the Azure storage account ID of the replication target.</span></span> <span data-ttu-id="97106-149">Usato come account di archiviazione di destinazione per la replica se non viene fornita un'alternativa durante l'abilitazione della replica tramite il cmdlet New-AzureRmRecoveryServicesASRReplicationProtectedItem.</span><span class="sxs-lookup"><span data-stu-id="97106-149">Used as the target storage account for replication if an alternate is not provided while enabling replication using the New-AzureRmRecoveryServicesASRReplicationProtectedItem cmdlet.</span></span>


```yaml
Type: String
Parameter Sets: Default, HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97106-150">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="97106-150">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="97106-151">Ora in ore per mantenere i punti di ripristino dopo la creazione.</span><span class="sxs-lookup"><span data-stu-id="97106-151">Time in hours to retain recovery points after creation.</span></span>

```yaml
Type: Int32
Parameter Sets: VMwareToAzure, AzureToAzure, AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97106-152">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="97106-152">-ReplicaDeletion</span></span>
<span data-ttu-id="97106-153">Specifica se la macchina virtuale della replica deve essere eliminata per disabilitare la replica da un sito gestito da VMM a un altro.</span><span class="sxs-lookup"><span data-stu-id="97106-153">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97106-154">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="97106-154">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="97106-155">Specifica l'intervallo di frequenza della replica in secondi.</span><span class="sxs-lookup"><span data-stu-id="97106-155">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="97106-156">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="97106-156">Valid values are:</span></span>

- <span data-ttu-id="97106-157">30</span><span class="sxs-lookup"><span data-stu-id="97106-157">30</span></span>
- <span data-ttu-id="97106-158">300</span><span class="sxs-lookup"><span data-stu-id="97106-158">300</span></span>
- <span data-ttu-id="97106-159">900</span><span class="sxs-lookup"><span data-stu-id="97106-159">900</span></span>

```yaml
Type: String
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases:
Accepted values: 30, 300, 900

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97106-160">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="97106-160">-ReplicationMethod</span></span>
<span data-ttu-id="97106-161">Specifica il metodo di replica.</span><span class="sxs-lookup"><span data-stu-id="97106-161">Specifies the replication method.</span></span>

```yaml
Type: String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97106-162">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="97106-162">-ReplicationPort</span></span>
<span data-ttu-id="97106-163">Specifica la porta usata per la replica.</span><span class="sxs-lookup"><span data-stu-id="97106-163">Specifies the port used for replication.</span></span>

```yaml
Type: UInt16
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97106-164">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="97106-164">-ReplicationStartTime</span></span>
<span data-ttu-id="97106-165">Specifica l'ora di inizio della replica.</span><span class="sxs-lookup"><span data-stu-id="97106-165">Specifies the replication start time.</span></span>
<span data-ttu-id="97106-166">Non deve essere più tardi di 24 ore dall'inizio del processo.</span><span class="sxs-lookup"><span data-stu-id="97106-166">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97106-167">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="97106-167">-VMwareToAzure</span></span>
<span data-ttu-id="97106-168">Parametro switch che indica che il criterio specfied viene usato per replicare le macchine virtuali VMware in Azure.</span><span class="sxs-lookup"><span data-stu-id="97106-168">Switch parameter indicating that the specfied policy is used to replicate VMware virtual machines to Azure.</span></span>

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

### <span data-ttu-id="97106-169">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="97106-169">-VmmToVmm</span></span>
<span data-ttu-id="97106-170">Parametro switch che indica che il criterio specfied viene usato per replicare le macchine virtuali Hyper-V gestite da VMM tra due siti Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="97106-170">Switch parameter indicating that the specfied policy is used to replicate VMM managed Hyper-V virtual machines between two Hyper-V sites.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97106-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97106-171">-WhatIf</span></span>
<span data-ttu-id="97106-172">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="97106-172">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="97106-173">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="97106-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97106-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97106-174">CommonParameters</span></span>
<span data-ttu-id="97106-175">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97106-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97106-176">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97106-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97106-177">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="97106-177">INPUTS</span></span>

### <span data-ttu-id="97106-178">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="97106-178">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="97106-179">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="97106-179">OUTPUTS</span></span>

### <span data-ttu-id="97106-180">System. Object</span><span class="sxs-lookup"><span data-stu-id="97106-180">System.Object</span></span>

## <span data-ttu-id="97106-181">Note</span><span class="sxs-lookup"><span data-stu-id="97106-181">NOTES</span></span>

## <span data-ttu-id="97106-182">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="97106-182">RELATED LINKS</span></span>
