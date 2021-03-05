---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: 830f84b8f14e84693b6657fdea2542c2acf59b25
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973661"
---
# <span data-ttu-id="1e492-101">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="1e492-101">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="1e492-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e492-102">SYNOPSIS</span></span>
<span data-ttu-id="1e492-103">Rimuove la configurazione di autenticazione client di un oggetto profilo SSL.</span><span class="sxs-lookup"><span data-stu-id="1e492-103">Removes the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="1e492-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1e492-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayClientAuthConfiguration -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e492-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1e492-105">DESCRIPTION</span></span>
<span data-ttu-id="1e492-106">Il cmdlet **Remove-AzApplicationGatewayClientAuthConfiguration rimuove** la configurazione di autenticazione client di un oggetto profilo SSL.</span><span class="sxs-lookup"><span data-stu-id="1e492-106">The **Remove-AzApplicationGatewayClientAuthConfiguration** cmdlet removes the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="1e492-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1e492-107">EXAMPLES</span></span>

### <span data-ttu-id="1e492-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1e492-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "Profile01" -ApplicationGateway $AppGw
PS C:\> Remove-AzApplicationGatewayClientAuthConfiguration -SslProfile $profile
```

<span data-ttu-id="1e492-109">Il primo comando recupera il gateway applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw risorsa.</span><span class="sxs-lookup"><span data-stu-id="1e492-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="1e492-110">Il secondo comando recupera il profilo SSL denominato Profile01 per $AppGw e lo archivia nella $profile variabile.</span><span class="sxs-lookup"><span data-stu-id="1e492-110">The second command gets the SSL profile named Profile01 for $AppGw and stores it in the $profile variable.</span></span> <span data-ttu-id="1e492-111">L'ultimo comando rimuove la configurazione di autenticazione client del profilo SSL archiviato in $profile.</span><span class="sxs-lookup"><span data-stu-id="1e492-111">The last command removes the client authentication configuration of the ssl profile stored in $profile.</span></span>

## <span data-ttu-id="1e492-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e492-112">PARAMETERS</span></span>

### <span data-ttu-id="1e492-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e492-113">-DefaultProfile</span></span>
<span data-ttu-id="1e492-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1e492-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e492-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="1e492-115">-SslProfile</span></span>
<span data-ttu-id="1e492-116">Profilo SSL</span><span class="sxs-lookup"><span data-stu-id="1e492-116">The ssl profile</span></span>

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

### <span data-ttu-id="1e492-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e492-117">CommonParameters</span></span>
<span data-ttu-id="1e492-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e492-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e492-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1e492-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e492-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="1e492-120">INPUTS</span></span>

### <span data-ttu-id="1e492-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="1e492-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="1e492-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1e492-122">OUTPUTS</span></span>

### <span data-ttu-id="1e492-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="1e492-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="1e492-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="1e492-124">NOTES</span></span>

## <span data-ttu-id="1e492-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1e492-125">RELATED LINKS</span></span>

[<span data-ttu-id="1e492-126">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="1e492-126">New-AzApplicationGatewayClientAuthConfiguration</span></span>](./New-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="1e492-127">Add-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="1e492-127">Add-AzApplicationGatewayClientAuthConfiguration</span></span>](./Add-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="1e492-128">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="1e492-128">Get-AzApplicationGatewayClientAuthConfiguration</span></span>](./Get-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="1e492-129">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="1e492-129">Set-AzApplicationGatewayClientAuthConfiguration</span></span>](./Set-AzApplicationGatewayClientAuthConfiguration.md)