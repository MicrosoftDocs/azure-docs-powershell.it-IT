---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: fdd461ea2908e59ba824b09a49bed3b6b8f4d38f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328073"
---
# <span data-ttu-id="2a601-101">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2a601-101">Remove-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="2a601-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2a601-102">SYNOPSIS</span></span>
<span data-ttu-id="2a601-103">Rimuove una configurazione di Reindirizzamento da un gateway applicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="2a601-103">Removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="2a601-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2a601-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRedirectConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a601-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2a601-105">DESCRIPTION</span></span>
<span data-ttu-id="2a601-106">Il cmdlet **Remove-AzApplicationGatewayRedirectConfiguration** rimuove una configurazione di Reindirizzamento da un gateway applicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="2a601-106">The **Remove-AzApplicationGatewayRedirectConfiguration** cmdlet removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="2a601-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2a601-107">EXAMPLES</span></span>

### <span data-ttu-id="2a601-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2a601-108">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$AppGw = Remove-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01"
```

<span data-ttu-id="2a601-109">Il primo comando ottiene un gateway dell'applicazione e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="2a601-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="2a601-110">Il secondo comando rimuove la configurazione di reindirizzamento denominata Redirect01 dal gateway dell'applicazione archiviato in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="2a601-110">The second command removes the redirect configuration named Redirect01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="2a601-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2a601-111">PARAMETERS</span></span>

### <span data-ttu-id="2a601-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2a601-112">-ApplicationGateway</span></span>
<span data-ttu-id="2a601-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2a601-113">The applicationGateway</span></span>

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

### <span data-ttu-id="2a601-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a601-114">-DefaultProfile</span></span>
<span data-ttu-id="2a601-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2a601-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a601-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="2a601-116">-Name</span></span>
<span data-ttu-id="2a601-117">Nome della configurazione di Reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="2a601-117">The name of the redirect configuration</span></span>

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

### <span data-ttu-id="2a601-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a601-118">CommonParameters</span></span>
<span data-ttu-id="2a601-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a601-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a601-120">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a601-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a601-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2a601-121">INPUTS</span></span>

### <span data-ttu-id="2a601-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2a601-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2a601-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2a601-123">OUTPUTS</span></span>

### <span data-ttu-id="2a601-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2a601-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2a601-125">Note</span><span class="sxs-lookup"><span data-stu-id="2a601-125">NOTES</span></span>

## <span data-ttu-id="2a601-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2a601-126">RELATED LINKS</span></span>

[<span data-ttu-id="2a601-127">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2a601-127">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="2a601-128">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2a601-128">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="2a601-129">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2a601-129">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="2a601-130">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2a601-130">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
