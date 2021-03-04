---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: https://docs.microsoft.com/powershell/module/az.network/stop-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzApplicationGateway.md
ms.openlocfilehash: 0cf179bf02c8590bd5c5e30277c7299c7b13b06b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951869"
---
# <span data-ttu-id="4210c-101">Stop-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4210c-101">Stop-AzApplicationGateway</span></span>

## <span data-ttu-id="4210c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4210c-102">SYNOPSIS</span></span>
<span data-ttu-id="4210c-103">Arresta un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="4210c-103">Stops an application gateway</span></span>

## <span data-ttu-id="4210c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4210c-104">SYNTAX</span></span>

```
Stop-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4210c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4210c-105">DESCRIPTION</span></span>
<span data-ttu-id="4210c-106">Il cmdlet **Stop-AzApplicationGateway** interrompe un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="4210c-106">The **Stop-AzApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="4210c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4210c-107">EXAMPLES</span></span>

### <span data-ttu-id="4210c-108">Esempio 1: Arrestare un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="4210c-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="4210c-109">Questo comando interrompe l'archiviazione del gateway applicazione nella $AppGw variabile.</span><span class="sxs-lookup"><span data-stu-id="4210c-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="4210c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4210c-110">PARAMETERS</span></span>

### <span data-ttu-id="4210c-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4210c-111">-ApplicationGateway</span></span>
<span data-ttu-id="4210c-112">Specifica il gateway applicazione arrestato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4210c-112">Specifies the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="4210c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4210c-113">-AsJob</span></span>
<span data-ttu-id="4210c-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="4210c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4210c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4210c-115">-DefaultProfile</span></span>
<span data-ttu-id="4210c-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4210c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4210c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4210c-117">CommonParameters</span></span>
<span data-ttu-id="4210c-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4210c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4210c-119">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4210c-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4210c-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="4210c-120">INPUTS</span></span>

### <span data-ttu-id="4210c-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4210c-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4210c-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4210c-122">OUTPUTS</span></span>

### <span data-ttu-id="4210c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4210c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4210c-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="4210c-124">NOTES</span></span>

## <span data-ttu-id="4210c-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4210c-125">RELATED LINKS</span></span>

[<span data-ttu-id="4210c-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4210c-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="4210c-127">New-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4210c-127">New-AzApplicationGateway</span></span>](./New-AzApplicationGateway.md)

[<span data-ttu-id="4210c-128">Remove-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4210c-128">Remove-AzApplicationGateway</span></span>](./Remove-AzApplicationGateway.md)

[<span data-ttu-id="4210c-129">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4210c-129">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)

[<span data-ttu-id="4210c-130">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4210c-130">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


