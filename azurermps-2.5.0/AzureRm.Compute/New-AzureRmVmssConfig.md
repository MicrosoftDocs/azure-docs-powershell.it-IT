---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmssconfig
schema: 2.0.0
ms.openlocfilehash: 4bc4782aaf235f81853a7304861a33ca53a75b45
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866743"
---
# <span data-ttu-id="6c82e-101">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="6c82e-101">New-AzureRmVmssConfig</span></span>

## <span data-ttu-id="6c82e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6c82e-102">SYNOPSIS</span></span>
<span data-ttu-id="6c82e-103">Crea un oggetto di configurazione VMSS.</span><span class="sxs-lookup"><span data-stu-id="6c82e-103">Creates a VMSS configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c82e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6c82e-104">SYNTAX</span></span>

### <span data-ttu-id="6c82e-105">DefaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6c82e-105">DefaultParameterSet (Default)</span></span>
```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c82e-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c82e-106">ExplicitIdentityParameterSet</span></span>
```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
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

### <span data-ttu-id="6c82e-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c82e-107">AssignIdentityParameterSet</span></span>
```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-AssignIdentity]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c82e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6c82e-108">DESCRIPTION</span></span>
<span data-ttu-id="6c82e-109">Il cmdlet **New-AzureRmVmssConfig** crea un oggetto vmss (Virtual Manager scale set) configurabile.</span><span class="sxs-lookup"><span data-stu-id="6c82e-109">The **New-AzureRmVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="6c82e-110">Altri cmdlet sono necessari per configurare l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="6c82e-110">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="6c82e-111">Questi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="6c82e-111">These cmdlets are:</span></span>

- <span data-ttu-id="6c82e-112">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="6c82e-112">Set-AzureRmVmssOsProfile</span></span>
- <span data-ttu-id="6c82e-113">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="6c82e-113">Set-AzureRmVmssStorageProfile</span></span>
- <span data-ttu-id="6c82e-114">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c82e-114">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="6c82e-115">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="6c82e-115">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="6c82e-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6c82e-116">EXAMPLES</span></span>

### <span data-ttu-id="6c82e-117">Esempio 1: creare un oggetto di configurazione VMSS</span><span class="sxs-lookup"><span data-stu-id="6c82e-117">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="6c82e-118">Questo esempio crea un oggetto di configurazione VMSS.</span><span class="sxs-lookup"><span data-stu-id="6c82e-118">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="6c82e-119">Il primo comando usa il cmdlet **New-AzureRmVmssConfig** per creare un oggetto di configurazione vmss e archivia il risultato nella variabile denominata $vmss.</span><span class="sxs-lookup"><span data-stu-id="6c82e-119">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="6c82e-120">Il secondo comando usa il cmdlet **New-AzureRmVmss** per creare un vmss che usa l'oggetto di configurazione vmss creato nel primo comando.</span><span class="sxs-lookup"><span data-stu-id="6c82e-120">The second command uses the **New-AzureRmVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="6c82e-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6c82e-121">PARAMETERS</span></span>

### <span data-ttu-id="6c82e-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="6c82e-122">-AssignIdentity</span></span>
<span data-ttu-id="6c82e-123">Specifica l'identità di sistema assegnata per il set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6c82e-123">Specify the system assigned identity for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="6c82e-124">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="6c82e-124">-AutoOSUpgrade</span></span>
<span data-ttu-id="6c82e-125">Imposta se gli aggiornamenti del sistema operativo devono essere applicati automaticamente alle istanze del set di scala in modo scorrevole quando una versione più recente dell'immagine diventa disponibile.</span><span class="sxs-lookup"><span data-stu-id="6c82e-125">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="6c82e-126">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="6c82e-126">-BootDiagnostic</span></span>
<span data-ttu-id="6c82e-127">Specifica il profilo set di diagnostica di avvio della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6c82e-127">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="6c82e-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c82e-128">-DefaultProfile</span></span>
<span data-ttu-id="6c82e-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6c82e-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c82e-130">-Extension</span><span class="sxs-lookup"><span data-stu-id="6c82e-130">-Extension</span></span>
<span data-ttu-id="6c82e-131">Specifica l'oggetto informazioni sull'estensione per VMSS.</span><span class="sxs-lookup"><span data-stu-id="6c82e-131">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="6c82e-132">Puoi usare il cmdlet **Add-AzureRmVmssExtension** per aggiungere questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="6c82e-132">You can use the **Add-AzureRmVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="6c82e-133">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="6c82e-133">-HealthProbeId</span></span>
<span data-ttu-id="6c82e-134">Specifica l'ID di un probe di bilanciamento del carico usato per determinare lo stato di un'istanza nel set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6c82e-134">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="6c82e-135">HealthProbeId è sotto forma di '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span><span class="sxs-lookup"><span data-stu-id="6c82e-135">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="6c82e-136">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="6c82e-136">-IdentityId</span></span>
<span data-ttu-id="6c82e-137">Specifica l'elenco delle identità utente associate al set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6c82e-137">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="6c82e-138">I riferimenti di identità utente saranno ID delle risorse ARM nella forma:'/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="6c82e-138">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="6c82e-139">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="6c82e-139">-IdentityType</span></span>
<span data-ttu-id="6c82e-140">Specifica il tipo di identità usato per il set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6c82e-140">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="6c82e-141">Il tipo ' SystemAssignedUserAssigned ' include sia un'identità creata in modo implicito che un set di identità assegnate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="6c82e-141">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="6c82e-142">Il tipo "None" rimuoverà le identità dal set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6c82e-142">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="6c82e-143">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="6c82e-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6c82e-144">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="6c82e-144">SystemAssigned</span></span>
- <span data-ttu-id="6c82e-145">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="6c82e-145">UserAssigned</span></span>
- <span data-ttu-id="6c82e-146">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="6c82e-146">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="6c82e-147">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6c82e-147">None</span></span>

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

### <span data-ttu-id="6c82e-148">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="6c82e-148">-LicenseType</span></span>
<span data-ttu-id="6c82e-149">Specificare il tipo di licenza, che è per portare il proprio scenario di licenza.</span><span class="sxs-lookup"><span data-stu-id="6c82e-149">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="6c82e-150">-Posizione</span><span class="sxs-lookup"><span data-stu-id="6c82e-150">-Location</span></span>
<span data-ttu-id="6c82e-151">Specifica la posizione di Azure in cui viene creato VMSS.</span><span class="sxs-lookup"><span data-stu-id="6c82e-151">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="6c82e-152">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c82e-152">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="6c82e-153">Specifica l'oggetto profilo di rete che contiene le proprietà di rete per la configurazione di VMSS.</span><span class="sxs-lookup"><span data-stu-id="6c82e-153">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="6c82e-154">Puoi usare il cmdlet **Add-AzureRmVmssNetworkInterfaceConfiguration** per aggiungere questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="6c82e-154">You can use the **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="6c82e-155">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="6c82e-155">-OsProfile</span></span>
<span data-ttu-id="6c82e-156">Specifica l'oggetto del profilo del sistema operativo che contiene le proprietà del sistema operativo per la configurazione di VMSS.</span><span class="sxs-lookup"><span data-stu-id="6c82e-156">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="6c82e-157">Puoi usare il cmdlet **set-AzureRmVmssOsProfile** per impostare questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="6c82e-157">You can use the **Set-AzureRmVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="6c82e-158">-Provisioning</span><span class="sxs-lookup"><span data-stu-id="6c82e-158">-Overprovision</span></span>
<span data-ttu-id="6c82e-159">Indica se il cmdlet viene sovradisposto da VMSS.</span><span class="sxs-lookup"><span data-stu-id="6c82e-159">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="6c82e-160">-PlanName</span><span class="sxs-lookup"><span data-stu-id="6c82e-160">-PlanName</span></span>
<span data-ttu-id="6c82e-161">Specifica il nome del piano.</span><span class="sxs-lookup"><span data-stu-id="6c82e-161">Specifies the plan name.</span></span>

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

### <span data-ttu-id="6c82e-162">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="6c82e-162">-PlanProduct</span></span>
<span data-ttu-id="6c82e-163">Specifica il prodotto piano.</span><span class="sxs-lookup"><span data-stu-id="6c82e-163">Specifies the plan product.</span></span>

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

### <span data-ttu-id="6c82e-164">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="6c82e-164">-PlanPromotionCode</span></span>
<span data-ttu-id="6c82e-165">Specifica il codice promozionale per il piano.</span><span class="sxs-lookup"><span data-stu-id="6c82e-165">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="6c82e-166">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="6c82e-166">-PlanPublisher</span></span>
<span data-ttu-id="6c82e-167">Specifica il piano Publisher.</span><span class="sxs-lookup"><span data-stu-id="6c82e-167">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="6c82e-168">-Priorità</span><span class="sxs-lookup"><span data-stu-id="6c82e-168">-Priority</span></span>
<span data-ttu-id="6c82e-169">Specifica la priorità per le macchine virtuali nel set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="6c82e-169">Specifies the priority for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="6c82e-170">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="6c82e-170">-RollingUpgradePolicy</span></span>
<span data-ttu-id="6c82e-171">Specifica i criteri di aggiornamento a rotazione.</span><span class="sxs-lookup"><span data-stu-id="6c82e-171">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="6c82e-172">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="6c82e-172">-SinglePlacementGroup</span></span>
<span data-ttu-id="6c82e-173">Specifica il gruppo di posizionamento singolo.</span><span class="sxs-lookup"><span data-stu-id="6c82e-173">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="6c82e-174">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="6c82e-174">-SkuCapacity</span></span>
<span data-ttu-id="6c82e-175">Specifica il numero di istanze in VMSS.</span><span class="sxs-lookup"><span data-stu-id="6c82e-175">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="6c82e-176">-SkuName</span><span class="sxs-lookup"><span data-stu-id="6c82e-176">-SkuName</span></span>
<span data-ttu-id="6c82e-177">Specifica le dimensioni di tutte le istanze di VMSS.</span><span class="sxs-lookup"><span data-stu-id="6c82e-177">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="6c82e-178">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="6c82e-178">-SkuTier</span></span>
<span data-ttu-id="6c82e-179">Specifica il livello di VMSS.</span><span class="sxs-lookup"><span data-stu-id="6c82e-179">Specifies the tier of VMSS.</span></span> <span data-ttu-id="6c82e-180">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="6c82e-180">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6c82e-181">Standard</span><span class="sxs-lookup"><span data-stu-id="6c82e-181">Standard</span></span>
- <span data-ttu-id="6c82e-182">Base</span><span class="sxs-lookup"><span data-stu-id="6c82e-182">Basic</span></span>

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

### <span data-ttu-id="6c82e-183">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="6c82e-183">-StorageProfile</span></span>
<span data-ttu-id="6c82e-184">Specifica l'oggetto profilo di archiviazione che contiene le proprietà del disco per la configurazione di VMSS.</span><span class="sxs-lookup"><span data-stu-id="6c82e-184">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="6c82e-185">Puoi usare il cmdlet **set-AzureRmVmssStorageProfile** per impostare questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="6c82e-185">You can use the **Set-AzureRmVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="6c82e-186">-Tag</span><span class="sxs-lookup"><span data-stu-id="6c82e-186">-Tag</span></span>
<span data-ttu-id="6c82e-187">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="6c82e-187">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6c82e-188">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="6c82e-188">For example:</span></span>

<span data-ttu-id="6c82e-189">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="6c82e-189">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6c82e-190">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="6c82e-190">-UpgradePolicyMode</span></span>
<span data-ttu-id="6c82e-191">Specifica la modalità di aggiornamento delle macchine virtuali nel set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="6c82e-191">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>

<span data-ttu-id="6c82e-192">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="6c82e-192">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6c82e-193">Automatico</span><span class="sxs-lookup"><span data-stu-id="6c82e-193">Automatic</span></span>
- <span data-ttu-id="6c82e-194">Manuale</span><span class="sxs-lookup"><span data-stu-id="6c82e-194">Manual</span></span>

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

### <span data-ttu-id="6c82e-195">-Zona</span><span class="sxs-lookup"><span data-stu-id="6c82e-195">-Zone</span></span>
<span data-ttu-id="6c82e-196">Specifica l'elenco delle aree per il set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6c82e-196">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="6c82e-197">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6c82e-197">-Confirm</span></span>
<span data-ttu-id="6c82e-198">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c82e-198">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c82e-199">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c82e-199">-WhatIf</span></span>
<span data-ttu-id="6c82e-200">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6c82e-200">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6c82e-201">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6c82e-201">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c82e-202">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c82e-202">CommonParameters</span></span>
<span data-ttu-id="6c82e-203">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c82e-203">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c82e-204">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c82e-204">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c82e-205">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6c82e-205">INPUTS</span></span>

### <span data-ttu-id="6c82e-206">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6c82e-206">None</span></span>
<span data-ttu-id="6c82e-207">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="6c82e-207">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6c82e-208">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6c82e-208">OUTPUTS</span></span>

### <span data-ttu-id="6c82e-209">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6c82e-209">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="6c82e-210">Note</span><span class="sxs-lookup"><span data-stu-id="6c82e-210">NOTES</span></span>

## <span data-ttu-id="6c82e-211">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6c82e-211">RELATED LINKS</span></span>

[<span data-ttu-id="6c82e-212">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="6c82e-212">Set-AzureRmVmssOsProfile</span></span>](./Set-AzureRmVmssOsProfile.md)

[<span data-ttu-id="6c82e-213">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="6c82e-213">Set-AzureRmVmssStorageProfile</span></span>](./Set-AzureRmVmssStorageProfile.md)

[<span data-ttu-id="6c82e-214">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c82e-214">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="6c82e-215">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="6c82e-215">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="6c82e-216">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6c82e-216">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)
