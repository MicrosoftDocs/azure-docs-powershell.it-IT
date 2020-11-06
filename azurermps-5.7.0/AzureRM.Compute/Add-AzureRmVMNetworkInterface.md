---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: BF80D456-DAB1-4B51-B50F-A75C2C66A472
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMNetworkInterface.md
ms.openlocfilehash: 11d2f8226e2cabba5fb431054a0e6c822e33af6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514527"
---
# <span data-ttu-id="7b316-101">Add-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7b316-101">Add-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="7b316-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7b316-102">SYNOPSIS</span></span>
<span data-ttu-id="7b316-103">Aggiunge un'interfaccia di rete a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7b316-103">Adds a network interface to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b316-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7b316-104">SYNTAX</span></span>

### <span data-ttu-id="7b316-105">GetNicFromNicId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7b316-105">GetNicFromNicId (Default)</span></span>
```
Add-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [-Id] <String> [-Primary] [<CommonParameters>]
```

### <span data-ttu-id="7b316-106">GetNicFromNicObject</span><span class="sxs-lookup"><span data-stu-id="7b316-106">GetNicFromNicObject</span></span>
```
Add-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine>
 [-NetworkInterface] <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterface]>
 [<CommonParameters>]
```

## <span data-ttu-id="7b316-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7b316-107">DESCRIPTION</span></span>
<span data-ttu-id="7b316-108">Il cmdlet **Add-AzureRmVMNetworkInterface** aggiunge un'interfaccia di rete a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7b316-108">The **Add-AzureRmVMNetworkInterface** cmdlet adds a network interface to a virtual machine.</span></span>
<span data-ttu-id="7b316-109">È possibile aggiungere un'interfaccia quando si crea una macchina virtuale o si aggiunge una a una macchina virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="7b316-109">You can add an interface when you create a virtual machine or add one to an existing virtual machine.</span></span>

## <span data-ttu-id="7b316-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7b316-110">EXAMPLES</span></span>

### <span data-ttu-id="7b316-111">Esempio 1: aggiungere un'interfaccia di rete a una nuova macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="7b316-111">Example 1: Add a network interface to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" 
PS C:\> Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
```

<span data-ttu-id="7b316-112">Il primo comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="7b316-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="7b316-113">Il comando assegna un nome e una dimensione alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7b316-113">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="7b316-114">Il secondo comando aggiunge un'interfaccia di rete alla macchina virtuale archiviata in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="7b316-114">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

### <span data-ttu-id="7b316-115">Esempio 2: aggiungere un'interfaccia di rete a una macchina virtuale esistente</span><span class="sxs-lookup"><span data-stu-id="7b316-115">Example 2: Add a network interface to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="7b316-116">Il primo comando ottiene la macchina virtuale denominata VirtualMachine07 usando il cmdlet **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="7b316-116">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="7b316-117">Il comando Archivia la macchina virtuale nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="7b316-117">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="7b316-118">Il secondo comando aggiunge un'interfaccia di rete alla macchina virtuale archiviata in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="7b316-118">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="7b316-119">Il comando finale aggiorna lo stato della macchina virtuale archiviata in $VirtualMachine in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="7b316-119">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="7b316-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7b316-120">PARAMETERS</span></span>

### <span data-ttu-id="7b316-121">-ID</span><span class="sxs-lookup"><span data-stu-id="7b316-121">-Id</span></span>
<span data-ttu-id="7b316-122">Specifica l'ID di un'interfaccia di rete da aggiungere a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7b316-122">Specifies the ID of a network interface to add to a virtual machine.</span></span>
<span data-ttu-id="7b316-123">Puoi usare il cmdlet [Get-AzureRmNetworkInterface](/powershell/module/azurerm.network/get-azurermnetworkinterface) per ottenere un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="7b316-123">You can use the [Get-AzureRmNetworkInterface](/powershell/module/azurerm.network/get-azurermnetworkinterface) cmdlet to obtain a network interface.</span></span>

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

### <span data-ttu-id="7b316-124">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7b316-124">-NetworkInterface</span></span>
<span data-ttu-id="7b316-125">Specifica l'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="7b316-125">Specifies the network interface.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterface]
Parameter Sets: GetNicFromNicObject
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b316-126">-Primaria</span><span class="sxs-lookup"><span data-stu-id="7b316-126">-Primary</span></span>
<span data-ttu-id="7b316-127">Indica che questo cmdlet aggiunge l'interfaccia di rete come interfaccia principale.</span><span class="sxs-lookup"><span data-stu-id="7b316-127">Indicates that this cmdlet adds the network interface as the primary interface.</span></span>

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

### <span data-ttu-id="7b316-128">-VM</span><span class="sxs-lookup"><span data-stu-id="7b316-128">-VM</span></span>
<span data-ttu-id="7b316-129">Specifica un oggetto macchina virtuale locale a cui aggiungere un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="7b316-129">Specifies a local virtual machine object to which to add a network interface.</span></span>
<span data-ttu-id="7b316-130">Per creare una macchina virtuale, usare il cmdlet **New-AzureRmVMConfig** .</span><span class="sxs-lookup"><span data-stu-id="7b316-130">To create a virtual machine, use the **New-AzureRmVMConfig** cmdlet.</span></span>
<span data-ttu-id="7b316-131">Per ottenere una macchina virtuale esistente, usare il cmdlet **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="7b316-131">To obtain an existing virtual machine, use the **Get-AzureRmVM** cmdlet.</span></span>

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

### <span data-ttu-id="7b316-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b316-132">CommonParameters</span></span>
<span data-ttu-id="7b316-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b316-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b316-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b316-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b316-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7b316-135">INPUTS</span></span>

### <span data-ttu-id="7b316-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7b316-136">None</span></span>
<span data-ttu-id="7b316-137">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="7b316-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7b316-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7b316-138">OUTPUTS</span></span>

## <span data-ttu-id="7b316-139">Note</span><span class="sxs-lookup"><span data-stu-id="7b316-139">NOTES</span></span>

## <span data-ttu-id="7b316-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7b316-140">RELATED LINKS</span></span>

[<span data-ttu-id="7b316-141">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="7b316-141">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="7b316-142">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7b316-142">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="7b316-143">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="7b316-143">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)
