---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGateway.md
ms.openlocfilehash: 541115347cfca85e0259e425912e83c4649e0952
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189022"
---
# <span data-ttu-id="87085-101">Get-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="87085-101">Get-AzP2sVpnGateway</span></span>

## <span data-ttu-id="87085-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="87085-102">SYNOPSIS</span></span>
<span data-ttu-id="87085-103">Ottiene un P2SVpnGateway esistente in VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="87085-103">Gets an existing P2SVpnGateway under VirtualHub.</span></span>

## <span data-ttu-id="87085-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="87085-104">SYNTAX</span></span>

### <span data-ttu-id="87085-105">ListBySubscriptionId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="87085-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzP2sVpnGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87085-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87085-106">ListByResourceGroupName</span></span>
```
Get-AzP2sVpnGateway [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="87085-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="87085-107">DESCRIPTION</span></span>
<span data-ttu-id="87085-108">Il cmdlet **Get-AzP2sVpnGateway** consente di ottenere un P2SVpnGateway esistente in VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="87085-108">The **Get-AzP2sVpnGateway** cmdlet enables you to get an existing P2SVpnGateway under VirtualHub.</span></span>

## <span data-ttu-id="87085-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="87085-109">EXAMPLES</span></span>

### <span data-ttu-id="87085-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="87085-110">Example 1</span></span>
```powershell
PS C:\> Get-AzP2sVpnGateway -ResourceGroupName P2SCortexGATesting -Name 683482ade8564515aed4b8448c9757ea-westus-gw

ResourceGroupName              : P2SCortexGATesting
Name                           : 683482ade8564515aed4b8448c9757ea-westus-gw
Id                             : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482ade8564515a
                                 ed4b8448c9757ea-westus-gw
Location                       : westus
VpnGatewayScaleUnit            : 1
VirtualHub                     : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub
VpnServerConfiguration         : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig
VpnServerConfigurationLocation :
VpnClientConnectionHealth      : null
Type                           : Microsoft.Network/p2sVpnGateways
ProvisioningState              : Succeeded
P2SConnectionConfigurations    : [
                                   {
                                     "ProvisioningState": "Succeeded",
                                     "VpnClientAddressPool": {
                                       "AddressPrefixes": [
                                         "192.168.2.0/24"
                                       ]
                                     },
                                     "RoutingConfiguration": {
                                       "AssociatedRouteTable": {
                                         "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub/hubRouteTables/defaultRouteTable"
                                       }
                                       "PropagatedRouteTables": {
                                         "Labels": [],
                                         "Ids": [
                                           {
                                            "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub/hubRouteTables/defaultRouteTable"
                                           }
                                        ]
                                       },
                                       "VnetRoutes": {
                                         "StaticRoutes": []
                                       }
                                     },
                                     "Name": "P2SConnectionConfigDefault",
                                     "Etag": "W/\"4b96e6a2-b4d8-46b3-9210-76d40f359bef\"",
                                     "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482
                                 ade8564515aed4b8448c9757ea-westus-gw/p2sConnectionConfigurations/P2SConnectionConfigDefault"
                                   }
                                 ]
```

<span data-ttu-id="87085-111">Il cmdlet **Get-AzP2sVpnGateway** consente di ottenere un P2SVpnGateway esistente in VirtualHub usato per la connettività punta a sito.</span><span class="sxs-lookup"><span data-stu-id="87085-111">The **Get-AzP2sVpnGateway** cmdlet enables you to get an existing P2SVpnGateway under VirtualHub that is used for Point to site connectivity.</span></span>

## <span data-ttu-id="87085-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="87085-112">PARAMETERS</span></span>

### <span data-ttu-id="87085-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87085-113">-DefaultProfile</span></span>
<span data-ttu-id="87085-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="87085-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87085-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="87085-115">-Name</span></span>
<span data-ttu-id="87085-116">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="87085-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, P2SVpnGatewayName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87085-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87085-117">-ResourceGroupName</span></span>
<span data-ttu-id="87085-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="87085-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87085-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87085-119">CommonParameters</span></span>
<span data-ttu-id="87085-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87085-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87085-121">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87085-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87085-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="87085-122">INPUTS</span></span>

### <span data-ttu-id="87085-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="87085-123">None</span></span>

## <span data-ttu-id="87085-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="87085-124">OUTPUTS</span></span>

### <span data-ttu-id="87085-125">Microsoft. Azure. Commands. Network. Models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="87085-125">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="87085-126">Note</span><span class="sxs-lookup"><span data-stu-id="87085-126">NOTES</span></span>

## <span data-ttu-id="87085-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="87085-127">RELATED LINKS</span></span>
