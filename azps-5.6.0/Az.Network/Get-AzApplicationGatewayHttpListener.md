---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D41EDAC-17D9-494B-8336-67906F4E1E81
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: e849d4c7eaf007a6e2fd8d6cbbda1cc49cbf2fb0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996532"
---
# <span data-ttu-id="4134b-101">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4134b-101">Get-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="4134b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4134b-102">SYNOPSIS</span></span>
<span data-ttu-id="4134b-103">Ottiene il listener HTTP di un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="4134b-103">Gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="4134b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4134b-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayHttpListener [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4134b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4134b-105">DESCRIPTION</span></span>
<span data-ttu-id="4134b-106">Il cmdlet **Get-AzApplicationGatewayHttpHttpHttp Listener** ottiene il listener HTTP di un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="4134b-106">The **Get-AzApplicationGatewayHttpListener** cmdlet gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="4134b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4134b-107">EXAMPLES</span></span>

### <span data-ttu-id="4134b-108">Esempio 1: Ottenere un listener HTTP specifico</span><span class="sxs-lookup"><span data-stu-id="4134b-108">Example 1: Get a specific HTTP listener</span></span>
```
PS C:\>$Appgw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listener = Get-AzApplicationGatewayHttpListener -Name "Listener01" -ApplicationGateway $Appgw
```

<span data-ttu-id="4134b-109">Questo comando ottiene un listener HTTP denominato Listener01.</span><span class="sxs-lookup"><span data-stu-id="4134b-109">This command gets an HTTP listener named Listener01.</span></span>

### <span data-ttu-id="4134b-110">Esempio 2: Ottenere un elenco di listener HTTP</span><span class="sxs-lookup"><span data-stu-id="4134b-110">Example 2: Get a list of HTTP listeners</span></span>
```
PS C:\>$Appgw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listeners = Get-AzApplicationGatewayHttpListener -ApplicationGateway $Appgw
```

<span data-ttu-id="4134b-111">Questo comando ottiene un elenco di listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="4134b-111">This command gets a list of HTTP listeners.</span></span>

## <span data-ttu-id="4134b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4134b-112">PARAMETERS</span></span>

### <span data-ttu-id="4134b-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4134b-113">-ApplicationGateway</span></span>
<span data-ttu-id="4134b-114">Specifica l'oggetto gateway applicazione che contiene il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="4134b-114">Specifies the application gateway object that contains the HTTP listener.</span></span>

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

### <span data-ttu-id="4134b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4134b-115">-DefaultProfile</span></span>
<span data-ttu-id="4134b-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4134b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4134b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="4134b-117">-Name</span></span>
<span data-ttu-id="4134b-118">Specifica il nome del listener HTTP a cui viene eseguito il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4134b-118">Specifies the name of the HTTP listener which this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4134b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4134b-119">CommonParameters</span></span>
<span data-ttu-id="4134b-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4134b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4134b-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4134b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4134b-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="4134b-122">INPUTS</span></span>

### <span data-ttu-id="4134b-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4134b-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4134b-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4134b-124">OUTPUTS</span></span>

### <span data-ttu-id="4134b-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpHttpApplication</span><span class="sxs-lookup"><span data-stu-id="4134b-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="4134b-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="4134b-126">NOTES</span></span>

## <span data-ttu-id="4134b-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4134b-127">RELATED LINKS</span></span>

[<span data-ttu-id="4134b-128">Add-AzApplicationGatewayHttpHttp Più</span><span class="sxs-lookup"><span data-stu-id="4134b-128">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="4134b-129">New-AzApplicationGatewayHttpHttp Più</span><span class="sxs-lookup"><span data-stu-id="4134b-129">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="4134b-130">Remove-AzApplicationGatewayHttpHttp Più</span><span class="sxs-lookup"><span data-stu-id="4134b-130">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="4134b-131">Set-AzApplicationGatewayHttpHttp Più</span><span class="sxs-lookup"><span data-stu-id="4134b-131">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


