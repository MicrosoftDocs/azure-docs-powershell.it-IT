---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 289B761C-1A1D-46D2-8755-B6B6A4758EFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: d376bc1e70d0441f139b64c19466a88daf6877c4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032346"
---
# <span data-ttu-id="b0dd8-101">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="b0dd8-101">Remove-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="b0dd8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b0dd8-102">SYNOPSIS</span></span>
<span data-ttu-id="b0dd8-103">Rimuove una configurazione IP front-end da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b0dd8-103">Removes a front-end IP configuration from an application gateway.</span></span>

## <span data-ttu-id="b0dd8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b0dd8-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendIPConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0dd8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b0dd8-105">DESCRIPTION</span></span>
<span data-ttu-id="b0dd8-106">Il cmdlet **Remove-AzApplicationGatewayFrontendIPConfig** rimuove l'IP frontend da un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="b0dd8-106">The **Remove-AzApplicationGatewayFrontendIPConfig** cmdlet removes frontend IP from an Azure application gateway.</span></span>

## <span data-ttu-id="b0dd8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b0dd8-107">EXAMPLES</span></span>

### <span data-ttu-id="b0dd8-108">Esempio 1: rimuovere una configurazione IP front-end</span><span class="sxs-lookup"><span data-stu-id="b0dd8-108">Example 1: Remove a front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIP02"
```

<span data-ttu-id="b0dd8-109">Il primo comando ottiene un gateway dell'applicazione denominato ApplicationGateway01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="b0dd8-109">The first command gets an application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b0dd8-110">Il secondo comando rimuove la configurazione IP front-end denominata FrontEndIP02 dal gateway dell'applicazione archiviato in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="b0dd8-110">The second command removes the front-end IP configuration named FrontEndIP02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="b0dd8-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b0dd8-111">PARAMETERS</span></span>

### <span data-ttu-id="b0dd8-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b0dd8-112">-ApplicationGateway</span></span>
<span data-ttu-id="b0dd8-113">Specifica un gateway dell'applicazione da cui rimuovere una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="b0dd8-113">Specifies an application gateway from which to remove a front-end IP configuration.</span></span>

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

### <span data-ttu-id="b0dd8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0dd8-114">-DefaultProfile</span></span>
<span data-ttu-id="b0dd8-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b0dd8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0dd8-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="b0dd8-116">-Name</span></span>
<span data-ttu-id="b0dd8-117">Specifica il nome di una configurazione IP front-end da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="b0dd8-117">Specifies the name of a front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="b0dd8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0dd8-118">CommonParameters</span></span>
<span data-ttu-id="b0dd8-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0dd8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0dd8-120">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b0dd8-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0dd8-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b0dd8-121">INPUTS</span></span>

### <span data-ttu-id="b0dd8-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b0dd8-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b0dd8-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b0dd8-123">OUTPUTS</span></span>

### <span data-ttu-id="b0dd8-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b0dd8-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b0dd8-125">Note</span><span class="sxs-lookup"><span data-stu-id="b0dd8-125">NOTES</span></span>

## <span data-ttu-id="b0dd8-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b0dd8-126">RELATED LINKS</span></span>

[<span data-ttu-id="b0dd8-127">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="b0dd8-127">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="b0dd8-128">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="b0dd8-128">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="b0dd8-129">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="b0dd8-129">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="b0dd8-130">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="b0dd8-130">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


