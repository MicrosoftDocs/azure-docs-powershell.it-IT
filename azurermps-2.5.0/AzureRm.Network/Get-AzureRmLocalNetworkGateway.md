---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermlocalnetworkgateway
schema: 2.0.0
ms.openlocfilehash: 1a2a8aa8405be5dfc5275a07d253f06f1134e3e7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866491"
---
# <span data-ttu-id="8d143-101">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8d143-101">Get-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="8d143-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8d143-102">SYNOPSIS</span></span>
<span data-ttu-id="8d143-103">Ottiene un gateway di rete locale</span><span class="sxs-lookup"><span data-stu-id="8d143-103">Gets a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d143-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8d143-104">SYNTAX</span></span>

```
Get-AzureRmLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d143-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8d143-105">DESCRIPTION</span></span>
<span data-ttu-id="8d143-106">Il gateway di rete locale è l'oggetto che rappresenta il dispositivo VPN in locale.</span><span class="sxs-lookup"><span data-stu-id="8d143-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="8d143-107">Il cmdlet **Get-AzureRmLocalNetworkGateway** restituisce l'oggetto che rappresenta il Gateway on-Prem in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8d143-107">The **Get-AzureRmLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="8d143-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8d143-108">EXAMPLES</span></span>

### <span data-ttu-id="8d143-109">1: ottenere un gateway di rete locale</span><span class="sxs-lookup"><span data-stu-id="8d143-109">1: Get a Local Network Gateway</span></span>
```
Get-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="8d143-110">Restituisce l'oggetto del gateway di rete locale con il nome "myLocalGW" nel gruppo di risorse "myRG"</span><span class="sxs-lookup"><span data-stu-id="8d143-110">Returns the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="8d143-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8d143-111">PARAMETERS</span></span>

### <span data-ttu-id="8d143-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d143-112">-DefaultProfile</span></span>
<span data-ttu-id="8d143-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8d143-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d143-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="8d143-114">-Name</span></span>
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

### <span data-ttu-id="8d143-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d143-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="8d143-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d143-116">CommonParameters</span></span>
<span data-ttu-id="8d143-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d143-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d143-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d143-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d143-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8d143-119">INPUTS</span></span>

## <span data-ttu-id="8d143-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8d143-120">OUTPUTS</span></span>

### <span data-ttu-id="8d143-121">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8d143-121">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="8d143-122">Note</span><span class="sxs-lookup"><span data-stu-id="8d143-122">NOTES</span></span>

## <span data-ttu-id="8d143-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8d143-123">RELATED LINKS</span></span>

