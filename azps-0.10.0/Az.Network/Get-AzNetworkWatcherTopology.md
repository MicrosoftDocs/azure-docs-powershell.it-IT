---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchertopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherTopology.md
ms.openlocfilehash: 72f5c803c7fa4f4693da3660c41f73eadb464ab7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860710"
---
# <span data-ttu-id="3160e-101">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="3160e-101">Get-AzNetworkWatcherTopology</span></span>

## <span data-ttu-id="3160e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3160e-102">SYNOPSIS</span></span>
<span data-ttu-id="3160e-103">Ottiene una visualizzazione a livello di rete delle risorse e delle relative relazioni in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3160e-103">Gets a network level view of resources and their relationships in a resource group.</span></span>

## <span data-ttu-id="3160e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3160e-104">SYNTAX</span></span>

### <span data-ttu-id="3160e-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3160e-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherTopology -NetworkWatcher <PSNetworkWatcher> -TargetResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3160e-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="3160e-106">SetByName</span></span>
```
Get-AzNetworkWatcherTopology -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3160e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3160e-107">DESCRIPTION</span></span>
<span data-ttu-id="3160e-108">Il cmdlet Get-AzNetworkWatcherTopology una visualizzazione a livello di rete delle risorse e delle relative relazioni in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3160e-108">The Get-AzNetworkWatcherTopology cmdlet a network level view of resources and their relationships in a resource group.</span></span> <span data-ttu-id="3160e-109">Nota: se le risorse provenienti da più aree geografiche si trovano nel gruppo risorse, nell'output JSON verranno incluse solo le risorse della stessa area di Watcher Network.</span><span class="sxs-lookup"><span data-stu-id="3160e-109">Note: If resources from multiple regions reside in the resource group, only the resources in the same region as the Network Watcher will be included in the JSON output.</span></span>

## <span data-ttu-id="3160e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3160e-110">EXAMPLES</span></span>

### <span data-ttu-id="3160e-111">--------------------------Esempio 1: ottenere una topologia di Azure--------------------------</span><span class="sxs-lookup"><span data-stu-id="3160e-111">--------------------------  Example 1: Get an Azure Topology  --------------------------</span></span>
```
$networkWatcher = Get-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG 
Get-AzNetworkWatcherTopology -NetworkWatcher $networkWatcher -ResourceGroupName testresourcegroup

Id                : e33d80cf-4f76-4b8f-b51c-5bb8eba80103
CreatedDateTime   : 0/00/0000 9:21:51 PM
LastModified      : 0/00/0000 4:53:29 AM
TopologyResources : [
                      {
                        "Name": "testresourcegroup-vnet",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/virtualNetworks/testresourcegroup-vnet",
                        "Location": "westcentralus",
                        "TopologyAssociations": [
                          {
                            "Name": "default",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/virtualNetworks/testresourcegroup-vnet/subnets/default",
                            "AssociationType": "Contains"
                          }
                        ]
                      },
                      {
                        "Name": "default",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/virtualNetworks/testresourcegroup-vnet/subnets/default",
                        "Location": "westcentralus",
                        "TopologyAssociations": []
                      },
                      {
                        "Name": "VM0",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Compute/virtualMachines/VM0",
                        "TopologyAssociations": [
                          {
                            "Name": "vm0131",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkInterfaces/vm0131",
                            "AssociationType": "Contains"
                          }
                        ]
                      },
                      {
                        "Name": "vm0131",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkInterfaces/vm0131",
                        "Location": "westcentralus",
                        "TopologyAssociations": [
                          {
                            "Name": "VM0",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Compute/virtualMachines/VM0",
                            "AssociationType": "Associated"
                          },
                          {
                            "Name": "VM0-nsg",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkSecurityGroups/VM0-nsg",
                            "AssociationType": "Associated"
                          },
                          {
                            "Name": "default",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/virtualNetworks/testresourcegroup-vnet/subnets/default",
                            "AssociationType": "Associated"
                          },
                          {
                            "Name": "VM0-ip",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/publicIPAddresses/VM0-ip",
                            "AssociationType": "Associated"
                          }
                        ]
                      },
                      {
                        "Name": "VM0-nsg",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkSecurityGroups/VM0-nsg",
                        "Location": "westcentralus",
                        "TopologyAssociations": [
                          {
                            "Name": "default-allow-rdp",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkSecurityGroups/VM0-nsg/securityRules/default-allow-rdp",
                            "AssociationType": "Contains"
                          }
                        ]
                      },
                      {
                        "Name": "default-allow-rdp",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkSecurityGroups/VM0-nsg/securityRules/default-allow-rdp",
                        "Location": "westcentralus",
                        "TopologyAssociations": []
                      },
                      {
                        "Name": "VM0-ip",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/publicIPAddresses/VM0-ip",
                        "Location": "westcentralus",
                        "TopologyAssociations": [
                          {
                            "Name": "vm0131",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkInterfaces/vm0131",
                            "AssociationType": "Associated"
                          }
                        ]
                      }
                    ]
```

<span data-ttu-id="3160e-112">In questo esempio viene eseguito il cmdlet Get-AzNetworkWatcherTopology in un gruppo di risorse che contiene una VM, una NIC, NSG e un IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="3160e-112">In this example we run the Get-AzNetworkWatcherTopology cmdlet on a resource group that contains a VM, Nic, NSG, and public IP.</span></span>

## <span data-ttu-id="3160e-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3160e-113">PARAMETERS</span></span>

### <span data-ttu-id="3160e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3160e-114">-DefaultProfile</span></span>
<span data-ttu-id="3160e-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3160e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3160e-116">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3160e-116">-NetworkWatcher</span></span>
<span data-ttu-id="3160e-117">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="3160e-117">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3160e-118">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="3160e-118">-NetworkWatcherName</span></span>
<span data-ttu-id="3160e-119">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="3160e-119">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3160e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3160e-120">-ResourceGroupName</span></span>
<span data-ttu-id="3160e-121">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="3160e-121">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3160e-122">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3160e-122">-TargetResourceGroupName</span></span>
<span data-ttu-id="3160e-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3160e-123">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3160e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3160e-124">CommonParameters</span></span>
<span data-ttu-id="3160e-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3160e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3160e-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3160e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3160e-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3160e-127">INPUTS</span></span>

### <span data-ttu-id="3160e-128">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3160e-128">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="3160e-129">System. String</span><span class="sxs-lookup"><span data-stu-id="3160e-129">System.String</span></span>

## <span data-ttu-id="3160e-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3160e-130">OUTPUTS</span></span>

### <span data-ttu-id="3160e-131">Microsoft. Azure. Commands. Network. Models. PSTopology</span><span class="sxs-lookup"><span data-stu-id="3160e-131">Microsoft.Azure.Commands.Network.Models.PSTopology</span></span>

## <span data-ttu-id="3160e-132">Note</span><span class="sxs-lookup"><span data-stu-id="3160e-132">NOTES</span></span>
<span data-ttu-id="3160e-133">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher, topologia, visualizzazione</span><span class="sxs-lookup"><span data-stu-id="3160e-133">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, topology, view</span></span> 

## <span data-ttu-id="3160e-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3160e-134">RELATED LINKS</span></span>

[<span data-ttu-id="3160e-135">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3160e-135">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="3160e-136">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3160e-136">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="3160e-137">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3160e-137">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="3160e-138">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3160e-138">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3160e-139">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="3160e-139">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="3160e-140">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3160e-140">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3160e-141">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3160e-141">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3160e-142">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3160e-142">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3160e-143">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="3160e-143">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="3160e-144">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="3160e-144">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="3160e-145">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="3160e-145">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="3160e-146">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="3160e-146">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

