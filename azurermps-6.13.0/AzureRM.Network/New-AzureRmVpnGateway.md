---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnGateway.md
ms.openlocfilehash: b29b57ea7d7a5182a25cb05ae05e6d1644a5c18b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513668"
---
# <span data-ttu-id="d5010-101">New-AzureRmVpnGateway</span><span class="sxs-lookup"><span data-stu-id="d5010-101">New-AzureRmVpnGateway</span></span>

## <span data-ttu-id="d5010-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d5010-102">SYNOPSIS</span></span>
<span data-ttu-id="d5010-103">Crea un gateway VPN scalabile.</span><span class="sxs-lookup"><span data-stu-id="d5010-103">Creates a Scalable VPN Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5010-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d5010-104">SYNTAX</span></span>

### <span data-ttu-id="d5010-105">ByVirtualHubName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d5010-105">ByVirtualHubName (Default)</span></span>
```
New-AzureRmVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5010-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="d5010-106">ByVirtualHubObject</span></span>
```
New-AzureRmVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5010-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="d5010-107">ByVirtualHubResourceId</span></span>
```
New-AzureRmVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5010-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d5010-108">DESCRIPTION</span></span>

<span data-ttu-id="d5010-109">New-AzureRmVpnGateway crea un gateway VPN scalabile.</span><span class="sxs-lookup"><span data-stu-id="d5010-109">New-AzureRmVpnGateway creates a scalable VPN Gateway.</span></span> <span data-ttu-id="d5010-110">Questa è la connettività definita dal software per le connessioni al sito all'interno del VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="d5010-110">This is software defined connectivity for site to site connections inside the VirtualHub.</span></span> 

<span data-ttu-id="d5010-111">Questo gateway viene ridimensionato e ridimensionato in base all'unità di scala specificata in questo o nel cmdlet Set-AzureRmVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="d5010-111">This gateway resizes and scales based on the scale unit specified in this or the Set-AzureRmVpnGateway cmdlet.</span></span> 

<span data-ttu-id="d5010-112">Una connessione viene configurata da un ramo/sito noto come VPNSite al gateway scalabile.</span><span class="sxs-lookup"><span data-stu-id="d5010-112">A connection is set up from a branch/Site known as VPNSite to the scalable gateway.</span></span> <span data-ttu-id="d5010-113">Ogni connessione è costituita da due tunnel Active-Active.</span><span class="sxs-lookup"><span data-stu-id="d5010-113">Each connection comprises of 2 Active-Active tunnels.</span></span>

<span data-ttu-id="d5010-114">Il VpnGateway sarà nella stessa posizione della VirtualHub a cui si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="d5010-114">The VpnGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="d5010-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d5010-115">EXAMPLES</span></span>

### <span data-ttu-id="d5010-116">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d5010-116">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2

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

<span data-ttu-id="d5010-117">Quanto sopra creerà un gruppo di risorse, una WAN virtuale, una rete virtuale, un hub virtuale in West US nel gruppo di risorse "testRG" in Azure.</span><span class="sxs-lookup"><span data-stu-id="d5010-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="d5010-118">Un gateway VPN verrà creato in seguito nell'hub virtuale con due unità di scala.</span><span class="sxs-lookup"><span data-stu-id="d5010-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="d5010-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d5010-119">PARAMETERS</span></span>

### <span data-ttu-id="d5010-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d5010-120">-AsJob</span></span>
<span data-ttu-id="d5010-121">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d5010-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d5010-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5010-122">-DefaultProfile</span></span>
<span data-ttu-id="d5010-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d5010-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5010-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="d5010-124">-Name</span></span>
<span data-ttu-id="d5010-125">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="d5010-125">The resource name.</span></span>

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

### <span data-ttu-id="d5010-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5010-126">-ResourceGroupName</span></span>
<span data-ttu-id="d5010-127">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="d5010-127">The resource name.</span></span>

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

### <span data-ttu-id="d5010-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="d5010-128">-Tag</span></span>
<span data-ttu-id="d5010-129">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="d5010-129">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="d5010-130">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="d5010-130">-VirtualHub</span></span>
<span data-ttu-id="d5010-131">VirtualHub a cui deve essere associato questo VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="d5010-131">The VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="d5010-132">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="d5010-132">-VirtualHubId</span></span>
<span data-ttu-id="d5010-133">ID dell'VirtualHub a cui deve essere associato questo VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="d5010-133">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="d5010-134">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="d5010-134">-VirtualHubName</span></span>
<span data-ttu-id="d5010-135">ID dell'VirtualHub a cui deve essere associato questo VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="d5010-135">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="d5010-136">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="d5010-136">-VpnConnection</span></span>
<span data-ttu-id="d5010-137">L'elenco di VpnConnections che deve avere questo VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="d5010-137">The list of VpnConnections that this VpnGateway needs to have.</span></span>

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

### <span data-ttu-id="d5010-138">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="d5010-138">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="d5010-139">Unità di misura per questo VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="d5010-139">The scale unit for this VpnGateway.</span></span>

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

### <span data-ttu-id="d5010-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d5010-140">-Confirm</span></span>
<span data-ttu-id="d5010-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5010-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5010-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5010-142">-WhatIf</span></span>
<span data-ttu-id="d5010-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d5010-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5010-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d5010-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5010-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5010-145">CommonParameters</span></span>
<span data-ttu-id="d5010-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5010-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5010-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5010-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5010-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d5010-148">INPUTS</span></span>

### <span data-ttu-id="d5010-149">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="d5010-149">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="d5010-150">System. String</span><span class="sxs-lookup"><span data-stu-id="d5010-150">System.String</span></span>

## <span data-ttu-id="d5010-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d5010-151">OUTPUTS</span></span>

### <span data-ttu-id="d5010-152">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="d5010-152">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="d5010-153">Note</span><span class="sxs-lookup"><span data-stu-id="d5010-153">NOTES</span></span>

## <span data-ttu-id="d5010-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d5010-154">RELATED LINKS</span></span>
