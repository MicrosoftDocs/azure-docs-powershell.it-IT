---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMConfig.md
ms.openlocfilehash: 6809088110944648781fc2264bd2c56f98cbee1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518839"
---
# <span data-ttu-id="ffcb1-101">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="ffcb1-101">New-AzureRmVMConfig</span></span>

## <span data-ttu-id="ffcb1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ffcb1-102">SYNOPSIS</span></span>
<span data-ttu-id="ffcb1-103">Crea un oggetto macchina virtuale configurabile.</span><span class="sxs-lookup"><span data-stu-id="ffcb1-103">Creates a configurable virtual machine object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ffcb1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ffcb1-104">SYNTAX</span></span>

### <span data-ttu-id="ffcb1-105">DefaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ffcb1-105">DefaultParameterSet (Default)</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-Zone <String[]>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ffcb1-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="ffcb1-106">ExplicitIdentityParameterSet</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-Tags <Hashtable>] [-EnableUltraSSD] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ffcb1-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="ffcb1-107">AssignIdentityParameterSet</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-AssignIdentity] [-Zone <String[]>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ffcb1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ffcb1-108">DESCRIPTION</span></span>
<span data-ttu-id="ffcb1-109">Il cmdlet **New-AzureRmVMConfig** crea un oggetto macchina virtuale configurabile locale per Azure.</span><span class="sxs-lookup"><span data-stu-id="ffcb1-109">The **New-AzureRmVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="ffcb1-110">Altri cmdlet possono essere usati per configurare un oggetto macchina virtuale, ad esempio set-AzureRmVMOperatingSystem, set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface e set-AzureRmVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="ffcb1-110">Other cmdlets can be used to configure a virtual machine object, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>

## <span data-ttu-id="ffcb1-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ffcb1-111">EXAMPLES</span></span>

### <span data-ttu-id="ffcb1-112">Esempio 1: creare un oggetto macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="ffcb1-112">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="ffcb1-113">Il primo comando ottiene il set di disponibilità denominato AvailablitySet03 nel gruppo di risorse denominato ResourceGroup11 e quindi archivia tale oggetto nella variabile $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="ffcb1-113">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="ffcb1-114">Il secondo comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="ffcb1-114">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="ffcb1-115">Il comando assegna un nome e una dimensione alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ffcb1-115">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="ffcb1-116">La macchina virtuale appartiene al set di disponibilità archiviato in $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="ffcb1-116">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="ffcb1-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ffcb1-117">PARAMETERS</span></span>

### <span data-ttu-id="ffcb1-118">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="ffcb1-118">-AssignIdentity</span></span>
<span data-ttu-id="ffcb1-119">Specificare l'identità di sistema assegnata per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ffcb1-119">Specify the system assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="ffcb1-120">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="ffcb1-120">-AvailabilitySetId</span></span>
<span data-ttu-id="ffcb1-121">Specifica l'ID di un set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="ffcb1-121">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="ffcb1-122">Per ottenere un oggetto set di disponibilità, usare il cmdlet Get-AzureRmAvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="ffcb1-122">To obtain an availability set object, use the Get-AzureRmAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="ffcb1-123">L'oggetto set di disponibilità contiene una proprietà ID.</span><span class="sxs-lookup"><span data-stu-id="ffcb1-123">The availability set object contains an ID property.</span></span>

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

### <span data-ttu-id="ffcb1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffcb1-124">-DefaultProfile</span></span>
<span data-ttu-id="ffcb1-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ffcb1-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ffcb1-126">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="ffcb1-126">-EnableUltraSSD</span></span>
<span data-ttu-id="ffcb1-127">Consente a una funzionalità di avere uno o più dischi di dati gestiti con il tipo di account di archiviazione UltraSSD_LRS nella VM.</span><span class="sxs-lookup"><span data-stu-id="ffcb1-127">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="ffcb1-128">Dischi gestiti con tipo di account di archiviazione UltraSSD_LRS possono essere aggiunti a una macchina virtuale solo se questa proprietà è abilitata.</span><span class="sxs-lookup"><span data-stu-id="ffcb1-128">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>


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

### <span data-ttu-id="ffcb1-129">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="ffcb1-129">-IdentityId</span></span>
<span data-ttu-id="ffcb1-130">Specifica l'elenco delle identità utente associate al set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ffcb1-130">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="ffcb1-131">I riferimenti di identità utente saranno ID delle risorse ARM nella forma:'/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="ffcb1-131">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="ffcb1-132">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="ffcb1-132">-IdentityType</span></span>
<span data-ttu-id="ffcb1-133">Identità della macchina virtuale, se configurata.</span><span class="sxs-lookup"><span data-stu-id="ffcb1-133">The identity of the virtual machine, if configured.</span></span>

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

### <span data-ttu-id="ffcb1-134">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="ffcb1-134">-LicenseType</span></span>
<span data-ttu-id="ffcb1-135">Il tipo di licenza, che è per portare il proprio scenario di licenza.</span><span class="sxs-lookup"><span data-stu-id="ffcb1-135">The license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="ffcb1-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="ffcb1-136">-Tags</span></span>
<span data-ttu-id="ffcb1-137">Tag allegati alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="ffcb1-137">The tags attached to the resource.</span></span>

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

### <span data-ttu-id="ffcb1-138">-VMName</span><span class="sxs-lookup"><span data-stu-id="ffcb1-138">-VMName</span></span>
<span data-ttu-id="ffcb1-139">Specifica un nome per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ffcb1-139">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="ffcb1-140">-VMSize</span><span class="sxs-lookup"><span data-stu-id="ffcb1-140">-VMSize</span></span>
<span data-ttu-id="ffcb1-141">Specifica le dimensioni per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ffcb1-141">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="ffcb1-142">-Zona</span><span class="sxs-lookup"><span data-stu-id="ffcb1-142">-Zone</span></span>
<span data-ttu-id="ffcb1-143">Specifica l'elenco delle aree per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ffcb1-143">Specifies the zone list for the virtual machine.</span></span>

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

### <span data-ttu-id="ffcb1-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffcb1-144">CommonParameters</span></span>
<span data-ttu-id="ffcb1-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffcb1-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffcb1-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffcb1-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffcb1-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ffcb1-147">INPUTS</span></span>

### <span data-ttu-id="ffcb1-148">System. String</span><span class="sxs-lookup"><span data-stu-id="ffcb1-148">System.String</span></span>

### <span data-ttu-id="ffcb1-149">System. String []</span><span class="sxs-lookup"><span data-stu-id="ffcb1-149">System.String[]</span></span>

### <span data-ttu-id="ffcb1-150">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ffcb1-150">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ffcb1-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ffcb1-151">OUTPUTS</span></span>

### <span data-ttu-id="ffcb1-152">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ffcb1-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="ffcb1-153">Note</span><span class="sxs-lookup"><span data-stu-id="ffcb1-153">NOTES</span></span>

## <span data-ttu-id="ffcb1-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ffcb1-154">RELATED LINKS</span></span>

[<span data-ttu-id="ffcb1-155">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ffcb1-155">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="ffcb1-156">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="ffcb1-156">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="ffcb1-157">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="ffcb1-157">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="ffcb1-158">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ffcb1-158">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)


