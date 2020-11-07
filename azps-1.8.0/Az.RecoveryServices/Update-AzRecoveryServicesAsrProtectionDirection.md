---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectiondirection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: 9dd28cd3a05db15cef64a1e6023b1684909fdc13
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677533"
---
# <span data-ttu-id="06830-101">Update-AzRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="06830-101">Update-AzRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="06830-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="06830-102">SYNOPSIS</span></span>
<span data-ttu-id="06830-103">Aggiorna la direzione di replica per l'elemento protetto di replica o il piano di ripristino specificato.</span><span class="sxs-lookup"><span data-stu-id="06830-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="06830-104">Usato per ripetere la protezione/inversione della replica di un piano di ripristino o di elemento replicato non riuscito.</span><span class="sxs-lookup"><span data-stu-id="06830-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

## <span data-ttu-id="06830-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="06830-105">SYNTAX</span></span>

### <span data-ttu-id="06830-106">ByRPIObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="06830-106">ByRPIObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06830-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="06830-107">AzureToVMware</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToVMware] [-Account <ASRRunAsAccount>]
 -DataStore <ASRDataStore> [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 -RetentionVolume <ASRRetentionVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="06830-108">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="06830-108">VMwareToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VMwareToAzure] -Account <ASRRunAsAccount>
 [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06830-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="06830-109">HyperVToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-HyperVToAzure] [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06830-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="06830-110">EnterpriseToEnterprise</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VmmToVmm]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06830-111">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="06830-111">AzureToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -LogStorageAccountId <String>
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryResourceGroupId <String>] [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="06830-112">AzureToAzureWithMultipleStorageAccount</span><span class="sxs-lookup"><span data-stu-id="06830-112">AzureToAzureWithMultipleStorageAccount</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-RecoveryResourceGroupId <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="06830-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="06830-113">ByRPObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06830-114">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="06830-114">ByPEObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -Direction <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06830-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06830-115">DESCRIPTION</span></span>
<span data-ttu-id="06830-116">Il cmdlet **Update-AzRecoveryServicesAsrProtectionDirection** aggiorna la direzione di replica per l'oggetto di recupero del sito di Azure specificato dopo il completamento di un'operazione di failover di commit.</span><span class="sxs-lookup"><span data-stu-id="06830-116">The **Update-AzRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="06830-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="06830-117">EXAMPLES</span></span>

### <span data-ttu-id="06830-118">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="06830-118">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="06830-119">Avviare l'operazione di direzione dell'aggiornamento per il piano di ripristino specificato e restituire l'oggetto processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="06830-119">Start the update direction operation for the specified recovery plan and returns the ASR job object used to track the operation.</span></span>

### <span data-ttu-id="06830-120">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="06830-120">Example 2</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi
```

<span data-ttu-id="06830-121">Avviare l'operazione di direzione dell'aggiornamento per l'elemento protetto della replica specificato nell'area di Azure di destinazione definita dal mapping del contenitore di protezione e dall'uso dell'archiviazione della cache (nella stessa area geografica di VM).</span><span class="sxs-lookup"><span data-stu-id="06830-121">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM).</span></span>

### <span data-ttu-id="06830-122">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="06830-122">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi
```

<span data-ttu-id="06830-123">Avviare l'operazione di direzione dell'aggiornamento per l'elemento protetto della replica specificato nell'area di Azure di destinazione definita dal mapping del contenitore di protezione e dalla configurazione della replica del disco fornita.</span><span class="sxs-lookup"><span data-stu-id="06830-123">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

## <span data-ttu-id="06830-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="06830-124">PARAMETERS</span></span>

### <span data-ttu-id="06830-125">-Account</span><span class="sxs-lookup"><span data-stu-id="06830-125">-Account</span></span>
<span data-ttu-id="06830-126">L'account RunAs da usare per spingere l'installazione del servizio di mobilità, se necessario.</span><span class="sxs-lookup"><span data-stu-id="06830-126">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="06830-127">Deve essere uno dall'elenco di account RunAs nel tessuto ASR.</span><span class="sxs-lookup"><span data-stu-id="06830-127">Must be one from the list of run as accounts in the ASR fabric.</span></span>

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

### <span data-ttu-id="06830-128">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="06830-128">-AzureToAzure</span></span>
<span data-ttu-id="06830-129">{{Fill AzureToAzure Description}}</span><span class="sxs-lookup"><span data-stu-id="06830-129">{{Fill AzureToAzure Description}}</span></span>

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

### <span data-ttu-id="06830-130">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="06830-130">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="06830-131">{{Fill AzureToAzureDiskReplicationConfiguration Description}}</span><span class="sxs-lookup"><span data-stu-id="06830-131">{{Fill AzureToAzureDiskReplicationConfiguration Description}}</span></span>

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

### <span data-ttu-id="06830-132">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="06830-132">-AzureToVMware</span></span>
<span data-ttu-id="06830-133">{{Fill AzureToVMware Description}}</span><span class="sxs-lookup"><span data-stu-id="06830-133">{{Fill AzureToVMware Description}}</span></span>

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

### <span data-ttu-id="06830-134">-Datastore</span><span class="sxs-lookup"><span data-stu-id="06830-134">-DataStore</span></span>
<span data-ttu-id="06830-135">Il datastore VMware da usare per il vmdisk.</span><span class="sxs-lookup"><span data-stu-id="06830-135">The VMware datastore to be used for the vmdisk's.</span></span>

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

### <span data-ttu-id="06830-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06830-136">-DefaultProfile</span></span>
<span data-ttu-id="06830-137">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="06830-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="06830-138">-Direzione</span><span class="sxs-lookup"><span data-stu-id="06830-138">-Direction</span></span>
<span data-ttu-id="06830-139">Specifica la direzione da usare per l'operazione di aggiornamento dopo un failover.</span><span class="sxs-lookup"><span data-stu-id="06830-139">Specifies the direction to be used for the update operation post a failover.</span></span>
<span data-ttu-id="06830-140">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="06830-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="06830-141">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="06830-141">PrimaryToRecovery</span></span>
- <span data-ttu-id="06830-142">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="06830-142">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="06830-143">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="06830-143">-HyperVToAzure</span></span>
<span data-ttu-id="06830-144">Riproteggere una macchina virtuale Hyper-V dopo il failback.</span><span class="sxs-lookup"><span data-stu-id="06830-144">Reprotect a Hyper-V virtual machine after failback.</span></span>

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

### <span data-ttu-id="06830-145">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="06830-145">-LogStorageAccountId</span></span>
<span data-ttu-id="06830-146">Specifica l'ID account di archiviazione per archiviare il log di replica delle VM.</span><span class="sxs-lookup"><span data-stu-id="06830-146">Specifies the storage account ID to store the replication log of VMs.</span></span>

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

### <span data-ttu-id="06830-147">-MasterTarget</span><span class="sxs-lookup"><span data-stu-id="06830-147">-MasterTarget</span></span>
<span data-ttu-id="06830-148">Dettagli del server di destinazione master.</span><span class="sxs-lookup"><span data-stu-id="06830-148">Master Target Server Details.</span></span>

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

### <span data-ttu-id="06830-149">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="06830-149">-ProcessServer</span></span>
<span data-ttu-id="06830-150">Process Server da usare per la replica.</span><span class="sxs-lookup"><span data-stu-id="06830-150">Process Server to be used for replication.</span></span>

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

### <span data-ttu-id="06830-151">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="06830-151">-ProtectionContainerMapping</span></span>
<span data-ttu-id="06830-152">Protezione containerMapping da usare per la replica.</span><span class="sxs-lookup"><span data-stu-id="06830-152">Protection containerMapping to be used for replication.</span></span>

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

### <span data-ttu-id="06830-153">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="06830-153">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="06830-154">Il set di disponibilità che deve essere creato dalla macchina virtuale al momento del failover</span><span class="sxs-lookup"><span data-stu-id="06830-154">The availability set that the virtual machine should be created in upon failover</span></span>

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

### <span data-ttu-id="06830-155">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="06830-155">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="06830-156">Specifica l'ID dell'account di archiviazione di Azure a cui eseguire la replica.</span><span class="sxs-lookup"><span data-stu-id="06830-156">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="06830-157">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="06830-157">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="06830-158">Specifica l'account di archiviazione per la diagnostica di avvio per ripristino di Azure VM.</span><span class="sxs-lookup"><span data-stu-id="06830-158">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="06830-159">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="06830-159">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="06830-160">ID risorsa del servizio cloud di ripristino a cui eseguire il failover della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="06830-160">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="06830-161">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="06830-161">-RecoveryPlan</span></span>
<span data-ttu-id="06830-162">Specifica un oggetto piano di ripristino ASR.</span><span class="sxs-lookup"><span data-stu-id="06830-162">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="06830-163">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="06830-163">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="06830-164">ID resourceGroup di ripristino per VM protetta.</span><span class="sxs-lookup"><span data-stu-id="06830-164">Recovery resourceGroup id for protected Vm.</span></span>

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

### <span data-ttu-id="06830-165">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="06830-165">-ReplicationProtectedItem</span></span>
<span data-ttu-id="06830-166">Specifica un elemento protetto da replica ASR.</span><span class="sxs-lookup"><span data-stu-id="06830-166">Specifies an ASR replication protected item.</span></span>

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

### <span data-ttu-id="06830-167">-RetentionVolume</span><span class="sxs-lookup"><span data-stu-id="06830-167">-RetentionVolume</span></span>
<span data-ttu-id="06830-168">Volume di conservazione nel server di destinazione master da usare.</span><span class="sxs-lookup"><span data-stu-id="06830-168">Retention Volume on the master target server to be used.</span></span>

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

### <span data-ttu-id="06830-169">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="06830-169">-VmmToVmm</span></span>
<span data-ttu-id="06830-170">Aggiornare la direzione della replica per una macchina virtuale con failover Hyper-V protetta tra due siti Hyper-V gestiti da VMM.</span><span class="sxs-lookup"><span data-stu-id="06830-170">Update replication direction for a failed over Hyper-V virtual machine that is protected between two VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="06830-171">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="06830-171">-VMwareToAzure</span></span>
<span data-ttu-id="06830-172">Aggiornare la direzione della replica da VMware a Azure.</span><span class="sxs-lookup"><span data-stu-id="06830-172">Update replication direction from VMware to Azure.</span></span>

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

### <span data-ttu-id="06830-173">-Confermare</span><span class="sxs-lookup"><span data-stu-id="06830-173">-Confirm</span></span>
<span data-ttu-id="06830-174">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06830-174">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06830-175">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06830-175">-WhatIf</span></span>
<span data-ttu-id="06830-176">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="06830-176">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="06830-177">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="06830-177">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06830-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06830-178">CommonParameters</span></span>
<span data-ttu-id="06830-179">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06830-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06830-180">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06830-180">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06830-181">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="06830-181">INPUTS</span></span>

### <span data-ttu-id="06830-182">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="06830-182">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="06830-183">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="06830-183">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="06830-184">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="06830-184">OUTPUTS</span></span>

### <span data-ttu-id="06830-185">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="06830-185">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="06830-186">Note</span><span class="sxs-lookup"><span data-stu-id="06830-186">NOTES</span></span>

## <span data-ttu-id="06830-187">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="06830-187">RELATED LINKS</span></span>
