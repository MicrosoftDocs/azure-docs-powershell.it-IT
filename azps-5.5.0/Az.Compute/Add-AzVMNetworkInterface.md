---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BF80D456-DAB1-4B51-B50F-A75C2C66A472
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
ms.openlocfilehash: 3c0a88d53ea1d2c6b77e08ab29a7def3ae9ee445
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199366"
---
# <span data-ttu-id="4355b-101">Add-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="4355b-101">Add-AzVMNetworkInterface</span></span>

## <span data-ttu-id="4355b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4355b-102">SYNOPSIS</span></span>
<span data-ttu-id="4355b-103">Aggiunge un'interfaccia di rete a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="4355b-103">Adds a network interface to a virtual machine.</span></span>

## <span data-ttu-id="4355b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4355b-104">SYNTAX</span></span>

### <span data-ttu-id="4355b-105">GetNicFromNicId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4355b-105">GetNicFromNicId (Default)</span></span>
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine> [-Id] <String> [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4355b-106">GetNicFromNicObject</span><span class="sxs-lookup"><span data-stu-id="4355b-106">GetNicFromNicObject</span></span>
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine>
 [-NetworkInterface] <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4355b-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4355b-107">DESCRIPTION</span></span>
<span data-ttu-id="4355b-108">Il cmdlet **Add-AzVMNetworkInterface aggiunge** un'interfaccia di rete a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="4355b-108">The **Add-AzVMNetworkInterface** cmdlet adds a network interface to a virtual machine.</span></span>
<span data-ttu-id="4355b-109">È possibile aggiungere un'interfaccia quando si crea una macchina virtuale o la si aggiunge a una macchina virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="4355b-109">You can add an interface when you create a virtual machine or add one to an existing virtual machine.</span></span>

## <span data-ttu-id="4355b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4355b-110">EXAMPLES</span></span>

### <span data-ttu-id="4355b-111">Esempio 1: Aggiungere un'interfaccia di rete a una nuova macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="4355b-111">Example 1: Add a network interface to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
```

<span data-ttu-id="4355b-112">Il primo comando crea un oggetto macchina virtuale e quindi lo archivia nella $VirtualMachine variabile.</span><span class="sxs-lookup"><span data-stu-id="4355b-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="4355b-113">Il comando assegna un nome e le dimensioni alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="4355b-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="4355b-114">Il secondo comando aggiunge un'interfaccia di rete alla macchina virtuale archiviata in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="4355b-114">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

### <span data-ttu-id="4355b-115">Esempio 2: Aggiungere un'interfaccia di rete a una macchina virtuale esistente</span><span class="sxs-lookup"><span data-stu-id="4355b-115">Example 2: Add a network interface to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="4355b-116">Il primo comando recupera la macchina virtuale denominata VirtualMachine07 usando il cmdlet **Get-AzVM.**</span><span class="sxs-lookup"><span data-stu-id="4355b-116">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="4355b-117">Il comando archivia la macchina virtuale nella $VirtualMachine variabile.</span><span class="sxs-lookup"><span data-stu-id="4355b-117">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="4355b-118">Il secondo comando aggiunge un'interfaccia di rete alla macchina virtuale archiviata in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="4355b-118">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="4355b-119">Il comando finale aggiorna lo stato della macchina virtuale archiviata in $VirtualMachine in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="4355b-119">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="4355b-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4355b-120">PARAMETERS</span></span>

### <span data-ttu-id="4355b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4355b-121">-DefaultProfile</span></span>
<span data-ttu-id="4355b-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4355b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4355b-123">-Id</span><span class="sxs-lookup"><span data-stu-id="4355b-123">-Id</span></span>
<span data-ttu-id="4355b-124">Specifica l'ID di un'interfaccia di rete da aggiungere a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="4355b-124">Specifies the ID of a network interface to add to a virtual machine.</span></span>
<span data-ttu-id="4355b-125">È possibile usare il cmdlet [Get-AzNetworkInterface](/powershell/module/az.network/get-aznetworkinterface) per ottenere un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="4355b-125">You can use the [Get-AzNetworkInterface](/powershell/module/az.network/get-aznetworkinterface) cmdlet to obtain a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: GetNicFromNicId
Aliases: NicId, NetworkInterfaceId

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4355b-126">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="4355b-126">-NetworkInterface</span></span>
<span data-ttu-id="4355b-127">Specifica l'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="4355b-127">Specifies the network interface.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]
Parameter Sets: GetNicFromNicObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4355b-128">-Principale</span><span class="sxs-lookup"><span data-stu-id="4355b-128">-Primary</span></span>
<span data-ttu-id="4355b-129">Indica che questo cmdlet aggiunge l'interfaccia di rete come interfaccia principale.</span><span class="sxs-lookup"><span data-stu-id="4355b-129">Indicates that this cmdlet adds the network interface as the primary interface.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetNicFromNicId
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4355b-130">-VM</span><span class="sxs-lookup"><span data-stu-id="4355b-130">-VM</span></span>
<span data-ttu-id="4355b-131">Specifica un oggetto macchina virtuale locale a cui aggiungere un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="4355b-131">Specifies a local virtual machine object to which to add a network interface.</span></span>
<span data-ttu-id="4355b-132">Per creare una macchina virtuale, usare il cmdlet **New-AzVMConfig.**</span><span class="sxs-lookup"><span data-stu-id="4355b-132">To create a virtual machine, use the **New-AzVMConfig** cmdlet.</span></span>
<span data-ttu-id="4355b-133">Per ottenere una macchina virtuale esistente, usare il cmdlet **Get-AzVM.**</span><span class="sxs-lookup"><span data-stu-id="4355b-133">To obtain an existing virtual machine, use the **Get-AzVM** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4355b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4355b-134">CommonParameters</span></span>
<span data-ttu-id="4355b-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4355b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4355b-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4355b-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4355b-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="4355b-137">INPUTS</span></span>

### <span data-ttu-id="4355b-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="4355b-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="4355b-139">System.String</span><span class="sxs-lookup"><span data-stu-id="4355b-139">System.String</span></span>

### <span data-ttu-id="4355b-140">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="4355b-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="4355b-141">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4355b-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4355b-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4355b-142">OUTPUTS</span></span>

### <span data-ttu-id="4355b-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="4355b-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="4355b-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="4355b-144">NOTES</span></span>

## <span data-ttu-id="4355b-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4355b-145">RELATED LINKS</span></span>

[<span data-ttu-id="4355b-146">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="4355b-146">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="4355b-147">Get-AZVM</span><span class="sxs-lookup"><span data-stu-id="4355b-147">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="4355b-148">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="4355b-148">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)
