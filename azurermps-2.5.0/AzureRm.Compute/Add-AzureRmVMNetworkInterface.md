---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BF80D456-DAB1-4B51-B50F-A75C2C66A472
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmnetworkinterface
schema: 2.0.0
ms.openlocfilehash: 112403f4cb742c5df39538eb2d8d8fac629d3379
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866772"
---
# <span data-ttu-id="571e5-101">Add-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="571e5-101">Add-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="571e5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="571e5-102">SYNOPSIS</span></span>
<span data-ttu-id="571e5-103">Aggiunge un'interfaccia di rete a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="571e5-103">Adds a network interface to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="571e5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="571e5-104">SYNTAX</span></span>

### <span data-ttu-id="571e5-105">GetNicFromNicId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="571e5-105">GetNicFromNicId (Default)</span></span>
```
Add-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [-Id] <String> [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="571e5-106">GetNicFromNicObject</span><span class="sxs-lookup"><span data-stu-id="571e5-106">GetNicFromNicObject</span></span>
```
Add-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine>
 [-NetworkInterface] <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="571e5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="571e5-107">DESCRIPTION</span></span>
<span data-ttu-id="571e5-108">Il cmdlet **Add-AzureRmVMNetworkInterface** aggiunge un'interfaccia di rete a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="571e5-108">The **Add-AzureRmVMNetworkInterface** cmdlet adds a network interface to a virtual machine.</span></span>
<span data-ttu-id="571e5-109">È possibile aggiungere un'interfaccia quando si crea una macchina virtuale o si aggiunge una a una macchina virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="571e5-109">You can add an interface when you create a virtual machine or add one to an existing virtual machine.</span></span>

## <span data-ttu-id="571e5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="571e5-110">EXAMPLES</span></span>

### <span data-ttu-id="571e5-111">Esempio 1: aggiungere un'interfaccia di rete a una nuova macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="571e5-111">Example 1: Add a network interface to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
```

<span data-ttu-id="571e5-112">Il primo comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="571e5-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="571e5-113">Il comando assegna un nome e una dimensione alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="571e5-113">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="571e5-114">Il secondo comando aggiunge un'interfaccia di rete alla macchina virtuale archiviata in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="571e5-114">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

### <span data-ttu-id="571e5-115">Esempio 2: aggiungere un'interfaccia di rete a una macchina virtuale esistente</span><span class="sxs-lookup"><span data-stu-id="571e5-115">Example 2: Add a network interface to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="571e5-116">Il primo comando ottiene la macchina virtuale denominata VirtualMachine07 usando il cmdlet **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="571e5-116">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="571e5-117">Il comando Archivia la macchina virtuale nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="571e5-117">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="571e5-118">Il secondo comando aggiunge un'interfaccia di rete alla macchina virtuale archiviata in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="571e5-118">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="571e5-119">Il comando finale aggiorna lo stato della macchina virtuale archiviata in $VirtualMachine in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="571e5-119">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="571e5-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="571e5-120">PARAMETERS</span></span>

### <span data-ttu-id="571e5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="571e5-121">-DefaultProfile</span></span>
<span data-ttu-id="571e5-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="571e5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="571e5-123">-ID</span><span class="sxs-lookup"><span data-stu-id="571e5-123">-Id</span></span>
<span data-ttu-id="571e5-124">Specifica l'ID di un'interfaccia di rete da aggiungere a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="571e5-124">Specifies the ID of a network interface to add to a virtual machine.</span></span>
<span data-ttu-id="571e5-125">Puoi usare il cmdlet [Get-AzureRmNetworkInterface](/powershell/module/azurerm.network/get-azurermnetworkinterface) per ottenere un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="571e5-125">You can use the [Get-AzureRmNetworkInterface](/powershell/module/azurerm.network/get-azurermnetworkinterface) cmdlet to obtain a network interface.</span></span>

```yaml
Type: String
Parameter Sets: GetNicFromNicId
Aliases: NicId, NetworkInterfaceId

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="571e5-126">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="571e5-126">-NetworkInterface</span></span>
<span data-ttu-id="571e5-127">Specifica l'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="571e5-127">Specifies the network interface.</span></span>

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

### <span data-ttu-id="571e5-128">-Primaria</span><span class="sxs-lookup"><span data-stu-id="571e5-128">-Primary</span></span>
<span data-ttu-id="571e5-129">Indica che questo cmdlet aggiunge l'interfaccia di rete come interfaccia principale.</span><span class="sxs-lookup"><span data-stu-id="571e5-129">Indicates that this cmdlet adds the network interface as the primary interface.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: GetNicFromNicId
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="571e5-130">-VM</span><span class="sxs-lookup"><span data-stu-id="571e5-130">-VM</span></span>
<span data-ttu-id="571e5-131">Specifica un oggetto macchina virtuale locale a cui aggiungere un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="571e5-131">Specifies a local virtual machine object to which to add a network interface.</span></span>
<span data-ttu-id="571e5-132">Per creare una macchina virtuale, usare il cmdlet **New-AzureRmVMConfig** .</span><span class="sxs-lookup"><span data-stu-id="571e5-132">To create a virtual machine, use the **New-AzureRmVMConfig** cmdlet.</span></span>
<span data-ttu-id="571e5-133">Per ottenere una macchina virtuale esistente, usare il cmdlet **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="571e5-133">To obtain an existing virtual machine, use the **Get-AzureRmVM** cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="571e5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="571e5-134">CommonParameters</span></span>
<span data-ttu-id="571e5-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="571e5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="571e5-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="571e5-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="571e5-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="571e5-137">INPUTS</span></span>

### <span data-ttu-id="571e5-138">System. Collections. Generic. list ' 1 [Microsoft. Azure. Commands. Network. Models. PSNetworkInterface]</span><span class="sxs-lookup"><span data-stu-id="571e5-138">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterface]</span></span>
<span data-ttu-id="571e5-139">Il parametro ' NetworkInterface ' accetta il valore di tipo ' System. Collections. Generic. list ' 1 [Microsoft. Azure. Commands. Network. Models. PSNetworkInterface]' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="571e5-139">Parameter 'NetworkInterface' accepts value of type 'System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterface]' from the pipeline</span></span>

### <span data-ttu-id="571e5-140">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="571e5-140">PSVirtualMachine</span></span>
<span data-ttu-id="571e5-141">Il parametro ' VM ' accetta il valore di tipo ' PSVirtualMachine ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="571e5-141">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="571e5-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="571e5-142">OUTPUTS</span></span>

### <span data-ttu-id="571e5-143">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="571e5-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="571e5-144">Note</span><span class="sxs-lookup"><span data-stu-id="571e5-144">NOTES</span></span>

## <span data-ttu-id="571e5-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="571e5-145">RELATED LINKS</span></span>

[<span data-ttu-id="571e5-146">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="571e5-146">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="571e5-147">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="571e5-147">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="571e5-148">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="571e5-148">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)
