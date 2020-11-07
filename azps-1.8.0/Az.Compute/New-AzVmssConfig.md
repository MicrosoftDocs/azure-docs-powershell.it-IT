---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: beb9c067fb2ca625fcf756747a52eef0bf1ca9b5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684761"
---
# <span data-ttu-id="18e75-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="18e75-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="18e75-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="18e75-102">SYNOPSIS</span></span>
<span data-ttu-id="18e75-103">Crea un oggetto di configurazione VMSS.</span><span class="sxs-lookup"><span data-stu-id="18e75-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="18e75-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="18e75-104">SYNTAX</span></span>

### <span data-ttu-id="18e75-105">DefaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="18e75-105">DefaultParameterSet (Default)</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-ZoneBalance]
 [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>] [-PlanName <String>] [-PlanPublisher <String>]
 [-PlanProduct <String>] [-PlanPromotionCode <String>] [-RollingUpgradePolicy <RollingUpgradePolicy>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18e75-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="18e75-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-ZoneBalance]
 [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>] [-PlanName <String>] [-PlanPublisher <String>]
 [-PlanProduct <String>] [-PlanPromotionCode <String>] [-RollingUpgradePolicy <RollingUpgradePolicy>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18e75-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="18e75-107">AssignIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-ZoneBalance]
 [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>] [-PlanName <String>] [-PlanPublisher <String>]
 [-PlanProduct <String>] [-PlanPromotionCode <String>] [-RollingUpgradePolicy <RollingUpgradePolicy>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-AssignIdentity] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18e75-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18e75-108">DESCRIPTION</span></span>
<span data-ttu-id="18e75-109">Il cmdlet **New-AzVmssConfig** crea un oggetto vmss (Virtual Manager scale set) configurabile.</span><span class="sxs-lookup"><span data-stu-id="18e75-109">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="18e75-110">Altri cmdlet sono necessari per configurare l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="18e75-110">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="18e75-111">Questi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="18e75-111">These cmdlets are:</span></span>
- <span data-ttu-id="18e75-112">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="18e75-112">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="18e75-113">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="18e75-113">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="18e75-114">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="18e75-114">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="18e75-115">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="18e75-115">Add-AzVmssExtension</span></span>

## <span data-ttu-id="18e75-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="18e75-116">EXAMPLES</span></span>

### <span data-ttu-id="18e75-117">Esempio 1: creare un oggetto di configurazione VMSS</span><span class="sxs-lookup"><span data-stu-id="18e75-117">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="18e75-118">Questo esempio crea un oggetto di configurazione VMSS.</span><span class="sxs-lookup"><span data-stu-id="18e75-118">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="18e75-119">Il primo comando usa il cmdlet **New-AzVmssConfig** per creare un oggetto di configurazione vmss e archivia il risultato nella variabile denominata $vmss.</span><span class="sxs-lookup"><span data-stu-id="18e75-119">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="18e75-120">Il secondo comando usa il cmdlet **New-AzVmss** per creare un vmss che usa l'oggetto di configurazione vmss creato nel primo comando.</span><span class="sxs-lookup"><span data-stu-id="18e75-120">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="18e75-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="18e75-121">PARAMETERS</span></span>

### <span data-ttu-id="18e75-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="18e75-122">-AssignIdentity</span></span>
<span data-ttu-id="18e75-123">Specifica l'identità di sistema assegnata per il set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="18e75-123">Specify the system assigned identity for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="18e75-124">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="18e75-124">-AutoOSUpgrade</span></span>
<span data-ttu-id="18e75-125">Imposta se gli aggiornamenti del sistema operativo devono essere applicati automaticamente alle istanze del set di scala in modo scorrevole quando una versione più recente dell'immagine diventa disponibile.</span><span class="sxs-lookup"><span data-stu-id="18e75-125">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="18e75-126">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="18e75-126">-BootDiagnostic</span></span>
<span data-ttu-id="18e75-127">Specifica il profilo set di diagnostica di avvio della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="18e75-127">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="18e75-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18e75-128">-DefaultProfile</span></span>
<span data-ttu-id="18e75-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="18e75-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18e75-130">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="18e75-130">-DisableAutoRollback</span></span>
<span data-ttu-id="18e75-131">Disabilitare il rollback automatico per i criteri di aggiornamento del sistema operativo automatico</span><span class="sxs-lookup"><span data-stu-id="18e75-131">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="18e75-132">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="18e75-132">-EnableUltraSSD</span></span>
<span data-ttu-id="18e75-133">Consente a una funzionalità di avere uno o più dischi di dati gestiti con UltraSSD_LRS tipo di account di archiviazione nel set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="18e75-133">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="18e75-134">Dischi gestiti con tipo di account di archiviazione UltraSSD_LRS può essere aggiunto a un VMSS solo se questa proprietà è abilitata.</span><span class="sxs-lookup"><span data-stu-id="18e75-134">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="18e75-135">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="18e75-135">-EvictionPolicy</span></span>
<span data-ttu-id="18e75-136">Specifica i criteri di eliminazione per le macchine virtuali nel set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="18e75-136">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="18e75-137">-Extension</span><span class="sxs-lookup"><span data-stu-id="18e75-137">-Extension</span></span>
<span data-ttu-id="18e75-138">Specifica l'oggetto informazioni sull'estensione per VMSS.</span><span class="sxs-lookup"><span data-stu-id="18e75-138">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="18e75-139">Puoi usare il cmdlet **Add-AzVmssExtension** per aggiungere questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="18e75-139">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18e75-140">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="18e75-140">-HealthProbeId</span></span>
<span data-ttu-id="18e75-141">Specifica l'ID di un probe di bilanciamento del carico usato per determinare lo stato di un'istanza nel set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="18e75-141">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="18e75-142">HealthProbeId è sotto forma di '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span><span class="sxs-lookup"><span data-stu-id="18e75-142">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="18e75-143">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="18e75-143">-IdentityId</span></span>
<span data-ttu-id="18e75-144">Specifica l'elenco delle identità utente associate al set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="18e75-144">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="18e75-145">I riferimenti di identità utente saranno ID delle risorse ARM nella forma:'/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="18e75-145">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="18e75-146">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="18e75-146">-IdentityType</span></span>
<span data-ttu-id="18e75-147">Specifica il tipo di identità usato per il set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="18e75-147">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="18e75-148">Il tipo ' SystemAssignedUserAssigned ' include sia un'identità creata in modo implicito che un set di identità assegnate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="18e75-148">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="18e75-149">Il tipo "None" rimuoverà le identità dal set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="18e75-149">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="18e75-150">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="18e75-150">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="18e75-151">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="18e75-151">SystemAssigned</span></span>
- <span data-ttu-id="18e75-152">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="18e75-152">UserAssigned</span></span>
- <span data-ttu-id="18e75-153">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="18e75-153">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="18e75-154">Nessuno</span><span class="sxs-lookup"><span data-stu-id="18e75-154">None</span></span>

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

### <span data-ttu-id="18e75-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="18e75-155">-LicenseType</span></span>
<span data-ttu-id="18e75-156">Specificare il tipo di licenza, che è per portare il proprio scenario di licenza.</span><span class="sxs-lookup"><span data-stu-id="18e75-156">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="18e75-157">-Posizione</span><span class="sxs-lookup"><span data-stu-id="18e75-157">-Location</span></span>
<span data-ttu-id="18e75-158">Specifica la posizione di Azure in cui viene creato VMSS.</span><span class="sxs-lookup"><span data-stu-id="18e75-158">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="18e75-159">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="18e75-159">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="18e75-160">Specifica l'oggetto profilo di rete che contiene le proprietà di rete per la configurazione di VMSS.</span><span class="sxs-lookup"><span data-stu-id="18e75-160">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="18e75-161">Puoi usare il cmdlet **Add-AzVmssNetworkInterfaceConfiguration** per aggiungere questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="18e75-161">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="18e75-162">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="18e75-162">-OsProfile</span></span>
<span data-ttu-id="18e75-163">Specifica l'oggetto del profilo del sistema operativo che contiene le proprietà del sistema operativo per la configurazione di VMSS.</span><span class="sxs-lookup"><span data-stu-id="18e75-163">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="18e75-164">Puoi usare il cmdlet **set-AzVmssOsProfile** per impostare questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="18e75-164">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="18e75-165">-Provisioning</span><span class="sxs-lookup"><span data-stu-id="18e75-165">-Overprovision</span></span>
<span data-ttu-id="18e75-166">Indica se il cmdlet viene sovradisposto da VMSS.</span><span class="sxs-lookup"><span data-stu-id="18e75-166">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="18e75-167">-PlanName</span><span class="sxs-lookup"><span data-stu-id="18e75-167">-PlanName</span></span>
<span data-ttu-id="18e75-168">Specifica il nome del piano.</span><span class="sxs-lookup"><span data-stu-id="18e75-168">Specifies the plan name.</span></span>

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

### <span data-ttu-id="18e75-169">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="18e75-169">-PlanProduct</span></span>
<span data-ttu-id="18e75-170">Specifica il prodotto piano.</span><span class="sxs-lookup"><span data-stu-id="18e75-170">Specifies the plan product.</span></span>

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

### <span data-ttu-id="18e75-171">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="18e75-171">-PlanPromotionCode</span></span>
<span data-ttu-id="18e75-172">Specifica il codice promozionale per il piano.</span><span class="sxs-lookup"><span data-stu-id="18e75-172">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="18e75-173">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="18e75-173">-PlanPublisher</span></span>
<span data-ttu-id="18e75-174">Specifica il piano Publisher.</span><span class="sxs-lookup"><span data-stu-id="18e75-174">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="18e75-175">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="18e75-175">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="18e75-176">Conteggio dei domini di errore per ogni gruppo di posizionamento.</span><span class="sxs-lookup"><span data-stu-id="18e75-176">Fault Domain count for each placement group.</span></span>

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

### <span data-ttu-id="18e75-177">-Priorità</span><span class="sxs-lookup"><span data-stu-id="18e75-177">-Priority</span></span>
<span data-ttu-id="18e75-178">Specifica la priorità per le macchine virtuali nel set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="18e75-178">Specifies the priority for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="18e75-179">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="18e75-179">-RollingUpgradePolicy</span></span>
<span data-ttu-id="18e75-180">Specifica i criteri di aggiornamento a rotazione.</span><span class="sxs-lookup"><span data-stu-id="18e75-180">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="18e75-181">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="18e75-181">-SinglePlacementGroup</span></span>
<span data-ttu-id="18e75-182">Specifica il gruppo di posizionamento singolo.</span><span class="sxs-lookup"><span data-stu-id="18e75-182">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="18e75-183">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="18e75-183">-SkuCapacity</span></span>
<span data-ttu-id="18e75-184">Specifica il numero di istanze in VMSS.</span><span class="sxs-lookup"><span data-stu-id="18e75-184">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="18e75-185">-SkuName</span><span class="sxs-lookup"><span data-stu-id="18e75-185">-SkuName</span></span>
<span data-ttu-id="18e75-186">Specifica le dimensioni di tutte le istanze di VMSS.</span><span class="sxs-lookup"><span data-stu-id="18e75-186">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="18e75-187">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="18e75-187">-SkuTier</span></span>
<span data-ttu-id="18e75-188">Specifica il livello di VMSS.</span><span class="sxs-lookup"><span data-stu-id="18e75-188">Specifies the tier of VMSS.</span></span> <span data-ttu-id="18e75-189">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="18e75-189">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="18e75-190">Standard</span><span class="sxs-lookup"><span data-stu-id="18e75-190">Standard</span></span>
- <span data-ttu-id="18e75-191">Base</span><span class="sxs-lookup"><span data-stu-id="18e75-191">Basic</span></span>

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

### <span data-ttu-id="18e75-192">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="18e75-192">-StorageProfile</span></span>
<span data-ttu-id="18e75-193">Specifica l'oggetto profilo di archiviazione che contiene le proprietà del disco per la configurazione di VMSS.</span><span class="sxs-lookup"><span data-stu-id="18e75-193">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="18e75-194">Puoi usare il cmdlet **set-AzVmssStorageProfile** per impostare questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="18e75-194">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="18e75-195">-Tag</span><span class="sxs-lookup"><span data-stu-id="18e75-195">-Tag</span></span>
<span data-ttu-id="18e75-196">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="18e75-196">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="18e75-197">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="18e75-197">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="18e75-198">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="18e75-198">-UpgradePolicyMode</span></span>
<span data-ttu-id="18e75-199">Specifica la modalità di aggiornamento delle macchine virtuali nel set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="18e75-199">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="18e75-200">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="18e75-200">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="18e75-201">Automatico</span><span class="sxs-lookup"><span data-stu-id="18e75-201">Automatic</span></span>
- <span data-ttu-id="18e75-202">Manuale</span><span class="sxs-lookup"><span data-stu-id="18e75-202">Manual</span></span>

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

### <span data-ttu-id="18e75-203">-Zona</span><span class="sxs-lookup"><span data-stu-id="18e75-203">-Zone</span></span>
<span data-ttu-id="18e75-204">Specifica l'elenco delle aree per il set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="18e75-204">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="18e75-205">-ZoneBalance</span><span class="sxs-lookup"><span data-stu-id="18e75-205">-ZoneBalance</span></span>
<span data-ttu-id="18e75-206">Se è necessario forzare la distribuzione rigorosa della macchina virtuale tra le aree x in caso di interruzioni di zona.</span><span class="sxs-lookup"><span data-stu-id="18e75-206">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="18e75-207">-Confermare</span><span class="sxs-lookup"><span data-stu-id="18e75-207">-Confirm</span></span>
<span data-ttu-id="18e75-208">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18e75-208">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18e75-209">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18e75-209">-WhatIf</span></span>
<span data-ttu-id="18e75-210">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="18e75-210">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="18e75-211">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="18e75-211">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18e75-212">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18e75-212">CommonParameters</span></span>
<span data-ttu-id="18e75-213">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18e75-213">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18e75-214">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18e75-214">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18e75-215">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="18e75-215">INPUTS</span></span>

### <span data-ttu-id="18e75-216">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="18e75-216">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="18e75-217">System. String</span><span class="sxs-lookup"><span data-stu-id="18e75-217">System.String</span></span>

### <span data-ttu-id="18e75-218">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="18e75-218">System.Collections.Hashtable</span></span>

### <span data-ttu-id="18e75-219">System. Int32</span><span class="sxs-lookup"><span data-stu-id="18e75-219">System.Int32</span></span>

### <span data-ttu-id="18e75-220">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. UpgradeMode, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="18e75-220">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="18e75-221">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetOSProfile</span><span class="sxs-lookup"><span data-stu-id="18e75-221">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="18e75-222">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetStorageProfile</span><span class="sxs-lookup"><span data-stu-id="18e75-222">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="18e75-223">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetNetworkConfiguration []</span><span class="sxs-lookup"><span data-stu-id="18e75-223">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="18e75-224">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetExtension []</span><span class="sxs-lookup"><span data-stu-id="18e75-224">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="18e75-225">System. String []</span><span class="sxs-lookup"><span data-stu-id="18e75-225">System.String[]</span></span>

### <span data-ttu-id="18e75-226">Microsoft. Azure. Management. Compute. Models. RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="18e75-226">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="18e75-227">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="18e75-227">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="18e75-228">Microsoft. Azure. Management. Compute. Models. BootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="18e75-228">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="18e75-229">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. ResourceIdentityType, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="18e75-229">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="18e75-230">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="18e75-230">OUTPUTS</span></span>

### <span data-ttu-id="18e75-231">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="18e75-231">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="18e75-232">Note</span><span class="sxs-lookup"><span data-stu-id="18e75-232">NOTES</span></span>

## <span data-ttu-id="18e75-233">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="18e75-233">RELATED LINKS</span></span>

[<span data-ttu-id="18e75-234">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="18e75-234">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="18e75-235">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="18e75-235">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="18e75-236">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="18e75-236">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="18e75-237">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="18e75-237">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="18e75-238">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="18e75-238">New-AzVmss</span></span>](./New-AzVmss.md)
