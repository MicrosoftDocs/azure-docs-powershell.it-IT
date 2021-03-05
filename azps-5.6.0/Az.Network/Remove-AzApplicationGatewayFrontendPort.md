---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A698954A-994E-45AD-BA36-1E03196CFCB0
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 4b28feb85ebc8f4d5669f28609aa4723061c1709
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992528"
---
# <span data-ttu-id="ec991-101">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="ec991-101">Remove-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="ec991-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec991-102">SYNOPSIS</span></span>
<span data-ttu-id="ec991-103">Rimuove una porta front-end da un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="ec991-103">Removes a front-end port from an application gateway.</span></span>

## <span data-ttu-id="ec991-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ec991-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendPort -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec991-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ec991-105">DESCRIPTION</span></span>
<span data-ttu-id="ec991-106">Il cmdlet **Remove-AzApplicationGatewayFrontendPort** rimuove una porta front-end da un gateway applicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="ec991-106">The **Remove-AzApplicationGatewayFrontendPort** cmdlet removes a front-end port from an Azure application gateway.</span></span>

## <span data-ttu-id="ec991-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ec991-107">EXAMPLES</span></span>

### <span data-ttu-id="ec991-108">Esempio: Rimuovere una porta front-end da un gateway applicazioni</span><span class="sxs-lookup"><span data-stu-id="ec991-108">Example: Remove a front-end port from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort02"
```

<span data-ttu-id="ec991-109">Il primo comando ottiene un gateway applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e archivia il gateway in $AppGw variabile.</span><span class="sxs-lookup"><span data-stu-id="ec991-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores the gateway in $AppGw variable.</span></span>
<span data-ttu-id="ec991-110">Il secondo comando rimuove la porta denominata FrontEndPort02 dal gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="ec991-110">The second command removes the port named FrontEndPort02 from the application gateway.</span></span>

## <span data-ttu-id="ec991-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec991-111">PARAMETERS</span></span>

### <span data-ttu-id="ec991-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ec991-112">-ApplicationGateway</span></span>
<span data-ttu-id="ec991-113">Specifica il gateway applicazione da cui rimuovere una porta front-end.</span><span class="sxs-lookup"><span data-stu-id="ec991-113">Specifies the application gateway from which to remove a front-end port.</span></span>

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

### <span data-ttu-id="ec991-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec991-114">-DefaultProfile</span></span>
<span data-ttu-id="ec991-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ec991-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec991-116">-Name</span><span class="sxs-lookup"><span data-stu-id="ec991-116">-Name</span></span>
<span data-ttu-id="ec991-117">Specifica il nome della porta frontend da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="ec991-117">Specifies name of the frontend port to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec991-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec991-118">CommonParameters</span></span>
<span data-ttu-id="ec991-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec991-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec991-120">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec991-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec991-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="ec991-121">INPUTS</span></span>

### <span data-ttu-id="ec991-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ec991-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ec991-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ec991-123">OUTPUTS</span></span>

### <span data-ttu-id="ec991-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ec991-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ec991-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="ec991-125">NOTES</span></span>

## <span data-ttu-id="ec991-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ec991-126">RELATED LINKS</span></span>

[<span data-ttu-id="ec991-127">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="ec991-127">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="ec991-128">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="ec991-128">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="ec991-129">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="ec991-129">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="ec991-130">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="ec991-130">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


