---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLocalNetworkGateway.md
ms.openlocfilehash: 83289067bef9cf294477dca60a8b26a9b61dcb41
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864670"
---
# <span data-ttu-id="980a8-101">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="980a8-101">Get-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="980a8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="980a8-102">SYNOPSIS</span></span>
<span data-ttu-id="980a8-103">Ottiene un gateway di rete locale</span><span class="sxs-lookup"><span data-stu-id="980a8-103">Gets a Local Network Gateway</span></span>

## <span data-ttu-id="980a8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="980a8-104">SYNTAX</span></span>

```
Get-AzLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="980a8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="980a8-105">DESCRIPTION</span></span>
<span data-ttu-id="980a8-106">Il gateway di rete locale è l'oggetto che rappresenta il dispositivo VPN in locale.</span><span class="sxs-lookup"><span data-stu-id="980a8-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="980a8-107">Il cmdlet **Get-AzLocalNetworkGateway** restituisce l'oggetto che rappresenta il Gateway on-Prem in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="980a8-107">The **Get-AzLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="980a8-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="980a8-108">EXAMPLES</span></span>

### <span data-ttu-id="980a8-109">1: ottenere un gateway di rete locale</span><span class="sxs-lookup"><span data-stu-id="980a8-109">1: Get a Local Network Gateway</span></span>
```
Get-AzLocalNetworkGateway -Name myLocalGW1 -ResourceGroupName myRG

Name                     : myLocalGW1
ResourceGroupName        : myRG
Location                 : eastus
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                           icrosoft.Network/localNetworkGateways/myLocalGW1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : x.x.x.x
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null
```

<span data-ttu-id="980a8-110">Restituisce l'oggetto del gateway di rete locale con il nome "myLocalGW1" nel gruppo di risorse "myRG"</span><span class="sxs-lookup"><span data-stu-id="980a8-110">Returns the object of the Local Network Gateway with the name "myLocalGW1" within the resource group "myRG"</span></span>

### <span data-ttu-id="980a8-111">2: ottenere gateway di rete locali tramite filtro</span><span class="sxs-lookup"><span data-stu-id="980a8-111">2: Get Local Network Gateways using filtering</span></span>
```
Get-AzLocalNetworkGateway -Name myLocalGW* -ResourceGroupName myRG

Name                     : myLocalGW1
ResourceGroupName        : myRG
Location                 : eastus
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                           icrosoft.Network/localNetworkGateways/myLocalGW1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : x.x.x.x
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null

Name                     : myLocalGW2
ResourceGroupName        : myRG
Location                 : eastus
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                           icrosoft.Network/localNetworkGateways/myLocalGW2
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : x.x.x.x
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null
```

<span data-ttu-id="980a8-112">Restituisce l'oggetto del gateway di rete locale con il nome che inizia con "myLocalGW" nel gruppo di risorse "myRG"</span><span class="sxs-lookup"><span data-stu-id="980a8-112">Returns the object of the Local Network Gateway with name starting with "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="980a8-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="980a8-113">PARAMETERS</span></span>

### <span data-ttu-id="980a8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="980a8-114">-DefaultProfile</span></span>
<span data-ttu-id="980a8-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="980a8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="980a8-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="980a8-116">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="980a8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="980a8-117">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="980a8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="980a8-118">CommonParameters</span></span>
<span data-ttu-id="980a8-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="980a8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="980a8-120">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="980a8-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="980a8-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="980a8-121">INPUTS</span></span>

### <span data-ttu-id="980a8-122">System. String</span><span class="sxs-lookup"><span data-stu-id="980a8-122">System.String</span></span>

## <span data-ttu-id="980a8-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="980a8-123">OUTPUTS</span></span>

### <span data-ttu-id="980a8-124">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="980a8-124">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="980a8-125">Note</span><span class="sxs-lookup"><span data-stu-id="980a8-125">NOTES</span></span>

## <span data-ttu-id="980a8-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="980a8-126">RELATED LINKS</span></span>

[<span data-ttu-id="980a8-127">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="980a8-127">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="980a8-128">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="980a8-128">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)

[<span data-ttu-id="980a8-129">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="980a8-129">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
