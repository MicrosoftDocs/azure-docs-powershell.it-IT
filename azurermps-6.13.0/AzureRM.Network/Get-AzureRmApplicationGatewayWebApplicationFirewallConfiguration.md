---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5D887302-7678-44C0-86F3-CEF2EF8A0991
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 1456afca27b6a5993fa014b738c415af5db98c6f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686911"
---
# <span data-ttu-id="6ce99-101">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ce99-101">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="6ce99-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6ce99-102">SYNOPSIS</span></span>
<span data-ttu-id="6ce99-103">Ottiene la configurazione WAF di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6ce99-103">Gets the WAF configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ce99-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6ce99-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ce99-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6ce99-105">DESCRIPTION</span></span>
<span data-ttu-id="6ce99-106">Il cmdlet **Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** ottiene la configurazione WAF (Web Application Firewall) di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6ce99-106">The **Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet gets the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="6ce99-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6ce99-107">EXAMPLES</span></span>

### <span data-ttu-id="6ce99-108">Esempio 1: ottenere una configurazione firewall applicazione Web Application Gateway</span><span class="sxs-lookup"><span data-stu-id="6ce99-108">Example 1: Get an application gateway web application firewall configuration</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FirewallConfig = Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGW
```

<span data-ttu-id="6ce99-109">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 e lo archivia nella variabile $AppGW.</span><span class="sxs-lookup"><span data-stu-id="6ce99-109">The first command gets the application gateway named ApplicationGateway01, and then stores it in the $AppGW variable.</span></span>
<span data-ttu-id="6ce99-110">Il secondo comando consente di ottenere la configurazione del firewall del gateway dell'applicazione in $AppGW e quindi di archiviarla in $FirewallConfig.</span><span class="sxs-lookup"><span data-stu-id="6ce99-110">The second command gets the firewall configuration of the application gateway in $AppGW, and then stores it in $FirewallConfig.</span></span>

## <span data-ttu-id="6ce99-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6ce99-111">PARAMETERS</span></span>

### <span data-ttu-id="6ce99-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6ce99-112">-ApplicationGateway</span></span>
<span data-ttu-id="6ce99-113">Specifica un oggetto gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6ce99-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="6ce99-114">Puoi usare il cmdlet Get-AzureRmApplicationGateway per ottenere un oggetto gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6ce99-114">You can use the Get-AzureRmApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="6ce99-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ce99-115">-DefaultProfile</span></span>
<span data-ttu-id="6ce99-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6ce99-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ce99-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ce99-117">CommonParameters</span></span>
<span data-ttu-id="6ce99-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ce99-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ce99-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ce99-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ce99-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6ce99-120">INPUTS</span></span>

### <span data-ttu-id="6ce99-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6ce99-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="6ce99-122">Parametri: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6ce99-122">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="6ce99-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6ce99-123">OUTPUTS</span></span>

### <span data-ttu-id="6ce99-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ce99-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="6ce99-125">Note</span><span class="sxs-lookup"><span data-stu-id="6ce99-125">NOTES</span></span>

## <span data-ttu-id="6ce99-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6ce99-126">RELATED LINKS</span></span>

[<span data-ttu-id="6ce99-127">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6ce99-127">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="6ce99-128">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ce99-128">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="6ce99-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ce99-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)


