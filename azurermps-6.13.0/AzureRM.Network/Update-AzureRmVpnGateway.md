---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/update-azurermvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVpnGateway.md
ms.openlocfilehash: 00730f6e252373eebbbbc476fdd889b2eeb39e12
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686374"
---
# <span data-ttu-id="a226a-101">Update-AzureRmVpnGateway</span><span class="sxs-lookup"><span data-stu-id="a226a-101">Update-AzureRmVpnGateway</span></span>

## <span data-ttu-id="a226a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a226a-102">SYNOPSIS</span></span>
<span data-ttu-id="a226a-103">Update-AzureRmVpnGateway aggiorna un gateway VPN scalabile allo stato obiettivo appropriato.</span><span class="sxs-lookup"><span data-stu-id="a226a-103">Update-AzureRmVpnGateway updates a scalable VPN Gateway to the appropriate goal state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a226a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a226a-104">SYNTAX</span></span>

### <span data-ttu-id="a226a-105">ByVpnGatewayName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a226a-105">ByVpnGatewayName (Default)</span></span>
```
Update-AzureRmVpnGateway -ResourceGroupName <String> -Name <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a226a-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="a226a-106">ByVpnGatewayObject</span></span>
```
Update-AzureRmVpnGateway -InputObject <PSVpnGateway> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a226a-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="a226a-107">ByVpnGatewayResourceId</span></span>
```
Update-AzureRmVpnGateway -ResourceId <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a226a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a226a-108">DESCRIPTION</span></span>
<span data-ttu-id="a226a-109">Update-AzureRmVpnGateway aggiorna un gateway VPN scalabile allo stato obiettivo appropriato.</span><span class="sxs-lookup"><span data-stu-id="a226a-109">Update-AzureRmVpnGateway updates a scalable VPN Gateway to the appropriate goal state.</span></span> <span data-ttu-id="a226a-110">Un AzureRmVpnGateway è una connettività definita dal software per le connessioni sito a sito all'interno di VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="a226a-110">An AzureRmVpnGateway is a software defined connectivity for site to site connections inside the VirtualHub.</span></span> <span data-ttu-id="a226a-111">Questo gateway viene ridimensionato e ridimensionato in base all'unità di scala specificata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="a226a-111">This gateway resizes and scales based on the scale unit specified by the user.</span></span> <span data-ttu-id="a226a-112">Una connessione può essere configurata da un ramo/sito noto come VPNSite al gateway scalabile.</span><span class="sxs-lookup"><span data-stu-id="a226a-112">A connection can be set up from a branch/Site known as VPNSite to the scalable gateway.</span></span> <span data-ttu-id="a226a-113">Ogni connessione è costituita da due tunnel Active-Active</span><span class="sxs-lookup"><span data-stu-id="a226a-113">Each connection comprises of 2 Active-Active tunnels</span></span>

## <span data-ttu-id="a226a-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a226a-114">EXAMPLES</span></span>

### <span data-ttu-id="a226a-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a226a-115">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> $vpnGateway = New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Set-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VpnGatewayScaleUnit 3

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

<span data-ttu-id="a226a-116">Quanto sopra creerà un gruppo di risorse, una WAN virtuale, una rete virtuale, un hub virtuale in West US nel gruppo di risorse "testRG" in Azure.</span><span class="sxs-lookup"><span data-stu-id="a226a-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="a226a-117">Un gateway VPN verrà creato in seguito nell'hub virtuale con due unità di scala.</span><span class="sxs-lookup"><span data-stu-id="a226a-117">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="a226a-118">Dopo aver creato il gateway, USA Set-AzureRmVpnGateway per aggiornare il gateway a 3 unità di scala.</span><span class="sxs-lookup"><span data-stu-id="a226a-118">After the gateway has been created, it uses Set-AzureRmVpnGateway to upgrade the gateway to 3 scale units.</span></span>

## <span data-ttu-id="a226a-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a226a-119">PARAMETERS</span></span>

### <span data-ttu-id="a226a-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a226a-120">-AsJob</span></span>
<span data-ttu-id="a226a-121">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a226a-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a226a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a226a-122">-DefaultProfile</span></span>
<span data-ttu-id="a226a-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a226a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a226a-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a226a-124">-InputObject</span></span>
<span data-ttu-id="a226a-125">Oggetto gateway VPN da modificare</span><span class="sxs-lookup"><span data-stu-id="a226a-125">The vpn gateway object to be modified</span></span>

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

### <span data-ttu-id="a226a-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="a226a-126">-Name</span></span>
<span data-ttu-id="a226a-127">Nome della rete WAN virtuale.</span><span class="sxs-lookup"><span data-stu-id="a226a-127">The virtual wan name.</span></span>

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

### <span data-ttu-id="a226a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a226a-128">-ResourceGroupName</span></span>
<span data-ttu-id="a226a-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a226a-129">The resource group name.</span></span>

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

### <span data-ttu-id="a226a-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a226a-130">-ResourceId</span></span>
<span data-ttu-id="a226a-131">ID risorsa di Azure della VpnGateway da modificare.</span><span class="sxs-lookup"><span data-stu-id="a226a-131">The Azure resource ID of the VpnGateway to be modified.</span></span>

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

### <span data-ttu-id="a226a-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="a226a-132">-Tag</span></span>
<span data-ttu-id="a226a-133">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="a226a-133">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="a226a-134">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="a226a-134">-VpnConnection</span></span>
<span data-ttu-id="a226a-135">L'elenco di VpnConnections che deve avere questo VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="a226a-135">The list of VpnConnections that this VpnGateway needs to have.</span></span>

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

### <span data-ttu-id="a226a-136">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="a226a-136">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="a226a-137">Unità di misura per questo VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="a226a-137">The scale unit for this VpnGateway.</span></span>

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

### <span data-ttu-id="a226a-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a226a-138">-Confirm</span></span>
<span data-ttu-id="a226a-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a226a-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a226a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a226a-140">-WhatIf</span></span>
<span data-ttu-id="a226a-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a226a-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a226a-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a226a-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a226a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a226a-143">CommonParameters</span></span>
<span data-ttu-id="a226a-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a226a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a226a-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a226a-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a226a-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a226a-146">INPUTS</span></span>

### <span data-ttu-id="a226a-147">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="a226a-147">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="a226a-148">System. String</span><span class="sxs-lookup"><span data-stu-id="a226a-148">System.String</span></span>

## <span data-ttu-id="a226a-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a226a-149">OUTPUTS</span></span>

### <span data-ttu-id="a226a-150">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="a226a-150">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="a226a-151">Note</span><span class="sxs-lookup"><span data-stu-id="a226a-151">NOTES</span></span>

## <span data-ttu-id="a226a-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a226a-152">RELATED LINKS</span></span>
