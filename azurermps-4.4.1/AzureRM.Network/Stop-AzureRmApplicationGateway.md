---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmApplicationGateway.md
ms.openlocfilehash: 6c2de883a797c445105edddfc562bc2d494fd234
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510415"
---
# <span data-ttu-id="e6719-101">Stop-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e6719-101">Stop-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="e6719-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e6719-102">SYNOPSIS</span></span>
<span data-ttu-id="e6719-103">Interrompe un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="e6719-103">Stops an application gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6719-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e6719-104">SYNTAX</span></span>

```
Stop-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6719-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e6719-105">DESCRIPTION</span></span>
<span data-ttu-id="e6719-106">Il cmdlet **Stop-AzureRmApplicationGateway** arresta un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e6719-106">The **Stop-AzureRmApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="e6719-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e6719-107">EXAMPLES</span></span>

### <span data-ttu-id="e6719-108">Esempio 1: arrestare un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="e6719-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="e6719-109">Questo comando Arresta il gateway dell'applicazione archiviato nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="e6719-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="e6719-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e6719-110">PARAMETERS</span></span>

### <span data-ttu-id="e6719-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e6719-111">-ApplicationGateway</span></span>
<span data-ttu-id="e6719-112">Specifica il gateway dell'applicazione che questo cmdlet si arresta.</span><span class="sxs-lookup"><span data-stu-id="e6719-112">Specifies the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="e6719-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6719-113">-DefaultProfile</span></span>
<span data-ttu-id="e6719-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e6719-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6719-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6719-115">CommonParameters</span></span>
<span data-ttu-id="e6719-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6719-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6719-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6719-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6719-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e6719-118">INPUTS</span></span>

### <span data-ttu-id="e6719-119">System. String</span><span class="sxs-lookup"><span data-stu-id="e6719-119">System.String</span></span>

## <span data-ttu-id="e6719-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e6719-120">OUTPUTS</span></span>

### <span data-ttu-id="e6719-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e6719-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e6719-122">Note</span><span class="sxs-lookup"><span data-stu-id="e6719-122">NOTES</span></span>

## <span data-ttu-id="e6719-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e6719-123">RELATED LINKS</span></span>

[<span data-ttu-id="e6719-124">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e6719-124">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="e6719-125">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e6719-125">New-AzureRmApplicationGateway</span></span>](./New-AzureRmApplicationGateway.md)

[<span data-ttu-id="e6719-126">Remove-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e6719-126">Remove-AzureRmApplicationGateway</span></span>](./Remove-AzureRmApplicationGateway.md)

[<span data-ttu-id="e6719-127">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e6719-127">Set-AzureRmApplicationGateway</span></span>](./Set-AzureRmApplicationGateway.md)

[<span data-ttu-id="e6719-128">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e6719-128">Start-AzureRmApplicationGateway</span></span>](./Start-AzureRmApplicationGateway.md)


