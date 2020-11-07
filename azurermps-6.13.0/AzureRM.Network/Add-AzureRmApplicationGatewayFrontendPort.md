---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 40198C86-A4EB-494A-86D5-DF632518EB95
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayFrontendPort.md
ms.openlocfilehash: 81952db3ce99ea41388d85085d58a2fb54ccc63f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520185"
---
# <span data-ttu-id="8a799-101">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="8a799-101">Add-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="8a799-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8a799-102">SYNOPSIS</span></span>
<span data-ttu-id="8a799-103">Aggiunge una porta front-end a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8a799-103">Adds a front-end port to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a799-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8a799-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a799-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8a799-105">DESCRIPTION</span></span>
<span data-ttu-id="8a799-106">Il cmdlet **Add-AzureRmApplicationGatewayFrontendPort** aggiunge una porta front-end a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8a799-106">The **Add-AzureRmApplicationGatewayFrontendPort** cmdlet adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="8a799-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8a799-107">EXAMPLES</span></span>

### <span data-ttu-id="8a799-108">Esempio 1: aggiungere una porta front-end a un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="8a799-108">Example 1: Add a front-end port to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="8a799-109">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="8a799-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="8a799-110">Il secondo comando aggiunge la porta 80 come porta front-end per il gateway dell'applicazione archiviata in $AppGw e denomina la porta FrontEndPort01.</span><span class="sxs-lookup"><span data-stu-id="8a799-110">The second command adds port 80 as a front-end port for the application gateway stored in $AppGw and names the port FrontEndPort01.</span></span>

## <span data-ttu-id="8a799-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8a799-111">PARAMETERS</span></span>

### <span data-ttu-id="8a799-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8a799-112">-ApplicationGateway</span></span>
<span data-ttu-id="8a799-113">Specifica il gateway dell'applicazione a cui questo cmdlet aggiunge una porta front-end.</span><span class="sxs-lookup"><span data-stu-id="8a799-113">Specifies the application gateway to which this cmdlet adds a front-end port.</span></span>

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

### <span data-ttu-id="8a799-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a799-114">-DefaultProfile</span></span>
<span data-ttu-id="8a799-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8a799-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a799-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="8a799-116">-Name</span></span>
<span data-ttu-id="8a799-117">Specifica il nome della porta front-end.</span><span class="sxs-lookup"><span data-stu-id="8a799-117">Specifies the name of the front-end port.</span></span>

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

### <span data-ttu-id="8a799-118">-Porta</span><span class="sxs-lookup"><span data-stu-id="8a799-118">-Port</span></span>
<span data-ttu-id="8a799-119">Specifica il numero di porta.</span><span class="sxs-lookup"><span data-stu-id="8a799-119">Specifies the port number.</span></span>

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

### <span data-ttu-id="8a799-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a799-120">CommonParameters</span></span>
<span data-ttu-id="8a799-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a799-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a799-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a799-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a799-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8a799-123">INPUTS</span></span>

### <span data-ttu-id="8a799-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8a799-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="8a799-125">Parametri: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8a799-125">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="8a799-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8a799-126">OUTPUTS</span></span>

### <span data-ttu-id="8a799-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8a799-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8a799-128">Note</span><span class="sxs-lookup"><span data-stu-id="8a799-128">NOTES</span></span>

## <span data-ttu-id="8a799-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8a799-129">RELATED LINKS</span></span>

[<span data-ttu-id="8a799-130">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="8a799-130">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="8a799-131">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="8a799-131">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="8a799-132">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="8a799-132">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="8a799-133">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="8a799-133">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)

