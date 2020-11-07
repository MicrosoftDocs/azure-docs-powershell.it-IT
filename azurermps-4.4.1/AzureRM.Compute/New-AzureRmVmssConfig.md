---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssConfig.md
ms.openlocfilehash: 3229f1e09cca1b32b62e5b7233806b20ed8ed78e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688034"
---
# <span data-ttu-id="361c8-101">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="361c8-101">New-AzureRmVmssConfig</span></span>

## <span data-ttu-id="361c8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="361c8-102">SYNOPSIS</span></span>
<span data-ttu-id="361c8-103">Crea un oggetto di configurazione VMSS.</span><span class="sxs-lookup"><span data-stu-id="361c8-103">Creates a VMSS configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="361c8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="361c8-104">SYNTAX</span></span>

```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int64>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-AssignIdentity]
 [-IdentityType <ResourceIdentityType>] [-RecoveryPolicyMode <RecoveryMode>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="361c8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="361c8-105">DESCRIPTION</span></span>
<span data-ttu-id="361c8-106">Il cmdlet **New-AzureRmVmssConfig** crea un oggetto vmss (Virtual Manager scale set) configurabile.</span><span class="sxs-lookup"><span data-stu-id="361c8-106">The **New-AzureRmVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span>
<span data-ttu-id="361c8-107">Altri cmdlet sono necessari per configurare l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="361c8-107">Other cmdlets are needed to configure the VMSS object.</span></span>
<span data-ttu-id="361c8-108">Questi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="361c8-108">These cmdlets are:</span></span>

- <span data-ttu-id="361c8-109">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="361c8-109">Set-AzureRmVmssOsProfile</span></span>
- <span data-ttu-id="361c8-110">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="361c8-110">Set-AzureRmVmssStorageProfile</span></span>
- <span data-ttu-id="361c8-111">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="361c8-111">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="361c8-112">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="361c8-112">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="361c8-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="361c8-113">EXAMPLES</span></span>

### <span data-ttu-id="361c8-114">Esempio 1: creare un oggetto di configurazione VMSS</span><span class="sxs-lookup"><span data-stu-id="361c8-114">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="361c8-115">Questo esempio crea un oggetto di configurazione VMSS.</span><span class="sxs-lookup"><span data-stu-id="361c8-115">This example creates a VMSS configuration object.</span></span>
<span data-ttu-id="361c8-116">Il primo comando usa il cmdlet **New-AzureRmVmssConfig** per creare un oggetto di configurazione vmss e archivia il risultato nella variabile denominata $vmss.</span><span class="sxs-lookup"><span data-stu-id="361c8-116">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="361c8-117">Il secondo comando usa il cmdlet **New-AzureRmVmss** per creare un vmss che usa l'oggetto di configurazione vmss creato nel primo comando.</span><span class="sxs-lookup"><span data-stu-id="361c8-117">The second command uses the **New-AzureRmVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="361c8-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="361c8-118">PARAMETERS</span></span>

### <span data-ttu-id="361c8-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="361c8-119">-AssignIdentity</span></span>
<span data-ttu-id="361c8-120">Specifica l'identità di sistema assegnata per il set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="361c8-120">Specify the system assigned identity for the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="361c8-121">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="361c8-121">-AutoOSUpgrade</span></span>
<span data-ttu-id="361c8-122">Imposta se gli aggiornamenti del sistema operativo devono essere applicati automaticamente alle istanze del set di scala in modo scorrevole quando una versione più recente dell'immagine diventa disponibile.</span><span class="sxs-lookup"><span data-stu-id="361c8-122">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="361c8-123">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="361c8-123">-BootDiagnostic</span></span>
<span data-ttu-id="361c8-124">Specifica il profilo set di diagnostica di avvio della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="361c8-124">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="361c8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="361c8-125">-DefaultProfile</span></span>
<span data-ttu-id="361c8-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="361c8-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="361c8-127">-Extension</span><span class="sxs-lookup"><span data-stu-id="361c8-127">-Extension</span></span>
<span data-ttu-id="361c8-128">Specifica l'oggetto informazioni sull'estensione per VMSS.</span><span class="sxs-lookup"><span data-stu-id="361c8-128">Specifies the extension information object for the VMSS.</span></span>
<span data-ttu-id="361c8-129">Puoi usare il cmdlet **Add-AzureRmVmssExtension** per aggiungere questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="361c8-129">You can use the **Add-AzureRmVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="361c8-130">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="361c8-130">-HealthProbeId</span></span>
<span data-ttu-id="361c8-131">Specifica l'ID di un probe di bilanciamento del carico usato per determinare lo stato di un'istanza nel set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="361c8-131">Specify the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span> <span data-ttu-id="361c8-132">HealthProbeId è sotto forma di '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span><span class="sxs-lookup"><span data-stu-id="361c8-132">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="361c8-133">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="361c8-133">-IdentityType</span></span>
<span data-ttu-id="361c8-134">Specificare l'identità del set di scale della macchina virtuale, se configurata.</span><span class="sxs-lookup"><span data-stu-id="361c8-134">Specify the identity of the virtual machine scale set, if configured.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: (All)
Aliases: 
Accepted values: SystemAssigned

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="361c8-135">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="361c8-135">-LicenseType</span></span>
<span data-ttu-id="361c8-136">Specificare il tipo di licenza, che è per portare il proprio scenario di licenza.</span><span class="sxs-lookup"><span data-stu-id="361c8-136">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="361c8-137">-Posizione</span><span class="sxs-lookup"><span data-stu-id="361c8-137">-Location</span></span>
<span data-ttu-id="361c8-138">Specifica la posizione di Azure in cui viene creato VMSS.</span><span class="sxs-lookup"><span data-stu-id="361c8-138">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="361c8-139">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="361c8-139">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="361c8-140">Specifica l'oggetto profilo di rete che contiene le proprietà di rete per la configurazione di VMSS.</span><span class="sxs-lookup"><span data-stu-id="361c8-140">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="361c8-141">Puoi usare il cmdlet **Add-AzureRmVmssNetworkInterfaceConfiguration** per aggiungere questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="361c8-141">You can use the **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="361c8-142">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="361c8-142">-OsProfile</span></span>
<span data-ttu-id="361c8-143">Specifica l'oggetto del profilo del sistema operativo che contiene le proprietà del sistema operativo per la configurazione di VMSS.</span><span class="sxs-lookup"><span data-stu-id="361c8-143">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="361c8-144">Puoi usare il cmdlet **set-AzureRmVmssOsProfile** per impostare questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="361c8-144">You can use the **Set-AzureRmVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="361c8-145">-Provisioning</span><span class="sxs-lookup"><span data-stu-id="361c8-145">-Overprovision</span></span>
<span data-ttu-id="361c8-146">Indica se il cmdlet viene sovradisposto da VMSS.</span><span class="sxs-lookup"><span data-stu-id="361c8-146">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="361c8-147">-PlanName</span><span class="sxs-lookup"><span data-stu-id="361c8-147">-PlanName</span></span>
<span data-ttu-id="361c8-148">Specifica il nome del piano.</span><span class="sxs-lookup"><span data-stu-id="361c8-148">Specifies the plan name.</span></span>

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

### <span data-ttu-id="361c8-149">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="361c8-149">-PlanProduct</span></span>
<span data-ttu-id="361c8-150">Specifica il prodotto piano.</span><span class="sxs-lookup"><span data-stu-id="361c8-150">Specifies the plan product.</span></span>

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

### <span data-ttu-id="361c8-151">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="361c8-151">-PlanPromotionCode</span></span>
<span data-ttu-id="361c8-152">Specifica il codice promozionale per il piano.</span><span class="sxs-lookup"><span data-stu-id="361c8-152">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="361c8-153">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="361c8-153">-PlanPublisher</span></span>
<span data-ttu-id="361c8-154">Specifica il piano Publisher.</span><span class="sxs-lookup"><span data-stu-id="361c8-154">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="361c8-155">-RecoveryPolicyMode</span><span class="sxs-lookup"><span data-stu-id="361c8-155">-RecoveryPolicyMode</span></span>
<span data-ttu-id="361c8-156">Specificare i criteri di ripristino.</span><span class="sxs-lookup"><span data-stu-id="361c8-156">Specify the recovery policy.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Compute.Automation.RecoveryMode]
Parameter Sets: (All)
Aliases: 
Accepted values: None, OverProvision, Reprovision

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="361c8-157">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="361c8-157">-RollingUpgradePolicy</span></span>
<span data-ttu-id="361c8-158">Specifica i criteri di aggiornamento a rotazione.</span><span class="sxs-lookup"><span data-stu-id="361c8-158">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="361c8-159">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="361c8-159">-SinglePlacementGroup</span></span>
<span data-ttu-id="361c8-160">Specifica il gruppo di posizionamento singolo.</span><span class="sxs-lookup"><span data-stu-id="361c8-160">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="361c8-161">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="361c8-161">-SkuCapacity</span></span>
<span data-ttu-id="361c8-162">Specifica il numero di istanze in VMSS.</span><span class="sxs-lookup"><span data-stu-id="361c8-162">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="361c8-163">-SkuName</span><span class="sxs-lookup"><span data-stu-id="361c8-163">-SkuName</span></span>
<span data-ttu-id="361c8-164">Specifica le dimensioni di tutte le istanze di VMSS.</span><span class="sxs-lookup"><span data-stu-id="361c8-164">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="361c8-165">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="361c8-165">-SkuTier</span></span>
<span data-ttu-id="361c8-166">Specifica il livello di VMSS.</span><span class="sxs-lookup"><span data-stu-id="361c8-166">Specifies the tier of VMSS.</span></span>

<span data-ttu-id="361c8-167">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="361c8-167">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="361c8-168">Standard</span><span class="sxs-lookup"><span data-stu-id="361c8-168">Standard</span></span>
- <span data-ttu-id="361c8-169">Base</span><span class="sxs-lookup"><span data-stu-id="361c8-169">Basic</span></span>

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

### <span data-ttu-id="361c8-170">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="361c8-170">-StorageProfile</span></span>
<span data-ttu-id="361c8-171">Specifica l'oggetto profilo di archiviazione che contiene le proprietà del disco per la configurazione di VMSS.</span><span class="sxs-lookup"><span data-stu-id="361c8-171">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="361c8-172">Puoi usare il cmdlet **set-AzureRmVmssStorageProfile** per impostare questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="361c8-172">You can use the **Set-AzureRmVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="361c8-173">-Tag</span><span class="sxs-lookup"><span data-stu-id="361c8-173">-Tag</span></span>
<span data-ttu-id="361c8-174">Specifica i tag che verranno assegnati a VMSS.</span><span class="sxs-lookup"><span data-stu-id="361c8-174">Specifies the tags that will be assigned to the VMSS.</span></span>

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

### <span data-ttu-id="361c8-175">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="361c8-175">-UpgradePolicyMode</span></span>
<span data-ttu-id="361c8-176">Specifica la modalità di aggiornamento delle macchine virtuali nel set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="361c8-176">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>

<span data-ttu-id="361c8-177">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="361c8-177">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="361c8-178">Automatico</span><span class="sxs-lookup"><span data-stu-id="361c8-178">Automatic</span></span>
- <span data-ttu-id="361c8-179">Manuale</span><span class="sxs-lookup"><span data-stu-id="361c8-179">Manual</span></span>

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

### <span data-ttu-id="361c8-180">-Zona</span><span class="sxs-lookup"><span data-stu-id="361c8-180">-Zone</span></span>
<span data-ttu-id="361c8-181">Specifica l'elenco delle aree per il set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="361c8-181">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="361c8-182">-Confermare</span><span class="sxs-lookup"><span data-stu-id="361c8-182">-Confirm</span></span>
<span data-ttu-id="361c8-183">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="361c8-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="361c8-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="361c8-184">-WhatIf</span></span>
<span data-ttu-id="361c8-185">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="361c8-185">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="361c8-186">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="361c8-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="361c8-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="361c8-187">CommonParameters</span></span>
<span data-ttu-id="361c8-188">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="361c8-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="361c8-189">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="361c8-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="361c8-190">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="361c8-190">INPUTS</span></span>

## <span data-ttu-id="361c8-191">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="361c8-191">OUTPUTS</span></span>

### <span data-ttu-id="361c8-192">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="361c8-192">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="361c8-193">Note</span><span class="sxs-lookup"><span data-stu-id="361c8-193">NOTES</span></span>

## <span data-ttu-id="361c8-194">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="361c8-194">RELATED LINKS</span></span>

[<span data-ttu-id="361c8-195">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="361c8-195">Set-AzureRmVmssOsProfile</span></span>](./Set-AzureRmVmssOsProfile.md)

[<span data-ttu-id="361c8-196">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="361c8-196">Set-AzureRmVmssStorageProfile</span></span>](./Set-AzureRmVmssStorageProfile.md)

[<span data-ttu-id="361c8-197">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="361c8-197">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="361c8-198">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="361c8-198">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="361c8-199">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="361c8-199">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)


