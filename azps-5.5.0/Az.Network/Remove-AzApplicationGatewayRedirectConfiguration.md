---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: fdd461ea2908e59ba824b09a49bed3b6b8f4d38f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179543"
---
# <span data-ttu-id="17386-101">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="17386-101">Remove-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="17386-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17386-102">SYNOPSIS</span></span>
<span data-ttu-id="17386-103">Rimuove una configurazione di reindirizzamento da un Gateway applicazioni esistente.</span><span class="sxs-lookup"><span data-stu-id="17386-103">Removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="17386-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="17386-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRedirectConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17386-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="17386-105">DESCRIPTION</span></span>
<span data-ttu-id="17386-106">Il cmdlet **Remove-AzApplicationGatewayRedirectConfiguration** rimuove una configurazione di reindirizzamento da un Gateway applicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="17386-106">The **Remove-AzApplicationGatewayRedirectConfiguration** cmdlet removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="17386-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="17386-107">EXAMPLES</span></span>

### <span data-ttu-id="17386-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="17386-108">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$AppGw = Remove-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01"
```

<span data-ttu-id="17386-109">Il primo comando ottiene un gateway applicazione e lo archivia nella $AppGw variabile.</span><span class="sxs-lookup"><span data-stu-id="17386-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="17386-110">Il secondo comando rimuove la configurazione di reindirizzamento denominata Redirect01 dal gateway applicazione archiviato in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="17386-110">The second command removes the redirect configuration named Redirect01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="17386-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17386-111">PARAMETERS</span></span>

### <span data-ttu-id="17386-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="17386-112">-ApplicationGateway</span></span>
<span data-ttu-id="17386-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="17386-113">The applicationGateway</span></span>

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

### <span data-ttu-id="17386-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17386-114">-DefaultProfile</span></span>
<span data-ttu-id="17386-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="17386-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17386-116">-Name</span><span class="sxs-lookup"><span data-stu-id="17386-116">-Name</span></span>
<span data-ttu-id="17386-117">Nome della configurazione di reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="17386-117">The name of the redirect configuration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17386-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17386-118">CommonParameters</span></span>
<span data-ttu-id="17386-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17386-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17386-120">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17386-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17386-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="17386-121">INPUTS</span></span>

### <span data-ttu-id="17386-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="17386-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="17386-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="17386-123">OUTPUTS</span></span>

### <span data-ttu-id="17386-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="17386-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="17386-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="17386-125">NOTES</span></span>

## <span data-ttu-id="17386-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="17386-126">RELATED LINKS</span></span>

[<span data-ttu-id="17386-127">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="17386-127">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="17386-128">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="17386-128">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="17386-129">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="17386-129">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="17386-130">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="17386-130">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
