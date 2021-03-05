---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmss.md
ms.openlocfilehash: 4290c178ad1f84400f542c16a2f90c51c654985c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013709"
---
# <span data-ttu-id="34913-101">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="34913-101">Get-AzVmss</span></span>

## <span data-ttu-id="34913-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34913-102">SYNOPSIS</span></span>
<span data-ttu-id="34913-103">Ottiene le proprietà di un sistema VMSS.</span><span class="sxs-lookup"><span data-stu-id="34913-103">Gets the properties of a VMSS.</span></span>

## <span data-ttu-id="34913-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="34913-104">SYNTAX</span></span>

### <span data-ttu-id="34913-105">DefaultParameter (Default)</span><span class="sxs-lookup"><span data-stu-id="34913-105">DefaultParameter (Default)</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34913-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="34913-106">FriendMethod</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34913-107">OSUpgradeHistoryMethodParameter</span><span class="sxs-lookup"><span data-stu-id="34913-107">OSUpgradeHistoryMethodParameter</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-OSUpgradeHistory]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34913-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="34913-108">DESCRIPTION</span></span>
<span data-ttu-id="34913-109">Il cmdlet **Get-AzVmss ottiene** la visualizzazione modello e istanza di un set di scalabilità macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="34913-109">The **Get-AzVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="34913-110">La visualizzazione modello è le proprietà specificate dall'utente del set di scalabilità della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="34913-110">The model view is the user specified properties of the virtual machine scale set.</span></span>
<span data-ttu-id="34913-111">La visualizzazione dell'istanza è lo stato del livello di istanza del set di scalabilità della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="34913-111">The instance view is the instance level status of the virtual machine scale set.</span></span>
<span data-ttu-id="34913-112">Specificare il *parametro InstanceView* per ottenere solo la visualizzazione dell'istanza di un set di scalabilità delle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="34913-112">Specify the *InstanceView* parameter to get only the instance view of a virtual machine scale set.</span></span>

## <span data-ttu-id="34913-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="34913-113">EXAMPLES</span></span>

### <span data-ttu-id="34913-114">Esempio 1: Ottenere le proprietà di un sistema VMSS</span><span class="sxs-lookup"><span data-stu-id="34913-114">Example 1: Get the properties of a VMSS</span></span>
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

<span data-ttu-id="34913-115">Questo comando ottiene le proprietà del sistema VMSS denominato VMSS001 che appartiene al gruppo di risorse denominato Group001.</span><span class="sxs-lookup"><span data-stu-id="34913-115">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="34913-116">Poiché il comando non specifica il parametro del parametro *InstanceView,* il cmdlet ottiene la visualizzazione del modello del set di scalabilità della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="34913-116">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine scale set.</span></span>

### <span data-ttu-id="34913-117">Esempio 2: Ottenere tutte le vm in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="34913-117">Example 2: Get all Vmss in a resource group</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "Group001"

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
```

<span data-ttu-id="34913-118">Ottenere tutte le vm nel gruppo di risorse "Group001"</span><span class="sxs-lookup"><span data-stu-id="34913-118">Get all Vmss in resource group "Group001"</span></span>

### <span data-ttu-id="34913-119">Esempio 3: Ottenere tutte le vm in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="34913-119">Example 3: Get all Vmss in a subscription</span></span>
```
PS C:\> Get-AzVmss

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
Group002                                       VMSS003      eastus     Standard_A1        1         Succeeded
Group002                                       VMSS004      eastus Standard_DS1_v2        2         Succeeded
```

<span data-ttu-id="34913-120">Scarica tutte le Vms in abbonamento.</span><span class="sxs-lookup"><span data-stu-id="34913-120">Get all Vmss in subscription.</span></span>

### <span data-ttu-id="34913-121">Esempio 4: Ottenere tutte le vms con i filtri</span><span class="sxs-lookup"><span data-stu-id="34913-121">Example 4: Get all Vmss using filtering</span></span>
```
PS C:\> Get-AzVmss -Name VMSS00*

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
Group002                                       VMSS003      eastus     Standard_A1        1         Succeeded
Group002                                       VMSS004      eastus Standard_DS1_v2        2         Succeeded
```

<span data-ttu-id="34913-122">Ottieni tutte le vm in abbonamento che iniziano con "VMSS00".</span><span class="sxs-lookup"><span data-stu-id="34913-122">Get all Vmss in subscription that start with "VMSS00".</span></span>

## <span data-ttu-id="34913-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34913-123">PARAMETERS</span></span>

### <span data-ttu-id="34913-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34913-124">-DefaultProfile</span></span>
<span data-ttu-id="34913-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="34913-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34913-126">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="34913-126">-InstanceView</span></span>
<span data-ttu-id="34913-127">Indica che questo cmdlet ottiene solo la visualizzazione dell'istanza del set di scalabilità della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="34913-127">Indicates that this cmdlet gets only the instance view of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="34913-128">-OSUpgradeHistory</span><span class="sxs-lookup"><span data-stu-id="34913-128">-OSUpgradeHistory</span></span>
<span data-ttu-id="34913-129">Indica che questo cmdlet elenca la cronologia di aggiornamento del sistema operativo del set di scalabilità delle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="34913-129">Indicates that this cmdlet lists the os upgrade history of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="34913-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34913-130">-ResourceGroupName</span></span>
<span data-ttu-id="34913-131">Specifica il nome del gruppo di risorse del sistema VMSS.</span><span class="sxs-lookup"><span data-stu-id="34913-131">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="34913-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="34913-132">-VMScaleSetName</span></span>
<span data-ttu-id="34913-133">Specie il nome del sistema VMSS.</span><span class="sxs-lookup"><span data-stu-id="34913-133">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="34913-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34913-134">CommonParameters</span></span>
<span data-ttu-id="34913-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34913-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34913-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="34913-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34913-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="34913-137">INPUTS</span></span>

### <span data-ttu-id="34913-138">System.String</span><span class="sxs-lookup"><span data-stu-id="34913-138">System.String</span></span>

## <span data-ttu-id="34913-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="34913-139">OUTPUTS</span></span>

### <span data-ttu-id="34913-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="34913-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="34913-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="34913-141">NOTES</span></span>

## <span data-ttu-id="34913-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="34913-142">RELATED LINKS</span></span>

[<span data-ttu-id="34913-143">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="34913-143">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="34913-144">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="34913-144">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="34913-145">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="34913-145">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="34913-146">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="34913-146">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="34913-147">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="34913-147">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="34913-148">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="34913-148">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="34913-149">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="34913-149">Update-AzVmss</span></span>](./Update-AzVmss.md)


