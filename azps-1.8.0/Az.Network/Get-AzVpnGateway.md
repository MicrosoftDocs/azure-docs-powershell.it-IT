---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnGateway.md
ms.openlocfilehash: fa91ce991a109c91b27560b0b969d1af0f4342d9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678403"
---
# <span data-ttu-id="70191-101">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="70191-101">Get-AzVpnGateway</span></span>

## <span data-ttu-id="70191-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="70191-102">SYNOPSIS</span></span>
<span data-ttu-id="70191-103">Ottiene una risorsa VpnGateway con ResourceGroupName e GatewayName o elenca tutti i gateway per ResourceGroupName o SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="70191-103">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="70191-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="70191-104">SYNTAX</span></span>

### <span data-ttu-id="70191-105">ListBySubscriptionId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="70191-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70191-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70191-106">ListByResourceGroupName</span></span>
```
Get-AzVpnGateway [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="70191-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="70191-107">DESCRIPTION</span></span>
<span data-ttu-id="70191-108">Ottiene una risorsa VpnGateway con ResourceGroupName e GatewayName o elenca tutti i gateway per ResourceGroupName o SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="70191-108">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="70191-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="70191-109">EXAMPLES</span></span>

### <span data-ttu-id="70191-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="70191-110">Example 1</span></span>

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
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="70191-111">Quanto sopra creerà un gruppo di risorse, una WAN virtuale, una rete virtuale, un hub virtuale in West US nel gruppo di risorse "testRG" in Azure.</span><span class="sxs-lookup"><span data-stu-id="70191-111">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="70191-112">Un gateway VPN verrà creato in seguito nell'hub virtuale con due unità di scala.</span><span class="sxs-lookup"><span data-stu-id="70191-112">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="70191-113">Ottiene quindi il VpnGateway usando il relativo resourceGroupName e il nome del gateway.</span><span class="sxs-lookup"><span data-stu-id="70191-113">It then gets the VpnGateway using its resourceGroupName and the gateway name.</span></span>

### <span data-ttu-id="70191-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="70191-114">Example 2</span></span>

```powershell
PS C:\> Get-AzVpnGateway -Name test*

ResourceGroupName   : testRG
Name                : test1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/test1
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded

ResourceGroupName   : testRG
Name                : test2
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/test2
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="70191-115">Questo cmdlet consente di ottenere tutti i gateway che iniziano con "test".</span><span class="sxs-lookup"><span data-stu-id="70191-115">This cmdlet gets all Gateways that start with "test".</span></span>

## <span data-ttu-id="70191-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="70191-116">PARAMETERS</span></span>

### <span data-ttu-id="70191-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70191-117">-DefaultProfile</span></span>
<span data-ttu-id="70191-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="70191-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70191-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="70191-119">-Name</span></span>
<span data-ttu-id="70191-120">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="70191-120">The resource name.</span></span>

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

### <span data-ttu-id="70191-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70191-121">-ResourceGroupName</span></span>
<span data-ttu-id="70191-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="70191-122">The resource group name.</span></span>

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

### <span data-ttu-id="70191-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70191-123">CommonParameters</span></span>
<span data-ttu-id="70191-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70191-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70191-125">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="70191-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70191-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="70191-126">INPUTS</span></span>

### <span data-ttu-id="70191-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="70191-127">None</span></span>

## <span data-ttu-id="70191-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="70191-128">OUTPUTS</span></span>

### <span data-ttu-id="70191-129">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="70191-129">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="70191-130">Note</span><span class="sxs-lookup"><span data-stu-id="70191-130">NOTES</span></span>

## <span data-ttu-id="70191-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="70191-131">RELATED LINKS</span></span>

[<span data-ttu-id="70191-132">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="70191-132">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="70191-133">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="70191-133">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)

[<span data-ttu-id="70191-134">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="70191-134">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
