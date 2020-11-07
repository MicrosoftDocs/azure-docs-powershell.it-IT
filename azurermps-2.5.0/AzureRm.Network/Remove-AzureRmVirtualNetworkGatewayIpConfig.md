---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 60DA2175-7970-410C-A13C-B1314716AD8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
ms.openlocfilehash: f68709cad84adb6904e509472b1c960d6134144c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866035"
---
# <span data-ttu-id="1a77d-101">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="1a77d-101">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="1a77d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1a77d-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a77d-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1a77d-103">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a77d-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a77d-104">DESCRIPTION</span></span>

## <span data-ttu-id="1a77d-105">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1a77d-105">EXAMPLES</span></span>

### <span data-ttu-id="1a77d-106">1:</span><span class="sxs-lookup"><span data-stu-id="1a77d-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="1a77d-107">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1a77d-107">PARAMETERS</span></span>

### <span data-ttu-id="1a77d-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a77d-108">-DefaultProfile</span></span>
<span data-ttu-id="1a77d-109">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1a77d-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a77d-110">-Nome</span><span class="sxs-lookup"><span data-stu-id="1a77d-110">-Name</span></span>
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

### <span data-ttu-id="1a77d-111">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1a77d-111">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="1a77d-112">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1a77d-112">-Confirm</span></span>
<span data-ttu-id="1a77d-113">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a77d-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a77d-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a77d-114">-WhatIf</span></span>
<span data-ttu-id="1a77d-115">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1a77d-115">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a77d-116">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1a77d-116">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a77d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a77d-117">CommonParameters</span></span>
<span data-ttu-id="1a77d-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a77d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a77d-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a77d-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a77d-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1a77d-120">INPUTS</span></span>

### <span data-ttu-id="1a77d-121">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1a77d-121">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="1a77d-122">Il parametro ' VirtualNetworkGateway ' accetta il valore di tipo ' PSVirtualNetworkGateway ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="1a77d-122">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="1a77d-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1a77d-123">OUTPUTS</span></span>

### <span data-ttu-id="1a77d-124">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1a77d-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="1a77d-125">Note</span><span class="sxs-lookup"><span data-stu-id="1a77d-125">NOTES</span></span>

## <span data-ttu-id="1a77d-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1a77d-126">RELATED LINKS</span></span>

