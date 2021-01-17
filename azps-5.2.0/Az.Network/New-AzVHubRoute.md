---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRoute.md
ms.openlocfilehash: 9cd5a4417f3fd8d6d40cfdf70e6c76f1910ce7c3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330616"
---
# <span data-ttu-id="b5674-101">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="b5674-101">New-AzVHubRoute</span></span>

## <span data-ttu-id="b5674-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b5674-102">SYNOPSIS</span></span>
<span data-ttu-id="b5674-103">Crea un oggetto VHubRoute che può essere passato come parametro al comando New-AzVHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="b5674-103">Creates a VHubRoute object which can be passed as parameter to the New-AzVHubRouteTable command.</span></span>

## <span data-ttu-id="b5674-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b5674-104">SYNTAX</span></span>

```powershell
New-AzVHubRoute -Name <String> -Destination <String[]> -DestinationType <String> -NextHop <String> -NextHopType <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5674-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b5674-105">DESCRIPTION</span></span>

<span data-ttu-id="b5674-106">Crea un oggetto VHubRoute.</span><span class="sxs-lookup"><span data-stu-id="b5674-106">Creates a VHubRoute object.</span></span>

## <span data-ttu-id="b5674-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b5674-107">EXAMPLES</span></span>

### <span data-ttu-id="b5674-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b5674-108">Example 1</span></span>

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

<span data-ttu-id="b5674-109">Il comando precedente creerà un oggetto VHubRoute con nextHop come firewall specificato, che potrà quindi essere aggiunto a una risorsa VHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="b5674-109">The above command will create a VHubRoute object with nextHop as the specified Firewall which can then be added to a VHubRouteTable resource.</span></span>

### <span data-ttu-id="b5674-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b5674-110">Example 2</span></span>

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

<span data-ttu-id="b5674-111">Il comando precedente creerà un oggetto VHubRoute con nextHop come hubVnetConnection specificato, che potrà quindi essere aggiunto a una risorsa VHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="b5674-111">The above command will create a VHubRoute object with nextHop as the specified hubVnetConnection which can then be added to a VHubRouteTable resource.</span></span>


### <span data-ttu-id="b5674-112">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="b5674-112">Example 3</span></span>
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
<span data-ttu-id="b5674-113">I comandi descritti sopra otterranno la RoutingConfiguration di un AzVHubRoute già esistente e quindi aggiungeranno una route statica alla connessione.</span><span class="sxs-lookup"><span data-stu-id="b5674-113">The above commands will get the RoutingConfiguration of an already existing AzVHubRoute and then add a static route on the connection.</span></span> <span data-ttu-id="b5674-114">In alternativa, se si spera di creare una nuova connessione con la route statica al suo interno, vedere l'esempio 1 [qui.](New-AzRoutingConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b5674-114">Alternatively, if you hope to create a new connection with the static route within it, please see Example 1 [here.](New-AzRoutingConfiguration.md)</span></span>
## <span data-ttu-id="b5674-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b5674-115">PARAMETERS</span></span>

### <span data-ttu-id="b5674-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5674-116">-DefaultProfile</span></span>
<span data-ttu-id="b5674-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b5674-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5674-118">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="b5674-118">-Destination</span></span>
<span data-ttu-id="b5674-119">Elenco di destinazioni.</span><span class="sxs-lookup"><span data-stu-id="b5674-119">List of Destinations.</span></span>

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

### <span data-ttu-id="b5674-120">-DestinationType</span><span class="sxs-lookup"><span data-stu-id="b5674-120">-DestinationType</span></span>
<span data-ttu-id="b5674-121">Tipo di destinazioni.</span><span class="sxs-lookup"><span data-stu-id="b5674-121">Type of Destinations.</span></span>

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

### <span data-ttu-id="b5674-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="b5674-122">-Name</span></span>
<span data-ttu-id="b5674-123">Nome della route.</span><span class="sxs-lookup"><span data-stu-id="b5674-123">The route name.</span></span>

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

### <span data-ttu-id="b5674-124">-NextHop</span><span class="sxs-lookup"><span data-stu-id="b5674-124">-NextHop</span></span>
<span data-ttu-id="b5674-125">L'hop successivo.</span><span class="sxs-lookup"><span data-stu-id="b5674-125">The next hop.</span></span>

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

### <span data-ttu-id="b5674-126">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="b5674-126">-NextHopType</span></span>
<span data-ttu-id="b5674-127">Il tipo di hop successivo.</span><span class="sxs-lookup"><span data-stu-id="b5674-127">The Next Hop type.</span></span>

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

### <span data-ttu-id="b5674-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5674-128">CommonParameters</span></span>
<span data-ttu-id="b5674-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5674-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5674-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b5674-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5674-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b5674-131">INPUTS</span></span>

### <span data-ttu-id="b5674-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b5674-132">System.String</span></span>

## <span data-ttu-id="b5674-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b5674-133">OUTPUTS</span></span>

### <span data-ttu-id="b5674-134">Microsoft. Azure. Commands. Network. Models. PSVHubRoute</span><span class="sxs-lookup"><span data-stu-id="b5674-134">Microsoft.Azure.Commands.Network.Models.PSVHubRoute</span></span>

## <span data-ttu-id="b5674-135">Note</span><span class="sxs-lookup"><span data-stu-id="b5674-135">NOTES</span></span>

## <span data-ttu-id="b5674-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b5674-136">RELATED LINKS</span></span>

[<span data-ttu-id="b5674-137">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="b5674-137">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="b5674-138">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="b5674-138">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="b5674-139">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="b5674-139">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)

[<span data-ttu-id="b5674-140">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="b5674-140">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)