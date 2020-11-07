---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
ms.openlocfilehash: 53a4eb40d82a721c93102067c8c7e9fe0cbd86be
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862882"
---
# <span data-ttu-id="e0adf-101">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e0adf-101">Reset-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="e0adf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e0adf-102">SYNOPSIS</span></span>

## <span data-ttu-id="e0adf-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e0adf-103">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0adf-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e0adf-104">DESCRIPTION</span></span>

## <span data-ttu-id="e0adf-105">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e0adf-105">EXAMPLES</span></span>

### <span data-ttu-id="e0adf-106">1:</span><span class="sxs-lookup"><span data-stu-id="e0adf-106">1:</span></span>
```

```

## <span data-ttu-id="e0adf-107">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e0adf-107">PARAMETERS</span></span>

### <span data-ttu-id="e0adf-108">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e0adf-108">-AsJob</span></span>
<span data-ttu-id="e0adf-109">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e0adf-109">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e0adf-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0adf-110">-DefaultProfile</span></span>
<span data-ttu-id="e0adf-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e0adf-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0adf-112">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="e0adf-112">-GatewayVip</span></span>
<span data-ttu-id="e0adf-113">Il gateway VIP per reimpostare una particolare istanza del gateway, ad esempio nel caso dei gateway abilitati per la funzionalità Active-Active. Per impostazione predefinita, l'istanza primaria del gateway verrà reimpostata se non viene passato alcun valore.</span><span class="sxs-lookup"><span data-stu-id="e0adf-113">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

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

### <span data-ttu-id="e0adf-114">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e0adf-114">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="e0adf-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0adf-115">CommonParameters</span></span>
<span data-ttu-id="e0adf-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0adf-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0adf-117">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0adf-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0adf-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e0adf-118">INPUTS</span></span>

### <span data-ttu-id="e0adf-119">Stringa</span><span class="sxs-lookup"><span data-stu-id="e0adf-119">String</span></span>
<span data-ttu-id="e0adf-120">Il parametro ' GatewayVip ' accetta il valore di tipo ' String ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="e0adf-120">Parameter 'GatewayVip' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="e0adf-121">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e0adf-121">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="e0adf-122">Il parametro ' VirtualNetworkGateway ' accetta il valore di tipo ' PSVirtualNetworkGateway ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="e0adf-122">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="e0adf-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e0adf-123">OUTPUTS</span></span>

### <span data-ttu-id="e0adf-124">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e0adf-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="e0adf-125">Note</span><span class="sxs-lookup"><span data-stu-id="e0adf-125">NOTES</span></span>

## <span data-ttu-id="e0adf-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e0adf-126">RELATED LINKS</span></span>

[<span data-ttu-id="e0adf-127">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e0adf-127">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="e0adf-128">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e0adf-128">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="e0adf-129">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e0adf-129">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="e0adf-130">Ridimensionare-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e0adf-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="e0adf-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e0adf-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)


