---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnGateway.md
ms.openlocfilehash: f1e7b829856558f438793a921154aa3f04666ff8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513715"
---
# <span data-ttu-id="4a552-101">Get-AzureRmVpnGateway</span><span class="sxs-lookup"><span data-stu-id="4a552-101">Get-AzureRmVpnGateway</span></span>

## <span data-ttu-id="4a552-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4a552-102">SYNOPSIS</span></span>
<span data-ttu-id="4a552-103">Ottiene una risorsa VpnGateway con ResourceGroupName e GatewayName o elenca tutti i gateway per ResourceGroupName o SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="4a552-103">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a552-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4a552-104">SYNTAX</span></span>

### <span data-ttu-id="4a552-105">ListBySubscriptionId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4a552-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzureRmVpnGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a552-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a552-106">ListByResourceGroupName</span></span>
```
Get-AzureRmVpnGateway -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4a552-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4a552-107">DESCRIPTION</span></span>
<span data-ttu-id="4a552-108">Ottiene una risorsa VpnGateway con ResourceGroupName e GatewayName o elenca tutti i gateway per ResourceGroupName o SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="4a552-108">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="4a552-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4a552-109">EXAMPLES</span></span>

### <span data-ttu-id="4a552-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4a552-110">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

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

<span data-ttu-id="4a552-111">Quanto sopra creerà un gruppo di risorse, una WAN virtuale, una rete virtuale, un hub virtuale in West US nel gruppo di risorse "testRG" in Azure.</span><span class="sxs-lookup"><span data-stu-id="4a552-111">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="4a552-112">Un gateway VPN verrà creato in seguito nell'hub virtuale con due unità di scala.</span><span class="sxs-lookup"><span data-stu-id="4a552-112">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="4a552-113">Ottiene quindi il VpnGateway usando il relativo resourceGroupName e il nome del gateway.</span><span class="sxs-lookup"><span data-stu-id="4a552-113">It then gets the VpnGateway using its resourceGroupName and the gateway name.</span></span>

## <span data-ttu-id="4a552-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4a552-114">PARAMETERS</span></span>

### <span data-ttu-id="4a552-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a552-115">-DefaultProfile</span></span>
<span data-ttu-id="4a552-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4a552-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a552-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="4a552-117">-Name</span></span>
<span data-ttu-id="4a552-118">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="4a552-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VpnGatewayName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a552-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a552-119">-ResourceGroupName</span></span>
<span data-ttu-id="4a552-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4a552-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a552-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a552-121">CommonParameters</span></span>
<span data-ttu-id="4a552-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a552-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a552-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a552-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a552-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4a552-124">INPUTS</span></span>

### <span data-ttu-id="4a552-125">System. String</span><span class="sxs-lookup"><span data-stu-id="4a552-125">System.String</span></span>

## <span data-ttu-id="4a552-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4a552-126">OUTPUTS</span></span>

### <span data-ttu-id="4a552-127">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="4a552-127">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="4a552-128">Note</span><span class="sxs-lookup"><span data-stu-id="4a552-128">NOTES</span></span>

## <span data-ttu-id="4a552-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4a552-129">RELATED LINKS</span></span>
