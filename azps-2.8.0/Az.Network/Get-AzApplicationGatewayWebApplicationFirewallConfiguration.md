---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D887302-7678-44C0-86F3-CEF2EF8A0991
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: e2f477aa657bc4d21a650edffb7f014ae3c1ba62
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93853798"
---
# <span data-ttu-id="f532a-101">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="f532a-101">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="f532a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f532a-102">SYNOPSIS</span></span>
<span data-ttu-id="f532a-103">Ottiene la configurazione WAF di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f532a-103">Gets the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="f532a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f532a-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f532a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f532a-105">DESCRIPTION</span></span>
<span data-ttu-id="f532a-106">Il cmdlet **Get-AzApplicationGatewayWebApplicationFirewallConfiguration** ottiene la configurazione WAF (Web Application Firewall) di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f532a-106">The **Get-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet gets the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="f532a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f532a-107">EXAMPLES</span></span>

### <span data-ttu-id="f532a-108">Esempio 1: ottenere una configurazione firewall applicazione Web Application Gateway</span><span class="sxs-lookup"><span data-stu-id="f532a-108">Example 1: Get an application gateway web application firewall configuration</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FirewallConfig = Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGW
```

<span data-ttu-id="f532a-109">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 e lo archivia nella variabile $AppGW.</span><span class="sxs-lookup"><span data-stu-id="f532a-109">The first command gets the application gateway named ApplicationGateway01, and then stores it in the $AppGW variable.</span></span>
<span data-ttu-id="f532a-110">Il secondo comando consente di ottenere la configurazione del firewall del gateway dell'applicazione in $AppGW e quindi di archiviarla in $FirewallConfig.</span><span class="sxs-lookup"><span data-stu-id="f532a-110">The second command gets the firewall configuration of the application gateway in $AppGW, and then stores it in $FirewallConfig.</span></span>

## <span data-ttu-id="f532a-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f532a-111">PARAMETERS</span></span>

### <span data-ttu-id="f532a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f532a-112">-ApplicationGateway</span></span>
<span data-ttu-id="f532a-113">Specifica un oggetto gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f532a-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="f532a-114">Puoi usare il cmdlet Get-AzApplicationGateway per ottenere un oggetto gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f532a-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="f532a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f532a-115">-DefaultProfile</span></span>
<span data-ttu-id="f532a-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f532a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f532a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f532a-117">CommonParameters</span></span>
<span data-ttu-id="f532a-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f532a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f532a-119">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f532a-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f532a-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f532a-120">INPUTS</span></span>

### <span data-ttu-id="f532a-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f532a-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f532a-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f532a-122">OUTPUTS</span></span>

### <span data-ttu-id="f532a-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="f532a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="f532a-124">Note</span><span class="sxs-lookup"><span data-stu-id="f532a-124">NOTES</span></span>

## <span data-ttu-id="f532a-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f532a-125">RELATED LINKS</span></span>

[<span data-ttu-id="f532a-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f532a-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="f532a-127">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="f532a-127">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="f532a-128">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="f532a-128">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


