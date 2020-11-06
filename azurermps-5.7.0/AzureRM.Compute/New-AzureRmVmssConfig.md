---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssConfig.md
ms.openlocfilehash: 4b87c121368232769672c24bc5005f3a50bfd39a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512704"
---
# <span data-ttu-id="d43cd-101">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="d43cd-101">New-AzureRmVmssConfig</span></span>

## <span data-ttu-id="d43cd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d43cd-102">SYNOPSIS</span></span>
<span data-ttu-id="d43cd-103">Crea un oggetto di configurazione VMSS.</span><span class="sxs-lookup"><span data-stu-id="d43cd-103">Creates a VMSS configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d43cd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d43cd-104">SYNTAX</span></span>

```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int64>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-PlanName <String>]
 [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RecoveryPolicyMode <RecoveryMode>] [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>]
 [-IdentityType <ResourceIdentityType>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d43cd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d43cd-105">DESCRIPTION</span></span>
<span data-ttu-id="d43cd-106">Il cmdlet **New-AzureRmVmssConfig** crea un oggetto vmss (Virtual Manager scale set) configurabile.</span><span class="sxs-lookup"><span data-stu-id="d43cd-106">The **New-AzureRmVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span>
<span data-ttu-id="d43cd-107">Altri cmdlet sono necessari per configurare l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="d43cd-107">Other cmdlets are needed to configure the VMSS object.</span></span>
<span data-ttu-id="d43cd-108">Questi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="d43cd-108">These cmdlets are:</span></span>

- <span data-ttu-id="d43cd-109">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="d43cd-109">Set-AzureRmVmssOsProfile</span></span>
- <span data-ttu-id="d43cd-110">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="d43cd-110">Set-AzureRmVmssStorageProfile</span></span>
- <span data-ttu-id="d43cd-111">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="d43cd-111">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="d43cd-112">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="d43cd-112">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="d43cd-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d43cd-113">EXAMPLES</span></span>

### <span data-ttu-id="d43cd-114">Esempio 1: creare un oggetto di configurazione VMSS</span><span class="sxs-lookup"><span data-stu-id="d43cd-114">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="d43cd-115">Questo esempio crea un oggetto di configurazione VMSS.</span><span class="sxs-lookup"><span data-stu-id="d43cd-115">This example creates a VMSS configuration object.</span></span>
<span data-ttu-id="d43cd-116">Il primo comando usa il cmdlet **New-AzureRmVmssConfig** per creare un oggetto di configurazione vmss e archivia il risultato nella variabile denominata $vmss.</span><span class="sxs-lookup"><span data-stu-id="d43cd-116">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="d43cd-117">Il secondo comando usa il cmdlet **New-AzureRmVmss** per creare un vmss che usa l'oggetto di configurazione vmss creato nel primo comando.</span><span class="sxs-lookup"><span data-stu-id="d43cd-117">The second command uses the **New-AzureRmVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="d43cd-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d43cd-118">PARAMETERS</span></span>

### <span data-ttu-id="d43cd-119">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d43cd-119">-BootDiagnostic</span></span>
<span data-ttu-id="d43cd-120">Specifica il profilo set di diagnostica di avvio della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d43cd-120">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="d43cd-121">-Extension</span><span class="sxs-lookup"><span data-stu-id="d43cd-121">-Extension</span></span>
<span data-ttu-id="d43cd-122">Specifica l'oggetto informazioni sull'estensione per VMSS.</span><span class="sxs-lookup"><span data-stu-id="d43cd-122">Specifies the extension information object for the VMSS.</span></span>
<span data-ttu-id="d43cd-123">Puoi usare il cmdlet **Add-AzureRmVmssExtension** per aggiungere questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="d43cd-123">You can use the **Add-AzureRmVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="d43cd-124">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="d43cd-124">-IdentityType</span></span>
<span data-ttu-id="d43cd-125">Specificare l'identità del set di scale della macchina virtuale, se configurata.</span><span class="sxs-lookup"><span data-stu-id="d43cd-125">Specify the identity of the virtual machine scale set, if configured.</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d43cd-126">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="d43cd-126">-LicenseType</span></span>
<span data-ttu-id="d43cd-127">Specificare il tipo di licenza, che è per portare il proprio scenario di licenza.</span><span class="sxs-lookup"><span data-stu-id="d43cd-127">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="d43cd-128">-Posizione</span><span class="sxs-lookup"><span data-stu-id="d43cd-128">-Location</span></span>
<span data-ttu-id="d43cd-129">Specifica la posizione di Azure in cui viene creato VMSS.</span><span class="sxs-lookup"><span data-stu-id="d43cd-129">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="d43cd-130">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="d43cd-130">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="d43cd-131">Specifica l'oggetto profilo di rete che contiene le proprietà di rete per la configurazione di VMSS.</span><span class="sxs-lookup"><span data-stu-id="d43cd-131">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="d43cd-132">Puoi usare il cmdlet **Add-AzureRmVmssNetworkInterfaceConfiguration** per aggiungere questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="d43cd-132">You can use the **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="d43cd-133">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="d43cd-133">-OsProfile</span></span>
<span data-ttu-id="d43cd-134">Specifica l'oggetto del profilo del sistema operativo che contiene le proprietà del sistema operativo per la configurazione di VMSS.</span><span class="sxs-lookup"><span data-stu-id="d43cd-134">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="d43cd-135">Puoi usare il cmdlet **set-AzureRmVmssOsProfile** per impostare questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="d43cd-135">You can use the **Set-AzureRmVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="d43cd-136">-Provisioning</span><span class="sxs-lookup"><span data-stu-id="d43cd-136">-Overprovision</span></span>
<span data-ttu-id="d43cd-137">Indica se il cmdlet viene sovradisposto da VMSS.</span><span class="sxs-lookup"><span data-stu-id="d43cd-137">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="d43cd-138">-PlanName</span><span class="sxs-lookup"><span data-stu-id="d43cd-138">-PlanName</span></span>
<span data-ttu-id="d43cd-139">Specifica il nome del piano.</span><span class="sxs-lookup"><span data-stu-id="d43cd-139">Specifies the plan name.</span></span>

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

### <span data-ttu-id="d43cd-140">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="d43cd-140">-PlanProduct</span></span>
<span data-ttu-id="d43cd-141">Specifica il prodotto piano.</span><span class="sxs-lookup"><span data-stu-id="d43cd-141">Specifies the plan product.</span></span>

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

### <span data-ttu-id="d43cd-142">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="d43cd-142">-PlanPromotionCode</span></span>
<span data-ttu-id="d43cd-143">Specifica il codice promozionale per il piano.</span><span class="sxs-lookup"><span data-stu-id="d43cd-143">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="d43cd-144">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="d43cd-144">-PlanPublisher</span></span>
<span data-ttu-id="d43cd-145">Specifica il piano Publisher.</span><span class="sxs-lookup"><span data-stu-id="d43cd-145">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="d43cd-146">-RecoveryPolicyMode</span><span class="sxs-lookup"><span data-stu-id="d43cd-146">-RecoveryPolicyMode</span></span>
<span data-ttu-id="d43cd-147">Specificare i criteri di ripristino.</span><span class="sxs-lookup"><span data-stu-id="d43cd-147">Specify the recovery policy.</span></span>

```yaml
Type: RecoveryMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d43cd-148">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="d43cd-148">-SinglePlacementGroup</span></span>
<span data-ttu-id="d43cd-149">Specifica il gruppo di posizionamento singolo.</span><span class="sxs-lookup"><span data-stu-id="d43cd-149">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="d43cd-150">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="d43cd-150">-SkuCapacity</span></span>
<span data-ttu-id="d43cd-151">Specifica il numero di istanze in VMSS.</span><span class="sxs-lookup"><span data-stu-id="d43cd-151">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d43cd-152">-SkuName</span><span class="sxs-lookup"><span data-stu-id="d43cd-152">-SkuName</span></span>
<span data-ttu-id="d43cd-153">Specifica le dimensioni di tutte le istanze di VMSS.</span><span class="sxs-lookup"><span data-stu-id="d43cd-153">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="d43cd-154">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="d43cd-154">-SkuTier</span></span>
<span data-ttu-id="d43cd-155">Specifica il livello di VMSS.</span><span class="sxs-lookup"><span data-stu-id="d43cd-155">Specifies the tier of VMSS.</span></span>

<span data-ttu-id="d43cd-156">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d43cd-156">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d43cd-157">Standard</span><span class="sxs-lookup"><span data-stu-id="d43cd-157">Standard</span></span>
- <span data-ttu-id="d43cd-158">Base</span><span class="sxs-lookup"><span data-stu-id="d43cd-158">Basic</span></span>

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

### <span data-ttu-id="d43cd-159">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="d43cd-159">-StorageProfile</span></span>
<span data-ttu-id="d43cd-160">Specifica l'oggetto profilo di archiviazione che contiene le proprietà del disco per la configurazione di VMSS.</span><span class="sxs-lookup"><span data-stu-id="d43cd-160">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="d43cd-161">Puoi usare il cmdlet **set-AzureRmVmssStorageProfile** per impostare questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="d43cd-161">You can use the **Set-AzureRmVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="d43cd-162">-Tag</span><span class="sxs-lookup"><span data-stu-id="d43cd-162">-Tag</span></span>
<span data-ttu-id="d43cd-163">Specifica i tag che verranno assegnati a VMSS.</span><span class="sxs-lookup"><span data-stu-id="d43cd-163">Specifies the tags that will be assigned to the VMSS.</span></span>

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

### <span data-ttu-id="d43cd-164">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="d43cd-164">-UpgradePolicyMode</span></span>
<span data-ttu-id="d43cd-165">Specifica la modalità di aggiornamento delle macchine virtuali nel set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="d43cd-165">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>

<span data-ttu-id="d43cd-166">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d43cd-166">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d43cd-167">Automatico</span><span class="sxs-lookup"><span data-stu-id="d43cd-167">Automatic</span></span>
- <span data-ttu-id="d43cd-168">Manuale</span><span class="sxs-lookup"><span data-stu-id="d43cd-168">Manual</span></span>

```yaml
Type: UpgradeMode
Parameter Sets: (All)
Aliases: 
Accepted values: Automatic, Manual

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d43cd-169">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d43cd-169">-Confirm</span></span>
<span data-ttu-id="d43cd-170">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d43cd-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d43cd-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d43cd-171">-WhatIf</span></span>
<span data-ttu-id="d43cd-172">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d43cd-172">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d43cd-173">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d43cd-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d43cd-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d43cd-174">CommonParameters</span></span>
<span data-ttu-id="d43cd-175">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d43cd-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d43cd-176">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d43cd-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d43cd-177">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d43cd-177">INPUTS</span></span>

### <span data-ttu-id="d43cd-178">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d43cd-178">None</span></span>
<span data-ttu-id="d43cd-179">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="d43cd-179">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d43cd-180">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d43cd-180">OUTPUTS</span></span>

### <span data-ttu-id="d43cd-181">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="d43cd-181">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="d43cd-182">Note</span><span class="sxs-lookup"><span data-stu-id="d43cd-182">NOTES</span></span>

## <span data-ttu-id="d43cd-183">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d43cd-183">RELATED LINKS</span></span>

[<span data-ttu-id="d43cd-184">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="d43cd-184">Set-AzureRmVmssOsProfile</span></span>](./Set-AzureRmVmssOsProfile.md)

[<span data-ttu-id="d43cd-185">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="d43cd-185">Set-AzureRmVmssStorageProfile</span></span>](./Set-AzureRmVmssStorageProfile.md)

[<span data-ttu-id="d43cd-186">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="d43cd-186">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="d43cd-187">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="d43cd-187">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="d43cd-188">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d43cd-188">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)


