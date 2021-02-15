---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: 4fdfd5c5da9cc803cacdd2aca90b7f66771988fd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177647"
---
# <span data-ttu-id="00465-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="00465-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="00465-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00465-102">SYNOPSIS</span></span>
<span data-ttu-id="00465-103">Crea un oggetto di configurazione VMSS.</span><span class="sxs-lookup"><span data-stu-id="00465-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="00465-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="00465-104">SYNTAX</span></span>

### <span data-ttu-id="00465-105">DefaultParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="00465-105">DefaultParameterSet (Default)</span></span>
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

### <span data-ttu-id="00465-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="00465-106">ExplicitIdentityParameterSet</span></span>
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

## <span data-ttu-id="00465-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="00465-107">DESCRIPTION</span></span>
<span data-ttu-id="00465-108">Il cmdlet **New-AzVmssConfig** crea un oggetto VMSS (Virtual Manager Scale Set) locale configurabile.</span><span class="sxs-lookup"><span data-stu-id="00465-108">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="00465-109">Altri cmdlet sono necessari per configurare l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="00465-109">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="00465-110">Questi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="00465-110">These cmdlets are:</span></span>
- <span data-ttu-id="00465-111">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="00465-111">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="00465-112">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="00465-112">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="00465-113">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="00465-113">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="00465-114">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="00465-114">Add-AzVmssExtension</span></span>

## <span data-ttu-id="00465-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="00465-115">EXAMPLES</span></span>

### <span data-ttu-id="00465-116">Esempio 1: Creare un oggetto configurazione VMSS</span><span class="sxs-lookup"><span data-stu-id="00465-116">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="00465-117">Questo esempio crea un oggetto di configurazione VMSS.</span><span class="sxs-lookup"><span data-stu-id="00465-117">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="00465-118">Il primo comando usa il cmdlet **New-AzVmssConfig** per creare un oggetto di configurazione VMSS e archivia il risultato nella variabile $VMSS.</span><span class="sxs-lookup"><span data-stu-id="00465-118">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="00465-119">Il secondo comando usa il cmdlet **New-AzVmss** per creare un VMSS che usa l'oggetto configurazione VMSS creato nel primo comando.</span><span class="sxs-lookup"><span data-stu-id="00465-119">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

### <span data-ttu-id="00465-120">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="00465-120">Example 2</span></span>

<span data-ttu-id="00465-121">Crea un oggetto di configurazione VMSS.</span><span class="sxs-lookup"><span data-stu-id="00465-121">Creates a VMSS configuration object.</span></span> <span data-ttu-id="00465-122">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="00465-122">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzVmssConfig -Location <String> -Overprovision $false -SkuCapacity 2 -SkuName 'Standard_A0' -Tag 'Sql' -UpgradePolicyMode Automatic
```

## <span data-ttu-id="00465-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00465-123">PARAMETERS</span></span>

### <span data-ttu-id="00465-124">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="00465-124">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="00465-125">La quantità di tempo per cui le riparazioni automatiche vengono sospese a causa di una modifica di stato nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="00465-125">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="00465-126">Il tempo di tolleranza inizia al termine della modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="00465-126">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="00465-127">In questo modo si evitano riparazioni accidentali o accidentali.</span><span class="sxs-lookup"><span data-stu-id="00465-127">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="00465-128">La durata dell'ora deve essere specificata nel formato ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="00465-128">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="00465-129">Il periodo di tolleranza minimo consentito è 30 minuti (PT30M), che è anche il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="00465-129">The minimum allowed grace period is 30 minutes (PT30M), which is also the default value.</span></span> <span data-ttu-id="00465-130">Il periodo di tolleranza massimo consentito è 90 minuti (PT90M).</span><span class="sxs-lookup"><span data-stu-id="00465-130">The maximum allowed grace period is 90 minutes (PT90M).</span></span>

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

### <span data-ttu-id="00465-131">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="00465-131">-AutoOSUpgrade</span></span>
<span data-ttu-id="00465-132">Imposta se gli aggiornamenti del sistema operativo devono essere applicati automaticamente a istanze di set di scala in modalità di distribuzione quando diventa disponibile una versione più recente dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="00465-132">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="00465-133">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="00465-133">-BootDiagnostic</span></span>
<span data-ttu-id="00465-134">Specifica il profilo di diagnostica di avvio impostato per il set di dimensioni della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="00465-134">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="00465-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00465-135">-DefaultProfile</span></span>
<span data-ttu-id="00465-136">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="00465-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00465-137">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="00465-137">-DisableAutoRollback</span></span>
<span data-ttu-id="00465-138">Disabilitare il rollback automatico per i criteri di aggiornamento automatico del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="00465-138">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="00465-139">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="00465-139">-EnableAutomaticRepair</span></span>
<span data-ttu-id="00465-140">Abilita le riparazioni automatiche nel set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="00465-140">Enables automatic repairs on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="00465-141">-EnableUltrasSD</span><span class="sxs-lookup"><span data-stu-id="00465-141">-EnableUltraSSD</span></span>
<span data-ttu-id="00465-142">Consente di avere uno o più dischi dati gestiti con un UltraSSD_LRS di account di archiviazione nel set di scalabilità della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="00465-142">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="00465-143">I dischi gestiti con tipo di account di UltraSSD_LRS possono essere aggiunti a un sistema VMSS solo se questa proprietà è abilitata.</span><span class="sxs-lookup"><span data-stu-id="00465-143">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="00465-144">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="00465-144">-EncryptionAtHost</span></span>
<span data-ttu-id="00465-145">Questo parametro abiliterà la crittografia per tutti i dischi, incluso il disco Risorsa/Temp nell'host stesso.</span><span class="sxs-lookup"><span data-stu-id="00465-145">This parameter will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="00465-146">Impostazione predefinita: la crittografia nell'host verrà disabilitata a meno che questa proprietà non sia impostata su true per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="00465-146">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

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

### <span data-ttu-id="00465-147">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="00465-147">-EvictionPolicy</span></span>
<span data-ttu-id="00465-148">Specifica i criteri di sgomento per le macchine virtuali nel set di scala.</span><span class="sxs-lookup"><span data-stu-id="00465-148">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="00465-149">-Extension</span><span class="sxs-lookup"><span data-stu-id="00465-149">-Extension</span></span>
<span data-ttu-id="00465-150">Specifica l'oggetto informazioni sull'estensione per il sistema VMSS.</span><span class="sxs-lookup"><span data-stu-id="00465-150">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="00465-151">È possibile usare il cmdlet **Add-AzVmssExtension** per aggiungere l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="00465-151">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="00465-152">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="00465-152">-HealthProbeId</span></span>
<span data-ttu-id="00465-153">Specifica l'ID di una bilanciamento del carico usato per determinare l'integrità di un'istanza nel set di scalabilità della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="00465-153">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="00465-154">HealthProbeId ha il formato '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/azures/{resourceGroupName}'.</span><span class="sxs-lookup"><span data-stu-id="00465-154">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="00465-155">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="00465-155">-IdentityId</span></span>
<span data-ttu-id="00465-156">Specifica l'elenco delle identità utente associate al set di scalabilità delle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="00465-156">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="00465-157">I riferimenti di identità utente ARM id risorsa nel formato '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="00465-157">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="00465-158">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="00465-158">-IdentityType</span></span>
<span data-ttu-id="00465-159">Specifica il tipo di identità usato per il set di scalabilità delle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="00465-159">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="00465-160">Il tipo 'SystemAssignedUserAssigned' include sia un'identità creata in modo implicito che un set di identità assegnate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="00465-160">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="00465-161">Il tipo "Nessuna" rimuove le identità dal set di scalabilità delle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="00465-161">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="00465-162">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="00465-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="00465-163">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="00465-163">SystemAssigned</span></span>
- <span data-ttu-id="00465-164">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="00465-164">UserAssigned</span></span>
- <span data-ttu-id="00465-165">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="00465-165">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="00465-166">Nessuno</span><span class="sxs-lookup"><span data-stu-id="00465-166">None</span></span>

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

### <span data-ttu-id="00465-167">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="00465-167">-LicenseType</span></span>
<span data-ttu-id="00465-168">Specificare il tipo di licenza, ad esempio per portare il proprio scenario di licenza.</span><span class="sxs-lookup"><span data-stu-id="00465-168">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="00465-169">-Location</span><span class="sxs-lookup"><span data-stu-id="00465-169">-Location</span></span>
<span data-ttu-id="00465-170">Specifica la posizione di Azure in cui viene creato il sistema VMSS.</span><span class="sxs-lookup"><span data-stu-id="00465-170">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="00465-171">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="00465-171">-MaxPrice</span></span>
<span data-ttu-id="00465-172">Specifica il prezzo massimo che sei disposto a pagare per una macchina virtuale/VMSS Spot.</span><span class="sxs-lookup"><span data-stu-id="00465-172">Specifies the maximum price you are willing to pay for a Spot VM/VMSS.</span></span> <span data-ttu-id="00465-173">Questo prezzo è in dollari statunitensi.</span><span class="sxs-lookup"><span data-stu-id="00465-173">This price is in US Dollars.</span></span> <span data-ttu-id="00465-174">Questo prezzo verrà confrontato con il prezzo spot corrente per le dimensioni della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="00465-174">This price will be compared with the current Spot price for the VM size.</span></span> <span data-ttu-id="00465-175">Inoltre, i prezzi vengono confrontati al momento della creazione/aggiornamento di Spot VM/VMSS e l'operazione avrà esito positivo solo se maxPrice è maggiore del prezzo spot corrente.</span><span class="sxs-lookup"><span data-stu-id="00465-175">Also, the prices are compared at the time of create/update of Spot VM/VMSS and the operation will only succeed if the maxPrice is greater than the current Spot price.</span></span> <span data-ttu-id="00465-176">MaxPrice verrà usato anche per l'eliminazione di una VM/VMSS Spot se il prezzo spot corrente supera il valore maxPrice dopo la creazione di VM/VMSS.</span><span class="sxs-lookup"><span data-stu-id="00465-176">The maxPrice will also be used for evicting a Spot VM/VMSS if the current Spot price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="00465-177">I valori possibili sono: qualsiasi valore decimale maggiore di zero.</span><span class="sxs-lookup"><span data-stu-id="00465-177">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="00465-178">Esempio: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="00465-178">Example: 0.01538.</span></span>  <span data-ttu-id="00465-179">-1 indica che non è consigliabile sgombera la macchina virtuale/VMS Spot per motivi di prezzo.</span><span class="sxs-lookup"><span data-stu-id="00465-179">-1 indicates that the Spot VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="00465-180">Inoltre, il prezzo massimo predefinito è -1 se non è fornito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="00465-180">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="00465-181">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="00465-181">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="00465-182">Specifica l'oggetto profilo di rete che contiene le proprietà di rete per la configurazione di VMSS.</span><span class="sxs-lookup"><span data-stu-id="00465-182">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="00465-183">È possibile usare il cmdlet **Add-AzVmssNetworkInterfaceConfiguration** per aggiungere questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="00465-183">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="00465-184">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="00465-184">-OsProfile</span></span>
<span data-ttu-id="00465-185">Specifica l'oggetto profilo del sistema operativo che contiene le proprietà del sistema operativo per la configurazione VMSS.</span><span class="sxs-lookup"><span data-stu-id="00465-185">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="00465-186">È possibile usare il cmdlet **Set-AzVmssOsProfile** per impostare questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="00465-186">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="00465-187">-Overprovision</span><span class="sxs-lookup"><span data-stu-id="00465-187">-Overprovision</span></span>
<span data-ttu-id="00465-188">Indica se il cmdlet ha eseguito l'overprovisioning di VMSS.</span><span class="sxs-lookup"><span data-stu-id="00465-188">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="00465-189">-PlanName</span><span class="sxs-lookup"><span data-stu-id="00465-189">-PlanName</span></span>
<span data-ttu-id="00465-190">Specifica il nome del piano.</span><span class="sxs-lookup"><span data-stu-id="00465-190">Specifies the plan name.</span></span>

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

### <span data-ttu-id="00465-191">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="00465-191">-PlanProduct</span></span>
<span data-ttu-id="00465-192">Specifica il prodotto del piano.</span><span class="sxs-lookup"><span data-stu-id="00465-192">Specifies the plan product.</span></span>

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

### <span data-ttu-id="00465-193">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="00465-193">-PlanPromotionCode</span></span>
<span data-ttu-id="00465-194">Specifica il codice promozionale del piano.</span><span class="sxs-lookup"><span data-stu-id="00465-194">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="00465-195">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="00465-195">-PlanPublisher</span></span>
<span data-ttu-id="00465-196">Specifica l'autore del piano.</span><span class="sxs-lookup"><span data-stu-id="00465-196">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="00465-197">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="00465-197">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="00465-198">Fault Domain count for each placement group.</span><span class="sxs-lookup"><span data-stu-id="00465-198">Fault Domain count for each placement group.</span></span>

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

### <span data-ttu-id="00465-199">-Priority</span><span class="sxs-lookup"><span data-stu-id="00465-199">-Priority</span></span>
<span data-ttu-id="00465-200">Priorità del machien virtuale nel set di scale.</span><span class="sxs-lookup"><span data-stu-id="00465-200">The priority for the virtual machien in the scale set.</span></span>  <span data-ttu-id="00465-201">Solo i valori supportati sono "Normale", "Posizione" e "Basso".</span><span class="sxs-lookup"><span data-stu-id="00465-201">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="00465-202">"Normale" è per la macchina virtuale normale.</span><span class="sxs-lookup"><span data-stu-id="00465-202">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="00465-203">"Spot" è per una macchina virtuale spot.</span><span class="sxs-lookup"><span data-stu-id="00465-203">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="00465-204">"Low" è anche per la macchina virtuale spot, ma viene sostituito da "Spot".</span><span class="sxs-lookup"><span data-stu-id="00465-204">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="00465-205">Usare "Spot" invece di "Low".</span><span class="sxs-lookup"><span data-stu-id="00465-205">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="00465-206">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="00465-206">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="00465-207">ID risorsa del gruppo di posizionamento di prossimità da usare con questo set di scale.</span><span class="sxs-lookup"><span data-stu-id="00465-207">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="00465-208">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="00465-208">-RollingUpgradePolicy</span></span>
<span data-ttu-id="00465-209">Specifica i criteri di aggiornamento in sequenza.</span><span class="sxs-lookup"><span data-stu-id="00465-209">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="00465-210">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="00465-210">-ScaleInPolicy</span></span>
<span data-ttu-id="00465-211">Regole da seguire quando si ridimensiona un set di scalabilità delle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="00465-211">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="00465-212">I valori possibili sono " Default", "OldestVM" e "NewestVM".</span><span class="sxs-lookup"><span data-stu-id="00465-212">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="00465-213">"Impostazione predefinita" quando un set di scalabilità delle macchine virtuali viene ridimensionato, viene prima bilanciato tra le aree, se si tratta di un set di scala di zona.</span><span class="sxs-lookup"><span data-stu-id="00465-213">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="00465-214">Quindi, verrà bilanciato il più possibile tra i domini di errore.</span><span class="sxs-lookup"><span data-stu-id="00465-214">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="00465-215">All'interno di ogni dominio di errore, le macchine virtuali scelte per la rimozione saranno le più recenti non protette dalla scalabilità.</span><span class="sxs-lookup"><span data-stu-id="00465-215">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="00465-216">Quando il set di scale di una macchina virtuale viene ridimensionato, per la rimozione vengono scelte le macchine virtuali meno recenti che non sono protette dal scale-in.</span><span class="sxs-lookup"><span data-stu-id="00465-216">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="00465-217">Per i set di scala delle macchine virtuali zonali, il set di scala verrà prima bilanciato tra più aree.</span><span class="sxs-lookup"><span data-stu-id="00465-217">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="00465-218">All'interno di ogni area vengono scelte le macchine virtuali meno recenti non protette per la rimozione.</span><span class="sxs-lookup"><span data-stu-id="00465-218">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="00465-219">Nel caso di un set di scale per macchine virtuali in fase di ridimensionamento, per la rimozione verranno scelte le macchine virtuali più recenti non protette dal scale-in.</span><span class="sxs-lookup"><span data-stu-id="00465-219">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="00465-220">Per i set di scala delle macchine virtuali zonali, il set di scala verrà prima bilanciato tra più aree.</span><span class="sxs-lookup"><span data-stu-id="00465-220">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="00465-221">All'interno di ogni area vengono scelte le macchine virtuali più recenti non protette per la rimozione.</span><span class="sxs-lookup"><span data-stu-id="00465-221">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

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

### <span data-ttu-id="00465-222">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="00465-222">-SinglePlacementGroup</span></span>
<span data-ttu-id="00465-223">Specifica il singolo gruppo di posizionamento.</span><span class="sxs-lookup"><span data-stu-id="00465-223">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="00465-224">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="00465-224">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="00465-225">Specifica che le estensioni non vengono eseguite nelle macchine virtuali con overprovisioning aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="00465-225">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="00465-226">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="00465-226">-SkuCapacity</span></span>
<span data-ttu-id="00465-227">Specifica il numero di istanze nel sistema VMSS.</span><span class="sxs-lookup"><span data-stu-id="00465-227">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="00465-228">-SKUName</span><span class="sxs-lookup"><span data-stu-id="00465-228">-SkuName</span></span>
<span data-ttu-id="00465-229">Specifica le dimensioni di tutte le istanze di VMSS.</span><span class="sxs-lookup"><span data-stu-id="00465-229">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="00465-230">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="00465-230">-SkuTier</span></span>
<span data-ttu-id="00465-231">Specifica il livello di VMSS.</span><span class="sxs-lookup"><span data-stu-id="00465-231">Specifies the tier of VMSS.</span></span> <span data-ttu-id="00465-232">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="00465-232">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="00465-233">Standard</span><span class="sxs-lookup"><span data-stu-id="00465-233">Standard</span></span>
- <span data-ttu-id="00465-234">Di base</span><span class="sxs-lookup"><span data-stu-id="00465-234">Basic</span></span>

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

### <span data-ttu-id="00465-235">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="00465-235">-StorageProfile</span></span>
<span data-ttu-id="00465-236">Specifica l'oggetto del profilo di archiviazione che contiene le proprietà del disco per la configurazione di VMSS.</span><span class="sxs-lookup"><span data-stu-id="00465-236">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="00465-237">È possibile usare il cmdlet **Set-AzVmssStorageProfile** per impostare questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="00465-237">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="00465-238">-Tag</span><span class="sxs-lookup"><span data-stu-id="00465-238">-Tag</span></span>
<span data-ttu-id="00465-239">Coppie chiave-valore sotto forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="00465-239">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="00465-240">Ad esempio: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="00465-240">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="00465-241">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="00465-241">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="00465-242">Il periodo di tempo (in minuti) configurabile per l'eliminazione di una macchina virtuale dovrà approvare potenzialmente l'evento terminate pianificato prima che l'evento venga approvato automaticamente (timeout).</span><span class="sxs-lookup"><span data-stu-id="00465-242">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="00465-243">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="00465-243">-TerminateScheduledEvents</span></span>
<span data-ttu-id="00465-244">Abilitare Terminate Scheduled Events</span><span class="sxs-lookup"><span data-stu-id="00465-244">Enable the Terminate Scheduled events</span></span>

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

### <span data-ttu-id="00465-245">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="00465-245">-UpgradePolicyMode</span></span>
<span data-ttu-id="00465-246">È stata specificata la modalità di un aggiornamento alle macchine virtuali nel set di scala.</span><span class="sxs-lookup"><span data-stu-id="00465-246">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="00465-247">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="00465-247">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="00465-248">Automatico</span><span class="sxs-lookup"><span data-stu-id="00465-248">Automatic</span></span>
- <span data-ttu-id="00465-249">Manuale</span><span class="sxs-lookup"><span data-stu-id="00465-249">Manual</span></span>

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

### <span data-ttu-id="00465-250">-Zone</span><span class="sxs-lookup"><span data-stu-id="00465-250">-Zone</span></span>
<span data-ttu-id="00465-251">Specifica l'elenco di zona per il set di scale per le macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="00465-251">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="00465-252">-ZoneBalance</span><span class="sxs-lookup"><span data-stu-id="00465-252">-ZoneBalance</span></span>
<span data-ttu-id="00465-253">Se forzare rigorosamente anche la distribuzione di macchine virtuali in aree x in caso di interruzione della zona.</span><span class="sxs-lookup"><span data-stu-id="00465-253">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="00465-254">-Confirm</span><span class="sxs-lookup"><span data-stu-id="00465-254">-Confirm</span></span>
<span data-ttu-id="00465-255">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00465-255">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00465-256">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00465-256">-WhatIf</span></span>
<span data-ttu-id="00465-257">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="00465-257">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="00465-258">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="00465-258">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00465-259">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00465-259">CommonParameters</span></span>
<span data-ttu-id="00465-260">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00465-260">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00465-261">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="00465-261">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00465-262">INPUT</span><span class="sxs-lookup"><span data-stu-id="00465-262">INPUTS</span></span>

### <span data-ttu-id="00465-263">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="00465-263">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="00465-264">System.String</span><span class="sxs-lookup"><span data-stu-id="00465-264">System.String</span></span>

### <span data-ttu-id="00465-265">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="00465-265">System.Collections.Hashtable</span></span>

### <span data-ttu-id="00465-266">System.Int32</span><span class="sxs-lookup"><span data-stu-id="00465-266">System.Int32</span></span>

### <span data-ttu-id="00465-267">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="00465-267">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="00465-268">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span><span class="sxs-lookup"><span data-stu-id="00465-268">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="00465-269">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span><span class="sxs-lookup"><span data-stu-id="00465-269">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="00465-270">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="00465-270">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="00465-271">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span><span class="sxs-lookup"><span data-stu-id="00465-271">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="00465-272">System.String[]</span><span class="sxs-lookup"><span data-stu-id="00465-272">System.String[]</span></span>

### <span data-ttu-id="00465-273">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="00465-273">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="00465-274">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="00465-274">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="00465-275">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="00465-275">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="00465-276">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="00465-276">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="00465-277">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="00465-277">OUTPUTS</span></span>

### <span data-ttu-id="00465-278">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="00465-278">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="00465-279">NOTE</span><span class="sxs-lookup"><span data-stu-id="00465-279">NOTES</span></span>

## <span data-ttu-id="00465-280">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="00465-280">RELATED LINKS</span></span>

[<span data-ttu-id="00465-281">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="00465-281">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="00465-282">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="00465-282">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="00465-283">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="00465-283">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="00465-284">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="00465-284">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="00465-285">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="00465-285">New-AzVmss</span></span>](./New-AzVmss.md)
