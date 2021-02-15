---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: def44c0925239aed345eed84b4f34690d2db8746
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100395691"
---
# <span data-ttu-id="b6953-101">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6953-101">Set-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="b6953-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6953-102">SYNOPSIS</span></span>
<span data-ttu-id="b6953-103">Modifica la configurazione dell'autenticazione client di un oggetto profilo SSL.</span><span class="sxs-lookup"><span data-stu-id="b6953-103">Modifies the client auth configuration of a ssl profile object.</span></span>

## <span data-ttu-id="b6953-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b6953-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayClientAuthConfiguration -SslProfile <PSApplicationGatewaySslProfile>
 [-VerifyClientCertIssuerDN] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6953-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b6953-105">DESCRIPTION</span></span>
<span data-ttu-id="b6953-106">Il cmdlet **Set-AzApplicationGatewayClientAuthConfiguration** modifica la configurazione di autenticazione client di un oggetto profilo SSL.</span><span class="sxs-lookup"><span data-stu-id="b6953-106">The **Set-AzApplicationGatewayClientAuthConfiguration** cmdlet modifies the client auth configuration of a ssl profile object.</span></span>

## <span data-ttu-id="b6953-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b6953-107">EXAMPLES</span></span>

### <span data-ttu-id="b6953-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b6953-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> Set-AzApplicationGatewayClientAuthConfiguration -SslProfile $profile -VerifyClientCertIssuerDN
```

<span data-ttu-id="b6953-109">Il primo comando recupera il gateway applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw risorsa.</span><span class="sxs-lookup"><span data-stu-id="b6953-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="b6953-110">Il secondo comando recupera il profilo SSL denominato SslProfile01 per $AppGw e archivia le impostazioni nella variabile $profile locale.</span><span class="sxs-lookup"><span data-stu-id="b6953-110">The second command gets the ssl profile named SslProfile01 for $AppGw and stores the settings in the $profile variable.</span></span> <span data-ttu-id="b6953-111">L'ultimo comando modifica la configurazione dell'autenticazione client dell'oggetto profilo SSL archiviato in $profile.</span><span class="sxs-lookup"><span data-stu-id="b6953-111">The last command modifies the client auth configuration of the ssl profile object stored in $profile.</span></span>

## <span data-ttu-id="b6953-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6953-112">PARAMETERS</span></span>

### <span data-ttu-id="b6953-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6953-113">-DefaultProfile</span></span>
<span data-ttu-id="b6953-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b6953-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6953-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="b6953-115">-SslProfile</span></span>
<span data-ttu-id="b6953-116">Profilo SSL</span><span class="sxs-lookup"><span data-stu-id="b6953-116">The ssl profile</span></span>

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

### <span data-ttu-id="b6953-117">-VerifyClientCertIssuerDN</span><span class="sxs-lookup"><span data-stu-id="b6953-117">-VerifyClientCertIssuerDN</span></span>
<span data-ttu-id="b6953-118">Verificare il nome dell'autorità di certificazione client.</span><span class="sxs-lookup"><span data-stu-id="b6953-118">Verify client certificate issuer name.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6953-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6953-119">CommonParameters</span></span>
<span data-ttu-id="b6953-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6953-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6953-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b6953-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6953-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="b6953-122">INPUTS</span></span>

### <span data-ttu-id="b6953-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="b6953-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="b6953-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b6953-124">OUTPUTS</span></span>

### <span data-ttu-id="b6953-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="b6953-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="b6953-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="b6953-126">NOTES</span></span>

## <span data-ttu-id="b6953-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b6953-127">RELATED LINKS</span></span>


[<span data-ttu-id="b6953-128">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6953-128">New-AzApplicationGatewayClientAuthConfiguration</span></span>](./New-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="b6953-129">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6953-129">Get-AzApplicationGatewayClientAuthConfiguration</span></span>](./Get-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="b6953-130">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6953-130">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>](./Remove-AzApplicationGatewayClientAuthConfiguration.md)
