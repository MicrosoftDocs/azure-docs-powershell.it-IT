---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: d3695216cdbda51ae3583218f7d0993894f472eb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348055"
---
# <span data-ttu-id="50c4b-101">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="50c4b-101">Get-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="50c4b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="50c4b-102">SYNOPSIS</span></span>
<span data-ttu-id="50c4b-103">Ottiene una connessione di gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="50c4b-103">Gets a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="50c4b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="50c4b-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50c4b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50c4b-105">DESCRIPTION</span></span>
<span data-ttu-id="50c4b-106">La connessione Virtual Network Gateway è l'oggetto che rappresenta il tunnel IPsec (da sito a sito o da VNET a VNET) connesso al gateway di rete virtuale in Azure.</span><span class="sxs-lookup"><span data-stu-id="50c4b-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="50c4b-107">Il cmdlet **Get-AzVirtualNetworkGatewayConnection** restituisce l'oggetto della connessione in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="50c4b-107">The **Get-AzVirtualNetworkGatewayConnection** cmdlet returns the object of your connection based on Name and Resource Group Name.</span></span>
<span data-ttu-id="50c4b-108">Se il cmdlet **Get-AzVirtualNetworkGatewayConnection** viene emesso senza specificare il parametro-Name, l'output non visualizzerà i dettagli di ConnectionStatus e SharedKey.</span><span class="sxs-lookup"><span data-stu-id="50c4b-108">If the **Get-AzVirtualNetworkGatewayConnection** cmdlet is issued without specifying the -Name parameter, the output will not show ConnectionStatus and SharedKey details.</span></span>

## <span data-ttu-id="50c4b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="50c4b-109">EXAMPLES</span></span>

### <span data-ttu-id="50c4b-110">1: ottenere una connessione di gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="50c4b-110">1: Get a Virtual Network Gateway Connection</span></span>
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="50c4b-111">Restituisce l'oggetto della connessione del gateway di rete virtuale con il nome "tunnel" nel gruppo di risorse "myRG"</span><span class="sxs-lookup"><span data-stu-id="50c4b-111">Returns the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

### <span data-ttu-id="50c4b-112">2: ottenere tutte le connessioni di Virtual Network Gateway tramite filtro</span><span class="sxs-lookup"><span data-stu-id="50c4b-112">2: Get all Virtual Network Gateway Connections using filtering</span></span>
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel* -ResourceGroupName myRG
```

<span data-ttu-id="50c4b-113">Restituisce tutte le connessioni di Virtual Network Gateway che iniziano con "tunnel" nel gruppo di risorse "myRG"</span><span class="sxs-lookup"><span data-stu-id="50c4b-113">Returns all Virtual Network Gateway Connections that start with "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="50c4b-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="50c4b-114">PARAMETERS</span></span>

### <span data-ttu-id="50c4b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50c4b-115">-DefaultProfile</span></span>
<span data-ttu-id="50c4b-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="50c4b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50c4b-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="50c4b-117">-Name</span></span>
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

### <span data-ttu-id="50c4b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50c4b-118">-ResourceGroupName</span></span>
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

### <span data-ttu-id="50c4b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50c4b-119">CommonParameters</span></span>
<span data-ttu-id="50c4b-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50c4b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50c4b-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="50c4b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50c4b-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="50c4b-122">INPUTS</span></span>

### <span data-ttu-id="50c4b-123">System. String</span><span class="sxs-lookup"><span data-stu-id="50c4b-123">System.String</span></span>

## <span data-ttu-id="50c4b-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="50c4b-124">OUTPUTS</span></span>

### <span data-ttu-id="50c4b-125">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="50c4b-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="50c4b-126">Note</span><span class="sxs-lookup"><span data-stu-id="50c4b-126">NOTES</span></span>

## <span data-ttu-id="50c4b-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="50c4b-127">RELATED LINKS</span></span>

[<span data-ttu-id="50c4b-128">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="50c4b-128">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="50c4b-129">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="50c4b-129">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="50c4b-130">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="50c4b-130">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
