---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: e4b972944f757c9b0072f091dc820de5fa5d5b1c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964254"
---
# <span data-ttu-id="3552e-101">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3552e-101">Get-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="3552e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3552e-102">SYNOPSIS</span></span>
<span data-ttu-id="3552e-103">Ottiene una connessione gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="3552e-103">Gets a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="3552e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3552e-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3552e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3552e-105">DESCRIPTION</span></span>
<span data-ttu-id="3552e-106">La connessione a Gateway di rete virtuale è l'oggetto che rappresenta il tunnel IPsec (Site-to-Site o Vnet-to-Vnet) connesso al Gateway di rete virtuale in Azure.</span><span class="sxs-lookup"><span data-stu-id="3552e-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="3552e-107">Il cmdlet **Get-AzVirtualNetworkGatewayConnection** restituisce l'oggetto della connessione in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3552e-107">The **Get-AzVirtualNetworkGatewayConnection** cmdlet returns the object of your connection based on Name and Resource Group Name.</span></span>
<span data-ttu-id="3552e-108">Se il cmdlet **Get-AzVirtualNetworkGatewayConnection** viene generato senza specificare il parametro -Name, l'output non mostrerà i dettagli di ConnectionStatus e SharedKey.</span><span class="sxs-lookup"><span data-stu-id="3552e-108">If the **Get-AzVirtualNetworkGatewayConnection** cmdlet is issued without specifying the -Name parameter, the output will not show ConnectionStatus and SharedKey details.</span></span>

## <span data-ttu-id="3552e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3552e-109">EXAMPLES</span></span>

### <span data-ttu-id="3552e-110">1: Ottenere una connessione a un Gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="3552e-110">1: Get a Virtual Network Gateway Connection</span></span>
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="3552e-111">Restituisce l'oggetto della connessione a Gateway di rete virtuale con il nome "myTunnel" all'interno del gruppo di risorse "myRG"</span><span class="sxs-lookup"><span data-stu-id="3552e-111">Returns the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

### <span data-ttu-id="3552e-112">2: ottenere tutte le connessioni del Gateway di rete virtuale usando i filtri</span><span class="sxs-lookup"><span data-stu-id="3552e-112">2: Get all Virtual Network Gateway Connections using filtering</span></span>
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel* -ResourceGroupName myRG
```

<span data-ttu-id="3552e-113">Restituisce tutte le connessioni del Gateway di rete virtuale che iniziano con "myTunnel" all'interno del gruppo di risorse "myRG"</span><span class="sxs-lookup"><span data-stu-id="3552e-113">Returns all Virtual Network Gateway Connections that start with "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="3552e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3552e-114">PARAMETERS</span></span>

### <span data-ttu-id="3552e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3552e-115">-DefaultProfile</span></span>
<span data-ttu-id="3552e-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3552e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3552e-117">-Name</span><span class="sxs-lookup"><span data-stu-id="3552e-117">-Name</span></span>
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

### <span data-ttu-id="3552e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3552e-118">-ResourceGroupName</span></span>
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

### <span data-ttu-id="3552e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3552e-119">CommonParameters</span></span>
<span data-ttu-id="3552e-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3552e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3552e-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3552e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3552e-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="3552e-122">INPUTS</span></span>

### <span data-ttu-id="3552e-123">System.String</span><span class="sxs-lookup"><span data-stu-id="3552e-123">System.String</span></span>

## <span data-ttu-id="3552e-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3552e-124">OUTPUTS</span></span>

### <span data-ttu-id="3552e-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3552e-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="3552e-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="3552e-126">NOTES</span></span>

## <span data-ttu-id="3552e-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3552e-127">RELATED LINKS</span></span>

[<span data-ttu-id="3552e-128">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3552e-128">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="3552e-129">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3552e-129">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="3552e-130">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3552e-130">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
