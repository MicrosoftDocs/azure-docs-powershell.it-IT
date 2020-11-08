---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: 8c20a6be76f77a74082090d1386054a23b9b9ea0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190376"
---
# <span data-ttu-id="67835-101">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="67835-101">New-AzVMConfig</span></span>

## <span data-ttu-id="67835-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="67835-102">SYNOPSIS</span></span>
<span data-ttu-id="67835-103">Crea un oggetto macchina virtuale configurabile.</span><span class="sxs-lookup"><span data-stu-id="67835-103">Creates a configurable virtual machine object.</span></span>

## <span data-ttu-id="67835-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="67835-104">SYNTAX</span></span>

### <span data-ttu-id="67835-105">DefaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="67835-105">DefaultParameterSet (Default)</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>]
 [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD] 
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67835-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="67835-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>] [-MaxPrice <Double>]
 [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67835-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="67835-107">DESCRIPTION</span></span>
<span data-ttu-id="67835-108">Il cmdlet **New-AzVMConfig** crea un oggetto macchina virtuale configurabile locale per Azure.</span><span class="sxs-lookup"><span data-stu-id="67835-108">The **New-AzVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="67835-109">Altri cmdlet possono essere usati per configurare un oggetto macchina virtuale, ad esempio set-AzVMOperatingSystem, set-AzVMSourceImage, Add-AzVMNetworkInterface e set-AzVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="67835-109">Other cmdlets can be used to configure a virtual machine object, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

## <span data-ttu-id="67835-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="67835-110">EXAMPLES</span></span>

### <span data-ttu-id="67835-111">Esempio 1: creare un oggetto macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="67835-111">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="67835-112">Il primo comando ottiene il set di disponibilità denominato AvailabilitySet03 nel gruppo di risorse denominato ResourceGroup11 e quindi archivia tale oggetto nella variabile $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="67835-112">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="67835-113">Il secondo comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="67835-113">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="67835-114">Il comando assegna un nome e una dimensione alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="67835-114">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="67835-115">La macchina virtuale appartiene al set di disponibilità archiviato in $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="67835-115">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="67835-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="67835-116">PARAMETERS</span></span>

### <span data-ttu-id="67835-117">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="67835-117">-AvailabilitySetId</span></span>
<span data-ttu-id="67835-118">Specifica l'ID di un set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="67835-118">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="67835-119">Per ottenere un oggetto set di disponibilità, usare il cmdlet Get-AzAvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="67835-119">To obtain an availability set object, use the Get-AzAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="67835-120">L'oggetto set di disponibilità contiene una proprietà ID.</span><span class="sxs-lookup"><span data-stu-id="67835-120">The availability set object contains an ID property.</span></span> <br>
<span data-ttu-id="67835-121">Le macchine virtuali specificate nello stesso set di disponibilità vengono assegnate a nodi diversi per massimizzare la disponibilità.</span><span class="sxs-lookup"><span data-stu-id="67835-121">Virtual machines specified in the same availability set are allocated to different nodes to maximize availability.</span></span> <br>
<span data-ttu-id="67835-122">Per altre informazioni sui set di disponibilità, vedere [gestire la disponibilità di macchine virtuali](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-manage-availability?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="67835-122">For more information about availability sets, see [Manage the availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-manage-availability?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json).</span></span> <br>
<span data-ttu-id="67835-123">Per altre informazioni sulla manutenzione pianificata di Azure, vedere [manutenzione pianificata per le macchine virtuali in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-planned-maintenance?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="67835-123">For more information on Azure planned maintenance, see [Planned maintenance for virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-planned-maintenance?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)</span></span> <br>
<span data-ttu-id="67835-124">Attualmente, una VM può essere aggiunta solo alla disponibilità impostata in fase di creazione.</span><span class="sxs-lookup"><span data-stu-id="67835-124">Currently, a VM can only be added to availability set at creation time.</span></span> <span data-ttu-id="67835-125">Il set di disponibilità a cui è stata aggiunta la VM deve essere sotto lo stesso gruppo di risorse della risorsa set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="67835-125">The availability set to which the VM is being added should be under the same resource group as the availability set resource.</span></span> <span data-ttu-id="67835-126">Non è possibile aggiungere una VM esistente a un set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="67835-126">An existing VM cannot be added to an availability set.</span></span> <br>
<span data-ttu-id="67835-127">Questa proprietà non può esistere insieme a un riferimento a proprietà non null. virtualMachineScaleSet.</span><span class="sxs-lookup"><span data-stu-id="67835-127">This property cannot exist along with a non-null properties.virtualMachineScaleSet reference.</span></span>

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

### <span data-ttu-id="67835-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67835-128">-DefaultProfile</span></span>
<span data-ttu-id="67835-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="67835-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67835-130">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="67835-130">-EnableUltraSSD</span></span>
<span data-ttu-id="67835-131">Consente a una funzionalità di avere uno o più dischi di dati gestiti con il tipo di account di archiviazione UltraSSD_LRS nella VM.</span><span class="sxs-lookup"><span data-stu-id="67835-131">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="67835-132">Dischi gestiti con tipo di account di archiviazione UltraSSD_LRS possono essere aggiunti a una macchina virtuale solo se questa proprietà è abilitata.</span><span class="sxs-lookup"><span data-stu-id="67835-132">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>


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

### <span data-ttu-id="67835-133">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="67835-133">-EvictionPolicy</span></span>
<span data-ttu-id="67835-134">Criteri di eliminazione per la macchina virtuale di Azure spot.</span><span class="sxs-lookup"><span data-stu-id="67835-134">The eviction policy for the Azure Spot virtual machine.</span></span>  <span data-ttu-id="67835-135">I valori supportati sono "deallocate" e "Delete".</span><span class="sxs-lookup"><span data-stu-id="67835-135">Supported values are 'Deallocate' and 'Delete'.</span></span>

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

### <span data-ttu-id="67835-136">-HostId</span><span class="sxs-lookup"><span data-stu-id="67835-136">-HostId</span></span>
<span data-ttu-id="67835-137">ID dell'host</span><span class="sxs-lookup"><span data-stu-id="67835-137">The Id of Host</span></span>

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

### <span data-ttu-id="67835-138">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="67835-138">-IdentityId</span></span>
<span data-ttu-id="67835-139">Specifica l'elenco delle identità utente associate al set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="67835-139">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="67835-140">I riferimenti di identità utente saranno ID delle risorse ARM nella forma:'/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="67835-140">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="67835-141">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="67835-141">-IdentityType</span></span>
<span data-ttu-id="67835-142">Identità della macchina virtuale, se configurata.</span><span class="sxs-lookup"><span data-stu-id="67835-142">The identity of the virtual machine, if configured.</span></span>

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

### <span data-ttu-id="67835-143">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="67835-143">-LicenseType</span></span>
<span data-ttu-id="67835-144">Il tipo di licenza, che è per portare il proprio scenario di licenza.</span><span class="sxs-lookup"><span data-stu-id="67835-144">The license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="67835-145">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="67835-145">-MaxPrice</span></span>
<span data-ttu-id="67835-146">Specifica il prezzo massimo che si vuole pagare per una VM/VMSS a priorità bassa.</span><span class="sxs-lookup"><span data-stu-id="67835-146">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="67835-147">Questo prezzo è in dollari USA.</span><span class="sxs-lookup"><span data-stu-id="67835-147">This price is in US Dollars.</span></span> <span data-ttu-id="67835-148">Questo prezzo verrà confrontato con il prezzo corrente con priorità bassa per le dimensioni della VM.</span><span class="sxs-lookup"><span data-stu-id="67835-148">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="67835-149">Inoltre, i prezzi vengono confrontati al momento della creazione/aggiornamento della priorità bassa VM/VMSS e l'operazione avrà esito positivo solo se maxPrice è maggiore del prezzo corrente con priorità bassa.</span><span class="sxs-lookup"><span data-stu-id="67835-149">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="67835-150">Il maxPrice verrà usato anche per rimuovere una VM/VMSS a priorità bassa se il prezzo corrente con priorità bassa supera il maxPrice dopo la creazione di VM/VMSS.</span><span class="sxs-lookup"><span data-stu-id="67835-150">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="67835-151">I valori possibili sono: qualsiasi valore decimale maggiore di zero.</span><span class="sxs-lookup"><span data-stu-id="67835-151">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="67835-152">Esempio: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="67835-152">Example: 0.01538.</span></span>  <span data-ttu-id="67835-153">-1 indica che la priorità bassa VM/VMSS non deve essere sfrattata per motivi di prezzo.</span><span class="sxs-lookup"><span data-stu-id="67835-153">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="67835-154">Inoltre, il prezzo massimo predefinito è-1 se non è fornito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="67835-154">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="67835-155">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="67835-155">-EncryptionAtHost</span></span>
<span data-ttu-id="67835-156">La proprietà EncryptionAtHost può essere usata dall'utente nella richiesta per abilitare o disabilitare la crittografia host per la macchina virtuale o il set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="67835-156">EncryptionAtHost property can be used by user in the request to enable or disable the Host Encryption for the virtual machine or virtual machine scale set.</span></span> <span data-ttu-id="67835-157">Ciò consentirà la crittografia per tutti i dischi, incluso il disco Resource/Temp all'host stesso.</span><span class="sxs-lookup"><span data-stu-id="67835-157">This will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="67835-158">Impostazione predefinita: la crittografia all'host verrà disabilitata a meno che questa proprietà non sia impostata su true per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="67835-158">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

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

### <span data-ttu-id="67835-159">-Priorità</span><span class="sxs-lookup"><span data-stu-id="67835-159">-Priority</span></span>
<span data-ttu-id="67835-160">Priorità per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="67835-160">The priority for the virtual machine.</span></span>  <span data-ttu-id="67835-161">Solo i valori supportati sono "regolari", "spot" e "low".</span><span class="sxs-lookup"><span data-stu-id="67835-161">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="67835-162">"Normale" è per la normale macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="67835-162">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="67835-163">"Spot" è per la macchina virtuale spot.</span><span class="sxs-lookup"><span data-stu-id="67835-163">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="67835-164">"Basso" è anche per la macchina virtuale spot, ma è sostituito da "spot".</span><span class="sxs-lookup"><span data-stu-id="67835-164">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="67835-165">Usare "spot" invece di "low".</span><span class="sxs-lookup"><span data-stu-id="67835-165">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="67835-166">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="67835-166">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="67835-167">ID risorsa del gruppo di posizionamento di prossimità da usare con questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="67835-167">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

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

### <span data-ttu-id="67835-168">-Tag</span><span class="sxs-lookup"><span data-stu-id="67835-168">-Tags</span></span>
<span data-ttu-id="67835-169">Tag allegati alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="67835-169">The tags attached to the resource.</span></span>

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

### <span data-ttu-id="67835-170">-VMName</span><span class="sxs-lookup"><span data-stu-id="67835-170">-VMName</span></span>
<span data-ttu-id="67835-171">Specifica un nome per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="67835-171">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="67835-172">-VMSize</span><span class="sxs-lookup"><span data-stu-id="67835-172">-VMSize</span></span>
<span data-ttu-id="67835-173">Specifica le dimensioni per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="67835-173">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="67835-174">-VmssId</span><span class="sxs-lookup"><span data-stu-id="67835-174">-VmssId</span></span>
<span data-ttu-id="67835-175">ID del set di scale della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="67835-175">The Id of virtual machine scale set</span></span>

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

### <span data-ttu-id="67835-176">-Zona</span><span class="sxs-lookup"><span data-stu-id="67835-176">-Zone</span></span>
<span data-ttu-id="67835-177">Specifica l'elenco delle aree di disponibilità per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="67835-177">Specifies the availability zone list for the virtual machine.</span></span> <span data-ttu-id="67835-178">I valori consentiti dipendono dalle funzionalità dell'area geografica.</span><span class="sxs-lookup"><span data-stu-id="67835-178">The allowed values depend on the capabilities of the region.</span></span> <span data-ttu-id="67835-179">I valori consentiti saranno normalmente 1, 2, 3.</span><span class="sxs-lookup"><span data-stu-id="67835-179">Allowed values will normally be 1,2,3.</span></span>

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

### <span data-ttu-id="67835-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67835-180">CommonParameters</span></span>
<span data-ttu-id="67835-181">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67835-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67835-182">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="67835-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67835-183">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="67835-183">INPUTS</span></span>

### <span data-ttu-id="67835-184">System. String</span><span class="sxs-lookup"><span data-stu-id="67835-184">System.String</span></span>

### <span data-ttu-id="67835-185">System. String []</span><span class="sxs-lookup"><span data-stu-id="67835-185">System.String[]</span></span>

### <span data-ttu-id="67835-186">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="67835-186">System.Collections.Hashtable</span></span>

### <span data-ttu-id="67835-187">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="67835-187">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="67835-188">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="67835-188">OUTPUTS</span></span>

### <span data-ttu-id="67835-189">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="67835-189">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="67835-190">Note</span><span class="sxs-lookup"><span data-stu-id="67835-190">NOTES</span></span>

## <span data-ttu-id="67835-191">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="67835-191">RELATED LINKS</span></span>

[<span data-ttu-id="67835-192">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="67835-192">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="67835-193">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="67835-193">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="67835-194">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="67835-194">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="67835-195">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="67835-195">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)


