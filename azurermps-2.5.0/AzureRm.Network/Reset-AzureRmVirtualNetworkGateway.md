---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgateway
schema: 2.0.0
ms.openlocfilehash: f4039fb8a616a474a858728b6e222537c2d75c66
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866988"
---
# <span data-ttu-id="12495-101">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="12495-101">Reset-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="12495-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="12495-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12495-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="12495-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12495-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="12495-104">DESCRIPTION</span></span>

## <span data-ttu-id="12495-105">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="12495-105">EXAMPLES</span></span>

### <span data-ttu-id="12495-106">1:</span><span class="sxs-lookup"><span data-stu-id="12495-106">1:</span></span>
```

```

## <span data-ttu-id="12495-107">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="12495-107">PARAMETERS</span></span>

### <span data-ttu-id="12495-108">-AsJob</span><span class="sxs-lookup"><span data-stu-id="12495-108">-AsJob</span></span>
<span data-ttu-id="12495-109">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="12495-109">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12495-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12495-110">-DefaultProfile</span></span>
<span data-ttu-id="12495-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="12495-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12495-112">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="12495-112">-GatewayVip</span></span>
<span data-ttu-id="12495-113">Il gateway VIP per reimpostare una particolare istanza del gateway, ad esempio nel caso dei gateway abilitati per la funzionalità Active-Active. Per impostazione predefinita, l'istanza primaria del gateway verrà reimpostata se non viene passato alcun valore.</span><span class="sxs-lookup"><span data-stu-id="12495-113">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12495-114">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="12495-114">-VirtualNetworkGateway</span></span>
```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12495-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12495-115">CommonParameters</span></span>
<span data-ttu-id="12495-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12495-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12495-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12495-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12495-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="12495-118">INPUTS</span></span>

### <span data-ttu-id="12495-119">Stringa</span><span class="sxs-lookup"><span data-stu-id="12495-119">String</span></span>
<span data-ttu-id="12495-120">Il parametro ' GatewayVip ' accetta il valore di tipo ' String ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="12495-120">Parameter 'GatewayVip' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="12495-121">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="12495-121">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="12495-122">Il parametro ' VirtualNetworkGateway ' accetta il valore di tipo ' PSVirtualNetworkGateway ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="12495-122">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="12495-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="12495-123">OUTPUTS</span></span>

### <span data-ttu-id="12495-124">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="12495-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="12495-125">Note</span><span class="sxs-lookup"><span data-stu-id="12495-125">NOTES</span></span>

## <span data-ttu-id="12495-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="12495-126">RELATED LINKS</span></span>

[<span data-ttu-id="12495-127">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="12495-127">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="12495-128">New-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="12495-128">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="12495-129">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="12495-129">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="12495-130">Ridimensionare-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="12495-130">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="12495-131">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="12495-131">Set-AzureRmVirtualNetworkGateway</span></span>](./Set-AzureRmVirtualNetworkGateway.md)


