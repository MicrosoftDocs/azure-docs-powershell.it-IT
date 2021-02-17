---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: 64dc67a59b739ac7cab51c9c4a02fd7a73f8b4cc
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100407591"
---
# <span data-ttu-id="0f55b-101">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="0f55b-101">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="0f55b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f55b-102">SYNOPSIS</span></span>
<span data-ttu-id="0f55b-103">Rimuove la configurazione di autenticazione client di un oggetto profilo SSL.</span><span class="sxs-lookup"><span data-stu-id="0f55b-103">Removes the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="0f55b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0f55b-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayClientAuthConfiguration -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f55b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0f55b-105">DESCRIPTION</span></span>
<span data-ttu-id="0f55b-106">Il cmdlet **Remove-AzApplicationGatewayClientAuthConfiguration rimuove** la configurazione di autenticazione client di un oggetto profilo SSL.</span><span class="sxs-lookup"><span data-stu-id="0f55b-106">The **Remove-AzApplicationGatewayClientAuthConfiguration** cmdlet removes the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="0f55b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0f55b-107">EXAMPLES</span></span>

### <span data-ttu-id="0f55b-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0f55b-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "Profile01" -ApplicationGateway $AppGw
PS C:\> Remove-AzApplicationGatewayClientAuthConfiguration -SslProfile $profile
```

<span data-ttu-id="0f55b-109">Il primo comando recupera il gateway applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella $AppGw variabile.</span><span class="sxs-lookup"><span data-stu-id="0f55b-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="0f55b-110">Il secondo comando recupera il profilo SSL denominato Profile01 per $AppGw e lo archivia nella $profile variabile.</span><span class="sxs-lookup"><span data-stu-id="0f55b-110">The second command gets the SSL profile named Profile01 for $AppGw and stores it in the $profile variable.</span></span> <span data-ttu-id="0f55b-111">L'ultimo comando rimuove la configurazione di autenticazione client del profilo SSL archiviato in $profile.</span><span class="sxs-lookup"><span data-stu-id="0f55b-111">The last command removes the client authentication configuration of the ssl profile stored in $profile.</span></span>

## <span data-ttu-id="0f55b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f55b-112">PARAMETERS</span></span>

### <span data-ttu-id="0f55b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f55b-113">-DefaultProfile</span></span>
<span data-ttu-id="0f55b-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0f55b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f55b-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="0f55b-115">-SslProfile</span></span>
<span data-ttu-id="0f55b-116">Profilo SSL</span><span class="sxs-lookup"><span data-stu-id="0f55b-116">The ssl profile</span></span>

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

### <span data-ttu-id="0f55b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f55b-117">CommonParameters</span></span>
<span data-ttu-id="0f55b-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f55b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f55b-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0f55b-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f55b-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="0f55b-120">INPUTS</span></span>

### <span data-ttu-id="0f55b-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="0f55b-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="0f55b-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0f55b-122">OUTPUTS</span></span>

### <span data-ttu-id="0f55b-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="0f55b-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="0f55b-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="0f55b-124">NOTES</span></span>

## <span data-ttu-id="0f55b-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0f55b-125">RELATED LINKS</span></span>

[<span data-ttu-id="0f55b-126">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="0f55b-126">New-AzApplicationGatewayClientAuthConfiguration</span></span>](./New-AzApplicationGatewayClientAuthConfiguration.md)


[<span data-ttu-id="0f55b-127">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="0f55b-127">Get-AzApplicationGatewayClientAuthConfiguration</span></span>](./Get-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="0f55b-128">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="0f55b-128">Set-AzApplicationGatewayClientAuthConfiguration</span></span>](./Set-AzApplicationGatewayClientAuthConfiguration.md)
