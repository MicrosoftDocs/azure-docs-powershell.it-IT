---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectiondirection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: 326f73e0a056c6d68d0bdd96ddca1aea7c1c6147
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202636"
---
# <span data-ttu-id="9a762-101">Update-AzRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="9a762-101">Update-AzRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="9a762-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9a762-102">SYNOPSIS</span></span>
<span data-ttu-id="9a762-103">Aggiorna la direzione di replica per l'elemento protetto di replica o il piano di ripristino specificato.</span><span class="sxs-lookup"><span data-stu-id="9a762-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="9a762-104">Usato per ripetere la protezione/inversione della replica di un piano di ripristino o di elemento replicato non riuscito.</span><span class="sxs-lookup"><span data-stu-id="9a762-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

## <span data-ttu-id="9a762-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9a762-105">SYNTAX</span></span>

### <span data-ttu-id="9a762-106">ByRPIObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9a762-106">ByRPIObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a762-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="9a762-107">AzureToVMware</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToVMware] [-Account <ASRRunAsAccount>]
 -DataStore <ASRDataStore> [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 -RetentionVolume <ASRRetentionVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9a762-108">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="9a762-108">VMwareToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VMwareToAzure] -Account <ASRRunAsAccount>
 [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a762-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="9a762-109">HyperVToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-HyperVToAzure] [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a762-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="9a762-110">EnterpriseToEnterprise</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VmmToVmm]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a762-111">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="9a762-111">AzureToAzure</span></span>
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

### <span data-ttu-id="9a762-112">AzureToAzureWithMultipleStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9a762-112">AzureToAzureWithMultipleStorageAccount</span></span>
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

### <span data-ttu-id="9a762-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="9a762-113">ByRPObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a762-114">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="9a762-114">ByPEObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -Direction <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a762-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9a762-115">DESCRIPTION</span></span>
<span data-ttu-id="9a762-116">Il cmdlet **Update-AzRecoveryServicesAsrProtectionDirection** aggiorna la direzione di replica per l'oggetto di recupero del sito di Azure specificato dopo il completamento di un'operazione di failover di commit.</span><span class="sxs-lookup"><span data-stu-id="9a762-116">The **Update-AzRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="9a762-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9a762-117">EXAMPLES</span></span>

### <span data-ttu-id="9a762-118">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9a762-118">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="9a762-119">Avviare l'operazione di direzione dell'aggiornamento per il piano di ripristino specificato e restituire l'oggetto processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="9a762-119">Start the update direction operation for the specified recovery plan and returns the ASR job object used to track the operation.</span></span>

### <span data-ttu-id="9a762-120">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9a762-120">Example 2</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi
```

<span data-ttu-id="9a762-121">Avviare l'operazione di direzione dell'aggiornamento per l'elemento protetto della replica specificato nell'area di Azure di destinazione definita dal mapping del contenitore di protezione e dall'uso dell'archiviazione della cache (nella stessa area geografica di VM).</span><span class="sxs-lookup"><span data-stu-id="9a762-121">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM).</span></span>

### <span data-ttu-id="9a762-122">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="9a762-122">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi
```

<span data-ttu-id="9a762-123">Avviare l'operazione di direzione dell'aggiornamento per l'elemento protetto della replica specificato nell'area di Azure di destinazione definita dal mapping del contenitore di protezione e dalla configurazione della replica del disco fornita.</span><span class="sxs-lookup"><span data-stu-id="9a762-123">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

### <span data-ttu-id="9a762-124">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="9a762-124">Example 4</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi `
 -DiskEncryptionVaultId  $DiskEncryptionVaultId -DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
 -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

    
<span data-ttu-id="9a762-125">Avviare l'operazione di direzione dell'aggiornamento per l'elemento protetto di replica crittografato specificato nell'area di Azure di destinazione definita dal mapping del contenitore di protezione e dalla configurazione della replica del disco fornita.</span><span class="sxs-lookup"><span data-stu-id="9a762-125">Start the update direction operation for the specified encrypted replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

### <span data-ttu-id="9a762-126">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="9a762-126">Example 5</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="9a762-127">Avviare l'operazione di direzione dell'aggiornamento per l'elemento protetto della replica specificato nell'area di Azure di destinazione definita dal mapping del contenitore di protezione e dall'uso dell'archiviazione della cache (nella stessa area geografica) e del gruppo di posizionamento di prossimità.</span><span class="sxs-lookup"><span data-stu-id="9a762-127">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM) and proximity placement group.</span></span>


## <span data-ttu-id="9a762-128">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9a762-128">PARAMETERS</span></span>

### <span data-ttu-id="9a762-129">-Account</span><span class="sxs-lookup"><span data-stu-id="9a762-129">-Account</span></span>
<span data-ttu-id="9a762-130">L'account RunAs da usare per spingere l'installazione del servizio di mobilità, se necessario.</span><span class="sxs-lookup"><span data-stu-id="9a762-130">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="9a762-131">Deve essere uno dall'elenco di account RunAs nel tessuto ASR.</span><span class="sxs-lookup"><span data-stu-id="9a762-131">Must be one from the list of run as accounts in the ASR fabric.</span></span>

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

### <span data-ttu-id="9a762-132">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="9a762-132">-AzureToAzure</span></span>
<span data-ttu-id="9a762-133">Specifica il ripristino di emergenza di Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="9a762-133">Specifies the Azure to Azure disaster recovery.</span></span>

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

### <span data-ttu-id="9a762-134">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="9a762-134">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="9a762-135">Specifica la configurazione del disco per il ripristino di emergenza.</span><span class="sxs-lookup"><span data-stu-id="9a762-135">Specifies the disk configuration for disaster recovery.</span></span>

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

### <span data-ttu-id="9a762-136">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="9a762-136">-AzureToVMware</span></span>
<span data-ttu-id="9a762-137">Specifica lo scenario di switch Azure to vMWare.</span><span class="sxs-lookup"><span data-stu-id="9a762-137">Specifies the switch azure to vMWare scenario.</span></span>

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

### <span data-ttu-id="9a762-138">-Datastore</span><span class="sxs-lookup"><span data-stu-id="9a762-138">-DataStore</span></span>
<span data-ttu-id="9a762-139">Il VMware Data-Store da usare per il vmdisk.</span><span class="sxs-lookup"><span data-stu-id="9a762-139">The VMware data-store to be used for the vmdisk's.</span></span>

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

### <span data-ttu-id="9a762-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a762-140">-DefaultProfile</span></span>
<span data-ttu-id="9a762-141">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9a762-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="9a762-142">-Direzione</span><span class="sxs-lookup"><span data-stu-id="9a762-142">-Direction</span></span>
<span data-ttu-id="9a762-143">Specifica la direzione da usare per l'operazione di aggiornamento dopo un failover.</span><span class="sxs-lookup"><span data-stu-id="9a762-143">Specifies the direction to be used for the update operation post a failover.</span></span>
<span data-ttu-id="9a762-144">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="9a762-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9a762-145">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="9a762-145">PrimaryToRecovery</span></span>
- <span data-ttu-id="9a762-146">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="9a762-146">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="9a762-147">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="9a762-147">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="9a762-148">Specifica l'URL segreto di crittografia disco con la versione (Azure Disk Encryption) da usare come ripristino VM dopo il failover.</span><span class="sxs-lookup"><span data-stu-id="9a762-148">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="9a762-149">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="9a762-149">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="9a762-150">Specifica l'ID del Vault segreto del disco (crittografia disco Azure) da usare come ripristino VM dopo il failover.</span><span class="sxs-lookup"><span data-stu-id="9a762-150">Specifies the disk encryption secret vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="9a762-151">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="9a762-151">-HyperVToAzure</span></span>
<span data-ttu-id="9a762-152">Riproteggere una macchina virtuale Hyper-V dopo il failback.</span><span class="sxs-lookup"><span data-stu-id="9a762-152">Reprotect a Hyper-V virtual machine after failback.</span></span>

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

### <span data-ttu-id="9a762-153">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="9a762-153">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="9a762-154">Specifica l'URL della chiave di crittografia del disco (Azure Disk Encryption) da usare come ripristino VM dopo il failover.</span><span class="sxs-lookup"><span data-stu-id="9a762-154">Specifies the disk encryption key URL(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="9a762-155">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="9a762-155">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="9a762-156">Specifica l'ID della chiave di crittografia del disco (Azure Disk Encryption) da usare come ripristino VM dopo il failover.</span><span class="sxs-lookup"><span data-stu-id="9a762-156">Specifies the disk encryption key keyVault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="9a762-157">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="9a762-157">-LogStorageAccountId</span></span>
<span data-ttu-id="9a762-158">Specifica l'ID account di archiviazione per archiviare il log di replica delle VM.</span><span class="sxs-lookup"><span data-stu-id="9a762-158">Specifies the storage account ID to store the replication log of VMs.</span></span>

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

### <span data-ttu-id="9a762-159">-MasterTarget</span><span class="sxs-lookup"><span data-stu-id="9a762-159">-MasterTarget</span></span>
<span data-ttu-id="9a762-160">Dettagli del server di destinazione master.</span><span class="sxs-lookup"><span data-stu-id="9a762-160">Master Target Server Details.</span></span>

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

### <span data-ttu-id="9a762-161">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="9a762-161">-ProcessServer</span></span>
<span data-ttu-id="9a762-162">Process Server da usare per la replica.</span><span class="sxs-lookup"><span data-stu-id="9a762-162">Process Server to be used for replication.</span></span>

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

### <span data-ttu-id="9a762-163">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="9a762-163">-ProtectionContainerMapping</span></span>
<span data-ttu-id="9a762-164">Protezione containerMapping da usare per la replica.</span><span class="sxs-lookup"><span data-stu-id="9a762-164">Protection containerMapping to be used for replication.</span></span>

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

### <span data-ttu-id="9a762-165">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="9a762-165">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="9a762-166">Il set di disponibilità che deve essere creato dalla macchina virtuale al momento del failover</span><span class="sxs-lookup"><span data-stu-id="9a762-166">The availability set that the virtual machine should be created in upon failover</span></span>

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

### <span data-ttu-id="9a762-167">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="9a762-167">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="9a762-168">Specifica l'ID dell'account di archiviazione di Azure a cui eseguire la replica.</span><span class="sxs-lookup"><span data-stu-id="9a762-168">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="9a762-169">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="9a762-169">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="9a762-170">Specifica l'account di archiviazione per la diagnostica di avvio per ripristino di Azure VM.</span><span class="sxs-lookup"><span data-stu-id="9a762-170">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="9a762-171">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="9a762-171">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="9a762-172">ID risorsa del servizio cloud di ripristino a cui eseguire il failover della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9a762-172">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="9a762-173">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9a762-173">-RecoveryPlan</span></span>
<span data-ttu-id="9a762-174">Specifica un oggetto piano di ripristino ASR.</span><span class="sxs-lookup"><span data-stu-id="9a762-174">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="9a762-175">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="9a762-175">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="9a762-176">ID risorsa del gruppo posizionamento di prossimità di ripristino a cui eseguire il failover della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9a762-176">The resource ID of the recovery proximity placement group to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="9a762-177">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="9a762-177">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="9a762-178">ID resourceGroup di ripristino per VM protetta.</span><span class="sxs-lookup"><span data-stu-id="9a762-178">Recovery resourceGroup id for protected Vm.</span></span>

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

### <span data-ttu-id="9a762-179">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9a762-179">-ReplicationProtectedItem</span></span>
<span data-ttu-id="9a762-180">Specifica un elemento protetto da replica ASR.</span><span class="sxs-lookup"><span data-stu-id="9a762-180">Specifies an ASR replication protected item.</span></span>

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

### <span data-ttu-id="9a762-181">-RetentionVolume</span><span class="sxs-lookup"><span data-stu-id="9a762-181">-RetentionVolume</span></span>
<span data-ttu-id="9a762-182">Volume di conservazione nel server di destinazione master da usare.</span><span class="sxs-lookup"><span data-stu-id="9a762-182">Retention Volume on the master target server to be used.</span></span>

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

### <span data-ttu-id="9a762-183">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="9a762-183">-VmmToVmm</span></span>
<span data-ttu-id="9a762-184">Aggiornare la direzione della replica per una macchina virtuale con failover Hyper-V protetta tra due siti Hyper-V gestiti da VMM.</span><span class="sxs-lookup"><span data-stu-id="9a762-184">Update replication direction for a failed over Hyper-V virtual machine that is protected between two VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="9a762-185">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="9a762-185">-VMwareToAzure</span></span>
<span data-ttu-id="9a762-186">Aggiornare la direzione della replica da VMware a Azure.</span><span class="sxs-lookup"><span data-stu-id="9a762-186">Update replication direction from VMware to Azure.</span></span>

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

### <span data-ttu-id="9a762-187">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9a762-187">-Confirm</span></span>
<span data-ttu-id="9a762-188">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a762-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a762-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a762-189">-WhatIf</span></span>
<span data-ttu-id="9a762-190">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9a762-190">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9a762-191">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9a762-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a762-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a762-192">CommonParameters</span></span>
<span data-ttu-id="9a762-193">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a762-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a762-194">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9a762-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a762-195">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9a762-195">INPUTS</span></span>

### <span data-ttu-id="9a762-196">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9a762-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="9a762-197">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9a762-197">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="9a762-198">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9a762-198">OUTPUTS</span></span>

### <span data-ttu-id="9a762-199">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="9a762-199">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9a762-200">Note</span><span class="sxs-lookup"><span data-stu-id="9a762-200">NOTES</span></span>

## <span data-ttu-id="9a762-201">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9a762-201">RELATED LINKS</span></span>
