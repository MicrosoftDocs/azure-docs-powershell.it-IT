---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
ms.openlocfilehash: 419c7bc71def03bc2db004e378d80ea9c31f5183
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350692"
---
# <span data-ttu-id="9fd3c-101">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="9fd3c-101">Update-AzVpnGateway</span></span>

## <span data-ttu-id="9fd3c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9fd3c-102">SYNOPSIS</span></span>
<span data-ttu-id="9fd3c-103">Aggiorna un gateway VPN scalabile.</span><span class="sxs-lookup"><span data-stu-id="9fd3c-103">Updates a scalable VPN gateway.</span></span>

## <span data-ttu-id="9fd3c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9fd3c-104">SYNTAX</span></span>

### <span data-ttu-id="9fd3c-105">ByVpnGatewayName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9fd3c-105">ByVpnGatewayName (Default)</span></span>
```
Update-AzVpnGateway -ResourceGroupName <String> -Name <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fd3c-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="9fd3c-106">ByVpnGatewayObject</span></span>
```
Update-AzVpnGateway -InputObject <PSVpnGateway> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fd3c-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="9fd3c-107">ByVpnGatewayResourceId</span></span>
```
Update-AzVpnGateway -ResourceId <String> [-VpnConnection <PSVpnConnection[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fd3c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9fd3c-108">DESCRIPTION</span></span>
<span data-ttu-id="9fd3c-109">Il cmdlet **Update-AzVpnGateway** aggiorna un gateway VPN scalabile.</span><span class="sxs-lookup"><span data-stu-id="9fd3c-109">The **Update-AzVpnGateway** cmdlet updates a scalable VPN gateway.</span></span>  
<span data-ttu-id="9fd3c-110">Un gateway di Azure VPN è una connettività definita dal software per le connessioni sito-sito all'interno di VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="9fd3c-110">An Azure VPN gateway is a software defined connectivity for site to site connections inside the VirtualHub.</span></span> <span data-ttu-id="9fd3c-111">Questo gateway viene ridimensionato e ridimensionato in base all'unità di scala specificata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="9fd3c-111">This gateway resizes and scales based on the scale unit specified by the user.</span></span> <span data-ttu-id="9fd3c-112">Una connessione può essere configurata da un ramo/sito noto come sito VPN al gateway scalabile.</span><span class="sxs-lookup"><span data-stu-id="9fd3c-112">A connection can be set up from a branch/site known as VPN site to the scalable gateway.</span></span> <span data-ttu-id="9fd3c-113">Ogni connessione è costituita da due tunnel Active-Active</span><span class="sxs-lookup"><span data-stu-id="9fd3c-113">Each connection comprises of 2 Active-Active tunnels</span></span>

## <span data-ttu-id="9fd3c-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9fd3c-114">EXAMPLES</span></span>

### <span data-ttu-id="9fd3c-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9fd3c-115">Example 1</span></span>

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

<span data-ttu-id="9fd3c-116">Quanto sopra creerà un gruppo di risorse, una WAN virtuale, una rete virtuale, un hub virtuale in West US nel gruppo di risorse "testRG" in Azure.</span><span class="sxs-lookup"><span data-stu-id="9fd3c-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="9fd3c-117">Un gateway VPN verrà creato in seguito nell'hub virtuale con due unità di scala.</span><span class="sxs-lookup"><span data-stu-id="9fd3c-117">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="9fd3c-118">Dopo aver creato il gateway, USA Update-AzVpnGateway per aggiornare il gateway a 3 unità di scala.</span><span class="sxs-lookup"><span data-stu-id="9fd3c-118">After the gateway has been created, it uses  Update-AzVpnGateway to upgrade the gateway to 3 scale units.</span></span>

### <span data-ttu-id="9fd3c-119">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9fd3c-119">Example 2</span></span>

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

<span data-ttu-id="9fd3c-120">Quanto sopra creerà un gruppo di risorse, una WAN virtuale, una rete virtuale, un hub virtuale in West US nel gruppo di risorse "testRG" in Azure.</span><span class="sxs-lookup"><span data-stu-id="9fd3c-120">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="9fd3c-121">Un gateway VPN verrà creato in seguito nell'hub virtuale con due unità di scala.</span><span class="sxs-lookup"><span data-stu-id="9fd3c-121">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="9fd3c-122">Dopo aver creato il gateway, USA Set-AzVpnGateway per aggiornare BgpPeeringAddress.</span><span class="sxs-lookup"><span data-stu-id="9fd3c-122">After the gateway has been created, it uses Set-AzVpnGateway to update BgpPeeringAddress.</span></span>

## <span data-ttu-id="9fd3c-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9fd3c-123">PARAMETERS</span></span>

### <span data-ttu-id="9fd3c-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9fd3c-124">-AsJob</span></span>
<span data-ttu-id="9fd3c-125">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="9fd3c-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9fd3c-126">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="9fd3c-126">-BgpPeeringAddress</span></span>
<span data-ttu-id="9fd3c-127">Gli indirizzi di peering BGP per questo VpnGateway bgpsettings.</span><span class="sxs-lookup"><span data-stu-id="9fd3c-127">The BGP peering addresses for this VpnGateway bgpsettings.</span></span>

```yaml
Type: PSIpConfigurationBgpPeeringAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fd3c-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9fd3c-128">-Confirm</span></span>
<span data-ttu-id="9fd3c-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fd3c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fd3c-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fd3c-130">-DefaultProfile</span></span>
<span data-ttu-id="9fd3c-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9fd3c-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fd3c-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9fd3c-132">-InputObject</span></span>
<span data-ttu-id="9fd3c-133">Oggetto gateway VPN da modificare</span><span class="sxs-lookup"><span data-stu-id="9fd3c-133">The vpn gateway object to be modified</span></span>

```yaml
Type: PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9fd3c-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="9fd3c-134">-Name</span></span>
<span data-ttu-id="9fd3c-135">Nome del gateway VPN.</span><span class="sxs-lookup"><span data-stu-id="9fd3c-135">The vpn gateway name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fd3c-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fd3c-136">-ResourceGroupName</span></span>
<span data-ttu-id="9fd3c-137">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9fd3c-137">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fd3c-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9fd3c-138">-ResourceId</span></span>
<span data-ttu-id="9fd3c-139">ID risorsa di Azure della VpnGateway da modificare.</span><span class="sxs-lookup"><span data-stu-id="9fd3c-139">The Azure resource ID of the VpnGateway to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fd3c-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="9fd3c-140">-Tag</span></span>
<span data-ttu-id="9fd3c-141">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="9fd3c-141">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="9fd3c-142">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="9fd3c-142">-VpnConnection</span></span>
<span data-ttu-id="9fd3c-143">L'elenco di VpnConnections che deve avere questo VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="9fd3c-143">The list of VpnConnections that this VpnGateway needs to have.</span></span>

```yaml
Type: PSVpnConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fd3c-144">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="9fd3c-144">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="9fd3c-145">Unità di misura per questo VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="9fd3c-145">The scale unit for this VpnGateway.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fd3c-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fd3c-146">-WhatIf</span></span>
<span data-ttu-id="9fd3c-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9fd3c-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fd3c-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9fd3c-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fd3c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fd3c-149">CommonParameters</span></span>
<span data-ttu-id="9fd3c-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fd3c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fd3c-151">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9fd3c-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fd3c-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9fd3c-152">INPUTS</span></span>

### <span data-ttu-id="9fd3c-153">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="9fd3c-153">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="9fd3c-154">System. String</span><span class="sxs-lookup"><span data-stu-id="9fd3c-154">System.String</span></span>

## <span data-ttu-id="9fd3c-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9fd3c-155">OUTPUTS</span></span>

### <span data-ttu-id="9fd3c-156">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="9fd3c-156">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="9fd3c-157">Note</span><span class="sxs-lookup"><span data-stu-id="9fd3c-157">NOTES</span></span>

## <span data-ttu-id="9fd3c-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9fd3c-158">RELATED LINKS</span></span>
[<span data-ttu-id="9fd3c-159">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="9fd3c-159">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="9fd3c-160">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="9fd3c-160">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="9fd3c-161">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="9fd3c-161">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)