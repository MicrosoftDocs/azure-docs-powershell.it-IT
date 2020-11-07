---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmApplicationGateway.md
ms.openlocfilehash: 2faa1b245a38a5ef66bb5131f79000218c39d55c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519893"
---
# <span data-ttu-id="a03a1-101">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a03a1-101">Start-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="a03a1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a03a1-102">SYNOPSIS</span></span>
<span data-ttu-id="a03a1-103">Avvia un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a03a1-103">Starts an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a03a1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a03a1-104">SYNTAX</span></span>

```
Start-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a03a1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a03a1-105">DESCRIPTION</span></span>
<span data-ttu-id="a03a1-106">Il cmdlet **Start-AzureRmApplicationGateway** avvia un gateway dell'applicazione Azure</span><span class="sxs-lookup"><span data-stu-id="a03a1-106">The **Start-AzureRmApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="a03a1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a03a1-107">EXAMPLES</span></span>

### <span data-ttu-id="a03a1-108">Esempio1: avviare un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="a03a1-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="a03a1-109">Questo comando avvia il gateway dell'applicazione archiviato nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="a03a1-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="a03a1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a03a1-110">PARAMETERS</span></span>

### <span data-ttu-id="a03a1-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a03a1-111">-ApplicationGateway</span></span>
<span data-ttu-id="a03a1-112">Specifica il gateway dell'applicazione avviato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a03a1-112">Specifies the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="a03a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a03a1-113">-DefaultProfile</span></span>
<span data-ttu-id="a03a1-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a03a1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a03a1-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a03a1-115">CommonParameters</span></span>
<span data-ttu-id="a03a1-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a03a1-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a03a1-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a03a1-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a03a1-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a03a1-118">INPUTS</span></span>

### <span data-ttu-id="a03a1-119">System. String</span><span class="sxs-lookup"><span data-stu-id="a03a1-119">System.String</span></span>

## <span data-ttu-id="a03a1-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a03a1-120">OUTPUTS</span></span>

### <span data-ttu-id="a03a1-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a03a1-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a03a1-122">Note</span><span class="sxs-lookup"><span data-stu-id="a03a1-122">NOTES</span></span>

## <span data-ttu-id="a03a1-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a03a1-123">RELATED LINKS</span></span>

[<span data-ttu-id="a03a1-124">Stop-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a03a1-124">Stop-AzureRmApplicationGateway</span></span>](./Stop-AzureRmApplicationGateway.md)

