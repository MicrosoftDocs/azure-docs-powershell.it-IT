---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: 4b262b219c479cc2c56311c54d41eb05e2eb866d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477620"
---
# <span data-ttu-id="77539-101">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="77539-101">Update-AzVmss</span></span>

## <span data-ttu-id="77539-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="77539-102">SYNOPSIS</span></span>
<span data-ttu-id="77539-103">Aggiorna lo stato di un VMSS.</span><span class="sxs-lookup"><span data-stu-id="77539-103">Updates the state of a VMSS.</span></span>

## <span data-ttu-id="77539-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="77539-104">SYNTAX</span></span>

### <span data-ttu-id="77539-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="77539-105">DefaultParameter (Default)</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-AutomaticRepairGracePeriod <String>] [-BootDiagnosticsEnabled <Boolean>]
 [-BootDiagnosticsStorageUri <String>] [-CustomData <String>] [-DisableAutoRollback <Boolean>]
 [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticRepair <Boolean>]
 [-EnableAutomaticUpdate <Boolean>] [-ImageReferenceId <String>] [-ImageReferenceOffer <String>]
 [-ImageReferencePublisher <String>] [-ImageReferenceSku <String>] [-ImageReferenceVersion <String>]
 [-ImageUri <String>] [-LicenseType <String>] [-ManagedDiskStorageAccountType <String>]
 [-MaxBatchInstancePercent <Int32>] [-MaxPrice <Double>] [-MaxUnhealthyInstancePercent <Int32>]
 [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-OsDiskCaching <CachingTypes>]
 [-OsDiskWriteAccelerator <Boolean>] [-Overprovision <Boolean>] [-PauseTimeBetweenBatches <String>]
 [-PlanName <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>] [-PlanPublisher <String>]
 [-ProvisionVMAgent <Boolean>] [-ProximityPlacementGroupId <String>] [-ScaleInPolicy <String[]>]
 [-SinglePlacementGroup <Boolean>] [-SkipExtensionsOnOverprovisionedVMs <Boolean>] [-SkuCapacity <Int32>]
 [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-TerminateScheduledEvents <Boolean>]
 [-TimeZone <String>] [-UltraSSDEnabled <Boolean>] [-UpgradePolicyMode <UpgradeMode>]
 [-VhdContainer <String[]>] [-AsJob] [-EncryptionAtHost <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77539-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="77539-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-AutomaticRepairGracePeriod <String>] [-BootDiagnosticsEnabled <Boolean>]
 [-BootDiagnosticsStorageUri <String>] [-CustomData <String>] [-DisableAutoRollback <Boolean>]
 [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticRepair <Boolean>]
 [-EnableAutomaticUpdate <Boolean>] [-IdentityId <String[]>] -IdentityType <ResourceIdentityType>
 [-ImageReferenceId <String>] [-ImageReferenceOffer <String>] [-ImageReferencePublisher <String>]
 [-ImageReferenceSku <String>] [-ImageReferenceVersion <String>] [-ImageUri <String>] [-LicenseType <String>]
 [-ManagedDiskStorageAccountType <String>] [-MaxBatchInstancePercent <Int32>] [-MaxPrice <Double>]
 [-MaxUnhealthyInstancePercent <Int32>] [-MaxUnhealthyUpgradedInstancePercent <Int32>]
 [-OsDiskCaching <CachingTypes>] [-OsDiskWriteAccelerator <Boolean>] [-Overprovision <Boolean>]
 [-PauseTimeBetweenBatches <String>] [-PlanName <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>] [-ProximityPlacementGroupId <String>]
 [-ScaleInPolicy <String[]>] [-SinglePlacementGroup <Boolean>] [-SkipExtensionsOnOverprovisionedVMs <Boolean>]
 [-SkuCapacity <Int32>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-TerminateScheduledEvents <Boolean>]
 [-TimeZone <String>] [-UltraSSDEnabled <Boolean>] [-UpgradePolicyMode <UpgradeMode>]
 [-VhdContainer <String[]>] [-AsJob] [-EncryptionAtHost <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77539-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="77539-107">DESCRIPTION</span></span>
<span data-ttu-id="77539-108">Il cmdlet **Update-AzVmss** aggiorna lo stato di un set di scale della macchina virtuale (VMSS) allo stato di un oggetto vmss locale.</span><span class="sxs-lookup"><span data-stu-id="77539-108">The **Update-AzVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="77539-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="77539-109">EXAMPLES</span></span>

### <span data-ttu-id="77539-110">Esempio 1: aggiornare lo stato di un VMSS allo stato di un oggetto VMSS locale.</span><span class="sxs-lookup"><span data-stu-id="77539-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="77539-111">Questo comando Aggiorna lo stato del VMSS denominato VMSS001 che appartiene al gruppo di risorse denominato Group001 allo stato di un oggetto VMSS locale, $LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="77539-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="77539-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="77539-112">PARAMETERS</span></span>

### <span data-ttu-id="77539-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="77539-113">-AsJob</span></span>
<span data-ttu-id="77539-114">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="77539-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="77539-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="77539-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="77539-116">Imposta se gli aggiornamenti del sistema operativo devono essere applicati automaticamente alle istanze del set di scala in modo scorrevole quando una versione più recente dell'immagine diventa disponibile.</span><span class="sxs-lookup"><span data-stu-id="77539-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77539-117">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="77539-117">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="77539-118">La quantità di tempo per cui vengono sospese le riparazioni automatiche a causa di una modifica dello stato in VM.</span><span class="sxs-lookup"><span data-stu-id="77539-118">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="77539-119">Il tempo di grazia viene avviato dopo il completamento della modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="77539-119">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="77539-120">Questo consente di evitare riparazioni premature o accidentali.</span><span class="sxs-lookup"><span data-stu-id="77539-120">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="77539-121">La durata dell'ora deve essere specificata nel formato ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="77539-121">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="77539-122">Il periodo di tolleranza minimo consentito è di 30 minuti (PT30M), che è anche il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="77539-122">The minimum allowed grace period is 30 minutes (PT30M), which is also the default value.</span></span> <span data-ttu-id="77539-123">Il periodo di tolleranza massimo consentito è di 90 minuti (PT90M).</span><span class="sxs-lookup"><span data-stu-id="77539-123">The maximum allowed grace period is 90 minutes (PT90M).</span></span>

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

### <span data-ttu-id="77539-124">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="77539-124">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="77539-125">Se la diagnostica di avvio deve essere abilitata nel set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="77539-125">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77539-126">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="77539-126">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="77539-127">URI dell'account di archiviazione da usare per posizionare l'output e la schermata della console.</span><span class="sxs-lookup"><span data-stu-id="77539-127">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="77539-128">-CustomData</span><span class="sxs-lookup"><span data-stu-id="77539-128">-CustomData</span></span>
<span data-ttu-id="77539-129">Specifica una stringa codificata di base-64 di dati personalizzati.</span><span class="sxs-lookup"><span data-stu-id="77539-129">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="77539-130">Questa operazione viene decodificata in una matrice binaria che viene salvata come file nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="77539-130">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="77539-131">La lunghezza massima della matrice binaria è di 65535 byte.</span><span class="sxs-lookup"><span data-stu-id="77539-131">The maximum length of the binary array is 65535 bytes.</span></span> <br>
<span data-ttu-id="77539-132">Per usare cloud-init per la tua VM, Vedi [uso di cloud-init per personalizzare una VM di Linux durante la creazione](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="77539-132">For using cloud-init for your VM, see [Using cloud-init to customize a Linux VM during creation](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span>

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

### <span data-ttu-id="77539-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77539-133">-DefaultProfile</span></span>
<span data-ttu-id="77539-134">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="77539-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77539-135">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="77539-135">-DisableAutoRollback</span></span>
<span data-ttu-id="77539-136">Disabilitare il rollback automatico per i criteri di aggiornamento del sistema operativo automatico</span><span class="sxs-lookup"><span data-stu-id="77539-136">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77539-137">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="77539-137">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="77539-138">Indica che questo cmdlet disabilita l'autenticazione tramite password per il sistema operativo Linux.</span><span class="sxs-lookup"><span data-stu-id="77539-138">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77539-139">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="77539-139">-EnableAutomaticRepair</span></span>
<span data-ttu-id="77539-140">Abilitare o disabilitare le riparazioni automatiche nel set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="77539-140">Enable or disable automatic repairs on the virtual machine scale set.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77539-141">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="77539-141">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="77539-142">Indica se le macchine virtuali Windows in VMSS sono abilitate per gli aggiornamenti automatici.</span><span class="sxs-lookup"><span data-stu-id="77539-142">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77539-143">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="77539-143">-EncryptionAtHost</span></span>
<span data-ttu-id="77539-144">Questo parametro può essere usato dall'utente nella richiesta per abilitare o disabilitare la crittografia host per il set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="77539-144">This parameter can be used by user in the request to enable or disable the Host Encryption for the virtual machine scale set.</span></span> 

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77539-145">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="77539-145">-IdentityId</span></span>
<span data-ttu-id="77539-146">Specifica l'elenco delle identità utente associate al set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="77539-146">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="77539-147">I riferimenti di identità utente saranno ID delle risorse ARM nella forma:'/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="77539-147">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77539-148">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="77539-148">-IdentityType</span></span>
<span data-ttu-id="77539-149">Specifica il tipo di identità usato per il set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="77539-149">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="77539-150">Il tipo ' SystemAssignedUserAssigned ' include sia un'identità creata in modo implicito che un set di identità assegnate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="77539-150">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="77539-151">Il tipo "None" rimuoverà le identità dal set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="77539-151">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="77539-152">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="77539-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="77539-153">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="77539-153">SystemAssigned</span></span>
- <span data-ttu-id="77539-154">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="77539-154">UserAssigned</span></span>
- <span data-ttu-id="77539-155">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="77539-155">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="77539-156">Nessuno</span><span class="sxs-lookup"><span data-stu-id="77539-156">None</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77539-157">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="77539-157">-ImageReferenceId</span></span>
<span data-ttu-id="77539-158">Specifica l'ID riferimento immagine.</span><span class="sxs-lookup"><span data-stu-id="77539-158">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="77539-159">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="77539-159">-ImageReferenceOffer</span></span>
<span data-ttu-id="77539-160">Specifica il tipo di offerta VMImage (Virtual Machine Image).</span><span class="sxs-lookup"><span data-stu-id="77539-160">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="77539-161">Per ottenere un'offerta di immagine, usare il cmdlet Get-AzVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="77539-161">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="77539-162">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="77539-162">-ImageReferencePublisher</span></span>
<span data-ttu-id="77539-163">Specifica il nome di un autore di un VMImage.</span><span class="sxs-lookup"><span data-stu-id="77539-163">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="77539-164">Per ottenere un autore, usare il cmdlet Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="77539-164">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="77539-165">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="77539-165">-ImageReferenceSku</span></span>
<span data-ttu-id="77539-166">Specifica la SKU VMImage.</span><span class="sxs-lookup"><span data-stu-id="77539-166">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="77539-167">Per ottenere SKU, usare il cmdlet Get-AzVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="77539-167">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="77539-168">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="77539-168">-ImageReferenceVersion</span></span>
<span data-ttu-id="77539-169">Specifica la versione di VMImage.</span><span class="sxs-lookup"><span data-stu-id="77539-169">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="77539-170">Per usare la versione più recente, specificare il valore più recente invece di una determinata versione.</span><span class="sxs-lookup"><span data-stu-id="77539-170">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="77539-171">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="77539-171">-ImageUri</span></span>
<span data-ttu-id="77539-172">Specifica l'URI BLOB per l'immagine utente.</span><span class="sxs-lookup"><span data-stu-id="77539-172">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="77539-173">VMSS crea un disco del sistema operativo nello stesso contenitore dell'immagine utente.</span><span class="sxs-lookup"><span data-stu-id="77539-173">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="77539-174">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="77539-174">-LicenseType</span></span>
<span data-ttu-id="77539-175">Specificare il tipo di licenza, che è per portare il proprio scenario di licenza.</span><span class="sxs-lookup"><span data-stu-id="77539-175">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="77539-176">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="77539-176">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="77539-177">Specifica il tipo di account di archiviazione per il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="77539-177">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="77539-178">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="77539-178">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="77539-179">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="77539-179">StandardLRS</span></span>
- <span data-ttu-id="77539-180">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="77539-180">PremiumLRS</span></span>

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

### <span data-ttu-id="77539-181">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="77539-181">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="77539-182">Percentuale massima delle istanze totali della macchina virtuale che verranno aggiornate simultaneamente dall'aggiornamento a rotazione in un unico batch.</span><span class="sxs-lookup"><span data-stu-id="77539-182">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="77539-183">Poiché si tratta di un massimo, le istanze non sane nei batch precedenti o futuri possono causare una diminuzione della percentuale di istanze in un batch per garantire maggiore affidabilità.</span><span class="sxs-lookup"><span data-stu-id="77539-183">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="77539-184">Se il valore non è specificato, viene impostato su 20.</span><span class="sxs-lookup"><span data-stu-id="77539-184">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77539-185">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="77539-185">-MaxPrice</span></span>
<span data-ttu-id="77539-186">Specifica il prezzo massimo che si vuole pagare per una VM/VMSS a priorità bassa.</span><span class="sxs-lookup"><span data-stu-id="77539-186">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="77539-187">Questo prezzo è in dollari USA.</span><span class="sxs-lookup"><span data-stu-id="77539-187">This price is in US Dollars.</span></span> <span data-ttu-id="77539-188">Questo prezzo verrà confrontato con il prezzo corrente con priorità bassa per le dimensioni della VM.</span><span class="sxs-lookup"><span data-stu-id="77539-188">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="77539-189">Inoltre, i prezzi vengono confrontati al momento della creazione/aggiornamento della priorità bassa VM/VMSS e l'operazione avrà esito positivo solo se maxPrice è maggiore del prezzo corrente con priorità bassa.</span><span class="sxs-lookup"><span data-stu-id="77539-189">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="77539-190">Il maxPrice verrà usato anche per rimuovere una VM/VMSS a priorità bassa se il prezzo corrente con priorità bassa supera il maxPrice dopo la creazione di VM/VMSS.</span><span class="sxs-lookup"><span data-stu-id="77539-190">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="77539-191">I valori possibili sono: qualsiasi valore decimale maggiore di zero.</span><span class="sxs-lookup"><span data-stu-id="77539-191">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="77539-192">Esempio: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="77539-192">Example: 0.01538.</span></span>  <span data-ttu-id="77539-193">-1 indica che la priorità bassa VM/VMSS non deve essere sfrattata per motivi di prezzo.</span><span class="sxs-lookup"><span data-stu-id="77539-193">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="77539-194">Inoltre, il prezzo massimo predefinito è-1 se non è fornito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="77539-194">Also, the default max price is -1 if it is not provided by you.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77539-195">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="77539-195">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="77539-196">La percentuale massima delle istanze totali della macchina virtuale nel set di proporzioni che possono essere non sane contemporaneamente, come risultato dell'aggiornamento o per essere stati trovati in uno stato non sano dai controlli di integrità della macchina virtuale prima dell'interruzione dell'aggiornamento a rotazione.</span><span class="sxs-lookup"><span data-stu-id="77539-196">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="77539-197">Questo vincolo verrà controllato prima di iniziare qualsiasi batch.</span><span class="sxs-lookup"><span data-stu-id="77539-197">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="77539-198">Se il valore non è specificato, viene impostato su 20.</span><span class="sxs-lookup"><span data-stu-id="77539-198">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77539-199">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="77539-199">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="77539-200">La percentuale massima delle istanze di macchine virtuali aggiornate che possono essere trovate in uno stato non sano.</span><span class="sxs-lookup"><span data-stu-id="77539-200">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="77539-201">Questo controllo avverrà dopo l'aggiornamento di ogni batch.</span><span class="sxs-lookup"><span data-stu-id="77539-201">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="77539-202">Se questa percentuale viene mai superata, l'aggiornamento a rotazione viene interrotto.</span><span class="sxs-lookup"><span data-stu-id="77539-202">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="77539-203">Se il valore non è specificato, viene impostato su 20.</span><span class="sxs-lookup"><span data-stu-id="77539-203">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77539-204">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="77539-204">-OsDiskCaching</span></span>
<span data-ttu-id="77539-205">Specifica la modalità di memorizzazione nella cache del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="77539-205">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="77539-206">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="77539-206">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="77539-207">Nessuno</span><span class="sxs-lookup"><span data-stu-id="77539-207">None</span></span>
- <span data-ttu-id="77539-208">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="77539-208">ReadOnly</span></span>
- <span data-ttu-id="77539-209">ReadWrite il valore predefinito è ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="77539-209">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="77539-210">Se si modifica il valore di memorizzazione nella cache, il cmdlet riavvia la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="77539-210">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="77539-211">Questa impostazione influenza la coerenza e le prestazioni del disco.</span><span class="sxs-lookup"><span data-stu-id="77539-211">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77539-212">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="77539-212">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="77539-213">Specifica se WriteAccelerator deve essere abilitato o disabilitato nel disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="77539-213">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77539-214">-Provisioning</span><span class="sxs-lookup"><span data-stu-id="77539-214">-Overprovision</span></span>
<span data-ttu-id="77539-215">Indica se il cmdlet viene sovradisposto da VMSS.</span><span class="sxs-lookup"><span data-stu-id="77539-215">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77539-216">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="77539-216">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="77539-217">Il tempo di attesa tra il completamento dell'aggiornamento per tutte le macchine virtuali in un unico batch e l'avvio del batch successivo.</span><span class="sxs-lookup"><span data-stu-id="77539-217">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="77539-218">La durata dell'ora deve essere specificata nel formato ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="77539-218">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="77539-219">Il valore predefinito è 0 secondi (PT0S).</span><span class="sxs-lookup"><span data-stu-id="77539-219">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="77539-220">-PlanName</span><span class="sxs-lookup"><span data-stu-id="77539-220">-PlanName</span></span>
<span data-ttu-id="77539-221">Specifica il nome del piano.</span><span class="sxs-lookup"><span data-stu-id="77539-221">Specifies the plan name.</span></span>

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

### <span data-ttu-id="77539-222">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="77539-222">-PlanProduct</span></span>
<span data-ttu-id="77539-223">Specifica il prodotto piano.</span><span class="sxs-lookup"><span data-stu-id="77539-223">Specifies the plan product.</span></span>

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

### <span data-ttu-id="77539-224">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="77539-224">-PlanPromotionCode</span></span>
<span data-ttu-id="77539-225">Specifica il codice promozionale per il piano.</span><span class="sxs-lookup"><span data-stu-id="77539-225">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="77539-226">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="77539-226">-PlanPublisher</span></span>
<span data-ttu-id="77539-227">Specifica il piano Publisher.</span><span class="sxs-lookup"><span data-stu-id="77539-227">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="77539-228">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="77539-228">-ProvisionVMAgent</span></span>
<span data-ttu-id="77539-229">Indica se l'agente macchina virtuale deve essere eseguito il provisioning nelle macchine virtuali di Windows in VMSS.</span><span class="sxs-lookup"><span data-stu-id="77539-229">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77539-230">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="77539-230">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="77539-231">ID risorsa del gruppo di posizionamento di prossimità da usare con questo set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="77539-231">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="77539-232">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77539-232">-ResourceGroupName</span></span>
<span data-ttu-id="77539-233">Specifica il nome del gruppo di risorse a cui appartiene VMSS.</span><span class="sxs-lookup"><span data-stu-id="77539-233">Specifies the name of the resource group the VMSS belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77539-234">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="77539-234">-ScaleInPolicy</span></span>
<span data-ttu-id="77539-235">Regole da seguire durante la scalabilità in una scala macchina virtuale impostata.</span><span class="sxs-lookup"><span data-stu-id="77539-235">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="77539-236">I valori possibili sono: "default", "OldestVM" e "NewestVM".</span><span class="sxs-lookup"><span data-stu-id="77539-236">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="77539-237">"Impostazione predefinita" quando un set di scale di una macchina virtuale viene ridimensionato, il set di proporzioni sarà prima di tutto bilanciato tra le zone se si tratta di un set di scala zonale.</span><span class="sxs-lookup"><span data-stu-id="77539-237">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="77539-238">Verrà quindi bilanciato tra i domini di errore il più lontano possibile.</span><span class="sxs-lookup"><span data-stu-id="77539-238">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="77539-239">All'interno di ogni dominio di errore, le macchine virtuali scelte per la rimozione saranno quelle più recenti che non sono protette da scale-in.</span><span class="sxs-lookup"><span data-stu-id="77539-239">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="77539-240">' OldestVM ' quando un set di scale della macchina virtuale viene ridimensionato, le macchine virtuali meno recenti che non sono protette da scale-in verranno scelte per la rimozione.</span><span class="sxs-lookup"><span data-stu-id="77539-240">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="77539-241">Per i set di scale della macchina virtuale zonale, il set di proporzioni verrà prima bilanciato tra le aree.</span><span class="sxs-lookup"><span data-stu-id="77539-241">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="77539-242">All'interno di ogni zona le macchine virtuali meno recenti che non sono protette verranno scelte per la rimozione.</span><span class="sxs-lookup"><span data-stu-id="77539-242">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="77539-243">' NewestVM ' quando un set di scale della macchina virtuale viene ridimensionato, le macchine virtuali più recenti che non sono protette da scale-in verranno scelte per la rimozione.</span><span class="sxs-lookup"><span data-stu-id="77539-243">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="77539-244">Per i set di scale della macchina virtuale zonale, il set di proporzioni verrà prima bilanciato tra le aree.</span><span class="sxs-lookup"><span data-stu-id="77539-244">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="77539-245">All'interno di ogni zona le macchine virtuali più recenti che non sono protette verranno scelte per la rimozione.</span><span class="sxs-lookup"><span data-stu-id="77539-245">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

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

### <span data-ttu-id="77539-246">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="77539-246">-SinglePlacementGroup</span></span>
<span data-ttu-id="77539-247">Specifica il gruppo di posizionamento singolo.</span><span class="sxs-lookup"><span data-stu-id="77539-247">Specifies the single placement group.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77539-248">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="77539-248">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="77539-249">Specifica che le estensioni non vengono eseguite sulle VM extra provisioning.</span><span class="sxs-lookup"><span data-stu-id="77539-249">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77539-250">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="77539-250">-SkuCapacity</span></span>
<span data-ttu-id="77539-251">Specifica il numero di istanze in VMSS.</span><span class="sxs-lookup"><span data-stu-id="77539-251">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77539-252">-SkuName</span><span class="sxs-lookup"><span data-stu-id="77539-252">-SkuName</span></span>
<span data-ttu-id="77539-253">Specifica le dimensioni di tutte le istanze di VMSS.</span><span class="sxs-lookup"><span data-stu-id="77539-253">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="77539-254">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="77539-254">-SkuTier</span></span>
<span data-ttu-id="77539-255">Specifica il livello di VMSS.</span><span class="sxs-lookup"><span data-stu-id="77539-255">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="77539-256">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="77539-256">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="77539-257">Standard</span><span class="sxs-lookup"><span data-stu-id="77539-257">Standard</span></span>
- <span data-ttu-id="77539-258">Base</span><span class="sxs-lookup"><span data-stu-id="77539-258">Basic</span></span>

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

### <span data-ttu-id="77539-259">-Tag</span><span class="sxs-lookup"><span data-stu-id="77539-259">-Tag</span></span>
<span data-ttu-id="77539-260">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="77539-260">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="77539-261">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="77539-261">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77539-262">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="77539-262">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="77539-263">Intervallo di tempo configurabile (in minuti) una macchina virtuale che viene eliminata dovrà approvare l'evento di terminazione pianificata prima che l'evento venga approvato automaticamente (scaduta).</span><span class="sxs-lookup"><span data-stu-id="77539-263">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77539-264">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="77539-264">-TerminateScheduledEvents</span></span>
<span data-ttu-id="77539-265">Specifica se l'evento di terminazione pianificata è abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="77539-265">Specifies whether the Terminate Scheduled event is enabled or disabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77539-266">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="77539-266">-TimeZone</span></span>
<span data-ttu-id="77539-267">Specifica il fuso orario per il sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="77539-267">Specifies the time zone for Windows OS.</span></span> <span data-ttu-id="77539-268">ad esempio \" ora solare Pacifico \" .</span><span class="sxs-lookup"><span data-stu-id="77539-268">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="77539-269">I valori possibili possono essere [TimeZoneInfo.ID](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) valore da fusi orari restituiti da [TimeZoneInfo. GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones).</span><span class="sxs-lookup"><span data-stu-id="77539-269">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

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

### <span data-ttu-id="77539-270">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="77539-270">-UltraSSDEnabled</span></span>
<span data-ttu-id="77539-271">Il contrassegno che Abilita o Disabilita una funzionalità per avere uno o più dischi di dati gestiti con UltraSSD_LRS tipo di account di archiviazione nel set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="77539-271">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="77539-272">Dischi gestiti con tipo di account di archiviazione UltraSSD_LRS può essere aggiunto a un VMSS solo se questa proprietà è abilitata.</span><span class="sxs-lookup"><span data-stu-id="77539-272">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77539-273">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="77539-273">-UpgradePolicyMode</span></span>
<span data-ttu-id="77539-274">Specifica la modalità di aggiornamento delle macchine virtuali nel set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="77539-274">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="77539-275">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="77539-275">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="77539-276">Automatico</span><span class="sxs-lookup"><span data-stu-id="77539-276">Automatic</span></span>
- <span data-ttu-id="77539-277">Manuale</span><span class="sxs-lookup"><span data-stu-id="77539-277">Manual</span></span>
- <span data-ttu-id="77539-278">Implementazione</span><span class="sxs-lookup"><span data-stu-id="77539-278">Rolling</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.UpgradeMode
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77539-279">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="77539-279">-VhdContainer</span></span>
<span data-ttu-id="77539-280">Specifica gli URL del contenitore usati per archiviare i dischi del sistema operativo per VMSS.</span><span class="sxs-lookup"><span data-stu-id="77539-280">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="77539-281">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="77539-281">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="77539-282">Specifica un oggetto VMSS locale.</span><span class="sxs-lookup"><span data-stu-id="77539-282">Specifies a local VMSS object.</span></span>
<span data-ttu-id="77539-283">Per ottenere un oggetto VMSS, usa il cmdlet Get-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="77539-283">To obtain a VMSS object, use the Get-AzVmss cmdlet.</span></span>
<span data-ttu-id="77539-284">Questo oggetto macchina virtuale contiene lo stato aggiornato per VMSS.</span><span class="sxs-lookup"><span data-stu-id="77539-284">This virtual machine object contains the updated state for the VMSS.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77539-285">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="77539-285">-VMScaleSetName</span></span>
<span data-ttu-id="77539-286">Specifica il nome della VMSS creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77539-286">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77539-287">-Confermare</span><span class="sxs-lookup"><span data-stu-id="77539-287">-Confirm</span></span>
<span data-ttu-id="77539-288">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77539-288">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77539-289">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77539-289">-WhatIf</span></span>
<span data-ttu-id="77539-290">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="77539-290">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77539-291">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="77539-291">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77539-292">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77539-292">CommonParameters</span></span>
<span data-ttu-id="77539-293">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77539-293">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77539-294">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77539-294">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77539-295">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="77539-295">INPUTS</span></span>

### <span data-ttu-id="77539-296">System. String</span><span class="sxs-lookup"><span data-stu-id="77539-296">System.String</span></span>

### <span data-ttu-id="77539-297">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="77539-297">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="77539-298">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="77539-298">System.Boolean</span></span>

## <span data-ttu-id="77539-299">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="77539-299">OUTPUTS</span></span>

### <span data-ttu-id="77539-300">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="77539-300">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="77539-301">Note</span><span class="sxs-lookup"><span data-stu-id="77539-301">NOTES</span></span>

## <span data-ttu-id="77539-302">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="77539-302">RELATED LINKS</span></span>

[<span data-ttu-id="77539-303">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="77539-303">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="77539-304">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="77539-304">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="77539-305">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="77539-305">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="77539-306">Riavviare-AzVmss</span><span class="sxs-lookup"><span data-stu-id="77539-306">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="77539-307">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="77539-307">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="77539-308">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="77539-308">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="77539-309">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="77539-309">Stop-AzVmss</span></span>](./Stop-AzVmss.md)


