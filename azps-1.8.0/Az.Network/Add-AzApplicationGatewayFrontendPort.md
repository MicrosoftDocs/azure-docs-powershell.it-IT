---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40198C86-A4EB-494A-86D5-DF632518EB95
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 9eaaa8ae6ec4be7a1096bfd9de4a3e20c0cb5ff1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678702"
---
# <span data-ttu-id="ac9c6-101">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="ac9c6-101">Add-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="ac9c6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ac9c6-102">SYNOPSIS</span></span>
<span data-ttu-id="ac9c6-103">Aggiunge una porta front-end a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ac9c6-103">Adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="ac9c6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ac9c6-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac9c6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ac9c6-105">DESCRIPTION</span></span>
<span data-ttu-id="ac9c6-106">Il cmdlet **Add-AzApplicationGatewayFrontendPort** aggiunge una porta front-end a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ac9c6-106">The **Add-AzApplicationGatewayFrontendPort** cmdlet adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="ac9c6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ac9c6-107">EXAMPLES</span></span>

### <span data-ttu-id="ac9c6-108">Esempio 1: aggiungere una porta front-end a un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="ac9c6-108">Example 1: Add a front-end port to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="ac9c6-109">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="ac9c6-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="ac9c6-110">Il secondo comando aggiunge la porta 80 come porta front-end per il gateway dell'applicazione archiviata in $AppGw e denomina la porta FrontEndPort01.</span><span class="sxs-lookup"><span data-stu-id="ac9c6-110">The second command adds port 80 as a front-end port for the application gateway stored in $AppGw and names the port FrontEndPort01.</span></span>

## <span data-ttu-id="ac9c6-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ac9c6-111">PARAMETERS</span></span>

### <span data-ttu-id="ac9c6-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ac9c6-112">-ApplicationGateway</span></span>
<span data-ttu-id="ac9c6-113">Specifica il gateway dell'applicazione a cui questo cmdlet aggiunge una porta front-end.</span><span class="sxs-lookup"><span data-stu-id="ac9c6-113">Specifies the application gateway to which this cmdlet adds a front-end port.</span></span>

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

### <span data-ttu-id="ac9c6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac9c6-114">-DefaultProfile</span></span>
<span data-ttu-id="ac9c6-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ac9c6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac9c6-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="ac9c6-116">-Name</span></span>
<span data-ttu-id="ac9c6-117">Specifica il nome della porta front-end.</span><span class="sxs-lookup"><span data-stu-id="ac9c6-117">Specifies the name of the front-end port.</span></span>

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

### <span data-ttu-id="ac9c6-118">-Porta</span><span class="sxs-lookup"><span data-stu-id="ac9c6-118">-Port</span></span>
<span data-ttu-id="ac9c6-119">Specifica il numero di porta.</span><span class="sxs-lookup"><span data-stu-id="ac9c6-119">Specifies the port number.</span></span>

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

### <span data-ttu-id="ac9c6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac9c6-120">CommonParameters</span></span>
<span data-ttu-id="ac9c6-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac9c6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac9c6-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac9c6-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac9c6-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ac9c6-123">INPUTS</span></span>

### <span data-ttu-id="ac9c6-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ac9c6-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ac9c6-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ac9c6-125">OUTPUTS</span></span>

### <span data-ttu-id="ac9c6-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ac9c6-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ac9c6-127">Note</span><span class="sxs-lookup"><span data-stu-id="ac9c6-127">NOTES</span></span>

## <span data-ttu-id="ac9c6-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ac9c6-128">RELATED LINKS</span></span>

[<span data-ttu-id="ac9c6-129">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="ac9c6-129">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="ac9c6-130">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="ac9c6-130">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="ac9c6-131">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="ac9c6-131">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="ac9c6-132">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="ac9c6-132">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


