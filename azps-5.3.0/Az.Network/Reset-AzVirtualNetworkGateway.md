---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
ms.openlocfilehash: 15f918214a71fe38c850126b31f93d14940fa602
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475838"
---
# <span data-ttu-id="43c9c-101">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="43c9c-101">Reset-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="43c9c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="43c9c-102">SYNOPSIS</span></span>
<span data-ttu-id="43c9c-103">Reimposta il gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="43c9c-103">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="43c9c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="43c9c-104">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43c9c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43c9c-105">DESCRIPTION</span></span>
<span data-ttu-id="43c9c-106">Reimposta il gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="43c9c-106">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="43c9c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="43c9c-107">EXAMPLES</span></span>

### <span data-ttu-id="43c9c-108">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="43c9c-108">Example 1:</span></span>
```
$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway
```

## <span data-ttu-id="43c9c-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="43c9c-109">PARAMETERS</span></span>

### <span data-ttu-id="43c9c-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43c9c-110">-AsJob</span></span>
<span data-ttu-id="43c9c-111">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="43c9c-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="43c9c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43c9c-112">-DefaultProfile</span></span>
<span data-ttu-id="43c9c-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="43c9c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43c9c-114">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="43c9c-114">-GatewayVip</span></span>
<span data-ttu-id="43c9c-115">Il gateway VIP per reimpostare una particolare istanza del gateway, ad esempio nel caso dei gateway abilitati per la funzionalità Active-Active. Per impostazione predefinita, l'istanza primaria del gateway verrà reimpostata se non viene passato alcun valore.</span><span class="sxs-lookup"><span data-stu-id="43c9c-115">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

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

### <span data-ttu-id="43c9c-116">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="43c9c-116">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="43c9c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43c9c-117">CommonParameters</span></span>
<span data-ttu-id="43c9c-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43c9c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43c9c-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43c9c-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43c9c-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="43c9c-120">INPUTS</span></span>

### <span data-ttu-id="43c9c-121">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="43c9c-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="43c9c-122">System. String</span><span class="sxs-lookup"><span data-stu-id="43c9c-122">System.String</span></span>

## <span data-ttu-id="43c9c-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="43c9c-123">OUTPUTS</span></span>

### <span data-ttu-id="43c9c-124">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="43c9c-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="43c9c-125">Note</span><span class="sxs-lookup"><span data-stu-id="43c9c-125">NOTES</span></span>

## <span data-ttu-id="43c9c-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="43c9c-126">RELATED LINKS</span></span>

[<span data-ttu-id="43c9c-127">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="43c9c-127">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="43c9c-128">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="43c9c-128">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="43c9c-129">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="43c9c-129">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="43c9c-130">Ridimensionare-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="43c9c-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="43c9c-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="43c9c-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
