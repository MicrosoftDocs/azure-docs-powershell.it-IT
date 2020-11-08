---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: 3c22f34b1dc4e01cf4e3ea2f2b3f9c6045197734
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018252"
---
# <span data-ttu-id="42aec-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="42aec-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="42aec-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="42aec-102">SYNOPSIS</span></span>
<span data-ttu-id="42aec-103">Crea un oggetto di configurazione VMSS.</span><span class="sxs-lookup"><span data-stu-id="42aec-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="42aec-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="42aec-104">SYNTAX</span></span>

### <span data-ttu-id="42aec-105">DefaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="42aec-105">DefaultParameterSet (Default)</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutomaticRepairMaxInstanceRepairsPercent <Int32>] [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>]
 [-EnableUltraSSD] [-HealthProbeId <String>] [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-TerminateScheduledEvents]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-ProximityPlacementGroupId <String>]
 [-ScaleInPolicy <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="42aec-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="42aec-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutomaticRepairMaxInstanceRepairsPercent <Int32>] [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>]
 [-EnableUltraSSD] [-HealthProbeId <String>] [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-TerminateScheduledEvents]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-ProximityPlacementGroupId <String>]
 [-ScaleInPolicy <String[]>] -IdentityType <ResourceIdentityType> [-IdentityId <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42aec-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="42aec-107">AssignIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutomaticRepairMaxInstanceRepairsPercent <Int32>] [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>]
 [-EnableUltraSSD] [-HealthProbeId <String>] [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-TerminateScheduledEvents]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-ProximityPlacementGroupId <String>]
 [-ScaleInPolicy <String[]>] [-AssignIdentity] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="42aec-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="42aec-108">DESCRIPTION</span></span>
<span data-ttu-id="42aec-109">Il cmdlet **New-AzVmssConfig** crea un oggetto vmss (Virtual Manager scale set) configurabile.</span><span class="sxs-lookup"><span data-stu-id="42aec-109">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="42aec-110">Altri cmdlet sono necessari per configurare l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="42aec-110">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="42aec-111">Questi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="42aec-111">These cmdlets are:</span></span>
- <span data-ttu-id="42aec-112">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="42aec-112">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="42aec-113">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="42aec-113">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="42aec-114">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="42aec-114">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="42aec-115">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="42aec-115">Add-AzVmssExtension</span></span>

## <span data-ttu-id="42aec-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="42aec-116">EXAMPLES</span></span>

### <span data-ttu-id="42aec-117">Esempio 1: creare un oggetto di configurazione VMSS</span><span class="sxs-lookup"><span data-stu-id="42aec-117">Example 1: Create a VMSS configuration object</span></span>
```
PS C:\> $VMSS = New-AzVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic" -NetworkInterfaceConfiguration $NetCfg `
            | Add-AzVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
            | Set-AzVmssOSProfile -ComputerNamePrefix "Test" -AdminUsername $adminUsername -AdminPassword $AdminPassword `
            | Set-AzVmssStorageProfile -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VHDContainer `
            | Add-AzVmssAdditionalUnattendContent -ComponentName  $AUCComponentName -Content  $AUCContent -PassName  $AUCPassName -SettingName  $AUCSetting `
            | Remove-AzVmssAdditionalUnattendContent -ComponentName  $AUCComponentName;

New-AzVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

<span data-ttu-id="42aec-118">Questo esempio crea un oggetto di configurazione VMSS.</span><span class="sxs-lookup"><span data-stu-id="42aec-118">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="42aec-119">Il primo comando usa il cmdlet **New-AzVmssConfig** per creare un oggetto di configurazione vmss e archivia il risultato nella variabile denominata $vmss.</span><span class="sxs-lookup"><span data-stu-id="42aec-119">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="42aec-120">Il secondo comando usa il cmdlet **New-AzVmss** per creare un vmss che usa l'oggetto di configurazione vmss creato nel primo comando.</span><span class="sxs-lookup"><span data-stu-id="42aec-120">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="42aec-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="42aec-121">PARAMETERS</span></span>

### <span data-ttu-id="42aec-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="42aec-122">-AssignIdentity</span></span>
<span data-ttu-id="42aec-123">Specifica l'identità di sistema assegnata per il set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="42aec-123">Specify the system assigned identity for the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42aec-124">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="42aec-124">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="42aec-125">La quantità di tempo per cui vengono sospese le riparazioni automatiche a causa di una modifica dello stato in VM.</span><span class="sxs-lookup"><span data-stu-id="42aec-125">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="42aec-126">Il tempo di grazia viene avviato dopo il completamento della modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="42aec-126">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="42aec-127">Questo consente di evitare riparazioni premature o accidentali.</span><span class="sxs-lookup"><span data-stu-id="42aec-127">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="42aec-128">La durata dell'ora deve essere specificata nel formato ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="42aec-128">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="42aec-129">Il valore predefinito è 5 minuti (PT5M).</span><span class="sxs-lookup"><span data-stu-id="42aec-129">The default value is 5 minutes (PT5M).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42aec-130">-AutomaticRepairMaxInstanceRepairsPercent</span><span class="sxs-lookup"><span data-stu-id="42aec-130">-AutomaticRepairMaxInstanceRepairsPercent</span></span>
<span data-ttu-id="42aec-131">Percentuale (capacità di scalet) delle macchine virtuali che verranno riparate contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="42aec-131">The percentage (capacity of scaleset) of virtual machines that will be simultaneously repaired.</span></span> <span data-ttu-id="42aec-132">Il valore predefinito è 20%.</span><span class="sxs-lookup"><span data-stu-id="42aec-132">The default value is 20%.</span></span>

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

### <span data-ttu-id="42aec-133">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="42aec-133">-AutoOSUpgrade</span></span>
<span data-ttu-id="42aec-134">Imposta se gli aggiornamenti del sistema operativo devono essere applicati automaticamente alle istanze del set di scala in modo scorrevole quando una versione più recente dell'immagine diventa disponibile.</span><span class="sxs-lookup"><span data-stu-id="42aec-134">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="42aec-135">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="42aec-135">-BootDiagnostic</span></span>
<span data-ttu-id="42aec-136">Specifica il profilo set di diagnostica di avvio della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="42aec-136">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.BootDiagnostics
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42aec-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42aec-137">-DefaultProfile</span></span>
<span data-ttu-id="42aec-138">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="42aec-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42aec-139">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="42aec-139">-DisableAutoRollback</span></span>
<span data-ttu-id="42aec-140">Disabilitare il rollback automatico per i criteri di aggiornamento del sistema operativo automatico</span><span class="sxs-lookup"><span data-stu-id="42aec-140">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="42aec-141">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="42aec-141">-EnableAutomaticRepair</span></span>
<span data-ttu-id="42aec-142">Consente la riparazione automatica nel set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="42aec-142">Enables automatic repairs on the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42aec-143">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="42aec-143">-EnableUltraSSD</span></span>
<span data-ttu-id="42aec-144">Consente a una funzionalità di avere uno o più dischi di dati gestiti con UltraSSD_LRS tipo di account di archiviazione nel set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="42aec-144">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="42aec-145">Dischi gestiti con tipo di account di archiviazione UltraSSD_LRS può essere aggiunto a un VMSS solo se questa proprietà è abilitata.</span><span class="sxs-lookup"><span data-stu-id="42aec-145">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42aec-146">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="42aec-146">-EvictionPolicy</span></span>
<span data-ttu-id="42aec-147">Specifica i criteri di eliminazione per le macchine virtuali nel set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="42aec-147">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42aec-148">-Extension</span><span class="sxs-lookup"><span data-stu-id="42aec-148">-Extension</span></span>
<span data-ttu-id="42aec-149">Specifica l'oggetto informazioni sull'estensione per VMSS.</span><span class="sxs-lookup"><span data-stu-id="42aec-149">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="42aec-150">Puoi usare il cmdlet **Add-AzVmssExtension** per aggiungere questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="42aec-150">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42aec-151">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="42aec-151">-HealthProbeId</span></span>
<span data-ttu-id="42aec-152">Specifica l'ID di un probe di bilanciamento del carico usato per determinare lo stato di un'istanza nel set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="42aec-152">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="42aec-153">HealthProbeId è sotto forma di '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span><span class="sxs-lookup"><span data-stu-id="42aec-153">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42aec-154">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="42aec-154">-IdentityId</span></span>
<span data-ttu-id="42aec-155">Specifica l'elenco delle identità utente associate al set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="42aec-155">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="42aec-156">I riferimenti di identità utente saranno ID delle risorse ARM nella forma:'/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="42aec-156">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42aec-157">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="42aec-157">-IdentityType</span></span>
<span data-ttu-id="42aec-158">Specifica il tipo di identità usato per il set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="42aec-158">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="42aec-159">Il tipo ' SystemAssignedUserAssigned ' include sia un'identità creata in modo implicito che un set di identità assegnate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="42aec-159">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="42aec-160">Il tipo "None" rimuoverà le identità dal set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="42aec-160">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="42aec-161">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="42aec-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="42aec-162">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="42aec-162">SystemAssigned</span></span>
- <span data-ttu-id="42aec-163">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="42aec-163">UserAssigned</span></span>
- <span data-ttu-id="42aec-164">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="42aec-164">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="42aec-165">Nessuno</span><span class="sxs-lookup"><span data-stu-id="42aec-165">None</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42aec-166">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="42aec-166">-LicenseType</span></span>
<span data-ttu-id="42aec-167">Specificare il tipo di licenza, che è per portare il proprio scenario di licenza.</span><span class="sxs-lookup"><span data-stu-id="42aec-167">Specify the license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42aec-168">-Posizione</span><span class="sxs-lookup"><span data-stu-id="42aec-168">-Location</span></span>
<span data-ttu-id="42aec-169">Specifica la posizione di Azure in cui viene creato VMSS.</span><span class="sxs-lookup"><span data-stu-id="42aec-169">Specifies the Azure location where the VMSS is created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42aec-170">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="42aec-170">-MaxPrice</span></span>
<span data-ttu-id="42aec-171">Specifica il prezzo massimo che si vuole pagare per una VM/VMSS a priorità bassa.</span><span class="sxs-lookup"><span data-stu-id="42aec-171">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="42aec-172">Questo prezzo è in dollari USA.</span><span class="sxs-lookup"><span data-stu-id="42aec-172">This price is in US Dollars.</span></span> <span data-ttu-id="42aec-173">Questo prezzo verrà confrontato con il prezzo corrente con priorità bassa per le dimensioni della VM.</span><span class="sxs-lookup"><span data-stu-id="42aec-173">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="42aec-174">Inoltre, i prezzi vengono confrontati al momento della creazione/aggiornamento della priorità bassa VM/VMSS e l'operazione avrà esito positivo solo se maxPrice è maggiore del prezzo corrente con priorità bassa.</span><span class="sxs-lookup"><span data-stu-id="42aec-174">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="42aec-175">Il maxPrice verrà usato anche per rimuovere una VM/VMSS a priorità bassa se il prezzo corrente con priorità bassa supera il maxPrice dopo la creazione di VM/VMSS.</span><span class="sxs-lookup"><span data-stu-id="42aec-175">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="42aec-176">I valori possibili sono: qualsiasi valore decimale maggiore di zero.</span><span class="sxs-lookup"><span data-stu-id="42aec-176">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="42aec-177">Esempio: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="42aec-177">Example: 0.01538.</span></span>  <span data-ttu-id="42aec-178">-1 indica che la priorità bassa VM/VMSS non deve essere sfrattata per motivi di prezzo.</span><span class="sxs-lookup"><span data-stu-id="42aec-178">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="42aec-179">Inoltre, il prezzo massimo predefinito è-1 se non è fornito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="42aec-179">Also, the default max price is -1 if it is not provided by you.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42aec-180">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="42aec-180">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="42aec-181">Specifica l'oggetto profilo di rete che contiene le proprietà di rete per la configurazione di VMSS.</span><span class="sxs-lookup"><span data-stu-id="42aec-181">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="42aec-182">Puoi usare il cmdlet **Add-AzVmssNetworkInterfaceConfiguration** per aggiungere questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="42aec-182">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42aec-183">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="42aec-183">-OsProfile</span></span>
<span data-ttu-id="42aec-184">Specifica l'oggetto del profilo del sistema operativo che contiene le proprietà del sistema operativo per la configurazione di VMSS.</span><span class="sxs-lookup"><span data-stu-id="42aec-184">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="42aec-185">Puoi usare il cmdlet **set-AzVmssOsProfile** per impostare questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="42aec-185">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42aec-186">-Provisioning</span><span class="sxs-lookup"><span data-stu-id="42aec-186">-Overprovision</span></span>
<span data-ttu-id="42aec-187">Indica se il cmdlet viene sovradisposto da VMSS.</span><span class="sxs-lookup"><span data-stu-id="42aec-187">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42aec-188">-PlanName</span><span class="sxs-lookup"><span data-stu-id="42aec-188">-PlanName</span></span>
<span data-ttu-id="42aec-189">Specifica il nome del piano.</span><span class="sxs-lookup"><span data-stu-id="42aec-189">Specifies the plan name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42aec-190">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="42aec-190">-PlanProduct</span></span>
<span data-ttu-id="42aec-191">Specifica il prodotto piano.</span><span class="sxs-lookup"><span data-stu-id="42aec-191">Specifies the plan product.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42aec-192">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="42aec-192">-PlanPromotionCode</span></span>
<span data-ttu-id="42aec-193">Specifica il codice promozionale per il piano.</span><span class="sxs-lookup"><span data-stu-id="42aec-193">Specifies the plan promotion code.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42aec-194">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="42aec-194">-PlanPublisher</span></span>
<span data-ttu-id="42aec-195">Specifica il piano Publisher.</span><span class="sxs-lookup"><span data-stu-id="42aec-195">Specifies the plan publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42aec-196">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="42aec-196">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="42aec-197">Conteggio dei domini di errore per ogni gruppo di posizionamento.</span><span class="sxs-lookup"><span data-stu-id="42aec-197">Fault Domain count for each placement group.</span></span>

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

### <span data-ttu-id="42aec-198">-Priorità</span><span class="sxs-lookup"><span data-stu-id="42aec-198">-Priority</span></span>
<span data-ttu-id="42aec-199">Priorità per il machio virtuale nel set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="42aec-199">The priority for the virtual machien in the scale set.</span></span>  <span data-ttu-id="42aec-200">Solo i valori supportati sono "regolari", "spot" e "low".</span><span class="sxs-lookup"><span data-stu-id="42aec-200">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="42aec-201">"Normale" è per la normale macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="42aec-201">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="42aec-202">"Spot" è per la macchina virtuale spot.</span><span class="sxs-lookup"><span data-stu-id="42aec-202">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="42aec-203">"Basso" è anche per la macchina virtuale spot, ma è sostituito da "spot".</span><span class="sxs-lookup"><span data-stu-id="42aec-203">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="42aec-204">Usare "spot" invece di "low".</span><span class="sxs-lookup"><span data-stu-id="42aec-204">Please use 'Spot' instead of 'Low'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42aec-205">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="42aec-205">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="42aec-206">ID risorsa del gruppo di posizionamento di prossimità da usare con questo set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="42aec-206">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42aec-207">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="42aec-207">-RollingUpgradePolicy</span></span>
<span data-ttu-id="42aec-208">Specifica i criteri di aggiornamento a rotazione.</span><span class="sxs-lookup"><span data-stu-id="42aec-208">Specifies the rolling upgrade policy.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42aec-209">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="42aec-209">-ScaleInPolicy</span></span>
<span data-ttu-id="42aec-210">Regole da seguire durante la scalabilità in una scala macchina virtuale impostata.</span><span class="sxs-lookup"><span data-stu-id="42aec-210">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="42aec-211">I valori possibili sono: "default", "OldestVM" e "NewestVM".</span><span class="sxs-lookup"><span data-stu-id="42aec-211">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="42aec-212">"Impostazione predefinita" quando un set di scale di una macchina virtuale viene ridimensionato, il set di proporzioni sarà prima di tutto bilanciato tra le zone se si tratta di un set di scala zonale.</span><span class="sxs-lookup"><span data-stu-id="42aec-212">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="42aec-213">Verrà quindi bilanciato tra i domini di errore il più lontano possibile.</span><span class="sxs-lookup"><span data-stu-id="42aec-213">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="42aec-214">All'interno di ogni dominio di errore, le macchine virtuali scelte per la rimozione saranno quelle più recenti che non sono protette da scale-in.</span><span class="sxs-lookup"><span data-stu-id="42aec-214">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="42aec-215">' OldestVM ' quando un set di scale della macchina virtuale viene ridimensionato, le macchine virtuali meno recenti che non sono protette da scale-in verranno scelte per la rimozione.</span><span class="sxs-lookup"><span data-stu-id="42aec-215">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="42aec-216">Per i set di scale della macchina virtuale zonale, il set di proporzioni verrà prima bilanciato tra le aree.</span><span class="sxs-lookup"><span data-stu-id="42aec-216">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="42aec-217">All'interno di ogni zona le macchine virtuali meno recenti che non sono protette verranno scelte per la rimozione.</span><span class="sxs-lookup"><span data-stu-id="42aec-217">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="42aec-218">' NewestVM ' quando un set di scale della macchina virtuale viene ridimensionato, le macchine virtuali più recenti che non sono protette da scale-in verranno scelte per la rimozione.</span><span class="sxs-lookup"><span data-stu-id="42aec-218">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="42aec-219">Per i set di scale della macchina virtuale zonale, il set di proporzioni verrà prima bilanciato tra le aree.</span><span class="sxs-lookup"><span data-stu-id="42aec-219">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="42aec-220">All'interno di ogni zona le macchine virtuali più recenti che non sono protette verranno scelte per la rimozione.</span><span class="sxs-lookup"><span data-stu-id="42aec-220">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42aec-221">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="42aec-221">-SinglePlacementGroup</span></span>
<span data-ttu-id="42aec-222">Specifica il gruppo di posizionamento singolo.</span><span class="sxs-lookup"><span data-stu-id="42aec-222">Specifies the single placement group.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42aec-223">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="42aec-223">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="42aec-224">Specifica che le estensioni non vengono eseguite sulle VM extra provisioning.</span><span class="sxs-lookup"><span data-stu-id="42aec-224">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="42aec-225">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="42aec-225">-SkuCapacity</span></span>
<span data-ttu-id="42aec-226">Specifica il numero di istanze in VMSS.</span><span class="sxs-lookup"><span data-stu-id="42aec-226">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42aec-227">-SkuName</span><span class="sxs-lookup"><span data-stu-id="42aec-227">-SkuName</span></span>
<span data-ttu-id="42aec-228">Specifica le dimensioni di tutte le istanze di VMSS.</span><span class="sxs-lookup"><span data-stu-id="42aec-228">Specifies the size of all the instances of VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42aec-229">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="42aec-229">-SkuTier</span></span>
<span data-ttu-id="42aec-230">Specifica il livello di VMSS.</span><span class="sxs-lookup"><span data-stu-id="42aec-230">Specifies the tier of VMSS.</span></span> <span data-ttu-id="42aec-231">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="42aec-231">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="42aec-232">Standard</span><span class="sxs-lookup"><span data-stu-id="42aec-232">Standard</span></span>
- <span data-ttu-id="42aec-233">Base</span><span class="sxs-lookup"><span data-stu-id="42aec-233">Basic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42aec-234">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="42aec-234">-StorageProfile</span></span>
<span data-ttu-id="42aec-235">Specifica l'oggetto profilo di archiviazione che contiene le proprietà del disco per la configurazione di VMSS.</span><span class="sxs-lookup"><span data-stu-id="42aec-235">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="42aec-236">Puoi usare il cmdlet **set-AzVmssStorageProfile** per impostare questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="42aec-236">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42aec-237">-Tag</span><span class="sxs-lookup"><span data-stu-id="42aec-237">-Tag</span></span>
<span data-ttu-id="42aec-238">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="42aec-238">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="42aec-239">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="42aec-239">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42aec-240">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="42aec-240">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="42aec-241">Intervallo di tempo configurabile (in minuti) una macchina virtuale che viene eliminata dovrà approvare l'evento di terminazione pianificata prima che l'evento venga approvato automaticamente (scaduta).</span><span class="sxs-lookup"><span data-stu-id="42aec-241">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="42aec-242">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="42aec-242">-TerminateScheduledEvents</span></span>
<span data-ttu-id="42aec-243">Abilitare gli eventi pianificati di terminazione</span><span class="sxs-lookup"><span data-stu-id="42aec-243">Enable the Terminate Scheduled events</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42aec-244">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="42aec-244">-UpgradePolicyMode</span></span>
<span data-ttu-id="42aec-245">Specifica la modalità di aggiornamento delle macchine virtuali nel set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="42aec-245">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="42aec-246">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="42aec-246">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="42aec-247">Automatico</span><span class="sxs-lookup"><span data-stu-id="42aec-247">Automatic</span></span>
- <span data-ttu-id="42aec-248">Manuale</span><span class="sxs-lookup"><span data-stu-id="42aec-248">Manual</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.UpgradeMode]
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42aec-249">-Zona</span><span class="sxs-lookup"><span data-stu-id="42aec-249">-Zone</span></span>
<span data-ttu-id="42aec-250">Specifica l'elenco delle aree per il set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="42aec-250">Specifies the zone list for the virtual machine scale set.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42aec-251">-ZoneBalance</span><span class="sxs-lookup"><span data-stu-id="42aec-251">-ZoneBalance</span></span>
<span data-ttu-id="42aec-252">Se è necessario forzare la distribuzione rigorosa della macchina virtuale tra le aree x in caso di interruzioni di zona.</span><span class="sxs-lookup"><span data-stu-id="42aec-252">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="42aec-253">-Confermare</span><span class="sxs-lookup"><span data-stu-id="42aec-253">-Confirm</span></span>
<span data-ttu-id="42aec-254">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42aec-254">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42aec-255">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42aec-255">-WhatIf</span></span>
<span data-ttu-id="42aec-256">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="42aec-256">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="42aec-257">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="42aec-257">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42aec-258">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42aec-258">CommonParameters</span></span>
<span data-ttu-id="42aec-259">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42aec-259">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42aec-260">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="42aec-260">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42aec-261">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="42aec-261">INPUTS</span></span>

### <span data-ttu-id="42aec-262">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="42aec-262">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="42aec-263">System. String</span><span class="sxs-lookup"><span data-stu-id="42aec-263">System.String</span></span>

### <span data-ttu-id="42aec-264">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="42aec-264">System.Collections.Hashtable</span></span>

### <span data-ttu-id="42aec-265">System. Int32</span><span class="sxs-lookup"><span data-stu-id="42aec-265">System.Int32</span></span>

### <span data-ttu-id="42aec-266">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. UpgradeMode, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="42aec-266">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="42aec-267">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetOSProfile</span><span class="sxs-lookup"><span data-stu-id="42aec-267">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="42aec-268">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetStorageProfile</span><span class="sxs-lookup"><span data-stu-id="42aec-268">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="42aec-269">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetNetworkConfiguration []</span><span class="sxs-lookup"><span data-stu-id="42aec-269">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="42aec-270">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetExtension []</span><span class="sxs-lookup"><span data-stu-id="42aec-270">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="42aec-271">System. String []</span><span class="sxs-lookup"><span data-stu-id="42aec-271">System.String[]</span></span>

### <span data-ttu-id="42aec-272">Microsoft. Azure. Management. Compute. Models. RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="42aec-272">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="42aec-273">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="42aec-273">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="42aec-274">Microsoft. Azure. Management. Compute. Models. BootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="42aec-274">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="42aec-275">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. ResourceIdentityType, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="42aec-275">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="42aec-276">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="42aec-276">OUTPUTS</span></span>

### <span data-ttu-id="42aec-277">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="42aec-277">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="42aec-278">Note</span><span class="sxs-lookup"><span data-stu-id="42aec-278">NOTES</span></span>

## <span data-ttu-id="42aec-279">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="42aec-279">RELATED LINKS</span></span>

[<span data-ttu-id="42aec-280">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="42aec-280">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="42aec-281">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="42aec-281">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="42aec-282">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="42aec-282">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="42aec-283">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="42aec-283">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="42aec-284">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="42aec-284">New-AzVmss</span></span>](./New-AzVmss.md)
