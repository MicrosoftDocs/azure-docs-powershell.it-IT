---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteGateway.md
ms.openlocfilehash: 0d7bec7a40ced6ddcd5ffc61f48f233cea115459
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009469"
---
# <span data-ttu-id="4366d-101">Get-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="4366d-101">Get-AzExpressRouteGateway</span></span>

## <span data-ttu-id="4366d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4366d-102">SYNOPSIS</span></span>
<span data-ttu-id="4366d-103">Ottiene una risorsa ExpressRouteGateway usando ResourceGroupName e GatewayName OPPURE elenca tutti i gateway per ResourceGroupName o SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="4366d-103">Gets a ExpressRouteGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="4366d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4366d-104">SYNTAX</span></span>

### <span data-ttu-id="4366d-105">ListBySubscriptionId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4366d-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzExpressRouteGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4366d-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4366d-106">ListByResourceGroupName</span></span>
```
Get-AzExpressRouteGateway [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4366d-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="4366d-107">ByExpressRouteGatewayResourceId</span></span>
```
Get-AzExpressRouteGateway -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4366d-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4366d-108">DESCRIPTION</span></span>
<span data-ttu-id="4366d-109">Ottiene una risorsa ExpressRouteGateway usando ResourceGroupName e GatewayName OPPURE elenca tutti i gateway per ResourceGroupName o SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="4366d-109">Gets a ExpressRouteGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="4366d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4366d-110">EXAMPLES</span></span>

### <span data-ttu-id="4366d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4366d-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw"

ResourceGroupName   : testRG
Name                : testExpressRoutegw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw
Location            : West Central US
ExpressRouteGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/ExpressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="4366d-112">La procedura descritta sopra consente di creare un gruppo di risorse, WAN virtuale, rete virtuale, hub virtuale negli Stati Uniti centrali occidentali nel gruppo di risorse "testRG" in Azure.</span><span class="sxs-lookup"><span data-stu-id="4366d-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West Central US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="4366d-113">Successivamente verrà creato un gateway ExpressRoute nell'hub virtuale con 2 unità di scala.</span><span class="sxs-lookup"><span data-stu-id="4366d-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="4366d-114">Ottiene quindi ExpressRouteGateway usando il nome resourceGroupName e il nome del gateway.</span><span class="sxs-lookup"><span data-stu-id="4366d-114">It then gets the ExpressRouteGateway using its resourceGroupName and the gateway name.</span></span>

### <span data-ttu-id="4366d-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="4366d-115">Example 2</span></span>

```powershell
PS C:\> Get-AzExpressRouteGateway -Name test*

ResourceGroupName   : testRG
Name                : testExpressRoutegw1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw1
Location            : West Central US
ExpressRouteGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/ExpressRouteGateways
ProvisioningState   : Succeeded

ResourceGroupName   : testRG
Name                : testExpressRoutegw2
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw2
Location            : West Central US
ExpressRouteGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/ExpressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="4366d-116">Questo comando consente di ottenere tutti gli expressRouteGateway che iniziano con "test"</span><span class="sxs-lookup"><span data-stu-id="4366d-116">This command will get all ExpressRouteGateways that start with "test"</span></span>

## <span data-ttu-id="4366d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4366d-117">PARAMETERS</span></span>

### <span data-ttu-id="4366d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4366d-118">-DefaultProfile</span></span>
<span data-ttu-id="4366d-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4366d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4366d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4366d-120">-Name</span></span>
<span data-ttu-id="4366d-121">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="4366d-121">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, ExpressRouteGatewayName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="4366d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4366d-122">-ResourceGroupName</span></span>
<span data-ttu-id="4366d-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4366d-123">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="4366d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4366d-124">-ResourceId</span></span>
<span data-ttu-id="4366d-125">ID della risorsa Azure per expressRouteGateway da eliminare.</span><span class="sxs-lookup"><span data-stu-id="4366d-125">The Azure resource ID for the expressRouteGateway to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases: expressRouteGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4366d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4366d-126">CommonParameters</span></span>
<span data-ttu-id="4366d-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4366d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4366d-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4366d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4366d-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="4366d-129">INPUTS</span></span>

### <span data-ttu-id="4366d-130">System.String</span><span class="sxs-lookup"><span data-stu-id="4366d-130">System.String</span></span>

## <span data-ttu-id="4366d-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4366d-131">OUTPUTS</span></span>

### <span data-ttu-id="4366d-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="4366d-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="4366d-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="4366d-133">NOTES</span></span>

## <span data-ttu-id="4366d-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4366d-134">RELATED LINKS</span></span>
