---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: c407ce7147d3eb175fc181b76b140605e463d9a0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863605"
---
# <span data-ttu-id="039a3-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="039a3-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="039a3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="039a3-102">SYNOPSIS</span></span>
<span data-ttu-id="039a3-103">Crea un oggetto di configurazione VMSS.</span><span class="sxs-lookup"><span data-stu-id="039a3-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="039a3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="039a3-104">SYNTAX</span></span>

### <span data-ttu-id="039a3-105">DefaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="039a3-105">DefaultParameterSet (Default)</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="039a3-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="039a3-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="039a3-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="039a3-107">AssignIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-AssignIdentity]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="039a3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="039a3-108">DESCRIPTION</span></span>
<span data-ttu-id="039a3-109">Il cmdlet **New-AzVmssConfig** crea un oggetto vmss (Virtual Manager scale set) configurabile.</span><span class="sxs-lookup"><span data-stu-id="039a3-109">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="039a3-110">Altri cmdlet sono necessari per configurare l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="039a3-110">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="039a3-111">Questi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="039a3-111">These cmdlets are:</span></span>

- <span data-ttu-id="039a3-112">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="039a3-112">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="039a3-113">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="039a3-113">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="039a3-114">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="039a3-114">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="039a3-115">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="039a3-115">Add-AzVmssExtension</span></span>

## <span data-ttu-id="039a3-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="039a3-116">EXAMPLES</span></span>

### <span data-ttu-id="039a3-117">Esempio 1: creare un oggetto di configurazione VMSS</span><span class="sxs-lookup"><span data-stu-id="039a3-117">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="039a3-118">Questo esempio crea un oggetto di configurazione VMSS.</span><span class="sxs-lookup"><span data-stu-id="039a3-118">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="039a3-119">Il primo comando usa il cmdlet **New-AzVmssConfig** per creare un oggetto di configurazione vmss e archivia il risultato nella variabile denominata $vmss.</span><span class="sxs-lookup"><span data-stu-id="039a3-119">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="039a3-120">Il secondo comando usa il cmdlet **New-AzVmss** per creare un vmss che usa l'oggetto di configurazione vmss creato nel primo comando.</span><span class="sxs-lookup"><span data-stu-id="039a3-120">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="039a3-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="039a3-121">PARAMETERS</span></span>

### <span data-ttu-id="039a3-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="039a3-122">-AssignIdentity</span></span>
<span data-ttu-id="039a3-123">Specifica l'identità di sistema assegnata per il set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="039a3-123">Specify the system assigned identity for the virtual machine scale set.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="039a3-124">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="039a3-124">-AutoOSUpgrade</span></span>
<span data-ttu-id="039a3-125">Imposta se gli aggiornamenti del sistema operativo devono essere applicati automaticamente alle istanze del set di scala in modo scorrevole quando una versione più recente dell'immagine diventa disponibile.</span><span class="sxs-lookup"><span data-stu-id="039a3-125">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="039a3-126">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="039a3-126">-BootDiagnostic</span></span>
<span data-ttu-id="039a3-127">Specifica il profilo set di diagnostica di avvio della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="039a3-127">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

```yaml
Type: BootDiagnostics
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="039a3-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="039a3-128">-DefaultProfile</span></span>
<span data-ttu-id="039a3-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="039a3-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="039a3-130">-Extension</span><span class="sxs-lookup"><span data-stu-id="039a3-130">-Extension</span></span>
<span data-ttu-id="039a3-131">Specifica l'oggetto informazioni sull'estensione per VMSS.</span><span class="sxs-lookup"><span data-stu-id="039a3-131">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="039a3-132">Puoi usare il cmdlet **Add-AzVmssExtension** per aggiungere questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="039a3-132">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

```yaml
Type: VirtualMachineScaleSetExtension[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="039a3-133">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="039a3-133">-HealthProbeId</span></span>
<span data-ttu-id="039a3-134">Specifica l'ID di un probe di bilanciamento del carico usato per determinare lo stato di un'istanza nel set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="039a3-134">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="039a3-135">HealthProbeId è sotto forma di '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span><span class="sxs-lookup"><span data-stu-id="039a3-135">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="039a3-136">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="039a3-136">-IdentityId</span></span>
<span data-ttu-id="039a3-137">Specifica l'elenco delle identità utente associate al set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="039a3-137">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="039a3-138">I riferimenti di identità utente saranno ID delle risorse ARM nella forma:'/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="039a3-138">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="039a3-139">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="039a3-139">-IdentityType</span></span>
<span data-ttu-id="039a3-140">Specifica il tipo di identità usato per il set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="039a3-140">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="039a3-141">Il tipo ' SystemAssignedUserAssigned ' include sia un'identità creata in modo implicito che un set di identità assegnate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="039a3-141">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="039a3-142">Il tipo "None" rimuoverà le identità dal set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="039a3-142">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="039a3-143">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="039a3-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="039a3-144">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="039a3-144">SystemAssigned</span></span>
- <span data-ttu-id="039a3-145">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="039a3-145">UserAssigned</span></span>
- <span data-ttu-id="039a3-146">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="039a3-146">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="039a3-147">Nessuno</span><span class="sxs-lookup"><span data-stu-id="039a3-147">None</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="039a3-148">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="039a3-148">-LicenseType</span></span>
<span data-ttu-id="039a3-149">Specificare il tipo di licenza, che è per portare il proprio scenario di licenza.</span><span class="sxs-lookup"><span data-stu-id="039a3-149">Specify the license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="039a3-150">-Posizione</span><span class="sxs-lookup"><span data-stu-id="039a3-150">-Location</span></span>
<span data-ttu-id="039a3-151">Specifica la posizione di Azure in cui viene creato VMSS.</span><span class="sxs-lookup"><span data-stu-id="039a3-151">Specifies the Azure location where the VMSS is created.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="039a3-152">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="039a3-152">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="039a3-153">Specifica l'oggetto profilo di rete che contiene le proprietà di rete per la configurazione di VMSS.</span><span class="sxs-lookup"><span data-stu-id="039a3-153">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="039a3-154">Puoi usare il cmdlet **Add-AzVmssNetworkInterfaceConfiguration** per aggiungere questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="039a3-154">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

```yaml
Type: VirtualMachineScaleSetNetworkConfiguration[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="039a3-155">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="039a3-155">-OsProfile</span></span>
<span data-ttu-id="039a3-156">Specifica l'oggetto del profilo del sistema operativo che contiene le proprietà del sistema operativo per la configurazione di VMSS.</span><span class="sxs-lookup"><span data-stu-id="039a3-156">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="039a3-157">Puoi usare il cmdlet **set-AzVmssOsProfile** per impostare questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="039a3-157">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

```yaml
Type: VirtualMachineScaleSetOSProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="039a3-158">-Provisioning</span><span class="sxs-lookup"><span data-stu-id="039a3-158">-Overprovision</span></span>
<span data-ttu-id="039a3-159">Indica se il cmdlet viene sovradisposto da VMSS.</span><span class="sxs-lookup"><span data-stu-id="039a3-159">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="039a3-160">-PlanName</span><span class="sxs-lookup"><span data-stu-id="039a3-160">-PlanName</span></span>
<span data-ttu-id="039a3-161">Specifica il nome del piano.</span><span class="sxs-lookup"><span data-stu-id="039a3-161">Specifies the plan name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="039a3-162">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="039a3-162">-PlanProduct</span></span>
<span data-ttu-id="039a3-163">Specifica il prodotto piano.</span><span class="sxs-lookup"><span data-stu-id="039a3-163">Specifies the plan product.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="039a3-164">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="039a3-164">-PlanPromotionCode</span></span>
<span data-ttu-id="039a3-165">Specifica il codice promozionale per il piano.</span><span class="sxs-lookup"><span data-stu-id="039a3-165">Specifies the plan promotion code.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="039a3-166">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="039a3-166">-PlanPublisher</span></span>
<span data-ttu-id="039a3-167">Specifica il piano Publisher.</span><span class="sxs-lookup"><span data-stu-id="039a3-167">Specifies the plan publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="039a3-168">-Priorità</span><span class="sxs-lookup"><span data-stu-id="039a3-168">-Priority</span></span>
<span data-ttu-id="039a3-169">Specifica la priorità per le macchine virtuali nel set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="039a3-169">Specifies the priority for the virtual machines in the scale set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="039a3-170">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="039a3-170">-RollingUpgradePolicy</span></span>
<span data-ttu-id="039a3-171">Specifica i criteri di aggiornamento a rotazione.</span><span class="sxs-lookup"><span data-stu-id="039a3-171">Specifies the rolling upgrade policy.</span></span>

```yaml
Type: RollingUpgradePolicy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="039a3-172">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="039a3-172">-SinglePlacementGroup</span></span>
<span data-ttu-id="039a3-173">Specifica il gruppo di posizionamento singolo.</span><span class="sxs-lookup"><span data-stu-id="039a3-173">Specifies the single placement group.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="039a3-174">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="039a3-174">-SkuCapacity</span></span>
<span data-ttu-id="039a3-175">Specifica il numero di istanze in VMSS.</span><span class="sxs-lookup"><span data-stu-id="039a3-175">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="039a3-176">-SkuName</span><span class="sxs-lookup"><span data-stu-id="039a3-176">-SkuName</span></span>
<span data-ttu-id="039a3-177">Specifica le dimensioni di tutte le istanze di VMSS.</span><span class="sxs-lookup"><span data-stu-id="039a3-177">Specifies the size of all the instances of VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="039a3-178">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="039a3-178">-SkuTier</span></span>
<span data-ttu-id="039a3-179">Specifica il livello di VMSS.</span><span class="sxs-lookup"><span data-stu-id="039a3-179">Specifies the tier of VMSS.</span></span> <span data-ttu-id="039a3-180">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="039a3-180">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="039a3-181">Standard</span><span class="sxs-lookup"><span data-stu-id="039a3-181">Standard</span></span>
- <span data-ttu-id="039a3-182">Base</span><span class="sxs-lookup"><span data-stu-id="039a3-182">Basic</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="039a3-183">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="039a3-183">-StorageProfile</span></span>
<span data-ttu-id="039a3-184">Specifica l'oggetto profilo di archiviazione che contiene le proprietà del disco per la configurazione di VMSS.</span><span class="sxs-lookup"><span data-stu-id="039a3-184">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="039a3-185">Puoi usare il cmdlet **set-AzVmssStorageProfile** per impostare questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="039a3-185">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

```yaml
Type: VirtualMachineScaleSetStorageProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="039a3-186">-Tag</span><span class="sxs-lookup"><span data-stu-id="039a3-186">-Tag</span></span>
<span data-ttu-id="039a3-187">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="039a3-187">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="039a3-188">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="039a3-188">For example:</span></span>

<span data-ttu-id="039a3-189">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="039a3-189">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="039a3-190">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="039a3-190">-UpgradePolicyMode</span></span>
<span data-ttu-id="039a3-191">Specifica la modalità di aggiornamento delle macchine virtuali nel set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="039a3-191">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>

<span data-ttu-id="039a3-192">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="039a3-192">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="039a3-193">Automatico</span><span class="sxs-lookup"><span data-stu-id="039a3-193">Automatic</span></span>
- <span data-ttu-id="039a3-194">Manuale</span><span class="sxs-lookup"><span data-stu-id="039a3-194">Manual</span></span>

```yaml
Type: UpgradeMode
Parameter Sets: (All)
Aliases: 
Accepted values: Automatic, Manual, Rolling

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="039a3-195">-Zona</span><span class="sxs-lookup"><span data-stu-id="039a3-195">-Zone</span></span>
<span data-ttu-id="039a3-196">Specifica l'elenco delle aree per il set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="039a3-196">Specifies the zone list for the virtual machine scale set.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="039a3-197">-Confermare</span><span class="sxs-lookup"><span data-stu-id="039a3-197">-Confirm</span></span>
<span data-ttu-id="039a3-198">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="039a3-198">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="039a3-199">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="039a3-199">-WhatIf</span></span>
<span data-ttu-id="039a3-200">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="039a3-200">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="039a3-201">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="039a3-201">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="039a3-202">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="039a3-202">CommonParameters</span></span>
<span data-ttu-id="039a3-203">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="039a3-203">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="039a3-204">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="039a3-204">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="039a3-205">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="039a3-205">INPUTS</span></span>

### <span data-ttu-id="039a3-206">Nessuno</span><span class="sxs-lookup"><span data-stu-id="039a3-206">None</span></span>
<span data-ttu-id="039a3-207">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="039a3-207">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="039a3-208">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="039a3-208">OUTPUTS</span></span>

### <span data-ttu-id="039a3-209">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="039a3-209">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="039a3-210">Note</span><span class="sxs-lookup"><span data-stu-id="039a3-210">NOTES</span></span>

## <span data-ttu-id="039a3-211">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="039a3-211">RELATED LINKS</span></span>

[<span data-ttu-id="039a3-212">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="039a3-212">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="039a3-213">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="039a3-213">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="039a3-214">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="039a3-214">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="039a3-215">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="039a3-215">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="039a3-216">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="039a3-216">New-AzVmss</span></span>](./New-AzVmss.md)
