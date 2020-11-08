---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
ms.openlocfilehash: e9156887f328242f8c4896dc707a1814f58f2869
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192319"
---
# <span data-ttu-id="9de1f-101">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="9de1f-101">New-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="9de1f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9de1f-102">SYNOPSIS</span></span>
<span data-ttu-id="9de1f-103">Il cmdlet New-AzVirtualHubVnetConnection crea una risorsa HubVirtualNetworkConnection che peer una rete virtuale all'hub virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="9de1f-103">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="9de1f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9de1f-104">SYNTAX</span></span>

### <span data-ttu-id="9de1f-105">ByVirtualHubNameByRemoteVirtualNetworkObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9de1f-105">ByVirtualHubNameByRemoteVirtualNetworkObject (Default)</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9de1f-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="9de1f-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9de1f-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="9de1f-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9de1f-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="9de1f-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9de1f-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="9de1f-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9de1f-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="9de1f-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9de1f-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9de1f-111">DESCRIPTION</span></span>
<span data-ttu-id="9de1f-112">Il cmdlet New-AzVirtualHubVnetConnection crea una risorsa HubVirtualNetworkConnection che peer una rete virtuale all'hub virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="9de1f-112">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="9de1f-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9de1f-113">EXAMPLES</span></span>

### <span data-ttu-id="9de1f-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9de1f-114">Example 1</span></span>

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

<span data-ttu-id="9de1f-115">Il precedente creerà un gruppo di risorse, una WAN virtuale, una rete virtuale, un hub virtuale negli Stati Uniti centrali nel gruppo di risorse in Azure.</span><span class="sxs-lookup"><span data-stu-id="9de1f-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="9de1f-116">Verrà creata successivamente una connessione di rete virtuale che peererà la rete virtuale all'hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="9de1f-116">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

### <span data-ttu-id="9de1f-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9de1f-117">Example 2</span></span>

<span data-ttu-id="9de1f-118">Il cmdlet New-AzVirtualHubVnetConnection crea una risorsa HubVirtualNetworkConnection che peer una rete virtuale all'hub virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="9de1f-118">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span> <span data-ttu-id="9de1f-119">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="9de1f-119">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVirtualHubVnetConnection -EnableInternetSecurity -Name 'testvnetconnection' -ParentResourceName 'westushub' -RemoteVirtualNetwork <PSVirtualNetwork> -ResourceGroupName 'testRG'
```

## <span data-ttu-id="9de1f-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9de1f-120">PARAMETERS</span></span>

### <span data-ttu-id="9de1f-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9de1f-121">-AsJob</span></span>
<span data-ttu-id="9de1f-122">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="9de1f-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9de1f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9de1f-123">-DefaultProfile</span></span>
<span data-ttu-id="9de1f-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9de1f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9de1f-125">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="9de1f-125">-EnableInternetSecurity</span></span>
<span data-ttu-id="9de1f-126">Abilitare la sicurezza Internet per la connessione</span><span class="sxs-lookup"><span data-stu-id="9de1f-126">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="9de1f-127">-EnableInternetSecurityFlag</span><span class="sxs-lookup"><span data-stu-id="9de1f-127">-EnableInternetSecurityFlag</span></span>
<span data-ttu-id="9de1f-128">Abilitare la sicurezza Internet per la connessione</span><span class="sxs-lookup"><span data-stu-id="9de1f-128">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="9de1f-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="9de1f-129">-Name</span></span>
<span data-ttu-id="9de1f-130">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="9de1f-130">The resource name.</span></span>

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

### <span data-ttu-id="9de1f-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9de1f-131">-ParentObject</span></span>
<span data-ttu-id="9de1f-132">Risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="9de1f-132">The parent resource.</span></span>

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

### <span data-ttu-id="9de1f-133">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="9de1f-133">-ParentResourceId</span></span>
<span data-ttu-id="9de1f-134">Risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="9de1f-134">The parent resource.</span></span>

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

### <span data-ttu-id="9de1f-135">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="9de1f-135">-ParentResourceName</span></span>
<span data-ttu-id="9de1f-136">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9de1f-136">The resource group name.</span></span>

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

### <span data-ttu-id="9de1f-137">-RemoteVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9de1f-137">-RemoteVirtualNetwork</span></span>
<span data-ttu-id="9de1f-138">Rete virtuale remota a cui è connessa la connessione di rete virtuale Hub.</span><span class="sxs-lookup"><span data-stu-id="9de1f-138">The remote virtual network to which this hub virtual network connection is connected.</span></span>

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

### <span data-ttu-id="9de1f-139">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="9de1f-139">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="9de1f-140">Rete virtuale remota a cui è connessa la connessione di rete virtuale Hub.</span><span class="sxs-lookup"><span data-stu-id="9de1f-140">The remote virtual network to which this hub virtual network connection is connected.</span></span>

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

### <span data-ttu-id="9de1f-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9de1f-141">-ResourceGroupName</span></span>
<span data-ttu-id="9de1f-142">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9de1f-142">The resource group name.</span></span>

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

### <span data-ttu-id="9de1f-143">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="9de1f-143">-RoutingConfiguration</span></span>
<span data-ttu-id="9de1f-144">Configurazione di routing per la connessione</span><span class="sxs-lookup"><span data-stu-id="9de1f-144">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="9de1f-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9de1f-145">-Confirm</span></span>
<span data-ttu-id="9de1f-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9de1f-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9de1f-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9de1f-147">-WhatIf</span></span>
<span data-ttu-id="9de1f-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9de1f-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9de1f-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9de1f-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9de1f-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9de1f-150">CommonParameters</span></span>
<span data-ttu-id="9de1f-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9de1f-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9de1f-152">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9de1f-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9de1f-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9de1f-153">INPUTS</span></span>

### <span data-ttu-id="9de1f-154">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="9de1f-154">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="9de1f-155">System. String</span><span class="sxs-lookup"><span data-stu-id="9de1f-155">System.String</span></span>

## <span data-ttu-id="9de1f-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9de1f-156">OUTPUTS</span></span>

### <span data-ttu-id="9de1f-157">Microsoft. Azure. Commands. Network. Models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="9de1f-157">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="9de1f-158">Note</span><span class="sxs-lookup"><span data-stu-id="9de1f-158">NOTES</span></span>

## <span data-ttu-id="9de1f-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9de1f-159">RELATED LINKS</span></span>

[<span data-ttu-id="9de1f-160">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="9de1f-160">Get-AzVirtualHubVnetConnection</span></span>](./Get-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="9de1f-161">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="9de1f-161">Remove-AzVirtualHubVnetConnection</span></span>](./Remove-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="9de1f-162">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="9de1f-162">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
