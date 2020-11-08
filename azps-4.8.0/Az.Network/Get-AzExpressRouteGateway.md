---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteGateway.md
ms.openlocfilehash: 597b6fcff647b1b2032f0a1ac5d11961b9d1e959
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192112"
---
# <span data-ttu-id="4be23-101">Get-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="4be23-101">Get-AzExpressRouteGateway</span></span>

## <span data-ttu-id="4be23-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4be23-102">SYNOPSIS</span></span>
<span data-ttu-id="4be23-103">Ottiene una risorsa ExpressRouteGateway con ResourceGroupName e GatewayName o elenca tutti i gateway per ResourceGroupName o SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="4be23-103">Gets a ExpressRouteGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="4be23-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4be23-104">SYNTAX</span></span>

### <span data-ttu-id="4be23-105">ListBySubscriptionId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4be23-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzExpressRouteGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4be23-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4be23-106">ListByResourceGroupName</span></span>
```
Get-AzExpressRouteGateway [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4be23-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="4be23-107">ByExpressRouteGatewayResourceId</span></span>
```
Get-AzExpressRouteGateway -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4be23-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4be23-108">DESCRIPTION</span></span>
<span data-ttu-id="4be23-109">Ottiene una risorsa ExpressRouteGateway con ResourceGroupName e GatewayName o elenca tutti i gateway per ResourceGroupName o SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="4be23-109">Gets a ExpressRouteGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="4be23-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4be23-110">EXAMPLES</span></span>

### <span data-ttu-id="4be23-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4be23-111">Example 1</span></span>

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

<span data-ttu-id="4be23-112">Di cui sopra creeremo un gruppo di risorse, una rete virtuale WAN, Virtual Network, Virtual Hub in West Central US nel gruppo di risorse "testRG" in Azure.</span><span class="sxs-lookup"><span data-stu-id="4be23-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West Central US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="4be23-113">Un gateway ExpressRoute verrà creato in seguito nell'hub virtuale con due unità di scala.</span><span class="sxs-lookup"><span data-stu-id="4be23-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="4be23-114">Ottiene quindi il ExpressRouteGateway usando il relativo resourceGroupName e il nome del gateway.</span><span class="sxs-lookup"><span data-stu-id="4be23-114">It then gets the ExpressRouteGateway using its resourceGroupName and the gateway name.</span></span>

### <span data-ttu-id="4be23-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="4be23-115">Example 2</span></span>

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

<span data-ttu-id="4be23-116">Questo comando otterrà tutti i ExpressRouteGateways che iniziano con "test"</span><span class="sxs-lookup"><span data-stu-id="4be23-116">This command will get all ExpressRouteGateways that start with "test"</span></span>

## <span data-ttu-id="4be23-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4be23-117">PARAMETERS</span></span>

### <span data-ttu-id="4be23-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4be23-118">-DefaultProfile</span></span>
<span data-ttu-id="4be23-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4be23-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4be23-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="4be23-120">-Name</span></span>
<span data-ttu-id="4be23-121">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="4be23-121">The resource name.</span></span>

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

### <span data-ttu-id="4be23-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4be23-122">-ResourceGroupName</span></span>
<span data-ttu-id="4be23-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4be23-123">The resource group name.</span></span>

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

### <span data-ttu-id="4be23-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4be23-124">-ResourceId</span></span>
<span data-ttu-id="4be23-125">ID risorsa di Azure per l'expressRouteGateway da eliminare.</span><span class="sxs-lookup"><span data-stu-id="4be23-125">The Azure resource ID for the expressRouteGateway to be deleted.</span></span>

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

### <span data-ttu-id="4be23-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4be23-126">CommonParameters</span></span>
<span data-ttu-id="4be23-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4be23-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4be23-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4be23-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4be23-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4be23-129">INPUTS</span></span>

### <span data-ttu-id="4be23-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4be23-130">System.String</span></span>

## <span data-ttu-id="4be23-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4be23-131">OUTPUTS</span></span>

### <span data-ttu-id="4be23-132">Microsoft. Azure. Commands. Network. Models. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="4be23-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="4be23-133">Note</span><span class="sxs-lookup"><span data-stu-id="4be23-133">NOTES</span></span>

## <span data-ttu-id="4be23-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4be23-134">RELATED LINKS</span></span>