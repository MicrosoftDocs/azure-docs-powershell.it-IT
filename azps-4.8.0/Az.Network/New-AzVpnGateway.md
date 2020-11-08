---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGateway.md
ms.openlocfilehash: fa7374264e46e65dcddacb9f35e5822f18294147
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192072"
---
# <span data-ttu-id="bf84d-101">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="bf84d-101">New-AzVpnGateway</span></span>

## <span data-ttu-id="bf84d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bf84d-102">SYNOPSIS</span></span>
<span data-ttu-id="bf84d-103">Crea un gateway VPN scalabile.</span><span class="sxs-lookup"><span data-stu-id="bf84d-103">Creates a Scalable VPN Gateway.</span></span>

## <span data-ttu-id="bf84d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bf84d-104">SYNTAX</span></span>

### <span data-ttu-id="bf84d-105">ByVirtualHubName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bf84d-105">ByVirtualHubName (Default)</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf84d-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="bf84d-106">ByVirtualHubObject</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf84d-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="bf84d-107">ByVirtualHubResourceId</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf84d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf84d-108">DESCRIPTION</span></span>

<span data-ttu-id="bf84d-109">New-AzVpnGateway crea un gateway VPN scalabile.</span><span class="sxs-lookup"><span data-stu-id="bf84d-109">New-AzVpnGateway creates a scalable VPN Gateway.</span></span> <span data-ttu-id="bf84d-110">Questa è la connettività definita dal software per le connessioni al sito all'interno del VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="bf84d-110">This is software defined connectivity for site to site connections inside the VirtualHub.</span></span> 

<span data-ttu-id="bf84d-111">Questo gateway viene ridimensionato e ridimensionato in base all'unità di scala specificata in questo o nel cmdlet Set-AzVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="bf84d-111">This gateway resizes and scales based on the scale unit specified in this or the Set-AzVpnGateway cmdlet.</span></span> 

<span data-ttu-id="bf84d-112">Una connessione viene configurata da un ramo/sito noto come VPNSite al gateway scalabile.</span><span class="sxs-lookup"><span data-stu-id="bf84d-112">A connection is set up from a branch/Site known as VPNSite to the scalable gateway.</span></span> <span data-ttu-id="bf84d-113">Ogni connessione è costituita da due tunnel Active-Active.</span><span class="sxs-lookup"><span data-stu-id="bf84d-113">Each connection comprises of 2 Active-Active tunnels.</span></span>

<span data-ttu-id="bf84d-114">Il VpnGateway sarà nella stessa posizione della VirtualHub a cui si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="bf84d-114">The VpnGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="bf84d-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bf84d-115">EXAMPLES</span></span>

### <span data-ttu-id="bf84d-116">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bf84d-116">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2

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

<span data-ttu-id="bf84d-117">Quanto sopra creerà un gruppo di risorse, una WAN virtuale, una rete virtuale, un hub virtuale in West US nel gruppo di risorse "testRG" in Azure.</span><span class="sxs-lookup"><span data-stu-id="bf84d-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="bf84d-118">Un gateway VPN verrà creato in seguito nell'hub virtuale con due unità di scala.</span><span class="sxs-lookup"><span data-stu-id="bf84d-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="bf84d-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bf84d-119">PARAMETERS</span></span>

### <span data-ttu-id="bf84d-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bf84d-120">-AsJob</span></span>
<span data-ttu-id="bf84d-121">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="bf84d-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bf84d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf84d-122">-DefaultProfile</span></span>
<span data-ttu-id="bf84d-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bf84d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf84d-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="bf84d-124">-Name</span></span>
<span data-ttu-id="bf84d-125">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="bf84d-125">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf84d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf84d-126">-ResourceGroupName</span></span>
<span data-ttu-id="bf84d-127">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="bf84d-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf84d-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="bf84d-128">-Tag</span></span>
<span data-ttu-id="bf84d-129">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="bf84d-129">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="bf84d-130">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="bf84d-130">-VirtualHub</span></span>
<span data-ttu-id="bf84d-131">VirtualHub a cui deve essere associato questo VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="bf84d-131">The VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf84d-132">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="bf84d-132">-VirtualHubId</span></span>
<span data-ttu-id="bf84d-133">ID dell'VirtualHub a cui deve essere associato questo VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="bf84d-133">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf84d-134">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="bf84d-134">-VirtualHubName</span></span>
<span data-ttu-id="bf84d-135">ID dell'VirtualHub a cui deve essere associato questo VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="bf84d-135">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf84d-136">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="bf84d-136">-VpnConnection</span></span>
<span data-ttu-id="bf84d-137">L'elenco di VpnConnections che deve avere questo VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="bf84d-137">The list of VpnConnections that this VpnGateway needs to have.</span></span>

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

### <span data-ttu-id="bf84d-138">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="bf84d-138">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="bf84d-139">Unità di misura per questo VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="bf84d-139">The scale unit for this VpnGateway.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf84d-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bf84d-140">-Confirm</span></span>
<span data-ttu-id="bf84d-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf84d-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf84d-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf84d-142">-WhatIf</span></span>
<span data-ttu-id="bf84d-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bf84d-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf84d-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bf84d-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf84d-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf84d-145">CommonParameters</span></span>
<span data-ttu-id="bf84d-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf84d-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf84d-147">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf84d-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf84d-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bf84d-148">INPUTS</span></span>

### <span data-ttu-id="bf84d-149">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="bf84d-149">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="bf84d-150">System. String</span><span class="sxs-lookup"><span data-stu-id="bf84d-150">System.String</span></span>

## <span data-ttu-id="bf84d-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bf84d-151">OUTPUTS</span></span>

### <span data-ttu-id="bf84d-152">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="bf84d-152">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="bf84d-153">Note</span><span class="sxs-lookup"><span data-stu-id="bf84d-153">NOTES</span></span>

## <span data-ttu-id="bf84d-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bf84d-154">RELATED LINKS</span></span>

[<span data-ttu-id="bf84d-155">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="bf84d-155">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="bf84d-156">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="bf84d-156">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)

[<span data-ttu-id="bf84d-157">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="bf84d-157">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)