---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/powershell/module/az.network/start-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
ms.openlocfilehash: 4d2f3f225e185678dd1e3b0047810a5e68d4273f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951998"
---
# <span data-ttu-id="be3d6-101">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="be3d6-101">Start-AzApplicationGateway</span></span>

## <span data-ttu-id="be3d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be3d6-102">SYNOPSIS</span></span>
<span data-ttu-id="be3d6-103">Avvia un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="be3d6-103">Starts an application gateway.</span></span>

## <span data-ttu-id="be3d6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="be3d6-104">SYNTAX</span></span>

```
Start-AzApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be3d6-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="be3d6-105">DESCRIPTION</span></span>
<span data-ttu-id="be3d6-106">Il cmdlet **Start-AzApplicationGateway** avvia un gateway applicazione di Azure</span><span class="sxs-lookup"><span data-stu-id="be3d6-106">The **Start-AzApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="be3d6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="be3d6-107">EXAMPLES</span></span>

### <span data-ttu-id="be3d6-108">Esempio1: Avviare un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="be3d6-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="be3d6-109">Questo comando avvia il gateway applicazione archiviato nella variabile $AppGw variabile.</span><span class="sxs-lookup"><span data-stu-id="be3d6-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="be3d6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be3d6-110">PARAMETERS</span></span>

### <span data-ttu-id="be3d6-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="be3d6-111">-ApplicationGateway</span></span>
<span data-ttu-id="be3d6-112">Specifica il gateway applicazione che viene avviato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be3d6-112">Specifies the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="be3d6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be3d6-113">-DefaultProfile</span></span>
<span data-ttu-id="be3d6-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="be3d6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be3d6-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be3d6-115">CommonParameters</span></span>
<span data-ttu-id="be3d6-116">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be3d6-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be3d6-117">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be3d6-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be3d6-118">INPUT</span><span class="sxs-lookup"><span data-stu-id="be3d6-118">INPUTS</span></span>

### <span data-ttu-id="be3d6-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="be3d6-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="be3d6-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="be3d6-120">OUTPUTS</span></span>

### <span data-ttu-id="be3d6-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="be3d6-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="be3d6-122">NOTE</span><span class="sxs-lookup"><span data-stu-id="be3d6-122">NOTES</span></span>

## <span data-ttu-id="be3d6-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="be3d6-123">RELATED LINKS</span></span>

[<span data-ttu-id="be3d6-124">Stop-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="be3d6-124">Stop-AzApplicationGateway</span></span>](./Stop-AzApplicationGateway.md)


