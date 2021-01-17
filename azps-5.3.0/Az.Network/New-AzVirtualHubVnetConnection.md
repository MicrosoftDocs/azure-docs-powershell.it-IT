---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
ms.openlocfilehash: f4087782e247e574cd49634e148b6852e9fb8dc6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476502"
---
# <span data-ttu-id="5e9ff-101">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="5e9ff-101">New-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="5e9ff-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5e9ff-102">SYNOPSIS</span></span>
<span data-ttu-id="5e9ff-103">Il cmdlet New-AzVirtualHubVnetConnection crea una risorsa HubVirtualNetworkConnection che peer una rete virtuale all'hub virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="5e9ff-103">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="5e9ff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5e9ff-104">SYNTAX</span></span>

### <span data-ttu-id="5e9ff-105">ByVirtualHubNameByRemoteVirtualNetworkObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5e9ff-105">ByVirtualHubNameByRemoteVirtualNetworkObject (Default)</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e9ff-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="5e9ff-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e9ff-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="5e9ff-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e9ff-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="5e9ff-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5e9ff-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="5e9ff-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e9ff-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="5e9ff-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5e9ff-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e9ff-111">DESCRIPTION</span></span>
<span data-ttu-id="5e9ff-112">Il cmdlet New-AzVirtualHubVnetConnection crea una risorsa HubVirtualNetworkConnection che peer una rete virtuale all'hub virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="5e9ff-112">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="5e9ff-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5e9ff-113">EXAMPLES</span></span>

### <span data-ttu-id="5e9ff-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5e9ff-114">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
EnableInternetSecurity : False
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

<span data-ttu-id="5e9ff-115">Il precedente creerà un gruppo di risorse, una WAN virtuale, una rete virtuale, un hub virtuale negli Stati Uniti centrali nel gruppo di risorse in Azure.</span><span class="sxs-lookup"><span data-stu-id="5e9ff-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="5e9ff-116">Verrà creata successivamente una connessione di rete virtuale che peererà la rete virtuale all'hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="5e9ff-116">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

### <span data-ttu-id="5e9ff-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="5e9ff-117">Example 2</span></span>

<span data-ttu-id="5e9ff-118">Il cmdlet New-AzVirtualHubVnetConnection crea una risorsa HubVirtualNetworkConnection che peer una rete virtuale all'hub virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="5e9ff-118">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span> <span data-ttu-id="5e9ff-119">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="5e9ff-119">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVirtualHubVnetConnection -EnableInternetSecurity -Name 'testvnetconnection' -ParentResourceName 'westushub' -RemoteVirtualNetwork <PSVirtualNetwork> -ResourceGroupName 'testRG'
```


### <span data-ttu-id="5e9ff-120">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="5e9ff-120">Example 3</span></span>
```powershell
PS C:\> $rgName = "testRg"
PS C:\> $virtualHubName = "testHub"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName $rgName -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $rt1 = Get-AzVHubRouteTable -ResourceGroupName $rgName -VirtualHubName $virtualHubName -Name "defaultRouteTable"
PS C:\> $rt2 = Get-AzVHubRouteTable -ResourceGroupName $rgName -VirtualHubName $virtualHubName -Name "noneRouteTable"
PS C:\> $route1 = New-AzStaticRoute -Name "route1" -AddressPrefix @("10.20.0.0/16", "10.30.0.0/16")-NextHopIpAddress "10.90.0.5"
PS C:\> $routingconfig = New-AzRoutingConfiguration -AssociatedRouteTable $rt1.Id -Label @("testLabel") -Id @($rt2.Id) -StaticRoute @($route1)

AssociatedRouteTable  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/defaultRouteTable"
PropagatedRouteTables : {
                          "Labels": [
                            "testLabel"
                          ],
                          "Ids": [
                            {
                              "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/noneRouteTable"
                            }
                          ]
                        }
VnetRoutes            : {
                          "StaticRoutes": [
                            {
                              "Name": "route1",
                              "AddressPrefixes": [
                                "10.20.0.0/16",
                                "10.30.0.0/16"
                              ],
                              "NextHopIpAddress": "10.90.0.5"
                            }
                          ]
                        }
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName $rgName -VirtualHubName $virtualHubName -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork -RoutingConfiguration $routingconfig
```
<span data-ttu-id="5e9ff-121">Il precedente creerà una nuova configurazione di routing e creerà route statiche nella configurazione di routing con l'hop successivo come indirizzo IP specificato.</span><span class="sxs-lookup"><span data-stu-id="5e9ff-121">The above will create a new routing configuration and create static routes in the routing config with the next hop as a specified IP address.</span></span> <span data-ttu-id="5e9ff-122">Questa configurazione di routing può quindi essere passata al comando New-AzVirtualHubVnetConnection come parametro-RoutingConfiguration.</span><span class="sxs-lookup"><span data-stu-id="5e9ff-122">This routing configuration can then be passed into  the New-AzVirtualHubVnetConnection command as the parameter -RoutingConfiguration.</span></span>

## <span data-ttu-id="5e9ff-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5e9ff-123">PARAMETERS</span></span>

### <span data-ttu-id="5e9ff-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5e9ff-124">-AsJob</span></span>
<span data-ttu-id="5e9ff-125">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="5e9ff-125">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e9ff-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e9ff-126">-DefaultProfile</span></span>
<span data-ttu-id="5e9ff-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5e9ff-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e9ff-128">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="5e9ff-128">-EnableInternetSecurity</span></span>
<span data-ttu-id="5e9ff-129">Abilitare la sicurezza Internet per la connessione</span><span class="sxs-lookup"><span data-stu-id="5e9ff-129">Enable internet security for this connection</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e9ff-130">-EnableInternetSecurityFlag</span><span class="sxs-lookup"><span data-stu-id="5e9ff-130">-EnableInternetSecurityFlag</span></span>
<span data-ttu-id="5e9ff-131">Abilitare la sicurezza Internet per la connessione</span><span class="sxs-lookup"><span data-stu-id="5e9ff-131">Enable internet security for this connection</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e9ff-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="5e9ff-132">-Name</span></span>
<span data-ttu-id="5e9ff-133">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="5e9ff-133">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e9ff-134">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5e9ff-134">-ParentObject</span></span>
<span data-ttu-id="5e9ff-135">Risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="5e9ff-135">The parent resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkResourceId
Aliases: VirtualHub, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e9ff-136">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5e9ff-136">-ParentResourceId</span></span>
<span data-ttu-id="5e9ff-137">Risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="5e9ff-137">The parent resource.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceIdByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e9ff-138">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="5e9ff-138">-ParentResourceName</span></span>
<span data-ttu-id="5e9ff-139">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5e9ff-139">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e9ff-140">-RemoteVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5e9ff-140">-RemoteVirtualNetwork</span></span>
<span data-ttu-id="5e9ff-141">Rete virtuale remota a cui è connessa la connessione di rete virtuale Hub.</span><span class="sxs-lookup"><span data-stu-id="5e9ff-141">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e9ff-142">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="5e9ff-142">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="5e9ff-143">Rete virtuale remota a cui è connessa la connessione di rete virtuale Hub.</span><span class="sxs-lookup"><span data-stu-id="5e9ff-143">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkResourceId, ByVirtualHubObjectByRemoteVirtualNetworkResourceId, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e9ff-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e9ff-144">-ResourceGroupName</span></span>
<span data-ttu-id="5e9ff-145">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5e9ff-145">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e9ff-146">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="5e9ff-146">-RoutingConfiguration</span></span>
<span data-ttu-id="5e9ff-147">Configurazione di routing per la connessione</span><span class="sxs-lookup"><span data-stu-id="5e9ff-147">Routing configuration for this connection</span></span>

```yaml
Type: PSRoutingConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e9ff-148">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5e9ff-148">-Confirm</span></span>
<span data-ttu-id="5e9ff-149">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e9ff-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e9ff-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e9ff-150">-WhatIf</span></span>
<span data-ttu-id="5e9ff-151">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5e9ff-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e9ff-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5e9ff-152">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e9ff-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e9ff-153">CommonParameters</span></span>
<span data-ttu-id="5e9ff-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e9ff-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e9ff-155">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e9ff-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e9ff-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5e9ff-156">INPUTS</span></span>

### <span data-ttu-id="5e9ff-157">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="5e9ff-157">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="5e9ff-158">System. String</span><span class="sxs-lookup"><span data-stu-id="5e9ff-158">System.String</span></span>

## <span data-ttu-id="5e9ff-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5e9ff-159">OUTPUTS</span></span>

### <span data-ttu-id="5e9ff-160">Microsoft. Azure. Commands. Network. Models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="5e9ff-160">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="5e9ff-161">Note</span><span class="sxs-lookup"><span data-stu-id="5e9ff-161">NOTES</span></span>

## <span data-ttu-id="5e9ff-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5e9ff-162">RELATED LINKS</span></span>

[<span data-ttu-id="5e9ff-163">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="5e9ff-163">Get-AzVirtualHubVnetConnection</span></span>](./Get-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="5e9ff-164">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="5e9ff-164">Remove-AzVirtualHubVnetConnection</span></span>](./Remove-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="5e9ff-165">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="5e9ff-165">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
