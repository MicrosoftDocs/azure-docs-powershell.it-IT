---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: 522516df5d4500f55a17e769140149f021501210
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688559"
---
# <span data-ttu-id="df82f-101">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="df82f-101">Get-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="df82f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="df82f-102">SYNOPSIS</span></span>
<span data-ttu-id="df82f-103">Ottiene un gateway di rete locale</span><span class="sxs-lookup"><span data-stu-id="df82f-103">Gets a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df82f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="df82f-104">SYNTAX</span></span>

```
Get-AzureRmLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df82f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="df82f-105">DESCRIPTION</span></span>
<span data-ttu-id="df82f-106">Il gateway di rete locale è l'oggetto che rappresenta il dispositivo VPN in locale.</span><span class="sxs-lookup"><span data-stu-id="df82f-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="df82f-107">Il cmdlet **Get-AzureRmLocalNetworkGateway** restituisce l'oggetto che rappresenta il Gateway on-Prem in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="df82f-107">The **Get-AzureRmLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="df82f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="df82f-108">EXAMPLES</span></span>

### <span data-ttu-id="df82f-109">1: ottenere un gateway di rete locale</span><span class="sxs-lookup"><span data-stu-id="df82f-109">1: Get a Local Network Gateway</span></span>
```
Get-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="df82f-110">Restituisce l'oggetto del gateway di rete locale con il nome "myLocalGW" nel gruppo di risorse "myRG"</span><span class="sxs-lookup"><span data-stu-id="df82f-110">Returns the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="df82f-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="df82f-111">PARAMETERS</span></span>

### <span data-ttu-id="df82f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df82f-112">-DefaultProfile</span></span>
<span data-ttu-id="df82f-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="df82f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df82f-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="df82f-114">-Name</span></span>
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

### <span data-ttu-id="df82f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df82f-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="df82f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df82f-116">CommonParameters</span></span>
<span data-ttu-id="df82f-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df82f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df82f-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df82f-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df82f-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="df82f-119">INPUTS</span></span>

### <span data-ttu-id="df82f-120">System. String</span><span class="sxs-lookup"><span data-stu-id="df82f-120">System.String</span></span>

## <span data-ttu-id="df82f-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="df82f-121">OUTPUTS</span></span>

### <span data-ttu-id="df82f-122">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="df82f-122">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="df82f-123">Note</span><span class="sxs-lookup"><span data-stu-id="df82f-123">NOTES</span></span>

## <span data-ttu-id="df82f-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="df82f-124">RELATED LINKS</span></span>
