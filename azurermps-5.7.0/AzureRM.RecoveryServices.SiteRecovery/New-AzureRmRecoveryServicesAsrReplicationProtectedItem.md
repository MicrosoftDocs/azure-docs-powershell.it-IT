---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: fab7fa9f02f70b5afa1c4c5ffcbd07a8e1706998
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687023"
---
# <span data-ttu-id="6e2ec-101">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6e2ec-101">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="6e2ec-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6e2ec-102">SYNOPSIS</span></span>
<span data-ttu-id="6e2ec-103">Abilita la replica per un elemento protettivo ASR creando un elemento protetto da replica.</span><span class="sxs-lookup"><span data-stu-id="6e2ec-103">Enables replication for an ASR protectable item by creating a replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e2ec-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6e2ec-104">SYNTAX</span></span>

### <span data-ttu-id="6e2ec-105">EnterpriseToEnterprise (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6e2ec-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-VmmToVmm] -ProtectableItem <ASRProtectableItem>
 -Name <String> -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e2ec-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="6e2ec-106">VMwareToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -Account <ASRRunAsAccount> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] -ProcessServer <ASRProcessServer> [-RecoveryAzureNetworkId <String>]
 [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String> [-ReplicationGroupName <String>]
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e2ec-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="6e2ec-107">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -RecoveryResourceGroupId <String> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e2ec-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="6e2ec-108">HyperVSiteToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>]
 -RecoveryResourceGroupId <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e2ec-109">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="6e2ec-109">AzureToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure]
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> -AzureVmId <String>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryResourceGroupId <String> [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e2ec-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e2ec-110">DESCRIPTION</span></span>
<span data-ttu-id="6e2ec-111">Il cmdlet **New-AzureRmRecoveryServicesAsrReplicationProtectedItem** crea un nuovo elemento protetto da replica.</span><span class="sxs-lookup"><span data-stu-id="6e2ec-111">The **New-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet creates a new replication protected item.</span></span>
<span data-ttu-id="6e2ec-112">Usa questo cmdlet per abilitare la replica per un elemento protetto da ASR.</span><span class="sxs-lookup"><span data-stu-id="6e2ec-112">Use this cmdlet to enable replication for an ASR protectable item.</span></span>

## <span data-ttu-id="6e2ec-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6e2ec-113">EXAMPLES</span></span>

### <span data-ttu-id="6e2ec-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6e2ec-114">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $VM -Name $VM.Name -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="6e2ec-115">Avvia l'operazione di creazione di elementi protetti da replica per l'elemento protetto ASR specificato e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="6e2ec-115">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="6e2ec-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="6e2ec-116">Example 2</span></span>
```
PS C:\>$job = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $pi -Name $rpiName -ProtectionContainerMapping $pcm `
-RecoveryAzureStorageAccountId $RecoveryAzureStorageAccountId -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-ProcessServer $fabric.fabricSpecificDetails.ProcessServers[0] -Account $fabric.fabricSpecificDetails.RunAsAccounts[0]
```

<span data-ttu-id="6e2ec-117">Avvia l'operazione di creazione di elementi protetti da replica per l'elemento protetto ASR specificato e restituisce il processo ASR usato per tenere traccia dell'operazione (scenario vmWare-Azure).</span><span class="sxs-lookup"><span data-stu-id="6e2ec-117">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation(vmWare to Azure scenario).</span></span>

### <span data-ttu-id="6e2ec-118">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="6e2ec-118">Example 3</span></span>
```
PS C:>$job = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzureVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup
```

<span data-ttu-id="6e2ec-119">Avvia l'operazione di creazione di elementi protetti da replica per l'elemento protetto ASR specificato e restituisce il processo ASR usato per tenere traccia dell'operazione (scenario di Azure in Azure).</span><span class="sxs-lookup"><span data-stu-id="6e2ec-119">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="6e2ec-120">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="6e2ec-120">Example 4</span></span>
```
PS C:\> $disk1 = new-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = new-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="6e2ec-121">Avvia l'operazione di creazione di elementi protetta dalla replica per l'oggetto VmId specificato e restituisce il processo ASR usato per tenere traccia dell'operazione (scenario di Azure in Azure).</span><span class="sxs-lookup"><span data-stu-id="6e2ec-121">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

## <span data-ttu-id="6e2ec-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6e2ec-122">PARAMETERS</span></span>

### <span data-ttu-id="6e2ec-123">-Account</span><span class="sxs-lookup"><span data-stu-id="6e2ec-123">-Account</span></span>
<span data-ttu-id="6e2ec-124">L'account RunAs da usare per spingere l'installazione del servizio di mobilità, se necessario.</span><span class="sxs-lookup"><span data-stu-id="6e2ec-124">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="6e2ec-125">Deve essere uno dall'elenco di account RunAs nel tessuto ASR.</span><span class="sxs-lookup"><span data-stu-id="6e2ec-125">Must be one from the list of run as accounts in the ASR fabric.</span></span>

```yaml
Type: ASRRunAsAccount
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e2ec-126">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="6e2ec-126">-AzureToAzure</span></span>
<span data-ttu-id="6e2ec-127">Parametro switch per specificare che l'elemento replicato è una macchina virtuale di Azure che viene replicata in un'area di Azure di ripristino.</span><span class="sxs-lookup"><span data-stu-id="6e2ec-127">Switch parameter to specify that the replicated item is an Azure virtual machine replicating to a recovery Azure region.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e2ec-128">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e2ec-128">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="6e2ec-129">Specifica l'elenco dei dischi della macchina virtuale da replicare e l'account di archiviazione della cache e dell'account di archiviazione di ripristino da usare per replicare il disco.</span><span class="sxs-lookup"><span data-stu-id="6e2ec-129">Specifies the list of virtual machine disks to replicated and the cache storage account and recovery storage account to be used to replicate the disk.</span></span>

```yaml
Type: ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e2ec-130">-AzureVmId</span><span class="sxs-lookup"><span data-stu-id="6e2ec-130">-AzureVmId</span></span>
<span data-ttu-id="6e2ec-131">Specifica l'ID VM di Azure da replicare.</span><span class="sxs-lookup"><span data-stu-id="6e2ec-131">Specifies the azure vm id to be replicated.</span></span>

```yaml
Type: String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e2ec-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6e2ec-132">-Confirm</span></span>
<span data-ttu-id="6e2ec-133">Richiede la conferma prima di avviare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="6e2ec-133">Prompts  for confirmation before starting the operation.</span></span>

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

### <span data-ttu-id="6e2ec-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e2ec-134">-DefaultProfile</span></span>
<span data-ttu-id="6e2ec-135">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6e2ec-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="6e2ec-136">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="6e2ec-136">-HyperVToAzure</span></span>
<span data-ttu-id="6e2ec-137">Parametro switch per specificare che l'elemento replicato è una macchina virtuale Hyper-V che viene replicata in Azure.</span><span class="sxs-lookup"><span data-stu-id="6e2ec-137">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated to Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e2ec-138">-IncludeDiskId</span><span class="sxs-lookup"><span data-stu-id="6e2ec-138">-IncludeDiskId</span></span>
<span data-ttu-id="6e2ec-139">Elenco di dischi da includere per la replica.</span><span class="sxs-lookup"><span data-stu-id="6e2ec-139">The list of disks to include for replication.</span></span> <span data-ttu-id="6e2ec-140">Per impostazione predefinita, tutti i dischi sono inclusi.</span><span class="sxs-lookup"><span data-stu-id="6e2ec-140">By default all disks are included.</span></span>

```yaml
Type: String[]
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e2ec-141">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="6e2ec-141">-LogStorageAccountId</span></span>
<span data-ttu-id="6e2ec-142">Specifica l'ID dell'account di archiviazione del log o della cache da usare per archiviare i registri di replica.</span><span class="sxs-lookup"><span data-stu-id="6e2ec-142">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e2ec-143">-Nome</span><span class="sxs-lookup"><span data-stu-id="6e2ec-143">-Name</span></span>
<span data-ttu-id="6e2ec-144">Specifica un nome per l'elemento protetto da replica ASR.</span><span class="sxs-lookup"><span data-stu-id="6e2ec-144">Specifies a name for the ASR replication protected item.</span></span> <span data-ttu-id="6e2ec-145">Il nome deve essere univoco all'interno del Vault.</span><span class="sxs-lookup"><span data-stu-id="6e2ec-145">The name must be unique within the vault.</span></span>

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

### <span data-ttu-id="6e2ec-146">-OS</span><span class="sxs-lookup"><span data-stu-id="6e2ec-146">-OS</span></span>
<span data-ttu-id="6e2ec-147">Specifica la famiglia di sistemi operativi.</span><span class="sxs-lookup"><span data-stu-id="6e2ec-147">Specifies the operating system family.</span></span>
<span data-ttu-id="6e2ec-148">I valori accettabili per questo parametro sono: Windows o Linux.</span><span class="sxs-lookup"><span data-stu-id="6e2ec-148">The acceptable values for this parameter are: Windows or Linux.</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases:
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e2ec-149">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="6e2ec-149">-OSDiskName</span></span>
<span data-ttu-id="6e2ec-150">Specifica il nome del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="6e2ec-150">Specifies the name of the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e2ec-151">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="6e2ec-151">-ProcessServer</span></span>
<span data-ttu-id="6e2ec-152">Il server dei processi da usare per replicare il computer.</span><span class="sxs-lookup"><span data-stu-id="6e2ec-152">The Process Server to use to replicate this machine.</span></span> <span data-ttu-id="6e2ec-153">Usare l'elenco dei server di processo nel tessuto ASR che corrispondono al server di configurazione per specificarne uno.</span><span class="sxs-lookup"><span data-stu-id="6e2ec-153">Use the list of process servers in the ASR fabric corresponding to the Configuration server to specify one.</span></span>

```yaml
Type: ASRProcessServer
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e2ec-154">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="6e2ec-154">-ProtectableItem</span></span>
<span data-ttu-id="6e2ec-155">Specifica l'oggetto elemento protetto ASR per cui viene abilitata la replica.</span><span class="sxs-lookup"><span data-stu-id="6e2ec-155">Specifies the ASR protectable item object for which replication is being enabled.</span></span>

```yaml
Type: ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e2ec-156">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="6e2ec-156">-ProtectionContainerMapping</span></span>
<span data-ttu-id="6e2ec-157">Specifica l'oggetto mapping del contenitore di protezione ASR che corrisponde ai criteri di replica da usare per la replica.</span><span class="sxs-lookup"><span data-stu-id="6e2ec-157">Specifies the ASR protection container mapping object corresponding to the replication policy to be used for replication.</span></span>

```yaml
Type: ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e2ec-158">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="6e2ec-158">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="6e2ec-159">ID della AvailabilitySet in cui ripristinare il computer in caso di failover.</span><span class="sxs-lookup"><span data-stu-id="6e2ec-159">The ID of the AvailabilitySet to recover the machine to in the event of a failover.</span></span>

```yaml
Type: String
Parameter Sets: AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e2ec-160">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="6e2ec-160">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="6e2ec-161">ID della rete virtuale di Azure in cui ripristinare il computer in caso di failover.</span><span class="sxs-lookup"><span data-stu-id="6e2ec-161">The ID of the Azure virtual network to recover the machine to in the event of a failover.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e2ec-162">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="6e2ec-162">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="6e2ec-163">Specifica l'ID dell'account di archiviazione di Azure a cui eseguire la replica.</span><span class="sxs-lookup"><span data-stu-id="6e2ec-163">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e2ec-164">-RecoveryAzureSubnetName</span><span class="sxs-lookup"><span data-stu-id="6e2ec-164">-RecoveryAzureSubnetName</span></span>
<span data-ttu-id="6e2ec-165">La subnet all'interno della rete virtuale di Azure recupero a cui deve essere associata la macchina virtuale fallita in caso di failover.</span><span class="sxs-lookup"><span data-stu-id="6e2ec-165">The subnet within the recovery Azure virtual network to which the failed over virtual machine should be attached in the event of a failover.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e2ec-166">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="6e2ec-166">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="6e2ec-167">Specifica l'ID risorsa del servizio cloud di ripristino a cui eseguire il failover della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6e2ec-167">Specifies the resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

```yaml
Type: String
Parameter Sets: AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e2ec-168">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="6e2ec-168">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="6e2ec-169">Specifica l'identificatore ARM del gruppo di risorse in cui verrà creata la macchina virtuale in caso di failover.</span><span class="sxs-lookup"><span data-stu-id="6e2ec-169">Specifies the ARM identifier of the resource group in which the virtual machine will be created in the event of a failover.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e2ec-170">-RecoveryVmName</span><span class="sxs-lookup"><span data-stu-id="6e2ec-170">-RecoveryVmName</span></span>
<span data-ttu-id="6e2ec-171">Nome della VM di ripristino creata dopo il failover.</span><span class="sxs-lookup"><span data-stu-id="6e2ec-171">Name of the recovery Vm created after failover.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e2ec-172">-ReplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="6e2ec-172">-ReplicationGroupName</span></span>
<span data-ttu-id="6e2ec-173">Specifica il nome del gruppo di replica da usare per creare punti di ripristino coerenti con più VM.</span><span class="sxs-lookup"><span data-stu-id="6e2ec-173">Specifies the replication group name to use to create multi-VM consistent recovery points.</span></span> <span data-ttu-id="6e2ec-174">Per impostazione predefinita, ogni elemento protetto da replica viene creato in un gruppo di punti di ripristino coerenti e con più VM non vengono generati.</span><span class="sxs-lookup"><span data-stu-id="6e2ec-174">By default each replication protected item is created in a group of its own and multi-VM consistent recovery points are not generated.</span></span> <span data-ttu-id="6e2ec-175">Usare questa opzione solo se è necessario creare punti di ripristino coerenti con più VM in un gruppo di computer, proteggendo tutti i computer nello stesso gruppo di replica.</span><span class="sxs-lookup"><span data-stu-id="6e2ec-175">Use this option only if you need to create multi-VM consistent recovery points across a group of machines by protecting all machines to the same replication group.</span></span> 

```yaml
Type: String
Parameter Sets: VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e2ec-176">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="6e2ec-176">-VMwareToAzure</span></span>
<span data-ttu-id="6e2ec-177">Parametro switch per specificare che l'elemento replicato è una macchina virtuale VMware o un server fisico che verrà replicato in Azure.</span><span class="sxs-lookup"><span data-stu-id="6e2ec-177">Switch parameter to specify the replicated item is a VMware virtual machine or physical server that will be replicate to Azure.</span></span>

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

### <span data-ttu-id="6e2ec-178">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="6e2ec-178">-VmmToVmm</span></span>
<span data-ttu-id="6e2ec-179">Parametro switch per specificare che l'elemento replicato è una macchina virtuale Hyper-V che viene replicata tra i siti Hyper-V gestiti da VMM.</span><span class="sxs-lookup"><span data-stu-id="6e2ec-179">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated between VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="6e2ec-180">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="6e2ec-180">-WaitForCompletion</span></span>
<span data-ttu-id="6e2ec-181">Specifica che il cmdlet deve attendere il completamento dell'operazione prima della restituzione.</span><span class="sxs-lookup"><span data-stu-id="6e2ec-181">Specifies that the cmdlet should wait for completion of the operation before returning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e2ec-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e2ec-182">-WhatIf</span></span>
<span data-ttu-id="6e2ec-183">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6e2ec-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e2ec-184">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6e2ec-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e2ec-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e2ec-185">CommonParameters</span></span>
<span data-ttu-id="6e2ec-186">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e2ec-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e2ec-187">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e2ec-187">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e2ec-188">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6e2ec-188">INPUTS</span></span>

### <span data-ttu-id="6e2ec-189">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="6e2ec-189">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="6e2ec-190">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6e2ec-190">OUTPUTS</span></span>

### <span data-ttu-id="6e2ec-191">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="6e2ec-191">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6e2ec-192">Note</span><span class="sxs-lookup"><span data-stu-id="6e2ec-192">NOTES</span></span>

## <span data-ttu-id="6e2ec-193">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6e2ec-193">RELATED LINKS</span></span>

[<span data-ttu-id="6e2ec-194">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6e2ec-194">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="6e2ec-195">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6e2ec-195">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="6e2ec-196">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6e2ec-196">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
