---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40198C86-A4EB-494A-86D5-DF632518EB95
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 5926b2fb4b97d42ff8743ad227fdfb1b32326a20
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967966"
---
# <span data-ttu-id="62e25-101">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="62e25-101">Add-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="62e25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62e25-102">SYNOPSIS</span></span>
<span data-ttu-id="62e25-103">Aggiunge una porta front-end a un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="62e25-103">Adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="62e25-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="62e25-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62e25-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="62e25-105">DESCRIPTION</span></span>
<span data-ttu-id="62e25-106">Il cmdlet **Add-AzApplicationGatewayFrontendPort** aggiunge una porta front-end a un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="62e25-106">The **Add-AzApplicationGatewayFrontendPort** cmdlet adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="62e25-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="62e25-107">EXAMPLES</span></span>

### <span data-ttu-id="62e25-108">Esempio 1: Aggiungere una porta front-end a un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="62e25-108">Example 1: Add a front-end port to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="62e25-109">Il primo comando recupera il gateway applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella $AppGw variabile.</span><span class="sxs-lookup"><span data-stu-id="62e25-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="62e25-110">Il secondo comando aggiunge la porta 80 come porta front-end per il gateway applicazione archiviata in $AppGw e la porta FrontEndPort01.</span><span class="sxs-lookup"><span data-stu-id="62e25-110">The second command adds port 80 as a front-end port for the application gateway stored in $AppGw and names the port FrontEndPort01.</span></span>

## <span data-ttu-id="62e25-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62e25-111">PARAMETERS</span></span>

### <span data-ttu-id="62e25-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="62e25-112">-ApplicationGateway</span></span>
<span data-ttu-id="62e25-113">Specifica il gateway applicazione a cui questo cmdlet aggiunge una porta front-end.</span><span class="sxs-lookup"><span data-stu-id="62e25-113">Specifies the application gateway to which this cmdlet adds a front-end port.</span></span>

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

### <span data-ttu-id="62e25-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62e25-114">-DefaultProfile</span></span>
<span data-ttu-id="62e25-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="62e25-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62e25-116">-Name</span><span class="sxs-lookup"><span data-stu-id="62e25-116">-Name</span></span>
<span data-ttu-id="62e25-117">Specifica il nome della porta front-end.</span><span class="sxs-lookup"><span data-stu-id="62e25-117">Specifies the name of the front-end port.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62e25-118">-Porta</span><span class="sxs-lookup"><span data-stu-id="62e25-118">-Port</span></span>
<span data-ttu-id="62e25-119">Specifica il numero di porta.</span><span class="sxs-lookup"><span data-stu-id="62e25-119">Specifies the port number.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62e25-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62e25-120">CommonParameters</span></span>
<span data-ttu-id="62e25-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62e25-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62e25-122">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62e25-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62e25-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="62e25-123">INPUTS</span></span>

### <span data-ttu-id="62e25-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="62e25-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="62e25-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="62e25-125">OUTPUTS</span></span>

### <span data-ttu-id="62e25-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="62e25-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="62e25-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="62e25-127">NOTES</span></span>

## <span data-ttu-id="62e25-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="62e25-128">RELATED LINKS</span></span>

[<span data-ttu-id="62e25-129">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="62e25-129">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="62e25-130">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="62e25-130">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="62e25-131">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="62e25-131">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="62e25-132">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="62e25-132">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


