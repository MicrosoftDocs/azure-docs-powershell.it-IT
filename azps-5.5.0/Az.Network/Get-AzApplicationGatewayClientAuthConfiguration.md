---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: eee7040dab93a4f73bacdf440c6450a525fab9a3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189847"
---
# <span data-ttu-id="a1bfb-101">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="a1bfb-101">Get-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="a1bfb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1bfb-102">SYNOPSIS</span></span>
<span data-ttu-id="a1bfb-103">Ottiene la configurazione di autenticazione client di un oggetto profilo SSL.</span><span class="sxs-lookup"><span data-stu-id="a1bfb-103">Gets the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="a1bfb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a1bfb-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayClientAuthConfiguration -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1bfb-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a1bfb-105">DESCRIPTION</span></span>
<span data-ttu-id="a1bfb-106">Il cmdlet **Get-AzApplicationGatewayClientAuthConfiguration ottiene** la configurazione di autenticazione client di un oggetto profilo SSL.</span><span class="sxs-lookup"><span data-stu-id="a1bfb-106">The **Get-AzApplicationGatewayClientAuthConfiguration** cmdlet gets the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="a1bfb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a1bfb-107">EXAMPLES</span></span>

### <span data-ttu-id="a1bfb-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a1bfb-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SslProfile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> $ClientAuthConfig = Get-AzApplicationGatewayClientAuthConfiguration -SslProfile $SslProfile
```

<span data-ttu-id="a1bfb-109">Il primo comando recupera il gateway applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw risorsa.</span><span class="sxs-lookup"><span data-stu-id="a1bfb-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="a1bfb-110">Il secondo comando recupera il profilo SSL denominato SslProfile01 per $AppGw e lo archivia $SslProfile variabile.</span><span class="sxs-lookup"><span data-stu-id="a1bfb-110">The second command gets the SSL profile named SslProfile01 for $AppGw and stores it $SslProfile variable.</span></span> <span data-ttu-id="a1bfb-111">L'ultimo comando recupera la configurazione di autenticazione client dal profilo SSL $SslProfile e la archivia nella $ClientAuthConfig variabile.</span><span class="sxs-lookup"><span data-stu-id="a1bfb-111">The last command gets the client authentication configuration from the SSL profile $SslProfile and stores it in the $ClientAuthConfig variable.</span></span>

## <span data-ttu-id="a1bfb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1bfb-112">PARAMETERS</span></span>

### <span data-ttu-id="a1bfb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1bfb-113">-DefaultProfile</span></span>
<span data-ttu-id="a1bfb-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a1bfb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1bfb-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="a1bfb-115">-SslProfile</span></span>
<span data-ttu-id="a1bfb-116">Profilo SSL</span><span class="sxs-lookup"><span data-stu-id="a1bfb-116">The ssl profile</span></span>

```yaml
Type: PSApplicationGatewaySslProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1bfb-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1bfb-117">CommonParameters</span></span>
<span data-ttu-id="a1bfb-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1bfb-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1bfb-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a1bfb-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1bfb-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="a1bfb-120">INPUTS</span></span>

### <span data-ttu-id="a1bfb-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="a1bfb-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="a1bfb-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a1bfb-122">OUTPUTS</span></span>

### <span data-ttu-id="a1bfb-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="a1bfb-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="a1bfb-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="a1bfb-124">NOTES</span></span>

## <span data-ttu-id="a1bfb-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a1bfb-125">RELATED LINKS</span></span>

[<span data-ttu-id="a1bfb-126">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="a1bfb-126">New-AzApplicationGatewayClientAuthConfiguration</span></span>](./New-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="a1bfb-127">Add-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="a1bfb-127">Add-AzApplicationGatewayClientAuthConfiguration</span></span>](./Add-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="a1bfb-128">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="a1bfb-128">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>](./Remove-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="a1bfb-129">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="a1bfb-129">Set-AzApplicationGatewayClientAuthConfiguration</span></span>](./Set-AzApplicationGatewayClientAuthConfiguration.md)