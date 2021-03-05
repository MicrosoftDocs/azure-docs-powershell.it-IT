---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGateway.md
ms.openlocfilehash: 7e68e8e48ffa9d86222951b7ca2e076351872be6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984379"
---
# <span data-ttu-id="a2925-101">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="a2925-101">New-AzVpnGateway</span></span>

## <span data-ttu-id="a2925-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2925-102">SYNOPSIS</span></span>
<span data-ttu-id="a2925-103">Crea un Gateway VPN scalabile.</span><span class="sxs-lookup"><span data-stu-id="a2925-103">Creates a Scalable VPN Gateway.</span></span>

## <span data-ttu-id="a2925-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a2925-104">SYNTAX</span></span>

### <span data-ttu-id="a2925-105">ByVirtualHubName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a2925-105">ByVirtualHubName (Default)</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> [-VpnConnection <PSVpnConnection[]>] [-EnableRoutingPreferenceInternetFlag] [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a2925-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="a2925-106">ByVirtualHubObject</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> [-VpnConnection <PSVpnConnection[]>] [-EnableRoutingPreferenceInternetFlag] [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a2925-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="a2925-107">ByVirtualHubResourceId</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> [-VpnConnection <PSVpnConnection[]>] [-EnableRoutingPreferenceInternetFlag] [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a2925-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a2925-108">DESCRIPTION</span></span>
<span data-ttu-id="a2925-109">New-AzVpnGateway crea un Gateway VPN scalabile.</span><span class="sxs-lookup"><span data-stu-id="a2925-109">New-AzVpnGateway creates a scalable VPN Gateway.</span></span>
<span data-ttu-id="a2925-110">Connettività definita dal software per le connessioni da sito a sito all'interno di VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="a2925-110">This is software defined connectivity for site to site connections inside the VirtualHub.</span></span>

<span data-ttu-id="a2925-111">Il gateway viene ridimensionato e ridimensionato in base all'unità di scala specificata in questo o nel cmdlet Set-AzVpnGateway gateway.</span><span class="sxs-lookup"><span data-stu-id="a2925-111">This gateway resizes and scales based on the scale unit specified in this or the Set-AzVpnGateway cmdlet.</span></span>

<span data-ttu-id="a2925-112">Viene impostata una connessione da un ramo/sito noto come VPNSite al gateway scalabile.</span><span class="sxs-lookup"><span data-stu-id="a2925-112">A connection is set up from a branch/Site known as VPNSite to the scalable gateway.</span></span>
<span data-ttu-id="a2925-113">Ogni connessione comprende 2 Active-Active tunnel.</span><span class="sxs-lookup"><span data-stu-id="a2925-113">Each connection comprises of 2 Active-Active tunnels.</span></span>

<span data-ttu-id="a2925-114">VpnGateway si posizionerà nella stessa posizione del virtualhub a cui si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="a2925-114">The VpnGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="a2925-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a2925-115">EXAMPLES</span></span>

### <span data-ttu-id="a2925-116">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a2925-116">Example 1</span></span>
```
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2 -EnableRoutingPreferenceInternetFlag

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="a2925-117">La procedura precedente consente di creare un gruppo di risorse, WAN virtuale, rete virtuale, hub virtuale negli Stati Uniti occidentali nel gruppo di risorse "testRG" in Azure.</span><span class="sxs-lookup"><span data-stu-id="a2925-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="a2925-118">Successivamente verrà creato un gateway VPN nell'hub virtuale con 2 unità di scala.</span><span class="sxs-lookup"><span data-stu-id="a2925-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="a2925-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2925-119">PARAMETERS</span></span>

### <span data-ttu-id="a2925-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2925-120">-AsJob</span></span>
<span data-ttu-id="a2925-121">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a2925-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a2925-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2925-122">-DefaultProfile</span></span>
<span data-ttu-id="a2925-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a2925-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2925-124">-Name</span><span class="sxs-lookup"><span data-stu-id="a2925-124">-Name</span></span>
<span data-ttu-id="a2925-125">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="a2925-125">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2925-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2925-126">-ResourceGroupName</span></span>
<span data-ttu-id="a2925-127">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="a2925-127">The resource name.</span></span>

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

### <span data-ttu-id="a2925-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="a2925-128">-Tag</span></span>
<span data-ttu-id="a2925-129">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="a2925-129">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="a2925-130">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="a2925-130">-VirtualHub</span></span>
<span data-ttu-id="a2925-131">VirtualHub a cui deve essere associato questo VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="a2925-131">The VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2925-132">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="a2925-132">-VirtualHubId</span></span>
<span data-ttu-id="a2925-133">ID di VirtualHub a cui deve essere associato questo VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="a2925-133">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2925-134">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="a2925-134">-VirtualHubName</span></span>
<span data-ttu-id="a2925-135">ID di VirtualHub a cui deve essere associato questo VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="a2925-135">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2925-136">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="a2925-136">-VpnConnection</span></span>
<span data-ttu-id="a2925-137">Elenco di VpnConnections necessario per questo VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="a2925-137">The list of VpnConnections that this VpnGateway needs to have.</span></span>

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

### <span data-ttu-id="a2925-138">-VpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="a2925-138">-VpnGatewayNatRule</span></span>
<span data-ttu-id="a2925-139">Elenco di VpnGatewayNatRules associati a questo VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="a2925-139">The list of VpnGatewayNatRules that are associated with this VpnGateway.</span></span>

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

### <span data-ttu-id="a2925-140">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="a2925-140">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="a2925-141">L'unità di scala per questo VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="a2925-141">The scale unit for this VpnGateway.</span></span>

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

### <span data-ttu-id="a2925-142">-EnableRoutingPreferenceInternetFlag</span><span class="sxs-lookup"><span data-stu-id="a2925-142">-EnableRoutingPreferenceInternetFlag</span></span>
<span data-ttu-id="a2925-143">Flag per abilitare la preferenza di routing Internet in questo VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="a2925-143">Flag to enable Routing Preference Internet on this VpnGateway.</span></span>

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

### <span data-ttu-id="a2925-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a2925-144">-Confirm</span></span>
<span data-ttu-id="a2925-145">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2925-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2925-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2925-146">-WhatIf</span></span>
<span data-ttu-id="a2925-147">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a2925-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2925-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a2925-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2925-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2925-149">CommonParameters</span></span>
<span data-ttu-id="a2925-150">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2925-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2925-151">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a2925-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2925-152">INPUT</span><span class="sxs-lookup"><span data-stu-id="a2925-152">INPUTS</span></span>

### <span data-ttu-id="a2925-153">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a2925-153">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>
### <span data-ttu-id="a2925-154">System.String</span><span class="sxs-lookup"><span data-stu-id="a2925-154">System.String</span></span>
## <span data-ttu-id="a2925-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a2925-155">OUTPUTS</span></span>

### <span data-ttu-id="a2925-156">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="a2925-156">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>
## <span data-ttu-id="a2925-157">NOTE</span><span class="sxs-lookup"><span data-stu-id="a2925-157">NOTES</span></span>

## <span data-ttu-id="a2925-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a2925-158">RELATED LINKS</span></span>

[<span data-ttu-id="a2925-159">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="a2925-159">Get-AzVpnGateway</span></span>]()

[<span data-ttu-id="a2925-160">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="a2925-160">Remove-AzVpnGateway</span></span>]()

[<span data-ttu-id="a2925-161">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="a2925-161">Update-AzVpnGateway</span></span>]()

