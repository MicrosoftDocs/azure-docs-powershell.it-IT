---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHubVnetConnection.md
ms.openlocfilehash: 1454e3ba3fc3a7e229e064a32146ebddddc19392
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951582"
---
# <span data-ttu-id="1e5ec-101">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="1e5ec-101">Update-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="1e5ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e5ec-102">SYNOPSIS</span></span>
<span data-ttu-id="1e5ec-103">Aggiorna una connessione HubVirtualNetworkConnection esistente.</span><span class="sxs-lookup"><span data-stu-id="1e5ec-103">Updates an existing HubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="1e5ec-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1e5ec-104">SYNTAX</span></span>

### <span data-ttu-id="1e5ec-105">ByHubVirtualNetworkConnectionName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1e5ec-105">ByHubVirtualNetworkConnectionName (Default)</span></span>
```
Update-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e5ec-106">ByHubVirtualNetworkConnectionObject</span><span class="sxs-lookup"><span data-stu-id="1e5ec-106">ByHubVirtualNetworkConnectionObject</span></span>
```
Update-AzVirtualHubVnetConnection -InputObject <PSHubVirtualNetworkConnection>
 [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e5ec-107">ByHubVirtualNetworkConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="1e5ec-107">ByHubVirtualNetworkConnectionResourceId</span></span>
```
Update-AzVirtualHubVnetConnection -ResourceId <String> [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e5ec-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1e5ec-108">DESCRIPTION</span></span>
<span data-ttu-id="1e5ec-109">Aggiorna una connessione HubVirtualNetworkConnection esistente.</span><span class="sxs-lookup"><span data-stu-id="1e5ec-109">Updates an existing HubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="1e5ec-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1e5ec-110">EXAMPLES</span></span>

### <span data-ttu-id="1e5ec-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1e5ec-111">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Update-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -EnableInternetSecurity $true
Name                   : testvnetconnection
Id                     : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
EnableInternetSecurity : True
ProvisioningState      : Succeeded
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

<span data-ttu-id="1e5ec-112">Come descritto sopra, verrà creato un gruppo di risorse, WAN virtuale, rete virtuale, hub virtuale negli Stati Uniti centrali in tale gruppo di risorse in Azure.</span><span class="sxs-lookup"><span data-stu-id="1e5ec-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="1e5ec-113">Viene anche creata una connessione di rete virtuale, che è il peer della rete virtuale all'hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="1e5ec-113">A Virtual Network Connection is also created which is peer the Virtual Network to the Virtual Hub.</span></span> <span data-ttu-id="1e5ec-114">Questa connessione di rete virtuale viene quindi aggiornata per abilitare la sicurezza Internet.</span><span class="sxs-lookup"><span data-stu-id="1e5ec-114">This Virtual Network Connection is then updated to enable internet security.</span></span>

## <span data-ttu-id="1e5ec-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e5ec-115">PARAMETERS</span></span>

### <span data-ttu-id="1e5ec-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1e5ec-116">-AsJob</span></span>
<span data-ttu-id="1e5ec-117">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="1e5ec-117">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e5ec-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e5ec-118">-DefaultProfile</span></span>
<span data-ttu-id="1e5ec-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1e5ec-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e5ec-120">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="1e5ec-120">-EnableInternetSecurity</span></span>
<span data-ttu-id="1e5ec-121">Abilitare la sicurezza Internet per questa connessione.</span><span class="sxs-lookup"><span data-stu-id="1e5ec-121">Enable internet security for this connection.</span></span>

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

### <span data-ttu-id="1e5ec-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e5ec-122">-InputObject</span></span>
<span data-ttu-id="1e5ec-123">La risorsa hubvirtualnetworkconnection da modificare.</span><span class="sxs-lookup"><span data-stu-id="1e5ec-123">The hubvirtualnetworkconnection resource to modify.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection
Parameter Sets: ByHubVirtualNetworkConnectionObject
Aliases: HubVirtualNetworkConnection
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e5ec-124">-Name</span><span class="sxs-lookup"><span data-stu-id="1e5ec-124">-Name</span></span>
<span data-ttu-id="1e5ec-125">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="1e5ec-125">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases: ResourceName, HubVirtualNetworkConnectionName
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e5ec-126">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="1e5ec-126">-ParentResourceName</span></span>
<span data-ttu-id="1e5ec-127">Nome della risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="1e5ec-127">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases: VirtualHubName, ParentVirtualHubName
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e5ec-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e5ec-128">-ResourceGroupName</span></span>
<span data-ttu-id="1e5ec-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1e5ec-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases:
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e5ec-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e5ec-130">-ResourceId</span></span>
<span data-ttu-id="1e5ec-131">ID della risorsa hubvirtualnetworkconnection da modificare.</span><span class="sxs-lookup"><span data-stu-id="1e5ec-131">The resource id of the hubvirtualnetworkconnection resource to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionResourceId
Aliases: HubVirtualNetworkConnectionId
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e5ec-132">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="1e5ec-132">-RoutingConfiguration</span></span>
<span data-ttu-id="1e5ec-133">Configurazione del routing per questa connessione</span><span class="sxs-lookup"><span data-stu-id="1e5ec-133">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="1e5ec-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1e5ec-134">-Confirm</span></span>
<span data-ttu-id="1e5ec-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e5ec-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e5ec-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e5ec-136">-WhatIf</span></span>
<span data-ttu-id="1e5ec-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1e5ec-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e5ec-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1e5ec-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e5ec-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e5ec-139">CommonParameters</span></span>
<span data-ttu-id="1e5ec-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e5ec-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e5ec-141">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e5ec-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e5ec-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="1e5ec-142">INPUTS</span></span>

### <span data-ttu-id="1e5ec-143">System.String</span><span class="sxs-lookup"><span data-stu-id="1e5ec-143">System.String</span></span>

### <span data-ttu-id="1e5ec-144">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="1e5ec-144">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="1e5ec-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1e5ec-145">OUTPUTS</span></span>

### <span data-ttu-id="1e5ec-146">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="1e5ec-146">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="1e5ec-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="1e5ec-147">NOTES</span></span>

## <span data-ttu-id="1e5ec-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1e5ec-148">RELATED LINKS</span></span>

[<span data-ttu-id="1e5ec-149">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="1e5ec-149">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
