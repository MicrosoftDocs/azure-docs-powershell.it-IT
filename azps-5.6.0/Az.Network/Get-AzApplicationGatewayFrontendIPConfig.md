---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 364C41D0-A5DB-4AEF-853A-FE5A11AD9155
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: cab20e2b92343549b5138f14f88505c70624effb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996546"
---
# <span data-ttu-id="0ed96-101">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="0ed96-101">Get-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="0ed96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ed96-102">SYNOPSIS</span></span>
<span data-ttu-id="0ed96-103">Ottiene la configurazione IP front-end di un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="0ed96-103">Gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="0ed96-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0ed96-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFrontendIPConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ed96-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0ed96-105">DESCRIPTION</span></span>
<span data-ttu-id="0ed96-106">Il cmdlet **Get-AzApplicationGatewayFrontendIPConfig** ottiene la configurazione IP front-end di un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="0ed96-106">The **Get-AzApplicationGatewayFrontendIPConfig** cmdlet gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="0ed96-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0ed96-107">EXAMPLES</span></span>

### <span data-ttu-id="0ed96-108">Esempio 1: Ottenere una configurazione IP front-end specificata</span><span class="sxs-lookup"><span data-stu-id="0ed96-108">Example 1: Get a specified front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIP= Get-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -ApplicationGateway $AppGw
```

<span data-ttu-id="0ed96-109">Il primo comando recupera un gateway applicazione denominato ApplicationGateway01 dal gruppo di risorse denominato ResourceGroup01 e lo archivia nella $AppGw variabile. Il secondo comando recupera la configurazione IP front-end denominata FrontEndIP01 da $AppGw e la archivia nella variabile $FrontEndIP front-end.</span><span class="sxs-lookup"><span data-stu-id="0ed96-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the front-end IP configuration named FrontEndIP01 from $AppGw and stores it in the $FrontEndIP variable.</span></span>

### <span data-ttu-id="0ed96-110">Esempio 2: Ottenere un elenco di configurazioni IP front-end</span><span class="sxs-lookup"><span data-stu-id="0ed96-110">Example 2: Get a list of front-end IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIPs= Get-AzApplicationGatewayFrontendIPConfig  -ApplicationGateway $AppGw
```

<span data-ttu-id="0ed96-111">Il primo comando recupera un gateway applicazione denominato ApplicationGateway01 dal gruppo di risorse denominato ResourceGroup01 e lo archivia nella $AppGw variabile. Il secondo comando ottiene un elenco delle configurazioni IP front-end da $AppGw e lo archivia nella variabile $FrontEndIPs front-end.</span><span class="sxs-lookup"><span data-stu-id="0ed96-111">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets a list of the front-end IP configurations from $AppGw and stores it in the $FrontEndIPs variable.</span></span>

## <span data-ttu-id="0ed96-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ed96-112">PARAMETERS</span></span>

### <span data-ttu-id="0ed96-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0ed96-113">-ApplicationGateway</span></span>
<span data-ttu-id="0ed96-114">Specifica l'oggetto gateway applicazione che contiene la configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="0ed96-114">Specifies the application gateway object that contains the front-end IP configuration.</span></span>

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

### <span data-ttu-id="0ed96-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ed96-115">-DefaultProfile</span></span>
<span data-ttu-id="0ed96-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0ed96-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ed96-117">-Name</span><span class="sxs-lookup"><span data-stu-id="0ed96-117">-Name</span></span>
<span data-ttu-id="0ed96-118">Specifica il nome della configurazione IP front-end che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ed96-118">Specifies the name of the front-end IP configuration that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ed96-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ed96-119">CommonParameters</span></span>
<span data-ttu-id="0ed96-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ed96-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ed96-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0ed96-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ed96-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="0ed96-122">INPUTS</span></span>

### <span data-ttu-id="0ed96-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0ed96-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0ed96-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0ed96-124">OUTPUTS</span></span>

### <span data-ttu-id="0ed96-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="0ed96-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="0ed96-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="0ed96-126">NOTES</span></span>

## <span data-ttu-id="0ed96-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0ed96-127">RELATED LINKS</span></span>

[<span data-ttu-id="0ed96-128">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="0ed96-128">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="0ed96-129">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="0ed96-129">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="0ed96-130">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="0ed96-130">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="0ed96-131">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="0ed96-131">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


