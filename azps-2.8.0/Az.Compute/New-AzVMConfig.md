---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: 5dda2e33496e3391d55e7be20348fef681bc22b9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675314"
---
# <span data-ttu-id="7c417-101">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="7c417-101">New-AzVMConfig</span></span>

## <span data-ttu-id="7c417-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7c417-102">SYNOPSIS</span></span>
<span data-ttu-id="7c417-103">Crea un oggetto macchina virtuale configurabile.</span><span class="sxs-lookup"><span data-stu-id="7c417-103">Creates a configurable virtual machine object.</span></span>

## <span data-ttu-id="7c417-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7c417-104">SYNTAX</span></span>

### <span data-ttu-id="7c417-105">DefaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7c417-105">DefaultParameterSet (Default)</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>]
 [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c417-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c417-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>] [-MaxPrice <Double>]
 [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c417-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c417-107">AssignIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-AssignIdentity] [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-VmssId <String>] [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>]
 [-EnableUltraSSD] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c417-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7c417-108">DESCRIPTION</span></span>
<span data-ttu-id="7c417-109">Il cmdlet **New-AzVMConfig** crea un oggetto macchina virtuale configurabile locale per Azure.</span><span class="sxs-lookup"><span data-stu-id="7c417-109">The **New-AzVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="7c417-110">Altri cmdlet possono essere usati per configurare un oggetto macchina virtuale, ad esempio set-AzVMOperatingSystem, set-AzVMSourceImage, Add-AzVMNetworkInterface e set-AzVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="7c417-110">Other cmdlets can be used to configure a virtual machine object, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

## <span data-ttu-id="7c417-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7c417-111">EXAMPLES</span></span>

### <span data-ttu-id="7c417-112">Esempio 1: creare un oggetto macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="7c417-112">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="7c417-113">Il primo comando ottiene il set di disponibilità denominato AvailabilitySet03 nel gruppo di risorse denominato ResourceGroup11 e quindi archivia tale oggetto nella variabile $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="7c417-113">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="7c417-114">Il secondo comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="7c417-114">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="7c417-115">Il comando assegna un nome e una dimensione alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7c417-115">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="7c417-116">La macchina virtuale appartiene al set di disponibilità archiviato in $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="7c417-116">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="7c417-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7c417-117">PARAMETERS</span></span>

### <span data-ttu-id="7c417-118">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="7c417-118">-AssignIdentity</span></span>
<span data-ttu-id="7c417-119">Specificare l'identità di sistema assegnata per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7c417-119">Specify the system assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="7c417-120">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="7c417-120">-AvailabilitySetId</span></span>
<span data-ttu-id="7c417-121">Specifica l'ID di un set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="7c417-121">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="7c417-122">Per ottenere un oggetto set di disponibilità, usare il cmdlet Get-AzAvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="7c417-122">To obtain an availability set object, use the Get-AzAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="7c417-123">L'oggetto set di disponibilità contiene una proprietà ID.</span><span class="sxs-lookup"><span data-stu-id="7c417-123">The availability set object contains an ID property.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c417-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c417-124">-DefaultProfile</span></span>
<span data-ttu-id="7c417-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7c417-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c417-126">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="7c417-126">-EnableUltraSSD</span></span>
<span data-ttu-id="7c417-127">Consente a una funzionalità di avere uno o più dischi di dati gestiti con il tipo di account di archiviazione UltraSSD_LRS nella VM.</span><span class="sxs-lookup"><span data-stu-id="7c417-127">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="7c417-128">Dischi gestiti con tipo di account di archiviazione UltraSSD_LRS possono essere aggiunti a una macchina virtuale solo se questa proprietà è abilitata.</span><span class="sxs-lookup"><span data-stu-id="7c417-128">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>


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

### <span data-ttu-id="7c417-129">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="7c417-129">-EvictionPolicy</span></span>
<span data-ttu-id="7c417-130">Criteri di eliminazione per la macchina virtuale con priorità bassa.</span><span class="sxs-lookup"><span data-stu-id="7c417-130">The eviction policy for the low priority virtual machine.</span></span>  <span data-ttu-id="7c417-131">Solo il valore supportato è "deallocate".</span><span class="sxs-lookup"><span data-stu-id="7c417-131">Only supported value is 'Deallocate'.</span></span>

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

### <span data-ttu-id="7c417-132">-HostId</span><span class="sxs-lookup"><span data-stu-id="7c417-132">-HostId</span></span>
<span data-ttu-id="7c417-133">ID dell'host</span><span class="sxs-lookup"><span data-stu-id="7c417-133">The Id of Host</span></span>

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

### <span data-ttu-id="7c417-134">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="7c417-134">-IdentityId</span></span>
<span data-ttu-id="7c417-135">Specifica l'elenco delle identità utente associate al set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7c417-135">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="7c417-136">I riferimenti di identità utente saranno ID delle risorse ARM nella forma:'/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="7c417-136">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="7c417-137">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="7c417-137">-IdentityType</span></span>
<span data-ttu-id="7c417-138">Identità della macchina virtuale, se configurata.</span><span class="sxs-lookup"><span data-stu-id="7c417-138">The identity of the virtual machine, if configured.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c417-139">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="7c417-139">-LicenseType</span></span>
<span data-ttu-id="7c417-140">Il tipo di licenza, che è per portare il proprio scenario di licenza.</span><span class="sxs-lookup"><span data-stu-id="7c417-140">The license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c417-141">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="7c417-141">-MaxPrice</span></span>
<span data-ttu-id="7c417-142">Specifica il prezzo massimo che si vuole pagare per una VM/VMSS a priorità bassa.</span><span class="sxs-lookup"><span data-stu-id="7c417-142">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="7c417-143">Questo prezzo è in dollari USA.</span><span class="sxs-lookup"><span data-stu-id="7c417-143">This price is in US Dollars.</span></span> <span data-ttu-id="7c417-144">Questo prezzo verrà confrontato con il prezzo corrente con priorità bassa per le dimensioni della VM.</span><span class="sxs-lookup"><span data-stu-id="7c417-144">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="7c417-145">Inoltre, i prezzi vengono confrontati al momento della creazione/aggiornamento della priorità bassa VM/VMSS e l'operazione avrà esito positivo solo se maxPrice è maggiore del prezzo corrente con priorità bassa.</span><span class="sxs-lookup"><span data-stu-id="7c417-145">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="7c417-146">Il maxPrice verrà usato anche per rimuovere una VM/VMSS a priorità bassa se il prezzo corrente con priorità bassa supera il maxPrice dopo la creazione di VM/VMSS.</span><span class="sxs-lookup"><span data-stu-id="7c417-146">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="7c417-147">I valori possibili sono: qualsiasi valore decimale maggiore di zero.</span><span class="sxs-lookup"><span data-stu-id="7c417-147">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="7c417-148">Esempio: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="7c417-148">Example: 0.01538.</span></span>  <span data-ttu-id="7c417-149">-1 indica che la priorità bassa VM/VMSS non deve essere sfrattata per motivi di prezzo.</span><span class="sxs-lookup"><span data-stu-id="7c417-149">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="7c417-150">Inoltre, il prezzo massimo predefinito è-1 se non è fornito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="7c417-150">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="7c417-151">-Priorità</span><span class="sxs-lookup"><span data-stu-id="7c417-151">-Priority</span></span>
<span data-ttu-id="7c417-152">Priorità per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7c417-152">The priority for the virtual machine.</span></span>  <span data-ttu-id="7c417-153">Solo i valori supportati sono "regolari" e "bassi".</span><span class="sxs-lookup"><span data-stu-id="7c417-153">Only supported values are 'Regular' and 'Low'.</span></span>

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

### <span data-ttu-id="7c417-154">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="7c417-154">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="7c417-155">ID di ProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="7c417-155">The Id of ProximityPlacementGroup</span></span>

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

### <span data-ttu-id="7c417-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="7c417-156">-Tags</span></span>
<span data-ttu-id="7c417-157">Tag allegati alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="7c417-157">The tags attached to the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c417-158">-VMName</span><span class="sxs-lookup"><span data-stu-id="7c417-158">-VMName</span></span>
<span data-ttu-id="7c417-159">Specifica un nome per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7c417-159">Specifies a name for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c417-160">-VMSize</span><span class="sxs-lookup"><span data-stu-id="7c417-160">-VMSize</span></span>
<span data-ttu-id="7c417-161">Specifica le dimensioni per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7c417-161">Specifies the size for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c417-162">-VmssId</span><span class="sxs-lookup"><span data-stu-id="7c417-162">-VmssId</span></span>
<span data-ttu-id="7c417-163">ID del set di scale della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="7c417-163">The Id of virtual machine scale set</span></span>

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

### <span data-ttu-id="7c417-164">-Zona</span><span class="sxs-lookup"><span data-stu-id="7c417-164">-Zone</span></span>
<span data-ttu-id="7c417-165">Specifica l'elenco delle aree di disponibilità per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7c417-165">Specifies the availability zone list for the virtual machine.</span></span> <span data-ttu-id="7c417-166">I valori consentiti dipendono dalle funzionalità dell'area geografica.</span><span class="sxs-lookup"><span data-stu-id="7c417-166">The allowed values depend on the capabilities of the region.</span></span> <span data-ttu-id="7c417-167">I valori consentiti saranno normalmente 1, 2, 3.</span><span class="sxs-lookup"><span data-stu-id="7c417-167">Allowed values will normally be 1,2,3.</span></span>

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

### <span data-ttu-id="7c417-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c417-168">CommonParameters</span></span>
<span data-ttu-id="7c417-169">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c417-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c417-170">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7c417-170">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c417-171">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7c417-171">INPUTS</span></span>

### <span data-ttu-id="7c417-172">System. String</span><span class="sxs-lookup"><span data-stu-id="7c417-172">System.String</span></span>

### <span data-ttu-id="7c417-173">System. String []</span><span class="sxs-lookup"><span data-stu-id="7c417-173">System.String[]</span></span>

### <span data-ttu-id="7c417-174">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7c417-174">System.Collections.Hashtable</span></span>

### <span data-ttu-id="7c417-175">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7c417-175">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7c417-176">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7c417-176">OUTPUTS</span></span>

### <span data-ttu-id="7c417-177">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="7c417-177">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="7c417-178">Note</span><span class="sxs-lookup"><span data-stu-id="7c417-178">NOTES</span></span>

## <span data-ttu-id="7c417-179">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7c417-179">RELATED LINKS</span></span>

[<span data-ttu-id="7c417-180">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="7c417-180">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="7c417-181">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="7c417-181">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="7c417-182">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="7c417-182">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="7c417-183">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="7c417-183">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)


