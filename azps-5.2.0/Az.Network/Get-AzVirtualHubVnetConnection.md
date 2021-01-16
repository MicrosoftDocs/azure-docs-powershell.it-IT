---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubVnetConnection.md
ms.openlocfilehash: 688168317a622cb0375bb111050f3e54696047ff
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356128"
---
# <span data-ttu-id="91c3d-101">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="91c3d-101">Get-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="91c3d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="91c3d-102">SYNOPSIS</span></span>
<span data-ttu-id="91c3d-103">Ottiene una connessione di rete virtuale in un hub virtuale o elenca tutte le connessioni di rete virtuale in un hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="91c3d-103">Gets a Virtual Network Connection in a virtual hub or lists all virtual network connections in a virtual hub.</span></span>

## <span data-ttu-id="91c3d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="91c3d-104">SYNTAX</span></span>

### <span data-ttu-id="91c3d-105">ByVirtualHubName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="91c3d-105">ByVirtualHubName (Default)</span></span>
```
Get-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91c3d-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="91c3d-106">ByVirtualHubObject</span></span>
```
Get-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91c3d-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="91c3d-107">ByVirtualHubResourceId</span></span>
```
Get-AzVirtualHubVnetConnection -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91c3d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91c3d-108">DESCRIPTION</span></span>
<span data-ttu-id="91c3d-109">Ottiene una connessione di rete virtuale in un hub virtuale o elenca tutte le connessioni di rete virtuale in un hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="91c3d-109">Gets a Virtual Network Connection in a virtual hub or lists all virtual network connections in a virtual hub.</span></span>

## <span data-ttu-id="91c3d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="91c3d-110">EXAMPLES</span></span>

### <span data-ttu-id="91c3d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="91c3d-111">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork

PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
RoutingConfiguration : {
                            "AssociatedRouteTable": {
                                "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                            },
                            "PropagatedRouteTables": {
                                "Labels": [],
                                "Ids": [
                                    {
                                        "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                    }
                                ]
                            },
                            "VnetRoutes": {
                                "StaticRoutes": []
                            }
                        }
```

<span data-ttu-id="91c3d-112">Il precedente creerà un gruppo di risorse, una WAN virtuale, una rete virtuale, un hub virtuale negli Stati Uniti centrali nel gruppo di risorse in Azure.</span><span class="sxs-lookup"><span data-stu-id="91c3d-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="91c3d-113">Verrà creata successivamente una connessione di rete virtuale che peererà la rete virtuale all'hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="91c3d-113">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="91c3d-114">Dopo la creazione della connessione di rete virtuale Hub, viene ottenuta la connessione di rete virtuale Hub tramite il nome del gruppo di risorse, il nome dell'hub e il nome della connessione.</span><span class="sxs-lookup"><span data-stu-id="91c3d-114">After the hub virtual network connection is created, it gets the hub virtual network connection using its resource group name, the hub name and the connection name.</span></span>

### <span data-ttu-id="91c3d-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="91c3d-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
RoutingConfiguration : {
                            "AssociatedRouteTable": {
                                "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                            },
                            "PropagatedRouteTables": {
                                "Labels": [],
                                "Ids": [
                                    {
                                        "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                    }
                                ]
                            },
                            "VnetRoutes": {
                                "StaticRoutes": []
                            }
                        }
```

<span data-ttu-id="91c3d-116">Il precedente creerà un gruppo di risorse, una WAN virtuale, una rete virtuale, un hub virtuale negli Stati Uniti centrali nel gruppo di risorse in Azure.</span><span class="sxs-lookup"><span data-stu-id="91c3d-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="91c3d-117">Verrà creata successivamente una connessione di rete virtuale che peererà la rete virtuale all'hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="91c3d-117">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="91c3d-118">Dopo la creazione della connessione di rete virtuale Hub, viene elencata tutta la connessione di rete virtuale Hub con il nome del gruppo di risorse e il nome dell'hub.</span><span class="sxs-lookup"><span data-stu-id="91c3d-118">After the hub virtual network connection is created, it lists all the hub virtual network connection using its resource group name and the hub name.</span></span>

### <span data-ttu-id="91c3d-119">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="91c3d-119">Example 3</span></span>

```powershell
PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name test*

Name                 : testvnetconnection1
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection1
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
RoutingConfiguration : {
                            "AssociatedRouteTable": {
                                "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                            },
                            "PropagatedRouteTables": {
                                "Labels": [],
                                "Ids": [
                                    {
                                        "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                    }
                                ]
                            },
                            "VnetRoutes": {
                                "StaticRoutes": []
                            }
                        }

Name                 : testvnetconnection2
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection2
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
RoutingConfiguration : {
                            "AssociatedRouteTable": {
                                "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                            },
                            "PropagatedRouteTables": {
                                "Labels": [],
                                "Ids": [
                                    {
                                        "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                    }
                                ]
                            },
                            "VnetRoutes": {
                                "StaticRoutes": []
                            }
                        }
```

<span data-ttu-id="91c3d-120">Questo cmdlet elenca tutte le connessioni di rete virtuali Hub che iniziano con "test" usando il nome del gruppo di risorse e il nome dell'hub.</span><span class="sxs-lookup"><span data-stu-id="91c3d-120">This cmdlet lists all the hub virtual network connections starting with "test" using its resource group name and the hub name.</span></span>

## <span data-ttu-id="91c3d-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="91c3d-121">PARAMETERS</span></span>

### <span data-ttu-id="91c3d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91c3d-122">-DefaultProfile</span></span>
<span data-ttu-id="91c3d-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="91c3d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91c3d-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="91c3d-124">-Name</span></span>
<span data-ttu-id="91c3d-125">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="91c3d-125">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="91c3d-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="91c3d-126">-ParentObject</span></span>
<span data-ttu-id="91c3d-127">Risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="91c3d-127">The parent resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91c3d-128">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="91c3d-128">-ParentResourceId</span></span>
<span data-ttu-id="91c3d-129">ID risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="91c3d-129">The parent resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91c3d-130">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="91c3d-130">-ParentResourceName</span></span>
<span data-ttu-id="91c3d-131">Il nome della risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="91c3d-131">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91c3d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91c3d-132">-ResourceGroupName</span></span>
<span data-ttu-id="91c3d-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="91c3d-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91c3d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91c3d-134">CommonParameters</span></span>
<span data-ttu-id="91c3d-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91c3d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91c3d-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="91c3d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91c3d-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="91c3d-137">INPUTS</span></span>

### <span data-ttu-id="91c3d-138">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="91c3d-138">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="91c3d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="91c3d-139">System.String</span></span>

## <span data-ttu-id="91c3d-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="91c3d-140">OUTPUTS</span></span>

### <span data-ttu-id="91c3d-141">Microsoft. Azure. Commands. Network. Models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="91c3d-141">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="91c3d-142">Note</span><span class="sxs-lookup"><span data-stu-id="91c3d-142">NOTES</span></span>

## <span data-ttu-id="91c3d-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="91c3d-143">RELATED LINKS</span></span>

[<span data-ttu-id="91c3d-144">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="91c3d-144">New-AzVirtualHubVnetConnection</span></span>](./New-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="91c3d-145">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="91c3d-145">Remove-AzVirtualHubVnetConnection</span></span>](./Remove-AzVirtualHubVnetConnection.md)
