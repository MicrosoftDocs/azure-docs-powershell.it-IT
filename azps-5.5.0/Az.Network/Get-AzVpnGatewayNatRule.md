---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpngatewaynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnGatewayNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnGatewayNatRule.md
ms.openlocfilehash: 61dbb86c7eaa574abfcb3fad4bd37d6dbb242260
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189710"
---
# <span data-ttu-id="9235d-101">Get-AzVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="9235d-101">Get-AzVpnGatewayNatRule</span></span>

## <span data-ttu-id="9235d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9235d-102">SYNOPSIS</span></span>
<span data-ttu-id="9235d-103">Ottiene una regola NAT associata a VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="9235d-103">Gets a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="9235d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9235d-104">SYNTAX</span></span>

### <span data-ttu-id="9235d-105">ByVpnGatewayName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9235d-105">ByVpnGatewayName (Default)</span></span>
```
Get-AzVpnGatewayNatRule -ResourceGroupName <String> -ParentResourceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9235d-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="9235d-106">ByVpnGatewayObject</span></span>
```
Get-AzVpnGatewayNatRule -ParentObject <PSVpnGateway> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9235d-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="9235d-107">ByVpnGatewayResourceId</span></span>
```
Get-AzVpnGatewayNatRule -ParentResourceId <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9235d-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9235d-108">DESCRIPTION</span></span>
<span data-ttu-id="9235d-109">Ottiene una regola NAT associata a VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="9235d-109">Gets a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="9235d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9235d-110">EXAMPLES</span></span>

### <span data-ttu-id="9235d-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="9235d-111">Example</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> New-AzVpnGatewayNatRule -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testNatRule" -Type Static -Mode EgressSnat -InternalMapping "10.0.0.1/26" -ExternalMapping "192.168.0.0/26"
PS C:\> Get-AzVpnGatewayNatRule -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testNatRule"

Type                      : Static
Mode                      : EgressSnat
VpnConnectionProtocolType : IKEv2
InternalMappings          : 10.0.0.1/26
ExternalMappings          : 192.168.0.0/26
IpConfigurationId         :
IngressVpnSiteLinkConnections : [Microsoft.Azure.Commands.Network.Models.PSResourceId]
EgressVpnSiteLinkConnections  : [Microsoft.Azure.Commands.Network.Models.PSResourceId]
ProvisioningState         : Provisioned
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/vpnGateways/testvpngw/natRules/testNatRule

```

<span data-ttu-id="9235d-112">In questo modo verrà creato un gruppo di risorse, una WAN virtuale, una rete virtuale, un hub virtuale e vpngateway & una regola NAT associata a Vpngateway.</span><span class="sxs-lookup"><span data-stu-id="9235d-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and VpnGateway & a NAT rule associated with Vpngateway.</span></span>
<span data-ttu-id="9235d-113">La regola NAT viene quindi recuperata con il nome della regola NAT.</span><span class="sxs-lookup"><span data-stu-id="9235d-113">Then it gets the NAT rule using the NAT rule name.</span></span>

## <span data-ttu-id="9235d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9235d-114">PARAMETERS</span></span>

### <span data-ttu-id="9235d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9235d-115">-DefaultProfile</span></span>
<span data-ttu-id="9235d-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9235d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9235d-117">-Name</span><span class="sxs-lookup"><span data-stu-id="9235d-117">-Name</span></span>
<span data-ttu-id="9235d-118">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="9235d-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnGatewayNatRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9235d-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9235d-119">-ParentObject</span></span>
<span data-ttu-id="9235d-120">VpnGateway padre per questa VpnGatewayNatRule.</span><span class="sxs-lookup"><span data-stu-id="9235d-120">The parent VpnGateway for this VpnGatewayNatRule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: ParentVpnGateway, VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9235d-121">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="9235d-121">-ParentResourceId</span></span>
<span data-ttu-id="9235d-122">ID risorsa dell'elemento padre VpnGateway per questa VpnGatewayNatRule.</span><span class="sxs-lookup"><span data-stu-id="9235d-122">The resource id of the parent VpnGateway for this VpnGatewayNatRule.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: ParentVpnGatewayId, VpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9235d-123">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="9235d-123">-ParentResourceName</span></span>
<span data-ttu-id="9235d-124">Nome della risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="9235d-124">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9235d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9235d-125">-ResourceGroupName</span></span>
<span data-ttu-id="9235d-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9235d-126">The resource group name.</span></span>

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

### <span data-ttu-id="9235d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9235d-127">CommonParameters</span></span>
<span data-ttu-id="9235d-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9235d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9235d-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9235d-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9235d-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="9235d-130">INPUTS</span></span>

### <span data-ttu-id="9235d-131">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="9235d-131">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="9235d-132">System.String</span><span class="sxs-lookup"><span data-stu-id="9235d-132">System.String</span></span>

## <span data-ttu-id="9235d-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9235d-133">OUTPUTS</span></span>

### <span data-ttu-id="9235d-134">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="9235d-134">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span></span>

## <span data-ttu-id="9235d-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="9235d-135">NOTES</span></span>

## <span data-ttu-id="9235d-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9235d-136">RELATED LINKS</span></span>
