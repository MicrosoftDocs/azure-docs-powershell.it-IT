---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmssConfig.md
ms.openlocfilehash: ee18925960b7f2afd9e35250a3cc33a5bd16e073
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511847"
---
# <span data-ttu-id="75841-101">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="75841-101">New-AzureRmVmssConfig</span></span>

## <span data-ttu-id="75841-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="75841-102">SYNOPSIS</span></span>
<span data-ttu-id="75841-103">Crea un oggetto di configurazione VMSS.</span><span class="sxs-lookup"><span data-stu-id="75841-103">Creates a VMSS configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75841-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="75841-104">SYNTAX</span></span>

### <span data-ttu-id="75841-105">DefaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="75841-105">DefaultParameterSet (Default)</span></span>
```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-ZoneBalance]
 [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>] [-PlanName <String>] [-PlanPublisher <String>]
 [-PlanProduct <String>] [-PlanPromotionCode <String>] [-RollingUpgradePolicy <RollingUpgradePolicy>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75841-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="75841-106">ExplicitIdentityParameterSet</span></span>
```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
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

### <span data-ttu-id="75841-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="75841-107">AssignIdentityParameterSet</span></span>
```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-ZoneBalance]
 [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>] [-PlanName <String>] [-PlanPublisher <String>]
 [-PlanProduct <String>] [-PlanPromotionCode <String>] [-RollingUpgradePolicy <RollingUpgradePolicy>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-AssignIdentity] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75841-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="75841-108">DESCRIPTION</span></span>
<span data-ttu-id="75841-109">Il cmdlet **New-AzureRmVmssConfig** crea un oggetto vmss (Virtual Manager scale set) configurabile.</span><span class="sxs-lookup"><span data-stu-id="75841-109">The **New-AzureRmVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="75841-110">Altri cmdlet sono necessari per configurare l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="75841-110">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="75841-111">Questi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="75841-111">These cmdlets are:</span></span>
- <span data-ttu-id="75841-112">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="75841-112">Set-AzureRmVmssOsProfile</span></span>
- <span data-ttu-id="75841-113">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="75841-113">Set-AzureRmVmssStorageProfile</span></span>
- <span data-ttu-id="75841-114">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="75841-114">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="75841-115">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="75841-115">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="75841-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="75841-116">EXAMPLES</span></span>

### <span data-ttu-id="75841-117">Esempio 1: creare un oggetto di configurazione VMSS</span><span class="sxs-lookup"><span data-stu-id="75841-117">Example 1: Create a VMSS configuration object</span></span>
```
PS C:\> $VMSS = New-AzureRmVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic" -NetworkInterfaceConfiguration $NetCfg `
            | Add-AzureRmVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
            | Set-AzureRmVmssOSProfile -ComputerNamePrefix "Test" -AdminUsername $adminUsername -AdminPassword $AdminPassword `
            | Set-AzureRmVmssStorageProfile -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VHDContainer `
            | Add-AzureRmVmssAdditionalUnattendContent -ComponentName  $AUCComponentName -Content  $AUCContent -PassName  $AUCPassName -SettingName  $AUCSetting `
            | Remove-AzureRmVmssAdditionalUnattendContent -ComponentName  $AUCComponentName;

New-AzureRmVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

<span data-ttu-id="75841-118">Questo esempio crea un oggetto di configurazione VMSS.</span><span class="sxs-lookup"><span data-stu-id="75841-118">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="75841-119">Il primo comando usa il cmdlet **New-AzureRmVmssConfig** per creare un oggetto di configurazione vmss e archivia il risultato nella variabile denominata $vmss.</span><span class="sxs-lookup"><span data-stu-id="75841-119">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="75841-120">Il secondo comando usa il cmdlet **New-AzureRmVmss** per creare un vmss che usa l'oggetto di configurazione vmss creato nel primo comando.</span><span class="sxs-lookup"><span data-stu-id="75841-120">The second command uses the **New-AzureRmVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="75841-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="75841-121">PARAMETERS</span></span>

### <span data-ttu-id="75841-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="75841-122">-AssignIdentity</span></span>
<span data-ttu-id="75841-123">Specifica l'identità di sistema assegnata per il set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="75841-123">Specify the system assigned identity for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="75841-124">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="75841-124">-AutoOSUpgrade</span></span>
<span data-ttu-id="75841-125">Imposta se gli aggiornamenti del sistema operativo devono essere applicati automaticamente alle istanze del set di scala in modo scorrevole quando una versione più recente dell'immagine diventa disponibile.</span><span class="sxs-lookup"><span data-stu-id="75841-125">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="75841-126">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="75841-126">-BootDiagnostic</span></span>
<span data-ttu-id="75841-127">Specifica il profilo set di diagnostica di avvio della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="75841-127">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="75841-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75841-128">-DefaultProfile</span></span>
<span data-ttu-id="75841-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="75841-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75841-130">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="75841-130">-DisableAutoRollback</span></span>
<span data-ttu-id="75841-131">Disabilitare il rollback automatico per i criteri di aggiornamento del sistema operativo automatico</span><span class="sxs-lookup"><span data-stu-id="75841-131">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="75841-132">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="75841-132">-EnableUltraSSD</span></span>
<span data-ttu-id="75841-133">Consente a una funzionalità di avere uno o più dischi di dati gestiti con UltraSSD_LRS tipo di account di archiviazione nel set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="75841-133">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="75841-134">Dischi gestiti con tipo di account di archiviazione UltraSSD_LRS può essere aggiunto a un VMSS solo se questa proprietà è abilitata.</span><span class="sxs-lookup"><span data-stu-id="75841-134">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="75841-135">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="75841-135">-EvictionPolicy</span></span>
<span data-ttu-id="75841-136">Specifica i criteri di eliminazione per le macchine virtuali nel set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="75841-136">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="75841-137">-Extension</span><span class="sxs-lookup"><span data-stu-id="75841-137">-Extension</span></span>
<span data-ttu-id="75841-138">Specifica l'oggetto informazioni sull'estensione per VMSS.</span><span class="sxs-lookup"><span data-stu-id="75841-138">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="75841-139">Puoi usare il cmdlet **Add-AzureRmVmssExtension** per aggiungere questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="75841-139">You can use the **Add-AzureRmVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="75841-140">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="75841-140">-HealthProbeId</span></span>
<span data-ttu-id="75841-141">Specifica l'ID di un probe di bilanciamento del carico usato per determinare lo stato di un'istanza nel set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="75841-141">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="75841-142">HealthProbeId è sotto forma di '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span><span class="sxs-lookup"><span data-stu-id="75841-142">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="75841-143">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="75841-143">-IdentityId</span></span>
<span data-ttu-id="75841-144">Specifica l'elenco delle identità utente associate al set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="75841-144">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="75841-145">I riferimenti di identità utente saranno ID delle risorse ARM nella forma:'/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="75841-145">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="75841-146">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="75841-146">-IdentityType</span></span>
<span data-ttu-id="75841-147">Specifica il tipo di identità usato per il set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="75841-147">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="75841-148">Il tipo ' SystemAssignedUserAssigned ' include sia un'identità creata in modo implicito che un set di identità assegnate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="75841-148">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="75841-149">Il tipo "None" rimuoverà le identità dal set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="75841-149">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="75841-150">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="75841-150">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="75841-151">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="75841-151">SystemAssigned</span></span>
- <span data-ttu-id="75841-152">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="75841-152">UserAssigned</span></span>
- <span data-ttu-id="75841-153">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="75841-153">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="75841-154">Nessuno</span><span class="sxs-lookup"><span data-stu-id="75841-154">None</span></span>

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

### <span data-ttu-id="75841-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="75841-155">-LicenseType</span></span>
<span data-ttu-id="75841-156">Specificare il tipo di licenza, che è per portare il proprio scenario di licenza.</span><span class="sxs-lookup"><span data-stu-id="75841-156">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="75841-157">-Posizione</span><span class="sxs-lookup"><span data-stu-id="75841-157">-Location</span></span>
<span data-ttu-id="75841-158">Specifica la posizione di Azure in cui viene creato VMSS.</span><span class="sxs-lookup"><span data-stu-id="75841-158">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="75841-159">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="75841-159">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="75841-160">Specifica l'oggetto profilo di rete che contiene le proprietà di rete per la configurazione di VMSS.</span><span class="sxs-lookup"><span data-stu-id="75841-160">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="75841-161">Puoi usare il cmdlet **Add-AzureRmVmssNetworkInterfaceConfiguration** per aggiungere questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="75841-161">You can use the **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="75841-162">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="75841-162">-OsProfile</span></span>
<span data-ttu-id="75841-163">Specifica l'oggetto del profilo del sistema operativo che contiene le proprietà del sistema operativo per la configurazione di VMSS.</span><span class="sxs-lookup"><span data-stu-id="75841-163">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="75841-164">Puoi usare il cmdlet **set-AzureRmVmssOsProfile** per impostare questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="75841-164">You can use the **Set-AzureRmVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="75841-165">-Provisioning</span><span class="sxs-lookup"><span data-stu-id="75841-165">-Overprovision</span></span>
<span data-ttu-id="75841-166">Indica se il cmdlet viene sovradisposto da VMSS.</span><span class="sxs-lookup"><span data-stu-id="75841-166">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="75841-167">-PlanName</span><span class="sxs-lookup"><span data-stu-id="75841-167">-PlanName</span></span>
<span data-ttu-id="75841-168">Specifica il nome del piano.</span><span class="sxs-lookup"><span data-stu-id="75841-168">Specifies the plan name.</span></span>

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

### <span data-ttu-id="75841-169">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="75841-169">-PlanProduct</span></span>
<span data-ttu-id="75841-170">Specifica il prodotto piano.</span><span class="sxs-lookup"><span data-stu-id="75841-170">Specifies the plan product.</span></span>

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

### <span data-ttu-id="75841-171">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="75841-171">-PlanPromotionCode</span></span>
<span data-ttu-id="75841-172">Specifica il codice promozionale per il piano.</span><span class="sxs-lookup"><span data-stu-id="75841-172">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="75841-173">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="75841-173">-PlanPublisher</span></span>
<span data-ttu-id="75841-174">Specifica il piano Publisher.</span><span class="sxs-lookup"><span data-stu-id="75841-174">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="75841-175">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="75841-175">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="75841-176">Conteggio dei domini di errore per ogni gruppo di posizionamento.</span><span class="sxs-lookup"><span data-stu-id="75841-176">Fault Domain count for each placement group.</span></span>

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

### <span data-ttu-id="75841-177">-Priorità</span><span class="sxs-lookup"><span data-stu-id="75841-177">-Priority</span></span>
<span data-ttu-id="75841-178">Specifica la priorità per le macchine virtuali nel set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="75841-178">Specifies the priority for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="75841-179">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="75841-179">-RollingUpgradePolicy</span></span>
<span data-ttu-id="75841-180">Specifica i criteri di aggiornamento a rotazione.</span><span class="sxs-lookup"><span data-stu-id="75841-180">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="75841-181">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="75841-181">-SinglePlacementGroup</span></span>
<span data-ttu-id="75841-182">Specifica il gruppo di posizionamento singolo.</span><span class="sxs-lookup"><span data-stu-id="75841-182">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="75841-183">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="75841-183">-SkuCapacity</span></span>
<span data-ttu-id="75841-184">Specifica il numero di istanze in VMSS.</span><span class="sxs-lookup"><span data-stu-id="75841-184">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="75841-185">-SkuName</span><span class="sxs-lookup"><span data-stu-id="75841-185">-SkuName</span></span>
<span data-ttu-id="75841-186">Specifica le dimensioni di tutte le istanze di VMSS.</span><span class="sxs-lookup"><span data-stu-id="75841-186">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="75841-187">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="75841-187">-SkuTier</span></span>
<span data-ttu-id="75841-188">Specifica il livello di VMSS.</span><span class="sxs-lookup"><span data-stu-id="75841-188">Specifies the tier of VMSS.</span></span> <span data-ttu-id="75841-189">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="75841-189">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="75841-190">Standard</span><span class="sxs-lookup"><span data-stu-id="75841-190">Standard</span></span>
- <span data-ttu-id="75841-191">Base</span><span class="sxs-lookup"><span data-stu-id="75841-191">Basic</span></span>

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

### <span data-ttu-id="75841-192">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="75841-192">-StorageProfile</span></span>
<span data-ttu-id="75841-193">Specifica l'oggetto profilo di archiviazione che contiene le proprietà del disco per la configurazione di VMSS.</span><span class="sxs-lookup"><span data-stu-id="75841-193">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="75841-194">Puoi usare il cmdlet **set-AzureRmVmssStorageProfile** per impostare questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="75841-194">You can use the **Set-AzureRmVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="75841-195">-Tag</span><span class="sxs-lookup"><span data-stu-id="75841-195">-Tag</span></span>
<span data-ttu-id="75841-196">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="75841-196">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="75841-197">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="75841-197">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="75841-198">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="75841-198">-UpgradePolicyMode</span></span>
<span data-ttu-id="75841-199">Specifica la modalità di aggiornamento delle macchine virtuali nel set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="75841-199">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="75841-200">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="75841-200">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="75841-201">Automatico</span><span class="sxs-lookup"><span data-stu-id="75841-201">Automatic</span></span>
- <span data-ttu-id="75841-202">Manuale</span><span class="sxs-lookup"><span data-stu-id="75841-202">Manual</span></span>

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

### <span data-ttu-id="75841-203">-Zona</span><span class="sxs-lookup"><span data-stu-id="75841-203">-Zone</span></span>
<span data-ttu-id="75841-204">Specifica l'elenco delle aree per il set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="75841-204">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="75841-205">-ZoneBalance</span><span class="sxs-lookup"><span data-stu-id="75841-205">-ZoneBalance</span></span>
<span data-ttu-id="75841-206">Se è necessario forzare la distribuzione rigorosa della macchina virtuale tra le aree x in caso di interruzioni di zona.</span><span class="sxs-lookup"><span data-stu-id="75841-206">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="75841-207">-Confermare</span><span class="sxs-lookup"><span data-stu-id="75841-207">-Confirm</span></span>
<span data-ttu-id="75841-208">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75841-208">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75841-209">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75841-209">-WhatIf</span></span>
<span data-ttu-id="75841-210">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="75841-210">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="75841-211">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="75841-211">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75841-212">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75841-212">CommonParameters</span></span>
<span data-ttu-id="75841-213">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75841-213">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75841-214">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75841-214">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75841-215">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="75841-215">INPUTS</span></span>

### <span data-ttu-id="75841-216">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="75841-216">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="75841-217">System. String</span><span class="sxs-lookup"><span data-stu-id="75841-217">System.String</span></span>

### <span data-ttu-id="75841-218">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="75841-218">System.Collections.Hashtable</span></span>

### <span data-ttu-id="75841-219">System. Int32</span><span class="sxs-lookup"><span data-stu-id="75841-219">System.Int32</span></span>

### <span data-ttu-id="75841-220">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. UpgradeMode, Microsoft. Azure. Management. Compute, Version = 21.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="75841-220">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="75841-221">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetOSProfile</span><span class="sxs-lookup"><span data-stu-id="75841-221">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="75841-222">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetStorageProfile</span><span class="sxs-lookup"><span data-stu-id="75841-222">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="75841-223">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetNetworkConfiguration []</span><span class="sxs-lookup"><span data-stu-id="75841-223">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="75841-224">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetExtension []</span><span class="sxs-lookup"><span data-stu-id="75841-224">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="75841-225">System. String []</span><span class="sxs-lookup"><span data-stu-id="75841-225">System.String[]</span></span>

### <span data-ttu-id="75841-226">Microsoft. Azure. Management. Compute. Models. RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="75841-226">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="75841-227">Microsoft. Azure. Management. Compute. Models. BootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="75841-227">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="75841-228">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. ResourceIdentityType, Microsoft. Azure. Management. Compute, Version = 21.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="75841-228">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="75841-229">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="75841-229">OUTPUTS</span></span>

### <span data-ttu-id="75841-230">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="75841-230">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="75841-231">Note</span><span class="sxs-lookup"><span data-stu-id="75841-231">NOTES</span></span>

## <span data-ttu-id="75841-232">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="75841-232">RELATED LINKS</span></span>

[<span data-ttu-id="75841-233">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="75841-233">Set-AzureRmVmssOsProfile</span></span>](./Set-AzureRmVmssOsProfile.md)

[<span data-ttu-id="75841-234">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="75841-234">Set-AzureRmVmssStorageProfile</span></span>](./Set-AzureRmVmssStorageProfile.md)

[<span data-ttu-id="75841-235">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="75841-235">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="75841-236">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="75841-236">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="75841-237">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="75841-237">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)
