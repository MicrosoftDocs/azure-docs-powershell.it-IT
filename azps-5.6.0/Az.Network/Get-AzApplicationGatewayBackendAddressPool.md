---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4B2066B6-51D7-46D8-8A72-1A232B3E6589
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 458788041ce833cacb30616a7aa8268ed485c65b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978318"
---
# <span data-ttu-id="8fb85-101">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8fb85-101">Get-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="8fb85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8fb85-102">SYNOPSIS</span></span>
<span data-ttu-id="8fb85-103">Ottiene un pool di indirizzi back-end per un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="8fb85-103">Gets a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="8fb85-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8fb85-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendAddressPool [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8fb85-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8fb85-105">DESCRIPTION</span></span>
<span data-ttu-id="8fb85-106">Il cmdlet **Get-AzApplicationGatewayBackendAddressPool** ottiene una o più configurazioni di pool di indirizzi back-end da un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="8fb85-106">The **Get-AzApplicationGatewayBackendAddressPool** cmdlet gets one or more backend address pool configurations from an application gateway.</span></span>

## <span data-ttu-id="8fb85-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8fb85-107">EXAMPLES</span></span>

### <span data-ttu-id="8fb85-108">Esempio 1: Ottenere un pool di server back-end specificato</span><span class="sxs-lookup"><span data-stu-id="8fb85-108">Example 1: Get a specified back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPool = Get-AzApplicationGatewayBackendAddressPool -Name "Pool01" -ApplicationGateway $AppGw
```

<span data-ttu-id="8fb85-109">Il primo comando recupera il gateway applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella $AppGw variabile.</span><span class="sxs-lookup"><span data-stu-id="8fb85-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="8fb85-110">Il secondo comando ottiene il pool di indirizzi back-end associato $AppGw denominato Pool01 e lo archivia nella variabile $BackendPool back-end.</span><span class="sxs-lookup"><span data-stu-id="8fb85-110">The second command gets the back-end address pool associated with $AppGw named Pool01 and stores it in the $BackendPool variable.</span></span>

### <span data-ttu-id="8fb85-111">Esempio 2: Ottenere un elenco di pool di server back-end</span><span class="sxs-lookup"><span data-stu-id="8fb85-111">Example 2: Get a list of back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPools = Get-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw
```

<span data-ttu-id="8fb85-112">Il primo comando recupera il gateway applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella $AppGw variabile.</span><span class="sxs-lookup"><span data-stu-id="8fb85-112">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="8fb85-113">Il secondo comando ottiene un elenco dei pool di indirizzi back-end associati a $AppGw e archivia l'elenco nella variabile $BackendPools back-end.</span><span class="sxs-lookup"><span data-stu-id="8fb85-113">The second command gets a list of the back-end address pools associated with $AppGw, and stores the list in the $BackendPools variable.</span></span>

## <span data-ttu-id="8fb85-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8fb85-114">PARAMETERS</span></span>

### <span data-ttu-id="8fb85-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8fb85-115">-ApplicationGateway</span></span>
<span data-ttu-id="8fb85-116">Il cmdlet **Get-AzApplicationGatewayBackendAddressPool** ottiene un pool di indirizzi back-end per un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="8fb85-116">The **Get-AzApplicationGatewayBackendAddressPool** cmdlet gets a back-end address pool for an application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8fb85-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fb85-117">-DefaultProfile</span></span>
<span data-ttu-id="8fb85-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8fb85-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8fb85-119">-Name</span><span class="sxs-lookup"><span data-stu-id="8fb85-119">-Name</span></span>
<span data-ttu-id="8fb85-120">Specifica il nome del pool di indirizzi back-end che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8fb85-120">Specifies the name of the back-end address pool that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fb85-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fb85-121">CommonParameters</span></span>
<span data-ttu-id="8fb85-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fb85-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fb85-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8fb85-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fb85-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="8fb85-124">INPUTS</span></span>

### <span data-ttu-id="8fb85-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8fb85-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8fb85-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8fb85-126">OUTPUTS</span></span>

### <span data-ttu-id="8fb85-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8fb85-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="8fb85-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="8fb85-128">NOTES</span></span>

## <span data-ttu-id="8fb85-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8fb85-129">RELATED LINKS</span></span>

[<span data-ttu-id="8fb85-130">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8fb85-130">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="8fb85-131">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8fb85-131">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="8fb85-132">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8fb85-132">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="8fb85-133">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8fb85-133">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


