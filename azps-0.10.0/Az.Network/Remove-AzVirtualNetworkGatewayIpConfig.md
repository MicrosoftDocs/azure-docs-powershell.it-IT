---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 60DA2175-7970-410C-A13C-B1314716AD8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: b4503c94b750763fa7371f1c5297b0c181e32054
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862898"
---
# <span data-ttu-id="691a6-101">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="691a6-101">Remove-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="691a6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="691a6-102">SYNOPSIS</span></span>

## <span data-ttu-id="691a6-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="691a6-103">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="691a6-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="691a6-104">DESCRIPTION</span></span>

## <span data-ttu-id="691a6-105">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="691a6-105">EXAMPLES</span></span>

### <span data-ttu-id="691a6-106">1:</span><span class="sxs-lookup"><span data-stu-id="691a6-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="691a6-107">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="691a6-107">PARAMETERS</span></span>

### <span data-ttu-id="691a6-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="691a6-108">-DefaultProfile</span></span>
<span data-ttu-id="691a6-109">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="691a6-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="691a6-110">-Nome</span><span class="sxs-lookup"><span data-stu-id="691a6-110">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="691a6-111">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="691a6-111">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="691a6-112">-Confermare</span><span class="sxs-lookup"><span data-stu-id="691a6-112">-Confirm</span></span>
<span data-ttu-id="691a6-113">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="691a6-113">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="691a6-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="691a6-114">-WhatIf</span></span>
<span data-ttu-id="691a6-115">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="691a6-115">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="691a6-116">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="691a6-116">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="691a6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="691a6-117">CommonParameters</span></span>
<span data-ttu-id="691a6-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="691a6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="691a6-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="691a6-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="691a6-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="691a6-120">INPUTS</span></span>

### <span data-ttu-id="691a6-121">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="691a6-121">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="691a6-122">Il parametro ' VirtualNetworkGateway ' accetta il valore di tipo ' PSVirtualNetworkGateway ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="691a6-122">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="691a6-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="691a6-123">OUTPUTS</span></span>

### <span data-ttu-id="691a6-124">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="691a6-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="691a6-125">Note</span><span class="sxs-lookup"><span data-stu-id="691a6-125">NOTES</span></span>

## <span data-ttu-id="691a6-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="691a6-126">RELATED LINKS</span></span>

