---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
ms.openlocfilehash: 306bd7262347219afac3ec94ad59dafef579ff94
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677879"
---
# <span data-ttu-id="346fa-101">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="346fa-101">Update-AzVpnGateway</span></span>

## <span data-ttu-id="346fa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="346fa-102">SYNOPSIS</span></span>
<span data-ttu-id="346fa-103">Aggiorna un gateway VPN scalabile.</span><span class="sxs-lookup"><span data-stu-id="346fa-103">Updates a scalable VPN gateway.</span></span>

## <span data-ttu-id="346fa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="346fa-104">SYNTAX</span></span>

### <span data-ttu-id="346fa-105">ByVpnGatewayName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="346fa-105">ByVpnGatewayName (Default)</span></span>
```
Update-AzVpnGateway -ResourceGroupName <String> -Name <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="346fa-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="346fa-106">ByVpnGatewayObject</span></span>
```
Update-AzVpnGateway -InputObject <PSVpnGateway> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="346fa-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="346fa-107">ByVpnGatewayResourceId</span></span>
```
Update-AzVpnGateway -ResourceId <String> [-VpnConnection <PSVpnConnection[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="346fa-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="346fa-108">DESCRIPTION</span></span>
<span data-ttu-id="346fa-109">Il cmdlet **Update-AzVpnGateway** aggiorna un gateway VPN scalabile.</span><span class="sxs-lookup"><span data-stu-id="346fa-109">The **Update-AzVpnGateway** cmdlet updates a scalable VPN gateway.</span></span>  
<span data-ttu-id="346fa-110">Un gateway di Azure VPN è una connettività definita dal software per le connessioni sito-sito all'interno di VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="346fa-110">An Azure VPN gateway is a software defined connectivity for site to site connections inside the VirtualHub.</span></span> <span data-ttu-id="346fa-111">Questo gateway viene ridimensionato e ridimensionato in base all'unità di scala specificata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="346fa-111">This gateway resizes and scales based on the scale unit specified by the user.</span></span> <span data-ttu-id="346fa-112">Una connessione può essere configurata da un ramo/sito noto come sito VPN al gateway scalabile.</span><span class="sxs-lookup"><span data-stu-id="346fa-112">A connection can be set up from a branch/site known as VPN site to the scalable gateway.</span></span> <span data-ttu-id="346fa-113">Ogni connessione è costituita da due tunnel Active-Active</span><span class="sxs-lookup"><span data-stu-id="346fa-113">Each connection comprises of 2 Active-Active tunnels</span></span>

## <span data-ttu-id="346fa-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="346fa-114">EXAMPLES</span></span>

### <span data-ttu-id="346fa-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="346fa-115">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> $vpnGateway = New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Set-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VpnGatewayScaleUnit 3

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

<span data-ttu-id="346fa-116">Quanto sopra creerà un gruppo di risorse, una WAN virtuale, una rete virtuale, un hub virtuale in West US nel gruppo di risorse "testRG" in Azure.</span><span class="sxs-lookup"><span data-stu-id="346fa-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="346fa-117">Un gateway VPN verrà creato in seguito nell'hub virtuale con due unità di scala.</span><span class="sxs-lookup"><span data-stu-id="346fa-117">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="346fa-118">Dopo aver creato il gateway, USA Set-AzVpnGateway per aggiornare il gateway a 3 unità di scala.</span><span class="sxs-lookup"><span data-stu-id="346fa-118">After the gateway has been created, it uses Set-AzVpnGateway to upgrade the gateway to 3 scale units.</span></span>

## <span data-ttu-id="346fa-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="346fa-119">PARAMETERS</span></span>

### <span data-ttu-id="346fa-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="346fa-120">-AsJob</span></span>
<span data-ttu-id="346fa-121">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="346fa-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="346fa-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="346fa-122">-DefaultProfile</span></span>
<span data-ttu-id="346fa-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="346fa-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="346fa-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="346fa-124">-InputObject</span></span>
<span data-ttu-id="346fa-125">Oggetto gateway VPN da modificare</span><span class="sxs-lookup"><span data-stu-id="346fa-125">The vpn gateway object to be modified</span></span>

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

### <span data-ttu-id="346fa-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="346fa-126">-Name</span></span>
<span data-ttu-id="346fa-127">Nome della rete WAN virtuale.</span><span class="sxs-lookup"><span data-stu-id="346fa-127">The virtual wan name.</span></span>

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

### <span data-ttu-id="346fa-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="346fa-128">-ResourceGroupName</span></span>
<span data-ttu-id="346fa-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="346fa-129">The resource group name.</span></span>

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

### <span data-ttu-id="346fa-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="346fa-130">-ResourceId</span></span>
<span data-ttu-id="346fa-131">ID risorsa di Azure della VpnGateway da modificare.</span><span class="sxs-lookup"><span data-stu-id="346fa-131">The Azure resource ID of the VpnGateway to be modified.</span></span>

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

### <span data-ttu-id="346fa-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="346fa-132">-Tag</span></span>
<span data-ttu-id="346fa-133">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="346fa-133">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="346fa-134">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="346fa-134">-VpnConnection</span></span>
<span data-ttu-id="346fa-135">L'elenco di VpnConnections che deve avere questo VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="346fa-135">The list of VpnConnections that this VpnGateway needs to have.</span></span>

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

### <span data-ttu-id="346fa-136">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="346fa-136">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="346fa-137">Unità di misura per questo VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="346fa-137">The scale unit for this VpnGateway.</span></span>

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

### <span data-ttu-id="346fa-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="346fa-138">-Confirm</span></span>
<span data-ttu-id="346fa-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="346fa-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="346fa-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="346fa-140">-WhatIf</span></span>
<span data-ttu-id="346fa-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="346fa-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="346fa-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="346fa-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="346fa-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="346fa-143">CommonParameters</span></span>
<span data-ttu-id="346fa-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="346fa-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="346fa-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="346fa-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="346fa-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="346fa-146">INPUTS</span></span>

### <span data-ttu-id="346fa-147">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="346fa-147">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="346fa-148">System. String</span><span class="sxs-lookup"><span data-stu-id="346fa-148">System.String</span></span>

## <span data-ttu-id="346fa-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="346fa-149">OUTPUTS</span></span>

### <span data-ttu-id="346fa-150">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="346fa-150">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="346fa-151">Note</span><span class="sxs-lookup"><span data-stu-id="346fa-151">NOTES</span></span>

## <span data-ttu-id="346fa-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="346fa-152">RELATED LINKS</span></span>

[<span data-ttu-id="346fa-153">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="346fa-153">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="346fa-154">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="346fa-154">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="346fa-155">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="346fa-155">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)
