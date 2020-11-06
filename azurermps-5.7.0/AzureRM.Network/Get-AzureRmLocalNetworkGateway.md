---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: ca23e58b173ee67917099f2743dac7dbd3d1bc4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521897"
---
# <span data-ttu-id="0353d-101">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0353d-101">Get-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="0353d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0353d-102">SYNOPSIS</span></span>
<span data-ttu-id="0353d-103">Ottiene un gateway di rete locale</span><span class="sxs-lookup"><span data-stu-id="0353d-103">Gets a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0353d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0353d-104">SYNTAX</span></span>

```
Get-AzureRmLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0353d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0353d-105">DESCRIPTION</span></span>
<span data-ttu-id="0353d-106">Il gateway di rete locale è l'oggetto che rappresenta il dispositivo VPN in locale.</span><span class="sxs-lookup"><span data-stu-id="0353d-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="0353d-107">Il cmdlet **Get-AzureRmLocalNetworkGateway** restituisce l'oggetto che rappresenta il Gateway on-Prem in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0353d-107">The **Get-AzureRmLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="0353d-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0353d-108">EXAMPLES</span></span>

### <span data-ttu-id="0353d-109">1: ottenere un gateway di rete locale</span><span class="sxs-lookup"><span data-stu-id="0353d-109">1: Get a Local Network Gateway</span></span>
```
Get-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="0353d-110">Restituisce l'oggetto del gateway di rete locale con il nome "myLocalGW" nel gruppo di risorse "myRG"</span><span class="sxs-lookup"><span data-stu-id="0353d-110">Returns the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="0353d-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0353d-111">PARAMETERS</span></span>

### <span data-ttu-id="0353d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0353d-112">-DefaultProfile</span></span>
<span data-ttu-id="0353d-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0353d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0353d-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="0353d-114">-Name</span></span>
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

### <span data-ttu-id="0353d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0353d-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="0353d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0353d-116">CommonParameters</span></span>
<span data-ttu-id="0353d-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0353d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0353d-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0353d-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0353d-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0353d-119">INPUTS</span></span>

### <span data-ttu-id="0353d-120">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0353d-120">None</span></span>
<span data-ttu-id="0353d-121">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="0353d-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0353d-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0353d-122">OUTPUTS</span></span>

### <span data-ttu-id="0353d-123">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0353d-123">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="0353d-124">Note</span><span class="sxs-lookup"><span data-stu-id="0353d-124">NOTES</span></span>

## <span data-ttu-id="0353d-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0353d-125">RELATED LINKS</span></span>

