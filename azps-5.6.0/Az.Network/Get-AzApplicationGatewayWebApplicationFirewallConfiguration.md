---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D887302-7678-44C0-86F3-CEF2EF8A0991
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: d3b8a57fcd170a2a1f1e4e4c539cff8a60885260
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993928"
---
# <span data-ttu-id="7e93e-101">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="7e93e-101">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="7e93e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e93e-102">SYNOPSIS</span></span>
<span data-ttu-id="7e93e-103">Ottiene la configurazione WAF di un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="7e93e-103">Gets the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="7e93e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7e93e-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e93e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7e93e-105">DESCRIPTION</span></span>
<span data-ttu-id="7e93e-106">Il cmdlet **Get-AzApplicationGatewayWebApplicationFirewallConfiguration** ottiene la configurazione WAF (Web Application Firewall) di un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="7e93e-106">The **Get-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet gets the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="7e93e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7e93e-107">EXAMPLES</span></span>

### <span data-ttu-id="7e93e-108">Esempio 1: Ottenere la configurazione firewall di un'applicazione Web di gateway di applicazione</span><span class="sxs-lookup"><span data-stu-id="7e93e-108">Example 1: Get an application gateway web application firewall configuration</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FirewallConfig = Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGW
```

<span data-ttu-id="7e93e-109">Il primo comando recupera il gateway applicazione denominato ApplicationGateway01 e quindi lo archivia nella $AppGW variabile.</span><span class="sxs-lookup"><span data-stu-id="7e93e-109">The first command gets the application gateway named ApplicationGateway01, and then stores it in the $AppGW variable.</span></span>
<span data-ttu-id="7e93e-110">Il secondo comando recupera la configurazione del firewall del gateway applicazione in $AppGW e quindi lo archivia in $FirewallConfig.</span><span class="sxs-lookup"><span data-stu-id="7e93e-110">The second command gets the firewall configuration of the application gateway in $AppGW, and then stores it in $FirewallConfig.</span></span>

## <span data-ttu-id="7e93e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e93e-111">PARAMETERS</span></span>

### <span data-ttu-id="7e93e-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7e93e-112">-ApplicationGateway</span></span>
<span data-ttu-id="7e93e-113">Specifica un oggetto gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="7e93e-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="7e93e-114">È possibile usare il cmdlet Get-AzApplicationGateway per ottenere un oggetto gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="7e93e-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="7e93e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e93e-115">-DefaultProfile</span></span>
<span data-ttu-id="7e93e-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7e93e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e93e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e93e-117">CommonParameters</span></span>
<span data-ttu-id="7e93e-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e93e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e93e-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7e93e-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e93e-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="7e93e-120">INPUTS</span></span>

### <span data-ttu-id="7e93e-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7e93e-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7e93e-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7e93e-122">OUTPUTS</span></span>

### <span data-ttu-id="7e93e-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="7e93e-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="7e93e-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="7e93e-124">NOTES</span></span>

## <span data-ttu-id="7e93e-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7e93e-125">RELATED LINKS</span></span>

[<span data-ttu-id="7e93e-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7e93e-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="7e93e-127">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="7e93e-127">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="7e93e-128">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="7e93e-128">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


