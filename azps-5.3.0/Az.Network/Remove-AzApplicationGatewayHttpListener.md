---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C90AF6C-3193-4D75-A78F-3EC315C6D7DF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 81b750188a85add491e519c023c765f302e31dea
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486715"
---
# <span data-ttu-id="4c255-101">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4c255-101">Remove-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="4c255-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4c255-102">SYNOPSIS</span></span>
<span data-ttu-id="4c255-103">Rimuove un listener HTTP da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4c255-103">Removes an HTTP listener from an application gateway.</span></span>

## <span data-ttu-id="4c255-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4c255-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListener -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c255-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4c255-105">DESCRIPTION</span></span>
<span data-ttu-id="4c255-106">Il cmdlet **Remove-AzApplicationGatewayHttpListener** rimuove un listener HTTP da un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="4c255-106">The **Remove-AzApplicationGatewayHttpListener** cmdlet removes an HTTP listener from an Azure application gateway.</span></span>

## <span data-ttu-id="4c255-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4c255-107">EXAMPLES</span></span>

### <span data-ttu-id="4c255-108">Esempio 1: rimuovere un listener HTTP gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="4c255-108">Example 1: Remove an application gateway HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener02"
```

<span data-ttu-id="4c255-109">Il primo comando ottiene un gateway dell'applicazione e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="4c255-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="4c255-110">Il secondo comando rimuove il listener HTTP denominato Listener02 dal gateway dell'applicazione archiviato in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="4c255-110">The second command removes the HTTP listener named Listener02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="4c255-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4c255-111">PARAMETERS</span></span>

### <span data-ttu-id="4c255-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4c255-112">-ApplicationGateway</span></span>
<span data-ttu-id="4c255-113">Specifica il gateway dell'applicazione da cui rimuovere un listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="4c255-113">Specifies the application gateway from which to remove an HTTP listener.</span></span>

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

### <span data-ttu-id="4c255-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c255-114">-DefaultProfile</span></span>
<span data-ttu-id="4c255-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4c255-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c255-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="4c255-116">-Name</span></span>
<span data-ttu-id="4c255-117">Specifica il nome del listener HTTP rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c255-117">Specifies the name of the HTTP listener that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4c255-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c255-118">CommonParameters</span></span>
<span data-ttu-id="4c255-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c255-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c255-120">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c255-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c255-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4c255-121">INPUTS</span></span>

### <span data-ttu-id="4c255-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4c255-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4c255-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4c255-123">OUTPUTS</span></span>

### <span data-ttu-id="4c255-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4c255-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="4c255-125">Note</span><span class="sxs-lookup"><span data-stu-id="4c255-125">NOTES</span></span>

## <span data-ttu-id="4c255-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4c255-126">RELATED LINKS</span></span>

[<span data-ttu-id="4c255-127">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4c255-127">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="4c255-128">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4c255-128">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="4c255-129">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4c255-129">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="4c255-130">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4c255-130">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


