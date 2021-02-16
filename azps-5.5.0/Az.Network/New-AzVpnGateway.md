---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGateway.md
ms.openlocfilehash: 75942fa57681b046028e196b0438d8633e1cd3df
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179559"
---
# <span data-ttu-id="7b9ab-101">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="7b9ab-101">New-AzVpnGateway</span></span>

## <span data-ttu-id="7b9ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b9ab-102">SYNOPSIS</span></span>
<span data-ttu-id="7b9ab-103">Crea un Gateway VPN scalabile.</span><span class="sxs-lookup"><span data-stu-id="7b9ab-103">Creates a Scalable VPN Gateway.</span></span>

## <span data-ttu-id="7b9ab-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7b9ab-104">SYNTAX</span></span>

### <span data-ttu-id="7b9ab-105">ByVirtualHubName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7b9ab-105">ByVirtualHubName (Default)</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> [-VpnConnection <PSVpnConnection[]>] [-EnableRoutingPreferenceInternetFlag] [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7b9ab-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="7b9ab-106">ByVirtualHubObject</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> [-VpnConnection <PSVpnConnection[]>] [-EnableRoutingPreferenceInternetFlag] [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7b9ab-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="7b9ab-107">ByVirtualHubResourceId</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> [-VpnConnection <PSVpnConnection[]>] [-EnableRoutingPreferenceInternetFlag] [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7b9ab-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7b9ab-108">DESCRIPTION</span></span>
<span data-ttu-id="7b9ab-109">New-AzVpnGateway crea un Gateway VPN scalabile.</span><span class="sxs-lookup"><span data-stu-id="7b9ab-109">New-AzVpnGateway creates a scalable VPN Gateway.</span></span>
<span data-ttu-id="7b9ab-110">Connettività definita dal software per le connessioni da sito a sito all'interno di VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="7b9ab-110">This is software defined connectivity for site to site connections inside the VirtualHub.</span></span>

<span data-ttu-id="7b9ab-111">Il gateway viene ridimensionato e ridimensionato in base all'unità di scala specificata in questo o nel cmdlet Set-AzVpnGateway gateway.</span><span class="sxs-lookup"><span data-stu-id="7b9ab-111">This gateway resizes and scales based on the scale unit specified in this or the Set-AzVpnGateway cmdlet.</span></span>

<span data-ttu-id="7b9ab-112">Viene impostata una connessione da un ramo/sito noto come VPNSite al gateway scalabile.</span><span class="sxs-lookup"><span data-stu-id="7b9ab-112">A connection is set up from a branch/Site known as VPNSite to the scalable gateway.</span></span>
<span data-ttu-id="7b9ab-113">Ogni connessione comprende 2 Active-Active tunnel.</span><span class="sxs-lookup"><span data-stu-id="7b9ab-113">Each connection comprises of 2 Active-Active tunnels.</span></span>

<span data-ttu-id="7b9ab-114">VpnGateway si posizionerà nella stessa posizione del VirtualHub a cui si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="7b9ab-114">The VpnGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="7b9ab-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7b9ab-115">EXAMPLES</span></span>

### <span data-ttu-id="7b9ab-116">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7b9ab-116">Example 1</span></span>
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

<span data-ttu-id="7b9ab-117">In questo modo verrà creato un gruppo di risorse, WAN virtuale, rete virtuale, hub virtuale negli Stati Uniti occidentali nel gruppo di risorse "testRG" in Azure.</span><span class="sxs-lookup"><span data-stu-id="7b9ab-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="7b9ab-118">Successivamente verrà creato un gateway VPN nell'hub virtuale con 2 unità di scala.</span><span class="sxs-lookup"><span data-stu-id="7b9ab-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="7b9ab-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7b9ab-119">PARAMETERS</span></span>

### <span data-ttu-id="7b9ab-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7b9ab-120">-AsJob</span></span>
<span data-ttu-id="7b9ab-121">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7b9ab-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7b9ab-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b9ab-122">-DefaultProfile</span></span>
<span data-ttu-id="7b9ab-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7b9ab-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b9ab-124">-Name</span><span class="sxs-lookup"><span data-stu-id="7b9ab-124">-Name</span></span>
<span data-ttu-id="7b9ab-125">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="7b9ab-125">The resource name.</span></span>

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

### <span data-ttu-id="7b9ab-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b9ab-126">-ResourceGroupName</span></span>
<span data-ttu-id="7b9ab-127">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="7b9ab-127">The resource name.</span></span>

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

### <span data-ttu-id="7b9ab-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="7b9ab-128">-Tag</span></span>
<span data-ttu-id="7b9ab-129">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="7b9ab-129">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="7b9ab-130">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="7b9ab-130">-VirtualHub</span></span>
<span data-ttu-id="7b9ab-131">VirtualHub a cui deve essere associato questo VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="7b9ab-131">The VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="7b9ab-132">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="7b9ab-132">-VirtualHubId</span></span>
<span data-ttu-id="7b9ab-133">ID di VirtualHub a cui deve essere associato questo VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="7b9ab-133">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="7b9ab-134">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="7b9ab-134">-VirtualHubName</span></span>
<span data-ttu-id="7b9ab-135">ID di VirtualHub a cui deve essere associato questo VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="7b9ab-135">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="7b9ab-136">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="7b9ab-136">-VpnConnection</span></span>
<span data-ttu-id="7b9ab-137">Elenco di VpnConnections necessario per questo VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="7b9ab-137">The list of VpnConnections that this VpnGateway needs to have.</span></span>

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

### <span data-ttu-id="7b9ab-138">-VpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="7b9ab-138">-VpnGatewayNatRule</span></span>
<span data-ttu-id="7b9ab-139">Elenco di VpnGatewayNatRules associati a questo VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="7b9ab-139">The list of VpnGatewayNatRules that are associated with this VpnGateway.</span></span>

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

### <span data-ttu-id="7b9ab-140">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="7b9ab-140">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="7b9ab-141">L'unità di scala per questo VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="7b9ab-141">The scale unit for this VpnGateway.</span></span>

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

### <span data-ttu-id="7b9ab-142">-EnableRoutingPreferenceInternetFlag</span><span class="sxs-lookup"><span data-stu-id="7b9ab-142">-EnableRoutingPreferenceInternetFlag</span></span>
<span data-ttu-id="7b9ab-143">Flag per abilitare la preferenza di routing Internet in questo VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="7b9ab-143">Flag to enable Routing Preference Internet on this VpnGateway.</span></span>

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

### <span data-ttu-id="7b9ab-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7b9ab-144">-Confirm</span></span>
<span data-ttu-id="7b9ab-145">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b9ab-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b9ab-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b9ab-146">-WhatIf</span></span>
<span data-ttu-id="7b9ab-147">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7b9ab-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b9ab-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7b9ab-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b9ab-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b9ab-149">CommonParameters</span></span>
<span data-ttu-id="7b9ab-150">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b9ab-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b9ab-151">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7b9ab-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b9ab-152">INPUT</span><span class="sxs-lookup"><span data-stu-id="7b9ab-152">INPUTS</span></span>

### <span data-ttu-id="7b9ab-153">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="7b9ab-153">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>
### <span data-ttu-id="7b9ab-154">System.String</span><span class="sxs-lookup"><span data-stu-id="7b9ab-154">System.String</span></span>
## <span data-ttu-id="7b9ab-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7b9ab-155">OUTPUTS</span></span>

### <span data-ttu-id="7b9ab-156">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="7b9ab-156">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>
## <span data-ttu-id="7b9ab-157">NOTE</span><span class="sxs-lookup"><span data-stu-id="7b9ab-157">NOTES</span></span>

## <span data-ttu-id="7b9ab-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7b9ab-158">RELATED LINKS</span></span>

[<span data-ttu-id="7b9ab-159">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="7b9ab-159">Get-AzVpnGateway</span></span>]()

[<span data-ttu-id="7b9ab-160">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="7b9ab-160">Remove-AzVpnGateway</span></span>]()

[<span data-ttu-id="7b9ab-161">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="7b9ab-161">Update-AzVpnGateway</span></span>]()

