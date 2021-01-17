---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHubVnetConnection.md
ms.openlocfilehash: 0c07686b59f89bfee656701e14a7c938f49eeb86
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350755"
---
# <span data-ttu-id="27ae9-101">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="27ae9-101">Update-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="27ae9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="27ae9-102">SYNOPSIS</span></span>
<span data-ttu-id="27ae9-103">Aggiorna un HubVirtualNetworkConnection esistente.</span><span class="sxs-lookup"><span data-stu-id="27ae9-103">Updates an existing HubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="27ae9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="27ae9-104">SYNTAX</span></span>

### <span data-ttu-id="27ae9-105">ByHubVirtualNetworkConnectionName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="27ae9-105">ByHubVirtualNetworkConnectionName (Default)</span></span>
```
Update-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="27ae9-106">ByHubVirtualNetworkConnectionObject</span><span class="sxs-lookup"><span data-stu-id="27ae9-106">ByHubVirtualNetworkConnectionObject</span></span>
```
Update-AzVirtualHubVnetConnection -InputObject <PSHubVirtualNetworkConnection>
 [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="27ae9-107">ByHubVirtualNetworkConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="27ae9-107">ByHubVirtualNetworkConnectionResourceId</span></span>
```
Update-AzVirtualHubVnetConnection -ResourceId <String> [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27ae9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="27ae9-108">DESCRIPTION</span></span>
<span data-ttu-id="27ae9-109">Aggiorna un HubVirtualNetworkConnection esistente.</span><span class="sxs-lookup"><span data-stu-id="27ae9-109">Updates an existing HubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="27ae9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="27ae9-110">EXAMPLES</span></span>

### <span data-ttu-id="27ae9-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="27ae9-111">Example 1</span></span>
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

<span data-ttu-id="27ae9-112">Il precedente creerà un gruppo di risorse, una WAN virtuale, una rete virtuale, un hub virtuale negli Stati Uniti centrali nel gruppo di risorse in Azure.</span><span class="sxs-lookup"><span data-stu-id="27ae9-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="27ae9-113">Viene creata anche una connessione di rete virtuale che consente di peer la rete virtuale all'hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="27ae9-113">A Virtual Network Connection is also created which is peer the Virtual Network to the Virtual Hub.</span></span> <span data-ttu-id="27ae9-114">Questa connessione di rete virtuale viene quindi aggiornata per abilitare la sicurezza Internet.</span><span class="sxs-lookup"><span data-stu-id="27ae9-114">This Virtual Network Connection is then updated to enable internet security.</span></span>

## <span data-ttu-id="27ae9-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="27ae9-115">PARAMETERS</span></span>

### <span data-ttu-id="27ae9-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="27ae9-116">-AsJob</span></span>
<span data-ttu-id="27ae9-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="27ae9-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="27ae9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27ae9-118">-DefaultProfile</span></span>
<span data-ttu-id="27ae9-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="27ae9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27ae9-120">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="27ae9-120">-EnableInternetSecurity</span></span>
<span data-ttu-id="27ae9-121">Abilitare la sicurezza Internet per la connessione.</span><span class="sxs-lookup"><span data-stu-id="27ae9-121">Enable internet security for this connection.</span></span>

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

### <span data-ttu-id="27ae9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27ae9-122">-InputObject</span></span>
<span data-ttu-id="27ae9-123">La risorsa hubvirtualnetworkconnection da modificare.</span><span class="sxs-lookup"><span data-stu-id="27ae9-123">The hubvirtualnetworkconnection resource to modify.</span></span>

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

### <span data-ttu-id="27ae9-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="27ae9-124">-Name</span></span>
<span data-ttu-id="27ae9-125">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="27ae9-125">The resource name.</span></span>

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

### <span data-ttu-id="27ae9-126">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="27ae9-126">-ParentResourceName</span></span>
<span data-ttu-id="27ae9-127">Il nome della risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="27ae9-127">The parent resource name.</span></span>

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

### <span data-ttu-id="27ae9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27ae9-128">-ResourceGroupName</span></span>
<span data-ttu-id="27ae9-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="27ae9-129">The resource group name.</span></span>

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

### <span data-ttu-id="27ae9-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27ae9-130">-ResourceId</span></span>
<span data-ttu-id="27ae9-131">ID risorsa della risorsa hubvirtualnetworkconnection da modificare.</span><span class="sxs-lookup"><span data-stu-id="27ae9-131">The resource id of the hubvirtualnetworkconnection resource to modify.</span></span>

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

### <span data-ttu-id="27ae9-132">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="27ae9-132">-RoutingConfiguration</span></span>
<span data-ttu-id="27ae9-133">Configurazione di routing per la connessione</span><span class="sxs-lookup"><span data-stu-id="27ae9-133">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="27ae9-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="27ae9-134">-Confirm</span></span>
<span data-ttu-id="27ae9-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27ae9-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27ae9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27ae9-136">-WhatIf</span></span>
<span data-ttu-id="27ae9-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27ae9-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27ae9-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27ae9-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27ae9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27ae9-139">CommonParameters</span></span>
<span data-ttu-id="27ae9-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27ae9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27ae9-141">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27ae9-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27ae9-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="27ae9-142">INPUTS</span></span>

### <span data-ttu-id="27ae9-143">System. String</span><span class="sxs-lookup"><span data-stu-id="27ae9-143">System.String</span></span>

### <span data-ttu-id="27ae9-144">Microsoft. Azure. Commands. Network. Models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="27ae9-144">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="27ae9-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="27ae9-145">OUTPUTS</span></span>

### <span data-ttu-id="27ae9-146">Microsoft. Azure. Commands. Network. Models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="27ae9-146">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="27ae9-147">Note</span><span class="sxs-lookup"><span data-stu-id="27ae9-147">NOTES</span></span>

## <span data-ttu-id="27ae9-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="27ae9-148">RELATED LINKS</span></span>

[<span data-ttu-id="27ae9-149">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="27ae9-149">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
