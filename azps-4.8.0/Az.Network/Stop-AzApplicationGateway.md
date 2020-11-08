---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzApplicationGateway.md
ms.openlocfilehash: 4c7001bf69e6dc8f418f1bc56867154bf9d769ce
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188358"
---
# <span data-ttu-id="0ca14-101">Stop-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0ca14-101">Stop-AzApplicationGateway</span></span>

## <span data-ttu-id="0ca14-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0ca14-102">SYNOPSIS</span></span>
<span data-ttu-id="0ca14-103">Interrompe un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="0ca14-103">Stops an application gateway</span></span>

## <span data-ttu-id="0ca14-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0ca14-104">SYNTAX</span></span>

```
Stop-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ca14-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0ca14-105">DESCRIPTION</span></span>
<span data-ttu-id="0ca14-106">Il cmdlet **Stop-AzApplicationGateway** arresta un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0ca14-106">The **Stop-AzApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="0ca14-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0ca14-107">EXAMPLES</span></span>

### <span data-ttu-id="0ca14-108">Esempio 1: arrestare un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="0ca14-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="0ca14-109">Questo comando Arresta il gateway dell'applicazione archiviato nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="0ca14-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="0ca14-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0ca14-110">PARAMETERS</span></span>

### <span data-ttu-id="0ca14-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0ca14-111">-ApplicationGateway</span></span>
<span data-ttu-id="0ca14-112">Specifica il gateway dell'applicazione che questo cmdlet si arresta.</span><span class="sxs-lookup"><span data-stu-id="0ca14-112">Specifies the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="0ca14-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0ca14-113">-AsJob</span></span>
<span data-ttu-id="0ca14-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="0ca14-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ca14-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ca14-115">-DefaultProfile</span></span>
<span data-ttu-id="0ca14-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0ca14-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ca14-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ca14-117">CommonParameters</span></span>
<span data-ttu-id="0ca14-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ca14-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ca14-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ca14-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ca14-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0ca14-120">INPUTS</span></span>

### <span data-ttu-id="0ca14-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0ca14-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0ca14-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0ca14-122">OUTPUTS</span></span>

### <span data-ttu-id="0ca14-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0ca14-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0ca14-124">Note</span><span class="sxs-lookup"><span data-stu-id="0ca14-124">NOTES</span></span>

## <span data-ttu-id="0ca14-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0ca14-125">RELATED LINKS</span></span>

[<span data-ttu-id="0ca14-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0ca14-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="0ca14-127">New-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0ca14-127">New-AzApplicationGateway</span></span>](./New-AzApplicationGateway.md)

[<span data-ttu-id="0ca14-128">Remove-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0ca14-128">Remove-AzApplicationGateway</span></span>](./Remove-AzApplicationGateway.md)

[<span data-ttu-id="0ca14-129">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0ca14-129">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)

[<span data-ttu-id="0ca14-130">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0ca14-130">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


