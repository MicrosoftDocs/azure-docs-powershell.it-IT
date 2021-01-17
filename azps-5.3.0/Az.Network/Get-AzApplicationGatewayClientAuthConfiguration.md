---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: eee7040dab93a4f73bacdf440c6450a525fab9a3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475521"
---
# <span data-ttu-id="c0878-101">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="c0878-101">Get-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="c0878-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c0878-102">SYNOPSIS</span></span>
<span data-ttu-id="c0878-103">Ottiene la configurazione di autenticazione client di un oggetto profilo SSL.</span><span class="sxs-lookup"><span data-stu-id="c0878-103">Gets the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="c0878-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c0878-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayClientAuthConfiguration -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0878-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c0878-105">DESCRIPTION</span></span>
<span data-ttu-id="c0878-106">Il cmdlet **Get-AzApplicationGatewayClientAuthConfiguration** ottiene la configurazione di autenticazione del client di un oggetto profilo SSL.</span><span class="sxs-lookup"><span data-stu-id="c0878-106">The **Get-AzApplicationGatewayClientAuthConfiguration** cmdlet gets the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="c0878-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c0878-107">EXAMPLES</span></span>

### <span data-ttu-id="c0878-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c0878-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SslProfile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> $ClientAuthConfig = Get-AzApplicationGatewayClientAuthConfiguration -SslProfile $SslProfile
```

<span data-ttu-id="c0878-109">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="c0878-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="c0878-110">Il secondo comando ottiene il profilo SSL denominato SslProfile01 per $AppGw e lo archivia $SslProfile variabile.</span><span class="sxs-lookup"><span data-stu-id="c0878-110">The second command gets the SSL profile named SslProfile01 for $AppGw and stores it $SslProfile variable.</span></span> <span data-ttu-id="c0878-111">L'ultimo comando ottiene la configurazione di autenticazione del client dal profilo SSL $SslProfile e lo archivia nella variabile $ClientAuthConfig.</span><span class="sxs-lookup"><span data-stu-id="c0878-111">The last command gets the client authentication configuration from the SSL profile $SslProfile and stores it in the $ClientAuthConfig variable.</span></span>

## <span data-ttu-id="c0878-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c0878-112">PARAMETERS</span></span>

### <span data-ttu-id="c0878-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0878-113">-DefaultProfile</span></span>
<span data-ttu-id="c0878-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c0878-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0878-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="c0878-115">-SslProfile</span></span>
<span data-ttu-id="c0878-116">Profilo SSL</span><span class="sxs-lookup"><span data-stu-id="c0878-116">The ssl profile</span></span>

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

### <span data-ttu-id="c0878-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0878-117">CommonParameters</span></span>
<span data-ttu-id="c0878-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0878-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0878-119">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c0878-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0878-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c0878-120">INPUTS</span></span>

### <span data-ttu-id="c0878-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="c0878-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="c0878-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c0878-122">OUTPUTS</span></span>

### <span data-ttu-id="c0878-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="c0878-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="c0878-124">Note</span><span class="sxs-lookup"><span data-stu-id="c0878-124">NOTES</span></span>

## <span data-ttu-id="c0878-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c0878-125">RELATED LINKS</span></span>

[<span data-ttu-id="c0878-126">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="c0878-126">New-AzApplicationGatewayClientAuthConfiguration</span></span>](./New-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="c0878-127">Add-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="c0878-127">Add-AzApplicationGatewayClientAuthConfiguration</span></span>](./Add-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="c0878-128">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="c0878-128">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>](./Remove-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="c0878-129">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="c0878-129">Set-AzApplicationGatewayClientAuthConfiguration</span></span>](./Set-AzApplicationGatewayClientAuthConfiguration.md)