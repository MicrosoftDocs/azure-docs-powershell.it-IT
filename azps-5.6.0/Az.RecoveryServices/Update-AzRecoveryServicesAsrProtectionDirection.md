---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectiondirection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: c6e25b9b8ec7fe22f76ccec954312914af8dd53e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990847"
---
# <span data-ttu-id="26d8b-101">Update-AzRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="26d8b-101">Update-AzRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="26d8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26d8b-102">SYNOPSIS</span></span>
<span data-ttu-id="26d8b-103">Aggiorna la direzione della replica per l'elemento o il piano di ripristino specificato protetto da replica.</span><span class="sxs-lookup"><span data-stu-id="26d8b-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="26d8b-104">Usato per proteggere o annullare la replica di un elemento replicato o di un piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="26d8b-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

## <span data-ttu-id="26d8b-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="26d8b-105">SYNTAX</span></span>

### <span data-ttu-id="26d8b-106">ByRPIObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="26d8b-106">ByRPIObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26d8b-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="26d8b-107">AzureToVMware</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToVMware] [-Account <ASRRunAsAccount>]
 -DataStore <ASRDataStore> [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 -RetentionVolume <ASRRetentionVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26d8b-108">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="26d8b-108">VMwareToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VMwareToAzure] -Account <ASRRunAsAccount>
 [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26d8b-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="26d8b-109">HyperVToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-HyperVToAzure] [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26d8b-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="26d8b-110">EnterpriseToEnterprise</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VmmToVmm]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26d8b-111">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="26d8b-111">AzureToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -LogStorageAccountId <String>
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryResourceGroupId <String>] [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-RecoveryBootDiagStorageAccountId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26d8b-112">AzureToAzureWithMultipleStorageAccount</span><span class="sxs-lookup"><span data-stu-id="26d8b-112">AzureToAzureWithMultipleStorageAccount</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-RecoveryResourceGroupId <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-RecoveryBootDiagStorageAccountId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26d8b-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="26d8b-113">ByRPObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26d8b-114">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="26d8b-114">ByPEObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -Direction <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26d8b-115">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="26d8b-115">DESCRIPTION</span></span>
<span data-ttu-id="26d8b-116">Il cmdlet **Update-AzRecoveryServicesAsrProtectionDirection** aggiorna la direzione della replica per l'oggetto Azure Site Recovery specificato al termine di un'operazione di failover di commit.</span><span class="sxs-lookup"><span data-stu-id="26d8b-116">The **Update-AzRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="26d8b-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="26d8b-117">EXAMPLES</span></span>

### <span data-ttu-id="26d8b-118">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="26d8b-118">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="26d8b-119">Avviare l'operazione della direzione di aggiornamento per il piano di ripristino specificato e restituisce l'oggetto processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="26d8b-119">Start the update direction operation for the specified recovery plan and returns the ASR job object used to track the operation.</span></span>

### <span data-ttu-id="26d8b-120">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="26d8b-120">Example 2</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi
```

<span data-ttu-id="26d8b-121">Avviare l'operazione della direzione di aggiornamento per l'elemento protetto da replica specificato nell'area azure di destinazione definita dal mapping del contenitore di protezione e usando l'archiviazione della cache (nella stessa area della macchina virtuale).</span><span class="sxs-lookup"><span data-stu-id="26d8b-121">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM).</span></span>

### <span data-ttu-id="26d8b-122">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="26d8b-122">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi
```

<span data-ttu-id="26d8b-123">Avviare l'operazione della direzione di aggiornamento per l'elemento protetto da replica specificato nell'area azure di destinazione definita dal mapping del contenitore di protezione e dalla configurazione della replica del disco fornita.</span><span class="sxs-lookup"><span data-stu-id="26d8b-123">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

### <span data-ttu-id="26d8b-124">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="26d8b-124">Example 4</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi `
 -DiskEncryptionVaultId  $DiskEncryptionVaultId -DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
 -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

    
<span data-ttu-id="26d8b-125">Avviare l'operazione della direzione di aggiornamento per l'elemento protetto da replica crittografata specificato nell'area azure di destinazione definita dal mapping del contenitore di protezione e dalla configurazione della replica del disco specificata.</span><span class="sxs-lookup"><span data-stu-id="26d8b-125">Start the update direction operation for the specified encrypted replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

### <span data-ttu-id="26d8b-126">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="26d8b-126">Example 5</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="26d8b-127">Avviare l'operazione della direzione di aggiornamento per l'elemento protetto da replica specificato nell'area azure di destinazione definita dal mapping del contenitore di protezione e usando l'archiviazione cache (nella stessa area della macchina virtuale) e il gruppo di posizionamento di prossimità.</span><span class="sxs-lookup"><span data-stu-id="26d8b-127">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM) and proximity placement group.</span></span>


## <span data-ttu-id="26d8b-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26d8b-128">PARAMETERS</span></span>

### <span data-ttu-id="26d8b-129">-Account</span><span class="sxs-lookup"><span data-stu-id="26d8b-129">-Account</span></span>
<span data-ttu-id="26d8b-130">L'account Esegui come da usare per eseguire l'installazione push del servizio per dispositivi mobili, se necessario.</span><span class="sxs-lookup"><span data-stu-id="26d8b-130">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="26d8b-131">Deve essere nell'elenco di account run as nel tessuto ASR.</span><span class="sxs-lookup"><span data-stu-id="26d8b-131">Must be one from the list of run as accounts in the ASR fabric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26d8b-132">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="26d8b-132">-AzureToAzure</span></span>
<span data-ttu-id="26d8b-133">Specifica il ripristino di emergenza da Azure ad Azure.</span><span class="sxs-lookup"><span data-stu-id="26d8b-133">Specifies the Azure to Azure disaster recovery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26d8b-134">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="26d8b-134">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="26d8b-135">Specifica la configurazione del disco per il ripristino di emergenza.</span><span class="sxs-lookup"><span data-stu-id="26d8b-135">Specifies the disk configuration for disaster recovery.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26d8b-136">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="26d8b-136">-AzureToVMware</span></span>
<span data-ttu-id="26d8b-137">Specifica il passaggio da azure a vMWare.</span><span class="sxs-lookup"><span data-stu-id="26d8b-137">Specifies the switch azure to vMWare scenario.</span></span>

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

### <span data-ttu-id="26d8b-138">-DataStore</span><span class="sxs-lookup"><span data-stu-id="26d8b-138">-DataStore</span></span>
<span data-ttu-id="26d8b-139">Archivio dati VMware da usare per il vmdisk.</span><span class="sxs-lookup"><span data-stu-id="26d8b-139">The VMware data-store to be used for the vmdisk's.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRDataStore
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26d8b-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26d8b-140">-DefaultProfile</span></span>
<span data-ttu-id="26d8b-141">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="26d8b-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="26d8b-142">-Direction</span><span class="sxs-lookup"><span data-stu-id="26d8b-142">-Direction</span></span>
<span data-ttu-id="26d8b-143">Specifica la direzione da usare per l'operazione di aggiornamento dopo il failover.</span><span class="sxs-lookup"><span data-stu-id="26d8b-143">Specifies the direction to be used for the update operation post a failover.</span></span>
<span data-ttu-id="26d8b-144">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="26d8b-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="26d8b-145">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="26d8b-145">PrimaryToRecovery</span></span>
- <span data-ttu-id="26d8b-146">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="26d8b-146">RecoveryToPrimary</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPIObject, AzureToVMware, VMwareToAzure, HyperVToAzure, EnterpriseToEnterprise, ByRPObject, ByPEObject
Aliases:
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26d8b-147">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="26d8b-147">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="26d8b-148">Specifica l'URL segreto di crittografia del disco con la versione (crittografia del disco di Azure) da usare come macchina virtuale di ripristino dopo il failover.</span><span class="sxs-lookup"><span data-stu-id="26d8b-148">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26d8b-149">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="26d8b-149">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="26d8b-150">Specifica l'ID vault segreto di crittografia del disco (crittografia disco di Azure) da usare per la macchina virtuale di ripristino dopo il failover.</span><span class="sxs-lookup"><span data-stu-id="26d8b-150">Specifies the disk encryption secret vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26d8b-151">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="26d8b-151">-HyperVToAzure</span></span>
<span data-ttu-id="26d8b-152">Proteggere nuovamente una macchina virtuale di Hyper-V dopo il failback.</span><span class="sxs-lookup"><span data-stu-id="26d8b-152">Reprotect a Hyper-V virtual machine after failback.</span></span>

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

### <span data-ttu-id="26d8b-153">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="26d8b-153">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="26d8b-154">Specifica l'URL della chiave di crittografia del disco (crittografia disco di Azure) da usare per la macchina virtuale di ripristino dopo il failover.</span><span class="sxs-lookup"><span data-stu-id="26d8b-154">Specifies the disk encryption key URL(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26d8b-155">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="26d8b-155">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="26d8b-156">Specifica l'ID keyVault della chiave di crittografia del disco (crittografia disco di Azure) da usare per la macchina virtuale di ripristino dopo il failover.</span><span class="sxs-lookup"><span data-stu-id="26d8b-156">Specifies the disk encryption key keyVault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26d8b-157">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="26d8b-157">-LogStorageAccountId</span></span>
<span data-ttu-id="26d8b-158">Specifica l'ID account di archiviazione in cui archiviare il log di replica delle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="26d8b-158">Specifies the storage account ID to store the replication log of VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26d8b-159">-MasterTarget</span><span class="sxs-lookup"><span data-stu-id="26d8b-159">-MasterTarget</span></span>
<span data-ttu-id="26d8b-160">Master Target Server Details.</span><span class="sxs-lookup"><span data-stu-id="26d8b-160">Master Target Server Details.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRMasterTargetServer
Parameter Sets: AzureToVMware, VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26d8b-161">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="26d8b-161">-ProcessServer</span></span>
<span data-ttu-id="26d8b-162">Process Server da usare per la replica.</span><span class="sxs-lookup"><span data-stu-id="26d8b-162">Process Server to be used for replication.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: AzureToVMware, VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26d8b-163">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="26d8b-163">-ProtectionContainerMapping</span></span>
<span data-ttu-id="26d8b-164">ContainerMapping di protezione da usare per la replica.</span><span class="sxs-lookup"><span data-stu-id="26d8b-164">Protection containerMapping to be used for replication.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: AzureToVMware, VMwareToAzure, AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26d8b-165">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="26d8b-165">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="26d8b-166">Il set di disponibilità in cui deve essere creata la macchina virtuale in caso di failover</span><span class="sxs-lookup"><span data-stu-id="26d8b-166">The availability set that the virtual machine should be created in upon failover</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26d8b-167">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="26d8b-167">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="26d8b-168">Specifica l'ID dell'account di archiviazione di Azure in cui eseguire la replica.</span><span class="sxs-lookup"><span data-stu-id="26d8b-168">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVToAzure, AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26d8b-169">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="26d8b-169">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="26d8b-170">Specifica l'account di archiviazione per la diagnostica di avvio per azure VM di ripristino.</span><span class="sxs-lookup"><span data-stu-id="26d8b-170">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26d8b-171">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="26d8b-171">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="26d8b-172">ID risorsa del servizio cloud di ripristino su cui eseguire il failover della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="26d8b-172">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26d8b-173">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="26d8b-173">-RecoveryPlan</span></span>
<span data-ttu-id="26d8b-174">Specifica un oggetto del piano di ripristino a matrice.</span><span class="sxs-lookup"><span data-stu-id="26d8b-174">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26d8b-175">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="26d8b-175">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="26d8b-176">ID risorsa del gruppo di posizionamento di prossimità di ripristino in cui eseguire il failover della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="26d8b-176">The resource ID of the recovery proximity placement group to failover this virtual machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26d8b-177">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="26d8b-177">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="26d8b-178">ID ResourceGroup di ripristino per la macchina virtuale protetta.</span><span class="sxs-lookup"><span data-stu-id="26d8b-178">Recovery resourceGroup id for protected Vm.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26d8b-179">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="26d8b-179">-ReplicationProtectedItem</span></span>
<span data-ttu-id="26d8b-180">Specifica un elemento protetto da replica ASR.</span><span class="sxs-lookup"><span data-stu-id="26d8b-180">Specifies an ASR replication protected item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, AzureToVMware, VMwareToAzure, HyperVToAzure, EnterpriseToEnterprise, AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26d8b-181">-RetentionVolume</span><span class="sxs-lookup"><span data-stu-id="26d8b-181">-RetentionVolume</span></span>
<span data-ttu-id="26d8b-182">Volume di conservazione nel server di destinazione master da usare.</span><span class="sxs-lookup"><span data-stu-id="26d8b-182">Retention Volume on the master target server to be used.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRetentionVolume
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26d8b-183">-PiùVmm</span><span class="sxs-lookup"><span data-stu-id="26d8b-183">-VmmToVmm</span></span>
<span data-ttu-id="26d8b-184">Direzione di replica dell'aggiornamento per una macchina virtuale Hyper-V non riuscita protetta tra due siti di Hyper-V gestiti da FTP.</span><span class="sxs-lookup"><span data-stu-id="26d8b-184">Update replication direction for a failed over Hyper-V virtual machine that is protected between two VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="26d8b-185">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="26d8b-185">-VMwareToAzure</span></span>
<span data-ttu-id="26d8b-186">Aggiornare la direzione della replica da VMware ad Azure.</span><span class="sxs-lookup"><span data-stu-id="26d8b-186">Update replication direction from VMware to Azure.</span></span>

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

### <span data-ttu-id="26d8b-187">-Confirm</span><span class="sxs-lookup"><span data-stu-id="26d8b-187">-Confirm</span></span>
<span data-ttu-id="26d8b-188">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26d8b-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26d8b-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26d8b-189">-WhatIf</span></span>
<span data-ttu-id="26d8b-190">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="26d8b-190">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26d8b-191">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="26d8b-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26d8b-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26d8b-192">CommonParameters</span></span>
<span data-ttu-id="26d8b-193">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26d8b-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26d8b-194">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="26d8b-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26d8b-195">INPUT</span><span class="sxs-lookup"><span data-stu-id="26d8b-195">INPUTS</span></span>

### <span data-ttu-id="26d8b-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="26d8b-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="26d8b-197">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="26d8b-197">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="26d8b-198">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="26d8b-198">OUTPUTS</span></span>

### <span data-ttu-id="26d8b-199">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="26d8b-199">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="26d8b-200">NOTE</span><span class="sxs-lookup"><span data-stu-id="26d8b-200">NOTES</span></span>

## <span data-ttu-id="26d8b-201">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="26d8b-201">RELATED LINKS</span></span>
