---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRoute.md
ms.openlocfilehash: 3acbbb9cba8ed18ef933a7e76349eadf1224938a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987781"
---
# <span data-ttu-id="12e48-101">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="12e48-101">New-AzVHubRoute</span></span>

## <span data-ttu-id="12e48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12e48-102">SYNOPSIS</span></span>
<span data-ttu-id="12e48-103">Crea un oggetto VHubRoute che può essere passato come parametro al comando New-AzVHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="12e48-103">Creates a VHubRoute object which can be passed as parameter to the New-AzVHubRouteTable command.</span></span>

## <span data-ttu-id="12e48-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="12e48-104">SYNTAX</span></span>

```powershell
New-AzVHubRoute -Name <String> -Destination <String[]> -DestinationType <String> -NextHop <String> -NextHopType <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12e48-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="12e48-105">DESCRIPTION</span></span>

<span data-ttu-id="12e48-106">Crea un oggetto VHubRoute.</span><span class="sxs-lookup"><span data-stu-id="12e48-106">Creates a VHubRoute object.</span></span>

## <span data-ttu-id="12e48-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="12e48-107">EXAMPLES</span></span>

### <span data-ttu-id="12e48-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="12e48-108">Example 1</span></span>

```powershell
PS C:\> $rgName = "testRg"
PS C:\> $firewallName = "testFirewall"
PS C:\> $firewall = Get-AzFirewall -Name $firewallName -ResourceGroupName $rgName
PS C:\> New-AzVHubRoute -Name "private-traffic" -Destination @("10.30.0.0/16", "10.40.0.0/16") -DestinationType "CIDR" -NextHop $firewall.Id -NextHopType "ResourceId"

Name            : private-traffic
DestinationType : CIDR
Destinations    : {10.30.0.0/16, 10.40.0.0/16}
NextHopType     : ResourceId
NextHop         : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/azureFirewalls/testFirewall
```

<span data-ttu-id="12e48-109">Il comando precedente crea un oggetto VHubRoute con nextHop come firewall specificato, che può quindi essere aggiunto a una risorsa VHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="12e48-109">The above command will create a VHubRoute object with nextHop as the specified Firewall which can then be added to a VHubRouteTable resource.</span></span>

### <span data-ttu-id="12e48-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="12e48-110">Example 2</span></span>

```powershell
PS C:\> $rgName = "testRg"
PS C:\> $hubName = "testHub"
PS C:\> $hubVnetConnName = "testHubVnetConn"
PS C:\> $hubVnetConnection = Get-AzVirtualHubVnetConnection -Name $hubVnetConnName -ParentResourceName $hubName -ResourceGroupName $rgName
PS C:\> New-AzVHubRoute -Name "nva-traffic" -Destination @("10.20.0.0/16", "10.50.0.0/16") -DestinationType "CIDR" -NextHop $hubVnetConnection.Id -NextHopType "ResourceId"

Name            : private-traffic
DestinationType : CIDR
Destinations    : {10.30.0.0/16, 10.40.0.0/16}
NextHopType     : ResourceId
NextHop         : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubVirtualNetworkConnections/testHubVnetConn
```

<span data-ttu-id="12e48-111">Il comando precedente crea un oggetto VHubRoute con nextHop come hubVnetConnection specificato, che può quindi essere aggiunto a una risorsa VHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="12e48-111">The above command will create a VHubRoute object with nextHop as the specified hubVnetConnection which can then be added to a VHubRouteTable resource.</span></span>


### <span data-ttu-id="12e48-112">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="12e48-112">Example 3</span></span>
```powershell
PS C:\> $hub = Get-AzVirtualHub -ResourceGroupName {rgname} -Name {virtual-hub-name}
PS C:\> $hubVnetConn = Get-AzVirtualHubVnetConnection -ParentObject $hub -Name {connection-name}
PS C:\> $hubVnetConn
Name                   : conn_2
Id                     : /subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualHubs/{virtual-hub-name}/hubVirtualNetworkConnections/conn_2
RemoteVirtualNetwork   : /subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualNetworks/rVnet_2
EnableInternetSecurity : True
ProvisioningState      : Succeeded
RoutingConfiguration   : {
                           "AssociatedRouteTable": {
                             "Id": "/subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualHubs/{virtual-hub-name}/hubRouteTables/defaultRouteTable"
                           },
                           "PropagatedRouteTables": {
                             "Labels": [
                               "default"
                             ],
                             "Ids": [
                               {
                                 "Id":
                         "/subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualHubs/{virtual-hub-name}/hubRouteTables/defaultRouteTable"
                               }
                             ]
                           },
                           "VnetRoutes": {
                             "StaticRoutes": []
                           }
                         }
                         
PS C:\> $staticRoute1 = New-AzStaticRoute -Name "static_route1" -AddressPrefix @("10.2.1.0/24", "10.2.3.0/24") -NextHopIpAddress "10.2.0.5"
PS C:\> $routingConfig = $hubVnetConn.RoutingConfiguration
PS C:\> $routingConfig.VnetRoutes.StaticRoutes = @($staticRoute1)
PS C:\> $routingConfig
AssociatedRouteTable  : Microsoft.Azure.Commands.Network.Models.PSResourceId
PropagatedRouteTables : {
                          "Labels": [
                            "default"
                          ],
                          "Ids": [
                            {
                              "Id":
                        "/subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualHubs/rTestHub1/hubRouteTables/defaultRouteTable"
                            }
                          ]
                        }
VnetRoutes            : {
                          "StaticRoutes": [
                            {
                              "Name": "static_route1",
                              "AddressPrefixes": [
                                "10.2.1.0/24",
                                "10.2.3.0/24"
                              ],
                              "NextHopIpAddress": "10.2.0.5"
                            }
                          ]
                        }

PS C:\> Update-AzVirtualHubVnetConnection -InputObject $hubVnetConn -RoutingConfiguration $routingConfig
```
<span data-ttu-id="12e48-113">I comandi precedenti otterrà la RoutingConfiguration di un AzVHubRoute già esistente e quindi aggiungeranno una route statica nella connessione.</span><span class="sxs-lookup"><span data-stu-id="12e48-113">The above commands will get the RoutingConfiguration of an already existing AzVHubRoute and then add a static route on the connection.</span></span> <span data-ttu-id="12e48-114">In alternativa, se si desidera creare una nuova connessione con la route statica al suo interno, vedere l'esempio 1 [qui.](New-AzRoutingConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="12e48-114">Alternatively, if you hope to create a new connection with the static route within it, please see Example 1 [here.](New-AzRoutingConfiguration.md)</span></span>
## <span data-ttu-id="12e48-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12e48-115">PARAMETERS</span></span>

### <span data-ttu-id="12e48-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12e48-116">-DefaultProfile</span></span>
<span data-ttu-id="12e48-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="12e48-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e48-118">-Destination</span><span class="sxs-lookup"><span data-stu-id="12e48-118">-Destination</span></span>
<span data-ttu-id="12e48-119">Elenco delle destinazioni.</span><span class="sxs-lookup"><span data-stu-id="12e48-119">List of Destinations.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e48-120">-DestinationType</span><span class="sxs-lookup"><span data-stu-id="12e48-120">-DestinationType</span></span>
<span data-ttu-id="12e48-121">Tipo di destinazioni.</span><span class="sxs-lookup"><span data-stu-id="12e48-121">Type of Destinations.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e48-122">-Name</span><span class="sxs-lookup"><span data-stu-id="12e48-122">-Name</span></span>
<span data-ttu-id="12e48-123">Nome della route.</span><span class="sxs-lookup"><span data-stu-id="12e48-123">The route name.</span></span>

```yaml
Type: String
Parameter Sets: (all)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e48-124">-NextHop</span><span class="sxs-lookup"><span data-stu-id="12e48-124">-NextHop</span></span>
<span data-ttu-id="12e48-125">L'hop successivo.</span><span class="sxs-lookup"><span data-stu-id="12e48-125">The next hop.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e48-126">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="12e48-126">-NextHopType</span></span>
<span data-ttu-id="12e48-127">Tipo di hop successivo.</span><span class="sxs-lookup"><span data-stu-id="12e48-127">The Next Hop type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e48-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12e48-128">CommonParameters</span></span>
<span data-ttu-id="12e48-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12e48-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12e48-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="12e48-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12e48-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="12e48-131">INPUTS</span></span>

### <span data-ttu-id="12e48-132">System.String</span><span class="sxs-lookup"><span data-stu-id="12e48-132">System.String</span></span>

## <span data-ttu-id="12e48-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="12e48-133">OUTPUTS</span></span>

### <span data-ttu-id="12e48-134">Microsoft.Azure.Commands.Network.Models.PSVHubRoute</span><span class="sxs-lookup"><span data-stu-id="12e48-134">Microsoft.Azure.Commands.Network.Models.PSVHubRoute</span></span>

## <span data-ttu-id="12e48-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="12e48-135">NOTES</span></span>

## <span data-ttu-id="12e48-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="12e48-136">RELATED LINKS</span></span>

[<span data-ttu-id="12e48-137">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="12e48-137">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="12e48-138">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="12e48-138">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="12e48-139">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="12e48-139">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)

[<span data-ttu-id="12e48-140">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="12e48-140">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)