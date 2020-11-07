---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmApplicationGateway.md
ms.openlocfilehash: 88ca18eca50f1e68eab8599ad79f902ff1fd2551
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686252"
---
# <span data-ttu-id="d1240-101">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d1240-101">Start-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="d1240-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d1240-102">SYNOPSIS</span></span>
<span data-ttu-id="d1240-103">Avvia un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d1240-103">Starts an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1240-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d1240-104">SYNTAX</span></span>

```
Start-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1240-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d1240-105">DESCRIPTION</span></span>
<span data-ttu-id="d1240-106">Il cmdlet **Start-AzureRmApplicationGateway** avvia un gateway dell'applicazione Azure</span><span class="sxs-lookup"><span data-stu-id="d1240-106">The **Start-AzureRmApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="d1240-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d1240-107">EXAMPLES</span></span>

### <span data-ttu-id="d1240-108">Esempio1: avviare un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="d1240-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="d1240-109">Questo comando avvia il gateway dell'applicazione archiviato nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="d1240-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="d1240-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d1240-110">PARAMETERS</span></span>

### <span data-ttu-id="d1240-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d1240-111">-ApplicationGateway</span></span>
<span data-ttu-id="d1240-112">Specifica il gateway dell'applicazione avviato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1240-112">Specifies the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="d1240-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1240-113">-DefaultProfile</span></span>
<span data-ttu-id="d1240-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d1240-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1240-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1240-115">CommonParameters</span></span>
<span data-ttu-id="d1240-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1240-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1240-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1240-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1240-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d1240-118">INPUTS</span></span>

### <span data-ttu-id="d1240-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d1240-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="d1240-120">Parametri: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d1240-120">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="d1240-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d1240-121">OUTPUTS</span></span>

### <span data-ttu-id="d1240-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d1240-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d1240-123">Note</span><span class="sxs-lookup"><span data-stu-id="d1240-123">NOTES</span></span>

## <span data-ttu-id="d1240-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d1240-124">RELATED LINKS</span></span>

[<span data-ttu-id="d1240-125">Stop-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d1240-125">Stop-AzureRmApplicationGateway</span></span>](./Stop-AzureRmApplicationGateway.md)


