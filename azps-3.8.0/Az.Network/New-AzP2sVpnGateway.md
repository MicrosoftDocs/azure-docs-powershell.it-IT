---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzP2sVpnGateway.md
ms.openlocfilehash: 6d16703b7f0492bb2c37291e135cb1b9c836a572
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019732"
---
# <span data-ttu-id="d46bf-101">New-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="d46bf-101">New-AzP2sVpnGateway</span></span>

## <span data-ttu-id="d46bf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d46bf-102">SYNOPSIS</span></span>
<span data-ttu-id="d46bf-103">Creare un nuovo P2SVpnGateway in VirtualHub per la connettività punto a sito.</span><span class="sxs-lookup"><span data-stu-id="d46bf-103">Create a new P2SVpnGateway under VirtualHub for point to site connectivity.</span></span>

## <span data-ttu-id="d46bf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d46bf-104">SYNTAX</span></span>

### <span data-ttu-id="d46bf-105">ByVirtualHubNameByVpnServerConfigurationObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d46bf-105">ByVirtualHubNameByVpnServerConfigurationObject (Default)</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> [-VpnServerConfiguration <PSVpnServerConfiguration>] -VpnClientAddressPool <String[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d46bf-106">ByVirtualHubNameByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="d46bf-106">ByVirtualHubNameByVpnServerConfigurationResourceId</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d46bf-107">ByVirtualHubObjectByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="d46bf-107">ByVirtualHubObjectByVpnServerConfigurationObject</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> [-VpnServerConfiguration <PSVpnServerConfiguration>]
 -VpnClientAddressPool <String[]> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d46bf-108">ByVirtualHubObjectByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="d46bf-108">ByVirtualHubObjectByVpnServerConfigurationResourceId</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d46bf-109">ByVirtualHubResourceIdByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="d46bf-109">ByVirtualHubResourceIdByVpnServerConfigurationObject</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> [-VpnServerConfiguration <PSVpnServerConfiguration>] -VpnClientAddressPool <String[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d46bf-110">ByVirtualHubResourceIdByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="d46bf-110">ByVirtualHubResourceIdByVpnServerConfigurationResourceId</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d46bf-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d46bf-111">DESCRIPTION</span></span>
<span data-ttu-id="d46bf-112">Il cmdlet **New-AzP2sVpnGateway** consente di creare un nuovo P2SVpnGateway in VirtualHub per la connettività del sito da Point a client del sito a Azure VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="d46bf-112">The **New-AzP2sVpnGateway** cmdlet enables you to create a new P2SVpnGateway under VirtualHub for Point to site connectivity from Point to site clients to Azure VirtualWan.</span></span>

## <span data-ttu-id="d46bf-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d46bf-113">EXAMPLES</span></span>

### <span data-ttu-id="d46bf-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d46bf-114">Example 1</span></span>
```powershell
PS C:\> $virtualHub = Get-AzVirtualHub -ResourceGroupName P2SCortexGATesting -Name WestUsVirtualHub
PS C:\> $vpnServerConfig1 = Get-AzVpnServerConfiguration -ResourceGroupName P2SCortexGATesting -Name WestUsConfig
PS C:\> $vpnClientAddressSpaces = New-Object string[] 1
PS C:\> $vpnClientAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $createdP2SVpnGateway = New-AzP2sVpnGateway -ResourceGroupName P2SCortexGATesting -Name 683482ade8564515aed4b8448c9757ea-westus-gw -VirtualHub $virtualHub -VpnGatewayScaleUnit 1 -VpnClientAddressPool $vpnClientAddressSpaces -VpnServerConfiguration $vpnServerConfig1

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
                                     "Name": "P2SConnectionConfigDefault",
                                     "Etag": "W/\"4b96e6a2-b4d8-46b3-9210-76d40f359bef\"",
                                     "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482
                                 ade8564515aed4b8448c9757ea-westus-gw/p2sConnectionConfigurations/P2SConnectionConfigDefault"
                                   }
                                 ]
```

<span data-ttu-id="d46bf-115">Il cmdlet **New-AzP2sVpnGateway** consente di creare un nuovo P2SVpnGateway in VirtualHub per la connettività punto a sito.</span><span class="sxs-lookup"><span data-stu-id="d46bf-115">The **New-AzP2sVpnGateway** cmdlet enables you to create a new P2SVpnGateway under VirtualHub for Point to site connectivity.</span></span>

## <span data-ttu-id="d46bf-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d46bf-116">PARAMETERS</span></span>

### <span data-ttu-id="d46bf-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d46bf-117">-AsJob</span></span>
<span data-ttu-id="d46bf-118">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d46bf-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d46bf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d46bf-119">-DefaultProfile</span></span>
<span data-ttu-id="d46bf-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d46bf-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d46bf-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="d46bf-121">-Name</span></span>
<span data-ttu-id="d46bf-122">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="d46bf-122">The resource name.</span></span>

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

### <span data-ttu-id="d46bf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d46bf-123">-ResourceGroupName</span></span>
<span data-ttu-id="d46bf-124">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="d46bf-124">The resource name.</span></span>

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

### <span data-ttu-id="d46bf-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="d46bf-125">-Tag</span></span>
<span data-ttu-id="d46bf-126">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="d46bf-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="d46bf-127">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="d46bf-127">-VirtualHub</span></span>
<span data-ttu-id="d46bf-128">VirtualHub a cui deve essere associato questo P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="d46bf-128">The VirtualHub this P2SVpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="d46bf-129">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="d46bf-129">-VirtualHubId</span></span>
<span data-ttu-id="d46bf-130">ID dell'VirtualHub a cui deve essere associato questo P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="d46bf-130">The Id of the VirtualHub this P2SVpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="d46bf-131">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="d46bf-131">-VirtualHubName</span></span>
<span data-ttu-id="d46bf-132">ID dell'VirtualHub a cui deve essere associato questo P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="d46bf-132">The Id of the VirtualHub this P2SVpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="d46bf-133">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="d46bf-133">-VpnClientAddressPool</span></span>
<span data-ttu-id="d46bf-134">P2S VpnClient AddressPool per questo P2SVpnGateway P2SConnectionConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d46bf-134">P2S VpnClient AddressPool for this P2SVpnGateway P2SConnectionConfiguration.</span></span>

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

### <span data-ttu-id="d46bf-135">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="d46bf-135">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="d46bf-136">Unità di misura per questo P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="d46bf-136">The scale unit for this P2SVpnGateway.</span></span>

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

### <span data-ttu-id="d46bf-137">-VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="d46bf-137">-VpnServerConfiguration</span></span>
<span data-ttu-id="d46bf-138">VpnServerConfiguration da associare a questo P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="d46bf-138">The VpnServerConfiguration to be attached to this P2SVpnGateway.</span></span>

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

### <span data-ttu-id="d46bf-139">-VpnServerConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d46bf-139">-VpnServerConfigurationId</span></span>
<span data-ttu-id="d46bf-140">ID dell'oggetto di configurazione del server VPN a cui verrà associato questo P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="d46bf-140">The id of Vpn server configuration object this P2SVpnGateway will be attached to.</span></span>

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

### <span data-ttu-id="d46bf-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d46bf-141">-Confirm</span></span>
<span data-ttu-id="d46bf-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d46bf-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d46bf-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d46bf-143">-WhatIf</span></span>
<span data-ttu-id="d46bf-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d46bf-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d46bf-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d46bf-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d46bf-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d46bf-146">CommonParameters</span></span>
<span data-ttu-id="d46bf-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d46bf-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d46bf-148">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d46bf-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d46bf-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d46bf-149">INPUTS</span></span>

### <span data-ttu-id="d46bf-150">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="d46bf-150">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>
<span data-ttu-id="d46bf-151">System. String Microsoft. Azure. Commands. Network. Models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="d46bf-151">System.String Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="d46bf-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d46bf-152">OUTPUTS</span></span>

### <span data-ttu-id="d46bf-153">Microsoft. Azure. Commands. Network. Models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="d46bf-153">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="d46bf-154">Note</span><span class="sxs-lookup"><span data-stu-id="d46bf-154">NOTES</span></span>

## <span data-ttu-id="d46bf-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d46bf-155">RELATED LINKS</span></span>
