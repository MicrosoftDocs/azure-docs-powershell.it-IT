---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 21c924d02a18ae60f07abd616809358208256039
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191318"
---
# <span data-ttu-id="84aa0-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="84aa0-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="84aa0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84aa0-102">SYNOPSIS</span></span>
<span data-ttu-id="84aa0-103">Imposta proprietà di ripristino come la rete di destinazione e le dimensioni della macchina virtuale per l'elemento protetto da replica specificato.</span><span class="sxs-lookup"><span data-stu-id="84aa0-103">Sets recovery properties such as target network and virtual machine size for the specified replication protected item.</span></span>

## <span data-ttu-id="84aa0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="84aa0-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem> [-Name <String>]
 [-Size <String>] [-UpdateNic <String>] [-RecoveryNetworkId <String>] [-PrimaryNic <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>]
 [-NicSelectionType <String>] [-RecoveryResourceGroupId <String>] [-LicenseType <String>]
 [-RecoveryAvailabilitySet <String>] [-RecoveryAvailabilityZone <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-EnableAcceleratedNetworkingOnRecovery]
 [-RecoveryBootDiagStorageAccountId <String>]
 [-AzureToAzureUpdateReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-UseManagedDisk <String>]
 [-DiskIdToDiskEncryptionSetMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-RecoveryPublicIPAddressId <String>] [-RecoveryNetworkSecurityGroupId <String>]
 [-RecoveryLBBackendAddressPoolId <String[]>] [-TfoAzureVMName <String>]
 [-ASRVMNicConfiguration <ASRVMNicConfig[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="84aa0-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="84aa0-105">DESCRIPTION</span></span>
<span data-ttu-id="84aa0-106">Il cmdlet **Set-AzRecoveryServicesAsrReplicationProtectedItem** imposta le proprietà di ripristino per un elemento protetto da replica.</span><span class="sxs-lookup"><span data-stu-id="84aa0-106">The **Set-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="84aa0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="84aa0-107">EXAMPLES</span></span>

### <span data-ttu-id="84aa0-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="84aa0-108">Example 1</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -UpdateNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

<span data-ttu-id="84aa0-109">Avvia l'operazione di aggiornamento delle impostazioni degli elementi protetti da replica usando i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="84aa0-109">Starts the operation of updating the replication protected item settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="84aa0-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="84aa0-110">Example 2</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -UpdateNic "00:50:56:8F:3F:7B" -RecoveryNetworkId $recoveryNetwork -RecoveryNicSubnetName $recoverySubnet -NicSelectionType NotSelected
```

<span data-ttu-id="84aa0-111">Avvia l'operazione di aggiornamento delle impostazioni della scheda di interfaccia di rete (riduzione NIC) dell'elemento protetto dalla replica usando i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="84aa0-111">Starts the operation of updating the replication protected item Network Interface card(NIC Reduction) settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="84aa0-112">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="84aa0-112">Example 3</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -PrimaryNic "00:50:56:8F:3F:7B"
```

<span data-ttu-id="84aa0-113">Avvia l'operazione di aggiornamento dell'elemento protetto da replica principale NIC(da usare per le impostazioni della macchina virtuale recuperata ) usando i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="84aa0-113">Starts the operation of updating the replication protected item primary NIC(to used for recovered vm )settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="84aa0-114">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="84aa0-114">Example 4</span></span>
```
PS C:\>Set-ASRReplicationProtectedItem -InputObject $rpi -UpdateNic $updateNic -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName�-NicSelectionType SelectedByUser
```

<span data-ttu-id="84aa0-115">Avvia l'operazione di aggiornamento delle impostazioni NIC dell'elemento protetto da replica (da usare per le vm recuperate) usando i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="84aa0-115">Starts the operation of updating the replication protected item NIC (to used for recovered vm )settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="84aa0-116">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="84aa0-116">Example 5</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -UpdateNic $updateNic `
        -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName -EnableAcceleratedNetworkingOnRecovery
```

<span data-ttu-id="84aa0-117">Avvia l'operazione di aggiornamento dell'elemento protetto da replica selezionato, che consente di abilitare la rete accelerata nella macchina virtuale di ripristino (per il ripristino di emergenza da Azure ad Azure).</span><span class="sxs-lookup"><span data-stu-id="84aa0-117">Starts the operation of updating the replication protected item selected noc tp enable accelerated networking on recovery VM(for Azure to Azure disaster recovery).</span></span>
<span data-ttu-id="84aa0-118">Non passare -EnableAcceleratedNetworkingOnRecovery per disabilitare la rete accelerata.</span><span class="sxs-lookup"><span data-stu-id="84aa0-118">Don�t pass -EnableAcceleratedNetworkingOnRecovery to disable accelerated Networking.</span></span>

### <span data-ttu-id="84aa0-119">Esempio 6</span><span class="sxs-lookup"><span data-stu-id="84aa0-119">Example 6</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi `
    -DiskEncryptionVaultId  $DiskEncryptionVaultId   �-DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
     -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

<span data-ttu-id="84aa0-120">Avviare l'operazione di aggiornamento per l'elemento protetto da replica crittografata specificata per usare i dettagli di crittografia forniti per la macchina virtuale di failover.</span><span class="sxs-lookup"><span data-stu-id="84aa0-120">Start the update operation for the specified encrypted replication protected item to use supplied encryption details for failover VM.</span></span>

### <span data-ttu-id="84aa0-121">Esempio 7</span><span class="sxs-lookup"><span data-stu-id="84aa0-121">Example 7</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="84aa0-122">Avviare l'operazione di aggiornamento per l'elemento protetto da replica specificato per usare il gruppo di posizionamento di prossimità specificato per la macchina virtuale di failover.</span><span class="sxs-lookup"><span data-stu-id="84aa0-122">Start the update operation for the specified replication protected item to use the supplied proximity placement group for failover VM.</span></span>

## <span data-ttu-id="84aa0-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84aa0-123">PARAMETERS</span></span>

### <span data-ttu-id="84aa0-124">-ASRVMNicConfiguration</span><span class="sxs-lookup"><span data-stu-id="84aa0-124">-ASRVMNicConfiguration</span></span>
<span data-ttu-id="84aa0-125">Specifica i dettagli di configurazione NIC di failover e failover del test.</span><span class="sxs-lookup"><span data-stu-id="84aa0-125">Specifies the test failover and failover NIC configuration details.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84aa0-126">-AzureToAzureUpdateReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="84aa0-126">-AzureToAzureUpdateReplicationConfiguration</span></span>
<span data-ttu-id="84aa0-127">Specifica la configurazione del disco per udpated per la macchina virtuale su disco gestita (da Azure ad Azure DR).</span><span class="sxs-lookup"><span data-stu-id="84aa0-127">Specifies the disk configuration to udpated for managed disk Vm (Azure to Azure DR scenrio).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84aa0-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84aa0-128">-DefaultProfile</span></span>
<span data-ttu-id="84aa0-129">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="84aa0-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="84aa0-130">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="84aa0-130">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="84aa0-131">Specifica l'URL segreto di crittografia del disco con la versione (crittografia del disco di Azure) da usare come macchina virtuale di ripristino dopo il failover.</span><span class="sxs-lookup"><span data-stu-id="84aa0-131">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84aa0-132">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="84aa0-132">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="84aa0-133">Specifica l'ID vault della chiave segreta di crittografia del disco (crittografia del disco di Azure) da usare come macchina virtuale di ripristino dopo il failover.</span><span class="sxs-lookup"><span data-stu-id="84aa0-133">Specifies the disk encryption secret key vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84aa0-134">-DiskIdToDiskEncryptionSetMap</span><span class="sxs-lookup"><span data-stu-id="84aa0-134">-DiskIdToDiskEncryptionSetMap</span></span>
<span data-ttu-id="84aa0-135">Dizionario dell'ID di risorsa disco e del set di crittografia ARM DISCO.</span><span class="sxs-lookup"><span data-stu-id="84aa0-135">The dictionary of disk resource Id to disk encryption set ARM Id.</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84aa0-136">-EnableAcceleratedNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="84aa0-136">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="84aa0-137">Specifica il nic specificato nella macchina virtuale di ripristino dopo il failover usa la rete accelerata.</span><span class="sxs-lookup"><span data-stu-id="84aa0-137">Specifies the specified NIC on recovery vm after failover uses accelerated networking.</span></span>

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

### <span data-ttu-id="84aa0-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84aa0-138">-InputObject</span></span>
<span data-ttu-id="84aa0-139">Oggetto di input per il cmdlet: oggetto elemento protetto da replica ASR corrispondente all'elemento protetto da replica da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="84aa0-139">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84aa0-140">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="84aa0-140">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="84aa0-141">Specifica la versione dell'URL della chiave di crittografia del disco (crittografia disco di Azure) da usare per la macchina virtuale di ripristino dopo il failover.</span><span class="sxs-lookup"><span data-stu-id="84aa0-141">Specifies the disk encryption key URL version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84aa0-142">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="84aa0-142">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="84aa0-143">Specifica l'ID keyVault della chiave di crittografia del disco (crittografia disco di Azure) da usare come macchina virtuale di ripristino dopo il failover.</span><span class="sxs-lookup"><span data-stu-id="84aa0-143">Specifies the disk encryption key keyVault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84aa0-144">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="84aa0-144">-LicenseType</span></span>
<span data-ttu-id="84aa0-145">Specificare il tipo di licenza da usare per le macchine virtuali di Windows Server.</span><span class="sxs-lookup"><span data-stu-id="84aa0-145">Specifiy the license type selection to be used for Windows Server virtual machines.</span></span> <span data-ttu-id="84aa0-146">Se si è autorizzati a usare il vantaggio HUB (Hybrid Use Benefit) di Azure per le migrazioni e si vuole specificare che l'impostazione HUB deve essere usata durante il failover di questo elemento protetto, impostare il tipo di licenza su WindowsServer.</span><span class="sxs-lookup"><span data-stu-id="84aa0-146">If you are entitled to use the Azure Hybrid Use Benefit (HUB) for migrations and would like to specify that the HUB setting be used while failing over this protected item set the license type to be WindowsServer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NoLicenseType, WindowsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84aa0-147">-Name</span><span class="sxs-lookup"><span data-stu-id="84aa0-147">-Name</span></span>
<span data-ttu-id="84aa0-148">Specifica il nome della macchina virtuale di ripristino che verrà creata al failover.</span><span class="sxs-lookup"><span data-stu-id="84aa0-148">Specifies the name of the recovery virtual machine that will be created on failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84aa0-149">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="84aa0-149">-NicSelectionType</span></span>
<span data-ttu-id="84aa0-150">Specifica le proprietà nic (Network Interface Card) impostate dall'utente o impostate per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="84aa0-150">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="84aa0-151">È possibile specificare NotSelected per tornare ai valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="84aa0-151">You can specify NotSelected to go back to the default values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NotSelected, SelectedByUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84aa0-152">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="84aa0-152">-PrimaryNic</span></span>
<span data-ttu-id="84aa0-153">Specifica il nic che verrà usato come NIC principale per la MACCHINA virtuale di ripristino dopo il failover.</span><span class="sxs-lookup"><span data-stu-id="84aa0-153">Specifies the NIC which will be used as primary NIC for recvcovery VM after after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84aa0-154">-RecoveryAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="84aa0-154">-RecoveryAvailabilitySet</span></span>
<span data-ttu-id="84aa0-155">Set di disponibilità per l'elemento protetto da replica dopo il failover.</span><span class="sxs-lookup"><span data-stu-id="84aa0-155">Availability set for replication protected item after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84aa0-156">-RecoveryAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="84aa0-156">-RecoveryAvailabilityZone</span></span>
<span data-ttu-id="84aa0-157">Specifica l'area di disponibilità per l'elemento protetto da replica dopo il failover.</span><span class="sxs-lookup"><span data-stu-id="84aa0-157">Specifies availability zone for replication protected item after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84aa0-158">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="84aa0-158">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="84aa0-159">Specifica l'account di archiviazione per la diagnostica di avvio per il ripristino di Azure VM.</span><span class="sxs-lookup"><span data-stu-id="84aa0-159">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84aa0-160">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="84aa0-160">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="84aa0-161">ID risorsa del servizio cloud di ripristino su cui eseguire il failover della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="84aa0-161">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84aa0-162">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="84aa0-162">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="84aa0-163">Specifica i pool di indirizzi back-end di destinazione da associare al nic di ripristino.</span><span class="sxs-lookup"><span data-stu-id="84aa0-163">Specifies the target backend address pools to be associated with the recovery NIC.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84aa0-164">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="84aa0-164">-RecoveryNetworkId</span></span>
<span data-ttu-id="84aa0-165">Specifica l'ID della rete virtuale di Azure in cui eseguire il failed over per l'elemento protetto.</span><span class="sxs-lookup"><span data-stu-id="84aa0-165">Specifies the ID of the Azure virtual network to which the protected item should be failed over.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84aa0-166">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="84aa0-166">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="84aa0-167">Specifica l'ID del gruppo di sicurezza di rete da associare al nic di ripristino.</span><span class="sxs-lookup"><span data-stu-id="84aa0-167">Specifies the ID of the network security group to be associated with the recovery NIC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84aa0-168">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="84aa0-168">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="84aa0-169">Specifica l'indirizzo IP statico che deve essere assegnato alla scheda DI RETE principale al ripristino.</span><span class="sxs-lookup"><span data-stu-id="84aa0-169">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84aa0-170">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="84aa0-170">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="84aa0-171">Specifica il nome della subnet nella rete virtuale di azure di ripristino a cui deve essere connessa questa NIC dell'elemento protetto al failover.</span><span class="sxs-lookup"><span data-stu-id="84aa0-171">Specifies the name of the subnet on the recovery Azure virtual network to which this NIC of the protected item should be connected to on failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84aa0-172">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="84aa0-172">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="84aa0-173">Specifica l'ID risorsa del gruppo di posizionamento di prossimità di ripristino su cui eseguire il failover della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="84aa0-173">Specifies the Resource Id of the recovery proximity placement group to failover teh virtual machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84aa0-174">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="84aa0-174">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="84aa0-175">Specifica l'ID della risorsa dell'indirizzo IP pubblico da associare al nic di ripristino.</span><span class="sxs-lookup"><span data-stu-id="84aa0-175">Specifies the ID of the public IP address resource to be associated with the recovery NIC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84aa0-176">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="84aa0-176">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="84aa0-177">ID del gruppo di risorse Azure nell'area di ripristino in cui l'elemento protetto verrà recuperato in caso di failover.</span><span class="sxs-lookup"><span data-stu-id="84aa0-177">The ID of the Azure resource group in the recovery region in which the protected item will be recovered on failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84aa0-178">-Size</span><span class="sxs-lookup"><span data-stu-id="84aa0-178">-Size</span></span>
<span data-ttu-id="84aa0-179">Specifica le dimensioni della macchina virtuale di ripristino.</span><span class="sxs-lookup"><span data-stu-id="84aa0-179">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="84aa0-180">Il valore deve essere in base al set di dimensioni supportate dalle macchine virtuali di Azure.</span><span class="sxs-lookup"><span data-stu-id="84aa0-180">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84aa0-181">-TfoAzureVMName</span><span class="sxs-lookup"><span data-stu-id="84aa0-181">-TfoAzureVMName</span></span>
<span data-ttu-id="84aa0-182">Specifica il nome della macchina virtuale di failover del test.</span><span class="sxs-lookup"><span data-stu-id="84aa0-182">Specifies the name of the test failover VM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84aa0-183">-UpdateNic</span><span class="sxs-lookup"><span data-stu-id="84aa0-183">-UpdateNic</span></span>
<span data-ttu-id="84aa0-184">Specifica la nic della macchina virtuale per cui questo cmdlet imposta la proprietà di rete di ripristino deve essere udpated.</span><span class="sxs-lookup"><span data-stu-id="84aa0-184">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property needs to udpated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84aa0-185">-UseManagedDisk</span><span class="sxs-lookup"><span data-stu-id="84aa0-185">-UseManagedDisk</span></span>
<span data-ttu-id="84aa0-186">Specifica se la macchina virtuale di Azure creata al failover deve usare dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="84aa0-186">Specifies if the Azure virtual machine that is created on failover should use managed disks.</span></span>

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

### <span data-ttu-id="84aa0-187">-Confirm</span><span class="sxs-lookup"><span data-stu-id="84aa0-187">-Confirm</span></span>
<span data-ttu-id="84aa0-188">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84aa0-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84aa0-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84aa0-189">-WhatIf</span></span>
<span data-ttu-id="84aa0-190">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="84aa0-190">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="84aa0-191">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="84aa0-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84aa0-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84aa0-192">CommonParameters</span></span>
<span data-ttu-id="84aa0-193">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84aa0-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84aa0-194">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="84aa0-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84aa0-195">INPUT</span><span class="sxs-lookup"><span data-stu-id="84aa0-195">INPUTS</span></span>

### <span data-ttu-id="84aa0-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="84aa0-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="84aa0-197">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="84aa0-197">OUTPUTS</span></span>

### <span data-ttu-id="84aa0-198">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="84aa0-198">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="84aa0-199">NOTE</span><span class="sxs-lookup"><span data-stu-id="84aa0-199">NOTES</span></span>

## <span data-ttu-id="84aa0-200">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="84aa0-200">RELATED LINKS</span></span>

[<span data-ttu-id="84aa0-201">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="84aa0-201">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="84aa0-202">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="84aa0-202">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="84aa0-203">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="84aa0-203">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)
