---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: c5d77619fa5f89c60ce20a097e096709e9a48bae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520905"
---
# <span data-ttu-id="f8c50-101">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f8c50-101">Reset-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="f8c50-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f8c50-102">SYNOPSIS</span></span>
<span data-ttu-id="f8c50-103">Reimposta il gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="f8c50-103">Resets the Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8c50-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f8c50-104">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8c50-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f8c50-105">DESCRIPTION</span></span>
<span data-ttu-id="f8c50-106">Reimposta il gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="f8c50-106">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="f8c50-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f8c50-107">EXAMPLES</span></span>

### <span data-ttu-id="f8c50-108">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="f8c50-108">Example 1:</span></span>
```
$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway
```

## <span data-ttu-id="f8c50-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f8c50-109">PARAMETERS</span></span>

### <span data-ttu-id="f8c50-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8c50-110">-AsJob</span></span>
<span data-ttu-id="f8c50-111">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f8c50-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f8c50-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8c50-112">-DefaultProfile</span></span>
<span data-ttu-id="f8c50-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f8c50-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8c50-114">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="f8c50-114">-GatewayVip</span></span>
<span data-ttu-id="f8c50-115">Il gateway VIP per reimpostare una particolare istanza del gateway, ad esempio nel caso dei gateway abilitati per la funzionalità Active-Active. Per impostazione predefinita, l'istanza primaria del gateway verrà reimpostata se non viene passato alcun valore.</span><span class="sxs-lookup"><span data-stu-id="f8c50-115">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

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

### <span data-ttu-id="f8c50-116">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f8c50-116">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="f8c50-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8c50-117">CommonParameters</span></span>
<span data-ttu-id="f8c50-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8c50-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8c50-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8c50-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8c50-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f8c50-120">INPUTS</span></span>

### <span data-ttu-id="f8c50-121">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f8c50-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="f8c50-122">Parametri: VirtualNetworkGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f8c50-122">Parameters: VirtualNetworkGateway (ByValue)</span></span>

### <span data-ttu-id="f8c50-123">System. String</span><span class="sxs-lookup"><span data-stu-id="f8c50-123">System.String</span></span>
<span data-ttu-id="f8c50-124">Parametri: GatewayVip (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f8c50-124">Parameters: GatewayVip (ByValue)</span></span>

## <span data-ttu-id="f8c50-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f8c50-125">OUTPUTS</span></span>

### <span data-ttu-id="f8c50-126">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f8c50-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="f8c50-127">Note</span><span class="sxs-lookup"><span data-stu-id="f8c50-127">NOTES</span></span>

## <span data-ttu-id="f8c50-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f8c50-128">RELATED LINKS</span></span>

[<span data-ttu-id="f8c50-129">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f8c50-129">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="f8c50-130">New-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f8c50-130">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="f8c50-131">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f8c50-131">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="f8c50-132">Ridimensionare-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f8c50-132">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="f8c50-133">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f8c50-133">Set-AzureRmVirtualNetworkGateway</span></span>](./Set-AzureRmVirtualNetworkGateway.md)


