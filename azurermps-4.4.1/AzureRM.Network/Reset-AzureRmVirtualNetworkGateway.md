---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 2b2947ec86e928506624aea49b380db3c4f24bc0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687729"
---
# <span data-ttu-id="470ba-101">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="470ba-101">Reset-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="470ba-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="470ba-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="470ba-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="470ba-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="470ba-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="470ba-104">DESCRIPTION</span></span>

## <span data-ttu-id="470ba-105">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="470ba-105">EXAMPLES</span></span>

## <span data-ttu-id="470ba-106">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="470ba-106">PARAMETERS</span></span>

### <span data-ttu-id="470ba-107">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="470ba-107">-GatewayVip</span></span>
<span data-ttu-id="470ba-108">Il gateway VIP per reimpostare una particolare istanza del gateway, ad esempio nel caso dei gateway abilitati per la funzionalità Active-Active. Per impostazione predefinita, l'istanza primaria del gateway verrà reimpostata se non viene passato alcun valore.</span><span class="sxs-lookup"><span data-stu-id="470ba-108">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="470ba-109">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="470ba-109">-VirtualNetworkGateway</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="470ba-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="470ba-110">-DefaultProfile</span></span>
<span data-ttu-id="470ba-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="470ba-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="470ba-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="470ba-112">CommonParameters</span></span>
<span data-ttu-id="470ba-113">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="470ba-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="470ba-114">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="470ba-114">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="470ba-115">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="470ba-115">INPUTS</span></span>

### <span data-ttu-id="470ba-116">Stringa</span><span class="sxs-lookup"><span data-stu-id="470ba-116">String</span></span>
<span data-ttu-id="470ba-117">Il parametro ' GatewayVip ' accetta il valore di tipo ' String ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="470ba-117">Parameter 'GatewayVip' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="470ba-118">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="470ba-118">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="470ba-119">Il parametro ' VirtualNetworkGateway ' accetta il valore di tipo ' PSVirtualNetworkGateway ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="470ba-119">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="470ba-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="470ba-120">OUTPUTS</span></span>

### <span data-ttu-id="470ba-121">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="470ba-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="470ba-122">Note</span><span class="sxs-lookup"><span data-stu-id="470ba-122">NOTES</span></span>

## <span data-ttu-id="470ba-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="470ba-123">RELATED LINKS</span></span>

[<span data-ttu-id="470ba-124">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="470ba-124">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="470ba-125">New-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="470ba-125">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="470ba-126">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="470ba-126">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="470ba-127">Ridimensionare-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="470ba-127">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="470ba-128">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="470ba-128">Set-AzureRmVirtualNetworkGateway</span></span>](./Set-AzureRmVirtualNetworkGateway.md)


