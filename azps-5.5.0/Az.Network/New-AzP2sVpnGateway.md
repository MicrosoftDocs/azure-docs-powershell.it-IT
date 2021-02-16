---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzP2sVpnGateway.md
ms.openlocfilehash: 401fa91682e68b74e950d5010b22ce140436b06a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184423"
---
# <span data-ttu-id="de0a0-101">New-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="de0a0-101">New-AzP2sVpnGateway</span></span>

## <span data-ttu-id="de0a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de0a0-102">SYNOPSIS</span></span>
<span data-ttu-id="de0a0-103">Creare un nuovo P2SVpnGateway in VirtualHub per la connettività del sito punto a punto.</span><span class="sxs-lookup"><span data-stu-id="de0a0-103">Create a new P2SVpnGateway under VirtualHub for point to site connectivity.</span></span>

## <span data-ttu-id="de0a0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="de0a0-104">SYNTAX</span></span>

### <span data-ttu-id="de0a0-105">ByVirtualHubNameByVpnServerConfigurationObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="de0a0-105">ByVirtualHubNameByVpnServerConfigurationObject (Default)</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> [-VpnServerConfiguration <PSVpnServerConfiguration>] -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>] [-RoutingConfiguration <PSRoutingConfiguration>] [-EnableInternetSecurityFlag]
 [-EnableRoutingPreferenceInternetFlag] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de0a0-106">ByVirtualHubNameByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="de0a0-106">ByVirtualHubNameByVpnServerConfigurationResourceId</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>] [-RoutingConfiguration <PSRoutingConfiguration>] [-EnableInternetSecurityFlag]
 [-EnableRoutingPreferenceInternetFlag] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de0a0-107">ByVirtualHubObjectByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="de0a0-107">ByVirtualHubObjectByVpnServerConfigurationObject</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> [-VpnServerConfiguration <PSVpnServerConfiguration>]
 -VpnClientAddressPool <String[]> [-CustomDnsServer <String[]>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-EnableInternetSecurityFlag]
 [-EnableRoutingPreferenceInternetFlag] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de0a0-108">ByVirtualHubObjectByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="de0a0-108">ByVirtualHubObjectByVpnServerConfigurationResourceId</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>] [-RoutingConfiguration <PSRoutingConfiguration>] [-EnableInternetSecurityFlag]
 [-EnableRoutingPreferenceInternetFlag] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de0a0-109">ByVirtualHubResourceIdByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="de0a0-109">ByVirtualHubResourceIdByVpnServerConfigurationObject</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> [-VpnServerConfiguration <PSVpnServerConfiguration>] -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>] [-RoutingConfiguration <PSRoutingConfiguration>] [-EnableInternetSecurityFlag]
 [-EnableRoutingPreferenceInternetFlag] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de0a0-110">ByVirtualHubResourceIdByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="de0a0-110">ByVirtualHubResourceIdByVpnServerConfigurationResourceId</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>] [-RoutingConfiguration <PSRoutingConfiguration>] [-EnableInternetSecurityFlag]
 [-EnableRoutingPreferenceInternetFlag] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de0a0-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="de0a0-111">DESCRIPTION</span></span>
<span data-ttu-id="de0a0-112">Il cmdlet New-AzP2sVpnGateway consente di creare un nuovo P2SVpnGateway in VirtualHub per la connettività del punto al sito dai client dei punti al sito ad Azure VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="de0a0-112">The New-AzP2sVpnGateway cmdlet enables you to create a new P2SVpnGateway under VirtualHub for Point to site connectivity from Point to site clients to Azure VirtualWan.</span></span>

## <span data-ttu-id="de0a0-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="de0a0-113">EXAMPLES</span></span>

### <span data-ttu-id="de0a0-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="de0a0-114">Example 1</span></span>
```
PS C:\> $virtualHub = Get-AzVirtualHub -ResourceGroupName P2SCortexGATesting -Name WestUsVirtualHub
PS C:\> $vpnServerConfig1 = Get-AzVpnServerConfiguration -ResourceGroupName P2SCortexGATesting -Name WestUsConfig
PS C:\> $vpnClientAddressSpaces = New-Object string[] 1
PS C:\> $vpnClientAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $createdP2SVpnGateway = New-AzP2sVpnGateway -ResourceGroupName P2SCortexGATesting -Name 683482ade8564515aed4b8448c9757ea-westus-gw -VirtualHub $virtualHub -VpnGatewayScaleUnit 1 -VpnClientAddressPool $vpnClientAddressSpaces -VpnServerConfiguration $vpnServerConfig1 -EnableInternetSecurityFlag -EnableRoutingPreferenceInternetFlag

ResourceGroupName              : P2SCortexGATesting
Name                           : 683482ade8564515aed4b8448c9757ea-westus-gw
Id                             : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482ade8564515a
                                 ed4b8448c9757ea-westus-gw
Location                       : westus
VpnGatewayScaleUnit            : 1
VirtualHub                     : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub
VpnServerConfiguration         : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig
VpnServerConfigurationLocation :
VpnClientConnectionHealth      : null
Type                           : Microsoft.Network/p2sVpnGateways
ProvisioningState              : Succeeded
P2SConnectionConfigurations    : [
                                   {
                                     "ProvisioningState": "Succeeded",
                                     "VpnClientAddressPool": {
                                       "AddressPrefixes": [
                                         "192.168.2.0/24"
                                       ]
                                     },
                                     "EnableInternetSecurity": True,
                                     "RoutingConfiguration": {
                                       "AssociatedRouteTable": {
                                         "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub/hubRouteTables/defaultRouteTable"
                                       }
                                       "PropagatedRouteTables": {
                                         "Labels": [],
                                         "Ids": [
                                           {
                                            "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub/hubRouteTables/defaultRouteTable"
                                           }
                                        ]
                                       },
                                       "VnetRoutes": {
                                         "StaticRoutes": []
                                       }
                                     },
                                     "Name": "P2SConnectionConfigDefault",
                                     "Etag": "W/\"4b96e6a2-b4d8-46b3-9210-76d40f359bef\"",
                                     "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482
                                 ade8564515aed4b8448c9757ea-westus-gw/p2sConnectionConfigurations/P2SConnectionConfigDefault"
                                   }
                                 ]
```

<span data-ttu-id="de0a0-115">Il cmdlet New-AzP2sVpnGateway consente di creare un nuovo P2SVpnGateway in VirtualHub per la connettività del sito point to site.</span><span class="sxs-lookup"><span data-stu-id="de0a0-115">The New-AzP2sVpnGateway cmdlet enables you to create a new P2SVpnGateway under VirtualHub for Point to site connectivity.</span></span>

## <span data-ttu-id="de0a0-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de0a0-116">PARAMETERS</span></span>

### <span data-ttu-id="de0a0-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de0a0-117">-AsJob</span></span>
<span data-ttu-id="de0a0-118">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="de0a0-118">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de0a0-119">-CustomDnsServer</span><span class="sxs-lookup"><span data-stu-id="de0a0-119">-CustomDnsServer</span></span>
<span data-ttu-id="de0a0-120">Elenco dei server DNS personalizzati.</span><span class="sxs-lookup"><span data-stu-id="de0a0-120">The list of Custom Dns Servers.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de0a0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de0a0-121">-DefaultProfile</span></span>
<span data-ttu-id="de0a0-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="de0a0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de0a0-123">-Name</span><span class="sxs-lookup"><span data-stu-id="de0a0-123">-Name</span></span>
<span data-ttu-id="de0a0-124">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="de0a0-124">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, P2SVpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de0a0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de0a0-125">-ResourceGroupName</span></span>
<span data-ttu-id="de0a0-126">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="de0a0-126">The resource name.</span></span>

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

### <span data-ttu-id="de0a0-127">-EnableInternetSecurityFlag</span><span class="sxs-lookup"><span data-stu-id="de0a0-127">-EnableInternetSecurityFlag</span></span>
<span data-ttu-id="de0a0-128">Abilita il contrassegno di sicurezza Internet per queste connessioni P2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="de0a0-128">Enable internet security flag for this P2SVpnGateway connections</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de0a0-129">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="de0a0-129">-RoutingConfiguration</span></span>
<span data-ttu-id="de0a0-130">Configurazione del routing per questa connessione</span><span class="sxs-lookup"><span data-stu-id="de0a0-130">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="de0a0-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="de0a0-131">-Tag</span></span>
<span data-ttu-id="de0a0-132">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="de0a0-132">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de0a0-133">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="de0a0-133">-VirtualHub</span></span>
<span data-ttu-id="de0a0-134">VirtualHub a cui deve essere associato questo P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="de0a0-134">The VirtualHub this P2SVpnGateway needs to be associated with.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObjectByVpnServerConfigurationObject, ByVirtualHubObjectByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de0a0-135">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="de0a0-135">-VirtualHubId</span></span>
<span data-ttu-id="de0a0-136">ID di VirtualHub a cui deve essere associato questo P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="de0a0-136">The Id of the VirtualHub this P2SVpnGateway needs to be associated with.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceIdByVpnServerConfigurationObject, ByVirtualHubResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de0a0-137">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="de0a0-137">-VirtualHubName</span></span>
<span data-ttu-id="de0a0-138">ID di VirtualHub a cui deve essere associato questo P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="de0a0-138">The Id of the VirtualHub this P2SVpnGateway needs to be associated with.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByVpnServerConfigurationObject, ByVirtualHubNameByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de0a0-139">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="de0a0-139">-VpnClientAddressPool</span></span>
<span data-ttu-id="de0a0-140">P2S VpnClient AddressPool per questo P2SVpnGateway P2SConnectionConfiguration.</span><span class="sxs-lookup"><span data-stu-id="de0a0-140">P2S VpnClient AddressPool for this P2SVpnGateway P2SConnectionConfiguration.</span></span>

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

### <span data-ttu-id="de0a0-141">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="de0a0-141">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="de0a0-142">L'unità di scala per questo P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="de0a0-142">The scale unit for this P2SVpnGateway.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de0a0-143">-VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="de0a0-143">-VpnServerConfiguration</span></span>
<span data-ttu-id="de0a0-144">VpnServerConfiguration da associare a questo P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="de0a0-144">The VpnServerConfiguration to be attached to this P2SVpnGateway.</span></span>

```yaml
Type: PSVpnServerConfiguration
Parameter Sets: ByVirtualHubNameByVpnServerConfigurationObject, ByVirtualHubObjectByVpnServerConfigurationObject, ByVirtualHubResourceIdByVpnServerConfigurationObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de0a0-145">-VpnServerConfigurationId</span><span class="sxs-lookup"><span data-stu-id="de0a0-145">-VpnServerConfigurationId</span></span>
<span data-ttu-id="de0a0-146">ID dell'oggetto di configurazione del server Vpn a cui verrà associato questo P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="de0a0-146">The id of Vpn server configuration object this P2SVpnGateway will be attached to.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByVpnServerConfigurationResourceId, ByVirtualHubObjectByVpnServerConfigurationResourceId, ByVirtualHubResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de0a0-147">-EnableRoutingPreferenceInternetFlag</span><span class="sxs-lookup"><span data-stu-id="de0a0-147">-EnableRoutingPreferenceInternetFlag</span></span>
<span data-ttu-id="de0a0-148">Flag per abilitare la preferenza di routing Internet in questo P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="de0a0-148">Flag to enable Routing Preference Internet on this P2SVpnGateway.</span></span>

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

### <span data-ttu-id="de0a0-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="de0a0-149">-Confirm</span></span>
<span data-ttu-id="de0a0-150">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de0a0-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de0a0-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de0a0-151">-WhatIf</span></span>
<span data-ttu-id="de0a0-152">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="de0a0-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de0a0-153">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="de0a0-153">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de0a0-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de0a0-154">CommonParameters</span></span>
<span data-ttu-id="de0a0-155">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de0a0-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de0a0-156">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="de0a0-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de0a0-157">INPUT</span><span class="sxs-lookup"><span data-stu-id="de0a0-157">INPUTS</span></span>

### <span data-ttu-id="de0a0-158">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="de0a0-158">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>
<span data-ttu-id="de0a0-159">System.String Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="de0a0-159">System.String Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="de0a0-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="de0a0-160">OUTPUTS</span></span>

### <span data-ttu-id="de0a0-161">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="de0a0-161">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>
## <span data-ttu-id="de0a0-162">NOTE</span><span class="sxs-lookup"><span data-stu-id="de0a0-162">NOTES</span></span>

## <span data-ttu-id="de0a0-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="de0a0-163">RELATED LINKS</span></span>

[<span data-ttu-id="de0a0-164">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="de0a0-164">New-AzRoutingConfiguration</span></span>]()

