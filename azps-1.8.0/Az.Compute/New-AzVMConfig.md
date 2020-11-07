---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: 4fd4c3a903910068933a46d3343e8dc990565b8b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684768"
---
# <span data-ttu-id="13f4e-101">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="13f4e-101">New-AzVMConfig</span></span>

## <span data-ttu-id="13f4e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="13f4e-102">SYNOPSIS</span></span>
<span data-ttu-id="13f4e-103">Crea un oggetto macchina virtuale configurabile.</span><span class="sxs-lookup"><span data-stu-id="13f4e-103">Creates a configurable virtual machine object.</span></span>

## <span data-ttu-id="13f4e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="13f4e-104">SYNTAX</span></span>

### <span data-ttu-id="13f4e-105">DefaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="13f4e-105">DefaultParameterSet (Default)</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-Zone <String[]>] [-Tags <Hashtable>] [-EnableUltraSSD] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="13f4e-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="13f4e-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>] [-Tags <Hashtable>]
 [-EnableUltraSSD] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13f4e-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="13f4e-107">AssignIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-AssignIdentity] [-Zone <String[]>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13f4e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="13f4e-108">DESCRIPTION</span></span>
<span data-ttu-id="13f4e-109">Il cmdlet **New-AzVMConfig** crea un oggetto macchina virtuale configurabile locale per Azure.</span><span class="sxs-lookup"><span data-stu-id="13f4e-109">The **New-AzVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="13f4e-110">Altri cmdlet possono essere usati per configurare un oggetto macchina virtuale, ad esempio set-AzVMOperatingSystem, set-AzVMSourceImage, Add-AzVMNetworkInterface e set-AzVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="13f4e-110">Other cmdlets can be used to configure a virtual machine object, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

## <span data-ttu-id="13f4e-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="13f4e-111">EXAMPLES</span></span>

### <span data-ttu-id="13f4e-112">Esempio 1: creare un oggetto macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="13f4e-112">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="13f4e-113">Il primo comando ottiene il set di disponibilità denominato AvailablitySet03 nel gruppo di risorse denominato ResourceGroup11 e quindi archivia tale oggetto nella variabile $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="13f4e-113">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="13f4e-114">Il secondo comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="13f4e-114">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="13f4e-115">Il comando assegna un nome e una dimensione alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="13f4e-115">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="13f4e-116">La macchina virtuale appartiene al set di disponibilità archiviato in $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="13f4e-116">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="13f4e-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="13f4e-117">PARAMETERS</span></span>

### <span data-ttu-id="13f4e-118">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="13f4e-118">-AssignIdentity</span></span>
<span data-ttu-id="13f4e-119">Specificare l'identità di sistema assegnata per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="13f4e-119">Specify the system assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="13f4e-120">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="13f4e-120">-AvailabilitySetId</span></span>
<span data-ttu-id="13f4e-121">Specifica l'ID di un set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="13f4e-121">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="13f4e-122">Per ottenere un oggetto set di disponibilità, usare il cmdlet Get-AzAvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="13f4e-122">To obtain an availability set object, use the Get-AzAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="13f4e-123">L'oggetto set di disponibilità contiene una proprietà ID.</span><span class="sxs-lookup"><span data-stu-id="13f4e-123">The availability set object contains an ID property.</span></span>

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

### <span data-ttu-id="13f4e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13f4e-124">-DefaultProfile</span></span>
<span data-ttu-id="13f4e-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="13f4e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13f4e-126">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="13f4e-126">-EnableUltraSSD</span></span>
<span data-ttu-id="13f4e-127">Consente a una funzionalità di avere uno o più dischi di dati gestiti con il tipo di account di archiviazione UltraSSD_LRS nella VM.</span><span class="sxs-lookup"><span data-stu-id="13f4e-127">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="13f4e-128">Dischi gestiti con tipo di account di archiviazione UltraSSD_LRS possono essere aggiunti a una macchina virtuale solo se questa proprietà è abilitata.</span><span class="sxs-lookup"><span data-stu-id="13f4e-128">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>


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

### <span data-ttu-id="13f4e-129">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="13f4e-129">-IdentityId</span></span>
<span data-ttu-id="13f4e-130">Specifica l'elenco delle identità utente associate al set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="13f4e-130">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="13f4e-131">I riferimenti di identità utente saranno ID delle risorse ARM nella forma:'/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="13f4e-131">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="13f4e-132">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="13f4e-132">-IdentityType</span></span>
<span data-ttu-id="13f4e-133">Identità della macchina virtuale, se configurata.</span><span class="sxs-lookup"><span data-stu-id="13f4e-133">The identity of the virtual machine, if configured.</span></span>

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

### <span data-ttu-id="13f4e-134">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="13f4e-134">-LicenseType</span></span>
<span data-ttu-id="13f4e-135">Il tipo di licenza, che è per portare il proprio scenario di licenza.</span><span class="sxs-lookup"><span data-stu-id="13f4e-135">The license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="13f4e-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="13f4e-136">-Tags</span></span>
<span data-ttu-id="13f4e-137">Tag allegati alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="13f4e-137">The tags attached to the resource.</span></span>

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

### <span data-ttu-id="13f4e-138">-VMName</span><span class="sxs-lookup"><span data-stu-id="13f4e-138">-VMName</span></span>
<span data-ttu-id="13f4e-139">Specifica un nome per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="13f4e-139">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="13f4e-140">-VMSize</span><span class="sxs-lookup"><span data-stu-id="13f4e-140">-VMSize</span></span>
<span data-ttu-id="13f4e-141">Specifica le dimensioni per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="13f4e-141">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="13f4e-142">-Zona</span><span class="sxs-lookup"><span data-stu-id="13f4e-142">-Zone</span></span>
<span data-ttu-id="13f4e-143">Specifica l'elenco delle aree di disponibilità per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="13f4e-143">Specifies the availability zone list for the virtual machine.</span></span> <span data-ttu-id="13f4e-144">I valori consentiti dipendono dalle funzionalità dell'area geografica.</span><span class="sxs-lookup"><span data-stu-id="13f4e-144">The allowed values depend on the capabilities of the region.</span></span> <span data-ttu-id="13f4e-145">I valori consentiti saranno normalmente 1, 2, 3.</span><span class="sxs-lookup"><span data-stu-id="13f4e-145">Allowed values will normally be 1,2,3.</span></span>

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

### <span data-ttu-id="13f4e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13f4e-146">CommonParameters</span></span>
<span data-ttu-id="13f4e-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13f4e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13f4e-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13f4e-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13f4e-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="13f4e-149">INPUTS</span></span>

### <span data-ttu-id="13f4e-150">System. String</span><span class="sxs-lookup"><span data-stu-id="13f4e-150">System.String</span></span>

### <span data-ttu-id="13f4e-151">System. String []</span><span class="sxs-lookup"><span data-stu-id="13f4e-151">System.String[]</span></span>

### <span data-ttu-id="13f4e-152">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="13f4e-152">System.Collections.Hashtable</span></span>

### <span data-ttu-id="13f4e-153">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="13f4e-153">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="13f4e-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="13f4e-154">OUTPUTS</span></span>

### <span data-ttu-id="13f4e-155">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="13f4e-155">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="13f4e-156">Note</span><span class="sxs-lookup"><span data-stu-id="13f4e-156">NOTES</span></span>

## <span data-ttu-id="13f4e-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="13f4e-157">RELATED LINKS</span></span>

[<span data-ttu-id="13f4e-158">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="13f4e-158">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="13f4e-159">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="13f4e-159">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="13f4e-160">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="13f4e-160">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="13f4e-161">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="13f4e-161">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)


