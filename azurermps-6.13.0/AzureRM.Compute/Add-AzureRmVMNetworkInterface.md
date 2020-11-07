---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BF80D456-DAB1-4B51-B50F-A75C2C66A472
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVMNetworkInterface.md
ms.openlocfilehash: a7e84ee56e09e2008d76ccd9177d320be7ada96a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686631"
---
# <span data-ttu-id="89aaa-101">Add-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="89aaa-101">Add-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="89aaa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="89aaa-102">SYNOPSIS</span></span>
<span data-ttu-id="89aaa-103">Aggiunge un'interfaccia di rete a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="89aaa-103">Adds a network interface to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89aaa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="89aaa-104">SYNTAX</span></span>

### <span data-ttu-id="89aaa-105">GetNicFromNicId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="89aaa-105">GetNicFromNicId (Default)</span></span>
```
Add-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [-Id] <String> [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89aaa-106">GetNicFromNicObject</span><span class="sxs-lookup"><span data-stu-id="89aaa-106">GetNicFromNicObject</span></span>
```
Add-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine>
 [-NetworkInterface] <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89aaa-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="89aaa-107">DESCRIPTION</span></span>
<span data-ttu-id="89aaa-108">Il cmdlet **Add-AzureRmVMNetworkInterface** aggiunge un'interfaccia di rete a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="89aaa-108">The **Add-AzureRmVMNetworkInterface** cmdlet adds a network interface to a virtual machine.</span></span>
<span data-ttu-id="89aaa-109">È possibile aggiungere un'interfaccia quando si crea una macchina virtuale o si aggiunge una a una macchina virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="89aaa-109">You can add an interface when you create a virtual machine or add one to an existing virtual machine.</span></span>

## <span data-ttu-id="89aaa-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="89aaa-110">EXAMPLES</span></span>

### <span data-ttu-id="89aaa-111">Esempio 1: aggiungere un'interfaccia di rete a una nuova macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="89aaa-111">Example 1: Add a network interface to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
```

<span data-ttu-id="89aaa-112">Il primo comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="89aaa-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="89aaa-113">Il comando assegna un nome e una dimensione alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="89aaa-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="89aaa-114">Il secondo comando aggiunge un'interfaccia di rete alla macchina virtuale archiviata in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="89aaa-114">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

### <span data-ttu-id="89aaa-115">Esempio 2: aggiungere un'interfaccia di rete a una macchina virtuale esistente</span><span class="sxs-lookup"><span data-stu-id="89aaa-115">Example 2: Add a network interface to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="89aaa-116">Il primo comando ottiene la macchina virtuale denominata VirtualMachine07 usando il cmdlet **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="89aaa-116">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="89aaa-117">Il comando Archivia la macchina virtuale nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="89aaa-117">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="89aaa-118">Il secondo comando aggiunge un'interfaccia di rete alla macchina virtuale archiviata in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="89aaa-118">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="89aaa-119">Il comando finale aggiorna lo stato della macchina virtuale archiviata in $VirtualMachine in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="89aaa-119">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="89aaa-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="89aaa-120">PARAMETERS</span></span>

### <span data-ttu-id="89aaa-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89aaa-121">-DefaultProfile</span></span>
<span data-ttu-id="89aaa-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="89aaa-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89aaa-123">-ID</span><span class="sxs-lookup"><span data-stu-id="89aaa-123">-Id</span></span>
<span data-ttu-id="89aaa-124">Specifica l'ID di un'interfaccia di rete da aggiungere a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="89aaa-124">Specifies the ID of a network interface to add to a virtual machine.</span></span>
<span data-ttu-id="89aaa-125">Puoi usare il cmdlet [Get-AzureRmNetworkInterface](/powershell/module/azurerm.network/get-azurermnetworkinterface) per ottenere un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="89aaa-125">You can use the [Get-AzureRmNetworkInterface](/powershell/module/azurerm.network/get-azurermnetworkinterface) cmdlet to obtain a network interface.</span></span>

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

### <span data-ttu-id="89aaa-126">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="89aaa-126">-NetworkInterface</span></span>
<span data-ttu-id="89aaa-127">Specifica l'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="89aaa-127">Specifies the network interface.</span></span>

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

### <span data-ttu-id="89aaa-128">-Primaria</span><span class="sxs-lookup"><span data-stu-id="89aaa-128">-Primary</span></span>
<span data-ttu-id="89aaa-129">Indica che questo cmdlet aggiunge l'interfaccia di rete come interfaccia principale.</span><span class="sxs-lookup"><span data-stu-id="89aaa-129">Indicates that this cmdlet adds the network interface as the primary interface.</span></span>

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

### <span data-ttu-id="89aaa-130">-VM</span><span class="sxs-lookup"><span data-stu-id="89aaa-130">-VM</span></span>
<span data-ttu-id="89aaa-131">Specifica un oggetto macchina virtuale locale a cui aggiungere un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="89aaa-131">Specifies a local virtual machine object to which to add a network interface.</span></span>
<span data-ttu-id="89aaa-132">Per creare una macchina virtuale, usare il cmdlet **New-AzureRmVMConfig** .</span><span class="sxs-lookup"><span data-stu-id="89aaa-132">To create a virtual machine, use the **New-AzureRmVMConfig** cmdlet.</span></span>
<span data-ttu-id="89aaa-133">Per ottenere una macchina virtuale esistente, usare il cmdlet **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="89aaa-133">To obtain an existing virtual machine, use the **Get-AzureRmVM** cmdlet.</span></span>

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

### <span data-ttu-id="89aaa-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89aaa-134">CommonParameters</span></span>
<span data-ttu-id="89aaa-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89aaa-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89aaa-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89aaa-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89aaa-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="89aaa-137">INPUTS</span></span>

### <span data-ttu-id="89aaa-138">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="89aaa-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="89aaa-139">System. String</span><span class="sxs-lookup"><span data-stu-id="89aaa-139">System.String</span></span>

### <span data-ttu-id="89aaa-140">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. Internal. Network. Common. INetworkInterfaceReference, Microsoft. Azure. Commands. Common. Network, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="89aaa-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference, Microsoft.Azure.Commands.Common.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="89aaa-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="89aaa-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="89aaa-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="89aaa-142">OUTPUTS</span></span>

### <span data-ttu-id="89aaa-143">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="89aaa-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="89aaa-144">Note</span><span class="sxs-lookup"><span data-stu-id="89aaa-144">NOTES</span></span>

## <span data-ttu-id="89aaa-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="89aaa-145">RELATED LINKS</span></span>

[<span data-ttu-id="89aaa-146">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="89aaa-146">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="89aaa-147">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="89aaa-147">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="89aaa-148">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="89aaa-148">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)
