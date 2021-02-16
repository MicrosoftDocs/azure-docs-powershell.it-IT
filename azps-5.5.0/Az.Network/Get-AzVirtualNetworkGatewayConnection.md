---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: d3695216cdbda51ae3583218f7d0993894f472eb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191943"
---
# <span data-ttu-id="1b178-101">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="1b178-101">Get-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="1b178-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b178-102">SYNOPSIS</span></span>
<span data-ttu-id="1b178-103">Ottiene una connessione gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="1b178-103">Gets a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="1b178-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1b178-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b178-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1b178-105">DESCRIPTION</span></span>
<span data-ttu-id="1b178-106">La connessione al Gateway di rete virtuale è l'oggetto che rappresenta il tunnel IPsec (site-to-site o Vnet-to-Vnet) connesso al Gateway di rete virtuale in Azure.</span><span class="sxs-lookup"><span data-stu-id="1b178-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="1b178-107">Il cmdlet **Get-AzVirtualNetworkGatewayConnection** restituisce l'oggetto della connessione in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1b178-107">The **Get-AzVirtualNetworkGatewayConnection** cmdlet returns the object of your connection based on Name and Resource Group Name.</span></span>
<span data-ttu-id="1b178-108">Se il cmdlet **Get-AzVirtualNetworkGatewayConnection** viene generato senza specificare il parametro -Name, l'output non mostrerà i dettagli di ConnectionStatus e SharedKey.</span><span class="sxs-lookup"><span data-stu-id="1b178-108">If the **Get-AzVirtualNetworkGatewayConnection** cmdlet is issued without specifying the -Name parameter, the output will not show ConnectionStatus and SharedKey details.</span></span>

## <span data-ttu-id="1b178-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1b178-109">EXAMPLES</span></span>

### <span data-ttu-id="1b178-110">1: Ottenere una connessione a un Gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="1b178-110">1: Get a Virtual Network Gateway Connection</span></span>
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="1b178-111">Restituisce l'oggetto della connessione a Gateway di rete virtuale con il nome "myTunnel" all'interno del gruppo di risorse "myRG"</span><span class="sxs-lookup"><span data-stu-id="1b178-111">Returns the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

### <span data-ttu-id="1b178-112">2: ottenere tutte le connessioni del Gateway di rete virtuale usando i filtri</span><span class="sxs-lookup"><span data-stu-id="1b178-112">2: Get all Virtual Network Gateway Connections using filtering</span></span>
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel* -ResourceGroupName myRG
```

<span data-ttu-id="1b178-113">Restituisce tutte le connessioni a Gateway di rete virtuale che iniziano con "myTunnel" all'interno del gruppo di risorse "myRG"</span><span class="sxs-lookup"><span data-stu-id="1b178-113">Returns all Virtual Network Gateway Connections that start with "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="1b178-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b178-114">PARAMETERS</span></span>

### <span data-ttu-id="1b178-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b178-115">-DefaultProfile</span></span>
<span data-ttu-id="1b178-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1b178-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b178-117">-Name</span><span class="sxs-lookup"><span data-stu-id="1b178-117">-Name</span></span>
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

### <span data-ttu-id="1b178-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b178-118">-ResourceGroupName</span></span>
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

### <span data-ttu-id="1b178-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b178-119">CommonParameters</span></span>
<span data-ttu-id="1b178-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b178-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b178-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1b178-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b178-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="1b178-122">INPUTS</span></span>

### <span data-ttu-id="1b178-123">System.String</span><span class="sxs-lookup"><span data-stu-id="1b178-123">System.String</span></span>

## <span data-ttu-id="1b178-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1b178-124">OUTPUTS</span></span>

### <span data-ttu-id="1b178-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="1b178-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="1b178-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="1b178-126">NOTES</span></span>

## <span data-ttu-id="1b178-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1b178-127">RELATED LINKS</span></span>

[<span data-ttu-id="1b178-128">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="1b178-128">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="1b178-129">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="1b178-129">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="1b178-130">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="1b178-130">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
