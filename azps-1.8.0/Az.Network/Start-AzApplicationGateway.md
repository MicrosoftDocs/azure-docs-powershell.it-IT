---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
ms.openlocfilehash: f90e35e0b8a88d7fa7b5089adf205bf6fe14e18f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677904"
---
# <span data-ttu-id="4bb9f-101">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4bb9f-101">Start-AzApplicationGateway</span></span>

## <span data-ttu-id="4bb9f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4bb9f-102">SYNOPSIS</span></span>
<span data-ttu-id="4bb9f-103">Avvia un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4bb9f-103">Starts an application gateway.</span></span>

## <span data-ttu-id="4bb9f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4bb9f-104">SYNTAX</span></span>

```
Start-AzApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4bb9f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4bb9f-105">DESCRIPTION</span></span>
<span data-ttu-id="4bb9f-106">Il cmdlet **Start-AzApplicationGateway** avvia un gateway dell'applicazione Azure</span><span class="sxs-lookup"><span data-stu-id="4bb9f-106">The **Start-AzApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="4bb9f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4bb9f-107">EXAMPLES</span></span>

### <span data-ttu-id="4bb9f-108">Esempio1: avviare un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="4bb9f-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="4bb9f-109">Questo comando avvia il gateway dell'applicazione archiviato nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="4bb9f-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="4bb9f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4bb9f-110">PARAMETERS</span></span>

### <span data-ttu-id="4bb9f-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4bb9f-111">-ApplicationGateway</span></span>
<span data-ttu-id="4bb9f-112">Specifica il gateway dell'applicazione avviato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4bb9f-112">Specifies the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="4bb9f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bb9f-113">-DefaultProfile</span></span>
<span data-ttu-id="4bb9f-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4bb9f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4bb9f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bb9f-115">CommonParameters</span></span>
<span data-ttu-id="4bb9f-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bb9f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bb9f-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bb9f-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bb9f-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4bb9f-118">INPUTS</span></span>

### <span data-ttu-id="4bb9f-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4bb9f-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4bb9f-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4bb9f-120">OUTPUTS</span></span>

### <span data-ttu-id="4bb9f-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4bb9f-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4bb9f-122">Note</span><span class="sxs-lookup"><span data-stu-id="4bb9f-122">NOTES</span></span>

## <span data-ttu-id="4bb9f-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4bb9f-123">RELATED LINKS</span></span>

[<span data-ttu-id="4bb9f-124">Stop-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4bb9f-124">Stop-AzApplicationGateway</span></span>](./Stop-AzApplicationGateway.md)


