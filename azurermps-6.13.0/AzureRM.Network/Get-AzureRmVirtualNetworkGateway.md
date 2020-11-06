---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: af925c1de08a5a615f5435bb20377582fedc0089
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93522032"
---
# <span data-ttu-id="3537e-101">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3537e-101">Get-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="3537e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3537e-102">SYNOPSIS</span></span>
<span data-ttu-id="3537e-103">Ottiene un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="3537e-103">Gets a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3537e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3537e-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3537e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3537e-105">DESCRIPTION</span></span>
<span data-ttu-id="3537e-106">Il gateway di rete virtuale è l'oggetto che rappresenta il gateway in Azure.</span><span class="sxs-lookup"><span data-stu-id="3537e-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="3537e-107">Il cmdlet **Get-AzureRmVirtualNetworkGateway** restituisce l'oggetto del gateway in Azure in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3537e-107">The **Get-AzureRmVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="3537e-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3537e-108">EXAMPLES</span></span>

### <span data-ttu-id="3537e-109">1: ottenere un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="3537e-109">1: Get a Virtual Network Gateway</span></span>
```
Get-AzureRmVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="3537e-110">Restituisce l'oggetto del gateway di rete virtuale con il nome "gateway" nel gruppo di risorse "myRG"</span><span class="sxs-lookup"><span data-stu-id="3537e-110">Returns the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="3537e-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3537e-111">PARAMETERS</span></span>

### <span data-ttu-id="3537e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3537e-112">-DefaultProfile</span></span>
<span data-ttu-id="3537e-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3537e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3537e-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="3537e-114">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3537e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3537e-115">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3537e-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3537e-116">CommonParameters</span></span>
<span data-ttu-id="3537e-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3537e-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3537e-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3537e-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3537e-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3537e-119">INPUTS</span></span>

### <span data-ttu-id="3537e-120">System. String</span><span class="sxs-lookup"><span data-stu-id="3537e-120">System.String</span></span>

## <span data-ttu-id="3537e-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3537e-121">OUTPUTS</span></span>

### <span data-ttu-id="3537e-122">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3537e-122">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="3537e-123">Note</span><span class="sxs-lookup"><span data-stu-id="3537e-123">NOTES</span></span>

## <span data-ttu-id="3537e-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3537e-124">RELATED LINKS</span></span>
