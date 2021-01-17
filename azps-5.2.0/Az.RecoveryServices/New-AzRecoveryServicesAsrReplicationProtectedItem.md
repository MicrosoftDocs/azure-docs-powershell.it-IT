---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: bde840903c53dae9ba47b9eb30634ce90f80ee9e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359561"
---
# <span data-ttu-id="b0882-101">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b0882-101">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="b0882-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b0882-102">SYNOPSIS</span></span>
<span data-ttu-id="b0882-103">Abilita la replica per un elemento protettivo ASR creando un elemento protetto da replica.</span><span class="sxs-lookup"><span data-stu-id="b0882-103">Enables replication for an ASR protectable item by creating a replication protected item.</span></span>

## <span data-ttu-id="b0882-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b0882-104">SYNTAX</span></span>

### <span data-ttu-id="b0882-105">EnterpriseToEnterprise (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b0882-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VmmToVmm] -ProtectableItem <ASRProtectableItem>
 -Name <String> -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0882-106">VMwareToAzureWithDiskType</span><span class="sxs-lookup"><span data-stu-id="b0882-106">VMwareToAzureWithDiskType</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -Account <ASRRunAsAccount> [-LogStorageAccountId <String>] -ProcessServer <ASRProcessServer>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-WaitForCompletion] -DiskType <String> [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0882-107">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="b0882-107">VMwareToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -Account <ASRRunAsAccount> [-LogStorageAccountId <String>]
 [-InMageAzureV2DiskInput <AsrInMageAzureV2DiskInput[]>] -ProcessServer <ASRProcessServer>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-WaitForCompletion] [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0882-108">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="b0882-108">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -RecoveryResourceGroupId <String> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0882-109">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="b0882-109">HyperVSiteToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>]
 -RecoveryResourceGroupId <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0882-110">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="b0882-110">AzureToAzure</span></span>
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

### <span data-ttu-id="b0882-111">AzureToAzureWithoutDiskDetails</span><span class="sxs-lookup"><span data-stu-id="b0882-111">AzureToAzureWithoutDiskDetails</span></span>
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

## <span data-ttu-id="b0882-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b0882-112">DESCRIPTION</span></span>
<span data-ttu-id="b0882-113">Il cmdlet **New-AzRecoveryServicesAsrReplicationProtectedItem** crea un nuovo elemento protetto da replica.</span><span class="sxs-lookup"><span data-stu-id="b0882-113">The **New-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet creates a new replication protected item.</span></span>
<span data-ttu-id="b0882-114">Usa questo cmdlet per abilitare la replica per un elemento protetto da ASR.</span><span class="sxs-lookup"><span data-stu-id="b0882-114">Use this cmdlet to enable replication for an ASR protectable item.</span></span>

## <span data-ttu-id="b0882-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b0882-115">EXAMPLES</span></span>

### <span data-ttu-id="b0882-116">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b0882-116">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $VM -Name $VM.Name -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="b0882-117">Avvia l'operazione di creazione di elementi protetti da replica per l'elemento protetto ASR specificato e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="b0882-117">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="b0882-118">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b0882-118">Example 2</span></span>
```
PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] `
-RecoveryResourceGroupId $RecoveryResourceGroupId -RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name `
-ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem -ProtectionContainerMapping $pcm `
-RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName -LogStorageAccountId $LogStorageAccountId
```

<span data-ttu-id="b0882-119">Avvia l'operazione di creazione di elementi protetti da replica per l'elemento protetto ASR specificato e restituisce il processo ASR usato per tenere traccia dell'operazione (scenario vmWare-Azure).</span><span class="sxs-lookup"><span data-stu-id="b0882-119">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation(vmWare to Azure scenario).</span></span>

### <span data-ttu-id="b0882-120">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="b0882-120">Example 3</span></span>
```
PS C:>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup
```

<span data-ttu-id="b0882-121">Avvia l'operazione di creazione di elementi protetti da replica per l'elemento protetto ASR specificato e restituisce il processo ASR usato per tenere traccia dell'operazione (scenario di Azure in Azure).</span><span class="sxs-lookup"><span data-stu-id="b0882-121">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="b0882-122">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="b0882-122">Example 4</span></span>
```
PS C:\> $disk1 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -RecoveryAzureNetworkId $RecoveryAzureNetworkId -RecoveryAzureSubnetName $RecoveryAzureSubnetName
```

<span data-ttu-id="b0882-123">Avvia l'operazione di creazione di elementi protetta dalla replica per l'oggetto VmId specificato e restituisce il processo ASR usato per tenere traccia dell'operazione (scenario di Azure in Azure).</span><span class="sxs-lookup"><span data-stu-id="b0882-123">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="b0882-124">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="b0882-124">Example 5</span></span>
```
PS C:\>$disk1 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
PS C:\>$disk2 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId2 -LogStorageAccountId $logStorageAccountId -DiskType $diskType2

PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem  `
-ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName `
-LogStorageAccountId $LogStorageAccountId -InMageAzureV2DiskInput $disk1,$disk2
```

<span data-ttu-id="b0882-125">Avvia l'operazione di creazione di elementi protetti da replica per l'elemento protetto ASR specificato, inclusi i dischi selettivi e restituisce il processo ASR usato per tenere traccia dell'operazione (scenario vmWare in Azure) con i dischi selezionati.</span><span class="sxs-lookup"><span data-stu-id="b0882-125">Starts the replication protected item creation operation for the specified ASR protectable item including selective disks and returns the ASR job used to track the operation(vmWare to Azure scenario) with selected disks.</span></span>

### <span data-ttu-id="b0882-126">Esempio 6</span><span class="sxs-lookup"><span data-stu-id="b0882-126">Example 6</span></span>
```
PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem  `
-ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName `
-LogStorageAccountId $LogStorageAccountId -DiskType Standard_LRS

Starts the replication protected item creation operation for the specified ASR protectable item with default disk type and returns the ASR job used to track the operation(vmWare to Azure scenario).
```

### <span data-ttu-id="b0882-127">Esempio 7</span><span class="sxs-lookup"><span data-stu-id="b0882-127">Example 7</span></span>
```
PS C:\> $disk1 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = new-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -DiskEncryptionVaultId  $DiskEncryptionVaultId -DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
 -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

<span data-ttu-id="b0882-128">Avvia l'operazione di creazione di elementi protetta dalla replica per l'oggetto VmId specificato e restituisce il processo ASR usato per tenere traccia dell'operazione (scenario di Azure in Azure). Per i dettagli di failover VM passati in cmdlet per la crittografia verrà usato.</span><span class="sxs-lookup"><span data-stu-id="b0882-128">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).For the failover VM details passed in cmdlet for encryption will be used .</span></span>

### <span data-ttu-id="b0882-129">Esempio 8</span><span class="sxs-lookup"><span data-stu-id="b0882-129">Example 8</span></span>
```
PS C:>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="b0882-130">Avvia l'operazione di creazione di elementi protetti da replica per una macchina virtuale all'interno del gruppo di posizionamento di prossimità e restituisce il processo ASR usato per tenere traccia dell'operazione (scenario di Azure in Azure).</span><span class="sxs-lookup"><span data-stu-id="b0882-130">Starts the replication protected item creation operation for a Virtual Machine inside Proximity placement group and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

## <span data-ttu-id="b0882-131">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b0882-131">PARAMETERS</span></span>

### <span data-ttu-id="b0882-132">-Account</span><span class="sxs-lookup"><span data-stu-id="b0882-132">-Account</span></span>
<span data-ttu-id="b0882-133">L'account RunAs da usare per spingere l'installazione del servizio di mobilità, se necessario.</span><span class="sxs-lookup"><span data-stu-id="b0882-133">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="b0882-134">Deve essere uno dall'elenco di account RunAs nel tessuto ASR.</span><span class="sxs-lookup"><span data-stu-id="b0882-134">Must be one from the list of run as accounts in the ASR fabric.</span></span>

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

### <span data-ttu-id="b0882-135">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="b0882-135">-AzureToAzure</span></span>
<span data-ttu-id="b0882-136">Parametro switch specifica la creazione dell'elemento replicato in uno scenario di Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="b0882-136">Switch parameter specifies creating the replicated item in azure to azure scenario.</span></span>

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

### <span data-ttu-id="b0882-137">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="b0882-137">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="b0882-138">Specifica la configurazione del disco in uno scenario di ripristino di emergenza di VM per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="b0882-138">Specifies the disk configuration to used Vm for Azure to Azure disaster recovery scenario.</span></span>

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

### <span data-ttu-id="b0882-139">-AzureVmId</span><span class="sxs-lookup"><span data-stu-id="b0882-139">-AzureVmId</span></span>
<span data-ttu-id="b0882-140">Specifica l'ID VM di Azure per la protezione dal ripristino di emergenza nell'area di ripristino.</span><span class="sxs-lookup"><span data-stu-id="b0882-140">Specifies the Azure VM id for disaster recovery protection in recovery region.</span></span>

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

### <span data-ttu-id="b0882-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0882-141">-DefaultProfile</span></span>
<span data-ttu-id="b0882-142">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b0882-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="b0882-143">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="b0882-143">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="b0882-144">Specifica l'URL segreto di crittografia disco con la versione (Azure Disk Encryption) da usare come ripristino VM dopo il failover.</span><span class="sxs-lookup"><span data-stu-id="b0882-144">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="b0882-145">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="b0882-145">-DiskEncryptionSetId</span></span>
<span data-ttu-id="b0882-146">Specifica l'ID risorsa del set di crittografia disco da usare per la crittografia dei dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="b0882-146">Specifies the resource Id of the disk encryption set, to be used for the encryption of the managed disks.</span></span>

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

### <span data-ttu-id="b0882-147">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="b0882-147">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="b0882-148">Specifica l'ID del Vault segreto del disco (crittografia disco Azure) da usare come ripristino VM dopo il failover.</span><span class="sxs-lookup"><span data-stu-id="b0882-148">Specifies the disk encryption secret vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="b0882-149">-DiskType</span><span class="sxs-lookup"><span data-stu-id="b0882-149">-DiskType</span></span>
<span data-ttu-id="b0882-150">Specifica il tipo di disco gestito VM di ripristino.</span><span class="sxs-lookup"><span data-stu-id="b0882-150">Specifies the Recovery VM managed disk type.</span></span>

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

### <span data-ttu-id="b0882-151">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="b0882-151">-HyperVToAzure</span></span>
<span data-ttu-id="b0882-152">Parametro switch per specificare che l'elemento replicato è una macchina virtuale Hyper-V che viene replicata in Azure.</span><span class="sxs-lookup"><span data-stu-id="b0882-152">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated to Azure.</span></span>

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

### <span data-ttu-id="b0882-153">-IncludeDiskId</span><span class="sxs-lookup"><span data-stu-id="b0882-153">-IncludeDiskId</span></span>
<span data-ttu-id="b0882-154">Elenco di dischi da includere per la replica.</span><span class="sxs-lookup"><span data-stu-id="b0882-154">The list of disks to include for replication.</span></span> <span data-ttu-id="b0882-155">Per impostazione predefinita, tutti i dischi sono inclusi.</span><span class="sxs-lookup"><span data-stu-id="b0882-155">By default all disks are included.</span></span>

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

### <span data-ttu-id="b0882-156">-InMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="b0882-156">-InMageAzureV2DiskInput</span></span>
<span data-ttu-id="b0882-157">Specifica l'input di configurazione del disco per vMWare disk ID per la protezione da un elemento protetto specificato.</span><span class="sxs-lookup"><span data-stu-id="b0882-157">Specifies the disk configuration input for vMWare disk id to protect from specified protectable item.</span></span>

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

### <span data-ttu-id="b0882-158">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="b0882-158">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="b0882-159">Specifica l'URL della chiave di crittografia del disco con la versione (Azure Disk Encryption) da usare come ripristino VM dopo il failover.</span><span class="sxs-lookup"><span data-stu-id="b0882-159">Specifies the disk encryption key URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="b0882-160">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="b0882-160">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="b0882-161">Specifica la chiave della chiave di crittografia del disco-ID Vault (crittografia disco Azure) da usare come VM di ripristino dopo il failover.</span><span class="sxs-lookup"><span data-stu-id="b0882-161">Specifies the disk encryption key key-vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="b0882-162">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="b0882-162">-LogStorageAccountId</span></span>
<span data-ttu-id="b0882-163">Specifica l'ID dell'account di archiviazione del log o della cache da usare per archiviare i registri di replica.</span><span class="sxs-lookup"><span data-stu-id="b0882-163">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="b0882-164">-Nome</span><span class="sxs-lookup"><span data-stu-id="b0882-164">-Name</span></span>
<span data-ttu-id="b0882-165">Specifica un nome per l'elemento protetto da replica ASR.</span><span class="sxs-lookup"><span data-stu-id="b0882-165">Specifies a name for the ASR replication protected item.</span></span> <span data-ttu-id="b0882-166">Il nome deve essere univoco all'interno del Vault.</span><span class="sxs-lookup"><span data-stu-id="b0882-166">The name must be unique within the vault.</span></span>

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

### <span data-ttu-id="b0882-167">-OS</span><span class="sxs-lookup"><span data-stu-id="b0882-167">-OS</span></span>
<span data-ttu-id="b0882-168">Specifica la famiglia di sistemi operativi.</span><span class="sxs-lookup"><span data-stu-id="b0882-168">Specifies the operating system family.</span></span>
<span data-ttu-id="b0882-169">I valori accettabili per questo parametro sono: Windows o Linux.</span><span class="sxs-lookup"><span data-stu-id="b0882-169">The acceptable values for this parameter are: Windows or Linux.</span></span>

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

### <span data-ttu-id="b0882-170">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="b0882-170">-OSDiskName</span></span>
<span data-ttu-id="b0882-171">Specifica il nome del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b0882-171">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="b0882-172">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="b0882-172">-ProcessServer</span></span>
<span data-ttu-id="b0882-173">Il server dei processi da usare per replicare il computer.</span><span class="sxs-lookup"><span data-stu-id="b0882-173">The Process Server to use to replicate this machine.</span></span> <span data-ttu-id="b0882-174">Usare l'elenco dei server di processo nel tessuto ASR che corrispondono al server di configurazione per specificarne uno.</span><span class="sxs-lookup"><span data-stu-id="b0882-174">Use the list of process servers in the ASR fabric corresponding to the Configuration server to specify one.</span></span>

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

### <span data-ttu-id="b0882-175">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="b0882-175">-ProtectableItem</span></span>
<span data-ttu-id="b0882-176">Specifica l'oggetto elemento protetto ASR per cui viene abilitata la replica.</span><span class="sxs-lookup"><span data-stu-id="b0882-176">Specifies the ASR protectable item object for which replication is being enabled.</span></span>

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

### <span data-ttu-id="b0882-177">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="b0882-177">-ProtectionContainerMapping</span></span>
<span data-ttu-id="b0882-178">Specifica l'oggetto mapping del contenitore di protezione ASR che corrisponde ai criteri di replica da usare per la replica.</span><span class="sxs-lookup"><span data-stu-id="b0882-178">Specifies the ASR protection container mapping object corresponding to the replication policy to be used for replication.</span></span>

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

### <span data-ttu-id="b0882-179">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="b0882-179">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="b0882-180">ID della AvailabilitySet in cui ripristinare il computer in caso di failover.</span><span class="sxs-lookup"><span data-stu-id="b0882-180">The ID of the AvailabilitySet to recover the machine to in the event of a failover.</span></span>

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

### <span data-ttu-id="b0882-181">-RecoveryAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="b0882-181">-RecoveryAvailabilityZone</span></span>
<span data-ttu-id="b0882-182">Specifica l'area di disponibilità di ripristino VM dopo il failover.</span><span class="sxs-lookup"><span data-stu-id="b0882-182">Specifies the recovery VM availability zone after failover.</span></span>


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

### <span data-ttu-id="b0882-183">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="b0882-183">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="b0882-184">ID della rete virtuale di Azure in cui ripristinare il computer in caso di failover.</span><span class="sxs-lookup"><span data-stu-id="b0882-184">The ID of the Azure virtual network to recover the machine to in the event of a failover.</span></span>

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

### <span data-ttu-id="b0882-185">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="b0882-185">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="b0882-186">Specifica l'ID dell'account di archiviazione di Azure a cui eseguire la replica.</span><span class="sxs-lookup"><span data-stu-id="b0882-186">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="b0882-187">-RecoveryAzureSubnetName</span><span class="sxs-lookup"><span data-stu-id="b0882-187">-RecoveryAzureSubnetName</span></span>
<span data-ttu-id="b0882-188">La subnet all'interno della rete virtuale di Azure recupero a cui deve essere associata la macchina virtuale fallita in caso di failover.</span><span class="sxs-lookup"><span data-stu-id="b0882-188">The subnet within the recovery Azure virtual network to which the failed over virtual machine should be attached in the event of a failover.</span></span>

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

### <span data-ttu-id="b0882-189">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="b0882-189">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="b0882-190">Specifica l'account di archiviazione per la diagnostica di avvio per ripristino di Azure VM.</span><span class="sxs-lookup"><span data-stu-id="b0882-190">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="b0882-191">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="b0882-191">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="b0882-192">Specifica l'ID risorsa del servizio cloud di ripristino a cui eseguire il failover della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b0882-192">Specifies the resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="b0882-193">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="b0882-193">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="b0882-194">Specifica l'ID del gruppo di posizionamento di prossimità usato dalla VM di failover nell'area di recupero di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b0882-194">Specify the proximity placement group Id to used by the failover Vm in target recovery region.</span></span>

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

### <span data-ttu-id="b0882-195">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="b0882-195">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="b0882-196">Specifica l'identificatore ARM del gruppo di risorse in cui verrà creata la macchina virtuale in caso di failover.</span><span class="sxs-lookup"><span data-stu-id="b0882-196">Specifies the ARM identifier of the resource group in which the virtual machine will be created in the event of a failover.</span></span>

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

### <span data-ttu-id="b0882-197">-RecoveryVmName</span><span class="sxs-lookup"><span data-stu-id="b0882-197">-RecoveryVmName</span></span>
<span data-ttu-id="b0882-198">Nome della VM di ripristino creata dopo il failover.</span><span class="sxs-lookup"><span data-stu-id="b0882-198">Name of the recovery Vm created after failover.</span></span>

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

### <span data-ttu-id="b0882-199">-ReplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="b0882-199">-ReplicationGroupName</span></span>
<span data-ttu-id="b0882-200">Specifica il nome del gruppo di replica da usare per creare punti di ripristino coerenti con più VM.</span><span class="sxs-lookup"><span data-stu-id="b0882-200">Specifies the replication group name to use to create multi-VM consistent recovery points.</span></span> <span data-ttu-id="b0882-201">Per impostazione predefinita, ogni elemento protetto da replica viene creato in un gruppo di punti di ripristino coerenti e con più VM non vengono generati.</span><span class="sxs-lookup"><span data-stu-id="b0882-201">By default each replication protected item is created in a group of its own and multi-VM consistent recovery points are not generated.</span></span> <span data-ttu-id="b0882-202">Usare questa opzione solo se è necessario creare punti di ripristino coerenti con più VM in un gruppo di computer, proteggendo tutti i computer nello stesso gruppo di replica.</span><span class="sxs-lookup"><span data-stu-id="b0882-202">Use this option only if you need to create multi-VM consistent recovery points across a group of machines by protecting all machines to the same replication group.</span></span> 

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

### <span data-ttu-id="b0882-203">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="b0882-203">-VmmToVmm</span></span>
<span data-ttu-id="b0882-204">Parametro switch per specificare che l'elemento replicato è una macchina virtuale Hyper-V che viene replicata tra i siti Hyper-V gestiti da VMM.</span><span class="sxs-lookup"><span data-stu-id="b0882-204">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated between VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="b0882-205">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="b0882-205">-VMwareToAzure</span></span>
<span data-ttu-id="b0882-206">Parametro switch per specificare che l'elemento replicato è una macchina virtuale VMware o un server fisico che verrà replicato in Azure.</span><span class="sxs-lookup"><span data-stu-id="b0882-206">Switch parameter to specify the replicated item is a VMware virtual machine or physical server that will be replicate to Azure.</span></span>

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

### <span data-ttu-id="b0882-207">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="b0882-207">-WaitForCompletion</span></span>
<span data-ttu-id="b0882-208">Specifica che il cmdlet deve attendere il completamento dell'operazione prima della restituzione.</span><span class="sxs-lookup"><span data-stu-id="b0882-208">Specifies that the cmdlet should wait for completion of the operation before returning.</span></span>

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

### <span data-ttu-id="b0882-209">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b0882-209">-Confirm</span></span>
<span data-ttu-id="b0882-210">Richiede la conferma prima di avviare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="b0882-210">Prompts  for confirmation before starting the operation.</span></span>

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

### <span data-ttu-id="b0882-211">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0882-211">-WhatIf</span></span>
<span data-ttu-id="b0882-212">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b0882-212">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0882-213">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b0882-213">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0882-214">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0882-214">CommonParameters</span></span>
<span data-ttu-id="b0882-215">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0882-215">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0882-216">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b0882-216">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0882-217">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b0882-217">INPUTS</span></span>

### <span data-ttu-id="b0882-218">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="b0882-218">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="b0882-219">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b0882-219">OUTPUTS</span></span>

### <span data-ttu-id="b0882-220">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="b0882-220">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b0882-221">Note</span><span class="sxs-lookup"><span data-stu-id="b0882-221">NOTES</span></span>

## <span data-ttu-id="b0882-222">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b0882-222">RELATED LINKS</span></span>

[<span data-ttu-id="b0882-223">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b0882-223">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="b0882-224">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b0882-224">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="b0882-225">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b0882-225">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
