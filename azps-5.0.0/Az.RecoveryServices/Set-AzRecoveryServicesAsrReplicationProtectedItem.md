---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 1b5f447e95e137ba9199ba596029f2088a977c91
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193664"
---
# <span data-ttu-id="dc131-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="dc131-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="dc131-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dc131-102">SYNOPSIS</span></span>
<span data-ttu-id="dc131-103">Imposta le proprietà di ripristino, ad esempio la rete di destinazione e la dimensione della macchina virtuale per l'elemento protetto della replica specificato.</span><span class="sxs-lookup"><span data-stu-id="dc131-103">Sets recovery properties such as target network and virtual machine size for the specified replication protected item.</span></span>

## <span data-ttu-id="dc131-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dc131-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem> [-Name <String>]
 [-Size <String>] [-UpdateNic <String>] [-RecoveryNetworkId <String>] [-PrimaryNic <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>]
 [-NicSelectionType <String>] [-RecoveryResourceGroupId <String>] [-LicenseType <String>]
 [-RecoveryAvailabilitySet <String>] [-RecoveryProximityPlacementGroupId <String>]
 [-EnableAcceleratedNetworkingOnRecovery] [-RecoveryBootDiagStorageAccountId <String>]
 [-AzureToAzureUpdateReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-UseManagedDisk <String>]
 [-DiskIdToDiskEncryptionSetMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-RecoveryPublicIPAddressId <String>] [-RecoveryNetworkSecurityGroupId <String>]
 [-RecoveryLBBackendAddressPoolId <String[]>] [-TfoAzureVMName <String>]
 [-ASRVMNicConfiguration <ASRVMNicConfig[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dc131-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dc131-105">DESCRIPTION</span></span>
<span data-ttu-id="dc131-106">Il cmdlet **set-AzRecoveryServicesAsrReplicationProtectedItem** imposta le proprietà di ripristino per un elemento protetto da replica.</span><span class="sxs-lookup"><span data-stu-id="dc131-106">The **Set-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="dc131-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dc131-107">EXAMPLES</span></span>

### <span data-ttu-id="dc131-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="dc131-108">Example 1</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -UpdateNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

<span data-ttu-id="dc131-109">Avvia l'operazione di aggiornamento delle impostazioni di elementi protetti da replica con i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="dc131-109">Starts the operation of updating the replication protected item settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="dc131-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="dc131-110">Example 2</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -UpdateNic "00:50:56:8F:3F:7B" -RecoveryNetworkId $recoveryNetwork -RecoveryNicSubnetName $recoverySubnet -NicSelectionType NotSelected
```

<span data-ttu-id="dc131-111">Avvia l'operazione di aggiornamento delle impostazioni della scheda interfaccia di rete (riduzione NIC) dell'elemento protetto da replica con i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="dc131-111">Starts the operation of updating the replication protected item Network Interface card(NIC Reduction) settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="dc131-112">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="dc131-112">Example 3</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -PrimaryNic "00:50:56:8F:3F:7B"
```

<span data-ttu-id="dc131-113">Avvia l'operazione di aggiornamento delle impostazioni della scheda NIC primaria dell'elemento protetto da replica (da usare per VM recuperate) usando i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="dc131-113">Starts the operation of updating the replication protected item primary NIC(to used for recovered vm )settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="dc131-114">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="dc131-114">Example 4</span></span>
```
PS C:\>Set-ASRReplicationProtectedItem -InputObject $rpi -UpdateNic $updateNic -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName�-NicSelectionType SelectedByUser
```

<span data-ttu-id="dc131-115">Avvia l'operazione di aggiornamento delle impostazioni di NIC dell'elemento protetto da replica (da usare per VM recuperate) usando i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="dc131-115">Starts the operation of updating the replication protected item NIC (to used for recovered vm )settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="dc131-116">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="dc131-116">Example 5</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -UpdateNic $updateNic `
        -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName -EnableAcceleratedNetworkingOnRecovery
```

<span data-ttu-id="dc131-117">Avvia l'operazione di aggiornamento dell'elemento protetto della replica il NOC selezionato TP Abilita la rete accelerata su VM di ripristino (per il ripristino di emergenza di Azure in Azure).</span><span class="sxs-lookup"><span data-stu-id="dc131-117">Starts the operation of updating the replication protected item selected noc tp enable accelerated networking on recovery VM(for Azure to Azure disaster recovery).</span></span>
<span data-ttu-id="dc131-118">Don t Pass-EnableAcceleratedNetworkingOnRecovery per disabilitare la rete accelerata.</span><span class="sxs-lookup"><span data-stu-id="dc131-118">Don�t pass -EnableAcceleratedNetworkingOnRecovery to disable accelerated Networking.</span></span>

### <span data-ttu-id="dc131-119">Esempio 6</span><span class="sxs-lookup"><span data-stu-id="dc131-119">Example 6</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi `
    -DiskEncryptionVaultId  $DiskEncryptionVaultId   �-DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
     -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

<span data-ttu-id="dc131-120">Avviare l'operazione di aggiornamento per l'elemento protetto di replica crittografato specificato per usare i dettagli di crittografia forniti per il failover VM.</span><span class="sxs-lookup"><span data-stu-id="dc131-120">Start the update operation for the specified encrypted replication protected item to use supplied encryption details for failover VM.</span></span>

### <span data-ttu-id="dc131-121">Esempio 7</span><span class="sxs-lookup"><span data-stu-id="dc131-121">Example 7</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="dc131-122">Avviare l'operazione di aggiornamento per l'elemento protetto di replica specificato per usare il gruppo di posizionamento di prossimità fornito per il failover VM.</span><span class="sxs-lookup"><span data-stu-id="dc131-122">Start the update operation for the specified replication protected item to use the supplied proximity placement group for failover VM.</span></span>


## <span data-ttu-id="dc131-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dc131-123">PARAMETERS</span></span>

### <span data-ttu-id="dc131-124">-ASRVMNicConfiguration</span><span class="sxs-lookup"><span data-stu-id="dc131-124">-ASRVMNicConfiguration</span></span>
<span data-ttu-id="dc131-125">Specifica il failover di test e i dettagli della configurazione della scheda di failover.</span><span class="sxs-lookup"><span data-stu-id="dc131-125">Specifies the test failover and failover NIC configuration details.</span></span>

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

### <span data-ttu-id="dc131-126">-AzureToAzureUpdateReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="dc131-126">-AzureToAzureUpdateReplicationConfiguration</span></span>
<span data-ttu-id="dc131-127">Specifica la configurazione del disco in udpated for Managed disk VM (Azure to Azure DR scenrio).</span><span class="sxs-lookup"><span data-stu-id="dc131-127">Specifies the disk configuration to udpated for managed disk Vm (Azure to Azure DR scenrio).</span></span>

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

### <span data-ttu-id="dc131-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc131-128">-DefaultProfile</span></span>
<span data-ttu-id="dc131-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dc131-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="dc131-130">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="dc131-130">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="dc131-131">Specifica l'URL segreto di crittografia disco con la versione (Azure Disk Encryption) da usare come ripristino VM dopo il failover.</span><span class="sxs-lookup"><span data-stu-id="dc131-131">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="dc131-132">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="dc131-132">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="dc131-133">Specifica l'ID del Vault della chiave segreta del disco (crittografia disco di Azure) da usare come ripristino VM dopo il failover.</span><span class="sxs-lookup"><span data-stu-id="dc131-133">Specifies the disk encryption secret key vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="dc131-134">-DiskIdToDiskEncryptionSetMap</span><span class="sxs-lookup"><span data-stu-id="dc131-134">-DiskIdToDiskEncryptionSetMap</span></span>
<span data-ttu-id="dc131-135">Il dizionario di ID risorsa disco in crittografia disco imposta ID ARM.</span><span class="sxs-lookup"><span data-stu-id="dc131-135">The dictionary of disk resource Id to disk encryption set ARM Id.</span></span>

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

### <span data-ttu-id="dc131-136">-EnableAcceleratedNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="dc131-136">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="dc131-137">Specifica la scheda NIC specificata in ripristino VM dopo il failover usa la rete accelerata.</span><span class="sxs-lookup"><span data-stu-id="dc131-137">Specifies the specified NIC on recovery vm after failover uses accelerated networking.</span></span>

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

### <span data-ttu-id="dc131-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc131-138">-InputObject</span></span>
<span data-ttu-id="dc131-139">Oggetto di input per il cmdlet: oggetto elemento protetto della replica ASR che corrisponde all'elemento protetto da replica per l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="dc131-139">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item to update.</span></span>

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

### <span data-ttu-id="dc131-140">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="dc131-140">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="dc131-141">Specifica la versione dell'URL della chiave di crittografia del disco (Azure Disk Encryption) da usare come ripristino VM dopo il failover.</span><span class="sxs-lookup"><span data-stu-id="dc131-141">Specifies the disk encryption key URL version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="dc131-142">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="dc131-142">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="dc131-143">Specifica l'ID della chiave di crittografia del disco (Azure Disk Encryption) da usare come ripristino VM dopo il failover.</span><span class="sxs-lookup"><span data-stu-id="dc131-143">Specifies the disk encryption key keyVault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>


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

### <span data-ttu-id="dc131-144">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="dc131-144">-LicenseType</span></span>
<span data-ttu-id="dc131-145">Specificare la selezione del tipo di licenza da usare per le macchine virtuali di Windows Server.</span><span class="sxs-lookup"><span data-stu-id="dc131-145">Specifiy the license type selection to be used for Windows Server virtual machines.</span></span> <span data-ttu-id="dc131-146">Se si ha diritto all'uso di Azure Hybrid use benefit (HUB) per le migrazioni e si vuole specificare che l'impostazione HUB venga usata durante il superamento di questo elemento protetto, impostare il tipo di licenza su WindowsServer.</span><span class="sxs-lookup"><span data-stu-id="dc131-146">If you are entitled to use the Azure Hybrid Use Benefit (HUB) for migrations and would like to specify that the HUB setting be used while failing over this protected item set the license type to be WindowsServer.</span></span>

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

### <span data-ttu-id="dc131-147">-Nome</span><span class="sxs-lookup"><span data-stu-id="dc131-147">-Name</span></span>
<span data-ttu-id="dc131-148">Specifica il nome della macchina virtuale di ripristino che verrà creata in failover.</span><span class="sxs-lookup"><span data-stu-id="dc131-148">Specifies the name of the recovery virtual machine that will be created on failover.</span></span>

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

### <span data-ttu-id="dc131-149">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="dc131-149">-NicSelectionType</span></span>
<span data-ttu-id="dc131-150">Specifica le proprietà della scheda di rete (NIC, Network Interface Card) impostate dall'utente o impostate per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="dc131-150">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="dc131-151">Puoi specificare NotSelected per tornare ai valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="dc131-151">You can specify NotSelected to go back to the default values.</span></span>

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

### <span data-ttu-id="dc131-152">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="dc131-152">-PrimaryNic</span></span>
<span data-ttu-id="dc131-153">Specifica la scheda NIC che verrà usata come NIC primaria per recvcovery VM dopo il failover.</span><span class="sxs-lookup"><span data-stu-id="dc131-153">Specifies the NIC which will be used as primary NIC for recvcovery VM after after failover.</span></span>

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

### <span data-ttu-id="dc131-154">-RecoveryAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="dc131-154">-RecoveryAvailabilitySet</span></span>
<span data-ttu-id="dc131-155">Set di disponibilità per l'elemento protetto da replica dopo il failover.</span><span class="sxs-lookup"><span data-stu-id="dc131-155">Availability set for replication protected item after failover.</span></span>

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

### <span data-ttu-id="dc131-156">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="dc131-156">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="dc131-157">Specifica l'account di archiviazione per la diagnostica di avvio per ripristino di Azure VM.</span><span class="sxs-lookup"><span data-stu-id="dc131-157">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="dc131-158">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="dc131-158">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="dc131-159">ID risorsa del servizio cloud di ripristino a cui eseguire il failover della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dc131-159">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="dc131-160">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="dc131-160">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="dc131-161">Specifica i pool di indirizzi backend di destinazione da associare alla NIC di ripristino.</span><span class="sxs-lookup"><span data-stu-id="dc131-161">Specifies the target backend address pools to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="dc131-162">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="dc131-162">-RecoveryNetworkId</span></span>
<span data-ttu-id="dc131-163">Specifica l'ID della rete virtuale di Azure a cui deve essere fallito l'elemento protetto.</span><span class="sxs-lookup"><span data-stu-id="dc131-163">Specifies the ID of the Azure virtual network to which the protected item should be failed over.</span></span>

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

### <span data-ttu-id="dc131-164">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="dc131-164">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="dc131-165">Specifica l'ID del gruppo di sicurezza di rete da associare alla NIC di ripristino.</span><span class="sxs-lookup"><span data-stu-id="dc131-165">Specifies the ID of the network security group to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="dc131-166">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="dc131-166">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="dc131-167">Specifica l'indirizzo IP statico che deve essere assegnato alla scheda NIC primaria al ripristino.</span><span class="sxs-lookup"><span data-stu-id="dc131-167">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

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

### <span data-ttu-id="dc131-168">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="dc131-168">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="dc131-169">Specifica il nome della subnet nella rete virtuale di Azure di ripristino a cui deve essere connessa questa NIC dell'elemento protetto per il failover.</span><span class="sxs-lookup"><span data-stu-id="dc131-169">Specifies the name of the subnet on the recovery Azure virtual network to which this NIC of the protected item should be connected to on failover.</span></span>

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

### <span data-ttu-id="dc131-170">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="dc131-170">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="dc131-171">Specifica l'ID risorsa del gruppo di posizionamento di prossimità di ripristino a cui eseguire il failover della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dc131-171">Specifies the Resource Id of the recovery proximity placement group to failover teh virtual machine to.</span></span>

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

### <span data-ttu-id="dc131-172">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="dc131-172">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="dc131-173">Specifica l'ID della risorsa indirizzo IP pubblico da associare alla NIC di ripristino.</span><span class="sxs-lookup"><span data-stu-id="dc131-173">Specifies the ID of the public IP address resource to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="dc131-174">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="dc131-174">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="dc131-175">ID del gruppo di risorse Azure nell'area di ripristino in cui verrà recuperato l'elemento protetto in failover.</span><span class="sxs-lookup"><span data-stu-id="dc131-175">The ID of the Azure resource group in the recovery region in which the protected item will be recovered on failover.</span></span>

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

### <span data-ttu-id="dc131-176">-Dimensione</span><span class="sxs-lookup"><span data-stu-id="dc131-176">-Size</span></span>
<span data-ttu-id="dc131-177">Specifica la dimensione della macchina virtuale di ripristino.</span><span class="sxs-lookup"><span data-stu-id="dc131-177">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="dc131-178">Il valore deve essere del set di dimensioni supportate da macchine virtuali di Azure.</span><span class="sxs-lookup"><span data-stu-id="dc131-178">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

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

### <span data-ttu-id="dc131-179">-TfoAzureVMName</span><span class="sxs-lookup"><span data-stu-id="dc131-179">-TfoAzureVMName</span></span>
<span data-ttu-id="dc131-180">Specifica il nome della VM di failover di test.</span><span class="sxs-lookup"><span data-stu-id="dc131-180">Specifies the name of the test failover VM.</span></span>

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

### <span data-ttu-id="dc131-181">-UpdateNic</span><span class="sxs-lookup"><span data-stu-id="dc131-181">-UpdateNic</span></span>
<span data-ttu-id="dc131-182">Specifica la scheda NIC della macchina virtuale per cui questo cmdlet imposta la proprietà di rete di ripristino deve udpated.</span><span class="sxs-lookup"><span data-stu-id="dc131-182">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property needs to udpated.</span></span>

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

### <span data-ttu-id="dc131-183">-UseManagedDisk</span><span class="sxs-lookup"><span data-stu-id="dc131-183">-UseManagedDisk</span></span>
<span data-ttu-id="dc131-184">Specifica se la macchina virtuale di Azure creata in failover deve usare i dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="dc131-184">Specifies if the Azure virtual machine that is created on failover should use managed disks.</span></span>

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

### <span data-ttu-id="dc131-185">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dc131-185">-Confirm</span></span>
<span data-ttu-id="dc131-186">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc131-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc131-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc131-187">-WhatIf</span></span>
<span data-ttu-id="dc131-188">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dc131-188">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dc131-189">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dc131-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc131-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc131-190">CommonParameters</span></span>
<span data-ttu-id="dc131-191">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc131-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc131-192">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dc131-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc131-193">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dc131-193">INPUTS</span></span>

### <span data-ttu-id="dc131-194">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="dc131-194">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="dc131-195">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dc131-195">OUTPUTS</span></span>

### <span data-ttu-id="dc131-196">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="dc131-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="dc131-197">Note</span><span class="sxs-lookup"><span data-stu-id="dc131-197">NOTES</span></span>

## <span data-ttu-id="dc131-198">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dc131-198">RELATED LINKS</span></span>

[<span data-ttu-id="dc131-199">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="dc131-199">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="dc131-200">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="dc131-200">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="dc131-201">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="dc131-201">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)
