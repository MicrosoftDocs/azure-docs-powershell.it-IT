---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
ms.openlocfilehash: b38108a9655378349efff44bae3e51efc3ce1f7f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186799"
---
# <span data-ttu-id="c5ace-101">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="c5ace-101">Update-AzVpnGateway</span></span>

## <span data-ttu-id="c5ace-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5ace-102">SYNOPSIS</span></span>
<span data-ttu-id="c5ace-103">Aggiorna un gateway VPN scalabile.</span><span class="sxs-lookup"><span data-stu-id="c5ace-103">Updates a scalable VPN gateway.</span></span>

## <span data-ttu-id="c5ace-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c5ace-104">SYNTAX</span></span>

### <span data-ttu-id="c5ace-105">ByVpnGatewayName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c5ace-105">ByVpnGatewayName (Default)</span></span>
```
Update-AzVpnGateway -ResourceGroupName <String> -Name <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5ace-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="c5ace-106">ByVpnGatewayObject</span></span>
```
Update-AzVpnGateway -InputObject <PSVpnGateway> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5ace-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="c5ace-107">ByVpnGatewayResourceId</span></span>
```
Update-AzVpnGateway -ResourceId <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5ace-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c5ace-108">DESCRIPTION</span></span>
<span data-ttu-id="c5ace-109">Il cmdlet **Update-AzVpnGateway** aggiorna un gateway VPN scalabile.</span><span class="sxs-lookup"><span data-stu-id="c5ace-109">The **Update-AzVpnGateway** cmdlet updates a scalable VPN gateway.</span></span>  
<span data-ttu-id="c5ace-110">Un gateway VPN di Azure è una connettività definita dal software per le connessioni da sito a sito all'interno di VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="c5ace-110">An Azure VPN gateway is a software defined connectivity for site to site connections inside the VirtualHub.</span></span> <span data-ttu-id="c5ace-111">Il gateway viene ridimensionato e ridimensionato in base all'unità di scala specificata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="c5ace-111">This gateway resizes and scales based on the scale unit specified by the user.</span></span> <span data-ttu-id="c5ace-112">È possibile configurare una connessione da una succursale/un sito noto come sito VPN al gateway scalabile.</span><span class="sxs-lookup"><span data-stu-id="c5ace-112">A connection can be set up from a branch/site known as VPN site to the scalable gateway.</span></span> <span data-ttu-id="c5ace-113">Ogni connessione comprende 2 Active-Active tunnel</span><span class="sxs-lookup"><span data-stu-id="c5ace-113">Each connection comprises of 2 Active-Active tunnels</span></span>

## <span data-ttu-id="c5ace-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c5ace-114">EXAMPLES</span></span>

### <span data-ttu-id="c5ace-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c5ace-115">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> $vpnGateway = New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Update-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VpnGatewayScaleUnit 3

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 3
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="c5ace-116">In questo modo verrà creato un gruppo di risorse, WAN virtuale, rete virtuale, hub virtuale negli Stati Uniti occidentali nel gruppo di risorse "testRG" in Azure.</span><span class="sxs-lookup"><span data-stu-id="c5ace-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="c5ace-117">Successivamente verrà creato un gateway VPN nell'hub virtuale con 2 unità di scala.</span><span class="sxs-lookup"><span data-stu-id="c5ace-117">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="c5ace-118">Dopo la creazione, il gateway usa Update-AzVpnGateway per aggiornare il gateway a 3 unità di scala.</span><span class="sxs-lookup"><span data-stu-id="c5ace-118">After the gateway has been created, it uses  Update-AzVpnGateway to upgrade the gateway to 3 scale units.</span></span>

### <span data-ttu-id="c5ace-119">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c5ace-119">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> $vpnGateway = New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\>$ipconfigurationId1 = 'Instance0'
PS C:\>$addresslist1 = @('169.254.21.5')
PS C:\>$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1
PS C:\>$ipconfigurationId2 = 'Instance1'
PS C:\>$addresslist2 = @('169.254.21.10')
PS C:\>$gw1ipconfBgp2 = New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId $ipconfigurationId2 -CustomAddress $addresslist2
PS C:\>$gw = Get-AzVpnGateway -ResourceGroupName testRg -Name testgw
PS C:\> Update-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -BgpPeeringAddress @($gw1ipconfBgp1,$gw1ipconfBgp2)

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 3
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="c5ace-120">In questo modo verrà creato un gruppo di risorse, WAN virtuale, rete virtuale, hub virtuale negli Stati Uniti occidentali nel gruppo di risorse "testRG" in Azure.</span><span class="sxs-lookup"><span data-stu-id="c5ace-120">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="c5ace-121">Successivamente verrà creato un gateway VPN nell'hub virtuale con 2 unità di scala.</span><span class="sxs-lookup"><span data-stu-id="c5ace-121">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="c5ace-122">Dopo la creazione, il gateway usa Set-AzVpnGateway per aggiornare BgpAddress.</span><span class="sxs-lookup"><span data-stu-id="c5ace-122">After the gateway has been created, it uses Set-AzVpnGateway to update BgpPeeringAddress.</span></span>

## <span data-ttu-id="c5ace-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5ace-123">PARAMETERS</span></span>

### <span data-ttu-id="c5ace-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c5ace-124">-AsJob</span></span>
<span data-ttu-id="c5ace-125">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c5ace-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c5ace-126">-BgpAddressingAddress</span><span class="sxs-lookup"><span data-stu-id="c5ace-126">-BgpPeeringAddress</span></span>
<span data-ttu-id="c5ace-127">Indirizzi di peering BGP per questo bgpsettings VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="c5ace-127">The BGP peering addresses for this VpnGateway bgpsettings.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5ace-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5ace-128">-DefaultProfile</span></span>
<span data-ttu-id="c5ace-129">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c5ace-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5ace-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5ace-130">-InputObject</span></span>
<span data-ttu-id="c5ace-131">Oggetto gateway VPN da modificare</span><span class="sxs-lookup"><span data-stu-id="c5ace-131">The vpn gateway object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5ace-132">-Name</span><span class="sxs-lookup"><span data-stu-id="c5ace-132">-Name</span></span>
<span data-ttu-id="c5ace-133">Nome del gateway VPN.</span><span class="sxs-lookup"><span data-stu-id="c5ace-133">The vpn gateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5ace-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5ace-134">-ResourceGroupName</span></span>
<span data-ttu-id="c5ace-135">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c5ace-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5ace-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5ace-136">-ResourceId</span></span>
<span data-ttu-id="c5ace-137">ID della risorsa Azure di VpnGateway da modificare.</span><span class="sxs-lookup"><span data-stu-id="c5ace-137">The Azure resource ID of the VpnGateway to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5ace-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="c5ace-138">-Tag</span></span>
<span data-ttu-id="c5ace-139">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="c5ace-139">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5ace-140">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="c5ace-140">-VpnConnection</span></span>
<span data-ttu-id="c5ace-141">Elenco di VpnConnections necessario per questo VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="c5ace-141">The list of VpnConnections that this VpnGateway needs to have.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5ace-142">-VpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="c5ace-142">-VpnGatewayNatRule</span></span>
<span data-ttu-id="c5ace-143">Elenco di VpnGatewayNatRules associati a questo VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="c5ace-143">The list of VpnGatewayNatRules that are associated with this VpnGateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5ace-144">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="c5ace-144">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="c5ace-145">L'unità di scala per questo VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="c5ace-145">The scale unit for this VpnGateway.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5ace-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c5ace-146">-Confirm</span></span>
<span data-ttu-id="c5ace-147">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5ace-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5ace-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5ace-148">-WhatIf</span></span>
<span data-ttu-id="c5ace-149">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c5ace-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5ace-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c5ace-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5ace-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5ace-151">CommonParameters</span></span>
<span data-ttu-id="c5ace-152">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5ace-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5ace-153">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c5ace-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5ace-154">INPUT</span><span class="sxs-lookup"><span data-stu-id="c5ace-154">INPUTS</span></span>

### <span data-ttu-id="c5ace-155">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="c5ace-155">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="c5ace-156">System.String</span><span class="sxs-lookup"><span data-stu-id="c5ace-156">System.String</span></span>

## <span data-ttu-id="c5ace-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c5ace-157">OUTPUTS</span></span>

### <span data-ttu-id="c5ace-158">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="c5ace-158">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="c5ace-159">NOTE</span><span class="sxs-lookup"><span data-stu-id="c5ace-159">NOTES</span></span>

## <span data-ttu-id="c5ace-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c5ace-160">RELATED LINKS</span></span>

[<span data-ttu-id="c5ace-161">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="c5ace-161">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="c5ace-162">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="c5ace-162">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="c5ace-163">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="c5ace-163">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)