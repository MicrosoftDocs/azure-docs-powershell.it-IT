---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: 4fdfd5c5da9cc803cacdd2aca90b7f66771988fd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300780"
---
# <span data-ttu-id="cfea7-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="cfea7-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="cfea7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cfea7-102">SYNOPSIS</span></span>
<span data-ttu-id="cfea7-103">Crea un oggetto di configurazione VMSS.</span><span class="sxs-lookup"><span data-stu-id="cfea7-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="cfea7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cfea7-104">SYNTAX</span></span>

### <span data-ttu-id="cfea7-105">DefaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cfea7-105">DefaultParameterSet (Default)</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-MaxPrice <Double>] [-TerminateScheduledEvents] [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>]
 [-ProximityPlacementGroupId <String>] [-ScaleInPolicy <String[]>] [-EncryptionAtHost]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfea7-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfea7-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-MaxPrice <Double>] [-TerminateScheduledEvents] [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>]
 [-ProximityPlacementGroupId <String>] [-ScaleInPolicy <String[]>] -IdentityType <ResourceIdentityType>
 [-IdentityId <String[]>] [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cfea7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cfea7-107">DESCRIPTION</span></span>
<span data-ttu-id="cfea7-108">Il cmdlet **New-AzVmssConfig** crea un oggetto vmss (Virtual Manager scale set) configurabile.</span><span class="sxs-lookup"><span data-stu-id="cfea7-108">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="cfea7-109">Altri cmdlet sono necessari per configurare l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="cfea7-109">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="cfea7-110">Questi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="cfea7-110">These cmdlets are:</span></span>
- <span data-ttu-id="cfea7-111">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="cfea7-111">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="cfea7-112">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="cfea7-112">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="cfea7-113">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="cfea7-113">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="cfea7-114">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="cfea7-114">Add-AzVmssExtension</span></span>

## <span data-ttu-id="cfea7-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cfea7-115">EXAMPLES</span></span>

### <span data-ttu-id="cfea7-116">Esempio 1: creare un oggetto di configurazione VMSS</span><span class="sxs-lookup"><span data-stu-id="cfea7-116">Example 1: Create a VMSS configuration object</span></span>
```powershell
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

<span data-ttu-id="cfea7-117">Questo esempio crea un oggetto di configurazione VMSS.</span><span class="sxs-lookup"><span data-stu-id="cfea7-117">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="cfea7-118">Il primo comando usa il cmdlet **New-AzVmssConfig** per creare un oggetto di configurazione vmss e archivia il risultato nella variabile denominata $vmss.</span><span class="sxs-lookup"><span data-stu-id="cfea7-118">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="cfea7-119">Il secondo comando usa il cmdlet **New-AzVmss** per creare un vmss che usa l'oggetto di configurazione vmss creato nel primo comando.</span><span class="sxs-lookup"><span data-stu-id="cfea7-119">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

### <span data-ttu-id="cfea7-120">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="cfea7-120">Example 2</span></span>

<span data-ttu-id="cfea7-121">Crea un oggetto di configurazione VMSS.</span><span class="sxs-lookup"><span data-stu-id="cfea7-121">Creates a VMSS configuration object.</span></span> <span data-ttu-id="cfea7-122">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="cfea7-122">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzVmssConfig -Location <String> -Overprovision $false -SkuCapacity 2 -SkuName 'Standard_A0' -Tag 'Sql' -UpgradePolicyMode Automatic
```

## <span data-ttu-id="cfea7-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cfea7-123">PARAMETERS</span></span>

### <span data-ttu-id="cfea7-124">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="cfea7-124">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="cfea7-125">La quantità di tempo per cui vengono sospese le riparazioni automatiche a causa di una modifica dello stato in VM.</span><span class="sxs-lookup"><span data-stu-id="cfea7-125">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="cfea7-126">Il tempo di grazia viene avviato dopo il completamento della modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="cfea7-126">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="cfea7-127">Questo consente di evitare riparazioni premature o accidentali.</span><span class="sxs-lookup"><span data-stu-id="cfea7-127">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="cfea7-128">La durata dell'ora deve essere specificata nel formato ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="cfea7-128">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="cfea7-129">Il periodo di tolleranza minimo consentito è di 30 minuti (PT30M), che è anche il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="cfea7-129">The minimum allowed grace period is 30 minutes (PT30M), which is also the default value.</span></span> <span data-ttu-id="cfea7-130">Il periodo di tolleranza massimo consentito è di 90 minuti (PT90M).</span><span class="sxs-lookup"><span data-stu-id="cfea7-130">The maximum allowed grace period is 90 minutes (PT90M).</span></span>

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

### <span data-ttu-id="cfea7-131">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="cfea7-131">-AutoOSUpgrade</span></span>
<span data-ttu-id="cfea7-132">Imposta se gli aggiornamenti del sistema operativo devono essere applicati automaticamente alle istanze del set di scala in modo scorrevole quando una versione più recente dell'immagine diventa disponibile.</span><span class="sxs-lookup"><span data-stu-id="cfea7-132">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="cfea7-133">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="cfea7-133">-BootDiagnostic</span></span>
<span data-ttu-id="cfea7-134">Specifica il profilo set di diagnostica di avvio della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="cfea7-134">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="cfea7-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfea7-135">-DefaultProfile</span></span>
<span data-ttu-id="cfea7-136">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cfea7-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cfea7-137">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="cfea7-137">-DisableAutoRollback</span></span>
<span data-ttu-id="cfea7-138">Disabilitare il rollback automatico per i criteri di aggiornamento del sistema operativo automatico</span><span class="sxs-lookup"><span data-stu-id="cfea7-138">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="cfea7-139">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="cfea7-139">-EnableAutomaticRepair</span></span>
<span data-ttu-id="cfea7-140">Consente la riparazione automatica nel set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="cfea7-140">Enables automatic repairs on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="cfea7-141">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="cfea7-141">-EnableUltraSSD</span></span>
<span data-ttu-id="cfea7-142">Consente a una funzionalità di avere uno o più dischi di dati gestiti con UltraSSD_LRS tipo di account di archiviazione nel set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="cfea7-142">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="cfea7-143">Dischi gestiti con tipo di account di archiviazione UltraSSD_LRS può essere aggiunto a un VMSS solo se questa proprietà è abilitata.</span><span class="sxs-lookup"><span data-stu-id="cfea7-143">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="cfea7-144">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="cfea7-144">-EncryptionAtHost</span></span>
<span data-ttu-id="cfea7-145">Questo parametro consentirà la crittografia per tutti i dischi, incluso il disco Resource/Temp all'host stesso.</span><span class="sxs-lookup"><span data-stu-id="cfea7-145">This parameter will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="cfea7-146">Impostazione predefinita: la crittografia all'host verrà disabilitata a meno che questa proprietà non sia impostata su true per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="cfea7-146">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

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

### <span data-ttu-id="cfea7-147">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="cfea7-147">-EvictionPolicy</span></span>
<span data-ttu-id="cfea7-148">Specifica i criteri di eliminazione per le macchine virtuali nel set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="cfea7-148">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="cfea7-149">-Extension</span><span class="sxs-lookup"><span data-stu-id="cfea7-149">-Extension</span></span>
<span data-ttu-id="cfea7-150">Specifica l'oggetto informazioni sull'estensione per VMSS.</span><span class="sxs-lookup"><span data-stu-id="cfea7-150">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="cfea7-151">Puoi usare il cmdlet **Add-AzVmssExtension** per aggiungere questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="cfea7-151">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="cfea7-152">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="cfea7-152">-HealthProbeId</span></span>
<span data-ttu-id="cfea7-153">Specifica l'ID di un probe di bilanciamento del carico usato per determinare lo stato di un'istanza nel set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="cfea7-153">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="cfea7-154">HealthProbeId è sotto forma di '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span><span class="sxs-lookup"><span data-stu-id="cfea7-154">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="cfea7-155">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="cfea7-155">-IdentityId</span></span>
<span data-ttu-id="cfea7-156">Specifica l'elenco delle identità utente associate al set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="cfea7-156">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="cfea7-157">I riferimenti di identità utente saranno ID delle risorse ARM nella forma:'/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="cfea7-157">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="cfea7-158">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="cfea7-158">-IdentityType</span></span>
<span data-ttu-id="cfea7-159">Specifica il tipo di identità usato per il set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="cfea7-159">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="cfea7-160">Il tipo ' SystemAssignedUserAssigned ' include sia un'identità creata in modo implicito che un set di identità assegnate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="cfea7-160">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="cfea7-161">Il tipo "None" rimuoverà le identità dal set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="cfea7-161">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="cfea7-162">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="cfea7-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cfea7-163">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="cfea7-163">SystemAssigned</span></span>
- <span data-ttu-id="cfea7-164">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="cfea7-164">UserAssigned</span></span>
- <span data-ttu-id="cfea7-165">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="cfea7-165">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="cfea7-166">Nessuno</span><span class="sxs-lookup"><span data-stu-id="cfea7-166">None</span></span>

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

### <span data-ttu-id="cfea7-167">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="cfea7-167">-LicenseType</span></span>
<span data-ttu-id="cfea7-168">Specificare il tipo di licenza, che è per portare il proprio scenario di licenza.</span><span class="sxs-lookup"><span data-stu-id="cfea7-168">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="cfea7-169">-Posizione</span><span class="sxs-lookup"><span data-stu-id="cfea7-169">-Location</span></span>
<span data-ttu-id="cfea7-170">Specifica la posizione di Azure in cui viene creato VMSS.</span><span class="sxs-lookup"><span data-stu-id="cfea7-170">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="cfea7-171">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="cfea7-171">-MaxPrice</span></span>
<span data-ttu-id="cfea7-172">Specifica il prezzo massimo che si vuole pagare per una VM/VMSS spot.</span><span class="sxs-lookup"><span data-stu-id="cfea7-172">Specifies the maximum price you are willing to pay for a Spot VM/VMSS.</span></span> <span data-ttu-id="cfea7-173">Questo prezzo è in dollari USA.</span><span class="sxs-lookup"><span data-stu-id="cfea7-173">This price is in US Dollars.</span></span> <span data-ttu-id="cfea7-174">Questo prezzo verrà confrontato con il prezzo a pronti corrente per le dimensioni della VM.</span><span class="sxs-lookup"><span data-stu-id="cfea7-174">This price will be compared with the current Spot price for the VM size.</span></span> <span data-ttu-id="cfea7-175">Inoltre, i prezzi vengono confrontati al momento della creazione/aggiornamento di spot VM/VMSS e l'operazione avrà esito positivo solo se maxPrice è maggiore del prezzo a pronti corrente.</span><span class="sxs-lookup"><span data-stu-id="cfea7-175">Also, the prices are compared at the time of create/update of Spot VM/VMSS and the operation will only succeed if the maxPrice is greater than the current Spot price.</span></span> <span data-ttu-id="cfea7-176">Il maxPrice verrà usato anche per rimuovere un punto VM/VMSS se il prezzo spot corrente supera il maxPrice dopo la creazione di VM/VMSS.</span><span class="sxs-lookup"><span data-stu-id="cfea7-176">The maxPrice will also be used for evicting a Spot VM/VMSS if the current Spot price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="cfea7-177">I valori possibili sono: qualsiasi valore decimale maggiore di zero.</span><span class="sxs-lookup"><span data-stu-id="cfea7-177">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="cfea7-178">Esempio: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="cfea7-178">Example: 0.01538.</span></span>  <span data-ttu-id="cfea7-179">-1 indica che lo spot VM/VMSS non deve essere rimosso per motivi di prezzo.</span><span class="sxs-lookup"><span data-stu-id="cfea7-179">-1 indicates that the Spot VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="cfea7-180">Inoltre, il prezzo massimo predefinito è-1 se non è fornito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="cfea7-180">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="cfea7-181">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="cfea7-181">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="cfea7-182">Specifica l'oggetto profilo di rete che contiene le proprietà di rete per la configurazione di VMSS.</span><span class="sxs-lookup"><span data-stu-id="cfea7-182">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="cfea7-183">Puoi usare il cmdlet **Add-AzVmssNetworkInterfaceConfiguration** per aggiungere questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="cfea7-183">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="cfea7-184">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="cfea7-184">-OsProfile</span></span>
<span data-ttu-id="cfea7-185">Specifica l'oggetto del profilo del sistema operativo che contiene le proprietà del sistema operativo per la configurazione di VMSS.</span><span class="sxs-lookup"><span data-stu-id="cfea7-185">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="cfea7-186">Puoi usare il cmdlet **set-AzVmssOsProfile** per impostare questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="cfea7-186">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="cfea7-187">-Provisioning</span><span class="sxs-lookup"><span data-stu-id="cfea7-187">-Overprovision</span></span>
<span data-ttu-id="cfea7-188">Indica se il cmdlet viene sovradisposto da VMSS.</span><span class="sxs-lookup"><span data-stu-id="cfea7-188">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="cfea7-189">-PlanName</span><span class="sxs-lookup"><span data-stu-id="cfea7-189">-PlanName</span></span>
<span data-ttu-id="cfea7-190">Specifica il nome del piano.</span><span class="sxs-lookup"><span data-stu-id="cfea7-190">Specifies the plan name.</span></span>

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

### <span data-ttu-id="cfea7-191">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="cfea7-191">-PlanProduct</span></span>
<span data-ttu-id="cfea7-192">Specifica il prodotto piano.</span><span class="sxs-lookup"><span data-stu-id="cfea7-192">Specifies the plan product.</span></span>

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

### <span data-ttu-id="cfea7-193">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="cfea7-193">-PlanPromotionCode</span></span>
<span data-ttu-id="cfea7-194">Specifica il codice promozionale per il piano.</span><span class="sxs-lookup"><span data-stu-id="cfea7-194">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="cfea7-195">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="cfea7-195">-PlanPublisher</span></span>
<span data-ttu-id="cfea7-196">Specifica il piano Publisher.</span><span class="sxs-lookup"><span data-stu-id="cfea7-196">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="cfea7-197">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="cfea7-197">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="cfea7-198">Conteggio dei domini di errore per ogni gruppo di posizionamento.</span><span class="sxs-lookup"><span data-stu-id="cfea7-198">Fault Domain count for each placement group.</span></span>

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

### <span data-ttu-id="cfea7-199">-Priorità</span><span class="sxs-lookup"><span data-stu-id="cfea7-199">-Priority</span></span>
<span data-ttu-id="cfea7-200">Priorità per il machio virtuale nel set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="cfea7-200">The priority for the virtual machien in the scale set.</span></span>  <span data-ttu-id="cfea7-201">Solo i valori supportati sono "regolari", "spot" e "low".</span><span class="sxs-lookup"><span data-stu-id="cfea7-201">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="cfea7-202">"Normale" è per la normale macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="cfea7-202">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="cfea7-203">"Spot" è per la macchina virtuale spot.</span><span class="sxs-lookup"><span data-stu-id="cfea7-203">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="cfea7-204">"Basso" è anche per la macchina virtuale spot, ma è sostituito da "spot".</span><span class="sxs-lookup"><span data-stu-id="cfea7-204">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="cfea7-205">Usare "spot" invece di "low".</span><span class="sxs-lookup"><span data-stu-id="cfea7-205">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="cfea7-206">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="cfea7-206">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="cfea7-207">ID risorsa del gruppo di posizionamento di prossimità da usare con questo set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="cfea7-207">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="cfea7-208">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="cfea7-208">-RollingUpgradePolicy</span></span>
<span data-ttu-id="cfea7-209">Specifica i criteri di aggiornamento a rotazione.</span><span class="sxs-lookup"><span data-stu-id="cfea7-209">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="cfea7-210">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="cfea7-210">-ScaleInPolicy</span></span>
<span data-ttu-id="cfea7-211">Regole da seguire durante la scalabilità in una scala macchina virtuale impostata.</span><span class="sxs-lookup"><span data-stu-id="cfea7-211">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="cfea7-212">I valori possibili sono: "default", "OldestVM" e "NewestVM".</span><span class="sxs-lookup"><span data-stu-id="cfea7-212">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="cfea7-213">"Impostazione predefinita" quando un set di scale di una macchina virtuale viene ridimensionato, il set di proporzioni sarà prima di tutto bilanciato tra le zone se si tratta di un set di scala zonale.</span><span class="sxs-lookup"><span data-stu-id="cfea7-213">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="cfea7-214">Verrà quindi bilanciato tra i domini di errore il più lontano possibile.</span><span class="sxs-lookup"><span data-stu-id="cfea7-214">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="cfea7-215">All'interno di ogni dominio di errore, le macchine virtuali scelte per la rimozione saranno quelle più recenti che non sono protette da scale-in.</span><span class="sxs-lookup"><span data-stu-id="cfea7-215">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="cfea7-216">' OldestVM ' quando un set di scale della macchina virtuale viene ridimensionato, le macchine virtuali meno recenti che non sono protette da scale-in verranno scelte per la rimozione.</span><span class="sxs-lookup"><span data-stu-id="cfea7-216">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="cfea7-217">Per i set di scale della macchina virtuale zonale, il set di proporzioni verrà prima bilanciato tra le aree.</span><span class="sxs-lookup"><span data-stu-id="cfea7-217">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="cfea7-218">All'interno di ogni zona le macchine virtuali meno recenti che non sono protette verranno scelte per la rimozione.</span><span class="sxs-lookup"><span data-stu-id="cfea7-218">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="cfea7-219">' NewestVM ' quando un set di scale della macchina virtuale viene ridimensionato, le macchine virtuali più recenti che non sono protette da scale-in verranno scelte per la rimozione.</span><span class="sxs-lookup"><span data-stu-id="cfea7-219">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="cfea7-220">Per i set di scale della macchina virtuale zonale, il set di proporzioni verrà prima bilanciato tra le aree.</span><span class="sxs-lookup"><span data-stu-id="cfea7-220">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="cfea7-221">All'interno di ogni zona le macchine virtuali più recenti che non sono protette verranno scelte per la rimozione.</span><span class="sxs-lookup"><span data-stu-id="cfea7-221">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

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

### <span data-ttu-id="cfea7-222">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="cfea7-222">-SinglePlacementGroup</span></span>
<span data-ttu-id="cfea7-223">Specifica il gruppo di posizionamento singolo.</span><span class="sxs-lookup"><span data-stu-id="cfea7-223">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="cfea7-224">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="cfea7-224">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="cfea7-225">Specifica che le estensioni non vengono eseguite sulle VM extra provisioning.</span><span class="sxs-lookup"><span data-stu-id="cfea7-225">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="cfea7-226">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="cfea7-226">-SkuCapacity</span></span>
<span data-ttu-id="cfea7-227">Specifica il numero di istanze in VMSS.</span><span class="sxs-lookup"><span data-stu-id="cfea7-227">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="cfea7-228">-SkuName</span><span class="sxs-lookup"><span data-stu-id="cfea7-228">-SkuName</span></span>
<span data-ttu-id="cfea7-229">Specifica le dimensioni di tutte le istanze di VMSS.</span><span class="sxs-lookup"><span data-stu-id="cfea7-229">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="cfea7-230">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="cfea7-230">-SkuTier</span></span>
<span data-ttu-id="cfea7-231">Specifica il livello di VMSS.</span><span class="sxs-lookup"><span data-stu-id="cfea7-231">Specifies the tier of VMSS.</span></span> <span data-ttu-id="cfea7-232">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="cfea7-232">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cfea7-233">Standard</span><span class="sxs-lookup"><span data-stu-id="cfea7-233">Standard</span></span>
- <span data-ttu-id="cfea7-234">Base</span><span class="sxs-lookup"><span data-stu-id="cfea7-234">Basic</span></span>

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

### <span data-ttu-id="cfea7-235">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="cfea7-235">-StorageProfile</span></span>
<span data-ttu-id="cfea7-236">Specifica l'oggetto profilo di archiviazione che contiene le proprietà del disco per la configurazione di VMSS.</span><span class="sxs-lookup"><span data-stu-id="cfea7-236">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="cfea7-237">Puoi usare il cmdlet **set-AzVmssStorageProfile** per impostare questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="cfea7-237">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="cfea7-238">-Tag</span><span class="sxs-lookup"><span data-stu-id="cfea7-238">-Tag</span></span>
<span data-ttu-id="cfea7-239">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="cfea7-239">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="cfea7-240">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="cfea7-240">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="cfea7-241">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="cfea7-241">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="cfea7-242">Intervallo di tempo configurabile (in minuti) una macchina virtuale che viene eliminata dovrà approvare l'evento di terminazione pianificata prima che l'evento venga approvato automaticamente (scaduta).</span><span class="sxs-lookup"><span data-stu-id="cfea7-242">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="cfea7-243">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="cfea7-243">-TerminateScheduledEvents</span></span>
<span data-ttu-id="cfea7-244">Abilitare gli eventi pianificati di terminazione</span><span class="sxs-lookup"><span data-stu-id="cfea7-244">Enable the Terminate Scheduled events</span></span>

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

### <span data-ttu-id="cfea7-245">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="cfea7-245">-UpgradePolicyMode</span></span>
<span data-ttu-id="cfea7-246">Specifica la modalità di aggiornamento delle macchine virtuali nel set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="cfea7-246">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="cfea7-247">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="cfea7-247">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cfea7-248">Automatico</span><span class="sxs-lookup"><span data-stu-id="cfea7-248">Automatic</span></span>
- <span data-ttu-id="cfea7-249">Manuale</span><span class="sxs-lookup"><span data-stu-id="cfea7-249">Manual</span></span>

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

### <span data-ttu-id="cfea7-250">-Zona</span><span class="sxs-lookup"><span data-stu-id="cfea7-250">-Zone</span></span>
<span data-ttu-id="cfea7-251">Specifica l'elenco delle aree per il set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="cfea7-251">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="cfea7-252">-ZoneBalance</span><span class="sxs-lookup"><span data-stu-id="cfea7-252">-ZoneBalance</span></span>
<span data-ttu-id="cfea7-253">Se è necessario forzare la distribuzione rigorosa della macchina virtuale tra le aree x in caso di interruzioni di zona.</span><span class="sxs-lookup"><span data-stu-id="cfea7-253">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="cfea7-254">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cfea7-254">-Confirm</span></span>
<span data-ttu-id="cfea7-255">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cfea7-255">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfea7-256">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfea7-256">-WhatIf</span></span>
<span data-ttu-id="cfea7-257">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cfea7-257">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cfea7-258">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cfea7-258">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfea7-259">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfea7-259">CommonParameters</span></span>
<span data-ttu-id="cfea7-260">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfea7-260">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfea7-261">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cfea7-261">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfea7-262">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cfea7-262">INPUTS</span></span>

### <span data-ttu-id="cfea7-263">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="cfea7-263">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="cfea7-264">System. String</span><span class="sxs-lookup"><span data-stu-id="cfea7-264">System.String</span></span>

### <span data-ttu-id="cfea7-265">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="cfea7-265">System.Collections.Hashtable</span></span>

### <span data-ttu-id="cfea7-266">System. Int32</span><span class="sxs-lookup"><span data-stu-id="cfea7-266">System.Int32</span></span>

### <span data-ttu-id="cfea7-267">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. UpgradeMode, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="cfea7-267">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="cfea7-268">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetOSProfile</span><span class="sxs-lookup"><span data-stu-id="cfea7-268">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="cfea7-269">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetStorageProfile</span><span class="sxs-lookup"><span data-stu-id="cfea7-269">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="cfea7-270">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetNetworkConfiguration []</span><span class="sxs-lookup"><span data-stu-id="cfea7-270">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="cfea7-271">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetExtension []</span><span class="sxs-lookup"><span data-stu-id="cfea7-271">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="cfea7-272">System. String []</span><span class="sxs-lookup"><span data-stu-id="cfea7-272">System.String[]</span></span>

### <span data-ttu-id="cfea7-273">Microsoft. Azure. Management. Compute. Models. RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="cfea7-273">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="cfea7-274">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="cfea7-274">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="cfea7-275">Microsoft. Azure. Management. Compute. Models. BootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="cfea7-275">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="cfea7-276">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. ResourceIdentityType, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="cfea7-276">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="cfea7-277">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cfea7-277">OUTPUTS</span></span>

### <span data-ttu-id="cfea7-278">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="cfea7-278">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="cfea7-279">Note</span><span class="sxs-lookup"><span data-stu-id="cfea7-279">NOTES</span></span>

## <span data-ttu-id="cfea7-280">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cfea7-280">RELATED LINKS</span></span>

[<span data-ttu-id="cfea7-281">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="cfea7-281">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="cfea7-282">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="cfea7-282">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="cfea7-283">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="cfea7-283">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="cfea7-284">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="cfea7-284">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="cfea7-285">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cfea7-285">New-AzVmss</span></span>](./New-AzVmss.md)
