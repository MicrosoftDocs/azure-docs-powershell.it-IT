---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnGateway.md
ms.openlocfilehash: b6537b9b8501aa2ec0aa76c9ede080893bf136ee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187095"
---
# <span data-ttu-id="f401f-101">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="f401f-101">Get-AzVpnGateway</span></span>

## <span data-ttu-id="f401f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f401f-102">SYNOPSIS</span></span>
<span data-ttu-id="f401f-103">Ottiene una risorsa VpnGateway usando ResourceGroupName e GatewayName OPPURE elenca tutti i gateway in base a ResourceGroupName o SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="f401f-103">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="f401f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f401f-104">SYNTAX</span></span>

### <span data-ttu-id="f401f-105">ListBySubscriptionId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f401f-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f401f-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f401f-106">ListByResourceGroupName</span></span>
```
Get-AzVpnGateway [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f401f-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f401f-107">DESCRIPTION</span></span>
<span data-ttu-id="f401f-108">Ottiene una risorsa VpnGateway usando ResourceGroupName e GatewayName OPPURE elenca tutti i gateway in base a ResourceGroupName o SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="f401f-108">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="f401f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f401f-109">EXAMPLES</span></span>

### <span data-ttu-id="f401f-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f401f-110">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
IpConfigurations    : {Instance0, Instance1}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="f401f-111">In questo modo verrà creato un gruppo di risorse, WAN virtuale, rete virtuale, hub virtuale negli Stati Uniti occidentali nel gruppo di risorse "testRG" in Azure.</span><span class="sxs-lookup"><span data-stu-id="f401f-111">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="f401f-112">Successivamente verrà creato un gateway VPN nell'hub virtuale con 2 unità di scala.</span><span class="sxs-lookup"><span data-stu-id="f401f-112">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="f401f-113">Ottiene quindi VpnGateway usando il nome resourceGroupName e il nome del gateway.</span><span class="sxs-lookup"><span data-stu-id="f401f-113">It then gets the VpnGateway using its resourceGroupName and the gateway name.</span></span>

### <span data-ttu-id="f401f-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f401f-114">Example 2</span></span>

```powershell
PS C:\> Get-AzVpnGateway -Name test*

ResourceGroupName   : testRG
Name                : test1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/test1
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
IpConfigurations    : {Instance0, Instance1}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded

ResourceGroupName   : testRG
Name                : test2
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/test2
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
IpConfigurations    : {Instance0, Instance1}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="f401f-115">Questo cmdlet ottiene tutti i gateway che iniziano con "test".</span><span class="sxs-lookup"><span data-stu-id="f401f-115">This cmdlet gets all Gateways that start with "test".</span></span>

## <span data-ttu-id="f401f-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f401f-116">PARAMETERS</span></span>

### <span data-ttu-id="f401f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f401f-117">-DefaultProfile</span></span>
<span data-ttu-id="f401f-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f401f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f401f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="f401f-119">-Name</span></span>
<span data-ttu-id="f401f-120">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="f401f-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VpnGatewayName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="f401f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f401f-121">-ResourceGroupName</span></span>
<span data-ttu-id="f401f-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f401f-122">The resource group name.</span></span>

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

### <span data-ttu-id="f401f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f401f-123">CommonParameters</span></span>
<span data-ttu-id="f401f-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f401f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f401f-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f401f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f401f-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="f401f-126">INPUTS</span></span>

### <span data-ttu-id="f401f-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f401f-127">None</span></span>

## <span data-ttu-id="f401f-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f401f-128">OUTPUTS</span></span>

### <span data-ttu-id="f401f-129">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="f401f-129">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="f401f-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="f401f-130">NOTES</span></span>

## <span data-ttu-id="f401f-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f401f-131">RELATED LINKS</span></span>

[<span data-ttu-id="f401f-132">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="f401f-132">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="f401f-133">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="f401f-133">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)

[<span data-ttu-id="f401f-134">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="f401f-134">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
