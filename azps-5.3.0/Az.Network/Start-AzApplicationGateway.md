---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
ms.openlocfilehash: 974e30d9a287d18293515c019b0032bf36f15b51
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476469"
---
# <span data-ttu-id="7acf8-101">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7acf8-101">Start-AzApplicationGateway</span></span>

## <span data-ttu-id="7acf8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7acf8-102">SYNOPSIS</span></span>
<span data-ttu-id="7acf8-103">Avvia un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7acf8-103">Starts an application gateway.</span></span>

## <span data-ttu-id="7acf8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7acf8-104">SYNTAX</span></span>

```
Start-AzApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7acf8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7acf8-105">DESCRIPTION</span></span>
<span data-ttu-id="7acf8-106">Il cmdlet **Start-AzApplicationGateway** avvia un gateway dell'applicazione Azure</span><span class="sxs-lookup"><span data-stu-id="7acf8-106">The **Start-AzApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="7acf8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7acf8-107">EXAMPLES</span></span>

### <span data-ttu-id="7acf8-108">Esempio1: avviare un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="7acf8-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="7acf8-109">Questo comando avvia il gateway dell'applicazione archiviato nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="7acf8-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="7acf8-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7acf8-110">PARAMETERS</span></span>

### <span data-ttu-id="7acf8-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7acf8-111">-ApplicationGateway</span></span>
<span data-ttu-id="7acf8-112">Specifica il gateway dell'applicazione avviato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7acf8-112">Specifies the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="7acf8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7acf8-113">-DefaultProfile</span></span>
<span data-ttu-id="7acf8-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7acf8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7acf8-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7acf8-115">CommonParameters</span></span>
<span data-ttu-id="7acf8-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7acf8-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7acf8-117">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7acf8-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7acf8-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7acf8-118">INPUTS</span></span>

### <span data-ttu-id="7acf8-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7acf8-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7acf8-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7acf8-120">OUTPUTS</span></span>

### <span data-ttu-id="7acf8-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7acf8-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7acf8-122">Note</span><span class="sxs-lookup"><span data-stu-id="7acf8-122">NOTES</span></span>

## <span data-ttu-id="7acf8-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7acf8-123">RELATED LINKS</span></span>

[<span data-ttu-id="7acf8-124">Stop-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7acf8-124">Stop-AzApplicationGateway</span></span>](./Stop-AzApplicationGateway.md)


