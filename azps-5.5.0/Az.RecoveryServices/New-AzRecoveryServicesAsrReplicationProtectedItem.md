---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: f27c9daa4e1d7df5b1feb3be42ccece780d66fb7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183895"
---
# <span data-ttu-id="31b39-101">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="31b39-101">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="31b39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31b39-102">SYNOPSIS</span></span>
<span data-ttu-id="31b39-103">Abilita la replica per un elemento protetto da ASR creando un elemento protetto da replica.</span><span class="sxs-lookup"><span data-stu-id="31b39-103">Enables replication for an ASR protectable item by creating a replication protected item.</span></span>

## <span data-ttu-id="31b39-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="31b39-104">SYNTAX</span></span>

### <span data-ttu-id="31b39-105">EnterpriseToEnterprise (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="31b39-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VmmToVmm] -ProtectableItem <ASRProtectableItem>
 -Name <String> -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31b39-106">VMwareToAzureWithDiskType</span><span class="sxs-lookup"><span data-stu-id="31b39-106">VMwareToAzureWithDiskType</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -Account <ASRRunAsAccount> [-LogStorageAccountId <String>] -ProcessServer <ASRProcessServer>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-RecoveryAvailabilityZone <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-WaitForCompletion] -DiskType <String>
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="31b39-107">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="31b39-107">VMwareToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -Account <ASRRunAsAccount> [-LogStorageAccountId <String>]
 [-InMageAzureV2DiskInput <AsrInMageAzureV2DiskInput[]>] -ProcessServer <ASRProcessServer>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-RecoveryAvailabilityZone <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-WaitForCompletion] [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31b39-108">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="31b39-108">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -RecoveryResourceGroupId <String> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31b39-109">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="31b39-109">HyperVSiteToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>]
 -RecoveryResourceGroupId <String> [-RecoveryAvailabilityZone <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-UseManagedDisk <String>] [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31b39-110">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="31b39-110">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure]
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> -AzureVmId <String>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilityZone <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-DiskEncryptionVaultId <String>]
 [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>] [-KeyEncryptionVaultId <String>]
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31b39-111">AzureToAzureWithoutDiskDetails</span><span class="sxs-lookup"><span data-stu-id="31b39-111">AzureToAzureWithoutDiskDetails</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure] -AzureVmId <String> -Name <String>
 [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 [-RecoveryAzureStorageAccountId <String>] -LogStorageAccountId <String> [-RecoveryAzureNetworkId <String>]
 [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String> [-ReplicationGroupName <String>]
 [-RecoveryAvailabilityZone <String>] [-RecoveryProximityPlacementGroupId <String>]
 [-RecoveryAvailabilitySetId <String>] [-RecoveryBootDiagStorageAccountId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31b39-112">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="31b39-112">DESCRIPTION</span></span>
<span data-ttu-id="31b39-113">Il cmdlet **New-AzRecoveryServicesAsrReplicationProtectedItem** crea un nuovo elemento protetto da replica.</span><span class="sxs-lookup"><span data-stu-id="31b39-113">The **New-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet creates a new replication protected item.</span></span>
<span data-ttu-id="31b39-114">Usare questo cmdlet per abilitare la replica per un elemento protetto da AsR.</span><span class="sxs-lookup"><span data-stu-id="31b39-114">Use this cmdlet to enable replication for an ASR protectable item.</span></span>

## <span data-ttu-id="31b39-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="31b39-115">EXAMPLES</span></span>

### <span data-ttu-id="31b39-116">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="31b39-116">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $VM -Name $VM.Name -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="31b39-117">Avvia l'operazione di creazione di elementi protetti da replica per l'elemento protetto da ASR specificato e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="31b39-117">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="31b39-118">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="31b39-118">Example 2</span></span>
```
PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] `
-RecoveryResourceGroupId $RecoveryResourceGroupId -RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name `
-ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem -ProtectionContainerMapping $pcm `
-RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName -LogStorageAccountId $LogStorageAccountId
```

<span data-ttu-id="31b39-119">Avvia l'operazione di creazione di elementi protetti da replica per l'elemento protetto da ASR specificato e restituisce il processo ASR usato per tenere traccia dell'operazione (scenario vmWare in Azure).</span><span class="sxs-lookup"><span data-stu-id="31b39-119">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation(vmWare to Azure scenario).</span></span>

### <span data-ttu-id="31b39-120">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="31b39-120">Example 3</span></span>
```
PS C:>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup
```

<span data-ttu-id="31b39-121">Avvia l'operazione di creazione di elementi protetti da replica per l'elemento protetto da ASR specificato e restituisce il processo ASR usato per tenere traccia dell'operazione (scenario da Azure ad Azure).</span><span class="sxs-lookup"><span data-stu-id="31b39-121">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="31b39-122">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="31b39-122">Example 4</span></span>
```
PS C:\> $disk1 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -RecoveryAzureNetworkId $RecoveryAzureNetworkId -RecoveryAzureSubnetName $RecoveryAzureSubnetName
```

<span data-ttu-id="31b39-123">Avvia l'operazione di creazione degli elementi protetti da replica per il valore VmId specificato e restituisce il processo ASR usato per tenere traccia dell'operazione (scenario da Azure ad Azure).</span><span class="sxs-lookup"><span data-stu-id="31b39-123">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="31b39-124">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="31b39-124">Example 5</span></span>
```
PS C:\>$disk1 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
PS C:\>$disk2 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId2 -LogStorageAccountId $logStorageAccountId -DiskType $diskType2

PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem  `
-ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName `
-LogStorageAccountId $LogStorageAccountId -InMageAzureV2DiskInput $disk1,$disk2
```

<span data-ttu-id="31b39-125">Avvia l'operazione di creazione di elementi protetti da replica per l'elemento protetto da ASR specificato, inclusi i dischi selettivi, e restituisce il processo ASR usato per tenere traccia dell'operazione (scenario da vmWare a Azure) con i dischi selezionati.</span><span class="sxs-lookup"><span data-stu-id="31b39-125">Starts the replication protected item creation operation for the specified ASR protectable item including selective disks and returns the ASR job used to track the operation(vmWare to Azure scenario) with selected disks.</span></span>

### <span data-ttu-id="31b39-126">Esempio 6</span><span class="sxs-lookup"><span data-stu-id="31b39-126">Example 6</span></span>
```
PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem  `
-ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName `
-LogStorageAccountId $LogStorageAccountId -DiskType Standard_LRS

Starts the replication protected item creation operation for the specified ASR protectable item with default disk type and returns the ASR job used to track the operation(vmWare to Azure scenario).
```

### <span data-ttu-id="31b39-127">Esempio 7</span><span class="sxs-lookup"><span data-stu-id="31b39-127">Example 7</span></span>
```
PS C:\> $disk1 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = new-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -DiskEncryptionVaultId  $DiskEncryptionVaultId -DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
 -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

<span data-ttu-id="31b39-128">Avvia l'operazione di creazione degli elementi protetti da replica per il valore VmId specificato e restituisce il processo ASR usato per tenere traccia dell'operazione (scenario da Azure ad Azure). Per il cmdlet di crittografia passato per la macchina virtuale di failover verranno usati i dettagli.</span><span class="sxs-lookup"><span data-stu-id="31b39-128">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).For the failover VM details passed in cmdlet for encryption will be used .</span></span>

### <span data-ttu-id="31b39-129">Esempio 8</span><span class="sxs-lookup"><span data-stu-id="31b39-129">Example 8</span></span>
```
PS C:>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="31b39-130">Avvia l'operazione di creazione di elementi protetti da replica per una macchina virtuale all'interno del gruppo di posizionamento di prossimità e restituisce il processo ASR usato per tenere traccia dell'operazione (scenario da Azure ad Azure).</span><span class="sxs-lookup"><span data-stu-id="31b39-130">Starts the replication protected item creation operation for a Virtual Machine inside Proximity placement group and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

## <span data-ttu-id="31b39-131">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31b39-131">PARAMETERS</span></span>

### <span data-ttu-id="31b39-132">-Account</span><span class="sxs-lookup"><span data-stu-id="31b39-132">-Account</span></span>
<span data-ttu-id="31b39-133">L'account Esegui come da usare per eseguire l'installazione push del servizio per dispositivi mobili, se necessario.</span><span class="sxs-lookup"><span data-stu-id="31b39-133">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="31b39-134">Deve essere nell'elenco di account run as nel tessuto ASR.</span><span class="sxs-lookup"><span data-stu-id="31b39-134">Must be one from the list of run as accounts in the ASR fabric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b39-135">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="31b39-135">-AzureToAzure</span></span>
<span data-ttu-id="31b39-136">Parametro switch specifica la creazione dell'elemento replicato in uno scenario azure.</span><span class="sxs-lookup"><span data-stu-id="31b39-136">Switch parameter specifies creating the replicated item in azure to azure scenario.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b39-137">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="31b39-137">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="31b39-138">Specifica la configurazione del disco da usare per lo scenario di ripristino di emergenza da Azure ad Azure.</span><span class="sxs-lookup"><span data-stu-id="31b39-138">Specifies the disk configuration to used Vm for Azure to Azure disaster recovery scenario.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b39-139">-AzureVmId</span><span class="sxs-lookup"><span data-stu-id="31b39-139">-AzureVmId</span></span>
<span data-ttu-id="31b39-140">Specifica l'ID della macchina virtuale di Azure per la protezione da ripristino di emergenza nell'area geografica di ripristino.</span><span class="sxs-lookup"><span data-stu-id="31b39-140">Specifies the Azure VM id for disaster recovery protection in recovery region.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b39-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31b39-141">-DefaultProfile</span></span>
<span data-ttu-id="31b39-142">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="31b39-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="31b39-143">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="31b39-143">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="31b39-144">Specifica l'URL segreto di crittografia del disco con la versione (crittografia del disco di Azure) da usare come macchina virtuale di ripristino dopo il failover.</span><span class="sxs-lookup"><span data-stu-id="31b39-144">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b39-145">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="31b39-145">-DiskEncryptionSetId</span></span>
<span data-ttu-id="31b39-146">Specifica l'ID risorsa del set di crittografia del disco da usare per la crittografia dei dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="31b39-146">Specifies the resource Id of the disk encryption set, to be used for the encryption of the managed disks.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b39-147">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="31b39-147">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="31b39-148">Specifica l'ID vault segreto di crittografia del disco (crittografia disco di Azure) da usare come macchina virtuale di ripristino dopo il failover.</span><span class="sxs-lookup"><span data-stu-id="31b39-148">Specifies the disk encryption secret vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b39-149">-DiskType</span><span class="sxs-lookup"><span data-stu-id="31b39-149">-DiskType</span></span>
<span data-ttu-id="31b39-150">Specifica il tipo di disco gestito dalla macchina virtuale di ripristino.</span><span class="sxs-lookup"><span data-stu-id="31b39-150">Specifies the Recovery VM managed disk type.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b39-151">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="31b39-151">-HyperVToAzure</span></span>
<span data-ttu-id="31b39-152">Il parametro switch per specificare che l'elemento replicato è una macchina virtuale di Hyper-V che viene replicata in Azure.</span><span class="sxs-lookup"><span data-stu-id="31b39-152">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated to Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b39-153">-IncludeDiskId</span><span class="sxs-lookup"><span data-stu-id="31b39-153">-IncludeDiskId</span></span>
<span data-ttu-id="31b39-154">L'elenco dei dischi da includere per la replica.</span><span class="sxs-lookup"><span data-stu-id="31b39-154">The list of disks to include for replication.</span></span> <span data-ttu-id="31b39-155">Per impostazione predefinita, sono inclusi tutti i dischi.</span><span class="sxs-lookup"><span data-stu-id="31b39-155">By default all disks are included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b39-156">-InMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="31b39-156">-InMageAzureV2DiskInput</span></span>
<span data-ttu-id="31b39-157">Specifica l'input di configurazione del disco per l'ID disco vMWare da proteggere dall'elemento protetto specificato.</span><span class="sxs-lookup"><span data-stu-id="31b39-157">Specifies the disk configuration input for vMWare disk id to protect from specified protectable item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.AsrInMageAzureV2DiskInput[]
Parameter Sets: VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b39-158">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="31b39-158">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="31b39-159">Specifica l'URL della chiave di crittografia del disco con la versione (crittografia disco di Azure) da usare per la macchina virtuale di ripristino dopo il failover.</span><span class="sxs-lookup"><span data-stu-id="31b39-159">Specifies the disk encryption key URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b39-160">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="31b39-160">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="31b39-161">Specifica l'ID chiave-vault della chiave di crittografia del disco (crittografia del disco di Azure) da usare come macchina virtuale di ripristino dopo il failover.</span><span class="sxs-lookup"><span data-stu-id="31b39-161">Specifies the disk encryption key key-vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b39-162">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="31b39-162">-LogStorageAccountId</span></span>
<span data-ttu-id="31b39-163">Specifica l'ID dell'account di archiviazione cache o del log da usare per archiviare i log di replica.</span><span class="sxs-lookup"><span data-stu-id="31b39-163">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b39-164">-Name</span><span class="sxs-lookup"><span data-stu-id="31b39-164">-Name</span></span>
<span data-ttu-id="31b39-165">Specifica un nome per l'elemento protetto da replica ASR.</span><span class="sxs-lookup"><span data-stu-id="31b39-165">Specifies a name for the ASR replication protected item.</span></span> <span data-ttu-id="31b39-166">Il nome deve essere univoco all'interno del vault.</span><span class="sxs-lookup"><span data-stu-id="31b39-166">The name must be unique within the vault.</span></span>

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

### <span data-ttu-id="31b39-167">-OS</span><span class="sxs-lookup"><span data-stu-id="31b39-167">-OS</span></span>
<span data-ttu-id="31b39-168">Specifica la famiglia di sistemi operativi.</span><span class="sxs-lookup"><span data-stu-id="31b39-168">Specifies the operating system family.</span></span>
<span data-ttu-id="31b39-169">I valori accettabili per questo parametro sono: Windows o Linux.</span><span class="sxs-lookup"><span data-stu-id="31b39-169">The acceptable values for this parameter are: Windows or Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases:
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b39-170">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="31b39-170">-OSDiskName</span></span>
<span data-ttu-id="31b39-171">Specifica il nome del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="31b39-171">Specifies the name of the operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b39-172">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="31b39-172">-ProcessServer</span></span>
<span data-ttu-id="31b39-173">Server dei processi da usare per replicare il computer.</span><span class="sxs-lookup"><span data-stu-id="31b39-173">The Process Server to use to replicate this machine.</span></span> <span data-ttu-id="31b39-174">Usare l'elenco dei server di processo nell'infrastruttura ASR corrispondente al server di configurazione per specificarne uno.</span><span class="sxs-lookup"><span data-stu-id="31b39-174">Use the list of process servers in the ASR fabric corresponding to the Configuration server to specify one.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b39-175">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="31b39-175">-ProtectableItem</span></span>
<span data-ttu-id="31b39-176">Specifica l'oggetto elemento protetto da AsR per cui viene abilitata la replica.</span><span class="sxs-lookup"><span data-stu-id="31b39-176">Specifies the ASR protectable item object for which replication is being enabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, VMwareToAzureWithDiskType, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31b39-177">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="31b39-177">-ProtectionContainerMapping</span></span>
<span data-ttu-id="31b39-178">Specifica l'oggetto mapping del contenitore di protezione ASR corrispondente al criterio di replica da usare per la replica.</span><span class="sxs-lookup"><span data-stu-id="31b39-178">Specifies the ASR protection container mapping object corresponding to the replication policy to be used for replication.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b39-179">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="31b39-179">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="31b39-180">ID del set di disponibilità in cui recuperare il computer in caso di failover.</span><span class="sxs-lookup"><span data-stu-id="31b39-180">The ID of the AvailabilitySet to recover the machine to in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b39-181">-RecoveryAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="31b39-181">-RecoveryAvailabilityZone</span></span>
<span data-ttu-id="31b39-182">Specifica l'area di disponibilità della macchina virtuale di ripristino dopo il failover.</span><span class="sxs-lookup"><span data-stu-id="31b39-182">Specifies the recovery VM availability zone after failover.</span></span>


```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b39-183">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="31b39-183">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="31b39-184">ID della rete virtuale di Azure in cui recuperare il computer in caso di failover.</span><span class="sxs-lookup"><span data-stu-id="31b39-184">The ID of the Azure virtual network to recover the machine to in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b39-185">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="31b39-185">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="31b39-186">Specifica l'ID dell'account di archiviazione di Azure in cui eseguire la replica.</span><span class="sxs-lookup"><span data-stu-id="31b39-186">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b39-187">-RecoveryAzureSubnetName</span><span class="sxs-lookup"><span data-stu-id="31b39-187">-RecoveryAzureSubnetName</span></span>
<span data-ttu-id="31b39-188">La subnet all'interno della rete virtuale di Azure di ripristino a cui deve essere collegata la macchina virtuale con errore in caso di failover.</span><span class="sxs-lookup"><span data-stu-id="31b39-188">The subnet within the recovery Azure virtual network to which the failed over virtual machine should be attached in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b39-189">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="31b39-189">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="31b39-190">Specifica l'account di archiviazione per la diagnostica di avvio per il ripristino di Azure VM.</span><span class="sxs-lookup"><span data-stu-id="31b39-190">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b39-191">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="31b39-191">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="31b39-192">Specifica l'ID risorsa del servizio cloud di ripristino su cui eseguire il failover della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="31b39-192">Specifies the resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b39-193">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="31b39-193">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="31b39-194">Specificare l'ID gruppo di posizionamento per prossimità usato dalla macchina virtuale di failover nell'area di ripristino di destinazione.</span><span class="sxs-lookup"><span data-stu-id="31b39-194">Specify the proximity placement group Id to used by the failover Vm in target recovery region.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b39-195">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="31b39-195">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="31b39-196">Specifica l ARM identificatore predefinito del gruppo di risorse in cui la macchina virtuale verrà creata in caso di failover.</span><span class="sxs-lookup"><span data-stu-id="31b39-196">Specifies the ARM identifier of the resource group in which the virtual machine will be created in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b39-197">-RecoveryVmName</span><span class="sxs-lookup"><span data-stu-id="31b39-197">-RecoveryVmName</span></span>
<span data-ttu-id="31b39-198">Nome della macchina virtuale di ripristino creata dopo il failover.</span><span class="sxs-lookup"><span data-stu-id="31b39-198">Name of the recovery Vm created after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b39-199">-ReplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="31b39-199">-ReplicationGroupName</span></span>
<span data-ttu-id="31b39-200">Specifica il nome del gruppo di replica da usare per creare punti di ripristino coerenti con più VM.</span><span class="sxs-lookup"><span data-stu-id="31b39-200">Specifies the replication group name to use to create multi-VM consistent recovery points.</span></span> <span data-ttu-id="31b39-201">Per impostazione predefinita, ogni elemento protetto da replica viene creato in un gruppo e non vengono generati punti di ripristino coerenti con più VM.</span><span class="sxs-lookup"><span data-stu-id="31b39-201">By default each replication protected item is created in a group of its own and multi-VM consistent recovery points are not generated.</span></span> <span data-ttu-id="31b39-202">Usare questa opzione solo se è necessario creare punti di ripristino coerenti con più vm in un gruppo di computer proteggendo tutti i computer nello stesso gruppo di replica.</span><span class="sxs-lookup"><span data-stu-id="31b39-202">Use this option only if you need to create multi-VM consistent recovery points across a group of machines by protecting all machines to the same replication group.</span></span> 

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b39-203">-UseManagedDisk</span><span class="sxs-lookup"><span data-stu-id="31b39-203">-UseManagedDisk</span></span>
<span data-ttu-id="31b39-204">Specifica se la macchina virtuale di Azure creata al failover deve usare dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="31b39-204">Specifies if the Azure virtual machine that is created on failover should use managed disks.</span></span> <span data-ttu-id="31b39-205">Accetta vero o falso.</span><span class="sxs-lookup"><span data-stu-id="31b39-205">It Accepts either True or False.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: True, False

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b39-206">-PiùVmm</span><span class="sxs-lookup"><span data-stu-id="31b39-206">-VmmToVmm</span></span>
<span data-ttu-id="31b39-207">Il parametro switch per specificare che l'elemento replicato è una macchina virtuale di Hyper-V replicata tra siti DI Hyper-V gestiti DA PIÙ.ER.</span><span class="sxs-lookup"><span data-stu-id="31b39-207">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated between VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="31b39-208">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="31b39-208">-VMwareToAzure</span></span>
<span data-ttu-id="31b39-209">Il parametro switch per specificare che l'elemento replicato è una macchina virtuale VMware o un server fisico che verrà replicato in Azure.</span><span class="sxs-lookup"><span data-stu-id="31b39-209">Switch parameter to specify the replicated item is a VMware virtual machine or physical server that will be replicate to Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b39-210">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="31b39-210">-WaitForCompletion</span></span>
<span data-ttu-id="31b39-211">Specifica che il cmdlet deve attendere il completamento dell'operazione prima di restituire.</span><span class="sxs-lookup"><span data-stu-id="31b39-211">Specifies that the cmdlet should wait for completion of the operation before returning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b39-212">-Confirm</span><span class="sxs-lookup"><span data-stu-id="31b39-212">-Confirm</span></span>
<span data-ttu-id="31b39-213">Chiede conferma prima di avviare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="31b39-213">Prompts  for confirmation before starting the operation.</span></span>

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

### <span data-ttu-id="31b39-214">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31b39-214">-WhatIf</span></span>
<span data-ttu-id="31b39-215">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="31b39-215">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31b39-216">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="31b39-216">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31b39-217">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31b39-217">CommonParameters</span></span>
<span data-ttu-id="31b39-218">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31b39-218">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31b39-219">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="31b39-219">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31b39-220">INPUT</span><span class="sxs-lookup"><span data-stu-id="31b39-220">INPUTS</span></span>

### <span data-ttu-id="31b39-221">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="31b39-221">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="31b39-222">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="31b39-222">OUTPUTS</span></span>

### <span data-ttu-id="31b39-223">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="31b39-223">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="31b39-224">NOTE</span><span class="sxs-lookup"><span data-stu-id="31b39-224">NOTES</span></span>

## <span data-ttu-id="31b39-225">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="31b39-225">RELATED LINKS</span></span>

[<span data-ttu-id="31b39-226">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="31b39-226">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="31b39-227">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="31b39-227">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="31b39-228">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="31b39-228">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
