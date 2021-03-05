---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: 71aa555528ff1cdb5748c1a4ac62481ddd17c17c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991492"
---
# <span data-ttu-id="6e803-101">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="6e803-101">New-AzVMConfig</span></span>

## <span data-ttu-id="6e803-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e803-102">SYNOPSIS</span></span>
<span data-ttu-id="6e803-103">Crea un oggetto macchina virtuale configurabile.</span><span class="sxs-lookup"><span data-stu-id="6e803-103">Creates a configurable virtual machine object.</span></span>

## <span data-ttu-id="6e803-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6e803-104">SYNTAX</span></span>

### <span data-ttu-id="6e803-105">DefaultParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="6e803-105">DefaultParameterSet (Default)</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>]
 [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD] 
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e803-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e803-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>] [-MaxPrice <Double>]
 [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e803-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6e803-107">DESCRIPTION</span></span>
<span data-ttu-id="6e803-108">Il cmdlet **New-AzVMConfig crea** un oggetto macchina virtuale locale configurabile per Azure.</span><span class="sxs-lookup"><span data-stu-id="6e803-108">The **New-AzVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="6e803-109">Altri cmdlet possono essere usati per configurare un oggetto macchina virtuale, ad esempio Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface e Set-AzVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="6e803-109">Other cmdlets can be used to configure a virtual machine object, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

## <span data-ttu-id="6e803-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6e803-110">EXAMPLES</span></span>

### <span data-ttu-id="6e803-111">Esempio 1: Creare un oggetto macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="6e803-111">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="6e803-112">Il primo comando ottiene il set di disponibilità denominato AvailabilitySet03 nel gruppo di risorse denominato ResourceGroup11 e quindi archivia l'oggetto nella $AvailabilitySet locale.</span><span class="sxs-lookup"><span data-stu-id="6e803-112">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="6e803-113">Il secondo comando crea un oggetto macchina virtuale e quindi lo archivia nella $VirtualMachine variabile.</span><span class="sxs-lookup"><span data-stu-id="6e803-113">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="6e803-114">Il comando assegna un nome e le dimensioni alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6e803-114">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="6e803-115">La macchina virtuale appartiene al set di disponibilità archiviato in $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="6e803-115">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="6e803-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6e803-116">PARAMETERS</span></span>

### <span data-ttu-id="6e803-117">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="6e803-117">-AvailabilitySetId</span></span>
<span data-ttu-id="6e803-118">Specifica l'ID di un set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="6e803-118">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="6e803-119">Per ottenere un oggetto set di disponibilità, usare il cmdlet Get-AzAvailabilitySet disponibilità.</span><span class="sxs-lookup"><span data-stu-id="6e803-119">To obtain an availability set object, use the Get-AzAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="6e803-120">L'oggetto set di disponibilità contiene una proprietà ID.</span><span class="sxs-lookup"><span data-stu-id="6e803-120">The availability set object contains an ID property.</span></span> <br>
<span data-ttu-id="6e803-121">Le macchine virtuali specificate nello stesso set di disponibilità sono allocate a nodi diversi per massimizzare la disponibilità.</span><span class="sxs-lookup"><span data-stu-id="6e803-121">Virtual machines specified in the same availability set are allocated to different nodes to maximize availability.</span></span> <br>
<span data-ttu-id="6e803-122">Per altre informazioni sui set di disponibilità, vedere [Gestire la disponibilità delle macchine virtuali.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-manage-availability?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="6e803-122">For more information about availability sets, see [Manage the availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-manage-availability?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json).</span></span> <br>
<span data-ttu-id="6e803-123">Per altre informazioni sulla manutenzione pianificata di Azure, vedere [Manutenzione pianificata per le macchine virtuali in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-planned-maintenance?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="6e803-123">For more information on Azure planned maintenance, see [Planned maintenance for virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-planned-maintenance?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)</span></span> <br>
<span data-ttu-id="6e803-124">Attualmente, una macchina virtuale può essere aggiunta solo al set di disponibilità al momento della creazione.</span><span class="sxs-lookup"><span data-stu-id="6e803-124">Currently, a VM can only be added to availability set at creation time.</span></span> <span data-ttu-id="6e803-125">Il set di disponibilità a cui viene aggiunta la macchina virtuale deve essere nello stesso gruppo di risorse della risorsa del set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="6e803-125">The availability set to which the VM is being added should be under the same resource group as the availability set resource.</span></span> <span data-ttu-id="6e803-126">Non è possibile aggiungere una macchina virtuale esistente a un set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="6e803-126">An existing VM cannot be added to an availability set.</span></span> <br>
<span data-ttu-id="6e803-127">Questa proprietà non può esistere insieme a una proprietà non Null. Riferimento VirtualMachineScaleSet.</span><span class="sxs-lookup"><span data-stu-id="6e803-127">This property cannot exist along with a non-null properties.virtualMachineScaleSet reference.</span></span>

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

### <span data-ttu-id="6e803-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e803-128">-DefaultProfile</span></span>
<span data-ttu-id="6e803-129">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6e803-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e803-130">-EnableUltrasSD</span><span class="sxs-lookup"><span data-stu-id="6e803-130">-EnableUltraSSD</span></span>
<span data-ttu-id="6e803-131">Consente di avere uno o più dischi dati gestiti con un UltraSSD_LRS di account di archiviazione nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6e803-131">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="6e803-132">I dischi gestiti con tipo di account di UltraSSD_LRS possono essere aggiunti a una macchina virtuale solo se questa proprietà è abilitata.</span><span class="sxs-lookup"><span data-stu-id="6e803-132">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>


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

### <span data-ttu-id="6e803-133">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="6e803-133">-EvictionPolicy</span></span>
<span data-ttu-id="6e803-134">Criteri di sgombero per la macchina virtuale Azure Spot.</span><span class="sxs-lookup"><span data-stu-id="6e803-134">The eviction policy for the Azure Spot virtual machine.</span></span>  <span data-ttu-id="6e803-135">I valori supportati sono "Deassegnazione" ed "Elimina".</span><span class="sxs-lookup"><span data-stu-id="6e803-135">Supported values are 'Deallocate' and 'Delete'.</span></span>

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

### <span data-ttu-id="6e803-136">-HostId</span><span class="sxs-lookup"><span data-stu-id="6e803-136">-HostId</span></span>
<span data-ttu-id="6e803-137">ID dell'host</span><span class="sxs-lookup"><span data-stu-id="6e803-137">The Id of Host</span></span>

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

### <span data-ttu-id="6e803-138">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="6e803-138">-IdentityId</span></span>
<span data-ttu-id="6e803-139">Specifica l'elenco delle identità utente associate al set di scalabilità delle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="6e803-139">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="6e803-140">I riferimenti di identità utente ARM id risorsa nel formato '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="6e803-140">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="6e803-141">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="6e803-141">-IdentityType</span></span>
<span data-ttu-id="6e803-142">L'identità della macchina virtuale, se configurata.</span><span class="sxs-lookup"><span data-stu-id="6e803-142">The identity of the virtual machine, if configured.</span></span>

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

### <span data-ttu-id="6e803-143">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="6e803-143">-LicenseType</span></span>
<span data-ttu-id="6e803-144">Specifica un tipo di licenza, che indica che l'immagine o il disco della macchina virtuale è stato concesso in licenza in locale.</span><span class="sxs-lookup"><span data-stu-id="6e803-144">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="6e803-145">I valori possibili per Windows Server sono:</span><span class="sxs-lookup"><span data-stu-id="6e803-145">Possible values for Windows Server are:</span></span>
- <span data-ttu-id="6e803-146">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="6e803-146">Windows_Client</span></span>
- <span data-ttu-id="6e803-147">Windows_Server I valori possibili per il sistema operativo Linux Server sono:</span><span class="sxs-lookup"><span data-stu-id="6e803-147">Windows_Server Possible values for Linux Server operating system are:</span></span> 
- <span data-ttu-id="6e803-148">RHEL_BYOS (per ESTRAI)</span><span class="sxs-lookup"><span data-stu-id="6e803-148">RHEL_BYOS (for RHEL)</span></span> 
- <span data-ttu-id="6e803-149">SLES_BYOS (per SUSE)</span><span class="sxs-lookup"><span data-stu-id="6e803-149">SLES_BYOS (for SUSE)</span></span> 

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

### <span data-ttu-id="6e803-150">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="6e803-150">-MaxPrice</span></span>
<span data-ttu-id="6e803-151">Specifica il prezzo massimo che si è disposti a pagare per una VM/VMSS con priorità bassa.</span><span class="sxs-lookup"><span data-stu-id="6e803-151">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="6e803-152">Questo prezzo è in dollari statunitensi.</span><span class="sxs-lookup"><span data-stu-id="6e803-152">This price is in US Dollars.</span></span> <span data-ttu-id="6e803-153">Questo prezzo verrà confrontato con l'attuale prezzo con priorità bassa per le dimensioni della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6e803-153">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="6e803-154">Inoltre, i prezzi vengono confrontati al momento della creazione/aggiornamento di VM/VMSS con priorità bassa e l'operazione avrà esito positivo solo se il valore maxPrice è maggiore del prezzo attuale con priorità bassa.</span><span class="sxs-lookup"><span data-stu-id="6e803-154">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="6e803-155">Il valore maxPrice verrà usato anche per eliminare una VM/VMSS con priorità bassa se il prezzo attuale con priorità bassa supera il valore maxPrice dopo la creazione di VM/VMSS.</span><span class="sxs-lookup"><span data-stu-id="6e803-155">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="6e803-156">I valori possibili sono: qualsiasi valore decimale maggiore di zero.</span><span class="sxs-lookup"><span data-stu-id="6e803-156">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="6e803-157">Esempio: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="6e803-157">Example: 0.01538.</span></span>  <span data-ttu-id="6e803-158">-1 indica che la VM/VMSS con priorità bassa non deve essere sfrattata per motivi di prezzo.</span><span class="sxs-lookup"><span data-stu-id="6e803-158">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="6e803-159">Inoltre, il prezzo massimo predefinito è -1 se non è fornito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="6e803-159">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="6e803-160">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="6e803-160">-EncryptionAtHost</span></span>
<span data-ttu-id="6e803-161">La proprietà EncryptionAtHost può essere usata dall'utente nella richiesta per abilitare o disabilitare La crittografia host per il set di scalabilità della macchina virtuale o della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6e803-161">EncryptionAtHost property can be used by user in the request to enable or disable the Host Encryption for the virtual machine or virtual machine scale set.</span></span> <span data-ttu-id="6e803-162">In questo modo verrà abilitata la crittografia per tutti i dischi, incluso il disco Risorsa/Temp nell'host stesso.</span><span class="sxs-lookup"><span data-stu-id="6e803-162">This will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="6e803-163">Impostazione predefinita: la crittografia nell'host verrà disabilitata a meno che questa proprietà non sia impostata su true per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="6e803-163">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

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

### <span data-ttu-id="6e803-164">-Priority</span><span class="sxs-lookup"><span data-stu-id="6e803-164">-Priority</span></span>
<span data-ttu-id="6e803-165">Priorità della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6e803-165">The priority for the virtual machine.</span></span>  <span data-ttu-id="6e803-166">Solo i valori supportati sono "Normale", "Posizione" e "Basso".</span><span class="sxs-lookup"><span data-stu-id="6e803-166">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="6e803-167">"Normale" è per la macchina virtuale normale.</span><span class="sxs-lookup"><span data-stu-id="6e803-167">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="6e803-168">"Spot" è per una macchina virtuale spot.</span><span class="sxs-lookup"><span data-stu-id="6e803-168">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="6e803-169">"Low" è anche per la macchina virtuale spot, ma viene sostituito da "Spot".</span><span class="sxs-lookup"><span data-stu-id="6e803-169">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="6e803-170">Usare "Spot" invece di "Low".</span><span class="sxs-lookup"><span data-stu-id="6e803-170">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="6e803-171">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="6e803-171">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="6e803-172">ID risorsa del gruppo di posizionamento di prossimità da usare con la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6e803-172">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

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

### <span data-ttu-id="6e803-173">-Tag</span><span class="sxs-lookup"><span data-stu-id="6e803-173">-Tags</span></span>
<span data-ttu-id="6e803-174">I tag associati alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="6e803-174">The tags attached to the resource.</span></span>

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

### <span data-ttu-id="6e803-175">-VMName</span><span class="sxs-lookup"><span data-stu-id="6e803-175">-VMName</span></span>
<span data-ttu-id="6e803-176">Specifica un nome per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6e803-176">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="6e803-177">-VMSize</span><span class="sxs-lookup"><span data-stu-id="6e803-177">-VMSize</span></span>
<span data-ttu-id="6e803-178">Specifica le dimensioni della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6e803-178">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="6e803-179">-VmssId</span><span class="sxs-lookup"><span data-stu-id="6e803-179">-VmssId</span></span>
<span data-ttu-id="6e803-180">ID del set di scala per le macchine virtuali</span><span class="sxs-lookup"><span data-stu-id="6e803-180">The Id of virtual machine scale set</span></span>

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

### <span data-ttu-id="6e803-181">-Zone</span><span class="sxs-lookup"><span data-stu-id="6e803-181">-Zone</span></span>
<span data-ttu-id="6e803-182">Specifica l'elenco delle aree di disponibilità per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6e803-182">Specifies the availability zone list for the virtual machine.</span></span> <span data-ttu-id="6e803-183">I valori consentiti dipendono dalle funzionalità dell'area geografica.</span><span class="sxs-lookup"><span data-stu-id="6e803-183">The allowed values depend on the capabilities of the region.</span></span> <span data-ttu-id="6e803-184">I valori consentiti saranno in genere 1,2,3.</span><span class="sxs-lookup"><span data-stu-id="6e803-184">Allowed values will normally be 1,2,3.</span></span>

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

### <span data-ttu-id="6e803-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e803-185">CommonParameters</span></span>
<span data-ttu-id="6e803-186">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e803-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e803-187">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6e803-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e803-188">INPUT</span><span class="sxs-lookup"><span data-stu-id="6e803-188">INPUTS</span></span>

### <span data-ttu-id="6e803-189">System.String</span><span class="sxs-lookup"><span data-stu-id="6e803-189">System.String</span></span>

### <span data-ttu-id="6e803-190">System.String[]</span><span class="sxs-lookup"><span data-stu-id="6e803-190">System.String[]</span></span>

### <span data-ttu-id="6e803-191">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="6e803-191">System.Collections.Hashtable</span></span>

### <span data-ttu-id="6e803-192">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6e803-192">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6e803-193">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6e803-193">OUTPUTS</span></span>

### <span data-ttu-id="6e803-194">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6e803-194">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="6e803-195">NOTE</span><span class="sxs-lookup"><span data-stu-id="6e803-195">NOTES</span></span>

## <span data-ttu-id="6e803-196">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6e803-196">RELATED LINKS</span></span>

[<span data-ttu-id="6e803-197">Update-AZVM</span><span class="sxs-lookup"><span data-stu-id="6e803-197">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="6e803-198">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="6e803-198">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="6e803-199">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="6e803-199">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="6e803-200">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="6e803-200">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)


