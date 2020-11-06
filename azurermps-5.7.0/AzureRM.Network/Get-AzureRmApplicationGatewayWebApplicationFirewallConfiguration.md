---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5D887302-7678-44C0-86F3-CEF2EF8A0991
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 44411d8f763e217d5513440a90f713c92c6d6398
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518931"
---
# <span data-ttu-id="97270-101">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="97270-101">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="97270-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="97270-102">SYNOPSIS</span></span>
<span data-ttu-id="97270-103">Ottiene la configurazione WAF di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="97270-103">Gets the WAF configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97270-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="97270-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97270-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="97270-105">DESCRIPTION</span></span>
<span data-ttu-id="97270-106">Il cmdlet **Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** ottiene la configurazione WAF (Web Application Firewall) di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="97270-106">The **Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet gets the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="97270-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="97270-107">EXAMPLES</span></span>

### <span data-ttu-id="97270-108">Esempio 1: ottenere una configurazione firewall applicazione Web Application Gateway</span><span class="sxs-lookup"><span data-stu-id="97270-108">Example 1: Get an application gateway web application firewall configuration</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FirewallConfig = Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGW
```

<span data-ttu-id="97270-109">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 e lo archivia nella variabile $AppGW.</span><span class="sxs-lookup"><span data-stu-id="97270-109">The first command gets the application gateway named ApplicationGateway01, and then stores it in the $AppGW variable.</span></span>

<span data-ttu-id="97270-110">Il secondo comando consente di ottenere la configurazione del firewall del gateway dell'applicazione in $AppGW e quindi di archiviarla in $FirewallConfig.</span><span class="sxs-lookup"><span data-stu-id="97270-110">The second command gets the firewall configuration of the application gateway in $AppGW, and then stores it in $FirewallConfig.</span></span>

## <span data-ttu-id="97270-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="97270-111">PARAMETERS</span></span>

### <span data-ttu-id="97270-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="97270-112">-ApplicationGateway</span></span>
<span data-ttu-id="97270-113">Specifica un oggetto gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="97270-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="97270-114">Puoi usare il cmdlet Get-AzureRmApplicationGateway per ottenere un oggetto gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="97270-114">You can use the Get-AzureRmApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="97270-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97270-115">-DefaultProfile</span></span>
<span data-ttu-id="97270-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="97270-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97270-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97270-117">CommonParameters</span></span>
<span data-ttu-id="97270-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97270-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97270-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97270-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97270-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="97270-120">INPUTS</span></span>

### <span data-ttu-id="97270-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="97270-121">PSApplicationGateway</span></span>
<span data-ttu-id="97270-122">Il parametro ' ApplicationGateway ' accetta il valore di tipo ' PSApplicationGateway ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="97270-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="97270-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="97270-123">OUTPUTS</span></span>

### <span data-ttu-id="97270-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="97270-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="97270-125">Note</span><span class="sxs-lookup"><span data-stu-id="97270-125">NOTES</span></span>

## <span data-ttu-id="97270-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="97270-126">RELATED LINKS</span></span>

[<span data-ttu-id="97270-127">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="97270-127">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="97270-128">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="97270-128">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="97270-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="97270-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)


