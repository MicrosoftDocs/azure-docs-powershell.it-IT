---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmconfig
schema: 2.0.0
ms.openlocfilehash: 3e42cf7c2be8433d9e1b7e85987e53b9f0050038
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866749"
---
# <span data-ttu-id="6f843-101">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="6f843-101">New-AzureRmVMConfig</span></span>

## <span data-ttu-id="6f843-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6f843-102">SYNOPSIS</span></span>
<span data-ttu-id="6f843-103">Crea un oggetto macchina virtuale configurabile.</span><span class="sxs-lookup"><span data-stu-id="6f843-103">Creates a configurable virtual machine object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f843-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6f843-104">SYNTAX</span></span>

### <span data-ttu-id="6f843-105">DefaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6f843-105">DefaultParameterSet (Default)</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-Zone <String[]>] [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6f843-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f843-106">ExplicitIdentityParameterSet</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f843-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f843-107">AssignIdentityParameterSet</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-AssignIdentity] [-Zone <String[]>] [-Tags <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f843-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6f843-108">DESCRIPTION</span></span>
<span data-ttu-id="6f843-109">Il cmdlet **New-AzureRmVMConfig** crea un oggetto macchina virtuale configurabile locale per Azure.</span><span class="sxs-lookup"><span data-stu-id="6f843-109">The **New-AzureRmVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="6f843-110">Altri cmdlet possono essere usati per configurare un oggetto macchina virtuale, ad esempio set-AzureRmVMOperatingSystem, set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface e set-AzureRmVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="6f843-110">Other cmdlets can be used to configure a virtual machine object, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>

## <span data-ttu-id="6f843-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6f843-111">EXAMPLES</span></span>

### <span data-ttu-id="6f843-112">Esempio 1: creare un oggetto macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="6f843-112">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="6f843-113">Il primo comando ottiene il set di disponibilità denominato AvailablitySet03 nel gruppo di risorse denominato ResourceGroup11 e quindi archivia tale oggetto nella variabile $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="6f843-113">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="6f843-114">Il secondo comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="6f843-114">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="6f843-115">Il comando assegna un nome e una dimensione alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6f843-115">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="6f843-116">La macchina virtuale appartiene al set di disponibilità archiviato in $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="6f843-116">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="6f843-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6f843-117">PARAMETERS</span></span>

### <span data-ttu-id="6f843-118">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="6f843-118">-AssignIdentity</span></span>
<span data-ttu-id="6f843-119">Specificare l'identità di sistema assegnata per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6f843-119">Specify the system assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="6f843-120">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="6f843-120">-AvailabilitySetId</span></span>
<span data-ttu-id="6f843-121">Specifica l'ID di un set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="6f843-121">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="6f843-122">Per ottenere un oggetto set di disponibilità, usare il cmdlet Get-AzureRmAvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="6f843-122">To obtain an availability set object, use the Get-AzureRmAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="6f843-123">L'oggetto set di disponibilità contiene una proprietà ID.</span><span class="sxs-lookup"><span data-stu-id="6f843-123">The availability set object contains an ID property.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f843-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f843-124">-DefaultProfile</span></span>
<span data-ttu-id="6f843-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6f843-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f843-126">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="6f843-126">-IdentityId</span></span>
<span data-ttu-id="6f843-127">Specifica l'elenco delle identità utente associate al set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6f843-127">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="6f843-128">I riferimenti di identità utente saranno ID delle risorse ARM nella forma:'/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="6f843-128">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="6f843-129">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="6f843-129">-IdentityType</span></span>
<span data-ttu-id="6f843-130">Identità della macchina virtuale, se configurata.</span><span class="sxs-lookup"><span data-stu-id="6f843-130">The identity of the virtual machine, if configured.</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f843-131">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="6f843-131">-LicenseType</span></span>
<span data-ttu-id="6f843-132">Il tipo di licenza, che è per portare il proprio scenario di licenza.</span><span class="sxs-lookup"><span data-stu-id="6f843-132">The license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f843-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="6f843-133">-Tags</span></span>
<span data-ttu-id="6f843-134">Tag allegati alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="6f843-134">The tags attached to the resource.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f843-135">-VMName</span><span class="sxs-lookup"><span data-stu-id="6f843-135">-VMName</span></span>
<span data-ttu-id="6f843-136">Specifica un nome per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6f843-136">Specifies a name for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f843-137">-VMSize</span><span class="sxs-lookup"><span data-stu-id="6f843-137">-VMSize</span></span>
<span data-ttu-id="6f843-138">Specifica le dimensioni per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6f843-138">Specifies the size for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f843-139">-Zona</span><span class="sxs-lookup"><span data-stu-id="6f843-139">-Zone</span></span>
<span data-ttu-id="6f843-140">Specifica l'elenco delle aree per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6f843-140">Specifies the zone list for the virtual machine.</span></span>

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

### <span data-ttu-id="6f843-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f843-141">CommonParameters</span></span>
<span data-ttu-id="6f843-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f843-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f843-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f843-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f843-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6f843-144">INPUTS</span></span>

### <span data-ttu-id="6f843-145">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6f843-145">None</span></span>
<span data-ttu-id="6f843-146">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="6f843-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6f843-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6f843-147">OUTPUTS</span></span>

### <span data-ttu-id="6f843-148">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6f843-148">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="6f843-149">Note</span><span class="sxs-lookup"><span data-stu-id="6f843-149">NOTES</span></span>

## <span data-ttu-id="6f843-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6f843-150">RELATED LINKS</span></span>

[<span data-ttu-id="6f843-151">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6f843-151">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="6f843-152">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="6f843-152">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="6f843-153">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="6f843-153">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="6f843-154">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="6f843-154">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)


