---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 289B761C-1A1D-46D2-8755-B6B6A4758EFC
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 0c226cf7dabbc170e137f1a809cee0afe3c7e76f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992541"
---
# <span data-ttu-id="5b60a-101">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="5b60a-101">Remove-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="5b60a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b60a-102">SYNOPSIS</span></span>
<span data-ttu-id="5b60a-103">Rimuove una configurazione IP front-end da un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="5b60a-103">Removes a front-end IP configuration from an application gateway.</span></span>

## <span data-ttu-id="5b60a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5b60a-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendIPConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b60a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5b60a-105">DESCRIPTION</span></span>
<span data-ttu-id="5b60a-106">Il cmdlet **Remove-AzApplicationGatewayFrontendIPConfig** rimuove l'indirizzo IP di frontend da un gateway applicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="5b60a-106">The **Remove-AzApplicationGatewayFrontendIPConfig** cmdlet removes frontend IP from an Azure application gateway.</span></span>

## <span data-ttu-id="5b60a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5b60a-107">EXAMPLES</span></span>

### <span data-ttu-id="5b60a-108">Esempio 1: Rimuovere una configurazione IP front-end</span><span class="sxs-lookup"><span data-stu-id="5b60a-108">Example 1: Remove a front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIP02"
```

<span data-ttu-id="5b60a-109">Il primo comando ottiene un gateway applicazione denominato ApplicationGateway01 e lo archivia nella $AppGw variabile.</span><span class="sxs-lookup"><span data-stu-id="5b60a-109">The first command gets an application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="5b60a-110">Il secondo comando rimuove la configurazione IP front-end denominata FrontEndIP02 dal gateway di applicazione archiviato in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="5b60a-110">The second command removes the front-end IP configuration named FrontEndIP02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="5b60a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b60a-111">PARAMETERS</span></span>

### <span data-ttu-id="5b60a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5b60a-112">-ApplicationGateway</span></span>
<span data-ttu-id="5b60a-113">Specifica un gateway applicazione da cui rimuovere una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="5b60a-113">Specifies an application gateway from which to remove a front-end IP configuration.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b60a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b60a-114">-DefaultProfile</span></span>
<span data-ttu-id="5b60a-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5b60a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b60a-116">-Name</span><span class="sxs-lookup"><span data-stu-id="5b60a-116">-Name</span></span>
<span data-ttu-id="5b60a-117">Specifica il nome di una configurazione IP front-end da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="5b60a-117">Specifies the name of a front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="5b60a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b60a-118">CommonParameters</span></span>
<span data-ttu-id="5b60a-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b60a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b60a-120">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5b60a-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b60a-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="5b60a-121">INPUTS</span></span>

### <span data-ttu-id="5b60a-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5b60a-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5b60a-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5b60a-123">OUTPUTS</span></span>

### <span data-ttu-id="5b60a-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5b60a-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5b60a-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="5b60a-125">NOTES</span></span>

## <span data-ttu-id="5b60a-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5b60a-126">RELATED LINKS</span></span>

[<span data-ttu-id="5b60a-127">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="5b60a-127">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="5b60a-128">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="5b60a-128">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="5b60a-129">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="5b60a-129">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="5b60a-130">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="5b60a-130">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


