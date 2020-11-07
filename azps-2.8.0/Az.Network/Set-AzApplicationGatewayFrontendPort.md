---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 85C0A1C3-FC6D-496A-B6B5-8DC2A73B8032
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: cdc1535532aad26ad4e3ee67e5fdd822ee3480e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852649"
---
# <span data-ttu-id="f53b2-101">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="f53b2-101">Set-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="f53b2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f53b2-102">SYNOPSIS</span></span>
<span data-ttu-id="f53b2-103">Modifica una porta front-end per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f53b2-103">Modifies a front-end port for an application gateway.</span></span>

## <span data-ttu-id="f53b2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f53b2-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f53b2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f53b2-105">DESCRIPTION</span></span>
<span data-ttu-id="f53b2-106">Il cmdlet **set-AzApplicationGatewayFrontendPort** modifica una porta front-end per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f53b2-106">The **Set-AzApplicationGatewayFrontendPort** cmdlet modifies a front-end port for an application gateway.</span></span>

## <span data-ttu-id="f53b2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f53b2-107">EXAMPLES</span></span>

### <span data-ttu-id="f53b2-108">Esempio 1: impostare una porta di front-end gateway applicazione in 80</span><span class="sxs-lookup"><span data-stu-id="f53b2-108">Example 1: Set an application gateway front-end port to 80</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="f53b2-109">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="f53b2-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="f53b2-110">Il secondo comando modifica il gateway in $AppGw per usare la porta 80 per la porta front-end denominata FrontEndPort01.</span><span class="sxs-lookup"><span data-stu-id="f53b2-110">The second command modifies the gateway in $AppGw to use port 80 for the front-end port named FrontEndPort01.</span></span>

## <span data-ttu-id="f53b2-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f53b2-111">PARAMETERS</span></span>

### <span data-ttu-id="f53b2-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f53b2-112">-ApplicationGateway</span></span>
<span data-ttu-id="f53b2-113">Specifica l'oggetto gateway dell'applicazione con cui questo cmdlet associa la porta front-end.</span><span class="sxs-lookup"><span data-stu-id="f53b2-113">Specifies the application gateway object with which this cmdlet associates the front-end port.</span></span>

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

### <span data-ttu-id="f53b2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f53b2-114">-DefaultProfile</span></span>
<span data-ttu-id="f53b2-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f53b2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f53b2-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="f53b2-116">-Name</span></span>
<span data-ttu-id="f53b2-117">Specifica il nome della porta front-end da modificare.</span><span class="sxs-lookup"><span data-stu-id="f53b2-117">Specifies the name of the front-end port to modify.</span></span>

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

### <span data-ttu-id="f53b2-118">-Porta</span><span class="sxs-lookup"><span data-stu-id="f53b2-118">-Port</span></span>
<span data-ttu-id="f53b2-119">Specifica il numero di porta da usare per la porta front-end.</span><span class="sxs-lookup"><span data-stu-id="f53b2-119">Specifies the port number to use for the front-end port.</span></span>

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

### <span data-ttu-id="f53b2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f53b2-120">CommonParameters</span></span>
<span data-ttu-id="f53b2-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f53b2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f53b2-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f53b2-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f53b2-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f53b2-123">INPUTS</span></span>

### <span data-ttu-id="f53b2-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f53b2-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f53b2-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f53b2-125">OUTPUTS</span></span>

### <span data-ttu-id="f53b2-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f53b2-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f53b2-127">Note</span><span class="sxs-lookup"><span data-stu-id="f53b2-127">NOTES</span></span>

## <span data-ttu-id="f53b2-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f53b2-128">RELATED LINKS</span></span>

[<span data-ttu-id="f53b2-129">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="f53b2-129">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="f53b2-130">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="f53b2-130">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="f53b2-131">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="f53b2-131">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="f53b2-132">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="f53b2-132">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)
