---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4518D2A9-7DE7-4617-86E0-7778B8CFE48C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 404a9ff22f6b6af480e167c5a4f958b9ac4b5d52
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203465"
---
# <span data-ttu-id="858d1-101">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="858d1-101">Get-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="858d1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="858d1-102">SYNOPSIS</span></span>
<span data-ttu-id="858d1-103">Ottiene la porta front-end di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="858d1-103">Gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="858d1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="858d1-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFrontendPort [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="858d1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="858d1-105">DESCRIPTION</span></span>
<span data-ttu-id="858d1-106">Il cmdlet **Get-AzApplicationGatewayFrontendPort** ottiene la porta front-end di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="858d1-106">The **Get-AzApplicationGatewayFrontendPort** cmdlet gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="858d1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="858d1-107">EXAMPLES</span></span>

### <span data-ttu-id="858d1-108">Esempio 1: ottenere una porta front-end specificata</span><span class="sxs-lookup"><span data-stu-id="858d1-108">Example 1: Get a specified front-end port</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPort = Get-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -ApplicationGateway $AppGw
```

<span data-ttu-id="858d1-109">Il primo comando ottiene un gateway dell'applicazione denominato ApplicationGateway01 dal gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="858d1-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="858d1-110">Il secondo comando ottiene la porta front-end denominata FrontEndPort01 da $AppGw e la archivia nella variabile $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="858d1-110">The second command gets the front-end port named FrontEndPort01 from $AppGw and stores it in the $FrontEndPort variable.</span></span>

### <span data-ttu-id="858d1-111">Esempio 2: ottenere un elenco di porte front-end</span><span class="sxs-lookup"><span data-stu-id="858d1-111">Example 2: Get a list of front-end ports</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPorts = Get-AzApplicationGatewayFrontendPort  -ApplicationGateway $AppGw
```

<span data-ttu-id="858d1-112">Il primo comando ottiene un gateway dell'applicazione denominato ApplicationGateway01 dal gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="858d1-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="858d1-113">Il secondo comando ottiene un elenco delle porte front-end da $AppGw e lo archivia nella variabile $FrontEndPorts.</span><span class="sxs-lookup"><span data-stu-id="858d1-113">The second command gets a list of the front-end ports from $AppGw and stores it in the $FrontEndPorts variable.</span></span>

## <span data-ttu-id="858d1-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="858d1-114">PARAMETERS</span></span>

### <span data-ttu-id="858d1-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="858d1-115">-ApplicationGateway</span></span>
<span data-ttu-id="858d1-116">Specifica l'oggetto gateway dell'applicazione che contiene la porta front-end.</span><span class="sxs-lookup"><span data-stu-id="858d1-116">Specifies the application gateway object that contains the front-end port.</span></span>

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

### <span data-ttu-id="858d1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="858d1-117">-DefaultProfile</span></span>
<span data-ttu-id="858d1-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="858d1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="858d1-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="858d1-119">-Name</span></span>
<span data-ttu-id="858d1-120">Specifica il nome della porta front-end da ottenere.</span><span class="sxs-lookup"><span data-stu-id="858d1-120">Specifies the name of the front-end port to get.</span></span>

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

### <span data-ttu-id="858d1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="858d1-121">CommonParameters</span></span>
<span data-ttu-id="858d1-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="858d1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="858d1-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="858d1-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="858d1-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="858d1-124">INPUTS</span></span>

### <span data-ttu-id="858d1-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="858d1-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="858d1-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="858d1-126">OUTPUTS</span></span>

### <span data-ttu-id="858d1-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="858d1-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="858d1-128">Note</span><span class="sxs-lookup"><span data-stu-id="858d1-128">NOTES</span></span>

## <span data-ttu-id="858d1-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="858d1-129">RELATED LINKS</span></span>

[<span data-ttu-id="858d1-130">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="858d1-130">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="858d1-131">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="858d1-131">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="858d1-132">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="858d1-132">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="858d1-133">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="858d1-133">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


