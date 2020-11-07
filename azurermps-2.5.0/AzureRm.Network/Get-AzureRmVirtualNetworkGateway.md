---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgateway
schema: 2.0.0
ms.openlocfilehash: 1700ec112767397653201ff16608afbfb4af8f3e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866287"
---
# <span data-ttu-id="eb0bf-101">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="eb0bf-101">Get-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="eb0bf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eb0bf-102">SYNOPSIS</span></span>
<span data-ttu-id="eb0bf-103">Ottiene un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="eb0bf-103">Gets a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb0bf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eb0bf-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb0bf-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eb0bf-105">DESCRIPTION</span></span>
<span data-ttu-id="eb0bf-106">Il gateway di rete virtuale è l'oggetto che rappresenta il gateway in Azure.</span><span class="sxs-lookup"><span data-stu-id="eb0bf-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="eb0bf-107">Il cmdlet **Get-AzureRmVirtualNetworkGateway** restituisce l'oggetto del gateway in Azure in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="eb0bf-107">The **Get-AzureRmVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="eb0bf-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eb0bf-108">EXAMPLES</span></span>

### <span data-ttu-id="eb0bf-109">1: ottenere un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="eb0bf-109">1: Get a Virtual Network Gateway</span></span>
```
Get-AzureRmVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="eb0bf-110">Restituisce l'oggetto del gateway di rete virtuale con il nome "gateway" nel gruppo di risorse "myRG"</span><span class="sxs-lookup"><span data-stu-id="eb0bf-110">Returns the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="eb0bf-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eb0bf-111">PARAMETERS</span></span>

### <span data-ttu-id="eb0bf-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb0bf-112">-DefaultProfile</span></span>
<span data-ttu-id="eb0bf-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eb0bf-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb0bf-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="eb0bf-114">-Name</span></span>
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

### <span data-ttu-id="eb0bf-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb0bf-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="eb0bf-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb0bf-116">CommonParameters</span></span>
<span data-ttu-id="eb0bf-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb0bf-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb0bf-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb0bf-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb0bf-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eb0bf-119">INPUTS</span></span>

## <span data-ttu-id="eb0bf-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eb0bf-120">OUTPUTS</span></span>

### <span data-ttu-id="eb0bf-121">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="eb0bf-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="eb0bf-122">Note</span><span class="sxs-lookup"><span data-stu-id="eb0bf-122">NOTES</span></span>

## <span data-ttu-id="eb0bf-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eb0bf-123">RELATED LINKS</span></span>

