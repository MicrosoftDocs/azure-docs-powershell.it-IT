---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermapplicationgateway
schema: 2.0.0
ms.openlocfilehash: 382c4cd1b189e0dc95edd4824dec58a280dbb889
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866644"
---
# <span data-ttu-id="3c073-101">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3c073-101">Start-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="3c073-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3c073-102">SYNOPSIS</span></span>
<span data-ttu-id="3c073-103">Avvia un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3c073-103">Starts an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c073-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3c073-104">SYNTAX</span></span>

```
Start-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c073-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c073-105">DESCRIPTION</span></span>
<span data-ttu-id="3c073-106">Il cmdlet **Start-AzureRmApplicationGateway** avvia un gateway dell'applicazione Azure</span><span class="sxs-lookup"><span data-stu-id="3c073-106">The **Start-AzureRmApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="3c073-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3c073-107">EXAMPLES</span></span>

### <span data-ttu-id="3c073-108">Esempio1: avviare un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="3c073-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="3c073-109">Questo comando avvia il gateway dell'applicazione archiviato nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="3c073-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="3c073-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3c073-110">PARAMETERS</span></span>

### <span data-ttu-id="3c073-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3c073-111">-ApplicationGateway</span></span>
<span data-ttu-id="3c073-112">Specifica il gateway dell'applicazione avviato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c073-112">Specifies the application gateway that this cmdlet starts.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c073-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c073-113">-DefaultProfile</span></span>
<span data-ttu-id="3c073-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3c073-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c073-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c073-115">CommonParameters</span></span>
<span data-ttu-id="3c073-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c073-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c073-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c073-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c073-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3c073-118">INPUTS</span></span>

### <span data-ttu-id="3c073-119">System. String</span><span class="sxs-lookup"><span data-stu-id="3c073-119">System.String</span></span>

## <span data-ttu-id="3c073-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3c073-120">OUTPUTS</span></span>

### <span data-ttu-id="3c073-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3c073-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3c073-122">Note</span><span class="sxs-lookup"><span data-stu-id="3c073-122">NOTES</span></span>

## <span data-ttu-id="3c073-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3c073-123">RELATED LINKS</span></span>

[<span data-ttu-id="3c073-124">Stop-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3c073-124">Stop-AzureRmApplicationGateway</span></span>](./Stop-AzureRmApplicationGateway.md)


