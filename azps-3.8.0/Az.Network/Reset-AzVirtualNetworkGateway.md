---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
ms.openlocfilehash: 15f918214a71fe38c850126b31f93d14940fa602
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021893"
---
# <span data-ttu-id="823e9-101">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="823e9-101">Reset-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="823e9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="823e9-102">SYNOPSIS</span></span>
<span data-ttu-id="823e9-103">Reimposta il gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="823e9-103">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="823e9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="823e9-104">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="823e9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="823e9-105">DESCRIPTION</span></span>
<span data-ttu-id="823e9-106">Reimposta il gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="823e9-106">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="823e9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="823e9-107">EXAMPLES</span></span>

### <span data-ttu-id="823e9-108">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="823e9-108">Example 1:</span></span>
```
$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway
```

## <span data-ttu-id="823e9-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="823e9-109">PARAMETERS</span></span>

### <span data-ttu-id="823e9-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="823e9-110">-AsJob</span></span>
<span data-ttu-id="823e9-111">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="823e9-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="823e9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="823e9-112">-DefaultProfile</span></span>
<span data-ttu-id="823e9-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="823e9-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="823e9-114">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="823e9-114">-GatewayVip</span></span>
<span data-ttu-id="823e9-115">Il gateway VIP per reimpostare una particolare istanza del gateway, ad esempio nel caso dei gateway abilitati per la funzionalità Active-Active. Per impostazione predefinita, l'istanza primaria del gateway verrà reimpostata se non viene passato alcun valore.</span><span class="sxs-lookup"><span data-stu-id="823e9-115">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

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

### <span data-ttu-id="823e9-116">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="823e9-116">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="823e9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="823e9-117">CommonParameters</span></span>
<span data-ttu-id="823e9-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="823e9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="823e9-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="823e9-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="823e9-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="823e9-120">INPUTS</span></span>

### <span data-ttu-id="823e9-121">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="823e9-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="823e9-122">System. String</span><span class="sxs-lookup"><span data-stu-id="823e9-122">System.String</span></span>

## <span data-ttu-id="823e9-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="823e9-123">OUTPUTS</span></span>

### <span data-ttu-id="823e9-124">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="823e9-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="823e9-125">Note</span><span class="sxs-lookup"><span data-stu-id="823e9-125">NOTES</span></span>

## <span data-ttu-id="823e9-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="823e9-126">RELATED LINKS</span></span>

[<span data-ttu-id="823e9-127">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="823e9-127">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="823e9-128">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="823e9-128">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="823e9-129">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="823e9-129">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="823e9-130">Ridimensionare-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="823e9-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="823e9-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="823e9-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
