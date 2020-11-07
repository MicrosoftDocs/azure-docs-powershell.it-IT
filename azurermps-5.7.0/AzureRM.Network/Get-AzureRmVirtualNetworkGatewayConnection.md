---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnection.md
ms.openlocfilehash: b4a6ae7db1221a2dee8a0bd5343ad78ed88a0abe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686194"
---
# <span data-ttu-id="42346-101">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="42346-101">Get-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="42346-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="42346-102">SYNOPSIS</span></span>
<span data-ttu-id="42346-103">Ottiene una connessione di gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="42346-103">Gets a Virtual Network Gateway Connection</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42346-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="42346-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42346-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="42346-105">DESCRIPTION</span></span>
<span data-ttu-id="42346-106">La connessione Virtual Network Gateway è l'oggetto che rappresenta il tunnel IPsec (da sito a sito o da VNET a VNET) connesso al gateway di rete virtuale in Azure.</span><span class="sxs-lookup"><span data-stu-id="42346-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="42346-107">Il cmdlet **Get-AzureRmVirtualNetworkGatewayConnection** restituisce l'oggetto della connessione in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="42346-107">The **Get-AzureRmVirtualNetworkGatewayConnection** cmdlet returns the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="42346-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="42346-108">EXAMPLES</span></span>

### <span data-ttu-id="42346-109">1: ottenere una connessione di gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="42346-109">1: Get a Virtual Network Gateway Connection</span></span>
```
Get-AzureRmVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="42346-110">Restituisce l'oggetto della connessione del gateway di rete virtuale con il nome "tunnel" nel gruppo di risorse "myRG"</span><span class="sxs-lookup"><span data-stu-id="42346-110">Returns the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="42346-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="42346-111">PARAMETERS</span></span>

### <span data-ttu-id="42346-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42346-112">-DefaultProfile</span></span>
<span data-ttu-id="42346-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="42346-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42346-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="42346-114">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42346-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42346-115">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42346-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42346-116">CommonParameters</span></span>
<span data-ttu-id="42346-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42346-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42346-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42346-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42346-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="42346-119">INPUTS</span></span>

### <span data-ttu-id="42346-120">Nessuno</span><span class="sxs-lookup"><span data-stu-id="42346-120">None</span></span>
<span data-ttu-id="42346-121">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="42346-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="42346-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="42346-122">OUTPUTS</span></span>

### <span data-ttu-id="42346-123">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="42346-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="42346-124">Note</span><span class="sxs-lookup"><span data-stu-id="42346-124">NOTES</span></span>

## <span data-ttu-id="42346-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="42346-125">RELATED LINKS</span></span>

