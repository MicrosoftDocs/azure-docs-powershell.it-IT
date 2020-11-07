---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmss.md
ms.openlocfilehash: 881908cf85ff4f22fb76b7222a2c09d40a1e9e32
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675373"
---
# <span data-ttu-id="b6073-101">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b6073-101">Get-AzVmss</span></span>

## <span data-ttu-id="b6073-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b6073-102">SYNOPSIS</span></span>
<span data-ttu-id="b6073-103">Ottiene le proprietà di un VMSS.</span><span class="sxs-lookup"><span data-stu-id="b6073-103">Gets the properties of a VMSS.</span></span>

## <span data-ttu-id="b6073-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b6073-104">SYNTAX</span></span>

### <span data-ttu-id="b6073-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b6073-105">DefaultParameter (Default)</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6073-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="b6073-106">FriendMethod</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6073-107">OSUpgradeHistoryMethodParameter</span><span class="sxs-lookup"><span data-stu-id="b6073-107">OSUpgradeHistoryMethodParameter</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-OSUpgradeHistory]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6073-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b6073-108">DESCRIPTION</span></span>
<span data-ttu-id="b6073-109">Il cmdlet **Get-AzVmss** ottiene il modello e la visualizzazione dell'istanza di un set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="b6073-109">The **Get-AzVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="b6073-110">La visualizzazione modello rappresenta le proprietà specificate dall'utente del set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b6073-110">The model view is the user specified properties of the virtual machine scale set.</span></span>
<span data-ttu-id="b6073-111">La visualizzazione istanza è lo stato del livello di istanza del set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b6073-111">The instance view is the instance level status of the virtual machine scale set.</span></span>
<span data-ttu-id="b6073-112">Specifica il parametro *InstanceView* per ottenere solo la visualizzazione istanza di un set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b6073-112">Specify the *InstanceView* parameter to get only the instance view of a virtual machine scale set.</span></span>

## <span data-ttu-id="b6073-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b6073-113">EXAMPLES</span></span>

### <span data-ttu-id="b6073-114">Esempio 1: ottenere le proprietà di un VMSS</span><span class="sxs-lookup"><span data-stu-id="b6073-114">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"

ResourceGroupName                           : Group001
Sku                                         :
  Name                                      : Standard_DS1_v2
  Tier                                      : Standard
  Capacity                                  : 2
UpgradePolicy                               :
  Mode                                      : Manual
VirtualMachineProfile                       :
  OsProfile                                 :
    ComputerNamePrefix                      : test
    AdminUsername                           : contoso
    WindowsConfiguration                    :
      ProvisionVMAgent                      : True
      EnableAutomaticUpdates                : True
  StorageProfile                            :
    ImageReference                          :
      Publisher                             : MicrosoftWindowsServer
      Offer                                 : WindowsServer
      Sku                                   : 2016-Datacenter
      Version                               : latest
    OsDisk                                  :
      Caching                               : None
      CreateOption                          : FromImage
      ManagedDisk                           :
        StorageAccountType                  : Premium_LRS
  NetworkProfile                            :
    NetworkInterfaceConfigurations[0]       :
      Name                                  : Group001
      Primary                               : True
      EnableAcceleratedNetworking           : False
      NetworkSecurityGroup                  :
        Id                                  : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/Group001
/providers/Microsoft.Network/networkSecurityGroups/Group001
      DnsSettings                           :
      IpConfigurations[0]                   :
        Name                                : Group001
        Subnet                              :
          Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/group001
/providers/Microsoft.Network/virtualNetworks/Group001/subnets/Group001
        PrivateIPAddressVersion             : IPv4
        LoadBalancerBackendAddressPools[0]  :
          Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/group001
/providers/Microsoft.Network/loadBalancers/Group001/backendAddressPools/Group001
        LoadBalancerInboundNatPools[0]      :
          Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/group001
/providers/Microsoft.Network/loadBalancers/Group001/inboundNatPools/Group001
        LoadBalancerInboundNatPools[1]      :
          Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/group001
/providers/Microsoft.Network/loadBalancers/Group001/inboundNatPools/Group001
      EnableIPForwarding                    : False
ProvisioningState                           : Succeeded
Overprovision                               : True
UniqueId                                    : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SinglePlacementGroup                        : False
Id                                          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/Group001/
providers/Microsoft.Compute/virtualMachineScaleSets/VMSS001
Name                                        : VMSS001
Type                                        : Microsoft.Compute/virtualMachineScaleSets
Location                                    : eastus
Tags                                        : {}
```

<span data-ttu-id="b6073-115">Questo comando consente di ottenere le proprietà del VMSS denominato VMSS001 che appartiene al gruppo di risorse denominato Group001.</span><span class="sxs-lookup"><span data-stu-id="b6073-115">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="b6073-116">Poiché il comando non specifica il parametro *InstanceView* switch, il cmdlet ottiene la visualizzazione modello del set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b6073-116">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine scale set.</span></span>

### <span data-ttu-id="b6073-117">Esempio 2: ottenere tutte le vmss in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="b6073-117">Example 2: Get all Vmss in a resource group</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "Group001"

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
```

<span data-ttu-id="b6073-118">Ottenere tutte le vmss nel gruppo di risorse "Group001"</span><span class="sxs-lookup"><span data-stu-id="b6073-118">Get all Vmss in resource group "Group001"</span></span>

### <span data-ttu-id="b6073-119">Esempio 3: ottenere tutti i vmss in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="b6073-119">Example 3: Get all Vmss in a subscription</span></span>
```
PS C:\> Get-AzVmss

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
Group002                                       VMSS003      eastus     Standard_A1        1         Succeeded
Group002                                       VMSS004      eastus Standard_DS1_v2        2         Succeeded
```

<span data-ttu-id="b6073-120">Ottenere tutti i vmss in abbonamento.</span><span class="sxs-lookup"><span data-stu-id="b6073-120">Get all Vmss in subscription.</span></span>

### <span data-ttu-id="b6073-121">Esempio 4: ottenere tutti i vmss usando il filtro</span><span class="sxs-lookup"><span data-stu-id="b6073-121">Example 4: Get all Vmss using filtering</span></span>
```
PS C:\> Get-AzVmss -Name VMSS00*

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
Group002                                       VMSS003      eastus     Standard_A1        1         Succeeded
Group002                                       VMSS004      eastus Standard_DS1_v2        2         Succeeded
```

<span data-ttu-id="b6073-122">Ottenere tutti i vmss in abbonamento che iniziano con "VMSS00".</span><span class="sxs-lookup"><span data-stu-id="b6073-122">Get all Vmss in subscription that start with "VMSS00".</span></span>

## <span data-ttu-id="b6073-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b6073-123">PARAMETERS</span></span>

### <span data-ttu-id="b6073-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6073-124">-DefaultProfile</span></span>
<span data-ttu-id="b6073-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b6073-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6073-126">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="b6073-126">-InstanceView</span></span>
<span data-ttu-id="b6073-127">Indica che questo cmdlet ottiene solo la visualizzazione istanza del set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b6073-127">Indicates that this cmdlet gets only the instance view of the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6073-128">-OSUpgradeHistory</span><span class="sxs-lookup"><span data-stu-id="b6073-128">-OSUpgradeHistory</span></span>
<span data-ttu-id="b6073-129">Indica che questo cmdlet elenca la cronologia di aggiornamento del sistema operativo del set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b6073-129">Indicates that this cmdlet lists the os upgrade history of the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OSUpgradeHistoryMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6073-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6073-130">-ResourceGroupName</span></span>
<span data-ttu-id="b6073-131">Specifica il nome del gruppo di risorse di VMSS.</span><span class="sxs-lookup"><span data-stu-id="b6073-131">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="b6073-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="b6073-132">-VMScaleSetName</span></span>
<span data-ttu-id="b6073-133">Specie il nome del VMSS.</span><span class="sxs-lookup"><span data-stu-id="b6073-133">Species the name of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="b6073-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6073-134">CommonParameters</span></span>
<span data-ttu-id="b6073-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6073-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6073-136">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b6073-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6073-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b6073-137">INPUTS</span></span>

### <span data-ttu-id="b6073-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b6073-138">System.String</span></span>

## <span data-ttu-id="b6073-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b6073-139">OUTPUTS</span></span>

### <span data-ttu-id="b6073-140">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b6073-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="b6073-141">Note</span><span class="sxs-lookup"><span data-stu-id="b6073-141">NOTES</span></span>

## <span data-ttu-id="b6073-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b6073-142">RELATED LINKS</span></span>

[<span data-ttu-id="b6073-143">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b6073-143">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="b6073-144">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b6073-144">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="b6073-145">Riavviare-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b6073-145">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="b6073-146">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b6073-146">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="b6073-147">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b6073-147">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="b6073-148">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b6073-148">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="b6073-149">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b6073-149">Update-AzVmss</span></span>](./Update-AzVmss.md)

